---
title: Создание рекомендаций с помощью демонстрационных данных
description: В этом документе приводятся инструкции по использованию омниканальных рекомендаций по продуктам в среде уровня 1 с одним блоком, используя готовые настраиваемые демонстрационные данные.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2e790d78b4d5216822ffda3a3895feb674876bd8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127844"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="025bb-103">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="025bb-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="025bb-104">В этом документе приводятся инструкции по использованию омниканальных рекомендаций по продуктам в среде уровня 1 с одним блоком, используя готовые настраиваемые демонстрационные данные.</span><span class="sxs-lookup"><span data-stu-id="025bb-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="025bb-105">Омниканальные рекомендации по продуктам предоставляют набор отобранных редактором продуктов или созданный программно список продуктов.</span><span class="sxs-lookup"><span data-stu-id="025bb-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="025bb-106">Эти списки могут использоваться в нескольких сценариях, в зависимости от потребностей бизнеса.</span><span class="sxs-lookup"><span data-stu-id="025bb-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="025bb-107">Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="025bb-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="025bb-108">В средах Dynamics 365 уровня 2 и выше рекомендации по продуктам автоматически рассчитываются на основе данных о клиентах.</span><span class="sxs-lookup"><span data-stu-id="025bb-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="025bb-109">Использование демонстрационных данных рекомендаций по продуктам не отключает никаких решений рекомендаций продуктов, уже подготовленных в среде и каких-либо затраты, связанных с их использованием.</span><span class="sxs-lookup"><span data-stu-id="025bb-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="025bb-110">В средах уровня 1 рекомендации продуктов основываются только на статических демонстрационных данных, хранящихся в CSV-файле.</span><span class="sxs-lookup"><span data-stu-id="025bb-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="025bb-111">Включение демонстрационных данных рекомендаций продуктов в среде</span><span class="sxs-lookup"><span data-stu-id="025bb-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="025bb-112">Чтобы включить демонстрационные данные рекомендаций продуктов, необходимо развернуть расширение демонстрации предварительной версии Dynamics 365 Commerce в соответствующей среде.</span><span class="sxs-lookup"><span data-stu-id="025bb-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="025bb-113">При этом автоматически включаются демонстрационные данные рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="025bb-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="025bb-114">Демонстрационные данные по умолчанию</span><span class="sxs-lookup"><span data-stu-id="025bb-114">Default demo data</span></span>
<span data-ttu-id="025bb-115">Каждая среда типа Onebox поставляется с предварительно загруженным набором демонстрационных данных рекомендаций продуктов, которые хранятся в разделенном запятыми файле "reco_demo_data.csv", расположенным в Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="025bb-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="025bb-116">Данные структурированы по следующим столбцам.</span><span class="sxs-lookup"><span data-stu-id="025bb-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="025bb-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="025bb-117">Column name</span></span>         | <span data-ttu-id="025bb-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="025bb-118">Mandatory</span></span>          | <span data-ttu-id="025bb-119">Описание</span><span class="sxs-lookup"><span data-stu-id="025bb-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="025bb-120">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="025bb-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="025bb-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="025bb-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="025bb-123">Особый тип списка рекомендованных продуктов, который будет создаваться на этапе демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="025bb-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="025bb-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="025bb-124">RecoBestSelling</span></span></li><li><span data-ttu-id="025bb-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="025bb-125">RecoNew</span></span></li><li><span data-ttu-id="025bb-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="025bb-126">RecoTrending</span></span></li><li><span data-ttu-id="025bb-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="025bb-127">RecoCart</span></span></li><li><span data-ttu-id="025bb-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="025bb-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="025bb-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="025bb-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="025bb-131">Конкретный номер операционной единицы, в которой предполагается, что отображаются рекомендации продуктов.</span><span class="sxs-lookup"><span data-stu-id="025bb-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="025bb-132">Категория</span><span class="sxs-lookup"><span data-stu-id="025bb-132">Category</span></span>            |                    |    <span data-ttu-id="025bb-133">Категория, для которой должен возвращаться определенный список.</span><span class="sxs-lookup"><span data-stu-id="025bb-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="025bb-134">Если категория не указана, список будет только для вершины иерархии переходов.</span><span class="sxs-lookup"><span data-stu-id="025bb-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="025bb-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="025bb-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="025bb-136">Для списков, требующих начального значения (RecoPeopleAlsoBuy и RecoCart), продукт, для которого эти списки должны отображать дополнительные продукты.</span><span class="sxs-lookup"><span data-stu-id="025bb-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="025bb-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="025bb-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="025bb-139">Один или несколько продуктов, которые должны быть возвращены в виде результата, разделенные точкой с запятой ";".</span><span class="sxs-lookup"><span data-stu-id="025bb-139">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="025bb-140">Настройка демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="025bb-140">Customize demo data</span></span>
<span data-ttu-id="025bb-141">Вы можете редактировать демонстрационные данные по умолчанию с любой информацией о продуктах и категориях, настроенных в головном отделении.</span><span class="sxs-lookup"><span data-stu-id="025bb-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="025bb-142">После обновления файла .csv возвращаемые пользователями рекомендации продуктов немедленно отразят внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="025bb-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="025bb-143">Расширение содержит файл данных с именем "RecoMockDataset.csv", который позволяет вам управлять набором данных, используемых для создания результатов демонстрационных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="025bb-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="025bb-144">Управлять именем файла можно с помощью настройки расширения, используя настройку **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="025bb-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="025bb-145">Это позволяет вам иметь несколько доступных наборов данных, которые можно легко переключать с помощью конфигурации.</span><span class="sxs-lookup"><span data-stu-id="025bb-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="025bb-146">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="025bb-146">Additional Resources</span></span>

[<span data-ttu-id="025bb-147">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="025bb-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="025bb-148">Включение ADLS в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="025bb-148">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="025bb-149">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="025bb-149">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="025bb-150">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="025bb-150">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="025bb-151">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="025bb-151">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="025bb-152">Добавление списков рекомендаций на сайт электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="025bb-152">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="025bb-153">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="025bb-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="025bb-154">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="025bb-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="025bb-155">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="025bb-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="025bb-156">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="025bb-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="025bb-157">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="025bb-157">Product recommendations FAQ</span></span>](faq-recommendations.md)
