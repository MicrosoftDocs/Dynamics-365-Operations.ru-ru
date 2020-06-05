---
title: Приложение Human Resources в Teams
description: Эта тема знакомит с приложением Microsoft Dynamics 365 Human Resources в Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388124"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="b0126-103">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="b0126-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="b0126-104">Приложение Microsoft Dynamics 365 Human Resources в Microsoft Teams позволяет сотрудникам быстро запросить отпуск и просмотреть сведения о балансе времени в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b0126-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="b0126-105">Сотрудники могут взаимодействовать с ботом для запроса информации.</span><span class="sxs-lookup"><span data-stu-id="b0126-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="b0126-106">Вкладка **Отгул** содержит более детальная информация.</span><span class="sxs-lookup"><span data-stu-id="b0126-106">The **Time off** tab provides more detailed information.</span></span>

![Бот для приложения отпусков Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Вкладка Отгул для приложения отпусков Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="b0126-109">Установка и настройка</span><span class="sxs-lookup"><span data-stu-id="b0126-109">Install and setup</span></span>

<span data-ttu-id="b0126-110">Приложение "Human Resources" можно найти в магазине "Teams".</span><span class="sxs-lookup"><span data-stu-id="b0126-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="b0126-111">Сведения об установке приложения Teams см. в разделе [Управление запросами на отпуск в Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="b0126-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="b0126-112">Сведения об управлении разрешениями приложений в Teams см. в разделе [Управление политиками разрешений приложений в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="b0126-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="b0126-113">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="b0126-113">Known issues</span></span>

| <span data-ttu-id="b0126-114">Расход</span><span class="sxs-lookup"><span data-stu-id="b0126-114">Issue</span></span> | <span data-ttu-id="b0126-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="b0126-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="b0126-116">Неверное сальдо при подаче запроса на отпуск для будущей даты.</span><span class="sxs-lookup"><span data-stu-id="b0126-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="b0126-117">Прогнозирование пока недоступно.</span><span class="sxs-lookup"><span data-stu-id="b0126-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="b0126-118">Сальдо отображается для текущей даты.</span><span class="sxs-lookup"><span data-stu-id="b0126-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="b0126-119">При уменьшении количества часов, взятых в существующем запросе, **Остаток сальдо** уменьшается вместо увеличения.</span><span class="sxs-lookup"><span data-stu-id="b0126-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="b0126-120">Мы решим эту известную проблему в будущем.</span><span class="sxs-lookup"><span data-stu-id="b0126-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="b0126-121">Отображение неверно, но правильные суммы корректируются при отправке.</span><span class="sxs-lookup"><span data-stu-id="b0126-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="b0126-122">Две карточки **предстоящих отпусков** отображаются для одних и тех же дат.</span><span class="sxs-lookup"><span data-stu-id="b0126-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="b0126-123">Карточки представляют собой отдельные отправки.</span><span class="sxs-lookup"><span data-stu-id="b0126-123">The cards represent individual submissions.</span></span> <span data-ttu-id="b0126-124">Мы будем продолжать получать отзывы и корректировки.</span><span class="sxs-lookup"><span data-stu-id="b0126-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="b0126-125">Не удается отменить запрос **На рассмотрении**.</span><span class="sxs-lookup"><span data-stu-id="b0126-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="b0126-126">Эта функциональная возможность в настоящее время не поддерживается и будет добавлена в будущем выпуске.</span><span class="sxs-lookup"><span data-stu-id="b0126-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="b0126-127">Сведения о сальдо рассчитываются на сегодняшний день.</span><span class="sxs-lookup"><span data-stu-id="b0126-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="b0126-128">В настоящее время в системе не отображается сальдо на период начисления, даже если оно настроено в параметрах отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="b0126-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="b0126-129">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="b0126-129">Privacy notice</span></span>

<span data-ttu-id="b0126-130">При помощи бота Dynamics 365 Human Resources в Microsoft Teams входные данные пользователя обрабатываются для понимания соответствующего запроса/цели.</span><span class="sxs-lookup"><span data-stu-id="b0126-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="b0126-131">Введенные пользователем данные, такие как "Поиск по счету Contoso", направляются в одну из функций Microsoft Cognitive Service, называемой Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="b0126-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="b0126-132">Узнайте подробнее о LUIS [здесь](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="b0126-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="b0126-133">Служба LUIS устраняет неоднозначность или понимает цель ввода данных пользователем (в данном случае, целью является поиск информации) и целевого объекта (в данном случае предполагаемая объект — это учетная запись под названием Contoso).</span><span class="sxs-lookup"><span data-stu-id="b0126-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="b0126-134">Затем эта информация передается в Microsoft [Azure bot framework](https://azure.microsoft.com/services/bot-service/) , которая взаимодействует с данными из Dynamics 365 Human Resources и извлекает их для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0126-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="b0126-135">Установив и разрешив доступ к использованию бота, вы соглашаетесь разрешить службе LUIS и Azure Bot Framework обрабатывать цель входных данных, что приводит к расширенному взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="b0126-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="b0126-136">Сравнение службы LUIS и Azure Bot Framework может иметь различные уровни соответствия по сравнению с Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b0126-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b0126-137">Хотя у службы LUIS есть доступ только к пользовательским запросам и она не предназначена для подключения к данным пользователя или учетной записи Dynamics 365 Human Resources, пользователь бота Dynamics 365 Human Resources может добровольно ввести запрос, содержащий данные о клиентах, личные данные или другие данные, которые могут быть отправлены в службу LUIS и Azure Bot Framework.</span><span class="sxs-lookup"><span data-stu-id="b0126-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="b0126-138">Содержимое пользовательских запросов и сообщений сохраняется в системе LUIS не более 30 дней, шифруется в состоянии покоя и не используется для обучения или улучшения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b0126-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="b0126-139">Дополнительные сведения Cognitive Services см. [здесь](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="b0126-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="b0126-140">Чтобы настроить параметры администрирования для приложений в Microsoft Teams, перейдите в [центр администрирования Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="b0126-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="b0126-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b0126-141">See also</span></span> 

[<span data-ttu-id="b0126-142">Загрузка и установка Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0126-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="b0126-143">Центр справки Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0126-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="b0126-144">Управление запросами на отпуск в Teams</span><span class="sxs-lookup"><span data-stu-id="b0126-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

