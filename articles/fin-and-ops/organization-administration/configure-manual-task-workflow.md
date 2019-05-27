---
title: Настройка ручных задач в workflow-процессе
description: В этом разделе описывается, как настроить свойства ручной задачи.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 669fce3ddade4d6e0a130da2420ab33ca4ff4671
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555230"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="2d9b0-103">Настройка ручных задач в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2d9b0-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d9b0-104">В этом разделе описывается, как настроить свойства ручной задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="2d9b0-105">Чтобы настроить ручную задачу, в редакторе workflow-процессов щелкните правой кнопкой мыши задачу и выберите **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2d9b0-106">Затем используйте следующие процедуры, чтобы настроить свойства для ручной задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="2d9b0-107">Задание имени задачи</span><span class="sxs-lookup"><span data-stu-id="2d9b0-107">Name the task</span></span>

<span data-ttu-id="2d9b0-108">Чтобы ввести имя ручной задачи, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="2d9b0-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2d9b0-110">В поле **Имя** введите уникальное имя задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2d9b0-111">Ввод строки темы и инструкций</span><span class="sxs-lookup"><span data-stu-id="2d9b0-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="2d9b0-112">Пользователям, назначенным этой задаче, должны быть предоставлены строка темы и инструкции.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="2d9b0-113">Например, при настройке задачи для заявок на закупку пользователь, который назначается задаче, увидит строку темы и инструкции на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2d9b0-114">Строка темы будет отображаться в строке сообщений на странице.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2d9b0-115">Пользователь может щелкнуть значок в строке сообщений, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="2d9b0-116">Чтобы ввести строку темы и инструкции, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="2d9b0-117">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2d9b0-118">В поле **Тема рабочего элемента** введите строку темы.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="2d9b0-119">Для того, чтобы персонализовать строку уведомления можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2d9b0-120">Заполнители заменяются соответствующей информацией, когда строка темы отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2d9b0-121">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2d9b0-122">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2d9b0-123">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2d9b0-124">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2d9b0-125">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-125">Click **Insert**.</span></span>

4. <span data-ttu-id="2d9b0-126">Для добавления переводов строки темы выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="2d9b0-127">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="2d9b0-128">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2d9b0-129">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2d9b0-130">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2d9b0-131">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="2d9b0-132">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-132">Click **Close**.</span></span>

5. <span data-ttu-id="2d9b0-133">В поле **Инструкции рабочего элемента** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="2d9b0-134">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2d9b0-135">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2d9b0-136">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2d9b0-137">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2d9b0-138">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2d9b0-139">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2d9b0-140">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-140">Click **Insert**.</span></span>

7. <span data-ttu-id="2d9b0-141">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2d9b0-142">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="2d9b0-143">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2d9b0-144">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2d9b0-145">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2d9b0-146">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 6.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="2d9b0-147">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="2d9b0-148">Назначение задачи</span><span class="sxs-lookup"><span data-stu-id="2d9b0-148">Assign the task</span></span>

<span data-ttu-id="2d9b0-149">Чтобы указать, кому требуется назначить ручную задачу, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="2d9b0-150">В левой области щелкните **Назначение**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="2d9b0-151">Во вкладке **Тип назначения** выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 3.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2d9b0-152">Параметр</span><span class="sxs-lookup"><span data-stu-id="2d9b0-152">Option</span></span></th>
    <th><span data-ttu-id="2d9b0-153">Пользователи, которым назначается задача</span><span class="sxs-lookup"><span data-stu-id="2d9b0-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="2d9b0-154">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="2d9b0-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2d9b0-155">Участник</span><span class="sxs-lookup"><span data-stu-id="2d9b0-155">Participant</span></span></td>
    <td><span data-ttu-id="2d9b0-156">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="2d9b0-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-157">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется назначить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="2d9b0-158">В списке <strong>Участник</strong> выберите группу или роль, которой требуется назначить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-159">Иерархия</span><span class="sxs-lookup"><span data-stu-id="2d9b0-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="2d9b0-160">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="2d9b0-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-161">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, которой требуется назначить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="2d9b0-162">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2d9b0-163">Эти имена представляют пользователей, которым можно назначить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="2d9b0-164">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2d9b0-165">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2d9b0-166">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2d9b0-167">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2d9b0-168">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должна быть назначена задача:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2d9b0-169"><strong>Назначить всем найденным пользователям</strong> — задача назначается всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2d9b0-170"><strong>Назначить только последнему найденному пользователю</strong> — задача назначается только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2d9b0-171"><strong>Исключить пользователей, для которых выполняется следующее</strong> — задача не назначается пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="2d9b0-172">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-173">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2d9b0-173">Workflow user</span></span></td>
    <td><span data-ttu-id="2d9b0-174">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2d9b0-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2d9b0-175">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-176">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2d9b0-176">User</span></span></td>
    <td><span data-ttu-id="2d9b0-177">Определенные пользователи Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d9b0-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-178">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2d9b0-179">Список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2d9b0-180">Выберите пользователей, которым требуется назначить задачу, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-181">Очередь</span><span class="sxs-lookup"><span data-stu-id="2d9b0-181">Queue</span></span></td>
    <td><span data-ttu-id="2d9b0-182">Очередь задач</span><span class="sxs-lookup"><span data-stu-id="2d9b0-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-183">После выбора значения в поле <strong>Очередь</strong> перейдите на вкладку <strong>На основе очереди</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="2d9b0-184">Для назначения задачи к конкретной очереди, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2d9b0-185">В списке <strong>Тип очереди</strong> выберите <strong>Очереди задач</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2d9b0-186">В списке <strong>Имя очереди</strong> выберите очередь.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2d9b0-187">Если определенное условие должно указывать, в какую очередь задача назначается, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2d9b0-188">В списке <strong>Тип очереди</strong> выберите <strong>Зависимые очереди задач</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2d9b0-189">В списке <strong>Имя очереди</strong> выберите <strong>Зависимая очередь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="2d9b0-190">Этот параметр используется только для нескольких workflow-процессов, таких как управление обращениями.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="2d9b0-191">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени отводится пользователю на завершение задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="2d9b0-192">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-192">Select one of the following options:</span></span>

    - <span data-ttu-id="2d9b0-193">**Часы** — введите число часов, которые есть у пользователя для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="2d9b0-194">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2d9b0-195">**Дни** — введите число дней, которые есть у пользователя для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="2d9b0-196">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2d9b0-197">**Недели** — введите число недель, которые есть у пользователя для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="2d9b0-198">**Месяцы** — введите день и неделю, к которой пользователь должен выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="2d9b0-199">Например, можно указать, что пользователь должен выполнить задачу до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2d9b0-200">**Годы** — введите день, неделю и месяц, к которым пользователь должен выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="2d9b0-201">Например, можно указать, что пользователь должен выполнить задачу до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="2d9b0-202">Если пользователь не выполнил задачу за выделенное время, задача считается просроченной.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="2d9b0-203">Просроченная задача может быть эскалирована на основе параметров, выбранных в области **Эскалация** этой страницы.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="2d9b0-204">Задание действий в случае, если задача просрочена</span><span class="sxs-lookup"><span data-stu-id="2d9b0-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="2d9b0-205">Если пользователь не выполнил ручную задачу за выделенное время, задача считается просроченной.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="2d9b0-206">Просроченную задачу можно эскалировать или автоматически назначить другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="2d9b0-207">Выполните следующие действия, чтобы эскалировать задачу, если она просрочена.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="2d9b0-208">В левой области щелкните **Эскалация**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2d9b0-209">Установите флажок **Использовать маршрут эскалации**, чтобы создать маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2d9b0-210">Задача будет автоматически назначена пользователям, перечисленным в маршруте эскалации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2d9b0-211">Например, в следующей таблице представляет собой маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="2d9b0-212">Последовательность</span><span class="sxs-lookup"><span data-stu-id="2d9b0-212">Sequence</span></span> | <span data-ttu-id="2d9b0-213">Путь эскалации</span><span class="sxs-lookup"><span data-stu-id="2d9b0-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="2d9b0-214">1</span><span class="sxs-lookup"><span data-stu-id="2d9b0-214">1</span></span>        | <span data-ttu-id="2d9b0-215">Назначит: Дарье</span><span class="sxs-lookup"><span data-stu-id="2d9b0-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="2d9b0-216">2</span><span class="sxs-lookup"><span data-stu-id="2d9b0-216">2</span></span>        | <span data-ttu-id="2d9b0-217">Назначить: Ирине</span><span class="sxs-lookup"><span data-stu-id="2d9b0-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="2d9b0-218">3</span><span class="sxs-lookup"><span data-stu-id="2d9b0-218">3</span></span>        | <span data-ttu-id="2d9b0-219">Конечное действие: отклонить</span><span class="sxs-lookup"><span data-stu-id="2d9b0-219">Final action: Reject</span></span> |

    <span data-ttu-id="2d9b0-220">В этом примере просроченная задача будет автоматически назначена Дарье.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="2d9b0-221">Если Дарья не выполнит задачу в отведенные сроки, эта система назначит задачу Ирине.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="2d9b0-222">Если Ирина не выполнит задачу за выделенное времени, система отклонит документ, который был отправлен для обработки.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="2d9b0-223">Чтобы добавить пользователя в маршрут эскалации, щелкните **Добавить эскалирование**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2d9b0-224">Во вкладке **Тип назначения** выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2d9b0-225">Параметр</span><span class="sxs-lookup"><span data-stu-id="2d9b0-225">Option</span></span></th>
    <th><span data-ttu-id="2d9b0-226">Пользователи, которым эскалируется задача</span><span class="sxs-lookup"><span data-stu-id="2d9b0-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="2d9b0-227">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="2d9b0-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2d9b0-228">Иерархия</span><span class="sxs-lookup"><span data-stu-id="2d9b0-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="2d9b0-229">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="2d9b0-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-230">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, в которую требуется эскалировать задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="2d9b0-231">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2d9b0-232">Эти имена представляют пользователей, которым можно эскалировать задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="2d9b0-233">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2d9b0-234">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2d9b0-235">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2d9b0-236">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2d9b0-237">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должна быть эскалирована задача:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="2d9b0-238"><strong>Назначить всем найденным пользователям</strong> — задача эскалируется всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="2d9b0-239"><strong>Назначить только последнему найденному пользователю</strong> — задача эскалируется только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2d9b0-240"><strong>Исключить пользователей, для которых выполняется следующее</strong> — задача не эскалируется пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="2d9b0-241">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-242">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2d9b0-242">Workflow user</span></span></td>
    <td><span data-ttu-id="2d9b0-243">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2d9b0-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2d9b0-244">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-245">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2d9b0-245">User</span></span></td>
    <td><span data-ttu-id="2d9b0-246">Определенные пользователи Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d9b0-246">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-247">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2d9b0-248">Список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2d9b0-249">Выберите пользователей, которым требуется эскалировать задачу, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="2d9b0-250">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени отводится пользователю на завершение задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="2d9b0-251">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-251">Select one of the following options:</span></span>

    - <span data-ttu-id="2d9b0-252">**Часы** — введите число часов, которые есть у пользователя для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="2d9b0-253">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2d9b0-254">**Дни** — введите число дней, которые есть у пользователя для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="2d9b0-255">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2d9b0-256">**Недели** — введите число недель, которые есть у пользователя для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="2d9b0-257">**Месяцы** — введите день и неделю, к которой пользователь должен выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="2d9b0-258">Например, можно указать, что пользователь должен выполнить задачу до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2d9b0-259">**Годы** — введите день, неделю и месяц, к которым пользователь должен выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="2d9b0-260">Например, можно указать, что пользователь должен выполнить задачу до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2d9b0-261">Повторите шаги с 3 по 4 для каждого пользователя, которого следует добавить в маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2d9b0-262">можно изменить порядок пользователей.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="2d9b0-263">Если пользователи, перечисленные в маршруте эскалации, не выполнили задачу за отведенное время, система выполняется действие с задачей.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="2d9b0-264">Чтобы указать действие, которое будет выполнять система, выберите строку **Действие** и на вкладке **Конечное действие** выберите действие.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="2d9b0-265">Укажите, когда система автоматически действует в отношении задачи</span><span class="sxs-lookup"><span data-stu-id="2d9b0-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="2d9b0-266">Можно настроить систему на выполнение действия с ручной задачей при соблюдении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="2d9b0-267">Например, задача требует, чтобы член подразделения "Отчеты по расходам" рассматривал чеки, которые отправляются вместе с отчетом по расходам.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="2d9b0-268">В соответствии с политикой компании эту задачу необходимо выполнить, если общая сумма отчета по расходам превышает USD 100.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="2d9b0-269">В этом сценарии можно настроить систему на автоматическую пометку задачи как **Завершено**, если общая сумма меньше 100.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="2d9b0-270">Выполните следующие шаги, чтобы указать, когда система должна выполнять действие в отношении ручной задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="2d9b0-271">В левой области щелкните **Автоматические действия**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="2d9b0-272">Установите флажок **Включить автоматические действия**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="2d9b0-273">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="2d9b0-274">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-274">Enter a condition.</span></span>
5. <span data-ttu-id="2d9b0-275">Введите все необходимые дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="2d9b0-276">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="2d9b0-277">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-277">Click **Test**.</span></span>
    2. <span data-ttu-id="2d9b0-278">На странице **Проверить условие workflow-процесса** в области **Проверить условие** выберите запись.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="2d9b0-279">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-279">Click **Test**.</span></span> <span data-ttu-id="2d9b0-280">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="2d9b0-281">Нажмите кнопку **OK** или **Отмена** для возврата на страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="2d9b0-282">Из списка **Действие автоматического завершения** выберите действие, которое система должна выполнить с задачей.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2d9b0-283">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="2d9b0-283">Specify when notifications are sent</span></span>

<span data-ttu-id="2d9b0-284">Можно отправлять уведомления пользователям, когда ручная задача делегирована, эскалирована, выполнена или отклонена при запросе изменения.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="2d9b0-285">Выполните следующие действия, чтобы определить, когда уведомления будут отправляться, и кому уведомления будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="2d9b0-286">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="2d9b0-287">Установите флажок рядом с событиями, для которых следует отправлять уведомления:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="2d9b0-288">**Делегировать** — задача назначена другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="2d9b0-289">**Эскалировать** — назначенный пользователь не выполнил задачу в отведенное время.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="2d9b0-290">**Завершено** — назначенный пользователь выполнил задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="2d9b0-291">**Отклонить** — назначенный пользователь отклонил отправленный документ.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="2d9b0-292">**Запросить изменение** — назначенный пользователь запросил изменение отправленного документа.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="2d9b0-293">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="2d9b0-294">На вкладке **Текст уведомления** в текстовом поле введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="2d9b0-295">Для того, чтобы персонализовать уведомление можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="2d9b0-296">Заполнители заменяются соответствующей информацией, когда уведомление отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="2d9b0-297">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2d9b0-298">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2d9b0-299">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2d9b0-300">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2d9b0-301">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-301">Click **Insert**.</span></span>

6. <span data-ttu-id="2d9b0-302">Для добавления переводов уведомления выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="2d9b0-303">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="2d9b0-304">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2d9b0-305">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2d9b0-306">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2d9b0-307">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="2d9b0-308">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-308">Click **Close**.</span></span>

7. <span data-ttu-id="2d9b0-309">На вкладке **Получатель** укажите, кому отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="2d9b0-310">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 8.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2d9b0-311">Параметр</span><span class="sxs-lookup"><span data-stu-id="2d9b0-311">Option</span></span></th>
    <th><span data-ttu-id="2d9b0-312">Получатели уведомления.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="2d9b0-313">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="2d9b0-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2d9b0-314">Участник</span><span class="sxs-lookup"><span data-stu-id="2d9b0-314">Participant</span></span></td>
    <td><span data-ttu-id="2d9b0-315">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="2d9b0-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-316">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2d9b0-317">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-318">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2d9b0-318">Workflow user</span></span></td>
    <td><span data-ttu-id="2d9b0-319">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2d9b0-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2d9b0-320">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2d9b0-321">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2d9b0-321">User</span></span></td>
    <td><span data-ttu-id="2d9b0-322">Определенные пользователи Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d9b0-322">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2d9b0-323">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2d9b0-324">Список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2d9b0-325">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="2d9b0-326">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="2d9b0-327">Задание предельного срока</span><span class="sxs-lookup"><span data-stu-id="2d9b0-327">Set a time limit</span></span>

<span data-ttu-id="2d9b0-328">Выполните следующие действия, если ручная задача должна быть выполнена за определенное время.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="2d9b0-329">Параметры, выбранные в этой процедуре, переопределяют параметры, выбранные в областях **Назначение** и **Эскалация** страницы.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="2d9b0-330">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2d9b0-331">Установите флажок **Задать ограничение по времени для элемента workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="2d9b0-332">В поле **Продолжительность** укажите, когда должна быть выполнена эта задача.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="2d9b0-333">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2d9b0-333">Select one of the following options:</span></span>

    - <span data-ttu-id="2d9b0-334">**Часы** — введите число часов, в течение которых должна быть выполнена эта задача.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="2d9b0-335">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2d9b0-336">**Дни** — введите число дней, в течение которых должна быть выполнена эта задача.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="2d9b0-337">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2d9b0-338">**Недели** — введите число недель, в течение которых должна быть выполнена эта задача.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="2d9b0-339">**Месяцы** — выберите день и неделю, к которым должна быть выполнена задача.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="2d9b0-340">Например, можно указать, что задача должна быть выполнена до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2d9b0-341">**Годы** — выберите день, неделю и месяц, к которым должна быть выполнена задача.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="2d9b0-342">Например, можно указать, что задача должна быть выполнена до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="2d9b0-343">По истечении предельного срока система выполнит действие в отношении задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="2d9b0-344">Из списка **Действие** выберите действие, которое должна выполнить система.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="2d9b0-345">Задание диапазона возможных для пользователя действий</span><span class="sxs-lookup"><span data-stu-id="2d9b0-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="2d9b0-346">Когда ручная задача назначается пользователю, он должен выполнить с ней действие.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="2d9b0-347">Выполните следующие действия, чтобы определить, какие действия пользователь может предпринять на задаче.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="2d9b0-348">Набор доступных действий может меняться в зависимости от дизайна задачи.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="2d9b0-349">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2d9b0-350">Установите флажок **Выполнено**, если требуется, чтобы пользователь мог пометить задачу как **Выполнено**.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="2d9b0-351">Установите флажок **Отклонить**, если требуется, чтобы пользователь мог отклонить представленный документ.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="2d9b0-352">Установите флажок **Запросить изменение**, если требуется, чтобы пользователь мог запросить изменения представленных документов.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="2d9b0-353">Установите флажок **Делегировать**, если требуется, чтобы пользователь мог назначить эту задачу другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="2d9b0-354">Установите флажок **Назначить повторно**, если требуется, чтобы пользователь мог назначить повторно эту задачу другому пользователю в очереди задач.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="2d9b0-355">Установите флажок **Запуск в производство**, если требуется, чтобы пользователь мог назначить повторно эту задачу в очередь задач.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="2d9b0-356">Другой пользователь затем сможет выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="2d9b0-356">Another user can then complete the task.</span></span>
