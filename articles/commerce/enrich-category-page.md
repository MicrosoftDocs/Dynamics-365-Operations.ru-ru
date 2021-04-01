---
title: Расширение возможностей целевой страницы категории
description: В этом разделе описывается обогащение страниц категорий в Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fbcf6ec60723b726e022b4e17bbde4c903e5cb57
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238793"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="46173-103">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="46173-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="46173-104">В этом разделе описывается обогащение страниц категорий в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="46173-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="46173-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="46173-105">Overview</span></span>

<span data-ttu-id="46173-106">Commerce предоставляет целевую страницу категории по умолчанию, которая используется при отображении данных категорий.</span><span class="sxs-lookup"><span data-stu-id="46173-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="46173-107">Страница категории по умолчанию содержит обязательные элементы, такие как уточнения, размещение товаров по категориям, параметры сортировки, сводка по выбору и элементы управления разбивкой на страницы.</span><span class="sxs-lookup"><span data-stu-id="46173-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="46173-108">Однако вместо того, чтобы использовать страницу категории по умолчанию, можно использовать "обогащенную" целевую страницу категории, имеющую больше содержимого и более специфичные элементы.</span><span class="sxs-lookup"><span data-stu-id="46173-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="46173-109">Типичное обогащение может включать добавление маркетинговой информации, относящейся к категории, на страницу категории.</span><span class="sxs-lookup"><span data-stu-id="46173-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="46173-110">Это содержимое может включать в себя размещение продуктов в различных категориях для целей перекрестных продаж, редакционные списки, изображения, видео и другой текст.</span><span class="sxs-lookup"><span data-stu-id="46173-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="46173-111">Можно изменить страницу категории по умолчанию или определить отдельную страницу категории для определенной категории.</span><span class="sxs-lookup"><span data-stu-id="46173-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Обогащенная целевая страница категории](./media/CategoryLandingPages.png)

<span data-ttu-id="46173-113">В конструкторе сайтов Commerce страница **Продукты** включает список категорий из канала, назначенного сайту.</span><span class="sxs-lookup"><span data-stu-id="46173-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="46173-114">Если для страницы категории выбрано состояние **Обогащенная**, страница категории является расширенной.</span><span class="sxs-lookup"><span data-stu-id="46173-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="46173-115">В противном случае для данной категории используется страница категории и содержимое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46173-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="46173-116">Можно просмотреть как обогащенные, так и необогащенные страницы категории для категории, выбрав название категории.</span><span class="sxs-lookup"><span data-stu-id="46173-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="46173-117">Чтобы расширить страницу категории, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="46173-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="46173-118">На странице **Продукты** выберите имя категории, для которой необходимо расширить страницу категории.</span><span class="sxs-lookup"><span data-stu-id="46173-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="46173-119">Страница категории по умолчанию для выбранной категории открывается в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="46173-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="46173-120">Выберите **Обогатить страницу категории**.</span><span class="sxs-lookup"><span data-stu-id="46173-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="46173-121">Выберите шаблон обогащенной страницы категории.</span><span class="sxs-lookup"><span data-stu-id="46173-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="46173-122">Если вносятся только небольшие изменения, можно выбрать страницу категории по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46173-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="46173-123">В качестве альтернативы можно выбрать конкретный шаблон страницы категории.</span><span class="sxs-lookup"><span data-stu-id="46173-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="46173-124">При выборе шаблона открывается редактор страниц, и выбранный шаблон используется для создания новой страницы категории для выбранной категории.</span><span class="sxs-lookup"><span data-stu-id="46173-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="46173-125">Страница извлекается для вас, и теперь можно вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="46173-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="46173-126">Модули, в которых используются данные спецификации категории, используют данные из выбранной категории.</span><span class="sxs-lookup"><span data-stu-id="46173-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="46173-127">Выбранные настройки шаблона определяют изменения, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="46173-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46173-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="46173-128">Additional resources</span></span>

[<span data-ttu-id="46173-129">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="46173-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="46173-130">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="46173-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="46173-131">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="46173-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="46173-132">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="46173-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="46173-133">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="46173-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="46173-134">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="46173-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="46173-135">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="46173-135">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="46173-136">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="46173-136">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]