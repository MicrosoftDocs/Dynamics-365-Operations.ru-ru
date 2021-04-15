---
title: Управление метаданными для поисковой оптимизации
description: В этом разделе описывается, как управлять метаданными оптимизации поисковой системы (SEO) в Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794219"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="57df1-103">Управление метаданными SEO</span><span class="sxs-lookup"><span data-stu-id="57df1-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57df1-104">В этом разделе описывается, как управлять метаданными оптимизации поисковой системы (SEO) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="57df1-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="57df1-105">Управление метаданными SEO для сайта может осуществляться с помощью карт сайта и метаданных страниц.</span><span class="sxs-lookup"><span data-stu-id="57df1-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="57df1-106">Карты сайта</span><span class="sxs-lookup"><span data-stu-id="57df1-106">Site maps</span></span>

<span data-ttu-id="57df1-107">Карта сайта — это доступный для чтения компьютером список в формате XML страниц на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="57df1-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="57df1-108">Она предназначена для использования поисковыми системами, чтобы они могли предоставлять лучшие результаты поиска на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="57df1-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="57df1-109">Карты сайта могут быть вручную обработаны поисковыми системами или опубликованы в файле robots.txt.</span><span class="sxs-lookup"><span data-stu-id="57df1-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="57df1-110">Dynamics 365 Commerce поддерживает автоматическое создание карт сайтов.</span><span class="sxs-lookup"><span data-stu-id="57df1-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="57df1-111">Карты сайта автоматически обновляются, когда страницы публикуются и их публикация отменяется.</span><span class="sxs-lookup"><span data-stu-id="57df1-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="57df1-112">Включение создания карты сайта</span><span class="sxs-lookup"><span data-stu-id="57df1-112">Turn on site map generation</span></span>

1. <span data-ttu-id="57df1-113">Войдите в средство разработки.</span><span class="sxs-lookup"><span data-stu-id="57df1-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="57df1-114">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="57df1-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="57df1-115">В области переходов слева выберите **Управление сайтом**.</span><span class="sxs-lookup"><span data-stu-id="57df1-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="57df1-116">Убедитесь, что параметр **Карты сайта включены** включен.</span><span class="sxs-lookup"><span data-stu-id="57df1-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="57df1-117">Метаданные страниц</span><span class="sxs-lookup"><span data-stu-id="57df1-117">Page metadata</span></span>

<span data-ttu-id="57df1-118">Dynamics 365 Commerce позволяет управлять метаданными SEO для отдельных страниц.</span><span class="sxs-lookup"><span data-stu-id="57df1-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="57df1-119">Эти сведения можно просмотреть и изменить в разделе **Свойства SEO** контейнера страницы.</span><span class="sxs-lookup"><span data-stu-id="57df1-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="57df1-120">Поддерживаются следующие свойства метаданных SEO:</span><span class="sxs-lookup"><span data-stu-id="57df1-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="57df1-121">Название должности</span><span class="sxs-lookup"><span data-stu-id="57df1-121">Title</span></span>
- <span data-ttu-id="57df1-122">Описание</span><span class="sxs-lookup"><span data-stu-id="57df1-122">Description</span></span>
- <span data-ttu-id="57df1-123">Ключевые слова SEO</span><span class="sxs-lookup"><span data-stu-id="57df1-123">SEO keywords</span></span>
- <span data-ttu-id="57df1-124">Метки ARIA</span><span class="sxs-lookup"><span data-stu-id="57df1-124">Aria labels</span></span>
- <span data-ttu-id="57df1-125">noindex</span><span class="sxs-lookup"><span data-stu-id="57df1-125">noindex</span></span>
- <span data-ttu-id="57df1-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="57df1-126">nofollow</span></span>
- <span data-ttu-id="57df1-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="57df1-127">noarchive</span></span>
- <span data-ttu-id="57df1-128">nocache</span><span class="sxs-lookup"><span data-stu-id="57df1-128">nocache</span></span>
- <span data-ttu-id="57df1-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="57df1-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="57df1-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="57df1-130">nosnippet</span></span>
- <span data-ttu-id="57df1-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="57df1-131">noImageIndex</span></span>
- <span data-ttu-id="57df1-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="57df1-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="57df1-133">Изменение метаданных страницы</span><span class="sxs-lookup"><span data-stu-id="57df1-133">Modify page metadata</span></span>

<span data-ttu-id="57df1-134">Чтобы изменить метаданные страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="57df1-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="57df1-135">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="57df1-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="57df1-136">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="57df1-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="57df1-137">Выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="57df1-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="57df1-138">На панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="57df1-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="57df1-139">В области свойств справа разверните пункт **Метатеги по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="57df1-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="57df1-140">Чтобы добавить новый метатег, выберите **Добавить**, затем введите тег в поле.</span><span class="sxs-lookup"><span data-stu-id="57df1-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="57df1-141">Чтобы удалить существующий метатег, выберите значок корзины справа от него.</span><span class="sxs-lookup"><span data-stu-id="57df1-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="57df1-142">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="57df1-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="57df1-143">В поле **Комментарии** введите **Обновлены метатеги**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="57df1-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="57df1-144">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="57df1-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="57df1-145">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="57df1-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="57df1-146">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="57df1-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57df1-147">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="57df1-147">Additional resources</span></span>

[<span data-ttu-id="57df1-148">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="57df1-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="57df1-149">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="57df1-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="57df1-150">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="57df1-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="57df1-151">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="57df1-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="57df1-152">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="57df1-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="57df1-153">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="57df1-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="57df1-154">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="57df1-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="57df1-155">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="57df1-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
