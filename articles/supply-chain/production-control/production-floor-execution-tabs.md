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
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077586"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="44288-103">Разработка интерфейса выполнения производственного цеха</span><span class="sxs-lookup"><span data-stu-id="44288-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="44288-104">Можно разработать содержимое пользовательского интерфейса для каждой конфигурации, используемой интерфейсом выполнения производственного цеха.</span><span class="sxs-lookup"><span data-stu-id="44288-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="44288-105">Например, сотрудникам в одной из производственных ячеек может потребоваться иметь возможность открыть инструкции по заданию в производственном цехе, в то время как в другой производственной ячейке инструкции не требуются.</span><span class="sxs-lookup"><span data-stu-id="44288-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="44288-106">В этом случае необходимо создать две конфигурации, одну с кнопкой для открытия вложенных документов, и одну без этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="44288-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="44288-107">Разработка вкладки</span><span class="sxs-lookup"><span data-stu-id="44288-107">Design a tab</span></span>

<span data-ttu-id="44288-108">На странице **Настройка выполнения производственного цеха** можно создавать и настраивать вкладки, выбрав **Разработка вкладок** в области действий.</span><span class="sxs-lookup"><span data-stu-id="44288-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="44288-109">Каждая вкладка разделена на четыре раздела, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="44288-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="44288-110">![Макет вкладки](media/pfe-tab-layout.png "Макет вкладки")</span><span class="sxs-lookup"><span data-stu-id="44288-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="44288-111">На рисунке показаны следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="44288-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="44288-112">Основная панель инструментов</span><span class="sxs-lookup"><span data-stu-id="44288-112">Primary toolbar</span></span>
1. <span data-ttu-id="44288-113">Дополнительная панель инструментов</span><span class="sxs-lookup"><span data-stu-id="44288-113">Secondary toolbar</span></span>
1. <span data-ttu-id="44288-114">Основное представление</span><span class="sxs-lookup"><span data-stu-id="44288-114">Main view</span></span>
1. <span data-ttu-id="44288-115">Подробное представление</span><span class="sxs-lookup"><span data-stu-id="44288-115">Detailed view</span></span>

<span data-ttu-id="44288-116">Чтобы создать и настроить новую вкладку, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="44288-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="44288-117">Перейдите в раздел **Управление производством &gt; Настройка &gt; Управление производством**.</span><span class="sxs-lookup"><span data-stu-id="44288-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="44288-118">Выберите **Разработка вкладок** на панели операций, чтобы открыть страницу **Разработка вкладок**.</span><span class="sxs-lookup"><span data-stu-id="44288-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="44288-119">![Страница разработки вкладок](media/pfe-design-tabs.png "Страница разработки вкладок")</span><span class="sxs-lookup"><span data-stu-id="44288-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="44288-120">На панели операций выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44288-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="44288-121">В заголовке страницы выполните следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="44288-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="44288-122">**Имя вкладки** — укажите имя вкладки.</span><span class="sxs-lookup"><span data-stu-id="44288-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="44288-123">**Главное представление** — выберите один из двух предварительно определенных списков заданий (*Активные задания*, *Все задания* или *Мое оборудование*).</span><span class="sxs-lookup"><span data-stu-id="44288-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="44288-124">**Представление сведений** — выберите пустое значение или **Сведения о задании**.</span><span class="sxs-lookup"><span data-stu-id="44288-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="44288-125">При выборе пустого значения на вкладке не будет представления сведений. Если выбрать **Сведения о задании**, подробное представление будет содержать подробное описание задания, выбранного в списке заданий в главном представлении.</span><span class="sxs-lookup"><span data-stu-id="44288-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="44288-126">В разделе **Основная панель инструментов** выберите кнопки, которые должны быть доступны на основной панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="44288-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="44288-127">В столбце **Доступные действия** отображается список всех кнопок, которые могут быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="44288-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="44288-128">В столбцах **Выбранные действия** отображается список всех кнопок, включенных в текущую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="44288-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="44288-129">С помощью кнопок между столбцами переместите выбранные элементы между столбцами, как требуется.</span><span class="sxs-lookup"><span data-stu-id="44288-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="44288-130">Используйте кнопки вверх и вниз рядом со столбцом **Выбранные действия** для управления порядком, в котором кнопки представлены в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="44288-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="44288-131">В разделе **Дополнительная** **панель инструментов** выберите кнопки, которые должны быть доступны на дополнительной панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="44288-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="44288-132">В столбце **Доступные действия** отображается список всех кнопок, которые могут быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="44288-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="44288-133">В столбцах **Выбранные действия** отображается список всех кнопок, включенных в текущую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="44288-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="44288-134">С помощью кнопок между столбцами переместите выбранные элементы между столбцами, как требуется.</span><span class="sxs-lookup"><span data-stu-id="44288-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="44288-135">Используйте кнопки вверх и вниз рядом со столбцом **Выбранные действия** для управления порядком, в котором кнопки представлены в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="44288-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="44288-136">Связь вкладки с конфигурацией</span><span class="sxs-lookup"><span data-stu-id="44288-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="44288-137">После разработки всех нужных вкладок можно связать их с конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="44288-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="44288-138">Перейдите в раздел **Управление производством &gt; Настройка &gt; Настройка выполнения производственного цеха**.</span><span class="sxs-lookup"><span data-stu-id="44288-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="44288-139">![Настроить управление производственным участком](media/pfe-config-prod-floor-execution.png "Настроить управление производственным участком")</span><span class="sxs-lookup"><span data-stu-id="44288-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="44288-140">На экспресс-вкладке **Выбор вкладки** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="44288-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="44288-141">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="44288-141">A new row is added to the grid.</span></span> <span data-ttu-id="44288-142">Для этой новой строки выберите имя вкладки, которую необходимо добавить в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="44288-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="44288-143">При необходимости продолжайте добавлять дополнительные вкладки.</span><span class="sxs-lookup"><span data-stu-id="44288-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="44288-144">Используйте кнопки **Вверх** и **Вниз** на панели инструментов, чтобы упорядочить вкладки нужным образом.</span><span class="sxs-lookup"><span data-stu-id="44288-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="44288-145">Вкладки будут отображаться слева направо в порядке, показанном на приведенном выше снимке экрана (вкладка сверху отображается слева).</span><span class="sxs-lookup"><span data-stu-id="44288-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
