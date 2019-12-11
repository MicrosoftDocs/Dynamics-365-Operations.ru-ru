---
title: Управление результатами рекомендаций по продукту на основе AI-ML
description: В этой теме объясняется, как адаптировать результаты рекомендаций продуктов на основе искусственного интеллекта и машинного обучения (AI-ML) для вашего бизнеса.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770078"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="4c2a8-103">Управление результатами рекомендаций по продукту на основе AI-ML</span><span class="sxs-lookup"><span data-stu-id="4c2a8-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4c2a8-104">В этой теме объясняется, как адаптировать результаты рекомендаций продуктов на основе искусственного интеллекта и машинного обучения (AI-ML) для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="4c2a8-105">После включения рекомендаций продуктов параметры по умолчанию вступят в силу; эти параметры могут работать для различных нужд.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="4c2a8-106">Лучше всего потратить некоторое время, оценивая, насколько результаты соответствуют движениям продаж продуктов.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="4c2a8-107">Перед повторным тестированием рекомендуется оценить результаты в течение нескольких дней, прежде чем изменять параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="4c2a8-108">Сведения о параметрах списка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4c2a8-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="4c2a8-109">Перед изменением параметров узнайте, как они будут влиять на результаты, указанные далее.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="4c2a8-110">Список популярных продуктов</span><span class="sxs-lookup"><span data-stu-id="4c2a8-110">Trending product list</span></span>

<span data-ttu-id="4c2a8-111">Список продуктов **Популярные** имеет два параметра, которые могут быть изменены: ![Пример параметров по умолчанию для списка популярных продуктов](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="4c2a8-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="4c2a8-112">**Включить новые продукты за последних X дней** — продукты, которые были добавлены в течение указанного количества дней до текущей даты, можно использовать для выбора кандидатов на продукты.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="4c2a8-113">Значение по умолчанию на рисунке предполагает, что в списке популярных продуктов можно использовать продукты со сроком давности 180 дней.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="4c2a8-114">**Включить продажи за последних X дней** — проводки продаж, которые были выполнены в течение указанного количества дней до текущей даты, можно использовать для заказа продуктов.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="4c2a8-115">Значение по умолчанию, приведенное выше, предполагает, что все покупки продукта за последние 30 дней будут использоваться для определения местоположения продукта в списке популярных продуктов.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="4c2a8-116">Список продуктов — лидеров продаж</span><span class="sxs-lookup"><span data-stu-id="4c2a8-116">Best selling product list</span></span>

<span data-ttu-id="4c2a8-117">В зависимости от бизнеса,лидеры продаж могут привести к получению результатов, отличающихся от популярных продуктов, даже если они оба используют данные проводок для заказа продуктов.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="4c2a8-118">Так как лидеры продаж не имеют отсечки на основе даты ассортимента, лидеры продаж все равно могут выделять самые популярны старые продукты, которые могли быть удалены из списка популярных продаж.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="4c2a8-119">Продукт **Лидер продаж** имеет один параметр, который может быть изменен:</span><span class="sxs-lookup"><span data-stu-id="4c2a8-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Пример параметра по умолчанию для списка лидеров продаж](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="4c2a8-121">**Включить продажи за последних X дней** — проводки продаж, которые были выполнены в течение указанного количества дней до текущей даты, можно использовать для заказа продуктов.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="4c2a8-122">Значение по умолчанию, приведенное выше, предполагает, что все покупки продукта за последние 30 дней будут использоваться для определения местоположения продукта в списке лидеров продаж.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="4c2a8-123">Добавление или удаление продуктов из списков рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="4c2a8-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="4c2a8-124">Для новых, популярных или лидеров продаж</span><span class="sxs-lookup"><span data-stu-id="4c2a8-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="4c2a8-125">Выберите **Retail** > **Рекомендации по продуктам** > **Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="4c2a8-126">В списке общих параметров Retail выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="4c2a8-127">Выберите список, в который требуется добавить или из которого требуется удалить продукты.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="4c2a8-128">Чтобы добавить продукты в таблицу, выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="4c2a8-129">В столбце "Продукт" выполните поиск продукта по параметру **Имя** или **Номер продукта**
![Пример поиска продукта в списке новых продуктов](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="4c2a8-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="4c2a8-130">В столбце "Тип строки" выберите один из двух вариантов:</span><span class="sxs-lookup"><span data-stu-id="4c2a8-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="4c2a8-131">**Включить** — принудительно переводит продукт в начало списка</span><span class="sxs-lookup"><span data-stu-id="4c2a8-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="4c2a8-132">**Исключить** — удаляет продукт из списка ![Пример включения или исключения продукта из списка новых продуктов](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="4c2a8-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="4c2a8-133">Изменение значения **Порядок отображения** приведет к изменению порядка, в котором продукты, помеченные как **Включить**, включаются в список.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="4c2a8-134">Если два продукта имеют одинаковое значение **порядок отображения**, то окончательный порядок этих двух результатов также будет зависит от серверной части.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="4c2a8-135">Чтобы удалить продукты из таблицы: выберите удаляемую строку и выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="4c2a8-136">Для списков "Людям также нравится" или "Часто покупают вместе"</span><span class="sxs-lookup"><span data-stu-id="4c2a8-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="4c2a8-137">В контексте **Часто покупают вместе** или **Людям часто нравится** машинное обучение используется для анализа шаблонов покупок потребителей с целью рекомендовать связанные продукты, обычно приобретаемые вместе с уникальным начальным продуктом.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="4c2a8-138">**Начальный продукт** — это продукт, для которого необходимо создать результаты.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="4c2a8-139">В контексте ручной настройки списков рекомендаций вы добавляете или удаляете результаты для этого продукта.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="4c2a8-140">Чтобы вручную добавить или удалить результаты для начального продукта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4c2a8-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="4c2a8-141">Выберите **Начальный продукт**.</span><span class="sxs-lookup"><span data-stu-id="4c2a8-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="4c2a8-142">В столбце **Продукт** выполните поиск продукта по параметру **Имя** или **Номер продукта**
![Пример поиска продукта в списке "Часто покупают вместе"](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="4c2a8-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="4c2a8-143">В столбце **Тип строки** выберите один из двух вариантов:</span><span class="sxs-lookup"><span data-stu-id="4c2a8-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="4c2a8-144">**Включить** — принудительно переводит продукт в начало списка</span><span class="sxs-lookup"><span data-stu-id="4c2a8-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="4c2a8-145">**Исключить** — исключает продукт, не допуская его появления в списке</span><span class="sxs-lookup"><span data-stu-id="4c2a8-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="4c2a8-146">![Пример включения или исключения продукта для списка "Часто покупают вместе"](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="4c2a8-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="4c2a8-147">Чтобы удалить продукты из таблицы: выберите удаляемую строку и выберите "Удалить".</span><span class="sxs-lookup"><span data-stu-id="4c2a8-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="4c2a8-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4c2a8-148">Additional resources</span></span>

[<span data-ttu-id="4c2a8-149">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="4c2a8-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4c2a8-150">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="4c2a8-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4c2a8-151">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="4c2a8-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
