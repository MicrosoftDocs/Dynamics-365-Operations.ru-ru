---
title: Определение расположения пользовательского хранилища для создаваемых документов
description: В этой статье объясняется, как расширить список мест хранения для документов, формируемых в форматах электронной отчетности (ER).
author: kfend
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 83ee74cf590fe559ae18161d68b38dff54ab7fbc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268766"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Указание пользовательского места хранения для созданных документов

[!include[banner](../includes/banner.md)]

Интерфейс прикладного программирования (API) платформы электронной отчетности (ER) позволяет расширять список местоположения хранения для документов, формируемых форматами ER. Эта статья содержит обзор основных задач, которые необходимо выполнить для добавления пользовательского места хранения.

## <a name="prerequisites"></a>Необходимые условия

Необходимо развернуть топологию, которая поддерживает непрерывную сборку. (Дополнительные сведения см. в разделе [Развертывание топологий, поддерживающих непрерывную сборку и автоматизацию тестирования](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Необходимо иметь доступ к этой топологии для одной из следующих ролей:

- Разработчик электронной отчетности
- Консультант по функциональным возможностям электронной отчетности
- Системный администратор

Кроме того, необходим доступ к среде разработки для этой топологии.

## <a name="create-or-import-an-er-format-configuration"></a>Создание или импорт конфигурации формата электронной отчетности

В текущей топологии [создайте новый формат ER](tasks/er-format-configuration-2016-11.md) для создания документов, для которых планируется добавить пользовательское хранилище. Можно также [импортировать существующий формат ER в эту топологию](general-electronic-reporting-manage-configuration-lifecycle.md).

![Страница конструктора форматов.](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Формат ER, который вы создаете или импортируете, должен содержать хотя бы один из следующих элементов формата:
>
> - Хранилище файлов
> - Папка
> - Средство объединения
> - Вложение

## <a name="create-a-new-document-type"></a>Создание нового типа документов

Чтобы указать способ маршрутизации документов, создаваемых форматом ER, необходимо настроить [пункты назначения электронной отчетности (ER)](electronic-reporting-destinations.md). В каждом пункте назначения ER, настроенном для хранения созданных документов в виде файлов, необходимо указать тип документа платформы управления документами. Различные типы документов могут использоваться для маршрутизации документов, создаваемых различными форматами электронной отчетности.

1. Добавьте новый [тип документа](../../fin-ops/organization-administration/configure-document-management.md) в формат ER, созданный или импортированный ранее. На рисунке ниже тип документа — **FileX**.
2. Этот отличать этот тип документа от других типов документов, включите определенное ключевое слово в его имя. Например, на следующем рисунке задано имя **(ЛОКАЛЬНАЯ) папка**.
3. В поле **Класс** укажите **Вложить файл**.
4. В поле **Группа** укажите **Файл**.

![Страница типов документов.](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Типы документов зависят от конкретной компании. Чтобы использовать формат ER с настроенным пунктом назначения в нескольких компаниях, необходимо настроить тип отдельный тип документов в каждой компании.

## <a name="review-source-code"></a>Проверка исходного кода

Просмотрите код метода **insertFile()** класса **ERDocuManagement**. Обратите внимание, что событие **AttachingFile()** возникает, когда созданный файл присоединяется к записи.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

Событие **AttachingFile()** возникает, когда обрабатываются следующие пункты назначения электронной отчетности:

- **Архив** — при использовании этого пункта назначения новая запись для запущенного формата ER будет создана в таблице ERFormatMappingRunJobTable. Поле **Архивировано** в этой записи имеет значение **False**. Если формат электронной отчетности успешно выполняется, созданный документ присоединяется к этой записи и возникает событие **AttachingFile()**. Тип документа, который выбран в этом месте назначения ER, определяет место хранения для прикрепленного файла (хранилище Microsoft Azure Storage или папка Microsoft SharePoint).
- **Архив заданий** — при использовании этого пункта назначения новая запись для запущенного формата ER будет создана в таблице ERFormatMappingRunJobTable. Поле **Архивировано** в этой записи имеет значение **True**. Если формат электронной отчетности успешно выполняется, созданный документ присоединяется к этой записи и возникает событие **AttachingFile()**. Тип документа, который настроен в параметрах ER, определяет место хранения для прикрепленного файла (хранилище Azure Storage или папка SharePoint).

![Страница параметров электронной отчетности.](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Настройка места назначения ER

1. Настройте архивированное место назначения для одного из ранее упомянутых элементов (файл, папка, средство слияния или вложение) формата ER, который вы создали или импортировали. Указания см. в разделе [Электронная отчетность — Настройка мест назначений](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Используйте тип документа, который был добавлен ранее для сконфигурированного места назначения. (Например, в этой статье это тип документа **FileX**.)

![Диалоговое окно параметров места назначения.](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Изменение исходного кода

1. Добавьте новый класс в проект Microsoft Visual Studio и напишите код для подписки на событие **AttachingFile()**, которое упомянуто выше. (Дополнительные сведения об используемом шаблоне расширения см. в разделе [Ответ с использованием EventHandlerResult](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Например, в новом классе напишите код, который выполняет следующие действия:

    1. Сохраните созданные файлы в папке локальной файловой системы сервера, на котором выполняется служба Application Object Server (AOS).
    2. Сохраните эти созданные файлы только в том случае, когда используется тип нового документа(например, тип **FileX**, содержащий ключевое слово "(ЛОКАЛЬНЫЙ)" в имени), а файла прикреплен к записи в журнале задания выполнения электронной отчетности.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Заново выполните сборку проекта

## <a name="run-the-er-format-that-you-created-or-imported"></a>Запуск созданного или импортированного формата ER

1. Выполните созданный или импортированный формат ER.
2. Перейдите в раздел **Управление организацией \> Электронная отчетность \> Задания электронной отчетности**. Найдите запись, которая была создана для этого задания выполнения, и которая создала файл, прикрепленный к ней.
3. Выполните поиск в локальной папке **C:\\0**, чтобы найти такой созданный файл.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)
- [Домашняя страница расширяемости](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
