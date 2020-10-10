---
title: Приложение Human Resources в Teams
description: Эта тема знакомит с приложением Microsoft Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828922"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="e7019-103">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="e7019-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e7019-104">Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет сотрудникам быстро запросить отпуск и просмотреть сведения о балансе времени в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e7019-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="e7019-105">Сотрудники могут взаимодействовать с ботом для запроса информации.</span><span class="sxs-lookup"><span data-stu-id="e7019-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="e7019-106">Вкладка **Отгул** содержит более подробную информацию. Кроме того, они могут отправлять пользователям сведения о предстоящем отгуле в группах и чатах вне приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e7019-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Бот для приложения отпусков Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Карточка запроса отпуска в Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="e7019-110">Установка и настройка</span><span class="sxs-lookup"><span data-stu-id="e7019-110">Install and setup</span></span>

<span data-ttu-id="e7019-111">Приложение "Human Resources" можно найти в магазине "Teams".</span><span class="sxs-lookup"><span data-stu-id="e7019-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="e7019-112">Сведения об установке приложения Teams см. в разделе [Управление запросами на отпуск в Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="e7019-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="e7019-113">Сведения об управлении разрешениями приложений в Teams см. в разделе [Управление политиками разрешений приложений в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e7019-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="e7019-114">Включение уведомлений для приложения Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="e7019-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="e7019-115">Если требуется, чтобы пользователи получали уведомления о запросах на отпуск в приложении Teams, необходимо включить уведомления в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e7019-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="e7019-116">Уведомления будут получать только пользователи, вошедшие в Teams и использующие приложение Human Resources Teams.</span><span class="sxs-lookup"><span data-stu-id="e7019-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="e7019-117">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="e7019-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e7019-118">Выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="e7019-118">Select **Links**.</span></span>

3. <span data-ttu-id="e7019-119">В разделе **Настройка** выберите **Системные параметры**.</span><span class="sxs-lookup"><span data-stu-id="e7019-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="e7019-120">На вкладке **Общие** установите для параметра **Включить уведомления для приложения Teams** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e7019-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Включение уведомлений приложения Teams в системных параметрах](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="e7019-122">Для включения уведомлений в Teams для всех пользователей выберите **Да** в ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="e7019-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Включение уведомлений Teams для всех пользователей](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="e7019-124">Включение и выключение уведомлений Teams для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="e7019-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="e7019-125">После включения уведомлений для приложения Human Resources Teams можно включать или отключать уведомления для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="e7019-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="e7019-126">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="e7019-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e7019-127">Выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="e7019-127">Select **Links**.</span></span>

3. <span data-ttu-id="e7019-128">В области **Пользователи** выберите **Параметры пользователей**.</span><span class="sxs-lookup"><span data-stu-id="e7019-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="e7019-129">Выберите вкладку **Рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="e7019-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="e7019-130">Установите для параметра **Включить уведомления для приложения Teams** значение **Да**, чтобы включить уведомления для пользователя, или значение **Нет**, чтобы отключить уведомления для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7019-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Включение уведомлений приложения Teams в параметрах пользователя на вкладке рабочего процесса](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="e7019-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e7019-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="e7019-133">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="e7019-133">Known issues</span></span>

| <span data-ttu-id="e7019-134">Расход</span><span class="sxs-lookup"><span data-stu-id="e7019-134">Issue</span></span> | <span data-ttu-id="e7019-135">Состояние</span><span class="sxs-lookup"><span data-stu-id="e7019-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="e7019-136">Горизонтальная прокрутка не работает для телефонов с Android</span><span class="sxs-lookup"><span data-stu-id="e7019-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="e7019-137">Горизонтальная прокрутка не является проблемой на устройствах с iOS или на настольном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e7019-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="e7019-138">Мы работаем над исправлением для Android.</span><span class="sxs-lookup"><span data-stu-id="e7019-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="e7019-139">Неверное сальдо при подаче запроса на отпуск для будущей даты.</span><span class="sxs-lookup"><span data-stu-id="e7019-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="e7019-140">Прогнозирование пока недоступно.</span><span class="sxs-lookup"><span data-stu-id="e7019-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="e7019-141">Сальдо отображается для текущей даты.</span><span class="sxs-lookup"><span data-stu-id="e7019-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="e7019-142">Не удается отменить запрос **На рассмотрении**.</span><span class="sxs-lookup"><span data-stu-id="e7019-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="e7019-143">Эта функциональная возможность в настоящее время не поддерживается и будет добавлена в будущем выпуске.</span><span class="sxs-lookup"><span data-stu-id="e7019-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="e7019-144">Сведения о сальдо рассчитываются на сегодняшний день.</span><span class="sxs-lookup"><span data-stu-id="e7019-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="e7019-145">В настоящее время в системе не отображается сальдо на период начисления, даже если оно настроено в параметрах отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="e7019-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="e7019-146">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="e7019-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="e7019-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="e7019-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="e7019-148">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="e7019-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="e7019-149">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="e7019-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="e7019-150">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="e7019-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="e7019-151">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="e7019-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="e7019-152">Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7019-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="e7019-153">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e7019-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="e7019-154">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e7019-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e7019-155">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="e7019-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="e7019-156">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e7019-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="e7019-157">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="e7019-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="e7019-158">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="e7019-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="e7019-159">Microsoft Teams, сетка событий Azure и Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="e7019-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="e7019-160">При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Microsoft Teams некоторые клиентские данные могут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="e7019-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="e7019-161">Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e7019-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="e7019-162">Эти данные могут храниться в сетке событий Microsoft Azure в течение 24 часов и будут обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e7019-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="e7019-163">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e7019-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="e7019-164">При взаимодействии с чат-ботом в приложении Human Resources содержимое беседы может храниться в Azure Cosmos DB и передаваться в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e7019-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="e7019-165">Эти данные могут храниться в Azure Cosmos DB течение 24 часов и могут быть обработаны вне географического региона, в котором развернута служба Human Resources для клиента, шифруются при передачи и хранении, и не используется корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e7019-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="e7019-166">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e7019-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="e7019-167">Для ограничения доступа к приложению Human Resources в Microsoft Teams для вашей организации или пользователей в организации см. раздел [Управление политиками разрешений приложений в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e7019-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="e7019-168">См. также</span><span class="sxs-lookup"><span data-stu-id="e7019-168">See also</span></span> 

[<span data-ttu-id="e7019-169">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e7019-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="e7019-170">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e7019-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="e7019-171">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="e7019-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

