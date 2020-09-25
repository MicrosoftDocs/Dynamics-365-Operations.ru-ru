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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766768"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="6ab41-103">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="6ab41-104">Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет быстро запросить отпуск и просмотреть сведения о балансе времени прямо в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6ab41-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="6ab41-105">Можно взаимодействовать с ботом для запроса информации.</span><span class="sxs-lookup"><span data-stu-id="6ab41-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="6ab41-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="6ab41-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="6ab41-107">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="6ab41-107">Install the app</span></span>

<span data-ttu-id="6ab41-108">Приложение "Human Resources" можно найти в магазине "Teams".</span><span class="sxs-lookup"><span data-stu-id="6ab41-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="6ab41-109">В Microsoft Teams выберите многоточие.</span><span class="sxs-lookup"><span data-stu-id="6ab41-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Многоточие приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="6ab41-111">Выполните поиск Dynamics 365 Human Resources, а затем выберите плитку **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Плитка HR приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="6ab41-113">Для установки приложения нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-113">Select the **Add** button to install the app.</span></span>

   ![Установка приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="6ab41-115">Если приложение не выполняет автоматический вход, выберите вкладку **Параметры**, чтобы выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="6ab41-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Вкладка Параметры приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="6ab41-117">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="6ab41-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="6ab41-118">Если имеется доступ к нескольким экземплярам "Human Resources", можно выбрать среду, к которой необходимо подключиться, на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="6ab41-119">Приложение в настоящее время не поддерживает роль "системный администратор" и выводит сообщение об ошибке, если вход осуществляется с учетной записью системного администратора.</span><span class="sxs-lookup"><span data-stu-id="6ab41-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="6ab41-120">Чтобы войти с использованием других учетных записей, на вкладке **Параметры** нажмите кнопку **переключателя счетов**, а затем выполните вход с учетной записью пользователя, не обладающей правами администратора системы.</span><span class="sxs-lookup"><span data-stu-id="6ab41-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="6ab41-121">Использование бота</span><span class="sxs-lookup"><span data-stu-id="6ab41-121">Use the bot</span></span>

<span data-ttu-id="6ab41-122">После установки приложения появится приветственное сообщение, позволяющее знать типы действий, которые может выполнять бот от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="6ab41-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Приветственное сообщение бота для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="6ab41-124">При первом взаимодействии с ботом может потребоваться выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="6ab41-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="6ab41-125">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="6ab41-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="6ab41-126">Можно спросить бота о следующем:</span><span class="sxs-lookup"><span data-stu-id="6ab41-126">You can ask the bot to:</span></span>

- <span data-ttu-id="6ab41-127">Отображение сведений о балансе времени для каждого типа отпусков, которые вам назначены.</span><span class="sxs-lookup"><span data-stu-id="6ab41-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Показать балансы приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="6ab41-129">Отображение дополнительных сведений о конкретном типе отпуска.</span><span class="sxs-lookup"><span data-stu-id="6ab41-129">Show additional details about a specific leave type.</span></span>

   ![Показать сведения приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="6ab41-131">Запустите запрос на отпуск для вас.</span><span class="sxs-lookup"><span data-stu-id="6ab41-131">Start a leave request for you.</span></span>

   ![Запрос на отпуск приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="6ab41-133">После того как вы запустите запрос на отпуск, вы можете скорректировать дни непосредственно в карточке.</span><span class="sxs-lookup"><span data-stu-id="6ab41-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Изменить запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="6ab41-135">По завершении ввода данных выберите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="6ab41-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="6ab41-136">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="6ab41-136">You can also select **Save as draft** to come back to it later.</span></span>

![Отправка запросов для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="6ab41-138">Управление отпуском в Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-138">Manage your leave in Teams</span></span>

<span data-ttu-id="6ab41-139">Вкладка **Отгул** служит для просмотра следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="6ab41-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="6ab41-140">Сведения о балансе времени для каждого типа отпусков, которые вам назначены</span><span class="sxs-lookup"><span data-stu-id="6ab41-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="6ab41-141">Предстоящие запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="6ab41-141">Upcoming leave requests</span></span>

- <span data-ttu-id="6ab41-142">Запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="6ab41-142">Time-off requests</span></span>

- <span data-ttu-id="6ab41-143">Черновые запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="6ab41-143">Draft leave requests</span></span>

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="6ab41-145">Создание нового запроса</span><span class="sxs-lookup"><span data-stu-id="6ab41-145">Create a new request</span></span>

1. <span data-ttu-id="6ab41-146">Выберите **Новый запрос** для создания нового запроса на отпуск.</span><span class="sxs-lookup"><span data-stu-id="6ab41-146">To create a new leave request, select **New request**.</span></span>

   ![Новый запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="6ab41-148">Введите день или дни, которые требуется взять отпуск, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Добавить отпуск для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="6ab41-150">Если применимо, введите код причины.</span><span class="sxs-lookup"><span data-stu-id="6ab41-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="6ab41-151">Кроме того, необходимо ввести комментарии и добавить вложения.</span><span class="sxs-lookup"><span data-stu-id="6ab41-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="6ab41-152">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="6ab41-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="6ab41-153">Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="6ab41-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="6ab41-154">Управление черновыми запросами</span><span class="sxs-lookup"><span data-stu-id="6ab41-154">Manage draft requests</span></span>

1. <span data-ttu-id="6ab41-155">Выберите вкладку **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-155">Select the **Drafts** tab.</span></span>

   ![Вкладка Черновики для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="6ab41-157">Выберите карандаш для редактирования запроса или выберите корзину, чтобы удалить запрос.</span><span class="sxs-lookup"><span data-stu-id="6ab41-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="6ab41-158">Внесите любые необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="6ab41-158">Make any necessary changes.</span></span> <span data-ttu-id="6ab41-159">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="6ab41-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="6ab41-160">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="6ab41-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Изменить черновик для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="6ab41-162">Уведомления Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-162">Teams notifications</span></span>

<span data-ttu-id="6ab41-163">Если вы или сотрудник, для которого вы являетесь утверждающим, отправляете запрос на отпуск, вы получите уведомление в приложении Human Resources в Teams.</span><span class="sxs-lookup"><span data-stu-id="6ab41-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="6ab41-164">Можно выбрать уведомление для его просмотра.</span><span class="sxs-lookup"><span data-stu-id="6ab41-164">You can select the notification to view it.</span></span> <span data-ttu-id="6ab41-165">Уведомления также появляются в области **Чат**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="6ab41-166">Если вы являетесь утверждающим, вы можете выбрать **Утвердить** или **Отклонить** в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="6ab41-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="6ab41-167">Кроме того, можно указать необязательное сообщение.</span><span class="sxs-lookup"><span data-stu-id="6ab41-167">You can also provide an optional message.</span></span>

![Уведомление о запросе отпуска в приложении Human Resources в Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="6ab41-169">Просмотр календаря отпусков рабочей группы</span><span class="sxs-lookup"><span data-stu-id="6ab41-169">View your team's leave calendar</span></span>

<span data-ttu-id="6ab41-170">Если вы являетесь руководителем с непосредственными подчиненными, вы можете просмотреть утвержденные и ожидающие утверждения запросы отгулов для вашей рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="6ab41-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="6ab41-171">В приложении Human Resources app в Teams выберите **Отгул**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="6ab41-172">Выберите **Календарь рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="6ab41-172">Select **Team calendar**.</span></span>

   ![Просмотр календаря в приложении Human Resources в Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="6ab41-174">В календаре отображаются утвержденные и ожидающие утверждения отгулы ваших непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="6ab41-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Календарь отгулов в приложении Human Resources в Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="6ab41-176">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="6ab41-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="6ab41-177">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="6ab41-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="6ab41-178">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="6ab41-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="6ab41-179">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="6ab41-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="6ab41-180">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="6ab41-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="6ab41-181">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="6ab41-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="6ab41-182">Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ab41-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="6ab41-183">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="6ab41-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="6ab41-184">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6ab41-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6ab41-185">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="6ab41-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="6ab41-186">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6ab41-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="6ab41-187">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="6ab41-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="6ab41-188">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="6ab41-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="6ab41-189">Сетка событий Microsoft Azure и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="6ab41-190">При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Teams некоторые клиентские данные будут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="6ab41-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="6ab41-191">Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6ab41-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="6ab41-192">Эти данные могут храниться в течение 24 часов и обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6ab41-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ab41-193">См. также</span><span class="sxs-lookup"><span data-stu-id="6ab41-193">See also</span></span>

[<span data-ttu-id="6ab41-194">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="6ab41-195">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="6ab41-196">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="6ab41-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
