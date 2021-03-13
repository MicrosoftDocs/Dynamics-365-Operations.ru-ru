---
title: Управление метаданными для поисковой оптимизации
description: В этом разделе описывается, как управлять метаданными оптимизации поисковой системы (SEO) в Microsoft Dynamics 365 Commerce.
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c7cf9e76ffb30ee5c8bba318b2644e67c757bff0
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097423"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="95c4f-103">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="95c4f-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="95c4f-104">В этом разделе описывается, как управлять метаданными оптимизации поисковой системы (SEO) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="95c4f-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="95c4f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="95c4f-105">Overview</span></span>

<span data-ttu-id="95c4f-106">Управление метаданными SEO для сайта может осуществляться с помощью карт сайта и метаданных страниц.</span><span class="sxs-lookup"><span data-stu-id="95c4f-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="95c4f-107">Карты сайта</span><span class="sxs-lookup"><span data-stu-id="95c4f-107">Site maps</span></span>

<span data-ttu-id="95c4f-108">Карта сайта — это доступный для чтения компьютером список в формате XML страниц на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="95c4f-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="95c4f-109">Она предназначена для использования поисковыми системами, чтобы они могли предоставлять лучшие результаты поиска на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="95c4f-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="95c4f-110">Карты сайта могут быть вручную обработаны поисковыми системами или опубликованы в файле robots.txt.</span><span class="sxs-lookup"><span data-stu-id="95c4f-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="95c4f-111">Dynamics 365 Commerce поддерживает автоматическое создание карт сайтов.</span><span class="sxs-lookup"><span data-stu-id="95c4f-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="95c4f-112">Карты сайта автоматически обновляются, когда страницы публикуются и их публикация отменяется.</span><span class="sxs-lookup"><span data-stu-id="95c4f-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="95c4f-113">Включение создания карты сайта</span><span class="sxs-lookup"><span data-stu-id="95c4f-113">Turn on site map generation</span></span>

1. <span data-ttu-id="95c4f-114">Войдите в средство разработки.</span><span class="sxs-lookup"><span data-stu-id="95c4f-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="95c4f-115">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="95c4f-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="95c4f-116">В области переходов слева выберите **Управление сайтом**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="95c4f-117">Убедитесь, что параметр **Карты сайта включены** включен.</span><span class="sxs-lookup"><span data-stu-id="95c4f-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="95c4f-118">Метаданные страниц</span><span class="sxs-lookup"><span data-stu-id="95c4f-118">Page metadata</span></span>

<span data-ttu-id="95c4f-119">Dynamics 365 Commerce позволяет управлять метаданными SEO для отдельных страниц.</span><span class="sxs-lookup"><span data-stu-id="95c4f-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="95c4f-120">Эти сведения можно просмотреть и изменить в разделе **Свойства SEO** контейнера страницы.</span><span class="sxs-lookup"><span data-stu-id="95c4f-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="95c4f-121">Поддерживаются следующие свойства метаданных SEO:</span><span class="sxs-lookup"><span data-stu-id="95c4f-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="95c4f-122">Название должности</span><span class="sxs-lookup"><span data-stu-id="95c4f-122">Title</span></span>
- <span data-ttu-id="95c4f-123">Описание</span><span class="sxs-lookup"><span data-stu-id="95c4f-123">Description</span></span>
- <span data-ttu-id="95c4f-124">Ключевые слова SEO</span><span class="sxs-lookup"><span data-stu-id="95c4f-124">SEO keywords</span></span>
- <span data-ttu-id="95c4f-125">Метки ARIA</span><span class="sxs-lookup"><span data-stu-id="95c4f-125">Aria labels</span></span>
- <span data-ttu-id="95c4f-126">noindex</span><span class="sxs-lookup"><span data-stu-id="95c4f-126">noindex</span></span>
- <span data-ttu-id="95c4f-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="95c4f-127">nofollow</span></span>
- <span data-ttu-id="95c4f-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="95c4f-128">noarchive</span></span>
- <span data-ttu-id="95c4f-129">nocache</span><span class="sxs-lookup"><span data-stu-id="95c4f-129">nocache</span></span>
- <span data-ttu-id="95c4f-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="95c4f-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="95c4f-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="95c4f-131">nosnippet</span></span>
- <span data-ttu-id="95c4f-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="95c4f-132">noImageIndex</span></span>
- <span data-ttu-id="95c4f-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="95c4f-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="95c4f-134">Изменение метаданных страницы</span><span class="sxs-lookup"><span data-stu-id="95c4f-134">Modify page metadata</span></span>

<span data-ttu-id="95c4f-135">Чтобы изменить метаданные страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="95c4f-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="95c4f-136">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="95c4f-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="95c4f-137">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="95c4f-138">Выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="95c4f-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="95c4f-139">На панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="95c4f-140">В области свойств справа разверните пункт **Метатеги по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="95c4f-141">Чтобы добавить новый метатег, выберите **Добавить**, затем введите тег в поле.</span><span class="sxs-lookup"><span data-stu-id="95c4f-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="95c4f-142">Чтобы удалить существующий метатег, выберите значок корзины справа от него.</span><span class="sxs-lookup"><span data-stu-id="95c4f-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="95c4f-143">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="95c4f-144">В поле **Комментарии** введите **Обновлены метатеги**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="95c4f-145">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="95c4f-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="95c4f-146">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="95c4f-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="95c4f-147">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="95c4f-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95c4f-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="95c4f-148">Additional resources</span></span>

[<span data-ttu-id="95c4f-149">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="95c4f-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="95c4f-150">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="95c4f-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="95c4f-151">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="95c4f-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="95c4f-152">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="95c4f-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="95c4f-153">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="95c4f-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="95c4f-154">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="95c4f-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="95c4f-155">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="95c4f-155">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="95c4f-156">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="95c4f-156">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
