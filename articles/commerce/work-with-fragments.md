---
title: Работа с фрагментами
description: В этом разделе описывается, зачем, когда и как использовать фрагменты в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914708"
---
# <a name="work-with-fragments"></a><span data-ttu-id="8b1f2-103">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="8b1f2-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8b1f2-104">В этом разделе описывается, зачем, когда и как использовать фрагменты в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8b1f2-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="8b1f2-105">Overview</span></span>

<span data-ttu-id="8b1f2-106">Фрагменты позволяют выполнять централизованную разработку для конфигураций модулей, которые должны быть повторно использованы на сайте.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="8b1f2-107">Например, заголовки, нижние колонтитулы и баннеры часто настраиваются как фрагменты, так как они являются общими для нескольких страниц.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="8b1f2-108">Фрагменты можно рассматривать как миниатюрные веб-страницы, которые могут быть вставлены на другие страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="8b1f2-109">Фрагменты имеют свой собственный жизненный цикл.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="8b1f2-110">Другими словами, они создаются, используются в ссылках, обновляются и удаляются как независимые сущности в инструментах разработки.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="8b1f2-111">После настройки фрагментов их можно использовать везде, где можно использовать модули в структуре сайта.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="8b1f2-112">На фрагменты можно ссылаться на страницах, в макетах, в шаблонах и в других фрагментах.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="8b1f2-113">Фрагменты могут быть вложены до семи уровней внутри других фрагментов.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="8b1f2-114">Например, если необходимо рекламировать сезонное событие на нескольких страницах сайта, можно использовать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="8b1f2-115">Первый шаг в процессе создания нового фрагмента — выбор типа модуля, с которого необходимо начать.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="8b1f2-116">В данном примере можно создать фрагмент из модуля главного имиджевого баннера.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="8b1f2-117">Фрагменты могут быть построены из любого типа модуля.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="8b1f2-118">Затем можно настроить фрагмент главного имиджевого баннера с использованием специфического рекламного содержимого.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="8b1f2-119">Можно также локализовать его, как требуется.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-119">You can also localize it as you require.</span></span> <span data-ttu-id="8b1f2-120">Новый отдельный фрагмент главного имиджевого баннера может затем использоваться как заранее настроенный модуль для всего сайта.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="8b1f2-121">Его можно легко добавить к шаблонам, на отдельные страницы или в другие фрагменты, которые могут содержать модули главного имиджевого баннера.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="8b1f2-122">Все места, в которые добавляется фрагмент, являются ссылками на центральный созданный вами фрагмент главного имиджевого баннера.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="8b1f2-123">При публикации изменений, внесенных в фрагмент, эти изменения немедленно отражаются во всех местах, где имеется ссылка на этот фрагмент на сайте.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="8b1f2-124">Таким образом, фрагменты предоставляют мощный и эффективный способ повторного использования конфигураций модулей на сайте и централизованного управления ими.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="8b1f2-125">Эффективно используя их, можно значительно повысить гибкость и снизить затраты, связанные с управлением содержимым сайта.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="8b1f2-126">На следующем рисунке показано, как можно использовать фрагменты для централизации создания общих конфигураций модулей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Рисунок, показывающий, как можно использовать фрагменты для централизации создания общих конфигураций модулей на сайте электронной коммерции](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="8b1f2-128">Создание фрагмента</span><span class="sxs-lookup"><span data-stu-id="8b1f2-128">Create a fragment</span></span>

<span data-ttu-id="8b1f2-129">Можно создать новый фрагмент либо сохранить существующую конфигурацию модуля в качестве фрагмента.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="8b1f2-130">Создание нового фрагмента</span><span class="sxs-lookup"><span data-stu-id="8b1f2-130">Create a new fragment</span></span>

<span data-ttu-id="8b1f2-131">Чтобы создать новый фрагмент, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="8b1f2-132">В области переходов слева выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="8b1f2-133">Выберите **Создать фрагмент страницы**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="8b1f2-134">Откроется диалоговое окно, в котором отображаются все доступные типы модулей.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="8b1f2-135">Как упоминалось ранее, фрагменты могут быть созданы из любого типа модуля.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="8b1f2-136">Выберите тип модуля для данного фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="8b1f2-137">При выборе универсального типа модуля-контейнера можно добиться большей гибкости, когда необходимо позднее выполнить обновление и настройку фрагмента.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="8b1f2-138">Сохранение существующей конфигурации модуля в качестве фрагмента</span><span class="sxs-lookup"><span data-stu-id="8b1f2-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="8b1f2-139">Чтобы преобразовать ранее настроенный модуль в фрагмент многократного использования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="8b1f2-140">Откройте страницу или шаблон, содержащий модуль, который требуется преобразовать в фрагмент.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="8b1f2-141">В области структуры в левой части выберите кнопку с многоточием (**...**) рядом с названием модуля, затем выберите **Сохранить как фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="8b1f2-142">Отобразится диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-142">A dialog box appears.</span></span>
1. <span data-ttu-id="8b1f2-143">Введите имя и метаданные для фрагмента.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="8b1f2-144">Выберите **ОК**, чтобы сохранить конфигурацию модуля в виде фрагмента, который может быть добавлен к другим страницам.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="8b1f2-145">Добавление, удаление или редактирование фрагментов на странице</span><span class="sxs-lookup"><span data-stu-id="8b1f2-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="8b1f2-146">Следующие процедуры описывают добавление, удаление и редактирование фрагментов.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="8b1f2-147">Добавление фрагмента</span><span class="sxs-lookup"><span data-stu-id="8b1f2-147">Add a fragment</span></span>

<span data-ttu-id="8b1f2-148">Чтобы добавить фрагмент на страницу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="8b1f2-149">В области структуры слева выберите контейнер или ячейку, в которую можно добавить дочерние модули.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="8b1f2-150">Выберите кнопку с многоточием рядом с именем контейнера или ячейки, затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="8b1f2-151">Отобразится диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b1f2-152">Если контейнер или слот не поддерживают новые дочерние модули, параметр **Добавить фрагмент** будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="8b1f2-153">В диалоговом окне найдите и выберите фрагмент, который требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="8b1f2-154">Если доступных фрагментов нет в списке, можно сначала создать фрагмент из типа модуля, поддерживаемого выбранным контейнером или слотом.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="8b1f2-155">Выберите **ОК**, чтобы добавить выбранный фрагмент в выбранный контейнер или ячейку на странице.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="8b1f2-156">Модули, разрешенные в контейнере или в слоте, определяются шаблоном страницы или собственными определениями модулей.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="8b1f2-157">Удаление фрагмента</span><span class="sxs-lookup"><span data-stu-id="8b1f2-157">Remove a fragment</span></span>

<span data-ttu-id="8b1f2-158">Чтобы удалить фрагмент из ячейки или контейнера на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="8b1f2-159">В области структуры в левой части выберите кнопку с многоточием рядом с названием удаляемого фрагмента, затем нажмите кнопку корзины.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="8b1f2-160">При появлении запроса на подтверждение удаления фрагмента выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="8b1f2-161">При удалении фрагмента со страницы просто удаляется ссылка на него с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="8b1f2-162">Вы **не** удаляете этот фрагмент с сайта.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="8b1f2-163">Чтобы удалить фрагменты с сайта, необходимо воспользоваться пользовательским интерфейсом (UI) инспектора фрагментов.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="8b1f2-164">Удалить фрагменты с сайта можно только в том случае, если на них в данный момент нет ссылок ни на одной странице, шаблоне или в других фрагментах.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="8b1f2-165">Редактирование фрагмента</span><span class="sxs-lookup"><span data-stu-id="8b1f2-165">Edit a fragment</span></span>

<span data-ttu-id="8b1f2-166">Чтобы изменить фрагменты, необходимо использовать интерфейс пользователя редактора фрагментов.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="8b1f2-167">Такое ограничение предусмотрено специально.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-167">This restriction is by design.</span></span> <span data-ttu-id="8b1f2-168">Это помогает гарантировать, что авторы не будут путать процесс редактирования модулей для определенной страницы с процессом редактирования фрагментов, которые могут использоваться несколькими страницами.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="8b1f2-169">Чтобы изменить фрагмент, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="8b1f2-170">В области переходов слева выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="8b1f2-171">В области **Фрагменты** выберите фрагмент для редактирования.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="8b1f2-172">Измените необходимые свойства модуля и структуру в фрагменте.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="8b1f2-173">Процесс похож на процесс редактирования модулей при редактировании в представлении редактора страниц.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="8b1f2-174">Кроме того, можно изменить фрагмент, выбрав его на странице, в шаблоне или в родительском фрагменте, а затем выбрав **Изменить фрагмент** в правой области свойств.</span><span class="sxs-lookup"><span data-stu-id="8b1f2-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b1f2-175">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8b1f2-175">Additional resources</span></span>

[<span data-ttu-id="8b1f2-176">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="8b1f2-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="8b1f2-177">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="8b1f2-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="8b1f2-178">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="8b1f2-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="8b1f2-179">Работа с группами публикаций</span><span class="sxs-lookup"><span data-stu-id="8b1f2-179">Work with publish groups</span></span>](publish-groups.md)
