---
title: Работа с модулями
description: В этом разделе описывается, как и когда использовать модули в Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801369"
---
# <a name="work-with-modules"></a><span data-ttu-id="2445d-103">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="2445d-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2445d-104">В этом разделе описывается, как и когда использовать модули в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2445d-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2445d-105">Модули являются логическими строительными блоками, составляющими структуру страницы, и они имеют различные цели и области действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-105">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="2445d-106">Некоторые модули являются контейнерами высокого уровня, и их единственная цель состоит в том, чтобы хранить и организовывать другие модули (дочерние модули).</span><span class="sxs-lookup"><span data-stu-id="2445d-106">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="2445d-107">Другие модули, такие как простой модуль размещения изображений, имеют очень конкретную цель.</span><span class="sxs-lookup"><span data-stu-id="2445d-107">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="2445d-108">Другие модули, например, модуль карусели, попадают где-то посередине между этими двумя категориями.</span><span class="sxs-lookup"><span data-stu-id="2445d-108">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="2445d-109">По умолчанию ваш сайт Dynamics 365 Commerce включает библиотеку модулей, которая позволяет использовать большинство основных сценариев электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="2445d-109">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="2445d-110">Вы должны быть способны создавать законченный сайт электронной коммерции только с помощью этих модулей.</span><span class="sxs-lookup"><span data-stu-id="2445d-110">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="2445d-111">Однако, возможно, вы захотите настроить эти модули или создать новые, пользовательские модули для конкретных нужд.</span><span class="sxs-lookup"><span data-stu-id="2445d-111">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="2445d-112">Если требуется создать пользовательские модули, предусмотрен пакет средств разработки дизайна модулей (SDK), который поможет в создании библиотеки пользовательских модулей.</span><span class="sxs-lookup"><span data-stu-id="2445d-112">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="2445d-113">Контейнерные модули и ячейки</span><span class="sxs-lookup"><span data-stu-id="2445d-113">Container modules and slots</span></span>

<span data-ttu-id="2445d-114">Как упоминалось ранее, некоторые модули предназначены для размещения дочерних модулей.</span><span class="sxs-lookup"><span data-stu-id="2445d-114">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="2445d-115">Эти модули называются *контейнерами* и позволяют использовать иерархии вложенных модулей.</span><span class="sxs-lookup"><span data-stu-id="2445d-115">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="2445d-116">Контейнерные модули содержат *ячейки*.</span><span class="sxs-lookup"><span data-stu-id="2445d-116">Container modules include *slots*.</span></span> <span data-ttu-id="2445d-117">Ячейки используются для обработки макета и назначения дочерних модулей в контейнере.</span><span class="sxs-lookup"><span data-stu-id="2445d-117">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="2445d-118">Примером является модуль-контейнер базовой страницы (модуль верхнего уровня для любой страницы), определяющий несколько важных ячеек:</span><span class="sxs-lookup"><span data-stu-id="2445d-118">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="2445d-119">Ячейка заголовка</span><span class="sxs-lookup"><span data-stu-id="2445d-119">A header slot</span></span>
- <span data-ttu-id="2445d-120">Ячейка подзаголовка</span><span class="sxs-lookup"><span data-stu-id="2445d-120">A sub-header slot</span></span>
- <span data-ttu-id="2445d-121">Основная ячейка</span><span class="sxs-lookup"><span data-stu-id="2445d-121">A main slot</span></span>
- <span data-ttu-id="2445d-122">Ячейка нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="2445d-122">A footer slot</span></span>
- <span data-ttu-id="2445d-123">Ячейка вложенного нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="2445d-123">A sub-footer slot</span></span>

<span data-ttu-id="2445d-124">Разработчик модуля определяет эти ячейки и определяет, какие дочерние модули и в каком количестве могут быть размещены непосредственно внутри него.</span><span class="sxs-lookup"><span data-stu-id="2445d-124">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="2445d-125">Например, ячейка заголовка может поддерживать только один модуль типа **Модуль заголовка**, в то время как ячейка основного текста может поддерживать неограниченное число модулей любого типа (за исключением других модулей-контейнеров страниц).</span><span class="sxs-lookup"><span data-stu-id="2445d-125">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="2445d-126">В средствах разработки авторам страниц нет необходимости знать заранее, какие модули могут или не могут быть помещены в каждое гнездо.</span><span class="sxs-lookup"><span data-stu-id="2445d-126">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="2445d-127">Когда авторы страниц выбирают ячейку и попытаются выбрать модуль для добавления в него, они увидят отфильтрованное представление типов модулей, которые поддерживаются для этого слота.</span><span class="sxs-lookup"><span data-stu-id="2445d-127">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="2445d-128">Модули содержимого</span><span class="sxs-lookup"><span data-stu-id="2445d-128">Content modules</span></span>

<span data-ttu-id="2445d-129">Модули содержимого содержат содержимое и мультимедийные элементы, такие как текст (например, заголовки, параграфы и ссылки) или ссылки на ресурсы (например, изображения, видео и PDF).</span><span class="sxs-lookup"><span data-stu-id="2445d-129">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="2445d-130">Типы модулей содержимого обычно включают в себя блок содержимого, блок текста и модули рекламного баннера.</span><span class="sxs-lookup"><span data-stu-id="2445d-130">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="2445d-131">Модули этих трех типов могут содержать текст или мультимедиа, и они не требуют каких-либо дочерних модулей для отображения на странице.</span><span class="sxs-lookup"><span data-stu-id="2445d-131">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="2445d-132">Большая часть типичных повседневных действий по разработке страниц и контента включает модули содержимого, в основном потому что эти модули определяют реальное содержимое, отображаемое в их родительских контейнерных модулях.</span><span class="sxs-lookup"><span data-stu-id="2445d-132">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="2445d-133">Доступно множество модулей содержимого, и эти модули обычно являются последними элементами, которые будут добавлены в иерархию вложенных модулей страницы.</span><span class="sxs-lookup"><span data-stu-id="2445d-133">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="2445d-134">На следующем рисунке показано, как вложены модули в ячейках родительских контейнеров-модулей.</span><span class="sxs-lookup"><span data-stu-id="2445d-134">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Вложение модулей](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="2445d-136">Добавление или удаление модулей</span><span class="sxs-lookup"><span data-stu-id="2445d-136">Add or remove modules</span></span>

<span data-ttu-id="2445d-137">Следующие процедуры описывают добавление и удаление модулей.</span><span class="sxs-lookup"><span data-stu-id="2445d-137">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="2445d-138">Добавление модуля</span><span class="sxs-lookup"><span data-stu-id="2445d-138">Add a module</span></span>

<span data-ttu-id="2445d-139">Чтобы добавить модуль в гнездо или контейнер на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-139">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="2445d-140">В области структуры слева или непосредственном на основном холсте выберите контейнер или область, к которой можно добавить дочерний модуль.</span><span class="sxs-lookup"><span data-stu-id="2445d-140">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2445d-141">Конструктор модулей определяет список типов модулей, которые могут быть добавлены в конкретную ячейку модуля.</span><span class="sxs-lookup"><span data-stu-id="2445d-141">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="2445d-142">Авторы шаблонов могут затем уточнить разрешенные параметры модуля, чтобы обеспечить согласованность оптимизации поисковых систем (SEO) и эффективность разработки для всех страниц, построенных на основе определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="2445d-142">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="2445d-143">При добавлении модуля в ячейку диалоговое окно **Добавить модуль** автоматически фильтруется таким образом, чтобы отображались только модули, поддерживаемые в выбранном контейнере или ячейке.</span><span class="sxs-lookup"><span data-stu-id="2445d-143">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="2445d-144">Список разрешенных модулей определяется шаблоном страницы или определением модуля контейнера.</span><span class="sxs-lookup"><span data-stu-id="2445d-144">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="2445d-145">При использовании области структуры выберите многоточие (**...**) рядом с именем модуля, а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2445d-145">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="2445d-146">Если используются элементы управления непосредственно внутри холста, выберите символ "плюс" (**+**) в пустой ячейке или рядом с выбранным модулем, а затем выберите команду **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2445d-146">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2445d-147">Если контейнер или слот не поддерживают новые дочерние модули, параметр **Добавить модуль** будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="2445d-147">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="2445d-148">В диалоговом окне **Добавить модуль** найдите и выберите модуль, который требуется добавить на страницу.</span><span class="sxs-lookup"><span data-stu-id="2445d-148">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="2445d-149">**Блок содержимого** — это правильный тип модуля для начинающих.</span><span class="sxs-lookup"><span data-stu-id="2445d-149">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="2445d-150">Выберите **ОК**, чтобы добавить выбранный модуль в выбранный контейнер или ячейку на странице.</span><span class="sxs-lookup"><span data-stu-id="2445d-150">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="2445d-151">Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="2445d-151">Remove a module</span></span>

<span data-ttu-id="2445d-152">Чтобы удалить модуль из ячейки или контейнера на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-152">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="2445d-153">В области структуры в левой части выберите кнопку с многоточием (**...**) рядом с названием удаляемого модуля, затем нажмите символ корзины.</span><span class="sxs-lookup"><span data-stu-id="2445d-153">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="2445d-154">Кроме того, на главном холсте можно выбрать символ корзины на панели инструментов выбранного модуля.</span><span class="sxs-lookup"><span data-stu-id="2445d-154">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="2445d-155">При появлении запроса на подтверждение удаления модуля выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2445d-155">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="2445d-156">Перемещение модуля в новое место</span><span class="sxs-lookup"><span data-stu-id="2445d-156">Move a module to a new position</span></span>

<span data-ttu-id="2445d-157">Чтобы переместить модуль на новую позицию на странице, воспользуйтесь одним из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="2445d-157">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="2445d-158">Перемещение модуля с помощью панели структуры</span><span class="sxs-lookup"><span data-stu-id="2445d-158">Move a module using the outline pane</span></span>

<span data-ttu-id="2445d-159">Чтобы переместить модуль с помощью панели структуры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-159">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="2445d-160">Выберите и удерживайте модуль, который требуется переместить, в области структуры, а затем перетащите модуль на новое место в структуре.</span><span class="sxs-lookup"><span data-stu-id="2445d-160">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="2445d-161">Синяя линия в структуре и на холсте обозначает место, где можно разместить модуль.</span><span class="sxs-lookup"><span data-stu-id="2445d-161">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="2445d-162">Отпустите модуль, чтобы поставить его в новую позицию.</span><span class="sxs-lookup"><span data-stu-id="2445d-162">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="2445d-163">Перемещение модуля непосредственно внутри холста</span><span class="sxs-lookup"><span data-stu-id="2445d-163">Move a module directly within the canvas</span></span>

<span data-ttu-id="2445d-164">Чтобы переместить модуль непосредственно внутри холста, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-164">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="2445d-165">Выберите модуль, который необходимо переместить, в холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-165">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="2445d-166">Выберите символ стрелки вверх или вниз на панели инструментов модуля, а затем перетащите стрелку в новое положение на странице.</span><span class="sxs-lookup"><span data-stu-id="2445d-166">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="2445d-167">Синяя линия на холсте и в структуре обозначает место, где можно разместить модуль.</span><span class="sxs-lookup"><span data-stu-id="2445d-167">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="2445d-168">Если модуль нельзя переместить вверх или вниз, символ стрелки будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="2445d-168">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="2445d-169">Отпустите модуль, чтобы поставить его в новую позицию.</span><span class="sxs-lookup"><span data-stu-id="2445d-169">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="2445d-170">Перемещение модуля с помощью меню многоточия</span><span class="sxs-lookup"><span data-stu-id="2445d-170">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="2445d-171">Чтобы переместить модуль с помощью меню многоточия, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-171">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="2445d-172">Выберите модуль в структуре или холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-172">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="2445d-173">Нажмите кнопку с многоточием (**...**) рядом с именем модуля в области структуры или на панели инструментов модуля в холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-173">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="2445d-174">Если модуль можно переместить вверх или вниз внутри контейнера или ячейки, можно увидеть параметры **Вверх** или **Вниз**.</span><span class="sxs-lookup"><span data-stu-id="2445d-174">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="2445d-175">Выберите нужный параметр перемещения, чтобы переместить модуль вверх или вниз относительно его одноуровневых элементов.</span><span class="sxs-lookup"><span data-stu-id="2445d-175">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="2445d-176">Настройка модулей</span><span class="sxs-lookup"><span data-stu-id="2445d-176">Configure modules</span></span>

<span data-ttu-id="2445d-177">Следующие процедуры описывают, как настраивать модули содержимого и контейнеры.</span><span class="sxs-lookup"><span data-stu-id="2445d-177">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="2445d-178">Настройка модуля содержимого</span><span class="sxs-lookup"><span data-stu-id="2445d-178">Configure a content module</span></span>

<span data-ttu-id="2445d-179">Чтобы настроить модуль содержимого на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-179">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="2445d-180">В области структуры слева разверните дерево и выберите модуль содержимого (например, **Блок содержимого**).</span><span class="sxs-lookup"><span data-stu-id="2445d-180">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="2445d-181">Или же выберите модуль, который необходимо переместить, в основном холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-181">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="2445d-182">В области свойств модуля справа введите свойства для всех нужных элементов управления модуля.</span><span class="sxs-lookup"><span data-stu-id="2445d-182">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="2445d-183">На панели команд выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2445d-183">On the command bar, select **Save**.</span></span> <span data-ttu-id="2445d-184">Это также приведет к обновлению холста предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="2445d-184">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="2445d-185">Изменение свойства текста модуля</span><span class="sxs-lookup"><span data-stu-id="2445d-185">Edit module text properties</span></span>

<span data-ttu-id="2445d-186">Свойства текста модуля, которые недоступны только для чтения, могут быть отредактированы непосредственно на холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-186">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="2445d-187">Чтобы изменить свойства текста модуля, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-187">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="2445d-188">Выберите элемент управления "текст" в холсте и затем поместите курсор в то место, где необходимо отредактировать текст.</span><span class="sxs-lookup"><span data-stu-id="2445d-188">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="2445d-189">Введите свой текст.</span><span class="sxs-lookup"><span data-stu-id="2445d-189">Enter your text content.</span></span>
1. <span data-ttu-id="2445d-190">Чтобы продолжить редактирование другого содержимого, выберите любое место вне текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="2445d-190">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="2445d-191">Выбор встроенного изображения</span><span class="sxs-lookup"><span data-stu-id="2445d-191">Inline image selection</span></span>

<span data-ttu-id="2445d-192">Изображения модуля, которые недоступны только для чтения, могут быть изменены непосредственно на холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-192">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="2445d-193">Чтобы выбрать новое изображение для модуля содержимого, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-193">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="2445d-194">Дважды щелкните изображение на холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-194">In the canvas, double-click the image.</span></span> <span data-ttu-id="2445d-195">Появится окно выбора мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2445d-195">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="2445d-196">Найдите и выберите новое изображение, которое необходимо использовать, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2445d-196">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="2445d-197">Новое изображение будет отображено на холсте.</span><span class="sxs-lookup"><span data-stu-id="2445d-197">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="2445d-198">Настройка модуля контейнера</span><span class="sxs-lookup"><span data-stu-id="2445d-198">Configure a container module</span></span>

<span data-ttu-id="2445d-199">Чтобы настроить модуль контейнера на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2445d-199">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="2445d-200">Выберите контейнерный модуль на странице (например, модуль карусели или гибкого контейнера).</span><span class="sxs-lookup"><span data-stu-id="2445d-200">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="2445d-201">В области свойств справа разверните вложенные элементы управления, выбрав заголовки, и задайте необходимые значения элементов управления.</span><span class="sxs-lookup"><span data-stu-id="2445d-201">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="2445d-202">В области структуры в левой части выберите кнопку с многоточием рядом с названием контейнера или любых ячеек внутри контейнера, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2445d-202">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="2445d-203">Затем добавьте дочерние модули к выбранному контейнеру.</span><span class="sxs-lookup"><span data-stu-id="2445d-203">Then, add child modules to the selected container.</span></span> <span data-ttu-id="2445d-204">Дополнительные сведения см. в разделе [Работа с модулями](#add-a-module) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="2445d-204">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="2445d-205">Если в родительском контейнере есть несколько одноуровневых дочерних модулей, можно изменить порядок их просмотра в родительском контейнере.</span><span class="sxs-lookup"><span data-stu-id="2445d-205">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="2445d-206">Нажмите кнопку с многоточием для модуля, затем воспользуйтесь кнопками со стрелками вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="2445d-206">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2445d-207">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2445d-207">Additional resources</span></span>

[<span data-ttu-id="2445d-208">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="2445d-208">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2445d-209">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="2445d-209">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="2445d-210">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="2445d-210">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="2445d-211">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="2445d-211">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2445d-212">Добавление модуля-контейнера на страницу</span><span class="sxs-lookup"><span data-stu-id="2445d-212">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="2445d-213">Работа с группами публикаций</span><span class="sxs-lookup"><span data-stu-id="2445d-213">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
