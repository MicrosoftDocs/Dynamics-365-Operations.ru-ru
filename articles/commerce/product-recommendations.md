---
title: Обзор рекомендаций по продуктам
description: В этом разделе приводятся общие сведения о рекомендациях продуктов. Рекомендации по продуктам позволяют пользователям легко и быстро находить нужные продукты и даже те продукты, которые они изначально не планировали покупать.
author: Moonma
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
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 044a5c21e4ebf1bf83edc74335e655b9388bc1d4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795605"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="b4d6a-104">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="b4d6a-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4d6a-105">Microsoft Dynamics 365 Commerce может использоваться для демонстрации рекомендаций по продуктам на веб-сайте электронной коммерции и на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="b4d6a-106">Рекомендации продуктов — это номенклатуры, которые могут заинтересовать клиента.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="b4d6a-107">Рекомендации основаны на тенденциях покупки других клиентов в интернет-магазинах и обычных магазинах.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="b4d6a-108">Рекомендации продуктов позволяют пользователям легко и быстро находить нужные им продукты, в то время как они имеют опыт, который хорошо им помогает.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="b4d6a-109">Перекрестные продажи и дополнительные продажи могут быть даже использованы, чтобы помочь клиентам найти другие продукты, которые они изначально не планировали покупать.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="b4d6a-110">При использовании рекомендаций для улучшения обнаружения продуктов они могут создавать дополнительные возможности конверсии, повышать доходы от продаж и даже улучшать степень удовлетворенности и удержания клиентов.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="b4d6a-111">В электронной коммерции рекомендации по продуктам производятся на основе технологий машинного обучения рекомендациям корпорации Microsoft в больших масштабах.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="b4d6a-112">Служба рекомендаций</span><span class="sxs-lookup"><span data-stu-id="b4d6a-112">Recommendation service</span></span>

<span data-ttu-id="b4d6a-113">Служба рекомендаций продуктов использует технологии искусственного интеллекта и машинного обучения (AI-ML) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4d6a-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="b4d6a-114">Данные в формате, требуемом службой рекомендаций, извлекаются из операционной базы данных Commerce и отправляются в Azure Data Lake Storage или хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="b4d6a-115">Служба рекомендаций использует сохраненные данные для обучения моделей рекомендаций для списков **Людям также нравятся**, **Часто покупаются вместе**, **Новое**, **Лидеры продаж** и **Популярное**.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="b4d6a-116">Сценарии</span><span class="sxs-lookup"><span data-stu-id="b4d6a-116">Scenarios</span></span>

<span data-ttu-id="b4d6a-117">Рекомендации по продукции доступны в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="b4d6a-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="b4d6a-118">**На любой странице магазина для обзора или целевой странице электронной коммерции**: если клиенты или продавцы магазина посетят страницу магазина, подсистема рекомендаций может предлагать продукты в списках **Новые**, **Лидеры продаж** и **Популярные**.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="b4d6a-119">**На странице сведений о продукте**: если клиенты или продавцы магазина посещают страницу **Сведения о продукте**, подсистема рекомендаций предлагает дополнительные номенклатуры, которые также могут быть приобретены с высокой вероятностью.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="b4d6a-120">Эти номенклатуры отображаются в списке **Людям также нравится**.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="b4d6a-121">**На странице проводки или на странице оформления заказа:** механизм рекомендаций предлагает номенклатуры, основываясь на полном списке номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="b4d6a-122">Эти номенклатуры отображаются в списке **Вместе с этими товарами часто покупают**.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="b4d6a-123">**Персонализированные рекомендации**: продавцы могут предоставлять пользователям, вошедшим в систему, персонализированный список **Для вас**, а также новые функции, которые позволяют персонализировать существующие сценарии со списками на основе этого клиента.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="b4d6a-124">Дополнительные сведения см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b4d6a-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="b4d6a-125">Типы рекомендаций продуктов</span><span class="sxs-lookup"><span data-stu-id="b4d6a-125">Types of product recommendations</span></span>

<span data-ttu-id="b4d6a-126">В следующей таблице описываются различные типы автоматизированных рекомендаций продуктов, которые могут быть реализованы в решении Dynamics 365 Commerce в розничной торговли с помощью [модуля коллекции продуктов](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b4d6a-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="b4d6a-127">Розничные торговцы могут также отображать персонализированные результаты для пользователя, выполнившего вход, если автор сайта выбирает этот вариант.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="b4d6a-128">Модуль семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="b4d6a-128">Product collection module</span></span>  | <span data-ttu-id="b4d6a-129">Вид</span><span class="sxs-lookup"><span data-stu-id="b4d6a-129">Type</span></span> | <span data-ttu-id="b4d6a-130">описание</span><span class="sxs-lookup"><span data-stu-id="b4d6a-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="b4d6a-131">Сoздать</span><span class="sxs-lookup"><span data-stu-id="b4d6a-131">New</span></span>                        | <span data-ttu-id="b4d6a-132">Алгоритмический</span><span class="sxs-lookup"><span data-stu-id="b4d6a-132">Algorithmic</span></span> | <span data-ttu-id="b4d6a-133">Этот модуль отображает список новейших продуктов, которые были недавно добавлены в каналы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="b4d6a-134">Лидеры продаж</span><span class="sxs-lookup"><span data-stu-id="b4d6a-134">Best selling</span></span>               | <span data-ttu-id="b4d6a-135">Алгоритмический</span><span class="sxs-lookup"><span data-stu-id="b4d6a-135">Algorithmic</span></span> | <span data-ttu-id="b4d6a-136">В этом модуле отображается список продуктов, которые ранжированы по наибольшему количеству продаж.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="b4d6a-137">Популярные</span><span class="sxs-lookup"><span data-stu-id="b4d6a-137">Trending</span></span>                   | <span data-ttu-id="b4d6a-138">Алгоритмический</span><span class="sxs-lookup"><span data-stu-id="b4d6a-138">Algorithmic</span></span> | <span data-ttu-id="b4d6a-139">Этот модуль отображает список самых эффективных продуктов для данного периода, отсортированных по наибольшему количеству продаж.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="b4d6a-140">Часто покупают вместе</span><span class="sxs-lookup"><span data-stu-id="b4d6a-140">Frequently bought together</span></span> | <span data-ttu-id="b4d6a-141">Искусственный интеллект – машинное обучение</span><span class="sxs-lookup"><span data-stu-id="b4d6a-141">AI-ML</span></span> | <span data-ttu-id="b4d6a-142">Этот модуль рекомендует список продуктов, которые обычно приобретают вместе с содержимым текущей корзины клиентов.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="b4d6a-143">Людям также нравится</span><span class="sxs-lookup"><span data-stu-id="b4d6a-143">People also like</span></span>           | <span data-ttu-id="b4d6a-144">Искусственный интеллект – машинное обучение</span><span class="sxs-lookup"><span data-stu-id="b4d6a-144">AI-ML</span></span> | <span data-ttu-id="b4d6a-145">Этот модуль рекомендует продукты для данного начального продукта на основе шаблонов покупок клиента.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="b4d6a-146">Для вас</span><span class="sxs-lookup"><span data-stu-id="b4d6a-146">Picks for you</span></span>              | <span data-ttu-id="b4d6a-147">Искусственный интеллект – машинное обучение</span><span class="sxs-lookup"><span data-stu-id="b4d6a-147">AI-ML</span></span> | <span data-ttu-id="b4d6a-148">Этот модуль рекомендует персонализированный список продуктов, основанный на шаблонах покупок вошедшего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="b4d6a-149">Для гостевого пользователя этот список будет свернут.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b4d6a-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4d6a-150">Additional resources</span></span>

[<span data-ttu-id="b4d6a-151">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b4d6a-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b4d6a-152">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="b4d6a-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b4d6a-153">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="b4d6a-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b4d6a-154">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="b4d6a-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b4d6a-155">Включение рекомендаций "покупать похожие образы"</span><span class="sxs-lookup"><span data-stu-id="b4d6a-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="b4d6a-156">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="b4d6a-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b4d6a-157">Добавление рекомендаций на экран проводок</span><span class="sxs-lookup"><span data-stu-id="b4d6a-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b4d6a-158">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="b4d6a-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b4d6a-159">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="b4d6a-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b4d6a-160">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="b4d6a-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b4d6a-161">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="b4d6a-161">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]