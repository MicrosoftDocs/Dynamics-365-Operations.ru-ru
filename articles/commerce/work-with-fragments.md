---
title: Работа с фрагментами
description: В этом разделе описывается, зачем, когда и как использовать фрагменты в Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f1525610fb16edd5ff9ccefe0194f6f27b797b62
ms.sourcegitcommit: 1a12b42cc17f004a981c716aed3da6cf538475a5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4415366"
---
# <a name="work-with-fragments"></a><span data-ttu-id="73e2b-103">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="73e2b-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="73e2b-104">В этом разделе описывается, зачем, когда и как использовать фрагменты в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="73e2b-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="73e2b-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="73e2b-105">Overview</span></span>

<span data-ttu-id="73e2b-106">Фрагменты позволяют выполнять централизованную разработку для конфигураций модулей, которые должны быть повторно использованы на сайте.</span><span class="sxs-lookup"><span data-stu-id="73e2b-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="73e2b-107">Например, заголовки, нижние колонтитулы и баннеры часто настраиваются как фрагменты, так как они являются общими для нескольких страниц.</span><span class="sxs-lookup"><span data-stu-id="73e2b-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="73e2b-108">Фрагменты можно рассматривать как миниатюрные веб-страницы, которые могут быть вставлены на другие страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="73e2b-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="73e2b-109">Фрагменты имеют свой собственный жизненный цикл.</span><span class="sxs-lookup"><span data-stu-id="73e2b-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="73e2b-110">Другими словами, они создаются, используются в ссылках, обновляются и удаляются как независимые сущности в инструментах разработки.</span><span class="sxs-lookup"><span data-stu-id="73e2b-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="73e2b-111">После настройки фрагментов их можно использовать везде, где можно использовать модули в структуре сайта.</span><span class="sxs-lookup"><span data-stu-id="73e2b-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="73e2b-112">На фрагменты можно ссылаться на страницах, в макетах, в шаблонах и в других фрагментах.</span><span class="sxs-lookup"><span data-stu-id="73e2b-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="73e2b-113">Фрагменты могут быть вложены до семи уровней внутри других фрагментов.</span><span class="sxs-lookup"><span data-stu-id="73e2b-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="73e2b-114">Например, если необходимо рекламировать сезонное событие на нескольких страницах сайта, можно использовать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="73e2b-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="73e2b-115">Первый шаг в процессе создания нового фрагмента — выбор типа модуля, с которого необходимо начать.</span><span class="sxs-lookup"><span data-stu-id="73e2b-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="73e2b-116">В данном примере можно создать фрагмент из модуля главного имиджевого баннера.</span><span class="sxs-lookup"><span data-stu-id="73e2b-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="73e2b-117">Фрагменты могут быть построены из любого типа модуля.</span><span class="sxs-lookup"><span data-stu-id="73e2b-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="73e2b-118">Затем можно настроить фрагмент главного имиджевого баннера с использованием специфического рекламного содержимого.</span><span class="sxs-lookup"><span data-stu-id="73e2b-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="73e2b-119">Можно также локализовать его, как требуется.</span><span class="sxs-lookup"><span data-stu-id="73e2b-119">You can also localize it as you require.</span></span> <span data-ttu-id="73e2b-120">Новый отдельный фрагмент главного имиджевого баннера может затем использоваться как заранее настроенный модуль для всего сайта.</span><span class="sxs-lookup"><span data-stu-id="73e2b-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="73e2b-121">Его можно легко добавить к шаблонам, на отдельные страницы или в другие фрагменты, которые могут содержать модули главного имиджевого баннера.</span><span class="sxs-lookup"><span data-stu-id="73e2b-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="73e2b-122">Все места, в которые добавляется фрагмент, являются ссылками на центральный созданный вами фрагмент главного имиджевого баннера.</span><span class="sxs-lookup"><span data-stu-id="73e2b-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="73e2b-123">При публикации изменений, внесенных в фрагмент, эти изменения немедленно отражаются во всех местах, где имеется ссылка на этот фрагмент на сайте.</span><span class="sxs-lookup"><span data-stu-id="73e2b-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="73e2b-124">Таким образом, фрагменты предоставляют мощный и эффективный способ повторного использования конфигураций модулей на сайте и централизованного управления ими.</span><span class="sxs-lookup"><span data-stu-id="73e2b-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="73e2b-125">Эффективно используя их, можно значительно повысить гибкость и снизить затраты, связанные с управлением содержимым сайта.</span><span class="sxs-lookup"><span data-stu-id="73e2b-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="73e2b-126">На следующем рисунке показано, как можно использовать фрагменты для централизации создания общих конфигураций модулей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="73e2b-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Рисунок, показывающий, как можно использовать фрагменты для централизации создания общих конфигураций модулей на сайте электронной коммерции](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="73e2b-128">Создание фрагмента</span><span class="sxs-lookup"><span data-stu-id="73e2b-128">Create a fragment</span></span>

<span data-ttu-id="73e2b-129">Можно создать новый фрагмент либо сохранить существующую конфигурацию модуля в качестве фрагмента.</span><span class="sxs-lookup"><span data-stu-id="73e2b-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="73e2b-130">Сохранение существующей конфигурации модуля в качестве фрагмента</span><span class="sxs-lookup"><span data-stu-id="73e2b-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="73e2b-131">Чтобы преобразовать ранее настроенный модуль в фрагмент многократного использования в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73e2b-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="73e2b-132">Откройте страницу или шаблон, содержащий модуль, который требуется преобразовать в фрагмент.</span><span class="sxs-lookup"><span data-stu-id="73e2b-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="73e2b-133">В области структуры слева или непосредственно в визуальном конструкторе страниц выберите настроенный ранее модуль.</span><span class="sxs-lookup"><span data-stu-id="73e2b-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="73e2b-134">Нажмите кнопку с многоточием (**...**) рядом с именем модуля в области структуры или на панели инструментов выбранного модуля в визуальном конструкторе страниц.</span><span class="sxs-lookup"><span data-stu-id="73e2b-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="73e2b-135">Выберите **Использовать совместно как фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="73e2b-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="73e2b-136">В диалоговом окне **Сохранить как фрагмент** укажите имя фрагмента.</span><span class="sxs-lookup"><span data-stu-id="73e2b-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="73e2b-137">Выберите **ОК**, чтобы сохранить конфигурацию модуля в виде фрагмента, который может быть добавлен к другим страницам.</span><span class="sxs-lookup"><span data-stu-id="73e2b-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="73e2b-138">Создание нового фрагмента</span><span class="sxs-lookup"><span data-stu-id="73e2b-138">Create a new fragment</span></span>

<span data-ttu-id="73e2b-139">Чтобы создать новый фрагмент в конфигураторе сайта Commerce, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="73e2b-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="73e2b-140">В области переходов слева выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="73e2b-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="73e2b-141">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="73e2b-141">Select **New**.</span></span> <span data-ttu-id="73e2b-142">Откроется диалоговое окно **Создать фрагмент**, в котором отображаются все доступные типы модулей.</span><span class="sxs-lookup"><span data-stu-id="73e2b-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="73e2b-143">Как упоминалось ранее, фрагменты могут быть созданы из любого типа модуля.</span><span class="sxs-lookup"><span data-stu-id="73e2b-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="73e2b-144">Выберите тип модуля для фрагмента.</span><span class="sxs-lookup"><span data-stu-id="73e2b-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="73e2b-145">При выборе универсального типа модуля-контейнера можно добиться большей гибкости, когда необходимо позднее выполнить обновление и настройку фрагмента.</span><span class="sxs-lookup"><span data-stu-id="73e2b-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="73e2b-146">Добавление, удаление или редактирование фрагментов на странице</span><span class="sxs-lookup"><span data-stu-id="73e2b-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="73e2b-147">Следующие процедуры описывают добавление, удаление и редактирование фрагментов.</span><span class="sxs-lookup"><span data-stu-id="73e2b-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="73e2b-148">Добавление фрагмента</span><span class="sxs-lookup"><span data-stu-id="73e2b-148">Add a fragment</span></span>

<span data-ttu-id="73e2b-149">Чтобы добавить фрагмент на страницу в конфигураторе сайта Commerce, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="73e2b-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="73e2b-150">В области структуры слева или непосредственном в визуальном конструкторе страниц выберите контейнер или область, к которой можно добавить дочерние модули.</span><span class="sxs-lookup"><span data-stu-id="73e2b-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="73e2b-151">Выберите многоточие (**...**) рядом с именем контейнера или ячейки.</span><span class="sxs-lookup"><span data-stu-id="73e2b-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="73e2b-152">В качестве альтернативы, если используется визуальный конструктор страниц, выберите символ "плюс" (**+**).</span><span class="sxs-lookup"><span data-stu-id="73e2b-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="73e2b-153">Выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="73e2b-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="73e2b-154">Если контейнер или слот не поддерживают новые дочерние модули, параметр **Добавить фрагмент** будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="73e2b-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="73e2b-155">В диалоговом окне **Выбрать фрагмент** найдите и выберите фрагмент, который требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="73e2b-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="73e2b-156">Если доступных фрагментов нет в списке, можно сначала создать фрагмент из типа модуля, поддерживаемого выбранным контейнером или слотом.</span><span class="sxs-lookup"><span data-stu-id="73e2b-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="73e2b-157">Выберите желаемый фрагмент, чтобы добавить его в контейнер или слот на странице.</span><span class="sxs-lookup"><span data-stu-id="73e2b-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="73e2b-158">Модули, разрешенные в контейнере или в слоте, определяются шаблоном страницы или собственными определениями модулей.</span><span class="sxs-lookup"><span data-stu-id="73e2b-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="73e2b-159">Удаление фрагмента</span><span class="sxs-lookup"><span data-stu-id="73e2b-159">Remove a fragment</span></span>

<span data-ttu-id="73e2b-160">Чтобы удалить фрагмент из гнезда или контейнера на странице в конфигураторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73e2b-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="73e2b-161">В области структуры в левой части выберите кнопку с многоточием (**...**) рядом с названием удаляемого фрагмента, затем нажмите символ корзины.</span><span class="sxs-lookup"><span data-stu-id="73e2b-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="73e2b-162">Кроме того, можно выбрать фрагмент в визуальном конструкторе страниц и выбрать символ корзины на панели инструментов фрагмента.</span><span class="sxs-lookup"><span data-stu-id="73e2b-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="73e2b-163">При появлении запроса на подтверждение удаления фрагмента выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73e2b-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="73e2b-164">При удалении фрагмента со страницы просто удаляется ссылка на него с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="73e2b-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="73e2b-165">Вы **не** удаляете этот фрагмент с сайта.</span><span class="sxs-lookup"><span data-stu-id="73e2b-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="73e2b-166">Чтобы удалить фрагменты с сайта, необходимо воспользоваться пользовательским интерфейсом (UI) инспектора фрагментов.</span><span class="sxs-lookup"><span data-stu-id="73e2b-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="73e2b-167">Удалить фрагменты с сайта можно только в том случае, если на них в данный момент нет ссылок ни на одной странице, шаблоне или в других фрагментах.</span><span class="sxs-lookup"><span data-stu-id="73e2b-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="73e2b-168">Редактирование фрагмента</span><span class="sxs-lookup"><span data-stu-id="73e2b-168">Edit a fragment</span></span>

<span data-ttu-id="73e2b-169">Чтобы изменить фрагменты, необходимо использовать интерфейс пользователя редактора фрагментов.</span><span class="sxs-lookup"><span data-stu-id="73e2b-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="73e2b-170">Такое ограничение предусмотрено специально.</span><span class="sxs-lookup"><span data-stu-id="73e2b-170">This restriction is by design.</span></span> <span data-ttu-id="73e2b-171">Это помогает гарантировать, что авторы не будут путать процесс редактирования модулей для определенной страницы с процессом редактирования фрагментов, которые могут использоваться несколькими страницами.</span><span class="sxs-lookup"><span data-stu-id="73e2b-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="73e2b-172">Чтобы изменить фрагмент в конфигураторе сайта Commerce, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="73e2b-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="73e2b-173">В области переходов слева выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="73e2b-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="73e2b-174">В области **Фрагменты** выберите фрагмент для редактирования.</span><span class="sxs-lookup"><span data-stu-id="73e2b-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="73e2b-175">Измените необходимые свойства модуля и структуру в фрагменте.</span><span class="sxs-lookup"><span data-stu-id="73e2b-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="73e2b-176">Процесс похож на процесс редактирования модулей при редактировании в представлении редактора страниц.</span><span class="sxs-lookup"><span data-stu-id="73e2b-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="73e2b-177">Кроме того, можно изменить фрагмент, выбрав его на странице, в шаблоне или в родительском фрагменте, а затем выбрав **Изменить фрагмент** в правой области свойств.</span><span class="sxs-lookup"><span data-stu-id="73e2b-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73e2b-178">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73e2b-178">Additional resources</span></span>

[<span data-ttu-id="73e2b-179">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="73e2b-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="73e2b-180">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="73e2b-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="73e2b-181">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="73e2b-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="73e2b-182">Работа с группами публикаций</span><span class="sxs-lookup"><span data-stu-id="73e2b-182">Work with publish groups</span></span>](publish-groups.md)
