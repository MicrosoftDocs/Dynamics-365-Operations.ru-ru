---
title: Настройка автоматизированных задач в workflow-процессе
description: В этом разделе описывается, как настроить свойства автоматизированной задачи.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f02b128036ebc0bd8789ecafd1e72e26fe31436
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747963"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="73271-103">Настройка автоматизированных задач в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="73271-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73271-104">В этом разделе описывается, как настроить свойства автоматизированной задачи.</span><span class="sxs-lookup"><span data-stu-id="73271-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="73271-105">Чтобы настроить автоматизированную задачу, в редакторе workflow-процессов щелкните правой кнопкой мыши задачу и выберите **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="73271-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="73271-106">Затем используйте следующие процедуры для настройки свойств автоматизированной задачи.</span><span class="sxs-lookup"><span data-stu-id="73271-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="73271-107">Задание имени задачи</span><span class="sxs-lookup"><span data-stu-id="73271-107">Name the task</span></span>

<span data-ttu-id="73271-108">Чтобы ввести имя автоматизированная задача, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73271-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="73271-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="73271-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="73271-110">В поле **Имя** введите уникальное имя задачи.</span><span class="sxs-lookup"><span data-stu-id="73271-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="73271-111">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="73271-111">Specify when notifications are sent</span></span>

<span data-ttu-id="73271-112">Можно отправлять уведомления пользователям при выполнении или отмене автоматизированной задачи.</span><span class="sxs-lookup"><span data-stu-id="73271-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="73271-113">Выполните следующие действия, чтобы определить, когда уведомления будут отправляться, и кому уведомления будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="73271-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="73271-114">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="73271-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="73271-115">Установите флажок рядом с событиями, для которых следует отправлять уведомления:</span><span class="sxs-lookup"><span data-stu-id="73271-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="73271-116">**Выполнение** - уведомления будут отправляться при выполнении задачи.</span><span class="sxs-lookup"><span data-stu-id="73271-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="73271-117">**Отменено** - уведомления будут отправляться при отмене задачи.</span><span class="sxs-lookup"><span data-stu-id="73271-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="73271-118">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="73271-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="73271-119">На вкладке **Текст уведомления** в текстовом поле введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="73271-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="73271-120">Для того, чтобы персонализовать уведомление можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="73271-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="73271-121">Заполнители заменяются соответствующей информацией, когда уведомление отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="73271-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="73271-122">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="73271-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="73271-123">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="73271-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="73271-124">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="73271-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="73271-125">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="73271-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="73271-126">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="73271-126">Click **Insert**.</span></span>

6. <span data-ttu-id="73271-127">Для добавления переводов уведомления выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="73271-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="73271-128">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="73271-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="73271-129">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="73271-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="73271-130">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="73271-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="73271-131">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="73271-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="73271-132">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="73271-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="73271-133">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="73271-133">Click **Close**.</span></span>

7. <span data-ttu-id="73271-134">На вкладке **Получатель** укажите, кому отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="73271-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="73271-135">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 8.</span><span class="sxs-lookup"><span data-stu-id="73271-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="73271-136">Параметр</span><span class="sxs-lookup"><span data-stu-id="73271-136">Option</span></span></th>
    <th><span data-ttu-id="73271-137">Получатели уведомления.</span><span class="sxs-lookup"><span data-stu-id="73271-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="73271-138">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="73271-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="73271-139">Участник</span><span class="sxs-lookup"><span data-stu-id="73271-139">Participant</span></span></td>
    <td><span data-ttu-id="73271-140">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="73271-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="73271-141">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="73271-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="73271-142">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="73271-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="73271-143">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="73271-143">Workflow user</span></span></td>
    <td><span data-ttu-id="73271-144">Пользователи, участвующие в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="73271-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="73271-145">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="73271-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="73271-146">Пользователь</span><span class="sxs-lookup"><span data-stu-id="73271-146">User</span></span></td>
    <td><span data-ttu-id="73271-147">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="73271-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="73271-148">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="73271-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="73271-149">Список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="73271-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="73271-150">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="73271-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="73271-151">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="73271-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]