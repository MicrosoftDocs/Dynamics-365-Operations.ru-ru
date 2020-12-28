---
title: Назначение списков задач магазинам или сотрудникам
description: В этом разделе описывается, как назначить списки задач магазинам или сотрудникам в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415304"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="67494-103">Назначение списков задач магазинам или сотрудникам</span><span class="sxs-lookup"><span data-stu-id="67494-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67494-104">В этом разделе описывается, как назначить списки задач магазинам или сотрудникам в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="67494-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="67494-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="67494-105">Overview</span></span>

<span data-ttu-id="67494-106">Управление задачами в Dynamics 365 Commerce позволяет назначить список задач нескольким магазинам или сотрудникам, либо комбинации магазинов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="67494-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="67494-107">Например, региональный менеджер для 20 магазинов может пожелать назначить список задач **Подготовка к сезону отпусков** всем 20 магазинам.</span><span class="sxs-lookup"><span data-stu-id="67494-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="67494-108">Запуск процесса назначения списка задач</span><span class="sxs-lookup"><span data-stu-id="67494-108">Start the task list assignment process</span></span>

<span data-ttu-id="67494-109">Чтобы запустить процесс назначения списка задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="67494-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="67494-110">Перейдите в **Retail и Commerce \> Управление задачами \> Администрирование управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="67494-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="67494-111">Выберите список задач для назначения.</span><span class="sxs-lookup"><span data-stu-id="67494-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="67494-112">Выберите **Запустить процесс**.</span><span class="sxs-lookup"><span data-stu-id="67494-112">Select **Start process**.</span></span>
1. <span data-ttu-id="67494-113">В диалоговом окне **запуск процесса** на вкладке **общие сведения** в поле **имя процесса** введите имя (например, **магазины для восточно-региона**).</span><span class="sxs-lookup"><span data-stu-id="67494-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="67494-114">В поле **Целевая дата** укажите дату.</span><span class="sxs-lookup"><span data-stu-id="67494-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="67494-115">Чтобы назначить список задач магазинам, на вкладке **магазины** используйте фильтр **Организационная иерархия** для поиска и выбора магазинов.</span><span class="sxs-lookup"><span data-stu-id="67494-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="67494-116">Чтобы назначить список задач сотрудникам, на вкладке **Работники** найдите и выберите сотрудников.</span><span class="sxs-lookup"><span data-stu-id="67494-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="67494-117">Выберите **ОК**, чтобы начать процесс.</span><span class="sxs-lookup"><span data-stu-id="67494-117">Select **OK** to start the process.</span></span> <span data-ttu-id="67494-118">Список задач назначается выбранным магазинам или сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="67494-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="67494-119">На следующем рисунке показан пример поиска и выбора магазинов в диалоговом окне **Запустить процесс**.</span><span class="sxs-lookup"><span data-stu-id="67494-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Поиск и выбор магазинов в диалоговом окне "Запуск процесса"](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="67494-121">Назначение списков задач на регулярной основе</span><span class="sxs-lookup"><span data-stu-id="67494-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="67494-122">У продавца бывают повторяющиеся задачи, например "Контрольный список для закрытия в четверг" или "Первое число месяца".</span><span class="sxs-lookup"><span data-stu-id="67494-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="67494-123">Таким образом, им, возможно, потребуется назначить список задач на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="67494-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="67494-124">Перейдите в **Retail и Commerce \> Управление задачами \> Администрирование управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="67494-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="67494-125">Выберите список задач для назначения.</span><span class="sxs-lookup"><span data-stu-id="67494-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="67494-126">Выберите **Запустить процесс**.</span><span class="sxs-lookup"><span data-stu-id="67494-126">Select **Start process**.</span></span>
1. <span data-ttu-id="67494-127">В диалоговом окне **запуск процесса** на вкладке **общие сведения** в поле **имя процесса** введите имя.</span><span class="sxs-lookup"><span data-stu-id="67494-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="67494-128">Для параметра **Повторение** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="67494-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="67494-129">В поле **Смещение целевой даты повторения в днях** введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="67494-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="67494-130">Например, если ввести **4**, то в качестве конечной даты будет выбрана дата повторения плюс четыре дня.</span><span class="sxs-lookup"><span data-stu-id="67494-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="67494-131">На вкладке **Выполнять в фоновом режиме** выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="67494-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="67494-132">В диалоговом окне **Определение повторения** введите критерий частоты и затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="67494-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="67494-133">На следующем рисунке показан пример ввода критерия частоты в диалоговом окне **определение повторения**.</span><span class="sxs-lookup"><span data-stu-id="67494-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Ввод критериев частоты в диалоговом окне «Определение повторения»](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="67494-135">Отслеживание статуса списка задач</span><span class="sxs-lookup"><span data-stu-id="67494-135">Track task list status</span></span>

<span data-ttu-id="67494-136">Если вы являетесь региональным менеджером или менеджером магазина, вам может потребоваться отслеживать статус списков задач, назначенных нескольким магазинам или сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="67494-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="67494-137">Можно проследить магазины или работников, которые не выполнили свои назначенные задачи вовремя.</span><span class="sxs-lookup"><span data-stu-id="67494-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="67494-138">Бэк-офис Commerce позволяет просматривать статус списков задач, переназначить задачи или изменять статус задачи.</span><span class="sxs-lookup"><span data-stu-id="67494-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="67494-139">Чтобы отследить статус списка задач для всех задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="67494-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="67494-140">Перейдите в **Retail и Commerce \> Управление задачами \> Процессы управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="67494-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="67494-141">Перейдите на вкладку **Все списки задач**, чтобы просмотреть статус всех списков задач, назначенных различным магазинам.</span><span class="sxs-lookup"><span data-stu-id="67494-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="67494-142">Чтобы отследить статус списка задач для всех назначенных вам задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="67494-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="67494-143">Перейдите в **Retail и Commerce \> Управление задачами \> Процессы управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="67494-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="67494-144">Выберите вкладку **мои задачи** или **все задачи**, чтобы просмотреть или изменить статус назначенных вам задач.</span><span class="sxs-lookup"><span data-stu-id="67494-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67494-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67494-145">Additional resources</span></span>

[<span data-ttu-id="67494-146">Обзор управления задачами</span><span class="sxs-lookup"><span data-stu-id="67494-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="67494-147">Настройка управления задачами</span><span class="sxs-lookup"><span data-stu-id="67494-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="67494-148">Создание списков задач и добавление задач</span><span class="sxs-lookup"><span data-stu-id="67494-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="67494-149">Управление задачами в POS</span><span class="sxs-lookup"><span data-stu-id="67494-149">Task management in POS</span></span>](task-mgmt-POS.md)
