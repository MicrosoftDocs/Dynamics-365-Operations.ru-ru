---
title: Тип места назначения ER архива
description: В этой теме приводятся сведения о настройке места назначения архива для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679686"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="8aa73-103">Тип места назначения ER архива</span><span class="sxs-lookup"><span data-stu-id="8aa73-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aa73-104">Можно настроить место назначения архива для каждого компонента **Папка** или **Файл** формата электронной отчетности (ER), настроенного для создания исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="8aa73-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="8aa73-105">На основании настройки места назначения созданный документ сохраняется в виде вложения записи списка заданий ER.</span><span class="sxs-lookup"><span data-stu-id="8aa73-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="8aa73-106">Чтобы просмотреть результаты, перейдите в раздел **Управление организацией** \> **Электронная отчетность** \> **Задания электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="8aa73-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="8aa73-107">Этот параметр можно использовать для отправки созданного документа в папку Microsoft SharePoint или хранилище Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa73-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="8aa73-108">Задайте для параметра **Включено** значение **Да** для отправки выходных данных в место назначения, которое определяется выбранным типом документа.</span><span class="sxs-lookup"><span data-stu-id="8aa73-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="8aa73-109">Для выбора доступны только типы, в которых для группы задано значение **Файл**.</span><span class="sxs-lookup"><span data-stu-id="8aa73-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="8aa73-110">[Типы](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) документов определяются в разделе **Управление организацией** \> **Управление документами** \> **Типы документов**.</span><span class="sxs-lookup"><span data-stu-id="8aa73-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="8aa73-111">Конфигурация для мест назначения электронной отчетности аналогична конфигурации системы управления документами.</span><span class="sxs-lookup"><span data-stu-id="8aa73-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="8aa73-112">[![Страница типов документов](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="8aa73-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="8aa73-113">Расположение определяет, где сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="8aa73-113">The location determines where the file is saved.</span></span> <span data-ttu-id="8aa73-114">После включения места назначения **Архив** результаты можно сохранить в архиве заданий.</span><span class="sxs-lookup"><span data-stu-id="8aa73-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="8aa73-115">Можно просмотреть результаты в пункте **Управление организацией** \> **Электронная отчетность** \> **Архивированные задания электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="8aa73-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="8aa73-116">Выберите тип документа для архива заданий в пункте **Управление организацией** \> **Рабочие области** \> **Электронная отчетность** \> **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="8aa73-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="8aa73-117">Дополнительные сведения см. в разделе [Настройка платформы для электронной отчетности (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="8aa73-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="8aa73-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="8aa73-118">SharePoint</span></span>

<span data-ttu-id="8aa73-119">Можно сохранить файл в указанной папке SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8aa73-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="8aa73-120">Чтобы задать сервер SharePoint по умолчанию, перейдите **Управление организацией** \> **Управление документами** \> **Параметры правления документами**.</span><span class="sxs-lookup"><span data-stu-id="8aa73-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="8aa73-121">На вкладке **SharePoint** настройте папку SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8aa73-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="8aa73-122">Затем ее можно выбрать в качестве папки, в которой будет сохранены выходные данные ER.</span><span class="sxs-lookup"><span data-stu-id="8aa73-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="8aa73-123">Местонахождение **SharePoint** должно быть выбрано для этого типа документа.</span><span class="sxs-lookup"><span data-stu-id="8aa73-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="8aa73-124">[![Выбор папки SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="8aa73-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="8aa73-125">Хранилище Azure</span><span class="sxs-lookup"><span data-stu-id="8aa73-125">Azure Storage</span></span>

<span data-ttu-id="8aa73-126">Если в качестве расположения типа документа указан **Хранилище Azure**, можно сохранить файл в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa73-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="8aa73-127">Платформа электронной отчетности постоянно хранит файлы в хранилище больших двоичных объектов Azure, в отличие от платформы управления данными, в которой применяется политика хранения в течение семи дней для документов, которые должны быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="8aa73-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="8aa73-128">Дополнительные сведения см. в разделе [API для получения состояния сообщения](../data-entities/recurring-integrations.md#api-for-getting-message-status) и [API проверки состояния](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="8aa73-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="8aa73-129">Файлы, связанные с электронной отчетностью, будут храниться в хранилище BLOB-объектов Azure как вложения записей таблицы приложений столько, сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="8aa73-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="8aa73-130">Один файл будет удален из хранилища BLOB-объектов Azure наряду с записью таблицы приложений, к которой был добавлен этот файл.</span><span class="sxs-lookup"><span data-stu-id="8aa73-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8aa73-131">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8aa73-131">Additional resources</span></span>

- [<span data-ttu-id="8aa73-132">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="8aa73-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="8aa73-133">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="8aa73-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="8aa73-134">Настройка управления документами</span><span class="sxs-lookup"><span data-stu-id="8aa73-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
