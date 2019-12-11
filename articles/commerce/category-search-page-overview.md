---
title: Обзор целевой страницы категории и страницы результатов поиска по умолчанию
description: В этом разделе представлен обзор целевой страницы категории по умолчанию и страницы результатов поиска в Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3835502c33fbc63f68f2d6350d805badb3891568
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697298"
---
# <a name="overview-of-default-category-landing-page-and-search-results-page"></a><span data-ttu-id="256dd-103">Обзор целевой страницы категории и страницы результатов поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="256dd-103">Overview of default category landing page and search results page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="256dd-104">В этом разделе представлен обзор целевой страницы категории по умолчанию и страницы результатов поиска в электронной коммерции Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="256dd-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="256dd-105">Целевая страница категории по умолчанию</span><span class="sxs-lookup"><span data-stu-id="256dd-105">Default category landing page</span></span>

<span data-ttu-id="256dd-106">Целевой страницей категории по умолчанию является страница, на которую обычно направляются пользователи веб-сайта при выборе категории в иерархии навигации.</span><span class="sxs-lookup"><span data-stu-id="256dd-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="256dd-107">Страница категории позволяет просматривать, а также выполнять сортировку и уточнение по категориям продуктов.</span><span class="sxs-lookup"><span data-stu-id="256dd-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Целевая страница категории по умолчанию](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="256dd-109">В верхней части страницы находится заголовок, отображающий все категории продуктов и другие страницы, которые были классифицированы менеджером по продажам.</span><span class="sxs-lookup"><span data-stu-id="256dd-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="256dd-110">Настройка выполняется как часть конфигурации иерархии навигации канала.</span><span class="sxs-lookup"><span data-stu-id="256dd-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="256dd-111">В нижней части страницы находится нижний колонтитул, содержащий быстрые ссылки на различные разделы, которые могут интересовать покупателя.</span><span class="sxs-lookup"><span data-stu-id="256dd-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="256dd-112">Следующие компоненты являются важными для категории:</span><span class="sxs-lookup"><span data-stu-id="256dd-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="256dd-113">**Плитки размещения продукта** показывают продукты, которые менеджер по продажам определил в категории в рамках настройки иерархии переходов.</span><span class="sxs-lookup"><span data-stu-id="256dd-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="256dd-114">**Уточнения и сводка выбора** представляют собой фильтры, которые представляют собой подсчитанные значения и могут быть использованы для уточнения номенклатур.</span><span class="sxs-lookup"><span data-stu-id="256dd-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="256dd-115">Менеджер по продажам настраивает их как часть конфигурации метаданных, относящихся к категориям каналов и атрибутам продуктов.</span><span class="sxs-lookup"><span data-stu-id="256dd-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="256dd-116">**Параметры сортировки** используются посетителями веб-сайта для сортировки продуктов.</span><span class="sxs-lookup"><span data-stu-id="256dd-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="256dd-117">По умолчанию доступны следующие параметры сортировки:</span><span class="sxs-lookup"><span data-stu-id="256dd-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="256dd-118">Цена — по возрастанию</span><span class="sxs-lookup"><span data-stu-id="256dd-118">Price – low to high</span></span>
    - <span data-ttu-id="256dd-119">Цена — по убыванию</span><span class="sxs-lookup"><span data-stu-id="256dd-119">Price – high to low</span></span>
    - <span data-ttu-id="256dd-120">Наименование продукта — \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="256dd-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="256dd-121">Наименование продукта — \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="256dd-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="256dd-122">Оценки — по возрастанию</span><span class="sxs-lookup"><span data-stu-id="256dd-122">Ratings – low to high</span></span>
    - <span data-ttu-id="256dd-123">Оценки — по убыванию</span><span class="sxs-lookup"><span data-stu-id="256dd-123">Ratings – high to low</span></span>

- <span data-ttu-id="256dd-124">**Разбивка на страницы** позволяет посетителям веб-сайта перемещаться с одной страницы результатов продуктов по категориям на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="256dd-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="256dd-125">**Общее число** предоставляет общее количество продуктов, определенных в категории.</span><span class="sxs-lookup"><span data-stu-id="256dd-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="256dd-126">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="256dd-126">Enrich a category landing page</span></span>

<span data-ttu-id="256dd-127">Если требуется, чтобы целевая страница категории была более специализированной для определенной категории, можно "обогатить" целевую страницу категории для этой категории.</span><span class="sxs-lookup"><span data-stu-id="256dd-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="256dd-128">Например, можно добавить маркетинговую видеозапись и некоторое повествование по категории, чтобы привлечь внимание покупателей.</span><span class="sxs-lookup"><span data-stu-id="256dd-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="256dd-129">Дополнительные сведения см. в разделе [Обогащение целевой страницы категории](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="256dd-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Обогащенная целевая страница категории](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="256dd-131">Автозаполнение и страницы результатов поиска</span><span class="sxs-lookup"><span data-stu-id="256dd-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="256dd-132">Пользователи веб-сайта могут исследовать сайт, перейдя к категории из иерархии переходов или вводя условие поиска в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="256dd-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="256dd-133">Как только пользователи начинают вводить текст в поле поиска, начинает работать функция автоматического заполнения, предлагающая условия поиска.</span><span class="sxs-lookup"><span data-stu-id="256dd-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="256dd-134">Ниже приведены некоторые типы предложений, которые могут быть показаны:</span><span class="sxs-lookup"><span data-stu-id="256dd-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="256dd-135">**Ключевые слова** используются для поиска номенклатур по всем продуктам, которые включаются в канал.</span><span class="sxs-lookup"><span data-stu-id="256dd-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="256dd-136">**Продукты** содержат прямые ссылки на страницу сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="256dd-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="256dd-137">**Предложения поиска по области категорий** содержат различные категории и позволяют пользователям выполнить поиск по ключевому слову в определенной категории.</span><span class="sxs-lookup"><span data-stu-id="256dd-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Иммерсивное автозаполнение](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="256dd-139">Когда пользователи выбирают одно из предложений ключевых слов или поиска по области категории или если нет предложений для введенного искомого термина, они перенаправлены на страницу результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="256dd-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="256dd-140">Пользователи могут затем просмотреть, отсортировать и уточнить список результатов поиска, чтобы найти нужную номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="256dd-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Целевая страница поиска](./media/SearchLanding.png)

<span data-ttu-id="256dd-142">Следующие компоненты являются важными для страницы результатов поиска:</span><span class="sxs-lookup"><span data-stu-id="256dd-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="256dd-143">**Плитки размещения продукта** отображают продукты для поиска пользователя.</span><span class="sxs-lookup"><span data-stu-id="256dd-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="256dd-144">По умолчанию эти плитки сортируются с помощью облачной оценки релевантности поиска для поиска пользователя.</span><span class="sxs-lookup"><span data-stu-id="256dd-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="256dd-145">**Уточнения и сводка выбора** представляют собой фильтры, которые представляют собой подсчитанные значения и могут быть использованы для уточнения номенклатур.</span><span class="sxs-lookup"><span data-stu-id="256dd-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="256dd-146">Менеджер по продажам настраивает их как часть конфигурации метаданных "категории каналов и атрибуты продуктов".</span><span class="sxs-lookup"><span data-stu-id="256dd-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="256dd-147">**Параметры сортировки** используются посетителями веб-сайта для сортировки продуктов.</span><span class="sxs-lookup"><span data-stu-id="256dd-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="256dd-148">По умолчанию доступны следующие параметры сортировки:</span><span class="sxs-lookup"><span data-stu-id="256dd-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="256dd-149">Цена — по возрастанию</span><span class="sxs-lookup"><span data-stu-id="256dd-149">Price – low to high</span></span>
    - <span data-ttu-id="256dd-150">Цена — по убыванию</span><span class="sxs-lookup"><span data-stu-id="256dd-150">Price – high to low</span></span>
    - <span data-ttu-id="256dd-151">Наименование продукта — \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="256dd-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="256dd-152">Наименование продукта — \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="256dd-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="256dd-153">Оценки — по возрастанию</span><span class="sxs-lookup"><span data-stu-id="256dd-153">Ratings – low to high</span></span>
    - <span data-ttu-id="256dd-154">Оценки — по убыванию</span><span class="sxs-lookup"><span data-stu-id="256dd-154">Ratings – high to low</span></span>
    - <span data-ttu-id="256dd-155">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="256dd-155">Default</span></span>

- <span data-ttu-id="256dd-156">**Разбивка на страницы** позволяет посетителям веб-сайта перемещаться с одной страницы результатов продуктов по категориям на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="256dd-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="256dd-157">**Общее число** предоставляет общее количество продуктов, определенных в категории и соответствующих критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="256dd-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="256dd-158">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="256dd-158">Additional resources</span></span>

[<span data-ttu-id="256dd-159">Обзор домашней страницы</span><span class="sxs-lookup"><span data-stu-id="256dd-159">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="256dd-160">Обзор страниц сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="256dd-160">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="256dd-161">Обзор страниц корзины и оформления заказа</span><span class="sxs-lookup"><span data-stu-id="256dd-161">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="256dd-162">Обзор страниц управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="256dd-162">Overview of account management pages</span></span>](quick-tour-account-management.md)

