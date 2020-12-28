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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 74229628e48ffb8ac974acd868e325eeca77d91e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415220"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="e84c7-103">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="e84c7-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e84c7-104">В этом разделе описывается, как управлять метаданными оптимизации поисковой системы (SEO) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e84c7-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e84c7-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e84c7-105">Overview</span></span>

<span data-ttu-id="e84c7-106">Управление метаданными SEO для сайта может осуществляться с помощью карт сайта и метаданных страниц.</span><span class="sxs-lookup"><span data-stu-id="e84c7-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="e84c7-107">Карты сайта</span><span class="sxs-lookup"><span data-stu-id="e84c7-107">Site maps</span></span>

<span data-ttu-id="e84c7-108">Карта сайта — это доступный для чтения компьютером список в формате XML страниц на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="e84c7-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="e84c7-109">Она предназначена для использования поисковыми системами, чтобы они могли предоставлять лучшие результаты поиска на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="e84c7-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="e84c7-110">Карты сайта могут быть вручную обработаны поисковыми системами или опубликованы в файле robots.txt.</span><span class="sxs-lookup"><span data-stu-id="e84c7-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="e84c7-111">Dynamics 365 Commerce поддерживает автоматическое создание карт сайтов.</span><span class="sxs-lookup"><span data-stu-id="e84c7-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="e84c7-112">Карты сайта автоматически обновляются, когда страницы публикуются и их публикация отменяется.</span><span class="sxs-lookup"><span data-stu-id="e84c7-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="e84c7-113">Включение создания карты сайта</span><span class="sxs-lookup"><span data-stu-id="e84c7-113">Turn on site map generation</span></span>

1. <span data-ttu-id="e84c7-114">Войдите в средство разработки.</span><span class="sxs-lookup"><span data-stu-id="e84c7-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="e84c7-115">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="e84c7-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e84c7-116">В области переходов слева выберите **Управление сайтом**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="e84c7-117">Убедитесь, что параметр **Карты сайта включены** включен.</span><span class="sxs-lookup"><span data-stu-id="e84c7-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="e84c7-118">Метаданные страниц</span><span class="sxs-lookup"><span data-stu-id="e84c7-118">Page metadata</span></span>

<span data-ttu-id="e84c7-119">Dynamics 365 Commerce позволяет управлять метаданными SEO для отдельных страниц.</span><span class="sxs-lookup"><span data-stu-id="e84c7-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="e84c7-120">Эти сведения можно просмотреть и изменить в разделе **Свойства SEO** контейнера страницы.</span><span class="sxs-lookup"><span data-stu-id="e84c7-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="e84c7-121">Поддерживаются следующие свойства метаданных SEO:</span><span class="sxs-lookup"><span data-stu-id="e84c7-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="e84c7-122">Название должности</span><span class="sxs-lookup"><span data-stu-id="e84c7-122">Title</span></span>
- <span data-ttu-id="e84c7-123">Описание</span><span class="sxs-lookup"><span data-stu-id="e84c7-123">Description</span></span>
- <span data-ttu-id="e84c7-124">Ключевые слова SEO</span><span class="sxs-lookup"><span data-stu-id="e84c7-124">SEO keywords</span></span>
- <span data-ttu-id="e84c7-125">Метки ARIA</span><span class="sxs-lookup"><span data-stu-id="e84c7-125">Aria labels</span></span>
- <span data-ttu-id="e84c7-126">noindex</span><span class="sxs-lookup"><span data-stu-id="e84c7-126">noindex</span></span>
- <span data-ttu-id="e84c7-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="e84c7-127">nofollow</span></span>
- <span data-ttu-id="e84c7-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="e84c7-128">noarchive</span></span>
- <span data-ttu-id="e84c7-129">nocache</span><span class="sxs-lookup"><span data-stu-id="e84c7-129">nocache</span></span>
- <span data-ttu-id="e84c7-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="e84c7-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="e84c7-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="e84c7-131">nosnippet</span></span>
- <span data-ttu-id="e84c7-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="e84c7-132">noImageIndex</span></span>
- <span data-ttu-id="e84c7-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="e84c7-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="e84c7-134">Изменение метаданных страницы</span><span class="sxs-lookup"><span data-stu-id="e84c7-134">Modify page metadata</span></span>

<span data-ttu-id="e84c7-135">Чтобы изменить метаданные страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e84c7-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="e84c7-136">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="e84c7-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e84c7-137">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="e84c7-138">Выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="e84c7-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="e84c7-139">На панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="e84c7-140">В области свойств справа разверните пункт **Метатеги по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="e84c7-141">Чтобы добавить новый метатег, выберите **Добавить**, затем введите тег в поле.</span><span class="sxs-lookup"><span data-stu-id="e84c7-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="e84c7-142">Чтобы удалить существующий метатег, выберите значок корзины справа от него.</span><span class="sxs-lookup"><span data-stu-id="e84c7-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="e84c7-143">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e84c7-144">В поле **Комментарии** введите **Обновлены метатеги**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="e84c7-145">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="e84c7-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="e84c7-146">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="e84c7-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e84c7-147">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e84c7-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e84c7-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e84c7-148">Additional resources</span></span>

[<span data-ttu-id="e84c7-149">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="e84c7-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e84c7-150">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="e84c7-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e84c7-151">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="e84c7-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e84c7-152">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="e84c7-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e84c7-153">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="e84c7-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e84c7-154">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="e84c7-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e84c7-155">Проверка специальных возможностей контента страницы</span><span class="sxs-lookup"><span data-stu-id="e84c7-155">Verify page content accessibility</span></span>](verify-accessibility.md)
