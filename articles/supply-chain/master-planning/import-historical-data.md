---
title: Импорт исторических данных для прогнозов спроса
description: Чтобы получить точные прогнозы спроса, требуются исторические данные по спросу на номенклатуру или ключу распределения номенклатуры. В этом разделе объясняется, как использовать объекты данных для импорта исторических данных о спросе из любой системы, чтобы получить более данные для прогноза спроса за больший исторический период.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301658"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="b454b-104">Импорт исторических данных для прогнозов спроса</span><span class="sxs-lookup"><span data-stu-id="b454b-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b454b-105">Для обеспечения точности прогнозов спроса необходимо иметь максимальный объем исторических данных по спросу, который можно получить для номенклатуры или ключа распределения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b454b-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="b454b-106">Если исторические данные по спросу еще не импортированы, используйте информационный объект **Исторический внешний спрос** (ReqDemPlanHistoricalExternalDemandEntity) в Dynamics 365 Supply Chain Management, чтобы импортировать его.</span><span class="sxs-lookup"><span data-stu-id="b454b-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="b454b-107">В рабочей области **Управление данными** можно просмотреть обзор всех полей объекта.</span><span class="sxs-lookup"><span data-stu-id="b454b-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="b454b-108">Откройте рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="b454b-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="b454b-109">Выберите плитку **Информационные объекты**.</span><span class="sxs-lookup"><span data-stu-id="b454b-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="b454b-110">Найдите в списке объект **Исторический внешний спрос**.</span><span class="sxs-lookup"><span data-stu-id="b454b-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="b454b-111">Выберите **Целевые поля**.</span><span class="sxs-lookup"><span data-stu-id="b454b-111">Select **Target fields**.</span></span> <span data-ttu-id="b454b-112">Следующие поля объекта являются обязательными: сайт (**DeliveringSiteId**), дата (**DemandDate**), количество (**DemandQuantity**) и номер номенклатуры (**ItemNumber**) или ключ распределения номенклатуры (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="b454b-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="b454b-113">Чтобы использовать информационный объект, необходим файл Microsoft Excel или файл значений с разделителями-запятыми (CSV), содержащий исторические данные о спросе.</span><span class="sxs-lookup"><span data-stu-id="b454b-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="b454b-114">В следующем примере показано, как импортировать данные из CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="b454b-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="b454b-115">Дополнительные сведения о том, как импортировать данные, в том числе о порядке очистки данных после импорта, см. в теме [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) и связанных с ней темах.</span><span class="sxs-lookup"><span data-stu-id="b454b-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="b454b-116">См. также [Создание статистического базового прогноза](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="b454b-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]