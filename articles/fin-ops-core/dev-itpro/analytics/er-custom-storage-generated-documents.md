---
title: Указание пользовательского места хранения для созданных документов
description: В этом разделе объясняется, как расширить список местоположения хранения для документов, формируемых форматами электронной отчетности (ER).
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: f65118b6a7393ced9d80c30fad7540a7b27da6c7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569092"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Указание пользовательского места хранения для созданных документов

[!include[banner](../includes/banner.md)]

Интерфейс прикладного программирования (API) платформы электронной отчетности (ER) позволяет расширять список местоположения хранения для документов, формируемых форматами ER. Этот раздел содержит обзор основных задач, которые необходимо выполнить для добавления пользовательского местоположения хранения.

## <a name="prerequisites"></a>Необходимые условия

Необходимо развернуть топологию, которая поддерживает непрерывную сборку. (Дополнительные сведения см. в разделе [Развертывание топологий, поддерживающих непрерывную сборку и автоматизацию тестирования](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Необходимо иметь доступ к этой топологии для одной из следующих ролей:

- Разработчик электронной отчетности
- Консультант по функциональным возможностям электронной отчетности
- Системный администратор

Кроме того, необходим доступ к среде разработки для этой топологии.

## <a name="create-or-import-an-er-format-configuration"></a>Создание или импорт конфигурации формата электронной отчетности

В текущей топологии [создайте новый формат ER](tasks/er-format-configuration-2016-11.md) для создания документов, для которых планируется добавить пользовательское хранилище. Можно также [импортировать существующий формат ER в эту топологию](general-electronic-reporting-manage-configuration-lifecycle.md).

![Страница конструктора форматов](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Формат ER, который вы создаете или импортируете, должен содержать хотя бы один из следующих элементов формата:
>
> - Хранилище файлов
> - Папка
> - Средство объединения
> - Вложение

## <a name="create-a-new-document-type"></a>Создание нового типа документов

Чтобы указать способ маршрутизации документов, создаваемых форматом ER, необходимо настроить [пункты назначения ER](electronic-reporting-destinations.md). В каждом пункте назначения ER, настроенном для хранения созданных документов в виде файлов, необходимо указать тип документа платформы управления документами. Различные типы документов могут использоваться для маршрутизации документов, создаваемых различными форматами электронной отчетности.

1. Добавьте новый [тип документа](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) в формат ER, созданный или импортированный ранее. На рисунке ниже тип документа — **FileX**.
2. Этот отличать этот тип документа от других типов документов, включите определенное ключевое слово в его имя. Например, на следующем рисунке задано имя **(ЛОКАЛЬНАЯ) папка**.
3. В поле **Класс** укажите **Вложить файл**.
4. В поле **Группа** укажите **Файл**.

![Страница типов документов](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Типы документов зависят от конкретной компании. Чтобы использовать формат ER с настроенным пунктом назначения в нескольких компаниях, необходимо настроить тип отдельный тип документов в каждой компании.

## <a name="review-source-code"></a>Проверка исходного кода

Просмотрите код метода **insertFile()** класса **ERDocuManagement**. Обратите внимание, что событие **AttachingFile()** возникает, когда созданный файл присоединяется к записи.

```
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

![Страница параметров электронной отчетности](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Настройка места назначения ER

1. Настройте архивированное место назначения для одного из ранее упомянутых элементов (файл, папка, средство слияния или вложение) формата ER, который вы создали или импортировали. Указания см. в разделе [Электронная отчетность — Настройка мест назначений](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Используйте тип документа, который был добавлен ранее для сконфигурированного места назначения. (Например, в этом разделе это тип документа **FileX**.)

![Диалоговое окно параметров места назначения](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Изменение исходного кода

1. Добавьте новый класс в проект Microsoft Visual Studio и напишите код для подписки на событие **AttachingFile()**, которое упомянуто выше. (Дополнительные сведения об используемом шаблоне расширения см. в разделе [Ответ с использованием EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Например, в новом классе напишите код, который выполняет следующие действия:

    1. Сохраните созданные файлы в папке локальной файловой системы сервера, на котором выполняется служба Application Object Server (AOS).
    2. Сохраните эти созданные файлы только в том случае, когда используется тип нового документа(например, тип **FileX**, содержащий ключевое слово "(ЛОКАЛЬНЫЙ)" в имени), а файла прикреплен к записи в журнале задания выполнения электронной отчетности.

    ```
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

- [Места назначения электронной отчетности](electronic-reporting-destinations.md)
- [Домашняя страница расширения](../extensibility/extensibility-home-page.md)
