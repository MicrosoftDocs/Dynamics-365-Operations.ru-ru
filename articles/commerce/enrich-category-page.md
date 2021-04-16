---
title: Расширение возможностей целевой страницы категории
description: В этом разделе описывается обогащение страниц категорий в Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799019"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="1ec94-103">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="1ec94-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ec94-104">В этом разделе описывается обогащение страниц категорий в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1ec94-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1ec94-105">Commerce предоставляет целевую страницу категории по умолчанию, которая используется при отображении данных категорий.</span><span class="sxs-lookup"><span data-stu-id="1ec94-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="1ec94-106">Страница категории по умолчанию содержит обязательные элементы, такие как уточнения, размещение товаров по категориям, параметры сортировки, сводка по выбору и элементы управления разбивкой на страницы.</span><span class="sxs-lookup"><span data-stu-id="1ec94-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="1ec94-107">Однако вместо того, чтобы использовать страницу категории по умолчанию, можно использовать "обогащенную" целевую страницу категории, имеющую больше содержимого и более специфичные элементы.</span><span class="sxs-lookup"><span data-stu-id="1ec94-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="1ec94-108">Типичное обогащение может включать добавление маркетинговой информации, относящейся к категории, на страницу категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="1ec94-109">Это содержимое может включать в себя размещение продуктов в различных категориях для целей перекрестных продаж, редакционные списки, изображения, видео и другой текст.</span><span class="sxs-lookup"><span data-stu-id="1ec94-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="1ec94-110">Можно изменить страницу категории по умолчанию или определить отдельную страницу категории для определенной категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Обогащенная целевая страница категории](./media/CategoryLandingPages.png)

<span data-ttu-id="1ec94-112">В конструкторе сайтов Commerce страница **Продукты** включает список категорий из канала, назначенного сайту.</span><span class="sxs-lookup"><span data-stu-id="1ec94-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="1ec94-113">Если для страницы категории выбрано состояние **Обогащенная**, страница категории является расширенной.</span><span class="sxs-lookup"><span data-stu-id="1ec94-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="1ec94-114">В противном случае для данной категории используется страница категории и содержимое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ec94-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="1ec94-115">Можно просмотреть как обогащенные, так и необогащенные страницы категории для категории, выбрав название категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="1ec94-116">Чтобы расширить страницу категории, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1ec94-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="1ec94-117">На странице **Продукты** выберите имя категории, для которой необходимо расширить страницу категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="1ec94-118">Страница категории по умолчанию для выбранной категории открывается в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="1ec94-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="1ec94-119">Выберите **Обогатить страницу категории**.</span><span class="sxs-lookup"><span data-stu-id="1ec94-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="1ec94-120">Выберите шаблон обогащенной страницы категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="1ec94-121">Если вносятся только небольшие изменения, можно выбрать страницу категории по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ec94-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="1ec94-122">В качестве альтернативы можно выбрать конкретный шаблон страницы категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="1ec94-123">При выборе шаблона открывается редактор страниц, и выбранный шаблон используется для создания новой страницы категории для выбранной категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="1ec94-124">Страница извлекается для вас, и теперь можно вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="1ec94-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="1ec94-125">Модули, в которых используются данные спецификации категории, используют данные из выбранной категории.</span><span class="sxs-lookup"><span data-stu-id="1ec94-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="1ec94-126">Выбранные настройки шаблона определяют изменения, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="1ec94-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ec94-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1ec94-127">Additional resources</span></span>

[<span data-ttu-id="1ec94-128">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="1ec94-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="1ec94-129">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="1ec94-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1ec94-130">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="1ec94-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1ec94-131">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="1ec94-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="1ec94-132">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="1ec94-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1ec94-133">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="1ec94-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1ec94-134">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="1ec94-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="1ec94-135">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="1ec94-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
