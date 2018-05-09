---
title: "Настройка процесса утверждения в workflow-процессе"
description: "Используйте следующую процедуру для настройки свойств для процесса утверждения."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7a7770abf84d8f3c77e348c6aedb785dcb8ea28b
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="configure-an-approval-process-in-a-workflow"></a><span data-ttu-id="7c194-103">Настройка процесса утверждения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="7c194-103">Configure an approval process in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c194-104">Используйте следующую процедуру для настройки свойств для процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="7c194-105">Чтобы настроить процесс утверждения, в редакторе workflow-процесса щелкните правой кнопкой мыши элемент утверждения, затем щелкните **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7c194-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="7c194-106">Задание названия для процесса утверждения</span><span class="sxs-lookup"><span data-stu-id="7c194-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="7c194-107">Чтобы ввести название процесса утверждения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7c194-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="7c194-108">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="7c194-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="7c194-109">В поле **Имя** введите уникальное название для процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="7c194-110">Укажите, когда система автоматически действует в отношении документа</span><span class="sxs-lookup"><span data-stu-id="7c194-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="7c194-111">Можно настроить систему на автоматическую обработку документов, если выполняются определенные условия.</span><span class="sxs-lookup"><span data-stu-id="7c194-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="7c194-112">Например, система может утверждать отчеты по расходам, имеющих общие суммы, которые меньше USD 100.</span><span class="sxs-lookup"><span data-stu-id="7c194-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="7c194-113">Выполните следующие действия, чтобы указать, когда система действует в отношении документа.</span><span class="sxs-lookup"><span data-stu-id="7c194-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="7c194-114">В левой области щелкните **Автоматические действия**.</span><span class="sxs-lookup"><span data-stu-id="7c194-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="7c194-115">Установите флажок **Включить автоматические действия**.</span><span class="sxs-lookup"><span data-stu-id="7c194-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="7c194-116">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="7c194-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="7c194-117">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="7c194-117">Enter a condition.</span></span>
5.  <span data-ttu-id="7c194-118">При необходимости введите дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="7c194-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="7c194-119">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7c194-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="7c194-120">Щелкните **Проверка** для открытия формы **Условия тестового workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="7c194-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="7c194-121">Выберите запись в области **Проверка условия** формы.</span><span class="sxs-lookup"><span data-stu-id="7c194-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="7c194-122">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="7c194-122">Click **Test**.</span></span> <span data-ttu-id="7c194-123">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="7c194-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="7c194-124">Щелкните **OK** или **Отмена** для возврата к форме **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7c194-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="7c194-125">Из списка **Действие автоматического завершения** выберите действие, которое система должна выполнить с документом.</span><span class="sxs-lookup"><span data-stu-id="7c194-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="7c194-126">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="7c194-126">Specify when notifications are sent</span></span>
<span data-ttu-id="7c194-127">Можно отправлять уведомления пользователям, когда документ утвержден, отклонен, делегирован, эскалирована или был запрос изменения.</span><span class="sxs-lookup"><span data-stu-id="7c194-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="7c194-128">Выполните следующие действия, чтобы определить, когда уведомления будут отправляться, и кому уведомления будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="7c194-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="7c194-129">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="7c194-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="7c194-130">Установите флажок рядом с событиями, для которых следует отправлять уведомления:</span><span class="sxs-lookup"><span data-stu-id="7c194-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="7c194-131">**Делегировать** – назначение документа другому пользователю для утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="7c194-132">**Эскалировать** - когда назначенный пользователь не выполнил действия с документом в отведенное время.</span><span class="sxs-lookup"><span data-stu-id="7c194-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="7c194-133">**Утвердить** - Когда документ был утвержден.</span><span class="sxs-lookup"><span data-stu-id="7c194-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="7c194-134">**Отклонить** - Когда документ был отклонен.</span><span class="sxs-lookup"><span data-stu-id="7c194-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="7c194-135">**Запросить изменение** — Когда назначенный пользователь запросил изменение представленного документа.</span><span class="sxs-lookup"><span data-stu-id="7c194-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="7c194-136">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="7c194-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="7c194-137">Выберите вкладку **Текст уведомления**.</span><span class="sxs-lookup"><span data-stu-id="7c194-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="7c194-138">В текстовом поле введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="7c194-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="7c194-139">Для персонализации текста можно вставить заполнители, которые будут заменены соответствующими данными, когда пользователи будут просматривать уведомление.</span><span class="sxs-lookup"><span data-stu-id="7c194-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="7c194-140">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="7c194-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="7c194-141">Щелкните в текстовом поле в местонахождение, в котором необходимо находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="7c194-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="7c194-142">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="7c194-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="7c194-143">В списке, который отображается выберите заполнитель, чтобы ввести.</span><span class="sxs-lookup"><span data-stu-id="7c194-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="7c194-144">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="7c194-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="7c194-145">Для добавления переводов уведомления, нажмите **Трансляции**.</span><span class="sxs-lookup"><span data-stu-id="7c194-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="7c194-146">В форме, которая отображается, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7c194-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="7c194-147">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="7c194-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="7c194-148">В списке, который отображается выберите язык в котором будет введен текст.</span><span class="sxs-lookup"><span data-stu-id="7c194-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="7c194-149">Введите нужный текст в текстовое поле **Переведенный текст**.</span><span class="sxs-lookup"><span data-stu-id="7c194-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="7c194-150">Чтобы настроить текст, введите Заполнители.</span><span class="sxs-lookup"><span data-stu-id="7c194-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="7c194-151">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="7c194-151">Click **Close**.</span></span>

8.  <span data-ttu-id="7c194-152">Выберите вкладку **Получатель**.</span><span class="sxs-lookup"><span data-stu-id="7c194-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="7c194-153">Задать кому отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="7c194-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="7c194-154">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для параметра перед тем как перейдите к шагу 10.</span><span class="sxs-lookup"><span data-stu-id="7c194-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7c194-155">Параметр</span><span class="sxs-lookup"><span data-stu-id="7c194-155">Option</span></span></th>
    <th><span data-ttu-id="7c194-156">Получатели уведомления.</span><span class="sxs-lookup"><span data-stu-id="7c194-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="7c194-157">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="7c194-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="7c194-158"><strong>Участник</strong></span><span class="sxs-lookup"><span data-stu-id="7c194-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="7c194-159">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="7c194-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="7c194-160">После выбора <strong>Участник</strong> перейдите на вкладку <strong>На основе роли</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c194-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="7c194-161">В списке <strong>Тип участника</strong> выберите тип группы или роли, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="7c194-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="7c194-162">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="7c194-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="7c194-163"><strong>Пользователь workflow-процесса</strong></span><span class="sxs-lookup"><span data-stu-id="7c194-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="7c194-164">Пользователи, участвующие в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="7c194-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="7c194-165">После выбора параметра <strong>Пользователь workflow-процесса</strong> перейдите на вкладку <strong>Пользователь workflow-процесса</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c194-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="7c194-166">В списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который участвует в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="7c194-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="7c194-167"><strong>Пользователь</strong></span><span class="sxs-lookup"><span data-stu-id="7c194-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="7c194-168">Определенные пользователи Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7c194-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="7c194-169">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c194-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="7c194-170">Список <strong>Доступные пользователи</strong> включает всех пользователей Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7c194-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="7c194-171">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>:.</span><span class="sxs-lookup"><span data-stu-id="7c194-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="7c194-172">Повторите шаги 3-9 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="7c194-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="7c194-173">Определение лица, ответственного за окончательное утверждение</span><span class="sxs-lookup"><span data-stu-id="7c194-173">Specify a final approver</span></span>
<span data-ttu-id="7c194-174">Можно предусмотреть утверждающее лицо для сценариев, когда утверждающие лицо — тот же человек, который отправил документ на утверждение.</span><span class="sxs-lookup"><span data-stu-id="7c194-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="7c194-175">Чтобы определить ответственного за окончательное утверждение, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7c194-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="7c194-176">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="7c194-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="7c194-177">Установите флажок **Использовать окончательного утверждающего лица**.</span><span class="sxs-lookup"><span data-stu-id="7c194-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="7c194-178">Из списка выберите пользователя, который будет выполнять окончательное утверждение.</span><span class="sxs-lookup"><span data-stu-id="7c194-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="7c194-179">Задание предельного срока</span><span class="sxs-lookup"><span data-stu-id="7c194-179">Set a time limit</span></span>
<span data-ttu-id="7c194-180">Выполните следующие действия, если процесс утверждения должна быть выполнена за определенное время.</span><span class="sxs-lookup"><span data-stu-id="7c194-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

| <span data-ttu-id="7c194-181">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7c194-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c194-182">Указанные в этих шагах параметры имеют больший приоритет, чем параметры, выбранные в областях **Назначение** и **Эскалация** для каждого шага утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="7c194-183">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="7c194-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="7c194-184">Установите флажок **Задать ограничение по времени для** **элемента workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="7c194-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="7c194-185">Укажите в поле **Продолжительность**, когда процесс утверждения должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="7c194-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="7c194-186">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="7c194-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="7c194-187">**Часы** — Введите число часов, в течение которых эта процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="7c194-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="7c194-188">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="7c194-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="7c194-189">**Дни** — Введите число дней, в течение которых эта процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="7c194-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="7c194-190">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="7c194-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="7c194-191">**Недели** — Введите число недель, в течение которых эта процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="7c194-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="7c194-192">**Месяцы** — Выберите день и неделю, когда процесс утверждения должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="7c194-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="7c194-193">Например, можно указать, что этот процесс утверждения должен быть завершен до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="7c194-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="7c194-194">**Годы** — Выберите день и неделю и месяц, когда процесс утверждения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="7c194-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="7c194-195">Например, можно указать, что этот процесс утверждения должен быть завершен до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="7c194-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="7c194-196">По истечении предельного срока система действует в отношении документа.</span><span class="sxs-lookup"><span data-stu-id="7c194-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="7c194-197">Из списка **Действие** выберите действие, которое должна выполнить система.</span><span class="sxs-lookup"><span data-stu-id="7c194-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="7c194-198">Задание диапазона возможных для пользователя действий</span><span class="sxs-lookup"><span data-stu-id="7c194-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="7c194-199">Когда документ назначен пользователю для утверждения, пользователь должен его обработать.</span><span class="sxs-lookup"><span data-stu-id="7c194-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="7c194-200">Выполните следующие действия, чтобы определить, какие действия пользователь может предпринять на отправленном документе.</span><span class="sxs-lookup"><span data-stu-id="7c194-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="7c194-201">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="7c194-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="7c194-202">Установите флажок **Утвердить**, если требуется, чтобы пользователь мог утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="7c194-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="7c194-203">Установите флажок **Отклонить**, если требуется, чтобы пользователь мог Отклонить документ.</span><span class="sxs-lookup"><span data-stu-id="7c194-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="7c194-204">Установите флажок **Запросить изменение**, если требуется, чтобы пользователи могли запрашивать изменение документа.</span><span class="sxs-lookup"><span data-stu-id="7c194-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="7c194-205">Установите флажок **Делегировать**, если пользователь может назначить документ другому пользователю на утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="7c194-206">**Примечание**. Флажок **Включение действий из списка работ на корпоративном портале** устарел.</span><span class="sxs-lookup"><span data-stu-id="7c194-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="7c194-207">Настройка шагов утверждения</span><span class="sxs-lookup"><span data-stu-id="7c194-207">Configure the approval steps</span></span>
<span data-ttu-id="7c194-208">Процесс утверждения состоит из шагов утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="7c194-209">Выполните следующую процедуру, чтобы добавить шаги процесса утверждения и настроить шаги.</span><span class="sxs-lookup"><span data-stu-id="7c194-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="7c194-210">В редакторе workflow-процесс, дважды щелкните процесс утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="7c194-211">Редактор workflow-процесс отображает шаги процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="7c194-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="7c194-212">Для добавления шага утверждения, перетащите шаг из зоны **Элементы workflow-процесса** на холст.</span><span class="sxs-lookup"><span data-stu-id="7c194-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="7c194-213">Для настройки стадии утверждения см. раздел [Настройка стадии утверждения](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="7c194-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






