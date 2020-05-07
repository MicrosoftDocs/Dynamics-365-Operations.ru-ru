---
title: Добавление новой страницы сайта
description: В этом разделе описывается, как добавить новую страницу сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269966"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="77d96-103">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="77d96-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="77d96-104">В этом разделе описывается, как добавить новую страницу сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="77d96-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="77d96-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="77d96-105">Overview</span></span>

<span data-ttu-id="77d96-106">Следующим шагом после создания шаблонов и фрагментов для сайта является начало создания страниц, использующих их.</span><span class="sxs-lookup"><span data-stu-id="77d96-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="77d96-107">Чтобы приступить к работе, необходимо выбрать шаблон или макет, имя страницы и URL-адрес страницы.</span><span class="sxs-lookup"><span data-stu-id="77d96-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="77d96-108">Шаблон или макет</span><span class="sxs-lookup"><span data-stu-id="77d96-108">Template or layout</span></span>

<span data-ttu-id="77d96-109">Для новой страницы можно использовать либо шаблон, либо макет.</span><span class="sxs-lookup"><span data-stu-id="77d96-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="77d96-110">Для получения дополнительных сведений см. раздел [Обзор шаблонов и макетов](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="77d96-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="77d96-111">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="77d96-111">Page name</span></span>

<span data-ttu-id="77d96-112">Имя страницы должно быть уникальным для страницы.</span><span class="sxs-lookup"><span data-stu-id="77d96-112">The page name must be unique to your page.</span></span> <span data-ttu-id="77d96-113">Оно должно быть описательным, чтобы можно было легко найти его, и другие люди знали, для чего предназначена страница.</span><span class="sxs-lookup"><span data-stu-id="77d96-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="77d96-114">Выберите имя страницы тщательно, так как позднее оно не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="77d96-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="77d96-115">URL-адрес страницы</span><span class="sxs-lookup"><span data-stu-id="77d96-115">Page URL</span></span>

<span data-ttu-id="77d96-116">Имеется возможность ввести URL-адрес для новой страницы.</span><span class="sxs-lookup"><span data-stu-id="77d96-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="77d96-117">При создании страницы можно ввести строку, которая будет использоваться для формирования полного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="77d96-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="77d96-118">Эта строка называется относительным URL-адресом или динамическим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="77d96-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="77d96-119">Затем полный URL-адрес создается на основе динамического URL-адреса, и ему назначается новая страница.</span><span class="sxs-lookup"><span data-stu-id="77d96-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="77d96-120">Можно изменить динамический URL-адрес позже, прежде чем опубликовать страницу.</span><span class="sxs-lookup"><span data-stu-id="77d96-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="77d96-121">Дополнительные сведения см. в разделе [Создание URL-адреса страницы](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="77d96-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="77d96-122">Dynamics 365 Commerce разделяет URL-адреса и содержимое.</span><span class="sxs-lookup"><span data-stu-id="77d96-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="77d96-123">Другими словами, можно создать страницу, не связанную с URL-адресом, и можно создать URL-адрес, не связанный со страницей.</span><span class="sxs-lookup"><span data-stu-id="77d96-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="77d96-124">Таким образом, можно выполнить замену URL-адреса и не требовать простоя, а перенаправлениями легче управлять.</span><span class="sxs-lookup"><span data-stu-id="77d96-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="77d96-125">Добавление новой страницы</span><span class="sxs-lookup"><span data-stu-id="77d96-125">Add a new page</span></span>

<span data-ttu-id="77d96-126">Чтобы добавить новую страницу сайта на сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="77d96-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="77d96-127">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="77d96-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="77d96-128">Выберите **Создать страницу**.</span><span class="sxs-lookup"><span data-stu-id="77d96-128">Select **New Page**.</span></span>
1. <span data-ttu-id="77d96-129">В диалоговом окне **Создать страницу** выберите шаблон, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="77d96-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="77d96-130">В поле **Имя страницы** введите имя страницы (например, **Моя новая страница**).</span><span class="sxs-lookup"><span data-stu-id="77d96-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="77d96-131">В поле **URL-адрес** введите строку (динамический URL-адрес) для завершения URL-адреса (например, **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="77d96-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="77d96-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="77d96-132">Select **OK**.</span></span> <span data-ttu-id="77d96-133">Появится редактор страниц.</span><span class="sxs-lookup"><span data-stu-id="77d96-133">The page editor appears.</span></span> <span data-ttu-id="77d96-134">Обратите внимание, что заголовок и нижний колонтитул автоматически добавляются на страницу в соответствии с выбранным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="77d96-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="77d96-135">В структуре страницы выберите слот **Главный**, нажмите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="77d96-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77d96-136">Выберите **Контейнер**, затем выберите **ОК**</span><span class="sxs-lookup"><span data-stu-id="77d96-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="77d96-137">Выберите **Гибкий контейнер**, выберите кнопку с многоточием, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="77d96-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="77d96-138">Выберите **Блок насыщенного содержимого**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="77d96-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="77d96-139">Выберите **Блок насыщенного содержимого**, выберите кнопку с многоточием, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="77d96-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="77d96-140">Выберите **Элемент блока насыщенного содержимого**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="77d96-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="77d96-141">В области свойств справа выберите **Абзац**, затем в поле введите **Мой тестовый текст**.</span><span class="sxs-lookup"><span data-stu-id="77d96-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="77d96-142">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="77d96-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="77d96-143">В поле **Комментарии** введите **Добавлена новая страница**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="77d96-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="77d96-144">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="77d96-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="77d96-145">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="77d96-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="77d96-146">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="77d96-146">Select **Publish**.</span></span>
1. <span data-ttu-id="77d96-147">В пути перехода (навигации) выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="77d96-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="77d96-148">В области переходов слева выберите **URL-адреса**.</span><span class="sxs-lookup"><span data-stu-id="77d96-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="77d96-149">Найдите и выберите свой URL-адрес (**mynewpage**) в списке.</span><span class="sxs-lookup"><span data-stu-id="77d96-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="77d96-150">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="77d96-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77d96-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77d96-151">Additional resources</span></span>

[<span data-ttu-id="77d96-152">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="77d96-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="77d96-153">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="77d96-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="77d96-154">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="77d96-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="77d96-155">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="77d96-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="77d96-156">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="77d96-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="77d96-157">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="77d96-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="77d96-158">Проверка специальных возможностей контента страницы</span><span class="sxs-lookup"><span data-stu-id="77d96-158">Verify page content accessibility</span></span>](verify-accessibility.md)
