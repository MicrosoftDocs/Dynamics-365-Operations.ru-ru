---
title: Работа с модулями
description: В этом разделе описывается, как и когда использовать модули в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025887"
---
# <a name="work-with-modules"></a><span data-ttu-id="6c125-103">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="6c125-103">Work with modules</span></span>

<span data-ttu-id="6c125-104">В этом разделе описывается, как и когда использовать модули в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c125-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="6c125-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="6c125-105">Overview</span></span>

<span data-ttu-id="6c125-106">Модули являются логическими строительными блоками, составляющими структуру страницы, и они имеют различные цели и области действия.</span><span class="sxs-lookup"><span data-stu-id="6c125-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="6c125-107">Некоторые модули являются контейнерами высокого уровня, и их единственная цель состоит в том, чтобы хранить и организовывать другие модули (дочерние модули).</span><span class="sxs-lookup"><span data-stu-id="6c125-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="6c125-108">Другие модули, такие как простой модуль размещения изображений, имеют очень конкретную цель.</span><span class="sxs-lookup"><span data-stu-id="6c125-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="6c125-109">Другие модули, например, модуль карусели, попадают где-то посередине между этими двумя категориями.</span><span class="sxs-lookup"><span data-stu-id="6c125-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="6c125-110">По умолчанию ваш сайт Dynamics 365 Commerce включает библиотеку начального комплекта модулей, которая позволяет использовать большинство основных сценариев электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="6c125-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="6c125-111">Вы должны быть способны создавать законченный сайт электронной коммерции только с помощью этих модулей.</span><span class="sxs-lookup"><span data-stu-id="6c125-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="6c125-112">Однако, возможно, вы захотите настроить эти модули или создать новые, пользовательские модули для конкретных нужд.</span><span class="sxs-lookup"><span data-stu-id="6c125-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="6c125-113">Если требуется создать пользовательские модули, предусмотрен пакет средств разработки дизайна модулей (SDK), который поможет в создании библиотеки пользовательских модулей.</span><span class="sxs-lookup"><span data-stu-id="6c125-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="6c125-114">Контейнерные модули и ячейки</span><span class="sxs-lookup"><span data-stu-id="6c125-114">Container modules and slots</span></span>

<span data-ttu-id="6c125-115">Как упоминалось ранее, некоторые модули предназначены для размещения дочерних модулей.</span><span class="sxs-lookup"><span data-stu-id="6c125-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="6c125-116">Эти модули называются *контейнерами* и позволяют использовать иерархии вложенных модулей.</span><span class="sxs-lookup"><span data-stu-id="6c125-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="6c125-117">Контейнерные модули содержат *ячейки*.</span><span class="sxs-lookup"><span data-stu-id="6c125-117">Container modules include *slots*.</span></span> <span data-ttu-id="6c125-118">Ячейки используются для обработки макета и назначения дочерних модулей в контейнере.</span><span class="sxs-lookup"><span data-stu-id="6c125-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="6c125-119">Примером является модуль-контейнер базовой страницы (модуль верхнего уровня для любой страницы), определяющий несколько важных ячеек:</span><span class="sxs-lookup"><span data-stu-id="6c125-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="6c125-120">Ячейка заголовка</span><span class="sxs-lookup"><span data-stu-id="6c125-120">A header slot</span></span>
- <span data-ttu-id="6c125-121">Ячейка основного текста</span><span class="sxs-lookup"><span data-stu-id="6c125-121">A body slot</span></span>
- <span data-ttu-id="6c125-122">Ячейка нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="6c125-122">A footer slot</span></span>

<span data-ttu-id="6c125-123">Разработчик модуля определяет эти ячейки и определяет, какие дочерние модули и в каком количестве могут быть размещены непосредственно внутри него.</span><span class="sxs-lookup"><span data-stu-id="6c125-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="6c125-124">Например, ячейка заголовка может поддерживать только один модуль типа **Модуль заголовка**, в то время как ячейка основного текста может поддерживать неограниченное число модулей любого типа (за исключением других модулей-контейнеров страниц).</span><span class="sxs-lookup"><span data-stu-id="6c125-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="6c125-125">В средствах разработки авторам страниц нет необходимости знать заранее, какие модули могут или не могут быть помещены в каждое гнездо.</span><span class="sxs-lookup"><span data-stu-id="6c125-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="6c125-126">Когда авторы страниц выбирают ячейку и попытаются выбрать модуль для добавления в него, они увидят отфильтрованное представление типов модулей, которые поддерживаются для этого слота.</span><span class="sxs-lookup"><span data-stu-id="6c125-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="6c125-127">Модули содержимого</span><span class="sxs-lookup"><span data-stu-id="6c125-127">Content modules</span></span>

<span data-ttu-id="6c125-128">Модули содержимого содержат содержимое и мультимедийные элементы, такие как текст (например, заголовки, параграфы и ссылки) или ссылки на ресурсы (например, изображения, видео и PDF).</span><span class="sxs-lookup"><span data-stu-id="6c125-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="6c125-129">Примерами типичных типов модулей содержимого являются **Главный имиджевый баннер**, **Компонент** и **Баннер**.</span><span class="sxs-lookup"><span data-stu-id="6c125-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="6c125-130">Модули этих трех типов могут содержать текст или мультимедиа, и они не требуют каких-либо дочерних модулей для отображения на странице.</span><span class="sxs-lookup"><span data-stu-id="6c125-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="6c125-131">Большая часть типичных повседневных действий по разработке страниц и контента включает модули содержимого, в основном потому что эти модули определяют реальное содержимое, отображаемое в их родительских контейнерных модулях.</span><span class="sxs-lookup"><span data-stu-id="6c125-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="6c125-132">Доступно множество модулей содержимого, и эти модули обычно являются последними элементами, которые будут добавлены в иерархию вложенных модулей страницы.</span><span class="sxs-lookup"><span data-stu-id="6c125-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="6c125-133">На следующем рисунке показано, как вложены модули в ячейках родительских контейнеров-модулей.</span><span class="sxs-lookup"><span data-stu-id="6c125-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Вложение модулей](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="6c125-135">Добавление или удаление модулей</span><span class="sxs-lookup"><span data-stu-id="6c125-135">Add or remove modules</span></span>

<span data-ttu-id="6c125-136">Следующие процедуры описывают добавление и удаление модулей.</span><span class="sxs-lookup"><span data-stu-id="6c125-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="6c125-137">Добавление модуля</span><span class="sxs-lookup"><span data-stu-id="6c125-137">Add a module</span></span>

<span data-ttu-id="6c125-138">Чтобы добавить модуль в гнездо или контейнер на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6c125-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="6c125-139">В области структуры слева выберите контейнер или ячейку, в которую можно добавить дочерний модуль.</span><span class="sxs-lookup"><span data-stu-id="6c125-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c125-140">Конструктор модулей определяет список типов модулей, которые могут быть добавлены в конкретную ячейку модуля.</span><span class="sxs-lookup"><span data-stu-id="6c125-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="6c125-141">Авторы шаблонов могут затем уточнить разрешенные параметры модуля, чтобы обеспечить согласованность оптимизации поисковых систем (SEO) и эффективность разработки для всех страниц, построенных на основе определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c125-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="6c125-142">Нажмите кнопку с многоточием (**...**) для модуля, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="6c125-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="6c125-143">Отобразится диалоговое окно **Добавление модуля**.</span><span class="sxs-lookup"><span data-stu-id="6c125-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="6c125-144">Это диалоговое окно автоматически фильтруется таким образом, чтобы отображались только модули, поддерживаемые в выбранном контейнере или гнезде.</span><span class="sxs-lookup"><span data-stu-id="6c125-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="6c125-145">Список модулей определяется шаблоном страницы или определением модуля контейнера.</span><span class="sxs-lookup"><span data-stu-id="6c125-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c125-146">Если контейнер или слот не поддерживают новые дочерние модули, параметр **Добавить модуль** будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="6c125-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="6c125-147">В диалоговом окне найдите и выберите модуль, который требуется добавить на страницу.</span><span class="sxs-lookup"><span data-stu-id="6c125-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="6c125-148">**Компонент** и **Главный имиджевый баннер** являются хорошими типами модулей для работы начинающих.</span><span class="sxs-lookup"><span data-stu-id="6c125-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="6c125-149">Выберите **ОК**, чтобы добавить выбранный модуль в выбранный контейнер или ячейку на странице.</span><span class="sxs-lookup"><span data-stu-id="6c125-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="6c125-150">Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="6c125-150">Remove a module</span></span>

<span data-ttu-id="6c125-151">Чтобы удалить модуль из ячейки или контейнера на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6c125-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="6c125-152">В области структуры в левой части выберите кнопку с многоточием рядом с названием удаляемого модуля, затем нажмите кнопку корзины.</span><span class="sxs-lookup"><span data-stu-id="6c125-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="6c125-153">При появлении запроса на подтверждение удаления модуля выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6c125-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="6c125-154">Настройка модулей</span><span class="sxs-lookup"><span data-stu-id="6c125-154">Configure modules</span></span>

<span data-ttu-id="6c125-155">Следующие процедуры описывают, как настраивать модули содержимого и контейнеры.</span><span class="sxs-lookup"><span data-stu-id="6c125-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="6c125-156">Настройка модуля содержимого</span><span class="sxs-lookup"><span data-stu-id="6c125-156">Configure a content module</span></span>

<span data-ttu-id="6c125-157">Чтобы настроить модуль содержимого на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6c125-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="6c125-158">В области структуры слева разверните дерево и выберите модуль содержимого (например, **Компонент**, **Главный имиджевый баннер** или **Баннер**).</span><span class="sxs-lookup"><span data-stu-id="6c125-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="6c125-159">В области свойств справа найдите элементы управления содержимым и параметрами модуля.</span><span class="sxs-lookup"><span data-stu-id="6c125-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="6c125-160">Введите свойства для всех нужных элементов управления модуля.</span><span class="sxs-lookup"><span data-stu-id="6c125-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="6c125-161">На панели команд выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="6c125-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="6c125-162">Это также приведет к обновлению холста предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="6c125-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="6c125-163">Настройка модуля контейнера</span><span class="sxs-lookup"><span data-stu-id="6c125-163">Configure a container module</span></span>

<span data-ttu-id="6c125-164">Чтобы настроить модуль контейнера на странице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6c125-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="6c125-165">Выберите контейнерный модуль на странице (например, модуль карусели или гибкого контейнера).</span><span class="sxs-lookup"><span data-stu-id="6c125-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="6c125-166">В области свойств справа разверните вложенные элементы управления, выбрав заголовки, и задайте необходимые значения элементов управления.</span><span class="sxs-lookup"><span data-stu-id="6c125-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="6c125-167">В области структуры в левой части выберите кнопку с многоточием рядом с названием контейнера или любых ячеек внутри контейнера, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="6c125-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="6c125-168">Затем добавьте дочерние модули к выбранному контейнеру.</span><span class="sxs-lookup"><span data-stu-id="6c125-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="6c125-169">Дополнительные сведения см. в разделе [Работа с модулями](#add-a-module) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="6c125-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="6c125-170">Если в родительском контейнере есть несколько одноуровневых дочерних модулей, можно изменить порядок их просмотра в родительском контейнере.</span><span class="sxs-lookup"><span data-stu-id="6c125-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="6c125-171">Нажмите кнопку с многоточием для модуля, затем воспользуйтесь кнопками со стрелками вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="6c125-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c125-172">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6c125-172">Additional resources</span></span>

[<span data-ttu-id="6c125-173">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="6c125-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="6c125-174">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="6c125-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="6c125-175">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="6c125-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="6c125-176">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="6c125-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="6c125-177">Добавление модуля-контейнера на страницу</span><span class="sxs-lookup"><span data-stu-id="6c125-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="6c125-178">Работа с группами публикаций</span><span class="sxs-lookup"><span data-stu-id="6c125-178">Work with publish groups</span></span>](publish-groups.md)

