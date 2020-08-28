---
title: Настройка ручных решений в workflow-процессе
description: В этом разделе описывается, как настроить свойства ручного решения.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 859e74b869fcf9b8a886f27f67f51bdf28819979
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698251"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="740f9-103">Настройка ручных решений в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="740f9-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="740f9-104">В этом разделе описывается, как настроить свойства ручного решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="740f9-105">Чтобы настроить ручное решение, в редакторе workflow-процессов щелкните правой кнопкой мыши ручное решение и выберите **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="740f9-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="740f9-106">Затем используйте следующие процедуры для настройки свойств ручного решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="740f9-107">Наименование решения</span><span class="sxs-lookup"><span data-stu-id="740f9-107">Name the decision</span></span>

<span data-ttu-id="740f9-108">Чтобы ввести имя ручного решения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="740f9-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="740f9-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="740f9-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="740f9-110">В поле **Имя** введите уникальное имя для ручного решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="740f9-111">Ввод строки темы и инструкций</span><span class="sxs-lookup"><span data-stu-id="740f9-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="740f9-112">Пользователям, назначенным ручному решению, должны быть предоставлены строка темы и инструкции.</span><span class="sxs-lookup"><span data-stu-id="740f9-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="740f9-113">Например, при настройке решения для заявок на закупку пользователь, который назначается решению, увидит строку темы и инструкции на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="740f9-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="740f9-114">Строка темы будет отображаться в строке сообщений на странице.</span><span class="sxs-lookup"><span data-stu-id="740f9-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="740f9-115">Пользователь может щелкнуть значок в строке сообщений, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="740f9-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="740f9-116">Чтобы ввести строку темы и инструкции, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="740f9-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="740f9-117">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="740f9-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="740f9-118">На вкладке **Инструкции** в поле **Тема рабочего элемента** введите строку темы.</span><span class="sxs-lookup"><span data-stu-id="740f9-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="740f9-119">Для того, чтобы персонализовать строку уведомления можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="740f9-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="740f9-120">Заполнители заменяются соответствующей информацией, когда строка темы отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="740f9-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="740f9-121">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="740f9-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="740f9-122">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="740f9-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="740f9-123">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="740f9-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="740f9-124">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="740f9-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="740f9-125">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-125">Click **Insert**.</span></span>

4. <span data-ttu-id="740f9-126">Для добавления переводов строки темы выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="740f9-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="740f9-127">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="740f9-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="740f9-128">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="740f9-129">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="740f9-130">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="740f9-131">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="740f9-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="740f9-132">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="740f9-132">Click **Close**.</span></span>

5. <span data-ttu-id="740f9-133">В поле **Инструкции рабочего элемента** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="740f9-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="740f9-134">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="740f9-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="740f9-135">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="740f9-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="740f9-136">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="740f9-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="740f9-137">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="740f9-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="740f9-138">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="740f9-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="740f9-139">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="740f9-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="740f9-140">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-140">Click **Insert**.</span></span>

7. <span data-ttu-id="740f9-141">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="740f9-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="740f9-142">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="740f9-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="740f9-143">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="740f9-144">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="740f9-145">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="740f9-146">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 6.</span><span class="sxs-lookup"><span data-stu-id="740f9-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="740f9-147">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="740f9-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="740f9-148">Укажите возможные результаты решения</span><span class="sxs-lookup"><span data-stu-id="740f9-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="740f9-149">Обычно, когда документ назначен лицу, принимающему решения, ему задается вопрос.</span><span class="sxs-lookup"><span data-stu-id="740f9-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="740f9-150">Ответ на этот вопрос обычно **Да** или **Нет** либо **Истина** или **Ложь**.</span><span class="sxs-lookup"><span data-stu-id="740f9-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="740f9-151">Выполните следующие шаги, чтобы определить возможные результаты ручного решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="740f9-152">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="740f9-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="740f9-153">На вкладке **Результаты** в поле **Результат 1** введите имя результата или параметр.</span><span class="sxs-lookup"><span data-stu-id="740f9-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="740f9-154">Для добавления переводов результата выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="740f9-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="740f9-155">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="740f9-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="740f9-156">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="740f9-157">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="740f9-158">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="740f9-159">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="740f9-159">Click **Close**.</span></span>

4. <span data-ttu-id="740f9-160">В поле **Результат 2** введите имя результата или параметра.</span><span class="sxs-lookup"><span data-stu-id="740f9-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="740f9-161">Для добавления переводов результата выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="740f9-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="740f9-162">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="740f9-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="740f9-163">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="740f9-164">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="740f9-165">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="740f9-166">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="740f9-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="740f9-167">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="740f9-167">Specify when notifications are sent</span></span>

<span data-ttu-id="740f9-168">Можно отправлять уведомления людям, когда решение было сделано, делегировано или эскалировано.</span><span class="sxs-lookup"><span data-stu-id="740f9-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="740f9-169">Выполните следующие действия, чтобы определить, когда уведомления будут отправляться, и кому уведомления будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="740f9-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="740f9-170">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="740f9-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="740f9-171">Установите флажок рядом с событиями, для которых следует отправлять уведомления:</span><span class="sxs-lookup"><span data-stu-id="740f9-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="740f9-172">**\[Выбор 1\]** — назначенный пользователь выбрал **\[Выбор 1\]**.</span><span class="sxs-lookup"><span data-stu-id="740f9-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="740f9-173">**\[Выбор 2\]** — назначенный пользователь выбрал **\[Выбор 2\]**.</span><span class="sxs-lookup"><span data-stu-id="740f9-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="740f9-174">**Делегировать** — назначенный пользователь назначает решение другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="740f9-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="740f9-175">**Эскалировать** — назначенный пользователь не принял решение в отведенное время.</span><span class="sxs-lookup"><span data-stu-id="740f9-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="740f9-176">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="740f9-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="740f9-177">На вкладке **Текст уведомления** в текстовом поле введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="740f9-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="740f9-178">Для того, чтобы персонализовать уведомление можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="740f9-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="740f9-179">Заполнители заменяются соответствующей информацией, когда уведомление отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="740f9-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="740f9-180">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="740f9-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="740f9-181">В текстовом поле щелкните в том месте, в котором должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="740f9-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="740f9-182">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="740f9-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="740f9-183">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="740f9-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="740f9-184">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-184">Click **Insert**.</span></span>

6. <span data-ttu-id="740f9-185">Для добавления переводов уведомления выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="740f9-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="740f9-186">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="740f9-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="740f9-187">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="740f9-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="740f9-188">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="740f9-189">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="740f9-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="740f9-190">Чтобы персонализировать текст, можно вставить заполнители, как описано на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="740f9-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="740f9-191">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="740f9-191">Click **Close**.</span></span>

7. <span data-ttu-id="740f9-192">На вкладке **Получатель** укажите, кому отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="740f9-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="740f9-193">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 8.</span><span class="sxs-lookup"><span data-stu-id="740f9-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="740f9-194">Параметр</span><span class="sxs-lookup"><span data-stu-id="740f9-194">Option</span></span></th>
    <th><span data-ttu-id="740f9-195">Получатели уведомления.</span><span class="sxs-lookup"><span data-stu-id="740f9-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="740f9-196">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="740f9-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="740f9-197">Участник</span><span class="sxs-lookup"><span data-stu-id="740f9-197">Participant</span></span></td>
    <td><span data-ttu-id="740f9-198">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="740f9-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-199">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="740f9-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="740f9-200">В списке <strong>Участник</strong> выберите группу, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="740f9-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-201">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="740f9-201">Workflow user</span></span></td>
    <td><span data-ttu-id="740f9-202">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="740f9-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="740f9-203">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="740f9-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-204">Пользователь</span><span class="sxs-lookup"><span data-stu-id="740f9-204">User</span></span></td>
    <td><span data-ttu-id="740f9-205">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="740f9-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-206">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="740f9-207">Список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="740f9-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="740f9-208">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="740f9-209">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="740f9-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="740f9-210">Назначение решения</span><span class="sxs-lookup"><span data-stu-id="740f9-210">Assign a decision</span></span>

<span data-ttu-id="740f9-211">Чтобы указать, кому требуется назначить ручное решение, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="740f9-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="740f9-212">В левой области щелкните **Назначение**.</span><span class="sxs-lookup"><span data-stu-id="740f9-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="740f9-213">Во вкладке **Тип назначения** выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 3.</span><span class="sxs-lookup"><span data-stu-id="740f9-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="740f9-214">Параметр</span><span class="sxs-lookup"><span data-stu-id="740f9-214">Option</span></span></th>
    <th><span data-ttu-id="740f9-215">Пользователи, которым назначено решение</span><span class="sxs-lookup"><span data-stu-id="740f9-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="740f9-216">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="740f9-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="740f9-217">Участник</span><span class="sxs-lookup"><span data-stu-id="740f9-217">Participant</span></span></td>
    <td><span data-ttu-id="740f9-218">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="740f9-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-219">После выбора значения в поле <strong>Участник</strong> на вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется назначить решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="740f9-220">В списке <strong>Участник</strong> выберите группу или роль, которой требуется назначить решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-221">Иерархия</span><span class="sxs-lookup"><span data-stu-id="740f9-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="740f9-222">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="740f9-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-223">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, которой требуется назначить решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="740f9-224">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="740f9-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="740f9-225">Эти имена представляют пользователей, которым можно назначить решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="740f9-226">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="740f9-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="740f9-227">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="740f9-228">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="740f9-229">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="740f9-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="740f9-230">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должно быть назначено решение:</span><span class="sxs-lookup"><span data-stu-id="740f9-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="740f9-231"><strong>Назначить всем найденным пользователям</strong> — решение назначается всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="740f9-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="740f9-232"><strong>Назначить только последнему найденному пользователю</strong> — решение назначается только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="740f9-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="740f9-233"><strong>Исключить пользователей, для которых выполняется следующее</strong> — решение не назначается пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="740f9-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="740f9-234">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-235">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="740f9-235">Workflow user</span></span></td>
    <td><span data-ttu-id="740f9-236">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="740f9-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="740f9-237">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="740f9-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-238">Пользователь</span><span class="sxs-lookup"><span data-stu-id="740f9-238">User</span></span></td>
    <td><span data-ttu-id="740f9-239">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="740f9-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-240">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="740f9-241">Список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="740f9-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="740f9-242">Выберите пользователей, которым требуется назначить решение, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="740f9-243">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени отводится пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="740f9-244">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="740f9-244">Select one of the following options:</span></span>

    - <span data-ttu-id="740f9-245">**Часы** — введите число часов, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="740f9-246">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="740f9-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="740f9-247">**Дни** — введите число дней, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="740f9-248">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="740f9-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="740f9-249">**Недели** — введите число недель, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="740f9-250">**Месяцы** — введите день и неделю, к которой пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="740f9-251">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="740f9-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="740f9-252">**Годы** — введите день, неделю и месяц, к которым пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="740f9-253">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="740f9-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="740f9-254">Если пользователь не принял решение за выделенное время, решение считается просроченным.</span><span class="sxs-lookup"><span data-stu-id="740f9-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="740f9-255">Просроченное решение эскалируется на основе параметров, выбранных в области **Эскалация** этой страницы.</span><span class="sxs-lookup"><span data-stu-id="740f9-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="740f9-256">Задание действий в случае, если Решение просрочена</span><span class="sxs-lookup"><span data-stu-id="740f9-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="740f9-257">Если пользователь не принял решение за выделенное время, решение считается просроченным.</span><span class="sxs-lookup"><span data-stu-id="740f9-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="740f9-258">Просроченное решение можно эскалировать или автоматически назначить другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="740f9-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="740f9-259">Выполните следующие действия, чтобы эскалировать просроченное решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="740f9-260">В левой области щелкните **Эскалация**.</span><span class="sxs-lookup"><span data-stu-id="740f9-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="740f9-261">Установите флажок **Использовать маршрут эскалации**, чтобы создать маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="740f9-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="740f9-262">Система автоматически назначает решение пользователям, перечисленным в маршруте эскалации.</span><span class="sxs-lookup"><span data-stu-id="740f9-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="740f9-263">Например, в следующей таблице представляет собой маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="740f9-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="740f9-264">Последовательность</span><span class="sxs-lookup"><span data-stu-id="740f9-264">Sequence</span></span> | <span data-ttu-id="740f9-265">Путь эскалации</span><span class="sxs-lookup"><span data-stu-id="740f9-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="740f9-266">1</span><span class="sxs-lookup"><span data-stu-id="740f9-266">1</span></span>        | <span data-ttu-id="740f9-267">Назначит: Дарье</span><span class="sxs-lookup"><span data-stu-id="740f9-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="740f9-268">2</span><span class="sxs-lookup"><span data-stu-id="740f9-268">2</span></span>        | <span data-ttu-id="740f9-269">Назначить: Ирине</span><span class="sxs-lookup"><span data-stu-id="740f9-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="740f9-270">3</span><span class="sxs-lookup"><span data-stu-id="740f9-270">3</span></span>        | <span data-ttu-id="740f9-271">Заключительное действие: \[Выбор 1\]</span><span class="sxs-lookup"><span data-stu-id="740f9-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="740f9-272">В этом примере просроченный решение будет автоматически назначена Дарье.</span><span class="sxs-lookup"><span data-stu-id="740f9-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="740f9-273">Если Дарья не примет решение в отведенные сроки, система назначит решение Ирине.</span><span class="sxs-lookup"><span data-stu-id="740f9-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="740f9-274">Если Ирина не примет решение в отведенные сроки, система выберет **\[Выбор 1\]** в качестве решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="740f9-275">Чтобы добавить пользователя в маршрут эскалации, щелкните **Добавить эскалирование**.</span><span class="sxs-lookup"><span data-stu-id="740f9-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="740f9-276">Выберите один из параметров в следующей таблице, а затем выполните дополнительные шаги для этого параметра, перед тем как перейти к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="740f9-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="740f9-277">Параметр</span><span class="sxs-lookup"><span data-stu-id="740f9-277">Option</span></span></th>
    <th><span data-ttu-id="740f9-278">Пользователи, которым эскалируется решение</span><span class="sxs-lookup"><span data-stu-id="740f9-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="740f9-279">Дополнительные шаги</span><span class="sxs-lookup"><span data-stu-id="740f9-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="740f9-280">Иерархия</span><span class="sxs-lookup"><span data-stu-id="740f9-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="740f9-281">Пользователи в определенной организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="740f9-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-282">После выбора значения в поле <strong>Иерархия</strong> на вкладке <strong>Выбор иерархии</strong> в списке <strong>Тип иерархии</strong> выберите тип иерархии, в которую требуется эскалировать решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="740f9-283">Система должна выполнить поиск по диапазону имен пользователей в иерархии.</span><span class="sxs-lookup"><span data-stu-id="740f9-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="740f9-284">Эти имена представляют пользователей, которым может быть эскалировано решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="740f9-285">Выполните следующие действия, чтобы указать начальную и конечную точку диапазона имен пользователей, которые извлекает система.</span><span class="sxs-lookup"><span data-stu-id="740f9-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="740f9-286">Для указания начальной точки выберите человека в списке <strong>Начать с</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="740f9-287">Для определения конечной точки щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="740f9-288">Введите условие для указания места в иерархии, в котором система должна остановить извлечение имен.</span><span class="sxs-lookup"><span data-stu-id="740f9-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="740f9-289">На вкладке <strong>Параметры иерархии</strong> укажите, каким пользователям в диапазоне должно быть эскалировано решение:</span><span class="sxs-lookup"><span data-stu-id="740f9-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="740f9-290"><strong>Назначить всем найденным пользователям</strong> — решение эскалируется всем пользователям в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="740f9-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="740f9-291"><strong>Назначить только последнему найденному пользователю</strong> — решение эскалируется только последнему пользователю в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="740f9-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="740f9-292"><strong>Исключить пользователей, для которых выполняется следующее:</strong> — решение не эскалируется пользователям в диапазоне, отвечающим определенному условию.</span><span class="sxs-lookup"><span data-stu-id="740f9-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="740f9-293">Чтобы указать условие, щелкните <strong>Добавить условие</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-294">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="740f9-294">Workflow user</span></span></td>
    <td><span data-ttu-id="740f9-295">Пользователи в текущем workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="740f9-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="740f9-296">После выбора значения в поле <strong>Пользователь workflow-процесса</strong> на вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите пользователя, который будет участвовать в workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="740f9-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="740f9-297">Пользователь</span><span class="sxs-lookup"><span data-stu-id="740f9-297">User</span></span></td>
    <td><span data-ttu-id="740f9-298">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="740f9-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="740f9-299">После выбора параметра <strong>Пользователь</strong> перейдите на вкладку <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="740f9-300">Список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="740f9-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="740f9-301">Выберите пользователей, которым требуется эскалировать решение, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f9-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="740f9-302">На вкладке **Ограничение по времени** в поле **Продолжительность** укажите, сколько времени отводится пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="740f9-303">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="740f9-303">Select one of the following options:</span></span>

    - <span data-ttu-id="740f9-304">**Часы** — введите число часов, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="740f9-305">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="740f9-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="740f9-306">**Дни** — введите число дней, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="740f9-307">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="740f9-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="740f9-308">**Недели** — введите число недель, которые предоставляются пользователю на принятие решения.</span><span class="sxs-lookup"><span data-stu-id="740f9-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="740f9-309">**Месяцы** — введите день и неделю, к которой пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="740f9-310">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="740f9-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="740f9-311">**Годы** — введите день, неделю и месяц, к которым пользователь должен принять решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="740f9-312">Например, можно указать, что пользователь должен принять решение до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="740f9-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="740f9-313">Повторите шаги с 3 по 4 для каждого пользователя, которого следует добавить в маршрут эскалации.</span><span class="sxs-lookup"><span data-stu-id="740f9-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="740f9-314">можно изменить порядок пользователей.</span><span class="sxs-lookup"><span data-stu-id="740f9-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="740f9-315">Если пользователи, перечисленные в пути эскалации, не приняли решение за отведенное время, система примет решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="740f9-316">Чтобы указать параметр, который выбирает система, выберите строку **Действие** и на вкладке **Конечное действие** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="740f9-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="740f9-317">Задание предельного срока</span><span class="sxs-lookup"><span data-stu-id="740f9-317">Set a time limit</span></span>

<span data-ttu-id="740f9-318">Выполните следующие действия, если решение должна быть принято за определенное время.</span><span class="sxs-lookup"><span data-stu-id="740f9-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="740f9-319">Параметры, выбранные в этой процедуре, переопределяют параметры, выбранные в областях **Назначение** и **Эскалация** страницы.</span><span class="sxs-lookup"><span data-stu-id="740f9-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="740f9-320">В левой области нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="740f9-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="740f9-321">Установите флажок **Задать ограничение по времени для элемента workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="740f9-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="740f9-322">В поле **Продолжительность** укажите, когда должно быть принято это решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="740f9-323">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="740f9-323">Select one of the following options:</span></span>

    - <span data-ttu-id="740f9-324">**Часы**— введите число часов.</span><span class="sxs-lookup"><span data-stu-id="740f9-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="740f9-325">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="740f9-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="740f9-326">**Дни** — введите число дней.</span><span class="sxs-lookup"><span data-stu-id="740f9-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="740f9-327">Затем выберите календарь, который используется в организации и введите информацию о рабочей неделе организации.</span><span class="sxs-lookup"><span data-stu-id="740f9-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="740f9-328">**Недели** — введите число недель.</span><span class="sxs-lookup"><span data-stu-id="740f9-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="740f9-329">**Месяцы** — выберите день и неделю, к которым должно быть принято решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="740f9-330">Например, можно указать, что решение должно быть принято до пятницы третьей недели месяца.</span><span class="sxs-lookup"><span data-stu-id="740f9-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="740f9-331">**Годы** — выберите день, неделю и месяц, к которым должно быть принято решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="740f9-332">Например, можно указать, что решение должно быть принято до пятницы третьей недели декабря.</span><span class="sxs-lookup"><span data-stu-id="740f9-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="740f9-333">По истечении предельного срока система принимает решение.</span><span class="sxs-lookup"><span data-stu-id="740f9-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="740f9-334">В списке **Действие** выберите параметр, который должна выбрать система.</span><span class="sxs-lookup"><span data-stu-id="740f9-334">In the **Action** list, select the option that the system should select.</span></span>
