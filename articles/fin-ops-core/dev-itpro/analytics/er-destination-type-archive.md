---
title: Тип места назначения ER архива
description: В этой теме приводятся сведения о настройке места назначения архива для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745593"
---
# <a name="archive-destination"></a><span data-ttu-id="20888-103">Место назначения архива</span><span class="sxs-lookup"><span data-stu-id="20888-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20888-104">Можно настроить место назначения архива для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="20888-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="20888-105">На основании настройки места назначения созданный документ сохраняется в виде вложения записи списка заданий ER.</span><span class="sxs-lookup"><span data-stu-id="20888-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="20888-106">Этот параметр можно использовать для отправки созданного документа в папку Microsoft SharePoint или хранилище Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20888-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="20888-107">Задайте для параметра **Включено** значение **Да** для отправки выходных данных в место назначения, которое определяется выбранным типом документа.</span><span class="sxs-lookup"><span data-stu-id="20888-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="20888-108">Для выбора доступны только типы, в которых для группы задано значение **Файл**.</span><span class="sxs-lookup"><span data-stu-id="20888-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="20888-109">[Типы](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) документов определяются в разделе **Управление организацией** \> **Управление документами** \> **Типы документов**.</span><span class="sxs-lookup"><span data-stu-id="20888-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="20888-110">Конфигурация для мест назначения электронной отчетности аналогична конфигурации системы управления документами.</span><span class="sxs-lookup"><span data-stu-id="20888-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="20888-111">[![Страница типов документов](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="20888-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="20888-112">Расположение определяет, где сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="20888-112">The location determines where the file is saved.</span></span> <span data-ttu-id="20888-113">После включения места назначения **Архив** результаты можно сохранить в архиве заданий.</span><span class="sxs-lookup"><span data-stu-id="20888-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="20888-114">Можно просмотреть результаты в пункте **Управление организацией** \> **Электронная отчетность** \> **Архивированные задания электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="20888-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="20888-115">Выберите тип документа для архива заданий в пункте **Управление организацией** \> **Рабочие области** \> **Электронная отчетность** \> **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="20888-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="20888-116">Дополнительные сведения см. в разделе [Настройка платформы для электронной отчетности (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="20888-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="20888-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="20888-117">SharePoint</span></span>

<span data-ttu-id="20888-118">Можно сохранить файл в указанной папке SharePoint.</span><span class="sxs-lookup"><span data-stu-id="20888-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="20888-119">Чтобы задать сервер SharePoint по умолчанию, перейдите **Управление организацией** \> **Управление документами** \> **Параметры правления документами**.</span><span class="sxs-lookup"><span data-stu-id="20888-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="20888-120">На вкладке **SharePoint** настройте папку SharePoint.</span><span class="sxs-lookup"><span data-stu-id="20888-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="20888-121">Затем ее можно выбрать в качестве папки, в которой будет сохранены выходные данные ER.</span><span class="sxs-lookup"><span data-stu-id="20888-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="20888-122">Местонахождение **SharePoint** должно быть выбрано для этого типа документа.</span><span class="sxs-lookup"><span data-stu-id="20888-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="20888-123">[![Выбор папки SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="20888-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="20888-124">Хранилище Azure</span><span class="sxs-lookup"><span data-stu-id="20888-124">Azure Storage</span></span>

<span data-ttu-id="20888-125">Если в качестве расположения типа документа указан **Хранилище Azure**, можно сохранить файл в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="20888-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20888-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20888-126">Additional resources</span></span>

- [<span data-ttu-id="20888-127">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="20888-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="20888-128">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="20888-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="20888-129">Настройка управления документами</span><span class="sxs-lookup"><span data-stu-id="20888-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
