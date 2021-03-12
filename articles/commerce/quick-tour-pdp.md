---
title: Обзор страниц сведений о продукте
description: В этом разделе представлен обзор страниц сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b0f50b4e7b78f4a5b9fe674a101476879923e10d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979836"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="e99ef-103">Обзор страниц сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="e99ef-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e99ef-104">В этом разделе представлен обзор страниц сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e99ef-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e99ef-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e99ef-105">Overview</span></span>

<span data-ttu-id="e99ef-106">Страница PDP предоставляет подробные сведения о продукте, и клиенты могут выбирать параметры продукта, такие как размер, стиль и цвет.</span><span class="sxs-lookup"><span data-stu-id="e99ef-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="e99ef-107">Страница PDP должна показать все сведения о продукте, необходимые клиенту для принятия решения о покупке.</span><span class="sxs-lookup"><span data-stu-id="e99ef-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="e99ef-108">Следующая иллюстрация показывает пример страницы сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="e99ef-108">The following illustration shows an example of a PDP.</span></span>

![Пример страницы сведений о продукте](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="e99ef-110">Модули заголовка и нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="e99ef-110">Header and footer modules</span></span>

<span data-ttu-id="e99ef-111">В верхней части страницы PDP имеется заголовок, отображающий все категории продуктов и другие страницы, которые предприятие розничной торговли хочет, чтобы они просматривались пользователями.</span><span class="sxs-lookup"><span data-stu-id="e99ef-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="e99ef-112">В нижней части страницы находится нижний колонтитул, содержащий быстрые ссылки на различные разделы, которые могут интересовать клиентов.</span><span class="sxs-lookup"><span data-stu-id="e99ef-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="e99ef-113">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="e99ef-113">Buy box module</span></span>

<span data-ttu-id="e99ef-114">Наиболее важным модулем в PDP является модуль поля покупки, который отображается как первый элемент в главном разделе страницы.</span><span class="sxs-lookup"><span data-stu-id="e99ef-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="e99ef-115">Модуль поля покупки содержит важную информацию о продукте, такую как наименование продукта, описание продукта, цену продукта, изображения продукта и оценки продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="e99ef-116">Модуль поля покупки позволяет клиенту выбирать параметры продукта (например, размер, стиль и цвет) и добавить продукт в корзину.</span><span class="sxs-lookup"><span data-stu-id="e99ef-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="e99ef-117">Он также позволяет покупателю купить продукт по Интернету и забрать его в магазине.</span><span class="sxs-lookup"><span data-stu-id="e99ef-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="e99ef-118">Модель покупки через Интернет и получения в магазине использует интеграцию с интерфейсами прикладного программирования (API) карт Bing, чтобы найти ближайшие магазины или магазины в другом местоположении, указанном клиентом.</span><span class="sxs-lookup"><span data-stu-id="e99ef-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="e99ef-119">Для модуля поля покупки требуется код продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="e99ef-120">Этот код извлекается из контекста страницы.</span><span class="sxs-lookup"><span data-stu-id="e99ef-120">This ID is derived from the page context.</span></span> <span data-ttu-id="e99ef-121">Если модуль поля покупки добавляется на страницу, где контекст страницы не содержит идентификатора продукта, информация не будет правильно отображена.</span><span class="sxs-lookup"><span data-stu-id="e99ef-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="e99ef-122">Модуль детализации продукта</span><span class="sxs-lookup"><span data-stu-id="e99ef-122">Product specifications module</span></span>

<span data-ttu-id="e99ef-123">Модуль спецификаций продукта может использоваться для демонстрации дополнительной информации о продукте.</span><span class="sxs-lookup"><span data-stu-id="e99ef-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="e99ef-124">Эти сведения взяты из атрибутов продукта в Commerce.</span><span class="sxs-lookup"><span data-stu-id="e99ef-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="e99ef-125">В модуле спецификаций продукта отображается каждый атрибут, в котором свойство **видимо** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e99ef-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="e99ef-126">Для получения атрибутов продукта требуется код продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="e99ef-127">Модуль рекомендаций</span><span class="sxs-lookup"><span data-stu-id="e99ef-127">Recommendations module</span></span>

<span data-ttu-id="e99ef-128">Модуль рекомендаций является важным модулем на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="e99ef-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="e99ef-129">Когда клиенты просматривают продукты, для них должны быть представлены дополнительные варианты продуктов, чтобы они могли найти правильный продукт и выполнить покупку.</span><span class="sxs-lookup"><span data-stu-id="e99ef-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="e99ef-130">Рекомендации помогают клиентам легко обнаруживать связанное содержимое и продолжать покупать.</span><span class="sxs-lookup"><span data-stu-id="e99ef-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="e99ef-131">Доступны различные типы списков рекомендаций:</span><span class="sxs-lookup"><span data-stu-id="e99ef-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="e99ef-132">Список **Людям также нравится** базируется на машинном обучении.</span><span class="sxs-lookup"><span data-stu-id="e99ef-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="e99ef-133">Для обеспечения рекомендаций используется история проводок других клиентов.</span><span class="sxs-lookup"><span data-stu-id="e99ef-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="e99ef-134">Этот список создается службой рекомендаций и напоминает списки "Клиенты, которые приобрели этот товар, также купили...".</span><span class="sxs-lookup"><span data-stu-id="e99ef-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="e99ef-135">Для создания этого списка необходим код продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="e99ef-136">Список **Связанные** может быть настроен для продукта в Commerce.</span><span class="sxs-lookup"><span data-stu-id="e99ef-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="e99ef-137">Например, для коричневой кожаной дорожной сумочки для списка связанных товаров могут быть настроены сумочки, изготовленные из кожи или предназначенные для путешествий.</span><span class="sxs-lookup"><span data-stu-id="e99ef-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="e99ef-138">Другие типы связанных списков, такие как **Аксессуары** и **Еще похожие**, можно также настроить в Commerce.</span><span class="sxs-lookup"><span data-stu-id="e99ef-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="e99ef-139">Для создания этого списка необходим код продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="e99ef-140">Таким образом, при добавлении на домашнюю страницу, в которой контекст страницы не содержит идентификатора продукта, список будет пустым.</span><span class="sxs-lookup"><span data-stu-id="e99ef-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="e99ef-141">Алгоритмически созданные списки рекомендаций, такие как **Тенденции**, **Лидеры продаж** и **Новые**, могут использоваться на страницах сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="e99ef-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="e99ef-142">Хотя эти списки могут не быть непосредственно связанными с продуктом на странице PDP, они являются еще одним способом помочь клиентам найти продукты, которые могут интересовать их.</span><span class="sxs-lookup"><span data-stu-id="e99ef-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="e99ef-143">Эти типы списков не требуют наличия кода продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="e99ef-144">Они являются универсальными списками, которые создаются на основе шаблонов покупок внутри сайта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="e99ef-145">Редакционные списки — это созданные вручную списки.</span><span class="sxs-lookup"><span data-stu-id="e99ef-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="e99ef-146">Например, розничная сеть может решить, что следует вручную создать списки продуктов, которые они хотят показать.</span><span class="sxs-lookup"><span data-stu-id="e99ef-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="e99ef-147">Модули оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="e99ef-147">Ratings and reviews modules</span></span>

<span data-ttu-id="e99ef-148">Для просмотра и добавления отзывов можно использовать три модуля:</span><span class="sxs-lookup"><span data-stu-id="e99ef-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="e99ef-149">**Оценки** — в этом модуле отображаются оценки и отзывы, предоставляемые другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="e99ef-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="e99ef-150">Клиенты могут отсортировать и отфильтровать оценки.</span><span class="sxs-lookup"><span data-stu-id="e99ef-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="e99ef-151">Этот модуль также дает клиентам возможность ставить отметки "нравится" или "не нравится" и сообщать о проблемах.</span><span class="sxs-lookup"><span data-stu-id="e99ef-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="e99ef-152">**Написать отзыв** — с помощью этого модуля клиенты могут создавать свои собственные отзывы о продукте.</span><span class="sxs-lookup"><span data-stu-id="e99ef-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="e99ef-153">**Гистограмма оценок** — этот модуль содержит гистограмму, в которой показана тенденция оценок продукта.</span><span class="sxs-lookup"><span data-stu-id="e99ef-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="e99ef-154">Дополнительные сведения см. в разделе [Обзор оценок и отзывов](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e99ef-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="e99ef-155">Модули маркетинга</span><span class="sxs-lookup"><span data-stu-id="e99ef-155">Marketing modules</span></span>

<span data-ttu-id="e99ef-156">Если маркетинговое содержимое является уникальным для конкретного продукта, на странице сведений о продукте можно добавить любой модуль маркетинга.</span><span class="sxs-lookup"><span data-stu-id="e99ef-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="e99ef-157">На страницу PDP можно добавлять модули маркетинга, "обогащая" страницу.</span><span class="sxs-lookup"><span data-stu-id="e99ef-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="e99ef-158">Дополнительные сведения см. в разделе [Расширение возможностей страницы продукта](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="e99ef-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e99ef-159">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e99ef-159">Additional resources</span></span>

[<span data-ttu-id="e99ef-160">Обзор домашней страницы</span><span class="sxs-lookup"><span data-stu-id="e99ef-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="e99ef-161">Обзор страниц корзины и оформления заказа</span><span class="sxs-lookup"><span data-stu-id="e99ef-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="e99ef-162">Обзор страниц управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="e99ef-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="e99ef-163">Страница сведений о расширении возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="e99ef-163">Enrich a product details page</span></span>](enrich-product-page.md)
