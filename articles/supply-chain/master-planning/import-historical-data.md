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
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66481b1dd8650960cad2947425c1e6c7450afcb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436279"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="1cbf6-104">Импорт исторических данных для прогнозов спроса</span><span class="sxs-lookup"><span data-stu-id="1cbf6-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cbf6-105">Для обеспечения точности прогнозов спроса необходимо иметь максимальный объем исторических данных по спросу, который можно получить для номенклатуры или ключа распределения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="1cbf6-106">Если исторические данные по спросу еще не импортированы, используйте информационный объект **Исторический внешний спрос** (ReqDemPlanHistoricalExternalDemandEntity) в Dynamics 365 Supply Chain Management, чтобы импортировать его.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="1cbf6-107">В рабочей области **Управление данными** можно просмотреть обзор всех полей объекта.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="1cbf6-108">Откройте рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="1cbf6-109">Щелкните плитку **Информационные объекты**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="1cbf6-110">Найдите в списке объект **Исторический внешний спрос**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="1cbf6-111">Щелкните **Целевые поля**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-111">Click **Target fields**.</span></span> <span data-ttu-id="1cbf6-112">Следующие поля объекта являются обязательными: сайт (**DeliveringSiteId**), дата (**DemandDate**), количество (**DemandQuantity**) и номер номенклатуры (**ItemNumber**) или ключ распределения номенклатуры (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="1cbf6-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="1cbf6-113">Чтобы использовать информационный объект, необходим файл Microsoft Excel или файл значений с разделителями-запятыми (CSV), содержащий исторические данные о спросе.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="1cbf6-114">В следующем примере показано, как импортировать данные из CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="1cbf6-115">Пример</span><span class="sxs-lookup"><span data-stu-id="1cbf6-115">Example</span></span>

<span data-ttu-id="1cbf6-116">Можно использовать следующий файл в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-116">You can use the following file as an example.</span></span> <span data-ttu-id="1cbf6-117">Загрузите [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="1cbf6-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="1cbf6-118">Этот файл содержит исторические данные по спросу для номенклатуры D0001.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="1cbf6-119">Он содержит только следующие обязательные поля: сайт, количество и дата спроса.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="1cbf6-120">Выберите компанию, в которую следует импортировать исторические данные о спросе.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="1cbf6-121">Откройте рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="1cbf6-122">Щелкните плитку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="1cbf6-123">Введите имя для проекта импорта, например **Импорт исторического спроса на номенклатуру D0001**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="1cbf6-124">В поле **Формат исходных данных** выберите формат импортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="1cbf6-125">Чтобы импортировать файл HistoricalDemandData из этого примера, выберите **CSV**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="1cbf6-126">В поле **Имя объекта** выберите **Исторический внешний спрос**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="1cbf6-127">Сохраните файл на своем компьютере, затем отправьте его.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="1cbf6-128">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-128">Click **Import**.</span></span>
9. <span data-ttu-id="1cbf6-129">Автоматически открывается страница **Сводка выполнения**.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="1cbf6-130">Проверьте импортированные данные на странице.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="1cbf6-131">После импорта исторических данных о спросе можно создать прогноз продаж.</span><span class="sxs-lookup"><span data-stu-id="1cbf6-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cbf6-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1cbf6-132">Additional resources</span></span>

[<span data-ttu-id="1cbf6-133">Создание статистического базового прогноза</span><span class="sxs-lookup"><span data-stu-id="1cbf6-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
