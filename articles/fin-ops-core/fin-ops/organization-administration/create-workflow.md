---
title: Обзор создания бизнес-правил
description: В этом разделе объясняется, как создать workflow-процесс.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 2168b33c8495eab61ec0c8262b042cd16420031c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190105"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="2f000-103">Обзор создания бизнес-правил</span><span class="sxs-lookup"><span data-stu-id="2f000-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f000-104">В этом разделе объясняется, как создать workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="2f000-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="2f000-105">Откройте редактор workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2f000-105">Open the workflow editor</span></span>

<span data-ttu-id="2f000-106">Модуль, в котором вы работаете, определяет типы рабочего процесса, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="2f000-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="2f000-107">Выполните следующие действия, чтобы выбрать тип workflow-процесса для создания и открытия редактора workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="2f000-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="2f000-108">Откройте модуль, для которой требуется создать новый workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="2f000-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="2f000-109">Например, чтобы создать workflow-процесс для заявок на покупку, нажмите кнопку **Закупки и источники**.</span><span class="sxs-lookup"><span data-stu-id="2f000-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="2f000-110">Щелкните **Настройка** &gt; **Workflow-процессы \[имя модуля\]**.</span><span class="sxs-lookup"><span data-stu-id="2f000-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="2f000-111">На открывшейся странице списка в области операций щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2f000-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="2f000-112">На странице **Создать workflow-процесс** выберите тип создаваемого workflow-процесса, затем нажмите **Создать workflow-процесс**.</span><span class="sxs-lookup"><span data-stu-id="2f000-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="2f000-113">Открывается редактор workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="2f000-113">The workflow editor appears.</span></span> <span data-ttu-id="2f000-114">Теперь можно использовать следующие процедуры для разработки workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="2f000-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="2f000-115">Перетащите элементы workflow-процесса на холст</span><span class="sxs-lookup"><span data-stu-id="2f000-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="2f000-116">Зона **Элементы workflow-процесса** редактора workflow-процесса содержит элементы, которые могут быть добавлены к вашему workflow-процессу.</span><span class="sxs-lookup"><span data-stu-id="2f000-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="2f000-117">Чтобы добавить элементы в workflow-процесс, перетащите их на холст.</span><span class="sxs-lookup"><span data-stu-id="2f000-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="2f000-118">Подключите элементы</span><span class="sxs-lookup"><span data-stu-id="2f000-118">Connect the elements</span></span>

<span data-ttu-id="2f000-119">Для того, чтобы подключить один элемент workflow-процесса к другому, наведите курсор на элемент, пока не появятся точки подключения.</span><span class="sxs-lookup"><span data-stu-id="2f000-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="2f000-120">Щелкните точку подключения и перетащите ее к другому элементу.</span><span class="sxs-lookup"><span data-stu-id="2f000-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="2f000-121">Не забудьте подключить все элементы.</span><span class="sxs-lookup"><span data-stu-id="2f000-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="2f000-122">Настроить свойства workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2f000-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="2f000-123">Следуйте этим действиям для настройки свойств для workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="2f000-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="2f000-124">Щелкните холст, чтобы убедиться в том, что ни один элемент workflow-процесс не выбран.</span><span class="sxs-lookup"><span data-stu-id="2f000-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="2f000-125">Щелкните **Свойства**, чтобы открыть страницу **Свойства** для workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="2f000-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="2f000-126">Следуйте процедурам из раздела [Настроить свойства workflow-процесса](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2f000-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="2f000-127">Настроить элементы документооборота</span><span class="sxs-lookup"><span data-stu-id="2f000-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="2f000-128">Настройте каждый элемент, который вы перетащили на холст.</span><span class="sxs-lookup"><span data-stu-id="2f000-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="2f000-129">Сведения о конфигурировании каждого элемента workflow-процесса см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2f000-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="2f000-130">Настройка задачи вручную</span><span class="sxs-lookup"><span data-stu-id="2f000-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="2f000-131">Настройка автоматизированной задачи</span><span class="sxs-lookup"><span data-stu-id="2f000-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="2f000-132">Настройка процесса утверждения</span><span class="sxs-lookup"><span data-stu-id="2f000-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="2f000-133">Настройка шага утверждения</span><span class="sxs-lookup"><span data-stu-id="2f000-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="2f000-134">Настройка решения, принимаемого вручную</span><span class="sxs-lookup"><span data-stu-id="2f000-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="2f000-135">Настройка решения, принимаемого по условию</span><span class="sxs-lookup"><span data-stu-id="2f000-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="2f000-136">Настройка параллельного мероприятия</span><span class="sxs-lookup"><span data-stu-id="2f000-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="2f000-137">Настройка параллельной ветви</span><span class="sxs-lookup"><span data-stu-id="2f000-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="2f000-138">Настройка документооборота элемента строки</span><span class="sxs-lookup"><span data-stu-id="2f000-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="2f000-139">Разрешение любых ошибок или предупреждений</span><span class="sxs-lookup"><span data-stu-id="2f000-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="2f000-140">Область **Ошибки/предупреждения** в нижней части редактора workflow-процессов отображает сообщения, созданные для workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="2f000-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="2f000-141">Чтобы найти элемент, в котором появилась ошибка или предупреждение, дважды щелкните ошибка или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="2f000-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="2f000-142">Необходимо разрешить все ошибки и предупреждения, прежде чем можно будет активировать workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="2f000-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="2f000-143">Сохранить и активировать workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="2f000-143">Save and activate the workflow</span></span>

<span data-ttu-id="2f000-144">Когда вы готовы сохранить и активировать workflow-процесс, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2f000-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="2f000-145">Щелкните **Сохранить и закрыть**, чтобы закрыть редактор workflow-процессов и открыть страницу **Сохранение workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="2f000-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="2f000-146">Введите комментарии об изменениях, внесенных в workflow-процесс, затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2f000-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="2f000-147">Если все ошибки и предупреждения были устранены, открывается страница **Активировать workflow-процесс**.</span><span class="sxs-lookup"><span data-stu-id="2f000-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="2f000-148">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2f000-148">Select one of the following options:</span></span>

    - <span data-ttu-id="2f000-149">Чтобы активировать эту версию workflow-процесса, нажмите **Активировать новую версию**.</span><span class="sxs-lookup"><span data-stu-id="2f000-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="2f000-150">Когда workflow-процесс станет активным, пользователи смогут представлять документы на обработку.</span><span class="sxs-lookup"><span data-stu-id="2f000-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="2f000-151">Если вы не хотите активировать данную версию, нажмите **Не активировать новую версию**.</span><span class="sxs-lookup"><span data-stu-id="2f000-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="2f000-152">workflow-процесс можно активировать позднее.</span><span class="sxs-lookup"><span data-stu-id="2f000-152">You can activate the workflow later.</span></span>
