---
title: Демонстрационные данные омниканальных рекомендаций продукта
description: В этом документе приводятся инструкции по использованию омниканальных рекомендаций по продуктам в среде уровня 1 с одним блоком, используя готовые настраиваемые демонстрационные данные.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226369"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="31781-103">Демонстрационные данные омниканальных рекомендаций продукта</span><span class="sxs-lookup"><span data-stu-id="31781-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="31781-104">В этом документе приводятся инструкции по использованию омниканальных рекомендаций по продуктам в среде уровня 1 с одним блоком, используя готовые настраиваемые демонстрационные данные.</span><span class="sxs-lookup"><span data-stu-id="31781-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="31781-105">Омниканальные рекомендации по продуктам предоставляют набор отобранных редактором продуктов или созданный программно упорядоченный список продуктов.</span><span class="sxs-lookup"><span data-stu-id="31781-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="31781-106">Эти списки могут использоваться в нескольких сценариях, в зависимости от потребностей бизнеса.</span><span class="sxs-lookup"><span data-stu-id="31781-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="31781-107">Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendaitons-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31781-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="31781-108">В средах Dynamics уровня 2 и выше рекомендации по продуктам автоматически рассчитываются на основе данных о клиентах.</span><span class="sxs-lookup"><span data-stu-id="31781-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="31781-109">Использование демонстрационных данных рекомендаций по продуктам не отключает никаких решений рекомендаций продуктов, уже подготовленных в среде и каких-либо затраты, связанных с их использованием.</span><span class="sxs-lookup"><span data-stu-id="31781-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="31781-110">В средах уровня 1 рекомендации продуктов основываются только на статических демонстрационных данных, хранящихся в CSV-файле.</span><span class="sxs-lookup"><span data-stu-id="31781-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="31781-111">Включение демонстрационных данных рекомендаций продуктов в среде</span><span class="sxs-lookup"><span data-stu-id="31781-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="31781-112">Клиентам необходимо развернуть **расширение демонстрации предварительной версии Dynamics 365 Commerce** в соответствующей среде, что автоматически включает демонстрационные данные рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="31781-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="31781-113">Демонстрационные данные по умолчанию</span><span class="sxs-lookup"><span data-stu-id="31781-113">Default demo data</span></span>
<span data-ttu-id="31781-114">Каждая среда типа Onebox поставляется с предварительно загруженным набором демонстрационных данных рекомендаций продуктов, которые хранятся разделенной запятыми файле **‘reco_demo_data.csv’**, расположенном в той же папке, что и этот документ на сервере Retail Server.</span><span class="sxs-lookup"><span data-stu-id="31781-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="31781-115">Эти данные структурированы по следующим столбцым</span><span class="sxs-lookup"><span data-stu-id="31781-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="31781-116">Наименование столбца</span><span class="sxs-lookup"><span data-stu-id="31781-116">Column name</span></span>         | <span data-ttu-id="31781-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31781-117">Mandatory</span></span>          | <span data-ttu-id="31781-118">Описание</span><span class="sxs-lookup"><span data-stu-id="31781-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="31781-119">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="31781-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="31781-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="31781-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="31781-122">Особый тип списка рекомендованных продуктов, который будет создаваться на этапе демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="31781-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="31781-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="31781-123">RecoBestSelling</span></span></li><li><span data-ttu-id="31781-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="31781-124">RecoNew</span></span></li><li><span data-ttu-id="31781-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="31781-125">RecoTrending</span></span></li><li><span data-ttu-id="31781-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="31781-126">RecoCart</span></span></li><li><span data-ttu-id="31781-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="31781-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="31781-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="31781-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="31781-130">Конкретный номер операционной единицы, в которой предполагается, что отображаются рекомендации по продуктам.</span><span class="sxs-lookup"><span data-stu-id="31781-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="31781-131">Категория</span><span class="sxs-lookup"><span data-stu-id="31781-131">Category</span></span>            |                    |    <span data-ttu-id="31781-132">Категория, для которой должен возвращаться определенный список.</span><span class="sxs-lookup"><span data-stu-id="31781-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="31781-133">Если категория не указана, список будет только для вершины иерархии переходов.</span><span class="sxs-lookup"><span data-stu-id="31781-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="31781-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="31781-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="31781-135">Для списков, требующих начального значения (RecoPeopleAlsoBuy и RecoCart), продукт, для которого эти списки должны отображать дополнительные продукты.</span><span class="sxs-lookup"><span data-stu-id="31781-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="31781-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="31781-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="31781-138">Один или несколько продуктов, которые должны быть возвращены в виде результата, разделенные точкой с запятой **";"**.</span><span class="sxs-lookup"><span data-stu-id="31781-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="31781-139">Настройка демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="31781-139">Customize demo data</span></span>
<span data-ttu-id="31781-140">Клиенты могут редактировать демонстрационные данные по умолчанию с любой информацией о продуктах и категориях, настроенных в головном отделении.</span><span class="sxs-lookup"><span data-stu-id="31781-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="31781-141">После обновления файла CSV возвращаемые пользователями рекомендации продуктов немедленно отразят внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="31781-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="31781-142">Расширение содержит файл данных с именем RecoMockDataset.csv, который позволяет пользователю управлять набором данных, используемых для создания результатов демонстрационных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="31781-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="31781-143">Управлять именем файла можно с помощью настройки расширения, используя настройку **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="31781-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="31781-144">Это позволяет клиентам иметь несколько доступных наборов данных, которые можно легко переключать с помощью конфигурации.</span><span class="sxs-lookup"><span data-stu-id="31781-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="31781-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="31781-145">Additional resources</span></span>

[<span data-ttu-id="31781-146">Обзор рекомендаций продуктов</span><span class="sxs-lookup"><span data-stu-id="31781-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="31781-147">Планирование среды</span><span class="sxs-lookup"><span data-stu-id="31781-147">Environment planning</span></span>](environment-planning.md)
