---
title: Управление запросами на отпуск в Teams
description: В этом разделе показано, как запросить отпуск в приложении Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428836"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="802d1-103">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="802d1-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="802d1-104">Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет быстро запросить отпуск и просмотреть сведения о балансе времени прямо в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="802d1-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="802d1-105">Можно взаимодействовать с ботом для запроса информации.</span><span class="sxs-lookup"><span data-stu-id="802d1-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="802d1-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="802d1-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="802d1-107">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="802d1-107">Install the app</span></span>

<span data-ttu-id="802d1-108">Приложение "Human Resources" можно найти в магазине "Teams".</span><span class="sxs-lookup"><span data-stu-id="802d1-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="802d1-109">В Microsoft Teams выберите многоточие.</span><span class="sxs-lookup"><span data-stu-id="802d1-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Многоточие приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="802d1-111">Выполните поиск Dynamics 365 Human Resources, а затем выберите плитку **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="802d1-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Плитка HR приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="802d1-113">Для установки приложения нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="802d1-113">Select the **Add** button to install the app.</span></span>

   ![Установка приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="802d1-115">Если приложение не выполняет автоматический вход, выберите вкладку **Параметры**, чтобы выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="802d1-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Вкладка Параметры приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="802d1-117">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="802d1-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="802d1-118">Если имеется доступ к нескольким экземплярам "Human Resources", можно выбрать среду, к которой необходимо подключиться, на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="802d1-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="802d1-119">Приложение в настоящее время не поддерживает роль "системный администратор" и выводит сообщение об ошибке, если вход осуществляется с учетной записью системного администратора.</span><span class="sxs-lookup"><span data-stu-id="802d1-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="802d1-120">Чтобы войти с использованием других учетных записей, на вкладке **Параметры** нажмите кнопку **переключателя счетов**, а затем выполните вход с учетной записью пользователя, не обладающей правами администратора системы.</span><span class="sxs-lookup"><span data-stu-id="802d1-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="802d1-121">Использование бота</span><span class="sxs-lookup"><span data-stu-id="802d1-121">Use the bot</span></span>

<span data-ttu-id="802d1-122">После установки приложения появится приветственное сообщение, позволяющее знать типы действий, которые может выполнять бот от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="802d1-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Приветственное сообщение бота для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="802d1-124">При первом взаимодействии с ботом может потребоваться выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="802d1-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="802d1-125">Если диалоговое окно входа не отображается, проверьте настройки обозревателя, чтобы разрешить всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="802d1-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="802d1-126">Можно спросить бота о следующем:</span><span class="sxs-lookup"><span data-stu-id="802d1-126">You can ask the bot to:</span></span>

- <span data-ttu-id="802d1-127">Отображение сведений о балансе времени для каждого типа отпусков, которые вам назначены.</span><span class="sxs-lookup"><span data-stu-id="802d1-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Показать балансы приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="802d1-129">Отображение дополнительных сведений о конкретном типе отпуска.</span><span class="sxs-lookup"><span data-stu-id="802d1-129">Show additional details about a specific leave type.</span></span>

   ![Показать сведения приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="802d1-131">Запустите запрос на отпуск для вас.</span><span class="sxs-lookup"><span data-stu-id="802d1-131">Start a leave request for you.</span></span>

   ![Запрос на отпуск приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="802d1-133">После запуска запроса на отпуск вы можете скорректировать дни в пределах карточки или выбрать параметр **Изменить сведения**, чтобы добавить дополнительные сведения о запросе.</span><span class="sxs-lookup"><span data-stu-id="802d1-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Изменить запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="802d1-135">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="802d1-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="802d1-136">Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="802d1-136">You can also type **Save as draft** to come back to it later.</span></span>

![Отправка запросов для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="802d1-138">Управление отпуском в Teams</span><span class="sxs-lookup"><span data-stu-id="802d1-138">Manage your leave in Teams</span></span>

<span data-ttu-id="802d1-139">Вкладка **Отгул** служит для просмотра следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="802d1-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="802d1-140">Сведения о балансе времени для каждого типа отпусков, которые вам назначены</span><span class="sxs-lookup"><span data-stu-id="802d1-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="802d1-141">Предстоящие запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="802d1-141">Upcoming leave requests</span></span>

- <span data-ttu-id="802d1-142">Запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="802d1-142">Time-off requests</span></span>

- <span data-ttu-id="802d1-143">Черновые запросы на отпуск</span><span class="sxs-lookup"><span data-stu-id="802d1-143">Draft leave requests</span></span>

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="802d1-145">Создание нового запроса</span><span class="sxs-lookup"><span data-stu-id="802d1-145">Create a new request</span></span>

1. <span data-ttu-id="802d1-146">Выберите **Новый запрос** для создания нового запроса на отпуск.</span><span class="sxs-lookup"><span data-stu-id="802d1-146">To create a new leave request, select **New request**.</span></span>

   ![Новый запрос для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="802d1-148">Введите день или дни, которые требуется взять отпуск, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="802d1-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Добавить отпуск для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="802d1-150">Если применимо, введите код причины.</span><span class="sxs-lookup"><span data-stu-id="802d1-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="802d1-151">Кроме того, необходимо ввести комментарии и добавить вложения.</span><span class="sxs-lookup"><span data-stu-id="802d1-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="802d1-152">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="802d1-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="802d1-153">Можно также ввести **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="802d1-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="802d1-154">Управление черновыми запросами</span><span class="sxs-lookup"><span data-stu-id="802d1-154">Manage draft requests</span></span>

1. <span data-ttu-id="802d1-155">Выберите вкладку **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="802d1-155">Select the **Drafts** tab.</span></span>

   ![Вкладка Черновики для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="802d1-157">Выберите карандаш для редактирования запроса или выберите корзину, чтобы удалить запрос.</span><span class="sxs-lookup"><span data-stu-id="802d1-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="802d1-158">Внесите любые необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="802d1-158">Make any necessary changes.</span></span> <span data-ttu-id="802d1-159">По завершении ввода данных введите **Отправить**, чтобы отправить его на утверждение.</span><span class="sxs-lookup"><span data-stu-id="802d1-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="802d1-160">Можно также выбрать **Сохранить как черновик**, чтобы вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="802d1-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Изменить черновик для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="802d1-162">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="802d1-162">Privacy notice</span></span>

<span data-ttu-id="802d1-163">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="802d1-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="802d1-164">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="802d1-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="802d1-165">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="802d1-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="802d1-166">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="802d1-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="802d1-167">Затем эта информация передается в Microsoft [Azure bot framework](https://azure.microsoft.com/services/bot-service/) , которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="802d1-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="802d1-168">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="802d1-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="802d1-169">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="802d1-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="802d1-170">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="802d1-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="802d1-171">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="802d1-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="802d1-172">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="802d1-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="802d1-173">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="802d1-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="802d1-174">См. также</span><span class="sxs-lookup"><span data-stu-id="802d1-174">See also</span></span>

[<span data-ttu-id="802d1-175">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="802d1-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="802d1-176">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="802d1-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="802d1-177">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="802d1-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
