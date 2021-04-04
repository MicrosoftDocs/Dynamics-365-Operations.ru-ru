---
title: Настройка процессов утверждения в workflow-процессе
description: Используйте следующую процедуру для настройки свойств для процесса утверждения.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37a079ee98495a27c1462df32f2973b012069ca8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562821"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="49ef0-103">Настройка процессов утверждения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="49ef0-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49ef0-104">Используйте следующую процедуру для настройки свойств для процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="49ef0-105">Чтобы настроить процесс утверждения, в редакторе workflow-процесса щелкните правой кнопкой мыши элемент утверждения, затем щелкните **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="49ef0-106">Задание названия для процесса утверждения</span><span class="sxs-lookup"><span data-stu-id="49ef0-106">Name the approval process</span></span>

<span data-ttu-id="49ef0-107">Чтобы ввести название процесса утверждения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49ef0-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="49ef0-108">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="49ef0-109">В поле **Имя** введите уникальное название для процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="49ef0-110">Укажите, когда система автоматически действует в отношении документа</span><span class="sxs-lookup"><span data-stu-id="49ef0-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="49ef0-111">Можно настроить систему на автоматическую обработку документов, если выполняются определенные условия.</span><span class="sxs-lookup"><span data-stu-id="49ef0-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="49ef0-112">Например, система может утверждать отчеты по расходам, имеющих общие суммы, которые меньше USD 100.</span><span class="sxs-lookup"><span data-stu-id="49ef0-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="49ef0-113">Выполните следующие действия, чтобы указать, когда система действует в отношении документа.</span><span class="sxs-lookup"><span data-stu-id="49ef0-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="49ef0-114">В левой области щелкните **Автоматические действия**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="49ef0-115">Установите флажок **Включить автоматические действия**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="49ef0-116">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="49ef0-117">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="49ef0-117">Enter a condition.</span></span>
5. <span data-ttu-id="49ef0-118">При необходимости введите дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="49ef0-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="49ef0-119">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49ef0-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="49ef0-120">Щелкните **Проверка** для открытия формы **Условия тестового workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="49ef0-121">Выберите запись в области **Проверка условия** формы.</span><span class="sxs-lookup"><span data-stu-id="49ef0-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="49ef0-122">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-122">Click **Test**.</span></span> <span data-ttu-id="49ef0-123">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="49ef0-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="49ef0-124">Щелкните **OK** или **Отмена** для возврата к форме **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="49ef0-125">Из списка **Действие автоматического завершения** выберите действие, которое система должна выполнить с документом.</span><span class="sxs-lookup"><span data-stu-id="49ef0-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="49ef0-126">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="49ef0-126">Specify when notifications are sent</span></span>

<span data-ttu-id="49ef0-127">Можно отправлять уведомления пользователям, когда документ утвержден, отклонен, делегирован, эскалирована или был запрос изменения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="49ef0-128">Выполните следующие действия, чтобы определить, когда уведомления будут отправляться, и кому уведомления будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="49ef0-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="49ef0-129">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="49ef0-130">Установите флажок рядом с событиями, для которых следует отправлять уведомления:</span><span class="sxs-lookup"><span data-stu-id="49ef0-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="49ef0-131">**Делегировать** – назначение документа другому пользователю для утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="49ef0-132">**Эскалировать** - когда назначенный пользователь не выполнил действия с документом в отведенное время.</span><span class="sxs-lookup"><span data-stu-id="49ef0-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="49ef0-133">**Утвердить** - Когда документ был утвержден.</span><span class="sxs-lookup"><span data-stu-id="49ef0-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="49ef0-134">**Отклонить** - Когда документ был отклонен.</span><span class="sxs-lookup"><span data-stu-id="49ef0-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="49ef0-135">**Запросить изменение** — Когда назначенный пользователь запросил изменение представленного документа.</span><span class="sxs-lookup"><span data-stu-id="49ef0-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="49ef0-136">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="49ef0-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="49ef0-137">Выберите вкладку **Текст уведомления**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="49ef0-138">В текстовом поле введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="49ef0-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="49ef0-139">Для персонализации текста можно вставить заполнители, которые будут заменены соответствующими данными, когда пользователи будут просматривать уведомление.</span><span class="sxs-lookup"><span data-stu-id="49ef0-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="49ef0-140">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="49ef0-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="49ef0-141">Щелкните в текстовом поле в местонахождение, в котором необходимо находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="49ef0-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="49ef0-142">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="49ef0-143">В списке, который отображается выберите заполнитель, чтобы ввести.</span><span class="sxs-lookup"><span data-stu-id="49ef0-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="49ef0-144">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-144">Click **Insert**.</span></span>

7. <span data-ttu-id="49ef0-145">Для добавления переводов уведомления, нажмите **Трансляции**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="49ef0-146">В форме, которая отображается, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="49ef0-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="49ef0-147">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-147">Click **Add**.</span></span>
    2. <span data-ttu-id="49ef0-148">В списке, который отображается выберите язык в котором будет введен текст.</span><span class="sxs-lookup"><span data-stu-id="49ef0-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="49ef0-149">Введите нужный текст в текстовое поле **Переведенный текст**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="49ef0-150">Чтобы настроить текст, введите Заполнители.</span><span class="sxs-lookup"><span data-stu-id="49ef0-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="49ef0-151">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-151">Click **Close**.</span></span>

8. <span data-ttu-id="49ef0-152">Выберите вкладку **Получатель**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="49ef0-153">Задать кому отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="49ef0-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="49ef0-154">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для параметра перед тем как перейдите к шагу 10.</span><span class="sxs-lookup"><span data-stu-id="49ef0-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="49ef0-155">Параметр</span><span class="sxs-lookup"><span data-stu-id="49ef0-155">Option</span></span></th>
    <th><span data-ttu-id="49ef0-156">Получатели уведомления.</span><span class="sxs-lookup"><span data-stu-id="49ef0-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="49ef0-157">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="49ef0-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="49ef0-158"><strong>Участник</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="49ef0-159">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="49ef0-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="49ef0-160">После выбора <strong>Участник</strong> перейдите на вкладку <strong>На основе роли</strong>.</span><span class="sxs-lookup"><span data-stu-id="49ef0-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="49ef0-161">В списке <strong>Тип участника</strong> выберите тип группы или роли, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="49ef0-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="49ef0-162">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="49ef0-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="49ef0-163"><strong>Пользователь workflow-процесса</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="49ef0-164">Пользователи, участвующие в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="49ef0-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="49ef0-165">После выбора параметра <strong>Пользователь workflow-процесса</strong> перейдите на вкладку <strong>Пользователь workflow-процесса</strong>.</span><span class="sxs-lookup"><span data-stu-id="49ef0-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="49ef0-166">В списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который участвует в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="49ef0-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="49ef0-167"><strong>Пользователь</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="49ef0-168">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="49ef0-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="49ef0-169">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="49ef0-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="49ef0-170">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="49ef0-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="49ef0-171">Повторите шаги 3-9 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="49ef0-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="49ef0-172">Определение лица, ответственного за окончательное утверждение</span><span class="sxs-lookup"><span data-stu-id="49ef0-172">Specify a final approver</span></span>

<span data-ttu-id="49ef0-173">Можно назначить окончательное утверждающего лицо для сценариев, в которых утверждающий является лицом, которое отправило документ на утверждение, и используется "Запретить утверждение отправителем".</span><span class="sxs-lookup"><span data-stu-id="49ef0-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="49ef0-174">Чтобы определить ответственного за окончательное утверждение, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49ef0-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="49ef0-175">В редакторе workflow-процесса щелкните правой кнопкой мыши элемент утверждения, затем выберите **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="49ef0-176">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="49ef0-177">Установите флажок **Использовать окончательного утверждающего лица**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="49ef0-178">Из списка выберите пользователя, который будет выполнять окончательное утверждение.</span><span class="sxs-lookup"><span data-stu-id="49ef0-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="49ef0-179">Задание предельного срока</span><span class="sxs-lookup"><span data-stu-id="49ef0-179">Set a time limit</span></span>

<span data-ttu-id="49ef0-180">Выполните следующие действия, если процесс утверждения должна быть выполнена за определенное время.</span><span class="sxs-lookup"><span data-stu-id="49ef0-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="49ef0-181">Указанные в этих шагах параметры имеют больший приоритет, чем параметры, выбранные в областях **Назначение** и **Эскалация** для каждого шага утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="49ef0-182">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="49ef0-183">Установите флажок **Задать ограничение по времени для** **элемента workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="49ef0-184">Укажите в поле **Продолжительность**, когда процесс утверждения должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="49ef0-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="49ef0-185">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="49ef0-185">Select one of the following options:</span></span>

    - <span data-ttu-id="49ef0-186">**Часы** — Введите число часов, в течение которых эта процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="49ef0-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="49ef0-187">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="49ef0-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="49ef0-188">**Дни** — Введите число дней, в течение которых эта процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="49ef0-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="49ef0-189">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="49ef0-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="49ef0-190">**Недели** — Введите число недель, в течение которых эта процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="49ef0-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="49ef0-191">**Месяцы** — Выберите день и неделю, когда процесс утверждения должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="49ef0-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="49ef0-192">Например, можно указать, что этот процесс утверждения должен быть завершен до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="49ef0-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="49ef0-193">**Годы** — Выберите день и неделю и месяц, когда процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="49ef0-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="49ef0-194">Например, можно указать, что этот процесс утверждения должен быть завершен до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="49ef0-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="49ef0-195">По истечении предельного срока система действует в отношении документа.</span><span class="sxs-lookup"><span data-stu-id="49ef0-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="49ef0-196">Из списка **Действие** выберите действие, которое должна выполнить система.</span><span class="sxs-lookup"><span data-stu-id="49ef0-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="49ef0-197">Задание диапазона возможных для пользователя действий</span><span class="sxs-lookup"><span data-stu-id="49ef0-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="49ef0-198">Когда документ назначен пользователю для утверждения, пользователь должен его обработать.</span><span class="sxs-lookup"><span data-stu-id="49ef0-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="49ef0-199">Выполните следующие действия, чтобы определить, какие действия пользователь может предпринять на отправленном документе.</span><span class="sxs-lookup"><span data-stu-id="49ef0-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="49ef0-200">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="49ef0-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="49ef0-201">Установите флажок **Утвердить**, если требуется, чтобы пользователь мог утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="49ef0-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="49ef0-202">Установите флажок **Отклонить**, если требуется, чтобы пользователь мог Отклонить документ.</span><span class="sxs-lookup"><span data-stu-id="49ef0-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="49ef0-203">Установите флажок **Запросить изменение**, если требуется, чтобы пользователи могли запрашивать изменение документа.</span><span class="sxs-lookup"><span data-stu-id="49ef0-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="49ef0-204">Установите флажок **Делегировать**, если пользователь может назначить документ другому пользователю на утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="49ef0-205">Флажок **Включение действий из списка работ на корпоративном портале** устарел.</span><span class="sxs-lookup"><span data-stu-id="49ef0-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="49ef0-206">Настройка шагов утверждения</span><span class="sxs-lookup"><span data-stu-id="49ef0-206">Configure the approval steps</span></span>

<span data-ttu-id="49ef0-207">Процесс утверждения состоит из шагов утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="49ef0-208">Выполните следующую процедуру, чтобы добавить шаги процесса утверждения и настроить шаги.</span><span class="sxs-lookup"><span data-stu-id="49ef0-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="49ef0-209">В редакторе workflow-процесс, дважды щелкните процесс утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="49ef0-210">Редактор workflow-процесс отображает шаги процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="49ef0-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="49ef0-211">Для добавления шага утверждения, перетащите шаг из зоны **Элементы workflow-процесса** на холст.</span><span class="sxs-lookup"><span data-stu-id="49ef0-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="49ef0-212">Для настройки стадии утверждения см. раздел [Настройка этапов утверждения в workflow-процессе](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="49ef0-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]