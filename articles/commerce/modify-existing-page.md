---
title: Изменение существующей страницы сайта
description: В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803737"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="d4dbb-103">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="d4dbb-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4dbb-104">В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d4dbb-105">Когда необходимо изменить страницу, первым шагом является ее открытие в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="d4dbb-106">Перейдите на сайт, содержащий страницу, затем в списке страниц найдите нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="d4dbb-107">Если не удается найти страницу, можно воспользоваться функциями расширенного поиска инструмента разработки.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="d4dbb-108">Либо введите точное имя страницы, либо введите первые несколько букв, а затем звездочку (\*).</span><span class="sxs-lookup"><span data-stu-id="d4dbb-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="d4dbb-109">Отображается отфильтрованный список страниц.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-109">A filtered list of pages appears.</span></span> <span data-ttu-id="d4dbb-110">С помощью этого списка можно найти нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="d4dbb-111">После того, как вы нашли правильную страницу, выберите имя страницы, чтобы открыть страницу в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="d4dbb-112">Если страница отображается в инспекторе страниц, можно выбрать **Изменить** и извлечь эту страницу перед открытием в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="d4dbb-113">Таким образом можно извлекать несколько страниц одновременно.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="d4dbb-114">После открытия страницы в редакторе страниц необходимо убедиться, что она извлечена вами.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="d4dbb-115">Панель команд в инструменте разработки является динамической, контекстно-зависимой и с учетом состояния.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="d4dbb-116">Таким образом отображаются только те действия, которые можно выполнить на странице в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="d4dbb-117">Например, если страница не извлечена вами, кнопки **Сохранить** и **Завершить правку** не появляются на панели команд.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="d4dbb-118">Состояние страницы также отображается в правой части окна.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="d4dbb-119">Если страница еще не извлечена, выберите **Изменить** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="d4dbb-120">Панель команд изменяется, отражая новое состояние страницы.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="d4dbb-121">Также вы получаете уведомление о том, что страница была извлечена вами.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="d4dbb-122">Следующий шаг состоит в выполнении фактических изменений.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="d4dbb-123">Часто для поиска и выбора модуля, который необходимо изменить, используется дерево структуры страниц в левой части, а затем вносятся изменения на панели свойств справа.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="d4dbb-124">Однако в некоторых случаях изменения могут включать добавление или удаление модулей или фрагментов.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="d4dbb-125">Чтобы добавить фрагмент или модуль, используйте деревом структуры страниц, чтобы найти гнездо, в которое необходимо добавить модуль или фрагмент, затем нажмите кнопку с многоточием (**...**) для этого гнезда.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="d4dbb-126">Появится меню, содержащее команды для добавления модуля или фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="d4dbb-127">Чтобы удалить модуль или фрагмент, найдите и выберите его в дереве структуры страницы, выберите кнопку с многоточием, затем выберите команду для удаления модуля или фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="d4dbb-128">Кроме того, можно просматривать и изменять свойства любого модуля, который отображается в разделе предварительного просмотра визуального конструктора страниц, выбрав его непосредственно.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="d4dbb-129">После завершения внесения изменений и предварительного просмотра их результатов следует вернуть страницу, выбрав **Завершить правку** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="d4dbb-130">Чтобы немедленно опубликовать изменения, выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="d4dbb-131">Последняя возвращенная версия измененной страницы публикуется и становится доступной внешним пользователям, просматривающим сайт.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="d4dbb-132">Пример: изменение видео на домашней странице</span><span class="sxs-lookup"><span data-stu-id="d4dbb-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="d4dbb-133">В следующем примере показано, как изменить домашнюю страницу, изменив видеозапись, которая отображается в модуле видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="d4dbb-134">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="d4dbb-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d4dbb-135">В области переходов слева выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="d4dbb-136">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="d4dbb-137">На панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="d4dbb-138">В структуре страницы выберите слот **Главный**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="d4dbb-139">В слоте **Главный** разверните все модули гибкого контейнера.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="d4dbb-140">Найдите и выберите модуль видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="d4dbb-141">В области свойств справа выберите свойство **видео**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="d4dbb-142">Отображается средство выбора активов.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-142">The asset picker appears.</span></span>
1. <span data-ttu-id="d4dbb-143">В средстве выбора активов выберите доступный видеоактив или выберите команду **Отправить новый актив**, чтобы отправить новый видеоактив.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="d4dbb-144">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-144">Select **OK**.</span></span>
1. <span data-ttu-id="d4dbb-145">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d4dbb-146">В поле **Комментарии** введите **Изменена видеозапись**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="d4dbb-147">Выберите **Предварительный просмотр** для предварительного просмотра обновленной страницы.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="d4dbb-148">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="d4dbb-149">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="d4dbb-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4dbb-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4dbb-150">Additional resources</span></span>

[<span data-ttu-id="d4dbb-151">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="d4dbb-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d4dbb-152">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="d4dbb-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d4dbb-153">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="d4dbb-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d4dbb-154">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="d4dbb-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d4dbb-155">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="d4dbb-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d4dbb-156">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="d4dbb-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="d4dbb-157">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="d4dbb-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="d4dbb-158">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="d4dbb-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
