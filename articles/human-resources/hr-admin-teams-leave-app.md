---
title: Приложение Human Resources в Teams
description: Эта тема знакомит с приложением Microsoft Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1cceb15d64215cb8d5c996df792e863d466f87d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053571"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="fc805-103">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fc805-104">Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет сотрудникам быстро запросить отпуск и просмотреть сведения о балансе времени в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fc805-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="fc805-105">Сотрудники могут взаимодействовать с ботом для запроса информации.</span><span class="sxs-lookup"><span data-stu-id="fc805-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="fc805-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="fc805-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="fc805-107">Кроме того, они могут отправлять пользователям сведения о предстоящих отгулах в рабочих группа и чатах вне приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fc805-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Бот для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot.png)

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Карточка запроса отпуска в Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="fc805-111">Установка и настройка</span><span class="sxs-lookup"><span data-stu-id="fc805-111">Install and setup</span></span>

<span data-ttu-id="fc805-112">Приложение Dynamics 365 Human Resources можно найти в магазине Teams.</span><span class="sxs-lookup"><span data-stu-id="fc805-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="fc805-113">Сведения об установке приложения Teams см. в разделе [Управление запросами на отпуск в Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="fc805-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="fc805-114">Сведения об управлении разрешениями приложений в Teams см. в разделе [Управление политиками разрешений приложений в Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="fc805-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="fc805-115">Если требуется, чтобы пользователи могли просматривать календарь отпусков и отсутствия в приложении, необходимо включить **Календарь отпусков и отсутствия в Teams** в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="fc805-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="fc805-116">Дополнительные сведения о включении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="fc805-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="fc805-117">Включение уведомлений для приложения Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="fc805-118">Если требуется, чтобы пользователи получали уведомления о запросах на отпуск в приложении Teams, необходимо включить уведомления в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fc805-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="fc805-119">Уведомления будут получать только пользователи, вошедшие в Teams и использующие приложение Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fc805-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="fc805-120">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="fc805-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="fc805-121">Выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="fc805-121">Select **Links**.</span></span>

3. <span data-ttu-id="fc805-122">В разделе **Настройка** выберите **Системные параметры**.</span><span class="sxs-lookup"><span data-stu-id="fc805-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="fc805-123">На вкладке **Общие** установите для параметра **Включить уведомления для приложения Teams** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="fc805-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Включение уведомлений приложения Teams в системных параметрах](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="fc805-125">Для включения уведомлений в Teams для всех пользователей выберите **Да** в ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="fc805-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Включение уведомлений Teams для всех пользователей](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="fc805-127">Включение и выключение уведомлений Teams для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="fc805-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="fc805-128">После включения уведомлений для приложения Dynamics 365 Human Resources Teams можно включать или отключать уведомления для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc805-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="fc805-129">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="fc805-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="fc805-130">Выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="fc805-130">Select **Links**.</span></span>

3. <span data-ttu-id="fc805-131">В области **Пользователи** выберите **Параметры пользователей**.</span><span class="sxs-lookup"><span data-stu-id="fc805-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="fc805-132">Выберите вкладку **Рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="fc805-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="fc805-133">Установите для параметра **Включить уведомления для приложения Teams** значение **Да**, чтобы включить уведомления для пользователя, или значение **Нет**, чтобы отключить уведомления для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc805-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Включение уведомлений приложения Teams в параметрах пользователя на вкладке рабочего процесса](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="fc805-135">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fc805-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="fc805-136">Поддерживаемые языки</span><span class="sxs-lookup"><span data-stu-id="fc805-136">Supported languages</span></span>

<span data-ttu-id="fc805-137">Приложение Dynamics 365 Human Resources в Teams поддерживает следующие языки:</span><span class="sxs-lookup"><span data-stu-id="fc805-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="fc805-138">Код языка</span><span class="sxs-lookup"><span data-stu-id="fc805-138">Locale ID</span></span> | <span data-ttu-id="fc805-139">Язык</span><span class="sxs-lookup"><span data-stu-id="fc805-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="fc805-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="fc805-140">de-DE</span></span> | <span data-ttu-id="fc805-141">Немецкий (Германия)</span><span class="sxs-lookup"><span data-stu-id="fc805-141">German (Germany)</span></span> |
| <span data-ttu-id="fc805-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="fc805-142">es-ES</span></span> | <span data-ttu-id="fc805-143">Испанский (Испания)</span><span class="sxs-lookup"><span data-stu-id="fc805-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="fc805-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="fc805-144">es-MX</span></span> | <span data-ttu-id="fc805-145">Испанский (Мексика)</span><span class="sxs-lookup"><span data-stu-id="fc805-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="fc805-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="fc805-146">fr-CA</span></span> | <span data-ttu-id="fc805-147">Французский (Канада)</span><span class="sxs-lookup"><span data-stu-id="fc805-147">French (Canada)</span></span> |
| <span data-ttu-id="fc805-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="fc805-148">fr-FR</span></span> | <span data-ttu-id="fc805-149">Французский (Франция)</span><span class="sxs-lookup"><span data-stu-id="fc805-149">French (France)</span></span> |
| <span data-ttu-id="fc805-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="fc805-150">it-IT</span></span> | <span data-ttu-id="fc805-151">Итальянский (Италия)</span><span class="sxs-lookup"><span data-stu-id="fc805-151">Italian (Italy)</span></span> |
| <span data-ttu-id="fc805-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="fc805-152">nl-NL</span></span> | <span data-ttu-id="fc805-153">Нидерландский (Нидерланды)</span><span class="sxs-lookup"><span data-stu-id="fc805-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="fc805-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="fc805-154">pt-BR</span></span> | <span data-ttu-id="fc805-155">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="fc805-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="fc805-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="fc805-156">tr-TR</span></span> | <span data-ttu-id="fc805-157">Турецкий (Турция)</span><span class="sxs-lookup"><span data-stu-id="fc805-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="fc805-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="fc805-158">zh-CN</span></span> | <span data-ttu-id="fc805-159">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="fc805-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="fc805-160">Основание</span><span class="sxs-lookup"><span data-stu-id="fc805-160">Notes</span></span>

<span data-ttu-id="fc805-161">Следующие рабочие элементы включены в будущие выпуски:</span><span class="sxs-lookup"><span data-stu-id="fc805-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="fc805-162">Рабочий элемент</span><span class="sxs-lookup"><span data-stu-id="fc805-162">Work item</span></span> | <span data-ttu-id="fc805-163">Состояние</span><span class="sxs-lookup"><span data-stu-id="fc805-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="fc805-164">Неверное сальдо при подаче запроса на отпуск для будущей даты.</span><span class="sxs-lookup"><span data-stu-id="fc805-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="fc805-165">Прогнозирование пока недоступно.</span><span class="sxs-lookup"><span data-stu-id="fc805-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="fc805-166">Сальдо отображается для текущей даты.</span><span class="sxs-lookup"><span data-stu-id="fc805-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="fc805-167">Не удается отменить запрос **На рассмотрении**.</span><span class="sxs-lookup"><span data-stu-id="fc805-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="fc805-168">Эта функциональная возможность в настоящее время не поддерживается и будет добавлена в будущем выпуске.</span><span class="sxs-lookup"><span data-stu-id="fc805-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="fc805-169">Сведения о сальдо рассчитываются на сегодняшний день.</span><span class="sxs-lookup"><span data-stu-id="fc805-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="fc805-170">В настоящее время в системе не отображается сальдо на период начисления, даже если оно настроено в параметрах отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="fc805-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="fc805-171">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="fc805-171">Troubleshooting</span></span>

<span data-ttu-id="fc805-172">Если пользователь не может войти в систему или использовать приложение Human Resources Teams, попробуйте выполнить следующие инструкции по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="fc805-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="fc805-173">Если после устранения неполадок все еще возникают проблемы, обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="fc805-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="fc805-174">Для получения дополнительных см. [Получение поддержки](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="fc805-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="fc805-175">Невозможно выполнить вход в приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="fc805-176">Если пользователь обращается к вам из-за того, что он не может войти в приложение, убедитесь, что у пользователя имеется соответствующая запись сотрудника в управлении персоналом.</span><span class="sxs-lookup"><span data-stu-id="fc805-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="fc805-177">Ошибка при утверждении запросов отпуска в приложении Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="fc805-178">Если пользователь получает ошибку при попытке утверждения запросов на отпуск в приложении Teams выполните следующие действия по устранению неполадок:</span><span class="sxs-lookup"><span data-stu-id="fc805-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="fc805-179">Убедитесь, что их учетная запись Teams совпадает с той, которая используется для доступа к модулю Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fc805-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="fc805-180">Проверьте, что они действительно являются утверждающим для этого запроса, проверив параметры рабочего процесса для утверждения отпуска.</span><span class="sxs-lookup"><span data-stu-id="fc805-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="fc805-181">Дополнительные сведения о рабочих процессах запроса отпуска см. в разделе [Создание рабочего процесса запроса отпуска](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="fc805-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="fc805-182">Утверждающие отпуска не получают сообщения чата Teams для утверждения запросов на отпуск</span><span class="sxs-lookup"><span data-stu-id="fc805-182">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="fc805-183">Убедитесь, что для среды и пользователя включены уведомления.</span><span class="sxs-lookup"><span data-stu-id="fc805-183">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="fc805-184">Дополнительные сведения см. в [Включение уведомлений для приложения Human Resources в Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) и [Включение и выключение уведомлений Teams для отдельных пользователей](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="fc805-184">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="fc805-185">Убедитесь, что пользователи вошли в систему на вкладке **Чаты** с теми же учетными данными, которые используются для утверждения запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="fc805-185">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="fc805-186">Используйте сообщения "выйти", а затем "войти", чтобы войти в систему, используя правильные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="fc805-186">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="fc805-187">Если проблема сохраняется, проверьте статус пакетного задания системы бизнес-событий как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="fc805-187">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="fc805-188">Если он находится на ожидающем или выполняющемся этапе, проверьте через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="fc805-188">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="fc805-189">Если статус не меняется, отправьте запрос в службу поддержки, чтобы ее сотрудники могли помочь в устранении проблемы.</span><span class="sxs-lookup"><span data-stu-id="fc805-189">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="fc805-190">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="fc805-190">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="fc805-191">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="fc805-191">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="fc805-192">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="fc805-192">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="fc805-193">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="fc805-193">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="fc805-194">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="fc805-194">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="fc805-195">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="fc805-195">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="fc805-196">Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc805-196">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span>

<span data-ttu-id="fc805-197">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="fc805-197">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="fc805-198">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fc805-198">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="fc805-199">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="fc805-199">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="fc805-200">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="fc805-200">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="fc805-201">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="fc805-201">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="fc805-202">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="fc805-202">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="fc805-203">Microsoft Teams, сетка событий Azure и Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="fc805-203">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="fc805-204">При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Microsoft Teams некоторые клиентские данные могут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="fc805-204">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="fc805-205">Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fc805-205">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="fc805-206">Эти данные могут храниться в сетке событий Microsoft Azure в течение 24 часов и будут обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="fc805-206">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="fc805-207">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="fc805-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="fc805-208">При взаимодействии с чат-ботом в приложении Human Resources содержимое беседы может храниться в Azure Cosmos DB и передаваться в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fc805-208">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="fc805-209">Эти данные могут храниться в Azure Cosmos DB течение 24 часов и могут быть обработаны вне географического региона, в котором развернута служба Human Resources для клиента, шифруются при передачи и хранении, и не используется корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="fc805-209">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="fc805-210">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="fc805-210">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="fc805-211">Для ограничения доступа к приложению Human Resources в Microsoft Teams для вашей организации или пользователей в организации см. раздел [Управление политиками разрешений приложений в Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="fc805-211">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc805-212">См. также</span><span class="sxs-lookup"><span data-stu-id="fc805-212">See also</span></span> 

[<span data-ttu-id="fc805-213">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-213">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="fc805-214">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-214">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="fc805-215">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="fc805-215">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]