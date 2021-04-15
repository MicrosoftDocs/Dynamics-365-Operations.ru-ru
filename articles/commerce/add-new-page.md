---
title: Добавление новой страницы сайта
description: В этом разделе описывается, как добавить новую страницу сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797559"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="a1acc-103">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="a1acc-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1acc-104">В этом разделе описывается, как добавить новую страницу сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1acc-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a1acc-105">Следующим шагом после создания шаблонов и фрагментов для сайта является начало создания страниц, использующих их.</span><span class="sxs-lookup"><span data-stu-id="a1acc-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="a1acc-106">Чтобы приступить к работе, необходимо выбрать шаблон или макет, имя страницы и URL-адрес страницы.</span><span class="sxs-lookup"><span data-stu-id="a1acc-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="a1acc-107">Шаблон или макет</span><span class="sxs-lookup"><span data-stu-id="a1acc-107">Template or layout</span></span>

<span data-ttu-id="a1acc-108">Для новой страницы можно использовать либо шаблон, либо макет.</span><span class="sxs-lookup"><span data-stu-id="a1acc-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="a1acc-109">Для получения дополнительных сведений см. раздел [Обзор шаблонов и макетов](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a1acc-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="a1acc-110">Имя страницы</span><span class="sxs-lookup"><span data-stu-id="a1acc-110">Page name</span></span>

<span data-ttu-id="a1acc-111">Имя страницы должно быть уникальным для страницы.</span><span class="sxs-lookup"><span data-stu-id="a1acc-111">The page name must be unique to your page.</span></span> <span data-ttu-id="a1acc-112">Оно должно быть описательным, чтобы можно было легко найти его, и другие люди знали, для чего предназначена страница.</span><span class="sxs-lookup"><span data-stu-id="a1acc-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="a1acc-113">Выберите имя страницы тщательно, так как позднее оно не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="a1acc-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="a1acc-114">URL-адрес страницы</span><span class="sxs-lookup"><span data-stu-id="a1acc-114">Page URL</span></span>

<span data-ttu-id="a1acc-115">Имеется возможность ввести URL-адрес для новой страницы.</span><span class="sxs-lookup"><span data-stu-id="a1acc-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="a1acc-116">При создании страницы можно ввести строку, которая будет использоваться для формирования полного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a1acc-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="a1acc-117">Эта строка называется относительным URL-адресом или динамическим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="a1acc-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="a1acc-118">Затем полный URL-адрес создается на основе динамического URL-адреса, и ему назначается новая страница.</span><span class="sxs-lookup"><span data-stu-id="a1acc-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="a1acc-119">Можно изменить динамический URL-адрес позже, прежде чем опубликовать страницу.</span><span class="sxs-lookup"><span data-stu-id="a1acc-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="a1acc-120">Дополнительные сведения см. в разделе [Создание URL-адреса страницы](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="a1acc-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a1acc-121">Dynamics 365 Commerce разделяет URL-адреса и содержимое.</span><span class="sxs-lookup"><span data-stu-id="a1acc-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="a1acc-122">Другими словами, можно создать страницу, не связанную с URL-адресом, и можно создать URL-адрес, не связанный со страницей.</span><span class="sxs-lookup"><span data-stu-id="a1acc-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="a1acc-123">Таким образом, можно выполнить замену URL-адреса и не требовать простоя, а перенаправлениями легче управлять.</span><span class="sxs-lookup"><span data-stu-id="a1acc-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="a1acc-124">Добавление новой страницы</span><span class="sxs-lookup"><span data-stu-id="a1acc-124">Add a new page</span></span>

<span data-ttu-id="a1acc-125">Чтобы добавить новую страницу сайта на сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a1acc-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="a1acc-126">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="a1acc-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="a1acc-127">Выберите **Создать страницу**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-127">Select **New Page**.</span></span>
1. <span data-ttu-id="a1acc-128">В диалоговом окне **Создать страницу** выберите шаблон, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="a1acc-129">В поле **Имя страницы** введите имя страницы (например, **Моя новая страница**).</span><span class="sxs-lookup"><span data-stu-id="a1acc-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="a1acc-130">В поле **URL-адрес** введите строку (динамический URL-адрес) для завершения URL-адреса (например, **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="a1acc-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="a1acc-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-131">Select **OK**.</span></span> <span data-ttu-id="a1acc-132">Появится редактор страниц.</span><span class="sxs-lookup"><span data-stu-id="a1acc-132">The page editor appears.</span></span> <span data-ttu-id="a1acc-133">Обратите внимание, что заголовок и нижний колонтитул автоматически добавляются на страницу в соответствии с выбранным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="a1acc-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="a1acc-134">В структуре страницы выберите слот **Главный**, нажмите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a1acc-135">Выберите **Контейнер**, затем выберите **ОК**</span><span class="sxs-lookup"><span data-stu-id="a1acc-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="a1acc-136">Выберите **Гибкий контейнер**, выберите кнопку с многоточием, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a1acc-137">Выберите **Блок насыщенного содержимого**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="a1acc-138">Выберите **Блок насыщенного содержимого**, выберите кнопку с многоточием, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a1acc-139">Выберите **Элемент блока насыщенного содержимого**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="a1acc-140">В области свойств справа выберите **Абзац**, затем в поле введите **Мой тестовый текст**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="a1acc-141">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="a1acc-142">В поле **Комментарии** введите **Добавлена новая страница**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="a1acc-143">Выберите **Предварительный просмотр** для предварительного просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="a1acc-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="a1acc-144">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="a1acc-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="a1acc-145">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-145">Select **Publish**.</span></span>
1. <span data-ttu-id="a1acc-146">В пути перехода (навигации) выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="a1acc-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="a1acc-147">В области переходов слева выберите **URL-адреса**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="a1acc-148">Найдите и выберите свой URL-адрес (**mynewpage**) в списке.</span><span class="sxs-lookup"><span data-stu-id="a1acc-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="a1acc-149">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="a1acc-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1acc-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a1acc-150">Additional resources</span></span>

[<span data-ttu-id="a1acc-151">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="a1acc-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="a1acc-152">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="a1acc-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="a1acc-153">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="a1acc-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="a1acc-154">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="a1acc-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="a1acc-155">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="a1acc-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="a1acc-156">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="a1acc-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="a1acc-157">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="a1acc-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="a1acc-158">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="a1acc-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
