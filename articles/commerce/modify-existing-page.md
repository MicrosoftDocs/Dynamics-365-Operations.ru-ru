---
title: Изменение существующей страницы сайта
description: В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c393fc143214c2c7c7ddad9a77e273e1e53e34ac
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003449"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="8a8f6-103">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="8a8f6-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8a8f6-104">В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8a8f6-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="8a8f6-105">Overview</span></span>

<span data-ttu-id="8a8f6-106">Когда необходимо изменить страницу, первым шагом является ее открытие в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="8a8f6-107">Перейдите на сайт, содержащий страницу, затем в списке страниц найдите нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="8a8f6-108">Если не удается найти страницу, можно воспользоваться функциями расширенного поиска инструмента разработки.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="8a8f6-109">Либо введите точное имя страницы, либо введите первые несколько букв, а затем звездочку (\*).</span><span class="sxs-lookup"><span data-stu-id="8a8f6-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="8a8f6-110">Отображается отфильтрованный список страниц.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-110">A filtered list of pages appears.</span></span> <span data-ttu-id="8a8f6-111">С помощью этого списка можно найти нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="8a8f6-112">После того, как вы нашли правильную страницу, выберите имя страницы, чтобы открыть страницу в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="8a8f6-113">Если страница отображается в инспекторе страниц, ее можно выбрать и извлечь перед открытием в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="8a8f6-114">Таким образом можно извлекать несколько страниц одновременно.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="8a8f6-115">После открытия страницы в редакторе страниц необходимо убедиться, что она извлечена вами.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="8a8f6-116">Панель команд в инструменте разработки является динамической, контекстно-зависимой и с учетом состояния.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="8a8f6-117">Таким образом отображаются только те действия, которые можно выполнить на странице в данный момент.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="8a8f6-118">Например, если страница не извлечена вами, кнопки **Сохранить** и **Вернуть** не появляются на панели команд.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="8a8f6-119">Состояние страницы также отображается в правой части окна.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="8a8f6-120">Если страница еще не извлечена, выберите **Извлечь** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="8a8f6-121">Панель команд изменяется, отражая новое состояние страницы.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="8a8f6-122">Также вы получаете уведомление о том, что страница была извлечена вами.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="8a8f6-123">Следующий шаг состоит в выполнении фактических изменений.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="8a8f6-124">Часто для поиска и выбора модуля, который необходимо изменить, используется дерево структуры страниц в левой части, а затем вносятся изменения на панели свойств справа.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="8a8f6-125">Однако в некоторых случаях изменения могут включать добавление или удаление модулей или фрагментов.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="8a8f6-126">Чтобы добавить фрагмент или модуль, используйте деревом структуры страниц, чтобы найти гнездо, в которое необходимо добавить модуль или фрагмент, затем нажмите кнопку с многоточием (**...**) для этого гнезда.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="8a8f6-127">Появится меню, содержащее команды для добавления модуля или фрагмента.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="8a8f6-128">Чтобы удалить модуль или фрагмент, найдите и выберите его в дереве структуры страницы, выберите кнопку с многоточием, затем выберите команду для удаления модуля или фрагмента.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="8a8f6-129">Кроме того, можно просматривать и изменять свойства любого модуля, который отображается в разделе предварительного просмотра "что видите, то и получите" (WYSIWYG), выбрав его непосредственно.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="8a8f6-130">После завершения внесения изменений и предварительного просмотра их результатов следует вернуть страницу, выбрав **Вернуть** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="8a8f6-131">Чтобы немедленно опубликовать изменения, выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="8a8f6-132">Последняя возвращенная версия измененной страницы публикуется и становится доступной внешним пользователям, просматривающим сайт.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="8a8f6-133">Пример: изменение видео на домашней странице</span><span class="sxs-lookup"><span data-stu-id="8a8f6-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="8a8f6-134">В следующем примере показано, как изменить домашнюю страницу, изменив видеозапись, которая отображается в модуле видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="8a8f6-135">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="8a8f6-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8a8f6-136">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="8a8f6-137">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="8a8f6-138">На панели команд выберите **Извлечь**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="8a8f6-139">В структуре страницы выберите слот **Главный**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="8a8f6-140">В слоте **Главный** разверните все модули гибкого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="8a8f6-141">Найдите и выберите модуль видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="8a8f6-142">В области свойств справа выберите свойство **видео**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="8a8f6-143">Отображается средство выбора активов.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-143">The asset picker appears.</span></span>
1. <span data-ttu-id="8a8f6-144">В средстве выбора активов выберите доступный видеоактив или выберите команду **Отправить новый актив**, чтобы отправить новый видеоактив.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="8a8f6-145">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-145">Select **OK**.</span></span>
1. <span data-ttu-id="8a8f6-146">Выберите **Сохранить**, затем выберите **Вернуть**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="8a8f6-147">В поле **Комментарии** введите **Изменена видеозапись**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="8a8f6-148">Выберите **Предварительный просмотр** для предварительного просмотра обновленной страницы.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="8a8f6-149">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="8a8f6-150">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a8f6-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a8f6-151">Additional resources</span></span>

[<span data-ttu-id="8a8f6-152">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="8a8f6-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="8a8f6-153">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="8a8f6-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8a8f6-154">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="8a8f6-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="8a8f6-155">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="8a8f6-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8a8f6-156">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="8a8f6-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="8a8f6-157">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="8a8f6-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="8a8f6-158">Проверка специальных возможностей контента страницы</span><span class="sxs-lookup"><span data-stu-id="8a8f6-158">Verify page content accessibility</span></span>](verify-accessibility.md)
