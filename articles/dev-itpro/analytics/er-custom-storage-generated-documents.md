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
ms.openlocfilehash: 3ea9de81045dfd01ffec2c8a1d98ea2ba4f2c49a
ms.sourcegitcommit: 0e01d3907b70261aee2df3e3ce0dde2f1343a43a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2019
ms.locfileid: "770096"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="57f66-103">Указание пользовательского места хранения для созданных документов</span><span class="sxs-lookup"><span data-stu-id="57f66-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="57f66-104">Интерфейс прикладного программирования (API) платформы электронной отчетности (ER) позволяет расширять список местоположения хранения для документов, формируемых форматами ER.</span><span class="sxs-lookup"><span data-stu-id="57f66-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="57f66-105">Этот раздел содержит обзор основных задач, которые необходимо выполнить для добавления пользовательского местоположения хранения.</span><span class="sxs-lookup"><span data-stu-id="57f66-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="57f66-106">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="57f66-106">Prerequisites</span></span>

<span data-ttu-id="57f66-107">Необходимо развернуть топологию Microsoft Dynamics 365 for Finance and Operations, которая поддерживает непрерывную сборку.</span><span class="sxs-lookup"><span data-stu-id="57f66-107">You must deploy a Microsoft Dynamics 365 for Finance and Operations topology that supports continuous build.</span></span> <span data-ttu-id="57f66-108">(Дополнительные сведения см. в разделе [Развертывание топологий, поддерживающих непрерывную сборку и автоматизацию тестирования](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Необходимо иметь доступ к этой топологии Finance and Operations для одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="57f66-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this Finance and Operations topology for one of the following roles:</span></span>

- <span data-ttu-id="57f66-109">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="57f66-109">Electronic reporting developer</span></span>
- <span data-ttu-id="57f66-110">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="57f66-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="57f66-111">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="57f66-111">System administrator</span></span>

<span data-ttu-id="57f66-112">Кроме того, необходим доступ к среде разработки для этой топологии Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="57f66-112">You must also have access to the development environment for this Finance and Operations topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="57f66-113">Создание или импорт конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="57f66-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="57f66-114">В текущей топологии Finance and Operations [создайте новый формат ER](tasks/er-format-configuration-2016-11.md) для создания документов, для которых планируется добавить пользовательское хранилище.</span><span class="sxs-lookup"><span data-stu-id="57f66-114">In the current Finance and Operations topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="57f66-115">Можно также [импортировать существующий формат ER в эту топологию](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="57f66-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Страница конструктора форматов](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="57f66-117">Формат ER, который вы создаете или импортируете, должен содержать хотя бы один из следующих элементов формата:</span><span class="sxs-lookup"><span data-stu-id="57f66-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="57f66-118">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="57f66-118">File</span></span>
> - <span data-ttu-id="57f66-119">Папка</span><span class="sxs-lookup"><span data-stu-id="57f66-119">Folder</span></span>
> - <span data-ttu-id="57f66-120">Средство объединения</span><span class="sxs-lookup"><span data-stu-id="57f66-120">Merger</span></span>
> - <span data-ttu-id="57f66-121">Вложение</span><span class="sxs-lookup"><span data-stu-id="57f66-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="57f66-122">Создание нового типа документов</span><span class="sxs-lookup"><span data-stu-id="57f66-122">Create a new document type</span></span>

<span data-ttu-id="57f66-123">Чтобы указать способ маршрутизации документов, создаваемых форматом ER, необходимо настроить [пункты назначения ER](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="57f66-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="57f66-124">В каждом пункте назначения ER, настроенном для хранения созданных документов в виде файлов, необходимо указать тип документа платформы управления документами.</span><span class="sxs-lookup"><span data-stu-id="57f66-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="57f66-125">Различные типы документов могут использоваться для маршрутизации документов, создаваемых различными форматами электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="57f66-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="57f66-126">Добавьте новый [тип документа](../../fin-and-ops/organization-administration/configure-document-management.md) в формат ER, созданный или импортированный ранее.</span><span class="sxs-lookup"><span data-stu-id="57f66-126">Add a new [document type](../../fin-and-ops/organization-administration/configure-document-management.md) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="57f66-127">На рисунке ниже тип документа — **FileX**.</span><span class="sxs-lookup"><span data-stu-id="57f66-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="57f66-128">Этот отличать этот тип документа от других типов документов, включите определенное ключевое слово в его имя.</span><span class="sxs-lookup"><span data-stu-id="57f66-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="57f66-129">Например, на следующем рисунке задано имя **(ЛОКАЛЬНАЯ) папка**.</span><span class="sxs-lookup"><span data-stu-id="57f66-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="57f66-130">В поле **Класс** укажите **Вложить файл**.</span><span class="sxs-lookup"><span data-stu-id="57f66-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="57f66-131">В поле **Группа** укажите **Файл**.</span><span class="sxs-lookup"><span data-stu-id="57f66-131">In the **Group** field, specify **File**.</span></span>

![Страница типов документов](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="57f66-133">Типы документов зависят от конкретной компании.</span><span class="sxs-lookup"><span data-stu-id="57f66-133">Document types are company-specific.</span></span> <span data-ttu-id="57f66-134">Чтобы использовать формат ER с настроенным пунктом назначения в нескольких компаниях, необходимо настроить тип отдельный тип документов в каждой компании.</span><span class="sxs-lookup"><span data-stu-id="57f66-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="57f66-135">Проверка исходного кода</span><span class="sxs-lookup"><span data-stu-id="57f66-135">Review source code</span></span>

<span data-ttu-id="57f66-136">Просмотрите код метода **insertFile()** класса **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="57f66-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="57f66-137">Обратите внимание, что событие **AttachingFile()** возникает, когда созданный файл присоединяется к записи.</span><span class="sxs-lookup"><span data-stu-id="57f66-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

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

<span data-ttu-id="57f66-138">Событие **AttachingFile()** возникает, когда обрабатываются следующие пункты назначения электронной отчетности:</span><span class="sxs-lookup"><span data-stu-id="57f66-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="57f66-139">**Архив** — при использовании этого пункта назначения новая запись для запущенного формата ER будет создана в таблице ERFormatMappingRunJobTable.</span><span class="sxs-lookup"><span data-stu-id="57f66-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="57f66-140">Поле **Архивировано** в этой записи имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="57f66-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="57f66-141">Если формат электронной отчетности успешно выполняется, созданный документ присоединяется к этой записи и возникает событие **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="57f66-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="57f66-142">Тип документа, который выбран в этом месте назначения ER, определяет место хранения для прикрепленного файла (хранилище Microsoft Azure Storage или папка Microsoft SharePoint).</span><span class="sxs-lookup"><span data-stu-id="57f66-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="57f66-143">**Архив заданий** — при использовании этого пункта назначения новая запись для запущенного формата ER будет создана в таблице ERFormatMappingRunJobTable.</span><span class="sxs-lookup"><span data-stu-id="57f66-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="57f66-144">Поле **Архивировано** в этой записи имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="57f66-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="57f66-145">Если формат электронной отчетности успешно выполняется, созданный документ присоединяется к этой записи и возникает событие **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="57f66-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="57f66-146">Тип документа, который настроен в параметрах ER, определяет место хранения для прикрепленного файла (хранилище Azure Storage или папка SharePoint).</span><span class="sxs-lookup"><span data-stu-id="57f66-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Страница параметров электронной отчетности](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="57f66-148">Настройка места назначения ER</span><span class="sxs-lookup"><span data-stu-id="57f66-148">Configure an ER destination</span></span>

1. <span data-ttu-id="57f66-149">Настройте архивированное место назначения для одного из ранее упомянутых элементов (файл, папка, средство слияния или вложение) формата ER, который вы создали или импортировали.</span><span class="sxs-lookup"><span data-stu-id="57f66-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="57f66-150">Указания см. в разделе [Электронная отчетность — Настройка мест назначений](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="57f66-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="57f66-151">Используйте тип документа, который был добавлен ранее для сконфигурированного места назначения.</span><span class="sxs-lookup"><span data-stu-id="57f66-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="57f66-152">(Например, в этом разделе это тип документа **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="57f66-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Диалоговое окно параметров места назначения](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="57f66-154">Изменение исходного кода</span><span class="sxs-lookup"><span data-stu-id="57f66-154">Modify source code</span></span>

1. <span data-ttu-id="57f66-155">Добавьте новый класс в проект Microsoft Visual Studio и напишите код для подписки на событие **AttachingFile()**, которое упомянуто выше.</span><span class="sxs-lookup"><span data-stu-id="57f66-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="57f66-156">(Дополнительные сведения об используемом шаблоне расширения см. в разделе [Ответ с использованием EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Например, в новом классе напишите код, который выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="57f66-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="57f66-157">Сохраните созданные файлы в папке локальной файловой системы сервера, на котором выполняется служба Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="57f66-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="57f66-158">Сохраните эти созданные файлы только в том случае, когда используется тип нового документа(например, тип **FileX**, содержащий ключевое слово "(ЛОКАЛЬНЫЙ)" в имени), а файла прикреплен к записи в журнале задания выполнения электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="57f66-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

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

2. <span data-ttu-id="57f66-159">Заново выполните сборку проекта</span><span class="sxs-lookup"><span data-stu-id="57f66-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="57f66-160">Запуск созданного или импортированного формата ER</span><span class="sxs-lookup"><span data-stu-id="57f66-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="57f66-161">Выполните созданный или импортированный формат ER.</span><span class="sxs-lookup"><span data-stu-id="57f66-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="57f66-162">Перейдите в раздел **Управление организацией \> Электронная отчетность \> Задания электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="57f66-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="57f66-163">Найдите запись, которая была создана для этого задания выполнения, и которая создала файл, прикрепленный к ней.</span><span class="sxs-lookup"><span data-stu-id="57f66-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="57f66-164">Выполните поиск в локальной папке **C:\\0**, чтобы найти такой созданный файл.</span><span class="sxs-lookup"><span data-stu-id="57f66-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57f66-165">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="57f66-165">Additional resources</span></span>

- [<span data-ttu-id="57f66-166">Места назначения электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="57f66-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="57f66-167">Домашняя страница расширения</span><span class="sxs-lookup"><span data-stu-id="57f66-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)