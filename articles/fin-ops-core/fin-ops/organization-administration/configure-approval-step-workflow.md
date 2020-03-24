---
title: Настройка этапов утверждения в workflow-процессе
description: В этом разделе описывается, как настроить свойства шага утверждения.
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
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5bd5300a061e12ccabdea83c20863c95e15fe19
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124689"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="80e26-103">Настройка этапов утверждения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="80e26-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80e26-104">В этом разделе описывается, как настроить свойства шага утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="80e26-105">Чтобы настроить шаг утверждения, в редакторе workflow-процессов щелкните правой кнопкой мыши шаг утверждения и выберите **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="80e26-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="80e26-106">Затем используйте следующие процедуры для настройки свойств шага утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="80e26-107">Создание названия шага</span><span class="sxs-lookup"><span data-stu-id="80e26-107">Name the step</span></span>
<span data-ttu-id="80e26-108">Чтобы ввести имя шаг утверждения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="80e26-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="80e26-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="80e26-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="80e26-110">В поле **Имя** введите уникальное имя шага утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="80e26-111">Ввод строки темы и инструкций</span><span class="sxs-lookup"><span data-stu-id="80e26-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="80e26-112">Пользователям, назначенным этой шагу утверждения, должны быть предоставлены строка темы и инструкции.</span><span class="sxs-lookup"><span data-stu-id="80e26-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="80e26-113">Например, при настройке шага утверждения для заявок на покупку, пользователь, который назначается шагу, увидит строку темы и инструкции на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="80e26-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="80e26-114">Строка темы будет отображаться в строке сообщений на странице.</span><span class="sxs-lookup"><span data-stu-id="80e26-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="80e26-115">Пользователь может щелкнуть значок в строке сообщений, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="80e26-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="80e26-116">Чтобы ввести строку темы и инструкции, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="80e26-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="80e26-117">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="80e26-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="80e26-118">В поле **Тема рабочего элемента** введите строку темы.</span><span class="sxs-lookup"><span data-stu-id="80e26-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="80e26-119">Для того, чтобы персонализовать строку уведомления можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="80e26-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="80e26-120">Заполнители заменяются соответствующей информацией, когда строка темы отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="80e26-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="80e26-121">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="80e26-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="80e26-122">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="80e26-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="80e26-123">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="80e26-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="80e26-124">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="80e26-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="80e26-125">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="80e26-125">Click **Insert**.</span></span>

4. <span data-ttu-id="80e26-126">Для добавления переводов строки темы выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="80e26-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="80e26-127">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="80e26-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="80e26-128">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="80e26-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="80e26-129">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="80e26-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="80e26-130">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="80e26-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="80e26-131">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="80e26-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="80e26-132">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="80e26-132">Click **Close**.</span></span>

5. <span data-ttu-id="80e26-133">В поле **Инструкции рабочего элемента** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="80e26-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="80e26-134">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="80e26-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="80e26-135">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="80e26-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="80e26-136">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="80e26-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="80e26-137">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="80e26-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="80e26-138">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="80e26-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="80e26-139">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="80e26-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="80e26-140">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="80e26-140">Click **Insert**.</span></span>

7. <span data-ttu-id="80e26-141">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="80e26-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="80e26-142">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="80e26-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="80e26-143">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="80e26-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="80e26-144">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="80e26-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="80e26-145">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="80e26-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="80e26-146">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 6.</span><span class="sxs-lookup"><span data-stu-id="80e26-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="80e26-147">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="80e26-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="80e26-148">Назначение шага утверждения</span><span class="sxs-lookup"><span data-stu-id="80e26-148">Assign the approval step</span></span>

<span data-ttu-id="80e26-149">Чтобы указать, кому требуется назначить шаг утверждения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="80e26-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="80e26-150">В левой области щелкните **Назначение**.</span><span class="sxs-lookup"><span data-stu-id="80e26-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="80e26-151">Во вкладке **Тип назначения** выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 3.</span><span class="sxs-lookup"><span data-stu-id="80e26-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="80e26-152">Параметр</span><span class="sxs-lookup"><span data-stu-id="80e26-152">Option</span></span></th>
    <th><span data-ttu-id="80e26-153">Пользователи, которым назначается шаг утверждения</span><span class="sxs-lookup"><span data-stu-id="80e26-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="80e26-154">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="80e26-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="80e26-155">Участник</span><span class="sxs-lookup"><span data-stu-id="80e26-155">Participant</span></span></td>
    <td><span data-ttu-id="80e26-156">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="80e26-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="80e26-157">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется назначить шаг.</span><span class="sxs-lookup"><span data-stu-id="80e26-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="80e26-158">В списке <strong>Участник</strong> выберите группу или роль, которой требуется назначить шаг.</span><span class="sxs-lookup"><span data-stu-id="80e26-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="80e26-159">Иерархия</span><span class="sxs-lookup"><span data-stu-id="80e26-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="80e26-160">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="80e26-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="80e26-161">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, которой требуется назначить шаг.</span><span class="sxs-lookup"><span data-stu-id="80e26-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="80e26-162">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="80e26-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="80e26-163">Эти имена представляют пользователей, которым можно назначить шаг.</span><span class="sxs-lookup"><span data-stu-id="80e26-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="80e26-164">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="80e26-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="80e26-165">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="80e26-166">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="80e26-167">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="80e26-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="80e26-168">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должен быть назначен шаг:</span><span class="sxs-lookup"><span data-stu-id="80e26-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="80e26-169"><strong>Назначить всем найденным пользователям</strong> — шаг назначается всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="80e26-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="80e26-170"><strong>Назначить только последнему найденному пользователю</strong> — шаг назначается только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="80e26-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="80e26-171"><strong>Исключить пользователей, для которых выполняется следующее</strong> — шаг не назначается пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="80e26-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="80e26-172">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="80e26-173">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="80e26-173">Workflow user</span></span></td>
    <td><span data-ttu-id="80e26-174">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="80e26-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="80e26-175">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="80e26-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="80e26-176">Пользователь</span><span class="sxs-lookup"><span data-stu-id="80e26-176">User</span></span></td>
    <td><span data-ttu-id="80e26-177">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="80e26-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="80e26-178">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="80e26-179">Список <strong>Доступные пользователи</strong> включает всех пользователей системы.</span><span class="sxs-lookup"><span data-stu-id="80e26-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="80e26-180">Выберите пользователей, которым требуется назначить шаг, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="80e26-181">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени пользователь может потратить на обработку документов, поступивших на этом шаге утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="80e26-182">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="80e26-182">Select one of the following options:</span></span>

    - <span data-ttu-id="80e26-183">**Часы** — введите число часов, предоставляются пользователю на ответ.</span><span class="sxs-lookup"><span data-stu-id="80e26-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="80e26-184">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="80e26-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="80e26-185">**Дни** — введите число дней, которые предоставляются пользователю на ответ.</span><span class="sxs-lookup"><span data-stu-id="80e26-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="80e26-186">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="80e26-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="80e26-187">**Недели** — введите число недель, которые предоставляются пользователю на ответ.</span><span class="sxs-lookup"><span data-stu-id="80e26-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="80e26-188">**Месяцы** — выберите день и неделю, к которым должен ответить пользователь.</span><span class="sxs-lookup"><span data-stu-id="80e26-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="80e26-189">Например, вам необходимо, чтобы пользователь ответил к пятнице третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="80e26-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="80e26-190">**Годы** — выберите день, неделю и месяц, к которым должен ответить пользователь.</span><span class="sxs-lookup"><span data-stu-id="80e26-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="80e26-191">Например, вам необходимо, чтобы пользователь ответил к пятнице третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="80e26-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="80e26-192">Если пользователь не предпринимает действие с документом за выделенное время, документ считается просроченным.</span><span class="sxs-lookup"><span data-stu-id="80e26-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="80e26-193">Просроченный документ эскалируется на основе параметров, выбранных в области **Эскалация** этой страницы.</span><span class="sxs-lookup"><span data-stu-id="80e26-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="80e26-194">Если шаг утверждения назначен нескольким пользователям или группе пользователей, перейдите на вкладку **Политика выполнения** и затем выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="80e26-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="80e26-195">**Один утверждающий** — Действие в отношении этого документа определяется первым отвечающим лицом.</span><span class="sxs-lookup"><span data-stu-id="80e26-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="80e26-196">Например, Сэм подал отчет по расходам на сумму 15 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="80e26-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="80e26-197">Отчет по расходам в настоящее время назначен Сью, Джо и Биллу.</span><span class="sxs-lookup"><span data-stu-id="80e26-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="80e26-198">Если Сью является первым отвечающим лицом для данного документа, действие, которое она совершает, применяется к документу.</span><span class="sxs-lookup"><span data-stu-id="80e26-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="80e26-199">Если Сью отклоняет документ, документ не утверждается и направляется назад Сэму.</span><span class="sxs-lookup"><span data-stu-id="80e26-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="80e26-200">Если Сью утверждает документ, он направляется Анне для утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Workflow-процесс с процессом утверждения](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="80e26-202">**Большинство утверждающих** — Действие в отношении этого документа определяется, когда отвечает большинство утверждающих лиц.</span><span class="sxs-lookup"><span data-stu-id="80e26-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="80e26-203">Например, Сэм подал отчет по расходам на сумму 15 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="80e26-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="80e26-204">Отчет по расходам в настоящее время назначен Сью, Джо и Биллу.</span><span class="sxs-lookup"><span data-stu-id="80e26-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="80e26-205">Если первые отвечающие утверждающие лица - Сью и Джо, их действие применяется к документу.</span><span class="sxs-lookup"><span data-stu-id="80e26-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="80e26-206">Если Сью утверждает документ, а Джо - нет, документ не утверждается и направляется назад к Сэму.</span><span class="sxs-lookup"><span data-stu-id="80e26-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="80e26-207">Если Сью и Джо утверждают документ, он направляется Анне для утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="80e26-208">**Процент от утверждающих** — Действие в отношении этого документа определяется, когда отвечает определенный процент утверждающих лиц.</span><span class="sxs-lookup"><span data-stu-id="80e26-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="80e26-209">Например, Сэм подал отчет по расходам на сумму 15 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="80e26-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="80e26-210">Отчет по расходам сейчас назначен Сью, Джо и Биллу и вы ввели как процент **50**.</span><span class="sxs-lookup"><span data-stu-id="80e26-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="80e26-211">Если первые отвечающие утверждающие лица — Сью и Джо, их действие применяется к документу, так как они соответствуют требованию в 50 процентов утверждающих.</span><span class="sxs-lookup"><span data-stu-id="80e26-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="80e26-212">Если Сью утверждает документ, а Джо - нет, документ не утверждается и направляется назад к Сэму.</span><span class="sxs-lookup"><span data-stu-id="80e26-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="80e26-213">Если Сью и Джо утверждают документ, он направляется Анне для утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="80e26-214">**Все утверждающие** - все утверждающие лица должны утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="80e26-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="80e26-215">В противном случае workflow-процесс невозможно продолжить.</span><span class="sxs-lookup"><span data-stu-id="80e26-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="80e26-216">Например, Сэм подал отчет по расходам на сумму 15 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="80e26-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="80e26-217">Отчет по расходам в настоящее время назначен Сью, Джо и Биллу.</span><span class="sxs-lookup"><span data-stu-id="80e26-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="80e26-218">Если Сью и Джо утверждает документ, а Билл - нет, документ не утверждается и направляется назад к Сэму.</span><span class="sxs-lookup"><span data-stu-id="80e26-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="80e26-219">Если Сью, Джо и Билл утверждают документ, он направляется Анне для утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="80e26-220">Задание условий использования для данного шага утверждения</span><span class="sxs-lookup"><span data-stu-id="80e26-220">Specify when the approval step is required</span></span>

<span data-ttu-id="80e26-221">Можно задать условий использования для данного шага утверждения</span><span class="sxs-lookup"><span data-stu-id="80e26-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="80e26-222">Шаг утверждения может быть обязательным всегда или только при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="80e26-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="80e26-223">Шаг утверждения Требуется всегда</span><span class="sxs-lookup"><span data-stu-id="80e26-223">The approval step is always required</span></span>

<span data-ttu-id="80e26-224">Выполните следующие действия, если шаг утверждения Требуется всегда.</span><span class="sxs-lookup"><span data-stu-id="80e26-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="80e26-225">В левой области щелкните **Условие**.</span><span class="sxs-lookup"><span data-stu-id="80e26-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="80e26-226">Установите переключатель в положение **Всегда выполнять этот шаг**.</span><span class="sxs-lookup"><span data-stu-id="80e26-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="80e26-227">шаг утверждения должен использоваться при соблюдении определенных условий</span><span class="sxs-lookup"><span data-stu-id="80e26-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="80e26-228">Настраиваемый шаг утверждения может быть обязательным только при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="80e26-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="80e26-229">Например, если вы настраиваете шаг утверждения для workflow-процесса заявки на покупку, вам может потребоваться, чтобы этот шаг утверждения выполнялся, только если сумма в заявке на покупку превышает 10 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="80e26-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="80e26-230">Выполните следующие действия, чтобы указать если шаг утверждения Требуется.</span><span class="sxs-lookup"><span data-stu-id="80e26-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="80e26-231">В левой области щелкните **Условие**.</span><span class="sxs-lookup"><span data-stu-id="80e26-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="80e26-232">Установите переключатель в положение **Выполнять этот шаг только при соблюдении следующего условия**.</span><span class="sxs-lookup"><span data-stu-id="80e26-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="80e26-233">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="80e26-233">Enter a condition.</span></span>
4. <span data-ttu-id="80e26-234">Введите все необходимые дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="80e26-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="80e26-235">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="80e26-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="80e26-236">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="80e26-236">Click **Test**.</span></span>
    2. <span data-ttu-id="80e26-237">На странице **Проверить условие workflow-процесса** в области **Проверить условие** выберите запись.</span><span class="sxs-lookup"><span data-stu-id="80e26-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="80e26-238">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="80e26-238">Click **Test**.</span></span> <span data-ttu-id="80e26-239">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="80e26-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="80e26-240">Нажмите кнопку **OK** или **Отмена** для возврата на страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="80e26-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="80e26-241">Задание действий в случае, если документ просрочен</span><span class="sxs-lookup"><span data-stu-id="80e26-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="80e26-242">Если пользователь не предпринимает действие с документом за выделенное время, документ считается просроченным.</span><span class="sxs-lookup"><span data-stu-id="80e26-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="80e26-243">Просроченный документ можно эскалировать или автоматически назначить другому пользователю для утверждения.</span><span class="sxs-lookup"><span data-stu-id="80e26-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="80e26-244">Выполните следующие шаги, чтобы эскалировать документ, если он просрочен.</span><span class="sxs-lookup"><span data-stu-id="80e26-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="80e26-245">В левой области щелкните **Эскалация**.</span><span class="sxs-lookup"><span data-stu-id="80e26-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="80e26-246">Установите флажок **Использовать маршрут эскалации**, чтобы создать маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="80e26-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="80e26-247">Документ будет автоматически назначена пользователям, перечисленным в маршруте эскалации.</span><span class="sxs-lookup"><span data-stu-id="80e26-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="80e26-248">Например, в следующей таблице представляет собой маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="80e26-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="80e26-249">Последовательность</span><span class="sxs-lookup"><span data-stu-id="80e26-249">Sequence</span></span> | <span data-ttu-id="80e26-250">Путь эскалации</span><span class="sxs-lookup"><span data-stu-id="80e26-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="80e26-251">1</span><span class="sxs-lookup"><span data-stu-id="80e26-251">1</span></span>        | <span data-ttu-id="80e26-252">Назначит: Дарье</span><span class="sxs-lookup"><span data-stu-id="80e26-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="80e26-253">2</span><span class="sxs-lookup"><span data-stu-id="80e26-253">2</span></span>        | <span data-ttu-id="80e26-254">Назначить: Ирине</span><span class="sxs-lookup"><span data-stu-id="80e26-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="80e26-255">3</span><span class="sxs-lookup"><span data-stu-id="80e26-255">3</span></span>        | <span data-ttu-id="80e26-256">Конечное действие: отклонить</span><span class="sxs-lookup"><span data-stu-id="80e26-256">Final action: Reject</span></span> |

    <span data-ttu-id="80e26-257">В этом примере просроченный документ будет автоматически назначена Дарье.</span><span class="sxs-lookup"><span data-stu-id="80e26-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="80e26-258">Если Дарья не ответит в отведенные сроки, система назначит документ Ирине.</span><span class="sxs-lookup"><span data-stu-id="80e26-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="80e26-259">Если Ирина не ответит в отведенные сроки, система отклонит документ.</span><span class="sxs-lookup"><span data-stu-id="80e26-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="80e26-260">Чтобы добавить пользователя в маршрут эскалации, щелкните **Добавить эскалирование**.</span><span class="sxs-lookup"><span data-stu-id="80e26-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="80e26-261">Во вкладке **Тип назначения** выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="80e26-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="80e26-262">Параметр</span><span class="sxs-lookup"><span data-stu-id="80e26-262">Option</span></span></th>
    <th><span data-ttu-id="80e26-263">Пользователи, которым эскалируется документ</span><span class="sxs-lookup"><span data-stu-id="80e26-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="80e26-264">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="80e26-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="80e26-265">Иерархия</span><span class="sxs-lookup"><span data-stu-id="80e26-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="80e26-266">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="80e26-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="80e26-267">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, в которую требуется эскалировать документ.</span><span class="sxs-lookup"><span data-stu-id="80e26-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="80e26-268">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="80e26-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="80e26-269">Эти имена представляют пользователей, которым может быть эскалирован документ.</span><span class="sxs-lookup"><span data-stu-id="80e26-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="80e26-270">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="80e26-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="80e26-271">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="80e26-272">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="80e26-273">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="80e26-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="80e26-274">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должен быть эскалирован документ:</span><span class="sxs-lookup"><span data-stu-id="80e26-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="80e26-275"><strong>Назначить всем найденным пользователям</strong> — документ эскалируется всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="80e26-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="80e26-276"><strong>Назначить только последнему найденному пользователю</strong> — документ эскалируется только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="80e26-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="80e26-277"><strong>Исключить пользователей, для которых выполняется следующее:</strong> — документ не эскалируется пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="80e26-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="80e26-278">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="80e26-279">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="80e26-279">Workflow user</span></span></td>
    <td><span data-ttu-id="80e26-280">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="80e26-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="80e26-281">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="80e26-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="80e26-282">Пользователь</span><span class="sxs-lookup"><span data-stu-id="80e26-282">User</span></span></td>
    <td><span data-ttu-id="80e26-283">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="80e26-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="80e26-284">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="80e26-285">Список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="80e26-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="80e26-286">Выберите пользователей, которым требуется эскалировать документ, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="80e26-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="80e26-287">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени пользователь может потратить на обработку документов.</span><span class="sxs-lookup"><span data-stu-id="80e26-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="80e26-288">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="80e26-288">Select one of the following options:</span></span>

    - <span data-ttu-id="80e26-289">**Часы** — введите число часов, предоставляются пользователю на ответ.</span><span class="sxs-lookup"><span data-stu-id="80e26-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="80e26-290">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="80e26-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="80e26-291">**Дни** — введите число дней, которые предоставляются пользователю на ответ.</span><span class="sxs-lookup"><span data-stu-id="80e26-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="80e26-292">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="80e26-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="80e26-293">**Недели** — введите число недель, которые предоставляются пользователю на ответ.</span><span class="sxs-lookup"><span data-stu-id="80e26-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="80e26-294">**Месяцы** — выберите день и неделю, к которым должен ответить пользователь.</span><span class="sxs-lookup"><span data-stu-id="80e26-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="80e26-295">Например, вам необходимо, чтобы пользователь ответил к пятнице третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="80e26-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="80e26-296">**Годы** — выберите день, неделю и месяц, к которым должен ответить пользователь.</span><span class="sxs-lookup"><span data-stu-id="80e26-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="80e26-297">Например, вам необходимо, чтобы пользователь ответил к пятнице третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="80e26-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="80e26-298">Повторите шаги с 3 по 4 для каждого пользователя, которого следует добавить в маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="80e26-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="80e26-299">можно изменить порядок пользователей.</span><span class="sxs-lookup"><span data-stu-id="80e26-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="80e26-300">Если пользователи, перечисленные в маршруте эскалации, не отвечают за отведенное время, система автоматически выполняет действие с документом.</span><span class="sxs-lookup"><span data-stu-id="80e26-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="80e26-301">Чтобы указать действие, которое будет выполнять система, выберите строку **Действие** и на вкладке **Конечное действие** выберите действие.</span><span class="sxs-lookup"><span data-stu-id="80e26-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
