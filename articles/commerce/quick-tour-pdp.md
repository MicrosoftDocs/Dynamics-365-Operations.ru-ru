---
title: Обзор страниц сведений о продукте
description: В этом разделе представлен обзор страниц сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697873"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="98c65-103">Обзор страниц сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="98c65-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="98c65-104">В этом разделе представлен обзор страниц сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="98c65-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="98c65-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="98c65-105">Overview</span></span>

<span data-ttu-id="98c65-106">Страница PDP предоставляет подробные сведения о продукте, и клиенты могут выбирать параметры продукта, такие как размер, стиль и цвет.</span><span class="sxs-lookup"><span data-stu-id="98c65-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="98c65-107">Страница PDP должна показать все сведения о продукте, необходимые клиенту для принятия решения о покупке.</span><span class="sxs-lookup"><span data-stu-id="98c65-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="98c65-108">Следующая иллюстрация показывает пример страницы сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="98c65-108">The following illustration shows an example of a PDP.</span></span>

![Пример страницы сведений о продукте](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="98c65-110">Модули заголовка и нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="98c65-110">Header and footer modules</span></span>

<span data-ttu-id="98c65-111">В верхней части страницы PDP имеется заголовок, отображающий все категории продуктов и другие страницы, которые предприятие розничной торговли хочет, чтобы они просматривались пользователями.</span><span class="sxs-lookup"><span data-stu-id="98c65-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="98c65-112">В нижней части страницы находится нижний колонтитул, содержащий быстрые ссылки на различные разделы, которые могут интересовать клиентов.</span><span class="sxs-lookup"><span data-stu-id="98c65-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="98c65-113">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="98c65-113">Buy box module</span></span>

<span data-ttu-id="98c65-114">Наиболее важным модулем страницы PDP является модуль поля покупки.</span><span class="sxs-lookup"><span data-stu-id="98c65-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="98c65-115">Таким образом, это первый элемент в основном разделе страницы.</span><span class="sxs-lookup"><span data-stu-id="98c65-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="98c65-116">Модуль поля покупки — это модуль-контейнер, который содержит несколько модулей, содержащих наиболее важную информацию о продукте.</span><span class="sxs-lookup"><span data-stu-id="98c65-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="98c65-117">Эти сведения включают название продукта, изображения продукта, описание, цену и рейтинги продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="98c65-118">Модуль поля покупки позволяет клиенту выбирать параметры продукта (например, размер, стиль и цвет) и добавить продукт в корзину.</span><span class="sxs-lookup"><span data-stu-id="98c65-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="98c65-119">Он также позволяет покупателю купить продукт по Интернету и забрать его в магазине.</span><span class="sxs-lookup"><span data-stu-id="98c65-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="98c65-120">Модель покупки через Интернет и получения в магазине использует интеграцию с интерфейсами прикладного программирования (API) карт Bing, чтобы найти ближайшие магазины или магазины в другом местоположении, указанном клиентом.</span><span class="sxs-lookup"><span data-stu-id="98c65-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="98c65-121">Для модуля поля покупки требуется код продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="98c65-122">Этот код извлекается из контекста страницы.</span><span class="sxs-lookup"><span data-stu-id="98c65-122">This ID is derived from the page context.</span></span> <span data-ttu-id="98c65-123">Если модуль поля покупки добавляется на страницу, где контекст страницы не содержит идентификатора продукта, информация не будет правильно отображена.</span><span class="sxs-lookup"><span data-stu-id="98c65-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="98c65-124">Модуль детализации продукта</span><span class="sxs-lookup"><span data-stu-id="98c65-124">Product specifications module</span></span>

<span data-ttu-id="98c65-125">Модуль спецификаций продукта может использоваться для демонстрации дополнительной информации о продукте.</span><span class="sxs-lookup"><span data-stu-id="98c65-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="98c65-126">Эти сведения взяты из атрибутов продукта в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="98c65-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="98c65-127">В модуле спецификаций продукта отображается каждый атрибут, в котором свойство **видимо** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="98c65-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="98c65-128">Для получения атрибутов продукта требуется код продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="98c65-129">Модуль рекомендаций</span><span class="sxs-lookup"><span data-stu-id="98c65-129">Recommendations module</span></span>

<span data-ttu-id="98c65-130">Модуль рекомендаций является важным модулем на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="98c65-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="98c65-131">Когда клиенты просматривают продукты, для них должны быть представлены дополнительные варианты продуктов, чтобы они могли найти правильный продукт и выполнить покупку.</span><span class="sxs-lookup"><span data-stu-id="98c65-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="98c65-132">Рекомендации помогают клиентам легко обнаруживать связанное содержимое и продолжать покупать.</span><span class="sxs-lookup"><span data-stu-id="98c65-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="98c65-133">Доступны различные типы списков рекомендаций:</span><span class="sxs-lookup"><span data-stu-id="98c65-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="98c65-134">Список **Людям также нравится** базируется на машинном обучении.</span><span class="sxs-lookup"><span data-stu-id="98c65-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="98c65-135">Для обеспечения рекомендаций используется история проводок других клиентов.</span><span class="sxs-lookup"><span data-stu-id="98c65-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="98c65-136">Этот список создается службой рекомендаций и напоминает списки "Клиенты, которые приобрели этот товар, также купили...".</span><span class="sxs-lookup"><span data-stu-id="98c65-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="98c65-137">Для создания этого списка необходим код продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="98c65-138">Список **Связанные** может быть настроен для продукта в Retail.</span><span class="sxs-lookup"><span data-stu-id="98c65-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="98c65-139">Например, для коричневой кожаной дорожной сумочки для списка связанных товаров могут быть настроены сумочки, изготовленные из кожи или предназначенные для путешествий.</span><span class="sxs-lookup"><span data-stu-id="98c65-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="98c65-140">Другие типы связанных списков, такие как **Аксессуары** и **Еще похожие**, можно также настроить в Retail.</span><span class="sxs-lookup"><span data-stu-id="98c65-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="98c65-141">Для создания этого списка необходим код продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="98c65-142">Таким образом, при добавлении на домашнюю страницу, в которой контекст страницы не содержит идентификатора продукта, список будет пустым.</span><span class="sxs-lookup"><span data-stu-id="98c65-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="98c65-143">Алгоритмически созданные списки рекомендаций, такие как **Тенденции**, **Лидеры продаж** и **Новые**, могут использоваться на страницах сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="98c65-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="98c65-144">Хотя эти списки могут не быть непосредственно связанными с продуктом на странице PDP, они являются еще одним способом помочь клиентам найти продукты, которые могут интересовать их.</span><span class="sxs-lookup"><span data-stu-id="98c65-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="98c65-145">Эти типы списков не требуют наличия кода продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="98c65-146">Они являются универсальными списками, которые создаются на основе шаблонов покупок внутри сайта.</span><span class="sxs-lookup"><span data-stu-id="98c65-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="98c65-147">Редакционные списки — это созданные вручную списки.</span><span class="sxs-lookup"><span data-stu-id="98c65-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="98c65-148">Например, розничная сеть может решить, что следует вручную создать списки продуктов, которые они хотят показать.</span><span class="sxs-lookup"><span data-stu-id="98c65-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="98c65-149">Модуль оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="98c65-149">Ratings and reviews module</span></span>

<span data-ttu-id="98c65-150">В модуле оценок и отзывов отображаются оценки и отзывы, предоставляемые другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="98c65-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="98c65-151">Он также позволяет клиенту написать собственный отзыв о продукте.</span><span class="sxs-lookup"><span data-stu-id="98c65-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="98c65-152">Кроме того, в нем содержится гистограмма, в которой показана тенденция оценок для продукта.</span><span class="sxs-lookup"><span data-stu-id="98c65-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="98c65-153">Дополнительные сведения см. в разделе [Обзор оценок и отзывов](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98c65-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="98c65-154">Модули маркетинга</span><span class="sxs-lookup"><span data-stu-id="98c65-154">Marketing modules</span></span>

<span data-ttu-id="98c65-155">Если маркетинговое содержимое является уникальным для конкретного продукта, на странице сведений о продукте можно добавить любой модуль маркетинга.</span><span class="sxs-lookup"><span data-stu-id="98c65-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="98c65-156">На страницу PDP можно добавлять модули маркетинга, "обогащая" страницу.</span><span class="sxs-lookup"><span data-stu-id="98c65-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="98c65-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98c65-157">Additional resources</span></span>

[<span data-ttu-id="98c65-158">Обзор домашней страницы</span><span class="sxs-lookup"><span data-stu-id="98c65-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="98c65-159">Обзор целевой страницы категории и страницы результатов поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="98c65-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="98c65-160">Обзор страниц корзины и оформления заказа</span><span class="sxs-lookup"><span data-stu-id="98c65-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="98c65-161">Обзор страниц управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="98c65-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
