---
title: "Настройка ручного решения в workflow-процессе"
description: "В этом разделе описывается, как настроить свойства ручного решения."
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
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c61c3c4fd3c888888e7ac8cc8fc8275c15ff4692
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="configure-a-manual-decision-in-a-workflow"></a><span data-ttu-id="2ab69-103">Настройка ручного решения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2ab69-103">Configure a manual decision in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ab69-104">В этом разделе описывается, как настроить свойства ручного решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="2ab69-105">Чтобы настроить ручное решение, в редакторе workflow-процессов щелкните правой кнопкой мыши ручное решение и выберите **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2ab69-106">Затем используйте следующие процедуры для настройки свойств ручного решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="2ab69-107">Наименование решения</span><span class="sxs-lookup"><span data-stu-id="2ab69-107">Name the decision</span></span>
<span data-ttu-id="2ab69-108">Чтобы ввести имя ручного решения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2ab69-108">Follow these steps to enter a name for the manual decision.</span></span>

1.  <span data-ttu-id="2ab69-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="2ab69-110">В поле **Имя** введите уникальное имя для ручного решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2ab69-111">Ввод строки темы и инструкций</span><span class="sxs-lookup"><span data-stu-id="2ab69-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="2ab69-112">Пользователям, назначенным ручному решению, должны быть предоставлены строка темы и инструкции.</span><span class="sxs-lookup"><span data-stu-id="2ab69-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="2ab69-113">Например, при настройке решения для заявок на закупку пользователь, который назначается решению, увидит строку темы и инструкции на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2ab69-114">Строка темы будет отображаться в строке сообщений на странице.</span><span class="sxs-lookup"><span data-stu-id="2ab69-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2ab69-115">Пользователь может щелкнуть значок в строке сообщений, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="2ab69-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="2ab69-116">Чтобы ввести строку темы и инструкции, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2ab69-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="2ab69-117">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="2ab69-118">На вкладке **Инструкции** в поле **Тема рабочего элемента** введите строку темы.</span><span class="sxs-lookup"><span data-stu-id="2ab69-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="2ab69-119">Для того, чтобы персонализовать строку уведомления можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="2ab69-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2ab69-120">Заполнители заменяются соответствующей информацией, когда строка темы отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="2ab69-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2ab69-121">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="2ab69-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="2ab69-122">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="2ab69-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="2ab69-123">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="2ab69-124">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="2ab69-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="2ab69-125">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="2ab69-126">Для добавления переводов строки темы выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ab69-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="2ab69-127">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="2ab69-128">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="2ab69-129">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="2ab69-130">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="2ab69-131">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="2ab69-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="2ab69-132">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-132">Click **Close**.</span></span>

5.  <span data-ttu-id="2ab69-133">В поле **Инструкции рабочего элемента** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="2ab69-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="2ab69-134">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="2ab69-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2ab69-135">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="2ab69-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2ab69-136">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="2ab69-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="2ab69-137">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="2ab69-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="2ab69-138">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="2ab69-139">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="2ab69-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="2ab69-140">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="2ab69-141">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ab69-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="2ab69-142">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="2ab69-143">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="2ab69-144">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="2ab69-145">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="2ab69-146">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 6.</span><span class="sxs-lookup"><span data-stu-id="2ab69-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="2ab69-147">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="2ab69-148">Укажите возможные результаты решения</span><span class="sxs-lookup"><span data-stu-id="2ab69-148">Specify the possible outcomes of a decision</span></span>
<span data-ttu-id="2ab69-149">Обычно, когда документ назначен лицу, принимающему решения, ему задается вопрос.</span><span class="sxs-lookup"><span data-stu-id="2ab69-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="2ab69-150">Ответ на этот вопрос обычно **Да** или **Нет** либо **Истина** или **Ложь**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="2ab69-151">Выполните следующие шаги, чтобы определить возможные результаты ручного решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1.  <span data-ttu-id="2ab69-152">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-152">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="2ab69-153">На вкладке **Результаты** в поле **Результат 1** введите имя результата или параметр.</span><span class="sxs-lookup"><span data-stu-id="2ab69-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3.  <span data-ttu-id="2ab69-154">Для добавления переводов результата выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ab69-154">To add translations of the outcome, follow these steps:</span></span>
    1.  <span data-ttu-id="2ab69-155">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-155">Click **Translations**.</span></span>
    2.  <span data-ttu-id="2ab69-156">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-156">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="2ab69-157">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="2ab69-158">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-158">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="2ab69-159">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-159">Click **Close**.</span></span>

4.  <span data-ttu-id="2ab69-160">В поле **Результат 2** введите имя результата или параметра.</span><span class="sxs-lookup"><span data-stu-id="2ab69-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5.  <span data-ttu-id="2ab69-161">Для добавления переводов результата выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ab69-161">To add translations of the outcome, follow these steps:</span></span>
    1.  <span data-ttu-id="2ab69-162">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-162">Click **Translations**.</span></span>
    2.  <span data-ttu-id="2ab69-163">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-163">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="2ab69-164">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="2ab69-165">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-165">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="2ab69-166">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2ab69-167">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="2ab69-167">Specify when notifications are sent</span></span>
<span data-ttu-id="2ab69-168">Можно отправлять уведомления людям, когда решение было сделано, делегировано или эскалировано.</span><span class="sxs-lookup"><span data-stu-id="2ab69-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="2ab69-169">Выполните следующие действия, чтобы определить, когда уведомления будут отправляться, и кому уведомления будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="2ab69-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="2ab69-170">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-170">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="2ab69-171">Установите флажок рядом с событиями, для которых следует отправлять уведомления:</span><span class="sxs-lookup"><span data-stu-id="2ab69-171">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="2ab69-172">**\[Выбор 1\]** — назначенный пользователь выбрал **\[Выбор 1\]**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    -   <span data-ttu-id="2ab69-173">**\[Выбор 2\]** — назначенный пользователь выбрал **\[Выбор 2\]**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    -   <span data-ttu-id="2ab69-174">**Делегировать** — назначенный пользователь назначает решение другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="2ab69-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    -   <span data-ttu-id="2ab69-175">**Эскалировать** — назначенный пользователь не принял решение в отведенное время.</span><span class="sxs-lookup"><span data-stu-id="2ab69-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3.  <span data-ttu-id="2ab69-176">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="2ab69-176">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="2ab69-177">На вкладке **Текст уведомления** в текстовом поле введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="2ab69-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="2ab69-178">Для того, чтобы персонализовать уведомление можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="2ab69-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="2ab69-179">Заполнители заменяются соответствующей информацией, когда уведомление отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="2ab69-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="2ab69-180">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="2ab69-180">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="2ab69-181">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="2ab69-181">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="2ab69-182">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-182">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="2ab69-183">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="2ab69-183">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="2ab69-184">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-184">Click **Insert**.</span></span>

6.  <span data-ttu-id="2ab69-185">Для добавления переводов уведомления выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ab69-185">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="2ab69-186">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-186">Click **Translations**.</span></span>
    2.  <span data-ttu-id="2ab69-187">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-187">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="2ab69-188">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="2ab69-189">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="2ab69-189">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="2ab69-190">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="2ab69-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="2ab69-191">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-191">Click **Close**.</span></span>

7.  <span data-ttu-id="2ab69-192">На вкладке **Получатель** укажите, кому отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="2ab69-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="2ab69-193">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 8.</span><span class="sxs-lookup"><span data-stu-id="2ab69-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="2ab69-194">Параметр</span><span class="sxs-lookup"><span data-stu-id="2ab69-194">Option</span></span></th>
    <th><span data-ttu-id="2ab69-195">Получатели уведомления.</span><span class="sxs-lookup"><span data-stu-id="2ab69-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="2ab69-196">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="2ab69-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="2ab69-197">Участник</span><span class="sxs-lookup"><span data-stu-id="2ab69-197">Participant</span></span></td>
    <td><span data-ttu-id="2ab69-198">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="2ab69-198">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="2ab69-199">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="2ab69-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2ab69-200">В списке <strong>Участник</strong> выберите группу, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="2ab69-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2ab69-201">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2ab69-201">Workflow user</span></span></td>
    <td><span data-ttu-id="2ab69-202">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2ab69-202">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="2ab69-203">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="2ab69-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="2ab69-204">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2ab69-204">User</span></span></td>
    <td><span data-ttu-id="2ab69-205">Определенные пользователи Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ab69-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="2ab69-206">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2ab69-207">Список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ab69-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2ab69-208">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="2ab69-209">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="2ab69-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="2ab69-210">Назначение решения</span><span class="sxs-lookup"><span data-stu-id="2ab69-210">Assign a decision</span></span>
<span data-ttu-id="2ab69-211">Чтобы указать, кому требуется назначить ручное решение, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2ab69-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1.  <span data-ttu-id="2ab69-212">В левой области щелкните **Назначение**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-212">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="2ab69-213">Во вкладке **Тип назначения** выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 3.</span><span class="sxs-lookup"><span data-stu-id="2ab69-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="2ab69-214">Параметр</span><span class="sxs-lookup"><span data-stu-id="2ab69-214">Option</span></span></th>
    <th><span data-ttu-id="2ab69-215">Пользователи, которым назначено решение</span><span class="sxs-lookup"><span data-stu-id="2ab69-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="2ab69-216">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="2ab69-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="2ab69-217">Участник</span><span class="sxs-lookup"><span data-stu-id="2ab69-217">Participant</span></span></td>
    <td><span data-ttu-id="2ab69-218">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="2ab69-218">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="2ab69-219">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется назначить решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2ab69-220">В списке <strong>Участник</strong> выберите группу или роль, которой требуется назначить решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2ab69-221">Иерархия</span><span class="sxs-lookup"><span data-stu-id="2ab69-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="2ab69-222">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="2ab69-222">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="2ab69-223">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, которой требуется назначить решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2ab69-224">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="2ab69-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2ab69-225">Эти имена представляют пользователей, которым можно назначить решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="2ab69-226">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="2ab69-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2ab69-227">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2ab69-228">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2ab69-229">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="2ab69-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="2ab69-230">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должно быть назначено решение:</span><span class="sxs-lookup"><span data-stu-id="2ab69-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2ab69-231"><strong>Назначить всем найденным пользователям</strong> — решение назначается всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2ab69-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2ab69-232"><strong>Назначить только последнему найденному пользователю</strong> — решение назначается только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2ab69-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2ab69-233"><strong>Исключить пользователей, для которых выполняется следующее</strong> — решение не назначается пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="2ab69-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2ab69-234">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="2ab69-235">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2ab69-235">Workflow user</span></span></td>
    <td><span data-ttu-id="2ab69-236">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2ab69-236">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="2ab69-237">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="2ab69-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2ab69-238">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2ab69-238">User</span></span></td>
    <td><span data-ttu-id="2ab69-239">Определенные пользователи Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ab69-239">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="2ab69-240">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2ab69-241">Список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ab69-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2ab69-242">Выберите пользователей, которым требуется назначить решение, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="2ab69-243">Очередь</span><span class="sxs-lookup"><span data-stu-id="2ab69-243">Queue</span></span></td>
    <td><span data-ttu-id="2ab69-244">Очередь задач</span><span class="sxs-lookup"><span data-stu-id="2ab69-244">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="2ab69-245">После выбора значения в поле <strong>Очередь</strong> перейдите на вкладку <strong>На основе очереди</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="2ab69-246">Для назначения Решение к конкретной очереди, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2ab69-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2ab69-247">В списке <strong>Тип очереди</strong> выберите <strong>Очереди задач</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2ab69-248">В списке <strong>Имя очереди</strong> выберите очередь.</span><span class="sxs-lookup"><span data-stu-id="2ab69-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="2ab69-249">Если определенное условие должно указывать, в какую очередь Решение назначается, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="2ab69-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2ab69-250">В списке <strong>Тип очереди</strong> выберите <strong>Зависимые очереди задач</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2ab69-251">В списке <strong>Имя очереди</strong> выберите <strong>Зависимая очередь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="2ab69-252">
    <strong>Примечание.</strong> Этот параметр используется только для нескольких workflow-процессов, таких как управление обращениями.</span><span class="sxs-lookup"><span data-stu-id="2ab69-252">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="2ab69-253">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени отводится пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2ab69-254">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2ab69-254">Select one of the following options:</span></span>
    -   <span data-ttu-id="2ab69-255">**Часы** — введите число часов, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2ab69-256">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="2ab69-257">**Дни** — введите число дней, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2ab69-258">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="2ab69-259">**Недели** — введите число недель, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    -   <span data-ttu-id="2ab69-260">**Месяцы** — введите день и неделю, к которой пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2ab69-261">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="2ab69-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="2ab69-262">**Годы** — введите день, неделю и месяц, к которым пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2ab69-263">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="2ab69-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="2ab69-264">Если пользователь не принял решение за выделенное время, решение считается просроченным.</span><span class="sxs-lookup"><span data-stu-id="2ab69-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2ab69-265">Просроченное решение эскалируется на основе параметров, выбранных в области **Эскалация** этой страницы.</span><span class="sxs-lookup"><span data-stu-id="2ab69-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="2ab69-266">Задание действий в случае, если Решение просрочена</span><span class="sxs-lookup"><span data-stu-id="2ab69-266">Specify what happens when a decision is overdue</span></span>
<span data-ttu-id="2ab69-267">Если пользователь не принял решение за выделенное время, решение считается просроченным.</span><span class="sxs-lookup"><span data-stu-id="2ab69-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2ab69-268">Просроченное решение можно эскалировать или автоматически назначить другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="2ab69-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="2ab69-269">Выполните следующие действия, чтобы эскалировать просроченное решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="2ab69-270">В левой области щелкните **Эскалация**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2ab69-271">Установите флажок **Использовать маршрут эскалации**, чтобы создать маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2ab69-272">Система автоматически назначает решение пользователям, перечисленным в маршруте эскалации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2ab69-273">Например, в следующей таблице представляет собой маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-273">For example, the following table represents an escalation path.</span></span>

   | <span data-ttu-id="2ab69-274">Последовательность</span><span class="sxs-lookup"><span data-stu-id="2ab69-274">Sequence</span></span> | <span data-ttu-id="2ab69-275">Путь эскалации</span><span class="sxs-lookup"><span data-stu-id="2ab69-275">Escalation path</span></span>            |
   |----------|----------------------------|
   | <span data-ttu-id="2ab69-276">1</span><span class="sxs-lookup"><span data-stu-id="2ab69-276">1</span></span>        | <span data-ttu-id="2ab69-277">Назначит: Дарье</span><span class="sxs-lookup"><span data-stu-id="2ab69-277">Assign to: Donna</span></span>           |
   | <span data-ttu-id="2ab69-278">2</span><span class="sxs-lookup"><span data-stu-id="2ab69-278">2</span></span>        | <span data-ttu-id="2ab69-279">Назначить: Ирине</span><span class="sxs-lookup"><span data-stu-id="2ab69-279">Assign to: Erin</span></span>            |
   | <span data-ttu-id="2ab69-280">3</span><span class="sxs-lookup"><span data-stu-id="2ab69-280">3</span></span>        | <span data-ttu-id="2ab69-281">Заключительное действие: \[Выбор 1\]</span><span class="sxs-lookup"><span data-stu-id="2ab69-281">Final action: \[Choice 1\]</span></span> |

   <span data-ttu-id="2ab69-282">В этом примере просроченный решение будет автоматически назначена Дарье.</span><span class="sxs-lookup"><span data-stu-id="2ab69-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="2ab69-283">Если Дарья не примет решение в отведенные сроки, система назначит решение Ирине.</span><span class="sxs-lookup"><span data-stu-id="2ab69-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="2ab69-284">Если Ирина не примет решение в отведенные сроки, система выберет **\[Выбор 1\]** в качестве решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>
3. <span data-ttu-id="2ab69-285">Чтобы добавить пользователя в маршрут эскалации, щелкните **Добавить эскалирование**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2ab69-286">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="2ab69-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th><span data-ttu-id="2ab69-287">Параметр</span><span class="sxs-lookup"><span data-stu-id="2ab69-287">Option</span></span></th>
   <th><span data-ttu-id="2ab69-288">Пользователи, которым эскалируется решение</span><span class="sxs-lookup"><span data-stu-id="2ab69-288">Users that the decision is escalated to</span></span></th>
   <th><span data-ttu-id="2ab69-289">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="2ab69-289">Additional steps</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="2ab69-290">Иерархия</span><span class="sxs-lookup"><span data-stu-id="2ab69-290">Hierarchy</span></span></td>
   <td><span data-ttu-id="2ab69-291">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="2ab69-291">Users in a specific organizational hierarchy</span></span></td>
   <td><ol>
   <li><span data-ttu-id="2ab69-292">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, в которую требуется эскалировать решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
   <li><span data-ttu-id="2ab69-293">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="2ab69-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2ab69-294">Эти имена представляют пользователей, которым может быть эскалировано решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="2ab69-295">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="2ab69-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
   <li><span data-ttu-id="2ab69-296">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
   <li><span data-ttu-id="2ab69-297">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2ab69-298">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="2ab69-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
   </ol></li>
   <li><span data-ttu-id="2ab69-299">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должно быть эскалировано решение:</span><span class="sxs-lookup"><span data-stu-id="2ab69-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
   <li><span data-ttu-id="2ab69-300"><strong>Назначить всем найденным пользователям</strong> — решение эскалируется всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2ab69-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
   <li><span data-ttu-id="2ab69-301"><strong>Назначить только последнему найденному пользователю</strong> — решение эскалируется только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2ab69-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
   <li><span data-ttu-id="2ab69-302"><strong>Исключить пользователей, для которых выполняется следующее:</strong> — решение не эскалируется пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="2ab69-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2ab69-303">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
   </ul></li>
   </ol></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="2ab69-304">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="2ab69-304">Workflow user</span></span></td>
   <td><span data-ttu-id="2ab69-305">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="2ab69-305">Users in the current workflow</span></span></td>
   <td><ul>
   <li><span data-ttu-id="2ab69-306">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="2ab69-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td><span data-ttu-id="2ab69-307">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2ab69-307">User</span></span></td>
   <td><span data-ttu-id="2ab69-308">Определенные пользователи Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ab69-308">Specific Finance and Operations users</span></span></td>
   <td><ol>
   <li><span data-ttu-id="2ab69-309">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
   <li><span data-ttu-id="2ab69-310">Список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ab69-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="2ab69-311">Выберите пользователей, которым требуется эскалировать решение, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="2ab69-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

4. <span data-ttu-id="2ab69-312">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени отводится пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2ab69-313">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2ab69-313">Select one of the following options:</span></span>
   -   <span data-ttu-id="2ab69-314">**Часы** — введите число часов, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2ab69-315">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
   -   <span data-ttu-id="2ab69-316">**Дни** — введите число дней, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2ab69-317">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
   -   <span data-ttu-id="2ab69-318">**Недели** — введите число недель, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="2ab69-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
   -   <span data-ttu-id="2ab69-319">**Месяцы** — введите день и неделю, к которой пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2ab69-320">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="2ab69-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
   -   <span data-ttu-id="2ab69-321">**Годы** — введите день, неделю и месяц, к которым пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2ab69-322">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="2ab69-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2ab69-323">Повторите шаги с 3 по 4 для каждого пользователя, которого следует добавить в маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2ab69-324">можно изменить порядок пользователей.</span><span class="sxs-lookup"><span data-stu-id="2ab69-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="2ab69-325">Если пользователи, перечисленные в пути эскалации, не приняли решение за отведенное время, система примет решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="2ab69-326">Чтобы указать параметр, который выбирает система, выберите строку **Действие** и на вкладке **Конечное действие** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="2ab69-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="2ab69-327">Задание предельного срока</span><span class="sxs-lookup"><span data-stu-id="2ab69-327">Set a time limit</span></span>
<span data-ttu-id="2ab69-328">Выполните следующие действия, если решение должна быть принято за определенное время.</span><span class="sxs-lookup"><span data-stu-id="2ab69-328">Follow these steps if the decision must be made in a specific time.</span></span> <span data-ttu-id="2ab69-329">**Примечание.** Параметры, выбранные в этой процедуре, переопределяют параметры, выбранные в областях **Назначение** и **Эскалация** страницы.</span><span class="sxs-lookup"><span data-stu-id="2ab69-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="2ab69-330">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="2ab69-331">Установите флажок **Задать ограничение по времени для элемента workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="2ab69-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="2ab69-332">В поле **Продолжительность** укажите, когда должно быть принято это решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="2ab69-333">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="2ab69-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="2ab69-334">**Часы**— введите число часов.</span><span class="sxs-lookup"><span data-stu-id="2ab69-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="2ab69-335">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="2ab69-336">**Дни** — введите число дней.</span><span class="sxs-lookup"><span data-stu-id="2ab69-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="2ab69-337">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="2ab69-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="2ab69-338">**Недели** — введите число недель.</span><span class="sxs-lookup"><span data-stu-id="2ab69-338">**Weeks** – Enter the number of weeks.</span></span>
    -   <span data-ttu-id="2ab69-339">**Месяцы** — выберите день и неделю, к которым должно быть принято решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="2ab69-340">Например, можно указать, что решение должно быть принято до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="2ab69-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="2ab69-341">**Годы** — выберите день, неделю и месяц, к которым должно быть принято решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="2ab69-342">Например, можно указать, что решение должно быть принято до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="2ab69-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="2ab69-343">По истечении предельного срока система принимает решение.</span><span class="sxs-lookup"><span data-stu-id="2ab69-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="2ab69-344">В списке **Действие** выберите параметр, который должна выбрать система.</span><span class="sxs-lookup"><span data-stu-id="2ab69-344">In the **Action** list, select the option that the system should select.</span></span>





