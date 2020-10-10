---
title: Управление запросами на отпуск в Teams
description: В этом разделе показано, как запросить отпуск в приложении Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828952"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="2d003-103">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="2d003-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2d003-104">Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет быстро запросить отпуск и просмотреть сведения о балансе времени прямо в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2d003-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="2d003-105">Можно взаимодействовать с ботом для запроса информации и запуска запроса на отгул.</span><span class="sxs-lookup"><span data-stu-id="2d003-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="2d003-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="2d003-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="2d003-107">Кроме того, можно отправлять пользователям сведения о предстоящих отгулах в рабочих группа и чатах вне приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2d003-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="2d003-108">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="2d003-108">Install the app</span></span>

<span data-ttu-id="2d003-109">Приложение "Human Resources" можно найти в магазине "Teams".</span><span class="sxs-lookup"><span data-stu-id="2d003-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="2d003-110">В Microsoft Teams выберите многоточие.</span><span class="sxs-lookup"><span data-stu-id="2d003-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Многоточие приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="2d003-112">Выполните поиск Dynamics 365 Human Resources, а затем выберите плитку **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2d003-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Плитка HR приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="2d003-114">Для установки приложения нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2d003-114">Select the **Add** button to install the app.</span></span>

   ![Установка приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="2d003-116">Если приложение не выполняет автоматический вход, выберите вкладку **Параметры**, чтобы выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="2d003-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Вкладка Параметры приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="2d003-118">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="2d003-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="2d003-119">Если имеется доступ к нескольким экземплярам "Human Resources", можно выбрать среду, к которой необходимо подключиться, на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="2d003-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="2d003-120">Приложение теперь поддерживает роль безопасности системного администратора.</span><span class="sxs-lookup"><span data-stu-id="2d003-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="2d003-121">Использование бота</span><span class="sxs-lookup"><span data-stu-id="2d003-121">Use the bot</span></span>

<span data-ttu-id="2d003-122">После установки приложения появится приветственное сообщение, позволяющее знать типы действий, которые может выполнять бот от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="2d003-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Приветственное сообщение бота для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="2d003-124">При первом взаимодействии с ботом может потребоваться выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="2d003-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="2d003-125">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="2d003-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="2d003-126">Можно спросить бота о следующем:</span><span class="sxs-lookup"><span data-stu-id="2d003-126">You can ask the bot to:</span></span>

- <span data-ttu-id="2d003-127">Отображение сведений о балансе времени для каждого типа отпусков, которые вам назначены.</span><span class="sxs-lookup"><span data-stu-id="2d003-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Показать балансы приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="2d003-129">Отображение дополнительных сведений о конкретном типе отпуска.</span><span class="sxs-lookup"><span data-stu-id="2d003-129">Show additional details about a specific leave type.</span></span>

   ![Показать сведения приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="2d003-131">Запустите запрос на отпуск для вас.</span><span class="sxs-lookup"><span data-stu-id="2d003-131">Start a leave request for you.</span></span>

   ![Запрос на отпуск приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="2d003-133">После того как вы запустите запрос на отпуск, вы можете скорректировать дни непосредственно в карточке.</span><span class="sxs-lookup"><span data-stu-id="2d003-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Изменить запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="2d003-135">По завершении ввода данных выберите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="2d003-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="2d003-136">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="2d003-136">You can also select **Save as draft** to come back to it later.</span></span>

![Отправка запросов для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="2d003-138">Управление отпуском в Teams</span><span class="sxs-lookup"><span data-stu-id="2d003-138">Manage your leave in Teams</span></span>

<span data-ttu-id="2d003-139">Вкладка **Отгул** служит для просмотра следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="2d003-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="2d003-140">Сведения о балансе времени для каждого типа отпусков, которые вам назначены</span><span class="sxs-lookup"><span data-stu-id="2d003-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="2d003-141">Предстоящие запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="2d003-141">Upcoming leave requests</span></span>

- <span data-ttu-id="2d003-142">Запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="2d003-142">Time-off requests</span></span>

- <span data-ttu-id="2d003-143">Черновые запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="2d003-143">Draft leave requests</span></span>

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="2d003-145">Создание нового запроса</span><span class="sxs-lookup"><span data-stu-id="2d003-145">Create a new request</span></span>

1. <span data-ttu-id="2d003-146">Выберите **Новый запрос** для создания нового запроса на отпуск.</span><span class="sxs-lookup"><span data-stu-id="2d003-146">To create a new leave request, select **New request**.</span></span>

   ![Новый запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="2d003-148">Введите день или дни, которые требуется взять отпуск, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2d003-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Добавить отпуск для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="2d003-150">Если применимо, введите код причины.</span><span class="sxs-lookup"><span data-stu-id="2d003-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="2d003-151">Кроме того, необходимо ввести комментарии и добавить вложения.</span><span class="sxs-lookup"><span data-stu-id="2d003-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="2d003-152">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="2d003-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2d003-153">Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="2d003-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="2d003-154">Управление черновыми запросами</span><span class="sxs-lookup"><span data-stu-id="2d003-154">Manage draft requests</span></span>

1. <span data-ttu-id="2d003-155">Выберите вкладку **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="2d003-155">Select the **Drafts** tab.</span></span>

   ![Вкладка Черновики для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="2d003-157">Выберите карандаш для редактирования запроса или выберите корзину, чтобы удалить запрос.</span><span class="sxs-lookup"><span data-stu-id="2d003-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="2d003-158">Внесите любые необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="2d003-158">Make any necessary changes.</span></span> <span data-ttu-id="2d003-159">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="2d003-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2d003-160">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="2d003-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Изменить черновик для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="2d003-162">Реагирование на уведомления Teams</span><span class="sxs-lookup"><span data-stu-id="2d003-162">Respond to Teams notifications</span></span>

<span data-ttu-id="2d003-163">Если вы или сотрудник, для которого вы являетесь утверждающим, отправляете запрос на отпуск, вы получите уведомление в приложении Human Resources в Teams.</span><span class="sxs-lookup"><span data-stu-id="2d003-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="2d003-164">Можно выбрать уведомление для его просмотра.</span><span class="sxs-lookup"><span data-stu-id="2d003-164">You can select the notification to view it.</span></span> <span data-ttu-id="2d003-165">Уведомления также появляются в области **Чат**.</span><span class="sxs-lookup"><span data-stu-id="2d003-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="2d003-166">Если вы являетесь утверждающим, вы можете выбрать **Утвердить** или **Отклонить** в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="2d003-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="2d003-167">Кроме того, можно указать необязательное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2d003-167">You can also provide an optional message.</span></span>

![Уведомление о запросе отпуска в приложении Human Resources в Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="2d003-169">Отправка сведений о предстоящих отгулах вашим коллегам</span><span class="sxs-lookup"><span data-stu-id="2d003-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="2d003-170">После установки приложения Human Resources для Teams можно легко отправлять сведения о предстоящем времени отгулов вашим коллегам в группах или чатах.</span><span class="sxs-lookup"><span data-stu-id="2d003-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="2d003-171">В рабочей группе или чате в Teams выберите кнопку Human Resources под окном чата.</span><span class="sxs-lookup"><span data-stu-id="2d003-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Кнопка Human Resources под окном чата](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="2d003-173">Выберите запрос отпуска, которым необходимо поделиться.</span><span class="sxs-lookup"><span data-stu-id="2d003-173">Select the leave request you want to share.</span></span> <span data-ttu-id="2d003-174">Если требуется поделиться черновиком запроса отпуска, сначала выберите **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="2d003-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Выбор предстоящего запроса отпуска для общего доступа](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="2d003-176">Ваш запрос отпуска будет отображен в чате.</span><span class="sxs-lookup"><span data-stu-id="2d003-176">Your leave request will display in the chat.</span></span>

![Карточка запроса отпуска в Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="2d003-178">Если поделиться черновиком запроса отпуска, он будет выведен в качестве черновика:</span><span class="sxs-lookup"><span data-stu-id="2d003-178">If you shared a draft request, it will display as a draft:</span></span>

![Карточка черновика запроса отпуска в Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="2d003-180">Просмотр календаря отпусков рабочей группы</span><span class="sxs-lookup"><span data-stu-id="2d003-180">View your team's leave calendar</span></span>

<span data-ttu-id="2d003-181">Если вы являетесь руководителем с непосредственными подчиненными, вы можете просмотреть утвержденные и ожидающие утверждения запросы отгулов для вашей рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="2d003-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="2d003-182">В приложении Human Resources app в Teams выберите **Отгул**.</span><span class="sxs-lookup"><span data-stu-id="2d003-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="2d003-183">Выберите **Календарь рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="2d003-183">Select **Team calendar**.</span></span>

   ![Просмотр календаря в приложении Human Resources в Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="2d003-185">В календаре отображаются утвержденные и ожидающие утверждения отгулы ваших непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="2d003-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Календарь отгулов в приложении Human Resources в Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="2d003-187">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="2d003-187">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="2d003-188">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="2d003-188">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="2d003-189">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="2d003-189">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2d003-190">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="2d003-190">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2d003-191">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2d003-191">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2d003-192">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="2d003-192">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2d003-193">Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d003-193">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2d003-194">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2d003-194">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2d003-195">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2d003-195">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2d003-196">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="2d003-196">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2d003-197">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2d003-197">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2d003-198">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2d003-198">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2d003-199">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2d003-199">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="2d003-200">Microsoft Teams, сетка событий Azure и Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="2d003-200">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="2d003-201">При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Microsoft Teams некоторые клиентские данные могут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="2d003-201">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="2d003-202">Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2d003-202">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="2d003-203">Эти данные могут храниться в сетке событий Microsoft Azure в течение 24 часов и будут обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2d003-203">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2d003-204">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2d003-204">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="2d003-205">При взаимодействии с чат-ботом в приложении Human Resources содержимое беседы может храниться в Azure Cosmos DB и передаваться в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2d003-205">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="2d003-206">Эти данные могут храниться в Azure Cosmos DB течение 24 часов и могут быть обработаны вне географического региона, в котором развернута служба Human Resources для клиента, шифруются при передачи и хранении, и не используется корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2d003-206">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2d003-207">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2d003-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="2d003-208">Для ограничения доступа к приложению Human Resources в Microsoft Teams для вашей организации или пользователей в организации см. раздел [Управление политиками разрешений приложений в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2d003-208">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="2d003-209">См. также</span><span class="sxs-lookup"><span data-stu-id="2d003-209">See also</span></span>

[<span data-ttu-id="2d003-210">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2d003-210">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2d003-211">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2d003-211">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2d003-212">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="2d003-212">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
