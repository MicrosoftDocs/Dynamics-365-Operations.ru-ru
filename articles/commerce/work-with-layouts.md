---
title: Работа с предустановленными макетами
description: В этом разделе описывается, как работать с предустановленными макетами в Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2539880e76ffb1861e0d18227a935a2ef35c120
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210883"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="e7633-103">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="e7633-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e7633-104">В этом разделе описывается, как работать с предустановленными макетами в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7633-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7633-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e7633-105">Overview</span></span>

<span data-ttu-id="e7633-106">Прежде чем выполнять процедуры, описанные в этом разделе, следует ознакомиться с разделом [Предустановленные и пользовательские макеты](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="e7633-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="e7633-107">Общие сведения см. в разделе [Общие сведения о шаблонах и макетах](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e7633-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="e7633-108">Создание нового предустановленного макета</span><span class="sxs-lookup"><span data-stu-id="e7633-108">Create a new preset layout</span></span>

<span data-ttu-id="e7633-109">Существует два метода создания предустановленного макета.</span><span class="sxs-lookup"><span data-stu-id="e7633-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="e7633-110">Можно сохранить существующий пользовательский макет или создать предустановленный макет с нуля.</span><span class="sxs-lookup"><span data-stu-id="e7633-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="e7633-111">Создание предустановленного макета из существующего пользовательского макета</span><span class="sxs-lookup"><span data-stu-id="e7633-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="e7633-112">Для создания предустановленного макета из существующего пользовательского макета выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7633-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="e7633-113">Откройте существующую страницу, которая в настоящее время не использует предустановленный макет, и имеет структуру модулей, которую необходимо повторно использовать для других страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="e7633-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="e7633-114">Выберите **Правка**, чтобы извлечь страницу.</span><span class="sxs-lookup"><span data-stu-id="e7633-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="e7633-115">Выберите **Сохранить как новый макет**.</span><span class="sxs-lookup"><span data-stu-id="e7633-115">Select **Save as new layout**.</span></span> <span data-ttu-id="e7633-116">Откроется диалоговое окно **Сохранить как новый макет**.</span><span class="sxs-lookup"><span data-stu-id="e7633-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="e7633-117">Введите имя и описание для предустановленного макета.</span><span class="sxs-lookup"><span data-stu-id="e7633-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="e7633-118">Введенные значения будут отображаться для других авторов при создании новых страниц из вашего макета или при переключении на него.</span><span class="sxs-lookup"><span data-stu-id="e7633-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="e7633-119">Поэтому введите значения, которые будут полезны для авторов страниц.</span><span class="sxs-lookup"><span data-stu-id="e7633-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="e7633-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e7633-120">Select **OK**.</span></span>

<span data-ttu-id="e7633-121">Предустановленный макет теперь будет доступен при создании новых страниц или выборе другого макета для страницы в той же иерархии шаблонов.</span><span class="sxs-lookup"><span data-stu-id="e7633-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="e7633-122">Чтобы быстро проверить, привязана ли в данный момент конкретная страница к предустановленному макету, выберите страницу в представлении списка страниц и проверьте метаданные макета на панели свойств справа.</span><span class="sxs-lookup"><span data-stu-id="e7633-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="e7633-123">Создание нового предустановленного макета</span><span class="sxs-lookup"><span data-stu-id="e7633-123">Create a new preset layout</span></span>

<span data-ttu-id="e7633-124">Для создания предустановленного макета с нуля выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7633-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="e7633-125">В области переходов слева выберите **Макеты**.</span><span class="sxs-lookup"><span data-stu-id="e7633-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="e7633-126">Выберите **Создать макет**.</span><span class="sxs-lookup"><span data-stu-id="e7633-126">Select **New Layout**.</span></span> <span data-ttu-id="e7633-127">Откроется диалоговое окно **Создать макет**.</span><span class="sxs-lookup"><span data-stu-id="e7633-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="e7633-128">Выберите шаблон, который будет использоваться для предустановленного макета.</span><span class="sxs-lookup"><span data-stu-id="e7633-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="e7633-129">Введите имя и описание для предустановленного макета.</span><span class="sxs-lookup"><span data-stu-id="e7633-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="e7633-130">Введенные значения будут отображаться для других авторов при создании новых страниц из вашего макета или при переключении на него.</span><span class="sxs-lookup"><span data-stu-id="e7633-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="e7633-131">Поэтому введите значения, которые будут полезны для авторов страниц.</span><span class="sxs-lookup"><span data-stu-id="e7633-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="e7633-132">Выберите **ОК**, чтобы создать новый предустановленный макет и открыть редактор макетов.</span><span class="sxs-lookup"><span data-stu-id="e7633-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="e7633-133">В редакторе макетов добавьте и настройте модули, используя дерево структуры в левой части и на панель свойств справа.</span><span class="sxs-lookup"><span data-stu-id="e7633-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="e7633-134">(Процесс похож на процесс для добавления и настройки модулей для шаблона в редакторе шаблонов.) Расположение модулей и всех заблокированных настроек по умолчанию становится централизованной конфигурацией модулей для всех страниц, использующих этот предустановленный макет.</span><span class="sxs-lookup"><span data-stu-id="e7633-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="e7633-135">Изменение предустановленного макета</span><span class="sxs-lookup"><span data-stu-id="e7633-135">Modify a preset layout</span></span>

<span data-ttu-id="e7633-136">Чтобы изменить предустановленный макет, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7633-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="e7633-137">В области переходов слева выберите **Макеты**.</span><span class="sxs-lookup"><span data-stu-id="e7633-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="e7633-138">В редакторе макетов в дереве структуры слева выберите модуль, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="e7633-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="e7633-139">Затем выполните любое из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="e7633-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="e7633-140">Чтобы переместить модуль вверх или вниз внутри родительского модуля, выберите кнопку с многоточием (**...**) для модуля, затем выберите **Переместить вверх** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="e7633-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="e7633-141">Чтобы изменить настройки модуля по умолчанию, используйте панель свойств для ввода значений по умолчанию и, при необходимости, блокировки для всех нижестоящих страниц.</span><span class="sxs-lookup"><span data-stu-id="e7633-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="e7633-142">Чтобы добавить новые модули или фрагменты в модули-контейнеры, выберите кнопку с многоточием, затем выберите **Добавить модуль** или **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="e7633-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="e7633-143">Чтобы удалить модуль из макета, выберите кнопку с многоточием, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e7633-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="e7633-144">Изменение темы предустановленного макета</span><span class="sxs-lookup"><span data-stu-id="e7633-144">Change a preset layout theme</span></span>

<span data-ttu-id="e7633-145">Стандартной практикой является задание темы по умолчанию для всех страниц, использующих предустановленный макет.</span><span class="sxs-lookup"><span data-stu-id="e7633-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="e7633-146">Чтобы задать или изменить тему для всех дочерних страниц, использующих предустановленный макет, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7633-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="e7633-147">В редакторе макетов в дереве структуры слева выберите модуль-контейнер страницы.</span><span class="sxs-lookup"><span data-stu-id="e7633-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="e7633-148">(Обычно этот модуль является вторым узлом и называется **Страница по умолчанию**.)</span><span class="sxs-lookup"><span data-stu-id="e7633-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="e7633-149">В области свойств справа в поле **Тема** выберите тему.</span><span class="sxs-lookup"><span data-stu-id="e7633-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="e7633-150">Сохранение, возврат, предварительный просмотр и публикация предустановленного макета</span><span class="sxs-lookup"><span data-stu-id="e7633-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="e7633-151">Для сохранения и возврата предустановленного макета выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7633-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="e7633-152">Выберите **Сохранить** в верхней части редактора макетов.</span><span class="sxs-lookup"><span data-stu-id="e7633-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="e7633-153">Сохраненные изменения не влияют на нисходящие страницы, пока они не будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="e7633-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="e7633-154">Выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e7633-154">Select **Finish editing**.</span></span> <span data-ttu-id="e7633-155">Ваши изменения теперь доступны для нижестоящих рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="e7633-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="e7633-156">Для предварительного просмотра изменений либо откройте существующую страницу, использующую этот предустановленный макет, либо создайте новую страницу на основе этого макета.</span><span class="sxs-lookup"><span data-stu-id="e7633-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="e7633-157">После предварительного просмотра изменений вашего предустановленного макета выполните одно из следующих действий, чтобы опубликовать макет на действующем сайте:</span><span class="sxs-lookup"><span data-stu-id="e7633-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="e7633-158">Перейдите к пункту **Маеты**, выберите макет, затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e7633-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="e7633-159">Выберите имя макета, чтобы открыть редактор макетов, затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e7633-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="e7633-160">Опубликуйте страницу, которая ссылается на неопубликованный макет.</span><span class="sxs-lookup"><span data-stu-id="e7633-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="e7633-161">Макет будет опубликован автоматически.</span><span class="sxs-lookup"><span data-stu-id="e7633-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="e7633-162">На предустановленные макеты могут ссылаться несколько страниц.</span><span class="sxs-lookup"><span data-stu-id="e7633-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="e7633-163">При публикации предустановленного макета имейте ввиду, что это может повлиять на компоновку нескольких страниц.</span><span class="sxs-lookup"><span data-stu-id="e7633-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7633-164">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7633-164">Additional resources</span></span>

[<span data-ttu-id="e7633-165">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="e7633-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e7633-166">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="e7633-166">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]