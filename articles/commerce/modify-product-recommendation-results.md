---
title: Корректировка результатов рекомендаций по продукту на основе AI-ML
description: В этой теме объясняется, как адаптировать результаты рекомендаций продуктов на основе искусственного интеллекта и машинного обучения (AI-ML) для вашего бизнеса.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: bc6a793061a3e644599f0882ff163f5f57b2162d
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664962"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="b4ebb-103">Корректировка результатов рекомендаций по продукту на основе AI-ML</span><span class="sxs-lookup"><span data-stu-id="b4ebb-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b4ebb-104">В этой теме объясняется, как корректировать результаты рекомендаций продуктов на основе искусственного интеллекта и машинного обучения (AI-ML) для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="b4ebb-105">После включения рекомендаций продуктов параметры по умолчанию вступят в силу; эти параметры могут работать для различных нужд.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="b4ebb-106">Лучше всего потратить некоторое время, оценивая, насколько результаты соответствуют движениям продаж продуктов.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="b4ebb-107">Перед повторным тестированием рекомендуется оценить результаты в течение нескольких дней, прежде чем изменять параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="b4ebb-108">Сведения о параметрах списка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="b4ebb-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="b4ebb-109">Перед изменением параметров узнайте, как они будут влиять на результаты, указанные далее.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="b4ebb-110">Список популярных продуктов</span><span class="sxs-lookup"><span data-stu-id="b4ebb-110">"Trending" product list</span></span>

<span data-ttu-id="b4ebb-111">Популярный продукт имеет два параметра, которые могут быть изменены:</span><span class="sxs-lookup"><span data-stu-id="b4ebb-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Пример параметров по умолчанию для списка популярного](./media/exampletrendingparameters.png)

1. <span data-ttu-id="b4ebb-113">**Включить новые продукты за последних X дней** — продукты, которые были добавлены в течение указанного количества дней до текущей даты, можно использовать для выбора кандидатов на продукты.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="b4ebb-114">Значение по умолчанию на рисунке предполагает, что в списке популярных продуктов можно использовать продукты со сроком давности 180 дней.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="b4ebb-115">**Включить продажи за последних X дней** — проводки продаж, которые были выполнены в течение указанного количества дней до текущей даты, можно использовать для заказа продуктов.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="b4ebb-116">Значение по умолчанию, приведенное выше, предполагает, что все покупки продукта за последние 30 дней будут использоваться для определения местоположения продукта в списке популярных продуктов.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="b4ebb-117">Список продуктов "Лидеры продаж"</span><span class="sxs-lookup"><span data-stu-id="b4ebb-117">"Best selling" product list</span></span>

<span data-ttu-id="b4ebb-118">В зависимости от бизнеса список "Лидеры продаж" может привести к получению результатов, отличающихся от популярных продуктов, даже если они оба используют данные проводок для заказа продуктов.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="b4ebb-119">Так как лидеры продаж не имеют отсечки на основе даты ассортимента, лидеры продаж все равно могут выделять самые популярны старые продукты, которые могли быть удалены из списка популярных продаж.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="b4ebb-120">Продукт "Лидер продаж" имеет один параметр, который может быть изменен:</span><span class="sxs-lookup"><span data-stu-id="b4ebb-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Пример параметра по умолчанию для списка лидеров продаж](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="b4ebb-122">**Включить продажи за последних X дней** — проводки продаж, которые были выполнены в течение указанного количества дней до текущей даты, можно использовать для заказа продуктов.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="b4ebb-123">Значение по умолчанию, приведенное выше, предполагает, что все покупки продукта за последние 30 дней будут использоваться для определения местоположения продукта в списке лидеров продаж.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="b4ebb-124">Добавление или удаление продуктов из списков рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="b4ebb-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="b4ebb-125">Для списков "Новые", "Популярные" или "Лидеры продаж"</span><span class="sxs-lookup"><span data-stu-id="b4ebb-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="b4ebb-126">Выберите **Retail и Commerce** > **Рекомендации продуктов** > **Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="b4ebb-127">В списке общих параметров выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="b4ebb-128">Выберите список, в который требуется добавить или из которого требуется удалить продукты.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="b4ebb-129">Чтобы добавить продукты в таблицу, выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="b4ebb-130">В столбце "Продукт" выполните поиск продукта по **Имя** или по **Номер продукта**.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Пример поиска продукта в списке "Новые товары"](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="b4ebb-132">В столбце "Тип строки" выберите один из двух вариантов:</span><span class="sxs-lookup"><span data-stu-id="b4ebb-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="b4ebb-133">**Включить** — принудительно переводит продукт в начало списка</span><span class="sxs-lookup"><span data-stu-id="b4ebb-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="b4ebb-134">**Исключить** — исключает продукт, не допуская его появления в списке</span><span class="sxs-lookup"><span data-stu-id="b4ebb-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Пример включения или исключения продукта из списка "Новый продукт"](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="b4ebb-136">Изменение значения **Порядок отображения** приведет к изменению порядка, в котором продукты, помеченные как **Включить**, включаются в список.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="b4ebb-137">Если два продукта имеют одинаковое значение **порядок отображения**, то окончательный порядок этих двух результатов также будет зависит от серверной части.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="b4ebb-138">Чтобы удалить продукты из таблицы: выберите удаляемую строку и выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="b4ebb-139">Для списков "Людям также нравится" или "Часто покупают вместе"</span><span class="sxs-lookup"><span data-stu-id="b4ebb-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="b4ebb-140">В контексте списков "Часто покупают вместе" или "Людям часто нравится" машинное обучение используется для анализа шаблонов покупок потребителей с целью рекомендовать связанные продукты, обычно приобретаемые вместе с уникальным начальным продуктом.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="b4ebb-141">*Начальный продукт* — это продукт, для которого необходимо создать результаты.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="b4ebb-142">В контексте ручной настройки списков рекомендаций вы добавляете или удаляете результаты для этого продукта.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="b4ebb-143">Чтобы вручную добавить или удалить результаты для начального продукта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b4ebb-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="b4ebb-144">Выберите **Начальный продукт**.</span><span class="sxs-lookup"><span data-stu-id="b4ebb-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="b4ebb-145">В столбце **Продукт** выполните поиск продукта по параметру **Имя** или **Номер продукта**
![Пример поиска продукта в списке "Часто покупают вместе"](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="b4ebb-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="b4ebb-146">В столбце **Тип строки** выберите один из двух вариантов:</span><span class="sxs-lookup"><span data-stu-id="b4ebb-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="b4ebb-147">**Включить** — принудительно переводит продукт в начало списка</span><span class="sxs-lookup"><span data-stu-id="b4ebb-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="b4ebb-148">**Исключить** — исключает продукт, не допуская его появления в списке</span><span class="sxs-lookup"><span data-stu-id="b4ebb-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="b4ebb-149">![Пример включения или исключения продукта для списка "Часто покупают вместе"](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="b4ebb-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="b4ebb-150">Чтобы удалить продукты из таблицы: выберите удаляемую строку и выберите "Удалить".</span><span class="sxs-lookup"><span data-stu-id="b4ebb-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b4ebb-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4ebb-151">Additional resources</span></span>

[<span data-ttu-id="b4ebb-152">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="b4ebb-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b4ebb-153">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b4ebb-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b4ebb-154">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="b4ebb-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b4ebb-155">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="b4ebb-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b4ebb-156">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="b4ebb-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b4ebb-157">Включение рекомендаций "покупать похожие образы"</span><span class="sxs-lookup"><span data-stu-id="b4ebb-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="b4ebb-158">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="b4ebb-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b4ebb-159">Добавление рекомендаций на экран проводок</span><span class="sxs-lookup"><span data-stu-id="b4ebb-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b4ebb-160">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="b4ebb-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b4ebb-161">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="b4ebb-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b4ebb-162">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="b4ebb-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
