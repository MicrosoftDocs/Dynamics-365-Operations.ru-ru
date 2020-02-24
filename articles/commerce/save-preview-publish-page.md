---
title: Сохранение, предварительный просмотр и публикация страницы
description: В этом разделе описывается, как сохранить, предварительно просмотреть и опубликовать страницу в Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 04200264fabca265484b5e66426810efe8028a50
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002828"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="eee6b-103">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-103">Save, preview, and publish a page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="eee6b-104">В этом разделе описывается, как сохранить, предварительно просмотреть и опубликовать страницу в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eee6b-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="eee6b-105">Сохранение страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-105">Save a page</span></span>

<span data-ttu-id="eee6b-106">Чтобы сохранить страницу, необходимо, чтобы она была извлечена для вас и открыта в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="eee6b-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="eee6b-107">Страницу следует сохранить непосредственно после ее изменения, чтобы гарантировать сохранение изменений.</span><span class="sxs-lookup"><span data-stu-id="eee6b-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="eee6b-108">При сохранении страницы эти изменения видны только вам.</span><span class="sxs-lookup"><span data-stu-id="eee6b-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="eee6b-109">Операция сохранения предназначена в основном для сохранения изменений, пока страница еще не готова для возврата.</span><span class="sxs-lookup"><span data-stu-id="eee6b-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="eee6b-110">После завершения изменения страницы рекомендуется вернуть ее в, чтобы изменения стали видимыми для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="eee6b-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="eee6b-111">На этом этапе страница может также быть извлечена другими пользователями, которые должны ее изменить.</span><span class="sxs-lookup"><span data-stu-id="eee6b-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="eee6b-112">Предварительный просмотр страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-112">Preview a page</span></span>

<span data-ttu-id="eee6b-113">Средство разработки предлагает два вида предварительного просмотра: область просмотра "что вы видите, то вы и получаете» (WYSIWYG) в редакторе страниц и отдельное окно предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="eee6b-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="eee6b-114">При использовании редактора страниц в центральной области появится предварительный просмотр "что вы видите, то и получите" (WYSIWYG).</span><span class="sxs-lookup"><span data-stu-id="eee6b-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="eee6b-115">Этот предварительный просмотр автоматически обновляется, когда пользователь сохраняет страницу.</span><span class="sxs-lookup"><span data-stu-id="eee6b-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="eee6b-116">Можно также обновить его вручную, выбрав **Обновить** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="eee6b-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="eee6b-117">В режиме предварительного просмотра WYSIWYG страница отображается точно в том виде, в котором она отображается пользователями сайта, но помощники по разработке отображаются поверх нее.</span><span class="sxs-lookup"><span data-stu-id="eee6b-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="eee6b-118">После завершения изменения страницы, возможно, потребуется просмотреть ее, чтобы увидеть, что увидят клиенты.</span><span class="sxs-lookup"><span data-stu-id="eee6b-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="eee6b-119">Чтобы просмотреть страницу, выберите **Предварительный просмотр** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="eee6b-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="eee6b-120">Предварительный просмотр появится в отдельном окне браузера.</span><span class="sxs-lookup"><span data-stu-id="eee6b-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="eee6b-121">Страница в окне предварительного просмотра отображается точно так же, как отображается пользователем сайта.</span><span class="sxs-lookup"><span data-stu-id="eee6b-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="eee6b-122">Можно изменить размеры окна, чтобы убедиться, что отзывчивые модули правильно обрабатываются во всех портах просмотра.</span><span class="sxs-lookup"><span data-stu-id="eee6b-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="eee6b-123">Для предварительного просмотра неопубликованного содержимого требуются проверка подлинности и правильные разрешения.</span><span class="sxs-lookup"><span data-stu-id="eee6b-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="eee6b-124">Поэтому при открытии кому-то общего доступа к URL-адресу предварительного просмотра этот человек должен иметь правильные разрешения на доступ к содержимому.</span><span class="sxs-lookup"><span data-stu-id="eee6b-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="eee6b-125">Публикация страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-125">Publish a page</span></span>

<span data-ttu-id="eee6b-126">После того как страница готова, следующим шагом является ее публикация, чтобы внешние пользователи могли просмотреть содержимое.</span><span class="sxs-lookup"><span data-stu-id="eee6b-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="eee6b-127">Прежде чем можно будет опубликовать страницу, ее необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="eee6b-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="eee6b-128">Можно публиковать и отменять публикацию страниц либо в инспекторе страниц, либо в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="eee6b-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="eee6b-129">Инспектор страниц отображает список страниц и позволяет выполнять массовые операции.</span><span class="sxs-lookup"><span data-stu-id="eee6b-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="eee6b-130">Редактор страниц можно использовать для публикации или отмены публикации только одной страницы, которая открыта в нем.</span><span class="sxs-lookup"><span data-stu-id="eee6b-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="eee6b-131">Чтобы опубликовать одну или несколько страниц из инспектора страниц, выберите страницы, убедитесь, что они возвращены, затем выберите команду **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="eee6b-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="eee6b-132">Страницы публикуются, и вы получаете уведомление об операции в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="eee6b-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="eee6b-133">Процедура публикации одной страницы с помощью редактора страниц аналогична.</span><span class="sxs-lookup"><span data-stu-id="eee6b-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="eee6b-134">Пока страница открыта в редакторе страниц, убедитесь, что она возвращена, затем выберите команду **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="eee6b-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="eee6b-135">Страница публикуется, и вы получаете уведомление об операции.</span><span class="sxs-lookup"><span data-stu-id="eee6b-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="eee6b-136">При публикации страницы публикуется только ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="eee6b-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="eee6b-137">Вы и другие пользователи могут перейти к странице и просмотреть ее только после того, как с ней будет связан URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="eee6b-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="eee6b-138">URL-адрес должен быть опубликован отдельно.</span><span class="sxs-lookup"><span data-stu-id="eee6b-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eee6b-139">Прежде чем можно будет опубликовать страницу, все изображения или фрагменты, на которые ссылается страница, уже должны быть опубликованы.</span><span class="sxs-lookup"><span data-stu-id="eee6b-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="eee6b-140">Сохранение, предварительный просмотр и публикация домашней страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="eee6b-141">Чтобы сохранить опубликовать домашнюю страницу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eee6b-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="eee6b-142">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="eee6b-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="eee6b-143">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="eee6b-144">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="eee6b-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="eee6b-145">Выберите **Извлечь**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="eee6b-146">Измените страницу нужным образом.</span><span class="sxs-lookup"><span data-stu-id="eee6b-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="eee6b-147">Выберите **Сохранить**, затем выберите **Вернуть**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="eee6b-148">В поле **Комментарии** введите примечание о внесенных изменениях, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="eee6b-149">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="eee6b-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="eee6b-150">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="eee6b-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="eee6b-151">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="eee6b-152">Публикация URL-адреса</span><span class="sxs-lookup"><span data-stu-id="eee6b-152">Publish a URL</span></span>

<span data-ttu-id="eee6b-153">Чтобы опубликовать URL-адрес, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eee6b-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="eee6b-154">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="eee6b-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="eee6b-155">В области переходов слева выберите **URL-адреса**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="eee6b-156">Найдите и выберите URL-адрес, который требуется опубликовать.</span><span class="sxs-lookup"><span data-stu-id="eee6b-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="eee6b-157">На панели команд выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eee6b-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eee6b-158">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eee6b-158">Additional resources</span></span>

[<span data-ttu-id="eee6b-159">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="eee6b-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="eee6b-160">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="eee6b-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="eee6b-161">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="eee6b-162">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="eee6b-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="eee6b-163">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="eee6b-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="eee6b-164">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="eee6b-164">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="eee6b-165">Проверка специальных возможностей контента страницы</span><span class="sxs-lookup"><span data-stu-id="eee6b-165">Verify page content accessibility</span></span>](verify-accessibility.md)
