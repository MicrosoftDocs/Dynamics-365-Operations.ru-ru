---
title: Разработка интерфейса выполнения производственного цеха
description: В этом разделе описывается разработка содержимого пользовательского интерфейса для каждой конфигурации.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664280"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="9e7ca-103">Разработка интерфейса выполнения производственного цеха</span><span class="sxs-lookup"><span data-stu-id="9e7ca-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9e7ca-104">Можно разработать содержимое пользовательского интерфейса для каждой конфигурации, используемой интерфейсом выполнения производственного цеха.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="9e7ca-105">Например, сотрудникам в одной из производственных ячеек может потребоваться иметь возможность открыть инструкции по заданию в производственном цехе, в то время как в другой производственной ячейке инструкции не требуются.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="9e7ca-106">В этом случае необходимо создать две конфигурации, одну с кнопкой для открытия вложенных документов, и одну без этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="9e7ca-107">Разработка вкладки</span><span class="sxs-lookup"><span data-stu-id="9e7ca-107">Design a tab</span></span>

<span data-ttu-id="9e7ca-108">На странице **Настройка выполнения производственного цеха** можно создавать и настраивать вкладки, выбрав **Разработка вкладок** в области действий.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="9e7ca-109">Каждая вкладка разделена на четыре раздела, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="9e7ca-110">![Макет вкладки](media/pfe-tab-layout.png "Макет вкладки")</span><span class="sxs-lookup"><span data-stu-id="9e7ca-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="9e7ca-111">На рисунке показаны следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="9e7ca-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="9e7ca-112">Основная панель инструментов</span><span class="sxs-lookup"><span data-stu-id="9e7ca-112">Primary toolbar</span></span>
1. <span data-ttu-id="9e7ca-113">Дополнительная панель инструментов</span><span class="sxs-lookup"><span data-stu-id="9e7ca-113">Secondary toolbar</span></span>
1. <span data-ttu-id="9e7ca-114">Основное представление</span><span class="sxs-lookup"><span data-stu-id="9e7ca-114">Main view</span></span>
1. <span data-ttu-id="9e7ca-115">Подробное представление</span><span class="sxs-lookup"><span data-stu-id="9e7ca-115">Detailed view</span></span>

<span data-ttu-id="9e7ca-116">Чтобы создать и настроить новую вкладку, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="9e7ca-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="9e7ca-117">Перейдите в раздел **Управление производством &gt; Настройка &gt; Управление производством**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="9e7ca-118">Выберите **Разработка вкладок** на панели операций, чтобы открыть страницу **Разработка вкладок**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="9e7ca-119">![Страница разработки вкладок](media/pfe-design-tabs.png "Страница разработки вкладок")</span><span class="sxs-lookup"><span data-stu-id="9e7ca-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="9e7ca-120">На панели операций выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="9e7ca-121">В заголовке страницы выполните следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="9e7ca-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="9e7ca-122">**Имя вкладки** — укажите имя вкладки.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="9e7ca-123">**Главное представление** — выберите один из двух предварительно определенных списков заданий (*Активные задания* или *Все задания*).</span><span class="sxs-lookup"><span data-stu-id="9e7ca-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="9e7ca-124">**Представление сведений** — выберите пустое значение или **Сведения о задании**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="9e7ca-125">При выборе пустого значения на вкладке не будет представления сведений. Если выбрать **Сведения о задании**, подробное представление будет содержать подробное описание задания, выбранного в списке заданий в главном представлении.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="9e7ca-126">В разделе **Основная панель инструментов** выберите кнопки, которые должны быть доступны на основной панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="9e7ca-127">В столбце **Доступные действия** отображается список всех кнопок, которые могут быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="9e7ca-128">В столбцах **Выбранные действия** отображается список всех кнопок, включенных в текущую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="9e7ca-129">С помощью кнопок между столбцами переместите выбранные элементы между столбцами, как требуется.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="9e7ca-130">Используйте кнопки вверх и вниз рядом со столбцом **Выбранные действия** для управления порядком, в котором кнопки представлены в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="9e7ca-131">В разделе **Дополнительная** **панель инструментов** выберите кнопки, которые должны быть доступны на дополнительной панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="9e7ca-132">В столбце **Доступные действия** отображается список всех кнопок, которые могут быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="9e7ca-133">В столбцах **Выбранные действия** отображается список всех кнопок, включенных в текущую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="9e7ca-134">С помощью кнопок между столбцами переместите выбранные элементы между столбцами, как требуется.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="9e7ca-135">Используйте кнопки вверх и вниз рядом со столбцом **Выбранные действия** для управления порядком, в котором кнопки представлены в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="9e7ca-136">Связь вкладки с конфигурацией</span><span class="sxs-lookup"><span data-stu-id="9e7ca-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="9e7ca-137">После разработки всех нужных вкладок можно связать их с конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="9e7ca-138">Перейдите в раздел **Управление производством &gt; Настройка &gt; Настройка выполнения производственного цеха**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="9e7ca-139">![Настроить управление производственным участком](media/pfe-config-prod-floor-execution.png "Настроить управление производственным участком")</span><span class="sxs-lookup"><span data-stu-id="9e7ca-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="9e7ca-140">На экспресс-вкладке **Выбор вкладки** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="9e7ca-141">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-141">A new row is added to the grid.</span></span> <span data-ttu-id="9e7ca-142">Для этой новой строки выберите имя вкладки, которую необходимо добавить в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="9e7ca-143">При необходимости продолжайте добавлять дополнительные вкладки.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="9e7ca-144">Используйте кнопки **Вверх** и **Вниз** на панели инструментов, чтобы упорядочить вкладки нужным образом.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="9e7ca-145">Вкладки будут отображаться слева направо в порядке, показанном на приведенном выше снимке экрана (вкладка сверху отображается слева).</span><span class="sxs-lookup"><span data-stu-id="9e7ca-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>