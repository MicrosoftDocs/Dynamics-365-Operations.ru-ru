---
title: Управление запросами на отпуск в Teams
description: В этом разделе показано, как запросить отпуск в приложении Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097267"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="c745f-103">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c745f-104">Приложение Dynamics 365 Human Resources в Microsoft Teams позволяет быстро запросить отпуск и просмотреть сведения о балансе времени прямо в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c745f-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="c745f-105">Можно взаимодействовать с ботом для запроса информации и запуска запроса на отгул.</span><span class="sxs-lookup"><span data-stu-id="c745f-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="c745f-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="c745f-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="c745f-107">Также можно отправлять пользователям сведения о предстоящих отгулах в Teams и чатах вне приложения управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="c745f-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="c745f-108">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="c745f-108">Install the app</span></span>

<span data-ttu-id="c745f-109">Приложение Dynamics 365 Human Resources можно найти в магазине Teams.</span><span class="sxs-lookup"><span data-stu-id="c745f-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="c745f-110">В Microsoft Teams перейдите к списку приложений.</span><span class="sxs-lookup"><span data-stu-id="c745f-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="c745f-111">Выполните поиск Dynamics 365 Human Resources, а затем выберите плитку **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="c745f-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="c745f-112">Для установки приложения нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c745f-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="c745f-113">Если приложение не выполняет автоматический вход, выберите вкладку **Параметры**, чтобы выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="c745f-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="c745f-114">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="c745f-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="c745f-115">Если имеется доступ к нескольким экземплярам "Human Resources", можно выбрать среду, к которой необходимо подключиться, на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c745f-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="c745f-116">Приложение теперь поддерживает роль безопасности системного администратора.</span><span class="sxs-lookup"><span data-stu-id="c745f-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="c745f-117">Использование бота</span><span class="sxs-lookup"><span data-stu-id="c745f-117">Use the bot</span></span>

<span data-ttu-id="c745f-118">После установки приложения появится приветственное сообщение, позволяющее знать типы действий, которые может выполнять бот от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="c745f-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="c745f-119">При первом взаимодействии с ботом может потребоваться выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="c745f-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="c745f-120">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="c745f-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="c745f-121">Можно спросить бота о следующем:</span><span class="sxs-lookup"><span data-stu-id="c745f-121">You can ask the bot to:</span></span>

- <span data-ttu-id="c745f-122">Просмотрите текущие сальдо отпусков.</span><span class="sxs-lookup"><span data-stu-id="c745f-122">View your current leave balances.</span></span> <span data-ttu-id="c745f-123">Например, отправьте сообщение с текстом "Просмотр сальдо отпусков".</span><span class="sxs-lookup"><span data-stu-id="c745f-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="c745f-124">Запустите запрос на отпуск для вас.</span><span class="sxs-lookup"><span data-stu-id="c745f-124">Start a leave request for you.</span></span> <span data-ttu-id="c745f-125">Например, отправьте сообщение с текстом "Взять отпуск" или "Я хотел бы взять отпуск на следующий четверг и пятницу", чтобы более точно указать, что требуется отпуск для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="c745f-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Начало запроса на отпуск в чате Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="c745f-127">Чат-бот будет заполнять запрос на отпуска.</span><span class="sxs-lookup"><span data-stu-id="c745f-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="c745f-128">Выберите **Запрос на отгул** и измените сведения для запроса.</span><span class="sxs-lookup"><span data-stu-id="c745f-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="c745f-129">Если необходимо отправить запросы на отпуск для нескольких типов отпусков для одной и той же даты, выберите пункт **Разбиение дня с помощью** в меню **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="c745f-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="c745f-130">Если выбран отгул на половину дня, когда единица запроса отпуска равна дням, можно указать, следует ли запросить время отпуска с первой половины или второй половины дня, выбрав параметр **Определение половины дня** в меню **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="c745f-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Определения половины дня](./media/HalfDayDefinitions.png)

- <span data-ttu-id="c745f-132">Закончив редактирование сведений о запросе на отпуск, нажмите кнопку **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="c745f-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Отправить запрос на отпуск](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="c745f-134">Управление отпуском в Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-134">Manage your leave in Teams</span></span>

<span data-ttu-id="c745f-135">Вкладка **Отгул** служит для просмотра следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="c745f-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="c745f-136">Сведения о балансе времени для каждого типа отпусков, которые вам назначены</span><span class="sxs-lookup"><span data-stu-id="c745f-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="c745f-137">Предстоящие запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="c745f-137">Upcoming leave requests</span></span>

- <span data-ttu-id="c745f-138">Запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="c745f-138">Time-off requests</span></span>

- <span data-ttu-id="c745f-139">Черновые запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="c745f-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="c745f-140">Создание нового запроса</span><span class="sxs-lookup"><span data-stu-id="c745f-140">Create a new request</span></span>

1. <span data-ttu-id="c745f-141">Выберите **Новый запрос** для создания нового запроса на отпуск.</span><span class="sxs-lookup"><span data-stu-id="c745f-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="c745f-142">Введите день или дни, которые требуется взять отпуск, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c745f-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Добавить отпуск для приложения отпусков Human Resources Teams](./media/TimeOffHours.png)

3. <span data-ttu-id="c745f-144">Если применимо, введите код причины.</span><span class="sxs-lookup"><span data-stu-id="c745f-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="c745f-145">Кроме того, необходимо ввести комментарии и добавить вложения.</span><span class="sxs-lookup"><span data-stu-id="c745f-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="c745f-146">Выберите пункт **Разбиение дня с помощью** в меню **Дополнительные параметры**, если хотите отправить несколько записей запроса отпуска для одной даты с разными типами отпуска.</span><span class="sxs-lookup"><span data-stu-id="c745f-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="c745f-147">Выберите параметр **Определение половины дня**, чтобы указать, нужно ли запрашивать отгул в первую половину дня или во вторую половину дня.</span><span class="sxs-lookup"><span data-stu-id="c745f-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="c745f-148">Этот параметр доступен, если единицей запроса отпуска является день, а запрошенное количество равно 0,5 дня.</span><span class="sxs-lookup"><span data-stu-id="c745f-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="c745f-149">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="c745f-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="c745f-150">Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="c745f-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="c745f-151">Управление черновыми запросами</span><span class="sxs-lookup"><span data-stu-id="c745f-151">Manage draft requests</span></span>

1. <span data-ttu-id="c745f-152">Выберите вкладку **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="c745f-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="c745f-153">Выберите карандаш для редактирования запроса или выберите корзину, чтобы удалить запрос.</span><span class="sxs-lookup"><span data-stu-id="c745f-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="c745f-154">Внесите любые необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="c745f-154">Make any necessary changes.</span></span> <span data-ttu-id="c745f-155">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="c745f-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="c745f-156">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="c745f-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="c745f-157">Реагирование на уведомления Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-157">Respond to Teams notifications</span></span>

<span data-ttu-id="c745f-158">Если вы или сотрудник, для которого вы являетесь утверждающим, отправляете запрос на отпуск, вы получите уведомление в приложении Human Resources в Teams.</span><span class="sxs-lookup"><span data-stu-id="c745f-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="c745f-159">Можно выбрать уведомление для его просмотра.</span><span class="sxs-lookup"><span data-stu-id="c745f-159">You can select the notification to view it.</span></span> <span data-ttu-id="c745f-160">Уведомления также появляются в области **Чат**.</span><span class="sxs-lookup"><span data-stu-id="c745f-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="c745f-161">Если вы являетесь утверждающим, вы можете выбрать **Утвердить** или **Отклонить** в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="c745f-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="c745f-162">Кроме того, можно указать необязательное сообщение.</span><span class="sxs-lookup"><span data-stu-id="c745f-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="c745f-163">Отправка сведений о предстоящих отгулах вашим коллегам</span><span class="sxs-lookup"><span data-stu-id="c745f-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="c745f-164">После установки приложения Human Resources для Teams можно легко отправлять сведения о предстоящем времени отгулов вашим коллегам в группах или чатах.</span><span class="sxs-lookup"><span data-stu-id="c745f-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="c745f-165">В рабочей группе или чате в Teams выберите кнопку Human Resources под окном чата.</span><span class="sxs-lookup"><span data-stu-id="c745f-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Кнопка Human Resources под окном чата](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="c745f-167">Выберите запрос отпуска, которым необходимо поделиться.</span><span class="sxs-lookup"><span data-stu-id="c745f-167">Select the leave request you want to share.</span></span> <span data-ttu-id="c745f-168">Если требуется поделиться черновиком запроса отпуска, сначала выберите **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="c745f-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="c745f-169">Ваш запрос отпуска будет отображен в чате.</span><span class="sxs-lookup"><span data-stu-id="c745f-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="c745f-170">Если поделиться черновиком запроса отпуска, он будет выведен в качестве черновика.</span><span class="sxs-lookup"><span data-stu-id="c745f-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="c745f-171">Просмотр календаря отпусков рабочей группы</span><span class="sxs-lookup"><span data-stu-id="c745f-171">View your team's leave calendar</span></span>

<span data-ttu-id="c745f-172">Если вы являетесь руководителем с непосредственными подчиненными, вы можете просмотреть утвержденные и ожидающие утверждения запросы отгулов для вашей рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="c745f-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="c745f-173">В приложении Human Resources app в Teams выберите **Отгул**.</span><span class="sxs-lookup"><span data-stu-id="c745f-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="c745f-174">Выберите **Календарь рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="c745f-174">Select **Team calendar**.</span></span> <span data-ttu-id="c745f-175">В календаре отображаются утвержденные и ожидающие утверждения отгулы ваших непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="c745f-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c745f-176">Если календарь рабочей группы не отображается, попросите администратора включить его.</span><span class="sxs-lookup"><span data-stu-id="c745f-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="c745f-177">Дополнительные сведения см. в разделе [Установка и настройка](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="c745f-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="c745f-178">Поддерживаемые языки</span><span class="sxs-lookup"><span data-stu-id="c745f-178">Supported languages</span></span>

<span data-ttu-id="c745f-179">Приложение Dynamics 365 Human Resources в Teams поддерживает следующие языки:</span><span class="sxs-lookup"><span data-stu-id="c745f-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="c745f-180">Код языка</span><span class="sxs-lookup"><span data-stu-id="c745f-180">Locale ID</span></span> | <span data-ttu-id="c745f-181">Язык</span><span class="sxs-lookup"><span data-stu-id="c745f-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="c745f-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="c745f-182">de-DE</span></span> | <span data-ttu-id="c745f-183">Немецкий (Германия)</span><span class="sxs-lookup"><span data-stu-id="c745f-183">German (Germany)</span></span> |
| <span data-ttu-id="c745f-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="c745f-184">es-ES</span></span> | <span data-ttu-id="c745f-185">Испанский (Испания)</span><span class="sxs-lookup"><span data-stu-id="c745f-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="c745f-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="c745f-186">es-MX</span></span> | <span data-ttu-id="c745f-187">Испанский (Мексика)</span><span class="sxs-lookup"><span data-stu-id="c745f-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="c745f-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="c745f-188">fr-CA</span></span> | <span data-ttu-id="c745f-189">Французский (Канада)</span><span class="sxs-lookup"><span data-stu-id="c745f-189">French (Canada)</span></span> |
| <span data-ttu-id="c745f-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="c745f-190">fr-FR</span></span> | <span data-ttu-id="c745f-191">Французский (Франция)</span><span class="sxs-lookup"><span data-stu-id="c745f-191">French (France)</span></span> |
| <span data-ttu-id="c745f-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="c745f-192">it-IT</span></span> | <span data-ttu-id="c745f-193">Итальянский (Италия)</span><span class="sxs-lookup"><span data-stu-id="c745f-193">Italian (Italy)</span></span> |
| <span data-ttu-id="c745f-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="c745f-194">nl-NL</span></span> | <span data-ttu-id="c745f-195">Нидерландский (Нидерланды)</span><span class="sxs-lookup"><span data-stu-id="c745f-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="c745f-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="c745f-196">pt-BR</span></span> | <span data-ttu-id="c745f-197">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="c745f-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="c745f-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="c745f-198">tr-TR</span></span> | <span data-ttu-id="c745f-199">Турецкий (Турция)</span><span class="sxs-lookup"><span data-stu-id="c745f-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="c745f-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="c745f-200">zh-CN</span></span> | <span data-ttu-id="c745f-201">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="c745f-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="c745f-202">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="c745f-202">Troubleshooting</span></span>

<span data-ttu-id="c745f-203">Если вы не можете войти в систему или использовать приложение Dynamics 365 Human Resources Teams, попробуйте выполнить следующие инструкции по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="c745f-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="c745f-204">Если после устранения неполадок все еще возникают проблемы, обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c745f-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="c745f-205">Для получения дополнительных см. [Получение поддержки](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="c745f-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="c745f-206">Невозможно выполнить вход в приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="c745f-207">Если вы не можете войти в приложение, возможно, что учетная запись, используемая для входа в Microsoft Teams, не связана с записью сотрудника в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c745f-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c745f-208">Обратитесь к системному администратору, чтобы убедиться, что запись сотрудника правильно связана.</span><span class="sxs-lookup"><span data-stu-id="c745f-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="c745f-209">Переводы выводятся неправильно</span><span class="sxs-lookup"><span data-stu-id="c745f-209">Translations don't display correctly</span></span>

<span data-ttu-id="c745f-210">Если переводы не показываются, как ожидалось, убедитесь, что язык, выбранный в Teams, совпадает с языком, выбранным в разделе **Параметры пользователя** в модуле управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="c745f-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="c745f-211">В Teams проверьте **Язык приложения** в **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c745f-211">In Teams, look at **App language** in **Settings**.</span></span>

![Параметры Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="c745f-213">В модуле управления персоналом выберите **Параметры**, а затем выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="c745f-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="c745f-214">Убедитесь, что поле **Язык** соответствует полю **Язык приложения** в Teams.</span><span class="sxs-lookup"><span data-stu-id="c745f-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Параметры пользователя управления персоналом](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="c745f-216">Если проблемы с переводом не устранены, сообщите нам о них.</span><span class="sxs-lookup"><span data-stu-id="c745f-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="c745f-217">Сведения см. в разделе [Получение поддержки для приложений Finance and Operations или Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c745f-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="c745f-218">Ошибка при утверждении запросов отпуска в приложении Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="c745f-219">При получении сообщения об ошибке при попытке утверждения запросов на отпуск в приложении Teams попробуйте выполнить следующие действия по устранению неполадок:</span><span class="sxs-lookup"><span data-stu-id="c745f-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="c745f-220">Убедитесь, что учетная запись, в которую вы входите в Microsoft Teams, совпадает с используемой для доступа в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c745f-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="c745f-221">Проверьте, что вы действительно являетесь утверждающим для этого запроса, проверив параметры рабочего процесса для утверждения отпуска.</span><span class="sxs-lookup"><span data-stu-id="c745f-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="c745f-222">Дополнительные сведения о рабочих процессах запроса отпуска см. в разделе [Создание рабочего процесса запроса отпуска](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c745f-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="c745f-223">Утверждающие отпуска не получают сообщения чата Teams для утверждения запросов на отпуск</span><span class="sxs-lookup"><span data-stu-id="c745f-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="c745f-224">Убедитесь, что для среды и пользователя включены уведомления.</span><span class="sxs-lookup"><span data-stu-id="c745f-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="c745f-225">Дополнительные сведения см. в [Включение уведомлений для приложения Human Resources в Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) и [Включение и выключение уведомлений Teams для отдельных пользователей](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="c745f-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="c745f-226">Убедитесь, что пользователи вошли в систему на вкладке **Чаты** с теми же учетными данными, которые используются для утверждения запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="c745f-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="c745f-227">Используйте сообщения "выйти", а затем "войти", чтобы войти в систему, используя правильные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c745f-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="c745f-228">Если проблема сохраняется, проверьте статус пакетного задания системы бизнес-событий как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="c745f-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="c745f-229">Если он находится на ожидающем или выполняющемся этапе, проверьте через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="c745f-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="c745f-230">Если статус не меняется, отправьте запрос в службу поддержки, чтобы ее сотрудники могли помочь в устранении проблемы.</span><span class="sxs-lookup"><span data-stu-id="c745f-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="c745f-231">Известные проблемы со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="c745f-231">Known accessibility issues</span></span>

<span data-ttu-id="c745f-232">Приложение Human Resources в Teams обладает следующими проблемами специальных возможностей, над которыми мы работаем, чтобы устранить их в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="c745f-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="c745f-233">Расход</span><span class="sxs-lookup"><span data-stu-id="c745f-233">Issue</span></span> | <span data-ttu-id="c745f-234">Временное решение или объяснение</span><span class="sxs-lookup"><span data-stu-id="c745f-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="c745f-235">При увеличении до 400% на рабочем столе скрываются из вида некоторые кнопки действий.</span><span class="sxs-lookup"><span data-stu-id="c745f-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="c745f-236">Рекомендуется использовать экранную лупу вместо этого, пока мы не сможем поддерживать этот уровень масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c745f-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="c745f-237">На вкладке **Отгулы** средство VoiceOver объявляет действие кнопки при чтении заголовка для сетки отгулов.</span><span class="sxs-lookup"><span data-stu-id="c745f-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="c745f-238">Заголовок и элементы в сетке группируются по годам, и их можно свернуть.</span><span class="sxs-lookup"><span data-stu-id="c745f-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="c745f-239">Средство VoiceOver интерпретирует это как элемент действия, но это не так.</span><span class="sxs-lookup"><span data-stu-id="c745f-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="c745f-240">На вкладке **Отгулы** имеется дополнительный жест прокрутки при переходе к полю **Код причины** в новом запросе.</span><span class="sxs-lookup"><span data-stu-id="c745f-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="c745f-241">Нет скрытого элемента управления, к которому пытается перейти навигация при прокрутке.</span><span class="sxs-lookup"><span data-stu-id="c745f-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="c745f-242">На вкладке **Отгулы** если вы проведите пальцем, когда календарь открыт, вы выходите за пределы элемента управления, а не переходите наверх в новом запросе или при редактировании запроса.</span><span class="sxs-lookup"><span data-stu-id="c745f-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="c745f-243">При достижении **К сегодняшней дате** считайте, что это конец элемента управления, и прокручивайте в обратном направлении, чтобы вернуться к началу.</span><span class="sxs-lookup"><span data-stu-id="c745f-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="c745f-244">На вкладке **Чат** фокус перемещается назад к началу, когда пользователь вводит дату при использовании вспомогательного средства или навигации с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="c745f-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="c745f-245">Нажимайте клавишу TAB, пока не будет снова достигнута область ввода.</span><span class="sxs-lookup"><span data-stu-id="c745f-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="c745f-246">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="c745f-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="c745f-247">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="c745f-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="c745f-248">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="c745f-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="c745f-249">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="c745f-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="c745f-250">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="c745f-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="c745f-251">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="c745f-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="c745f-252">Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="c745f-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="c745f-253">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c745f-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="c745f-254">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c745f-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c745f-255">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="c745f-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="c745f-256">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c745f-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="c745f-257">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="c745f-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="c745f-258">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="c745f-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="c745f-259">Microsoft Teams, сетка событий Azure и Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c745f-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="c745f-260">При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Microsoft Teams некоторые клиентские данные могут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="c745f-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="c745f-261">Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c745f-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="c745f-262">Эти данные могут храниться в сетке событий Microsoft Azure в течение 24 часов и будут обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c745f-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="c745f-263">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="c745f-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="c745f-264">При взаимодействии с чат-ботом в приложении Human Resources содержимое беседы может храниться в Azure Cosmos DB и передаваться в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c745f-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="c745f-265">Эти данные могут храниться в Azure Cosmos DB течение 24 часов и могут быть обработаны вне географического региона, в котором развернута служба Human Resources для клиента, шифруются при передачи и хранении, и не используется корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c745f-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="c745f-266">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="c745f-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="c745f-267">Для ограничения доступа к приложению Human Resources в Microsoft Teams для вашей организации или пользователей в организации см. раздел [Управление политиками разрешений приложений в Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="c745f-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="c745f-268">См. также</span><span class="sxs-lookup"><span data-stu-id="c745f-268">See also</span></span>

[<span data-ttu-id="c745f-269">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="c745f-270">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="c745f-271">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="c745f-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
