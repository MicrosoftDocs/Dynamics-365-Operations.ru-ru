---
title: Назначение списков задач магазинам или сотрудникам
description: В этом разделе описывается, как назначить списки задач магазинам или сотрудникам в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795269"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="cb13b-103">Назначение списков задач магазинам или сотрудникам</span><span class="sxs-lookup"><span data-stu-id="cb13b-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb13b-104">В этом разделе описывается, как назначить списки задач магазинам или сотрудникам в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb13b-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cb13b-105">Управление задачами в Dynamics 365 Commerce позволяет назначить список задач нескольким магазинам или сотрудникам, либо комбинации магазинов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="cb13b-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="cb13b-106">Например, региональный менеджер для 20 магазинов может пожелать назначить список задач **Подготовка к сезону отпусков** всем 20 магазинам.</span><span class="sxs-lookup"><span data-stu-id="cb13b-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="cb13b-107">Запуск процесса назначения списка задач</span><span class="sxs-lookup"><span data-stu-id="cb13b-107">Start the task list assignment process</span></span>

<span data-ttu-id="cb13b-108">Чтобы запустить процесс назначения списка задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cb13b-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="cb13b-109">Перейдите в **Retail и Commerce \> Управление задачами \> Администрирование управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="cb13b-110">Выберите список задач для назначения.</span><span class="sxs-lookup"><span data-stu-id="cb13b-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="cb13b-111">Выберите **Запустить процесс**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-111">Select **Start process**.</span></span>
1. <span data-ttu-id="cb13b-112">В диалоговом окне **запуск процесса** на вкладке **общие сведения** в поле **имя процесса** введите имя (например, **магазины для восточно-региона**).</span><span class="sxs-lookup"><span data-stu-id="cb13b-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="cb13b-113">В поле **Целевая дата** укажите дату.</span><span class="sxs-lookup"><span data-stu-id="cb13b-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="cb13b-114">Чтобы назначить список задач магазинам, на вкладке **магазины** используйте фильтр **Организационная иерархия** для поиска и выбора магазинов.</span><span class="sxs-lookup"><span data-stu-id="cb13b-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="cb13b-115">Чтобы назначить список задач сотрудникам, на вкладке **Работники** найдите и выберите сотрудников.</span><span class="sxs-lookup"><span data-stu-id="cb13b-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="cb13b-116">Выберите **ОК**, чтобы начать процесс.</span><span class="sxs-lookup"><span data-stu-id="cb13b-116">Select **OK** to start the process.</span></span> <span data-ttu-id="cb13b-117">Список задач назначается выбранным магазинам или сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="cb13b-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="cb13b-118">На следующем рисунке показан пример поиска и выбора магазинов в диалоговом окне **Запустить процесс**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Поиск и выбор магазинов в диалоговом окне "Запуск процесса"](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="cb13b-120">Назначение списков задач на регулярной основе</span><span class="sxs-lookup"><span data-stu-id="cb13b-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="cb13b-121">У продавца бывают повторяющиеся задачи, например "Контрольный список для закрытия в четверг" или "Первое число месяца".</span><span class="sxs-lookup"><span data-stu-id="cb13b-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="cb13b-122">Таким образом, им, возможно, потребуется назначить список задач на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="cb13b-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="cb13b-123">Перейдите в **Retail и Commerce \> Управление задачами \> Администрирование управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="cb13b-124">Выберите список задач для назначения.</span><span class="sxs-lookup"><span data-stu-id="cb13b-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="cb13b-125">Выберите **Запустить процесс**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-125">Select **Start process**.</span></span>
1. <span data-ttu-id="cb13b-126">В диалоговом окне **запуск процесса** на вкладке **общие сведения** в поле **имя процесса** введите имя.</span><span class="sxs-lookup"><span data-stu-id="cb13b-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="cb13b-127">Для параметра **Повторение** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="cb13b-128">В поле **Смещение целевой даты повторения в днях** введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="cb13b-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="cb13b-129">Например, если ввести **4**, то в качестве конечной даты будет выбрана дата повторения плюс четыре дня.</span><span class="sxs-lookup"><span data-stu-id="cb13b-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="cb13b-130">На вкладке **Выполнять в фоновом режиме** выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="cb13b-131">В диалоговом окне **Определение повторения** введите критерий частоты и затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="cb13b-132">На следующем рисунке показан пример ввода критерия частоты в диалоговом окне **определение повторения**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Ввод критериев частоты в диалоговом окне «Определение повторения»](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="cb13b-134">Отслеживание статуса списка задач</span><span class="sxs-lookup"><span data-stu-id="cb13b-134">Track task list status</span></span>

<span data-ttu-id="cb13b-135">Если вы являетесь региональным менеджером или менеджером магазина, вам может потребоваться отслеживать статус списков задач, назначенных нескольким магазинам или сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="cb13b-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="cb13b-136">Можно проследить магазины или работников, которые не выполнили свои назначенные задачи вовремя.</span><span class="sxs-lookup"><span data-stu-id="cb13b-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="cb13b-137">Бэк-офис Commerce позволяет просматривать статус списков задач, переназначить задачи или изменять статус задачи.</span><span class="sxs-lookup"><span data-stu-id="cb13b-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="cb13b-138">Чтобы отследить статус списка задач для всех задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cb13b-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="cb13b-139">Перейдите в **Retail и Commerce \> Управление задачами \> Процессы управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="cb13b-140">Перейдите на вкладку **Все списки задач**, чтобы просмотреть статус всех списков задач, назначенных различным магазинам.</span><span class="sxs-lookup"><span data-stu-id="cb13b-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="cb13b-141">Чтобы отследить статус списка задач для всех назначенных вам задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cb13b-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="cb13b-142">Перейдите в **Retail и Commerce \> Управление задачами \> Процессы управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="cb13b-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="cb13b-143">Выберите вкладку **мои задачи** или **все задачи**, чтобы просмотреть или изменить статус назначенных вам задач.</span><span class="sxs-lookup"><span data-stu-id="cb13b-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb13b-144">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cb13b-144">Additional resources</span></span>

[<span data-ttu-id="cb13b-145">Обзор управления задачами</span><span class="sxs-lookup"><span data-stu-id="cb13b-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="cb13b-146">Настройка управления задачами</span><span class="sxs-lookup"><span data-stu-id="cb13b-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="cb13b-147">Создание списков задач и добавление задач</span><span class="sxs-lookup"><span data-stu-id="cb13b-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="cb13b-148">Управление задачами в POS</span><span class="sxs-lookup"><span data-stu-id="cb13b-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
