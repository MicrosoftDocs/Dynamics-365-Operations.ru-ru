---
title: Изменение существующей страницы сайта
description: В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 8ca23dcf568cb0df6934f0d6201e4aafba5f9ba1
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961642"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="6c25a-103">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="6c25a-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6c25a-104">В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c25a-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c25a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="6c25a-105">Overview</span></span>

<span data-ttu-id="6c25a-106">Когда необходимо изменить страницу, первым шагом является ее открытие в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="6c25a-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="6c25a-107">Перейдите на сайт, содержащий страницу, затем в списке страниц найдите нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="6c25a-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="6c25a-108">Если не удается найти страницу, можно воспользоваться функциями расширенного поиска инструмента разработки.</span><span class="sxs-lookup"><span data-stu-id="6c25a-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="6c25a-109">Либо введите точное имя страницы, либо введите первые несколько букв, а затем звездочку (\*).</span><span class="sxs-lookup"><span data-stu-id="6c25a-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="6c25a-110">Отображается отфильтрованный список страниц.</span><span class="sxs-lookup"><span data-stu-id="6c25a-110">A filtered list of pages appears.</span></span> <span data-ttu-id="6c25a-111">С помощью этого списка можно найти нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="6c25a-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="6c25a-112">После того, как вы нашли правильную страницу, выберите имя страницы, чтобы открыть страницу в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="6c25a-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="6c25a-113">Если страница отображается в инспекторе страниц, можно выбрать **Изменить** и извлечь эту страницу перед открытием в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="6c25a-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="6c25a-114">Таким образом можно извлекать несколько страниц одновременно.</span><span class="sxs-lookup"><span data-stu-id="6c25a-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="6c25a-115">После открытия страницы в редакторе страниц необходимо убедиться, что она извлечена вами.</span><span class="sxs-lookup"><span data-stu-id="6c25a-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="6c25a-116">Панель команд в инструменте разработки является динамической, контекстно-зависимой и с учетом состояния.</span><span class="sxs-lookup"><span data-stu-id="6c25a-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="6c25a-117">Таким образом отображаются только те действия, которые можно выполнить на странице в данный момент.</span><span class="sxs-lookup"><span data-stu-id="6c25a-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="6c25a-118">Например, если страница не извлечена вами, кнопки **Сохранить** и **Завершить правку** не появляются на панели команд.</span><span class="sxs-lookup"><span data-stu-id="6c25a-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="6c25a-119">Состояние страницы также отображается в правой части окна.</span><span class="sxs-lookup"><span data-stu-id="6c25a-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="6c25a-120">Если страница еще не извлечена, выберите **Изменить** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="6c25a-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="6c25a-121">Панель команд изменяется, отражая новое состояние страницы.</span><span class="sxs-lookup"><span data-stu-id="6c25a-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="6c25a-122">Также вы получаете уведомление о том, что страница была извлечена вами.</span><span class="sxs-lookup"><span data-stu-id="6c25a-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="6c25a-123">Следующий шаг состоит в выполнении фактических изменений.</span><span class="sxs-lookup"><span data-stu-id="6c25a-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="6c25a-124">Часто для поиска и выбора модуля, который необходимо изменить, используется дерево структуры страниц в левой части, а затем вносятся изменения на панели свойств справа.</span><span class="sxs-lookup"><span data-stu-id="6c25a-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="6c25a-125">Однако в некоторых случаях изменения могут включать добавление или удаление модулей или фрагментов.</span><span class="sxs-lookup"><span data-stu-id="6c25a-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="6c25a-126">Чтобы добавить фрагмент или модуль, используйте деревом структуры страниц, чтобы найти гнездо, в которое необходимо добавить модуль или фрагмент, затем нажмите кнопку с многоточием (**...**) для этого гнезда.</span><span class="sxs-lookup"><span data-stu-id="6c25a-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="6c25a-127">Появится меню, содержащее команды для добавления модуля или фрагмента.</span><span class="sxs-lookup"><span data-stu-id="6c25a-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="6c25a-128">Чтобы удалить модуль или фрагмент, найдите и выберите его в дереве структуры страницы, выберите кнопку с многоточием, затем выберите команду для удаления модуля или фрагмента.</span><span class="sxs-lookup"><span data-stu-id="6c25a-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="6c25a-129">Кроме того, можно просматривать и изменять свойства любого модуля, который отображается в разделе предварительного просмотра визуального конструктора страниц, выбрав его непосредственно.</span><span class="sxs-lookup"><span data-stu-id="6c25a-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="6c25a-130">После завершения внесения изменений и предварительного просмотра их результатов следует вернуть страницу, выбрав **Завершить правку** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="6c25a-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="6c25a-131">Чтобы немедленно опубликовать изменения, выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="6c25a-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="6c25a-132">Последняя возвращенная версия измененной страницы публикуется и становится доступной внешним пользователям, просматривающим сайт.</span><span class="sxs-lookup"><span data-stu-id="6c25a-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="6c25a-133">Пример: изменение видео на домашней странице</span><span class="sxs-lookup"><span data-stu-id="6c25a-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="6c25a-134">В следующем примере показано, как изменить домашнюю страницу, изменив видеозапись, которая отображается в модуле видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="6c25a-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="6c25a-135">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="6c25a-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="6c25a-136">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="6c25a-137">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="6c25a-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="6c25a-138">На панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="6c25a-139">В структуре страницы выберите слот **Главный**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="6c25a-140">В слоте **Главный** разверните все модули гибкого контейнера.</span><span class="sxs-lookup"><span data-stu-id="6c25a-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="6c25a-141">Найдите и выберите модуль видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="6c25a-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="6c25a-142">В области свойств справа выберите свойство **видео**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="6c25a-143">Отображается средство выбора активов.</span><span class="sxs-lookup"><span data-stu-id="6c25a-143">The asset picker appears.</span></span>
1. <span data-ttu-id="6c25a-144">В средстве выбора активов выберите доступный видеоактив или выберите команду **Отправить новый актив**, чтобы отправить новый видеоактив.</span><span class="sxs-lookup"><span data-stu-id="6c25a-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="6c25a-145">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-145">Select **OK**.</span></span>
1. <span data-ttu-id="6c25a-146">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="6c25a-147">В поле **Комментарии** введите **Изменена видеозапись**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="6c25a-148">Выберите **Предварительный просмотр** для предварительного просмотра обновленной страницы.</span><span class="sxs-lookup"><span data-stu-id="6c25a-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="6c25a-149">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="6c25a-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="6c25a-150">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="6c25a-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c25a-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6c25a-151">Additional resources</span></span>

[<span data-ttu-id="6c25a-152">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="6c25a-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="6c25a-153">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="6c25a-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="6c25a-154">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="6c25a-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="6c25a-155">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="6c25a-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="6c25a-156">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="6c25a-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="6c25a-157">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="6c25a-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="6c25a-158">Проверка специальных возможностей контента страницы</span><span class="sxs-lookup"><span data-stu-id="6c25a-158">Verify page content accessibility</span></span>](verify-accessibility.md)
