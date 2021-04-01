---
title: Сохранение, предварительный просмотр и публикация страницы
description: В этом разделе описывается, как сохранить, предварительно просмотреть и опубликовать страницу в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 68fec8c2ddc05c71394045351cef880361f2e306
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254825"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="f2702-103">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2702-104">В этом разделе описывается, как сохранить, предварительно просмотреть и опубликовать страницу в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2702-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="f2702-105">Сохранение страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-105">Save a page</span></span>

<span data-ttu-id="f2702-106">Чтобы сохранить страницу, необходимо, чтобы она была извлечена для вас и открыта в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="f2702-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="f2702-107">Чтобы извлечь страницу, на панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="f2702-107">To check out a page, select **Edit** on the command bar.</span></span> <span data-ttu-id="f2702-108">После завершения редактирования страницы следует немедленно сохранить ее, чтобы гарантировать сохранение изменений.</span><span class="sxs-lookup"><span data-stu-id="f2702-108">After you've finished editing a page, you should immediately save it to ensure that your changes are stored.</span></span>

<span data-ttu-id="f2702-109">При сохранении страницы эти изменения видны только вам.</span><span class="sxs-lookup"><span data-stu-id="f2702-109">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="f2702-110">Операция сохранения предназначена в основном для сохранения изменений, пока страница еще не готова для возврата.</span><span class="sxs-lookup"><span data-stu-id="f2702-110">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="f2702-111">После завершения изменения страницы рекомендуется вернуть ее в, чтобы изменения стали видимыми для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="f2702-111">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="f2702-112">На этом этапе страница может также быть извлечена другими пользователями, которые должны ее изменить.</span><span class="sxs-lookup"><span data-stu-id="f2702-112">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="f2702-113">Предварительный просмотр страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-113">Preview a page</span></span>

<span data-ttu-id="f2702-114">Средство разработки предлагает два вида предварительного просмотра: визуальный конструктор страниц, который является областью просмотра "что вы видите, то вы и получаете» (WYSIWYG) в редакторе страниц, и отдельное окно предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="f2702-114">The authoring tool offers two kinds of preview features: visual page builder, which is a "what you see is what you get" (WYSIWYG) preview pane in the page editor, and a separate preview window.</span></span>

<span data-ttu-id="f2702-115">При использовании редактора страниц в центральной области появится предварительный просмотр "что вы видите, то и получите" (WYSIWYG).</span><span class="sxs-lookup"><span data-stu-id="f2702-115">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="f2702-116">Этот предварительный просмотр автоматически обновляется, когда пользователь сохраняет страницу.</span><span class="sxs-lookup"><span data-stu-id="f2702-116">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="f2702-117">Можно также обновить его вручную, выбрав **Обновить** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="f2702-117">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="f2702-118">В режиме предварительного просмотра страница отображается точно в том виде, в котором она отображается пользователями сайта, но помощники по разработке отображаются поверх нее.</span><span class="sxs-lookup"><span data-stu-id="f2702-118">The preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="f2702-119">После завершения изменения страницы, возможно, потребуется просмотреть ее, чтобы увидеть, что увидят клиенты.</span><span class="sxs-lookup"><span data-stu-id="f2702-119">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="f2702-120">Чтобы просмотреть страницу, выберите **Предварительный просмотр** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="f2702-120">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="f2702-121">Предварительный просмотр появится в отдельном окне браузера.</span><span class="sxs-lookup"><span data-stu-id="f2702-121">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="f2702-122">Страница в окне предварительного просмотра отображается точно так же, как отображается пользователем сайта.</span><span class="sxs-lookup"><span data-stu-id="f2702-122">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="f2702-123">Можно изменить размеры окна, чтобы убедиться, что отзывчивые модули правильно обрабатываются во всех портах просмотра.</span><span class="sxs-lookup"><span data-stu-id="f2702-123">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="f2702-124">Для предварительного просмотра неопубликованного содержимого требуются проверка подлинности и правильные разрешения.</span><span class="sxs-lookup"><span data-stu-id="f2702-124">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="f2702-125">Поэтому при открытии кому-то общего доступа к URL-адресу предварительного просмотра этот человек должен иметь правильные разрешения на доступ к содержимому.</span><span class="sxs-lookup"><span data-stu-id="f2702-125">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="f2702-126">Публикация страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-126">Publish a page</span></span>

<span data-ttu-id="f2702-127">После того как страница готова, следующим шагом является ее публикация, чтобы внешние пользователи могли просмотреть содержимое.</span><span class="sxs-lookup"><span data-stu-id="f2702-127">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="f2702-128">Прежде чем можно будет опубликовать страницу, необходимо вернуть ее, нажав кнопку **Завершить редактирование** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="f2702-128">Before you can publish a page, you must check it in by selecting **Finish editing** on the command bar.</span></span>

<span data-ttu-id="f2702-129">Можно публиковать и отменять публикацию страниц либо в инспекторе страниц, либо в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="f2702-129">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="f2702-130">Инспектор страниц отображает список страниц и позволяет выполнять массовые операции.</span><span class="sxs-lookup"><span data-stu-id="f2702-130">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="f2702-131">Редактор страниц можно использовать для публикации или отмены публикации только одной страницы, которая открыта в нем.</span><span class="sxs-lookup"><span data-stu-id="f2702-131">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="f2702-132">Чтобы опубликовать одну или несколько страниц из инспектора страниц, выберите страницы, убедитесь, что они возвращены, затем выберите команду **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="f2702-132">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="f2702-133">Страницы публикуются, и вы получаете уведомление об операции в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="f2702-133">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="f2702-134">Процедура публикации одной страницы с помощью редактора страниц аналогична.</span><span class="sxs-lookup"><span data-stu-id="f2702-134">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="f2702-135">Пока страница открыта в редакторе страниц, убедитесь, что она возвращена, затем выберите команду **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="f2702-135">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="f2702-136">Страница публикуется, и вы получаете уведомление об операции.</span><span class="sxs-lookup"><span data-stu-id="f2702-136">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="f2702-137">При публикации страницы публикуется только ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="f2702-137">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="f2702-138">Вы и другие пользователи могут перейти к странице и просмотреть ее только после того, как с ней будет связан URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f2702-138">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="f2702-139">URL-адрес должен быть опубликован отдельно.</span><span class="sxs-lookup"><span data-stu-id="f2702-139">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2702-140">Прежде чем можно будет опубликовать страницу, все изображения или фрагменты, на которые ссылается страница, уже должны быть опубликованы.</span><span class="sxs-lookup"><span data-stu-id="f2702-140">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="f2702-141">Сохранение, предварительный просмотр и публикация домашней страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-141">Save, preview, and publish a home page</span></span>

<span data-ttu-id="f2702-142">Чтобы сохранить опубликовать домашнюю страницу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2702-142">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="f2702-143">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="f2702-143">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f2702-144">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="f2702-144">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="f2702-145">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="f2702-145">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="f2702-146">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="f2702-146">Select **Edit**.</span></span>
1. <span data-ttu-id="f2702-147">Измените страницу нужным образом.</span><span class="sxs-lookup"><span data-stu-id="f2702-147">Modify the page as you require.</span></span>
1. <span data-ttu-id="f2702-148">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="f2702-148">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="f2702-149">В поле **Комментарии** введите примечание о внесенных изменениях, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2702-149">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="f2702-150">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="f2702-150">Select **Preview** to preview your page.</span></span> <span data-ttu-id="f2702-151">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="f2702-151">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="f2702-152">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="f2702-152">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="f2702-153">Публикация URL-адреса</span><span class="sxs-lookup"><span data-stu-id="f2702-153">Publish a URL</span></span>

<span data-ttu-id="f2702-154">Чтобы опубликовать URL-адрес, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2702-154">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="f2702-155">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="f2702-155">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f2702-156">В области переходов слева выберите **URL-адреса**.</span><span class="sxs-lookup"><span data-stu-id="f2702-156">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="f2702-157">Найдите и выберите URL-адрес, который требуется опубликовать.</span><span class="sxs-lookup"><span data-stu-id="f2702-157">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="f2702-158">На панели команд выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="f2702-158">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2702-159">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2702-159">Additional resources</span></span>

[<span data-ttu-id="f2702-160">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="f2702-160">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="f2702-161">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="f2702-161">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f2702-162">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-162">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="f2702-163">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="f2702-163">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="f2702-164">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="f2702-164">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="f2702-165">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="f2702-165">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="f2702-166">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="f2702-166">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="f2702-167">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="f2702-167">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]