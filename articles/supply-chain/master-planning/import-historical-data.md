---
title: Импорт исторических данных для прогнозов спроса
description: Чтобы получить точные прогнозы спроса, требуются исторические данные по спросу на номенклатуру или ключу распределения номенклатуры. В этом разделе объясняется, как использовать объекты данных для импорта исторических данных о спросе из любой системы, чтобы получить более данные для прогноза спроса за больший исторический период.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6ba2e1a3a884d29bff491f914aa2d5f9ece2b84
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154235"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="7c775-104">Импорт исторических данных для прогнозов спроса</span><span class="sxs-lookup"><span data-stu-id="7c775-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c775-105">Для обеспечения точности прогнозов спроса необходимо иметь максимальный объем исторических данных по спросу, который можно получить для номенклатуры или ключа распределения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7c775-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="7c775-106">Если исторические данные по спросу еще не импортированы, используйте информационный объект **Исторический внешний спрос** (ReqDemPlanHistoricalExternalDemandEntity) в Dynamics 365 Supply Chain Management, чтобы импортировать его.</span><span class="sxs-lookup"><span data-stu-id="7c775-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="7c775-107">В рабочей области **Управление данными** можно просмотреть обзор всех полей объекта.</span><span class="sxs-lookup"><span data-stu-id="7c775-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="7c775-108">Откройте рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="7c775-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="7c775-109">Выберите плитку **Информационные объекты**.</span><span class="sxs-lookup"><span data-stu-id="7c775-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="7c775-110">Найдите в списке объект **Исторический внешний спрос**.</span><span class="sxs-lookup"><span data-stu-id="7c775-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="7c775-111">Выберите **Целевые поля**.</span><span class="sxs-lookup"><span data-stu-id="7c775-111">Select **Target fields**.</span></span> <span data-ttu-id="7c775-112">Следующие поля объекта являются обязательными: сайт (**DeliveringSiteId**), дата (**DemandDate**), количество (**DemandQuantity**) и номер номенклатуры (**ItemNumber**) или ключ распределения номенклатуры (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="7c775-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="7c775-113">Чтобы использовать информационный объект, необходим файл Microsoft Excel или файл значений с разделителями-запятыми (CSV), содержащий исторические данные о спросе.</span><span class="sxs-lookup"><span data-stu-id="7c775-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="7c775-114">В следующем примере показано, как импортировать данные из CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="7c775-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="7c775-115">Дополнительные сведения о том, как импортировать данные, в том числе о порядке очистки данных после импорта, см. в теме [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) и связанных с ней темах.</span><span class="sxs-lookup"><span data-stu-id="7c775-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="7c775-116">Пример</span><span class="sxs-lookup"><span data-stu-id="7c775-116">Example</span></span>

<span data-ttu-id="7c775-117">Можно использовать следующий файл в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="7c775-117">You can use the following file as an example.</span></span> <span data-ttu-id="7c775-118">Загрузите [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="7c775-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="7c775-119">Этот файл содержит исторические данные по спросу для номенклатуры D0001.</span><span class="sxs-lookup"><span data-stu-id="7c775-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="7c775-120">Он содержит только следующие обязательные поля: сайт, количество и дата спроса.</span><span class="sxs-lookup"><span data-stu-id="7c775-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="7c775-121">Выберите компанию, в которую следует импортировать исторические данные о спросе.</span><span class="sxs-lookup"><span data-stu-id="7c775-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="7c775-122">Откройте рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="7c775-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="7c775-123">Выберите плитку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="7c775-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="7c775-124">Введите имя для проекта импорта, например **Импорт исторического спроса на номенклатуру D0001**.</span><span class="sxs-lookup"><span data-stu-id="7c775-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="7c775-125">В поле **Формат исходных данных** выберите формат импортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="7c775-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="7c775-126">Чтобы импортировать файл HistoricalDemandData из этого примера, выберите **CSV**.</span><span class="sxs-lookup"><span data-stu-id="7c775-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="7c775-127">В поле **Имя объекта** выберите **Исторический внешний спрос**.</span><span class="sxs-lookup"><span data-stu-id="7c775-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="7c775-128">Сохраните файл на своем компьютере, затем отправьте его.</span><span class="sxs-lookup"><span data-stu-id="7c775-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="7c775-129">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="7c775-129">Select **Import**.</span></span>
9. <span data-ttu-id="7c775-130">Автоматически открывается страница **Сводка выполнения**.</span><span class="sxs-lookup"><span data-stu-id="7c775-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="7c775-131">Проверьте импортированные данные на странице.</span><span class="sxs-lookup"><span data-stu-id="7c775-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="7c775-132">После импорта исторических данных о спросе можно создать прогноз продаж.</span><span class="sxs-lookup"><span data-stu-id="7c775-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c775-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7c775-133">Additional resources</span></span>

[<span data-ttu-id="7c775-134">Создание статистического базового прогноза</span><span class="sxs-lookup"><span data-stu-id="7c775-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="7c775-135">Обзор заданий импорта и экспорта данных</span><span class="sxs-lookup"><span data-stu-id="7c775-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)
