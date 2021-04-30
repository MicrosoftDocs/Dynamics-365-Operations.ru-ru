---
title: Управление запросами на отпуск в Teams
description: В этом разделе показано, как запросить отпуск в приложении Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 48bf6f7997d6159077419bcd05d27fd711c8fb4b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891038"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="dc667-103">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dc667-104">Приложение Dynamics 365 Human Resources в Microsoft Teams позволяет быстро запросить отпуск и просмотреть сведения о балансе времени прямо в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="dc667-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="dc667-105">Можно взаимодействовать с ботом для запроса информации и запуска запроса на отгул.</span><span class="sxs-lookup"><span data-stu-id="dc667-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="dc667-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="dc667-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="dc667-107">Также можно отправлять пользователям сведения о предстоящих отгулах в Teams и чатах вне приложения управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="dc667-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="dc667-108">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="dc667-108">Install the app</span></span>

<span data-ttu-id="dc667-109">Приложение Dynamics 365 Human Resources можно найти в магазине Teams.</span><span class="sxs-lookup"><span data-stu-id="dc667-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="dc667-110">В Microsoft Teams выберите многоточие.</span><span class="sxs-lookup"><span data-stu-id="dc667-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Многоточие приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="dc667-112">Выполните поиск Dynamics 365 Human Resources, а затем выберите плитку **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="dc667-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Плитка HR приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="dc667-114">Для установки приложения нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="dc667-114">Select the **Add** button to install the app.</span></span>

   ![Установка приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="dc667-116">Если приложение не выполняет автоматический вход, выберите вкладку **Параметры**, чтобы выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="dc667-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Вкладка Параметры приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="dc667-118">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="dc667-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="dc667-119">Если имеется доступ к нескольким экземплярам "Human Resources", можно выбрать среду, к которой необходимо подключиться, на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="dc667-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="dc667-120">Приложение теперь поддерживает роль безопасности системного администратора.</span><span class="sxs-lookup"><span data-stu-id="dc667-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="dc667-121">Использование бота</span><span class="sxs-lookup"><span data-stu-id="dc667-121">Use the bot</span></span>

<span data-ttu-id="dc667-122">После установки приложения появится приветственное сообщение, позволяющее знать типы действий, которые может выполнять бот от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="dc667-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Приветственное сообщение бота для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="dc667-124">При первом взаимодействии с ботом может потребоваться выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="dc667-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="dc667-125">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="dc667-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="dc667-126">Можно спросить бота о следующем:</span><span class="sxs-lookup"><span data-stu-id="dc667-126">You can ask the bot to:</span></span>

- <span data-ttu-id="dc667-127">Запустите запрос на отпуск для вас.</span><span class="sxs-lookup"><span data-stu-id="dc667-127">Start a leave request for you.</span></span>

  ![Начало запроса на отпуск в чате Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="dc667-129">Чат-бот будет заполнять запрос на отпуска.</span><span class="sxs-lookup"><span data-stu-id="dc667-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="dc667-130">Выберите **Запрос на отгул** и измените сведения для запроса.</span><span class="sxs-lookup"><span data-stu-id="dc667-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Изменение сведений запроса отпуска](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="dc667-132">Закончив редактирование сведений о запросе на отпуск, нажмите кнопку **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="dc667-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Отправить запрос на отпуск](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="dc667-134">Управление отпуском в Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-134">Manage your leave in Teams</span></span>

<span data-ttu-id="dc667-135">Вкладка **Отгул** служит для просмотра следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="dc667-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="dc667-136">Сведения о балансе времени для каждого типа отпусков, которые вам назначены</span><span class="sxs-lookup"><span data-stu-id="dc667-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="dc667-137">Предстоящие запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="dc667-137">Upcoming leave requests</span></span>

- <span data-ttu-id="dc667-138">Запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="dc667-138">Time-off requests</span></span>

- <span data-ttu-id="dc667-139">Черновые запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="dc667-139">Draft leave requests</span></span>

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="dc667-141">Создание нового запроса</span><span class="sxs-lookup"><span data-stu-id="dc667-141">Create a new request</span></span>

1. <span data-ttu-id="dc667-142">Выберите **Новый запрос** для создания нового запроса на отпуск.</span><span class="sxs-lookup"><span data-stu-id="dc667-142">To create a new leave request, select **New request**.</span></span>

   ![Новый запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="dc667-144">Введите день или дни, которые требуется взять отпуск, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="dc667-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Добавить отпуск для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="dc667-146">Если применимо, введите код причины.</span><span class="sxs-lookup"><span data-stu-id="dc667-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="dc667-147">Кроме того, необходимо ввести комментарии и добавить вложения.</span><span class="sxs-lookup"><span data-stu-id="dc667-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="dc667-148">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="dc667-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="dc667-149">Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="dc667-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="dc667-150">Управление черновыми запросами</span><span class="sxs-lookup"><span data-stu-id="dc667-150">Manage draft requests</span></span>

1. <span data-ttu-id="dc667-151">Выберите вкладку **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="dc667-151">Select the **Drafts** tab.</span></span>

   ![Вкладка Черновики для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="dc667-153">Выберите карандаш для редактирования запроса или выберите корзину, чтобы удалить запрос.</span><span class="sxs-lookup"><span data-stu-id="dc667-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="dc667-154">Внесите любые необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="dc667-154">Make any necessary changes.</span></span> <span data-ttu-id="dc667-155">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="dc667-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="dc667-156">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="dc667-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Изменить черновик для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="dc667-158">Реагирование на уведомления Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-158">Respond to Teams notifications</span></span>

<span data-ttu-id="dc667-159">Если вы или сотрудник, для которого вы являетесь утверждающим, отправляете запрос на отпуск, вы получите уведомление в приложении Human Resources в Teams.</span><span class="sxs-lookup"><span data-stu-id="dc667-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="dc667-160">Можно выбрать уведомление для его просмотра.</span><span class="sxs-lookup"><span data-stu-id="dc667-160">You can select the notification to view it.</span></span> <span data-ttu-id="dc667-161">Уведомления также появляются в области **Чат**.</span><span class="sxs-lookup"><span data-stu-id="dc667-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="dc667-162">Если вы являетесь утверждающим, вы можете выбрать **Утвердить** или **Отклонить** в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="dc667-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="dc667-163">Кроме того, можно указать необязательное сообщение.</span><span class="sxs-lookup"><span data-stu-id="dc667-163">You can also provide an optional message.</span></span>

![Уведомление о запросе отпуска в приложении Human Resources в Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="dc667-165">Отправка сведений о предстоящих отгулах вашим коллегам</span><span class="sxs-lookup"><span data-stu-id="dc667-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="dc667-166">После установки приложения Human Resources для Teams можно легко отправлять сведения о предстоящем времени отгулов вашим коллегам в группах или чатах.</span><span class="sxs-lookup"><span data-stu-id="dc667-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="dc667-167">В рабочей группе или чате в Teams выберите кнопку Human Resources под окном чата.</span><span class="sxs-lookup"><span data-stu-id="dc667-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Кнопка Human Resources под окном чата](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="dc667-169">Выберите запрос отпуска, которым необходимо поделиться.</span><span class="sxs-lookup"><span data-stu-id="dc667-169">Select the leave request you want to share.</span></span> <span data-ttu-id="dc667-170">Если требуется поделиться черновиком запроса отпуска, сначала выберите **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="dc667-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Выбор предстоящего запроса отпуска для общего доступа](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="dc667-172">Ваш запрос отпуска будет отображен в чате.</span><span class="sxs-lookup"><span data-stu-id="dc667-172">Your leave request will display in the chat.</span></span>

![Карточка запроса отпуска в Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="dc667-174">Если поделиться черновиком запроса отпуска, он будет выведен в качестве черновика:</span><span class="sxs-lookup"><span data-stu-id="dc667-174">If you shared a draft request, it will display as a draft:</span></span>

![Карточка черновика запроса отпуска в Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="dc667-176">Просмотр календаря отпусков рабочей группы</span><span class="sxs-lookup"><span data-stu-id="dc667-176">View your team's leave calendar</span></span>

<span data-ttu-id="dc667-177">Если вы являетесь руководителем с непосредственными подчиненными, вы можете просмотреть утвержденные и ожидающие утверждения запросы отгулов для вашей рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="dc667-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="dc667-178">В приложении Human Resources app в Teams выберите **Отгул**.</span><span class="sxs-lookup"><span data-stu-id="dc667-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="dc667-179">Выберите **Календарь рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="dc667-179">Select **Team calendar**.</span></span> <span data-ttu-id="dc667-180">В календаре отображаются утвержденные и ожидающие утверждения отгулы ваших непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="dc667-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Просмотр календаря в приложении Human Resources в Teams](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="dc667-182">Если календарь рабочей группы не отображается, попросите администратора включить его.</span><span class="sxs-lookup"><span data-stu-id="dc667-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="dc667-183">Дополнительные сведения см. в разделе [Установка и настройка](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="dc667-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="dc667-184">Поддерживаемые языки</span><span class="sxs-lookup"><span data-stu-id="dc667-184">Supported languages</span></span>

<span data-ttu-id="dc667-185">Приложение Dynamics 365 Human Resources в Teams поддерживает следующие языки:</span><span class="sxs-lookup"><span data-stu-id="dc667-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="dc667-186">Код языка</span><span class="sxs-lookup"><span data-stu-id="dc667-186">Locale ID</span></span> | <span data-ttu-id="dc667-187">Язык</span><span class="sxs-lookup"><span data-stu-id="dc667-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="dc667-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="dc667-188">de-DE</span></span> | <span data-ttu-id="dc667-189">Немецкий (Германия)</span><span class="sxs-lookup"><span data-stu-id="dc667-189">German (Germany)</span></span> |
| <span data-ttu-id="dc667-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="dc667-190">es-ES</span></span> | <span data-ttu-id="dc667-191">Испанский (Испания)</span><span class="sxs-lookup"><span data-stu-id="dc667-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="dc667-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="dc667-192">es-MX</span></span> | <span data-ttu-id="dc667-193">Испанский (Мексика)</span><span class="sxs-lookup"><span data-stu-id="dc667-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="dc667-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="dc667-194">fr-CA</span></span> | <span data-ttu-id="dc667-195">Французский (Канада)</span><span class="sxs-lookup"><span data-stu-id="dc667-195">French (Canada)</span></span> |
| <span data-ttu-id="dc667-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="dc667-196">fr-FR</span></span> | <span data-ttu-id="dc667-197">Французский (Франция)</span><span class="sxs-lookup"><span data-stu-id="dc667-197">French (France)</span></span> |
| <span data-ttu-id="dc667-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="dc667-198">it-IT</span></span> | <span data-ttu-id="dc667-199">Итальянский (Италия)</span><span class="sxs-lookup"><span data-stu-id="dc667-199">Italian (Italy)</span></span> |
| <span data-ttu-id="dc667-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="dc667-200">nl-NL</span></span> | <span data-ttu-id="dc667-201">Нидерландский (Нидерланды)</span><span class="sxs-lookup"><span data-stu-id="dc667-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="dc667-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="dc667-202">pt-BR</span></span> | <span data-ttu-id="dc667-203">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="dc667-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="dc667-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="dc667-204">tr-TR</span></span> | <span data-ttu-id="dc667-205">Турецкий (Турция)</span><span class="sxs-lookup"><span data-stu-id="dc667-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="dc667-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="dc667-206">zh-CN</span></span> | <span data-ttu-id="dc667-207">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="dc667-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="dc667-208">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="dc667-208">Troubleshooting</span></span>

<span data-ttu-id="dc667-209">Если вы не можете войти в систему или использовать приложение Dynamics 365 Human Resources Teams, попробуйте выполнить следующие инструкции по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="dc667-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="dc667-210">Если после устранения неполадок все еще возникают проблемы, обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="dc667-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="dc667-211">Для получения дополнительных см. [Получение поддержки](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="dc667-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="dc667-212">Невозможно выполнить вход в приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="dc667-213">Если вы не можете войти в приложение, возможно, что учетная запись, используемая для входа в Microsoft Teams, не связана с записью сотрудника в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc667-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="dc667-214">Обратитесь к системному администратору, чтобы убедиться, что запись сотрудника правильно связана.</span><span class="sxs-lookup"><span data-stu-id="dc667-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="dc667-215">Переводы выводятся неправильно</span><span class="sxs-lookup"><span data-stu-id="dc667-215">Translations don't display correctly</span></span>

<span data-ttu-id="dc667-216">Если переводы не показываются, как ожидалось, убедитесь, что язык, выбранный в Teams, совпадает с языком, выбранным в разделе **Параметры пользователя** в модуле управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="dc667-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="dc667-217">В Teams проверьте **Язык приложения** в **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="dc667-217">In Teams, look at **App language** in **Settings**.</span></span>

![Параметры Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="dc667-219">В модуле управления персоналом выберите **Параметры**, а затем выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="dc667-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="dc667-220">Убедитесь, что поле **Язык** соответствует полю **Язык приложения** в Teams.</span><span class="sxs-lookup"><span data-stu-id="dc667-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Параметры пользователя управления персоналом](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="dc667-222">Если проблемы с переводом не устранены, сообщите нам о них.</span><span class="sxs-lookup"><span data-stu-id="dc667-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="dc667-223">Сведения см. в разделе [Получение поддержки для приложений Finance and Operations или Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="dc667-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="dc667-224">Ошибка при утверждении запросов отпуска в приложении Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="dc667-225">При получении сообщения об ошибке при попытке утверждения запросов на отпуск в приложении Teams попробуйте выполнить следующие действия по устранению неполадок:</span><span class="sxs-lookup"><span data-stu-id="dc667-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="dc667-226">Убедитесь, что учетная запись, в которую вы входите в Microsoft Teams, совпадает с используемой для доступа в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc667-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="dc667-227">Проверьте, что вы действительно являетесь утверждающим для этого запроса, проверив параметры рабочего процесса для утверждения отпуска.</span><span class="sxs-lookup"><span data-stu-id="dc667-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="dc667-228">Дополнительные сведения о рабочих процессах запроса отпуска см. в разделе [Создание рабочего процесса запроса отпуска](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="dc667-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="dc667-229">Известные проблемы со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="dc667-229">Known accessibility issues</span></span>

<span data-ttu-id="dc667-230">Приложение Human Resources в Teams обладает следующими проблемами специальных возможностей, над которыми мы работаем, чтобы устранить их в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="dc667-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="dc667-231">Расход</span><span class="sxs-lookup"><span data-stu-id="dc667-231">Issue</span></span> | <span data-ttu-id="dc667-232">Временное решение или объяснение</span><span class="sxs-lookup"><span data-stu-id="dc667-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="dc667-233">При увеличении до 400% на рабочем столе скрываются из вида некоторые кнопки действий.</span><span class="sxs-lookup"><span data-stu-id="dc667-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="dc667-234">Рекомендуется использовать экранную лупу вместо этого, пока мы не сможем поддерживать этот уровень масштабирования.</span><span class="sxs-lookup"><span data-stu-id="dc667-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="dc667-235">На вкладке **Отгулы** средство VoiceOver объявляет действие кнопки при чтении заголовка для сетки отгулов.</span><span class="sxs-lookup"><span data-stu-id="dc667-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="dc667-236">Заголовок и элементы в сетке группируются по годам, и их можно свернуть.</span><span class="sxs-lookup"><span data-stu-id="dc667-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="dc667-237">Средство VoiceOver интерпретирует это как элемент действия, но это не так.</span><span class="sxs-lookup"><span data-stu-id="dc667-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="dc667-238">На вкладке **Отгулы** имеется дополнительный жест прокрутки при переходе к полю **Код причины** в новом запросе.</span><span class="sxs-lookup"><span data-stu-id="dc667-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="dc667-239">Нет скрытого элемента управления, к которому пытается перейти навигация при прокрутке.</span><span class="sxs-lookup"><span data-stu-id="dc667-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="dc667-240">На вкладке **Отгулы** если вы проведите пальцем, когда календарь открыт, вы выходите за пределы элемента управления, а не переходите наверх в новом запросе или при редактировании запроса.</span><span class="sxs-lookup"><span data-stu-id="dc667-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="dc667-241">При достижении **К сегодняшней дате** считайте, что это конец элемента управления, и прокручивайте в обратном направлении, чтобы вернуться к началу.</span><span class="sxs-lookup"><span data-stu-id="dc667-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="dc667-242">На вкладке **Чат** фокус перемещается назад к началу, когда пользователь вводит дату при использовании вспомогательного средства или навигации с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="dc667-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="dc667-243">Нажимайте клавишу TAB, пока не будет снова достигнута область ввода.</span><span class="sxs-lookup"><span data-stu-id="dc667-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="dc667-244">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="dc667-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="dc667-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="dc667-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="dc667-246">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="dc667-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="dc667-247">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="dc667-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="dc667-248">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="dc667-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="dc667-249">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="dc667-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="dc667-250">Затем эта информация передается в Microsoft  [Azure bot framework](https://azure.microsoft.com/services/bot-service/), которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc667-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="dc667-251">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="dc667-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="dc667-252">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc667-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="dc667-253">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="dc667-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="dc667-254">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dc667-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="dc667-255">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="dc667-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="dc667-256">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="dc667-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="dc667-257">Microsoft Teams, сетка событий Azure и Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="dc667-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="dc667-258">При использовании функции уведомлений для приложения Dynamics 365 Human Resources в Microsoft Teams некоторые клиентские данные могут выходить из географического региона, в котором развернута служба Human Resources вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="dc667-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="dc667-259">Dynamics 365 Human Resources передает сведения о запросе отпуска сотрудника и задачах рабочего процесса в сетку событий Microsoft Azure и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="dc667-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="dc667-260">Эти данные могут храниться в сетке событий Microsoft Azure в течение 24 часов и будут обрабатываться в США, шифруются при передаче и при хранении, и не используются корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dc667-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="dc667-261">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="dc667-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="dc667-262">При взаимодействии с чат-ботом в приложении Human Resources содержимое беседы может храниться в Azure Cosmos DB и передаваться в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="dc667-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="dc667-263">Эти данные могут храниться в Azure Cosmos DB течение 24 часов и могут быть обработаны вне географического региона, в котором развернута служба Human Resources для клиента, шифруются при передачи и хранении, и не используется корпорацией Майкрософт или ее подсистемами для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dc667-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="dc667-264">Чтобы понять, где хранятся данные в Teams, см. раздел: [Местоположение данных в Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="dc667-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="dc667-265">Для ограничения доступа к приложению Human Resources в Microsoft Teams для вашей организации или пользователей в организации см. раздел [Управление политиками разрешений приложений в Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="dc667-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="dc667-266">См. также</span><span class="sxs-lookup"><span data-stu-id="dc667-266">See also</span></span>

[<span data-ttu-id="dc667-267">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="dc667-268">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="dc667-269">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="dc667-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]