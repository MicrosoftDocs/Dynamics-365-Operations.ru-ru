---
title: Вопросы и ответы по рекомендациям по продуктам
description: В этой теме приводятся сведения о процессах и инструментах, которые можно использовать для устранения неполадок, связанных с рекомендациями по продуктам или их результатами.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b3db432ae10139bcd8ee400b0bbc1173e33ef206
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019819"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="1342c-103">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="1342c-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1342c-104">В этой теме приводятся сведения о процессах и инструментах, которые можно использовать для устранения неполадок, связанных с [рекомендациями по продуктам](product-recommendations.md) или их результатами.</span><span class="sxs-lookup"><span data-stu-id="1342c-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="1342c-105">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="1342c-105">Best practices</span></span>
<span data-ttu-id="1342c-106">Очень важно использовать концепцию шаблонов продуктов и вариантов.</span><span class="sxs-lookup"><span data-stu-id="1342c-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="1342c-107">Разумная группировка вариантов с родительским шаблоном продукта помогает создавать алгоритмы списка и сервис создает более эффективные модели.</span><span class="sxs-lookup"><span data-stu-id="1342c-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="1342c-108">Кроме того, служба может обслуживать только один экземпляр продукта вместо размещения всех тесно связанных вариантов в списке.</span><span class="sxs-lookup"><span data-stu-id="1342c-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="1342c-109">Если все тесно связанные друг с другом варианты помещены в список, могут возникать ошибочные или повторяющиеся результаты.</span><span class="sxs-lookup"><span data-stu-id="1342c-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="1342c-110">Почему продуктов нет в моих списках рекомендаций?</span><span class="sxs-lookup"><span data-stu-id="1342c-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="1342c-111">Как правило, если номенклатура отсутствует в списке рекомендаций по продукту, возможно, имеется проблема с конфигурацией продукта.</span><span class="sxs-lookup"><span data-stu-id="1342c-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="1342c-112">Например, может быть неправильная дата начала или окончания продукта, аналитика может быть неправильно настроена, или продукт может находиться в неправильном ассортименте канала и т. д.</span><span class="sxs-lookup"><span data-stu-id="1342c-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="1342c-113">Если номенклатура отсутствует в списке рекомендаций на основе искусственного интеллекта машинного обучения (AI-ML), номенклатура может не удовлетворять критериям списка рекомендаций, или у нее может быть недостаточно проводок покупки для отображения в списке рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="1342c-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="1342c-114">Рекомендуется выполнить проверку следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="1342c-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="1342c-115">**Убедитесь, что в центральном офисе включены рекомендации по продуктам.**</span><span class="sxs-lookup"><span data-stu-id="1342c-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="1342c-116">Дополнительные сведения о включении этой службы см. в разделе [Включение рекомендаций продуктов](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="1342c-117">**Убедитесь, что установлены ключевые свойства продукта.**</span><span class="sxs-lookup"><span data-stu-id="1342c-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="1342c-118">Например, для ассортимента продуктов необходимо задать значение **Включить**.</span><span class="sxs-lookup"><span data-stu-id="1342c-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="1342c-119">**Для новых продуктов в ассортименте может потребоваться до 3 часов, прежде чем продукт начнет отображаться в новом списке.**</span><span class="sxs-lookup"><span data-stu-id="1342c-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="1342c-120">**Если продукт по-прежнему не отображается в списках "Популярное", "Лидеры продаж", "Людям также нравится" или "Часто покупают вместе", то у продукта может быть недостаточно проводок.**</span><span class="sxs-lookup"><span data-stu-id="1342c-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="1342c-121">В этом случае можно подождать, пока не будет больше проводок, обновить параметры списка рекомендаций по умолчанию или использовать ручное вмешательство, чтобы изменить результаты списка рекомендуемых продуктов.</span><span class="sxs-lookup"><span data-stu-id="1342c-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="1342c-122">Дополнительные сведения о параметрах рекомендаций см. в разделе [Управление результатами рекомендаций по продукту на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="1342c-123">**Убедитесь, что продукт соответствует критериям рекомендаций для списка.**</span><span class="sxs-lookup"><span data-stu-id="1342c-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="1342c-124">Дополнительные сведения о параметрах рекомендаций продуктов см. в разделе [Управление результатами рекомендаций по продукту на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="1342c-125">Как предотвратить возврат неправильных результатов рекомендаций?</span><span class="sxs-lookup"><span data-stu-id="1342c-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="1342c-126">Для получения результатов для списков рекомендаций требуется большой объем проводок.</span><span class="sxs-lookup"><span data-stu-id="1342c-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="1342c-127">Таким образом, важно, чтобы пользователи предоставляли полные исторические данные проводок.</span><span class="sxs-lookup"><span data-stu-id="1342c-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="1342c-128">Кроме того, у продуктов, у которых нет проводок или слишком мало проводок, обычно нет результатов **Людям также нравятся** или **Часто покупаются вместе**, и они не появляются в списках **Популярное** или **Лидеры продаж**.</span><span class="sxs-lookup"><span data-stu-id="1342c-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="1342c-129">Эта ситуация часто может возникнуть для совсем новых продуктов или для старых продуктов с небольшим количеством покупок.</span><span class="sxs-lookup"><span data-stu-id="1342c-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="1342c-130">Популярные новые номенклатуры легко преодолеют эту проблему.</span><span class="sxs-lookup"><span data-stu-id="1342c-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="1342c-131">Рекомендуется выполнить следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="1342c-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="1342c-132">**Убедитесь, что продукт соответствует критериям рекомендаций для этого списка.**</span><span class="sxs-lookup"><span data-stu-id="1342c-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="1342c-133">Дополнительные сведения о параметрах рекомендаций продуктов см. в разделе "Изменение результатов рекомендаций по продукту на основе AI-ML".</span><span class="sxs-lookup"><span data-stu-id="1342c-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="1342c-134">**Если продукт является новым, рассмотрите возможность изменения списка рекомендаций до тех пор, пока у продукта не будет больше проводок.**</span><span class="sxs-lookup"><span data-stu-id="1342c-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="1342c-135">Дополнительные сведения о том, как изменить результаты списка рекомендаций, см. в разделе [Управление результатами рекомендаций по продукту на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="1342c-136">**Убедитесь, что продукт соответствует критериям рекомендаций для этого списка.**</span><span class="sxs-lookup"><span data-stu-id="1342c-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="1342c-137">Дополнительные сведения о параметрах рекомендаций продуктов см. в разделе [Управление результатами рекомендаций по продукту на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="1342c-138">**Если продукт является новым, рассмотрите возможность изменения списка рекомендаций до тех пор, пока у продукта не будет больше проводок**.</span><span class="sxs-lookup"><span data-stu-id="1342c-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="1342c-139">Дополнительные сведения о том, как изменить результаты списка рекомендаций, см. в разделе [Управление результатами рекомендаций по продукту на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="1342c-140">Может ли удаленный продукт по-прежнему отображаться в магазине?</span><span class="sxs-lookup"><span data-stu-id="1342c-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="1342c-141">Имеется возможность корректировать списки, которые были созданы алгоритмически, в случае возникновения потребности для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="1342c-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="1342c-142">Однако, если продукт удален из списка рекомендаций, продукт останется доступен в магазине.</span><span class="sxs-lookup"><span data-stu-id="1342c-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="1342c-143">Дополнительные сведения о том, как изменить результаты рекомендаций продуктов, см. в разделе [Управление результатами рекомендаций по продукту на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="1342c-144">Если необходимо блокировать обнаружение номенклатуры в магазине, необходимо изменить значение **ассортимент номенклатуры** на **Исключить**.</span><span class="sxs-lookup"><span data-stu-id="1342c-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="1342c-145">Как добавить список на страницу электронной коммерции?</span><span class="sxs-lookup"><span data-stu-id="1342c-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="1342c-146">Сведения о порядке добавления страниц рекомендаций продуктов на веб-сайт электронной коммерции см. в разделе [Добавление списков рекомендаций продуктов на страницы](./product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](./product-recommendations.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="1342c-147">Как включить рекомендации на POS-терминале?</span><span class="sxs-lookup"><span data-stu-id="1342c-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="1342c-148">После включения рекомендаций продуктов необходимо добавить панель рекомендации на экран управления POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="1342c-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="1342c-149">Дополнительные сведения см. в разделе [Добавление элемента управления рекомендациями на экране проводки на устройствах POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="1342c-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1342c-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1342c-150">Additional resources</span></span>

[<span data-ttu-id="1342c-151">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="1342c-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1342c-152">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1342c-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1342c-153">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="1342c-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="1342c-154">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="1342c-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1342c-155">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="1342c-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1342c-156">Включение рекомендаций "покупать похожие образы"</span><span class="sxs-lookup"><span data-stu-id="1342c-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="1342c-157">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="1342c-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1342c-158">Добавление рекомендаций на экран проводок</span><span class="sxs-lookup"><span data-stu-id="1342c-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1342c-159">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="1342c-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1342c-160">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="1342c-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1342c-161">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="1342c-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]