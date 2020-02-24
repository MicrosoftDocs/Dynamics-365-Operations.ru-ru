---
title: Обзор оповещений
description: В этой теме представлены общие сведения об оповещениях. Можно пользоваться оповещениями, чтобы знать о событиях, которые вы хотите отслеживать в течение рабочего дня.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 12fadd8387054db3e19d4136555724c23548e05c
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031027"
---
# <a name="alerts-overview"></a><span data-ttu-id="e064d-104">Обзор оповещений</span><span class="sxs-lookup"><span data-stu-id="e064d-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="e064d-105">Об оповещениях</span><span class="sxs-lookup"><span data-stu-id="e064d-105">About alerts</span></span>
<span data-ttu-id="e064d-106">Оповещения в системе уведомлений для критически важных событий в системе.</span><span class="sxs-lookup"><span data-stu-id="e064d-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="e064d-107">Можно пользоваться оповещениями, чтобы знать о событиях, которые вы хотите отслеживать в течение рабочего дня.</span><span class="sxs-lookup"><span data-stu-id="e064d-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="e064d-108">Можно легко создать свой набор правил оповещения, чтобы получать оповещения о просроченных поставках, удаленных заказах, изменении цен и других событиях, на которые требуется реагировать.</span><span class="sxs-lookup"><span data-stu-id="e064d-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="e064d-109">В системе планирования ресурсов предприятия (ERP) существует несколько типичных сценариев, где можно использовать функцию оповещений.</span><span class="sxs-lookup"><span data-stu-id="e064d-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="e064d-110">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="e064d-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="e064d-111">Сценари 1. Создание правила генерации оповещений для новых заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="e064d-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="e064d-112">Откройте страницу **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="e064d-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="e064d-113">В области действий на вкладке **Параметры** в группе **Поделиться** выберите **Создать пользовательское оповещение**.</span><span class="sxs-lookup"><span data-stu-id="e064d-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="e064d-114">В диалоговом окне **Создать правило генерации оповещений** на экспресс-вкладке **Оповещать меня, когда** в поле **Событие** выберите пункт **Запись создана**.</span><span class="sxs-lookup"><span data-stu-id="e064d-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="e064d-115">Сценарий 2. Создание правила генерации оповещений для отсрочки даты поставки</span><span class="sxs-lookup"><span data-stu-id="e064d-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="e064d-116">Откройте страницу **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="e064d-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="e064d-117">Выберите код заказа на покупку для доступа к сведениям о заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="e064d-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="e064d-118">Разверните экспресс-вкладку **Заголовок заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="e064d-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="e064d-119">В области действий на вкладке **Параметры** в группе **Поделиться** выберите **Создать пользовательское оповещение**.</span><span class="sxs-lookup"><span data-stu-id="e064d-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="e064d-120">В диалоговом окне **Создать правило генерации оповещений** на экспресс-вкладке **Оповещать меня, когда** в поле **Поле** выберите пункт **Дата поставки**.</span><span class="sxs-lookup"><span data-stu-id="e064d-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="e064d-121">В поле **Событие** выберите **отсрочено**.</span><span class="sxs-lookup"><span data-stu-id="e064d-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="e064d-122">После закрытия диалогового окна **Создать правило генерации оповещений** ваше правило отображается на странице **Управление правилами генерации оповещений**.</span><span class="sxs-lookup"><span data-stu-id="e064d-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="e064d-123">Можно использовать страницу **Управление правилами генерации оповещений** для обновления существующих правил генерации оповещений.</span><span class="sxs-lookup"><span data-stu-id="e064d-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="e064d-124">Например, можно изменить триггеры событий, обновить уведомления о событиях и обновить даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="e064d-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="e064d-125">Чтобы открыть страницу **Управление правилами генерации оповещений** используйте кнопку **Оповещать меня** на вкладке **Параметры** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="e064d-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="e064d-126">Что происходит при создании правила оповещений?</span><span class="sxs-lookup"><span data-stu-id="e064d-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="e064d-127">При создании правила оповещения, можно связать предварительно определенное событие с конкретным полем.</span><span class="sxs-lookup"><span data-stu-id="e064d-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="e064d-128">Например, наступает дата, указанная в поле, или содержимое поля изменяется.</span><span class="sxs-lookup"><span data-stu-id="e064d-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="e064d-129">Кроме того, можно связать событие с записями на определенной странице.</span><span class="sxs-lookup"><span data-stu-id="e064d-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="e064d-130">Например, при создании или удалении записи.</span><span class="sxs-lookup"><span data-stu-id="e064d-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="e064d-131">Когда происходит выбранное событие для этого поля, или для записи на странице, отправляется оповещение вам.</span><span class="sxs-lookup"><span data-stu-id="e064d-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="e064d-132">Например, вы создаете правило, в котором связываете поле **Дата поставки** в конкретной строке заказа на покупку с событием **был должен эту сумму уже в прошлом**.</span><span class="sxs-lookup"><span data-stu-id="e064d-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="e064d-133">Временная рамка задается как пять дней.</span><span class="sxs-lookup"><span data-stu-id="e064d-133">You set the time frame to five days.</span></span> <span data-ttu-id="e064d-134">В этом случае оповещение отправляется через 5 дней после даты поставки этой строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="e064d-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="e064d-135">Кроме того, можно усовершенствовать правила оповещений, задавая условия.</span><span class="sxs-lookup"><span data-stu-id="e064d-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="e064d-136">Например, то можно получать оповещения о новых заказах на покупку, созданных для конкретных счетов поставщика.</span><span class="sxs-lookup"><span data-stu-id="e064d-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="e064d-137">Подготовка для оповещения</span><span class="sxs-lookup"><span data-stu-id="e064d-137">Preparing for an alert</span></span>

<span data-ttu-id="e064d-138">Перед созданием правила оповещения необходимо определить когда или в каких ситуациях получать оповещение.</span><span class="sxs-lookup"><span data-stu-id="e064d-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="e064d-139">Если уже известно, о каких событиях необходимо оповещать, найдите страницу, на которой будут отображены данные, вызвавшие появление оповещения.</span><span class="sxs-lookup"><span data-stu-id="e064d-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="e064d-140">Событие может быть датой, которая наступила, или определенным изменением, которое произошло.</span><span class="sxs-lookup"><span data-stu-id="e064d-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="e064d-141">Поэтому необходимо найти страницу, где эта дата определяется, или на которой отображаются поле, которое изменилось, или созданная новая запись.</span><span class="sxs-lookup"><span data-stu-id="e064d-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="e064d-142">После получения этой информации можно создать правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="e064d-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="e064d-143">Компоненты правила оповещения</span><span class="sxs-lookup"><span data-stu-id="e064d-143">Components of an alert rule</span></span>

<span data-ttu-id="e064d-144">Правило оповещения имеет пять компонентов:</span><span class="sxs-lookup"><span data-stu-id="e064d-144">An alert rule has five components:</span></span>

- <span data-ttu-id="e064d-145">**Событие** — событие, запускающее правило оповещений, может быть датой, которая наступила или определенное изменение, которое произошло.</span><span class="sxs-lookup"><span data-stu-id="e064d-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="e064d-146">События определяются на экспресс-вкладке **Отправить оповещения по электронной почте для изменений статусов заданий** диалогового окна **Создать правило генерации оповещений**.</span><span class="sxs-lookup"><span data-stu-id="e064d-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="e064d-147">**Условие** — на экспресс-вкладке **Оповестить меня для** диалогового окна **Создать правило генерации оповещений** можно выбрать область условия, чтобы контролировать, когда вы получаете оповещения о событиях.</span><span class="sxs-lookup"><span data-stu-id="e064d-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="e064d-148">Можно применить правило к текущей записи только или ко всем записям, видимым на странице.</span><span class="sxs-lookup"><span data-stu-id="e064d-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="e064d-149">Если правило действует для всех юридических лиц, можно задать для параметра **Для всей организации** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e064d-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="e064d-150">**Срок действия правила** — на экспресс-вкладке **Оповестить меня до** диалогового окна **Создать правило генерации оповещений** можно указать, как долго должно действовать правило генерации оповещений.</span><span class="sxs-lookup"><span data-stu-id="e064d-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="e064d-151">**Содержание** — на экспресс-вкладке **Оповещать меня с** диалогового окна **Создать правило генерации оповещений** можно указать текст темы и текст сообщения, которые должны использоваться в сообщении оповещения.</span><span class="sxs-lookup"><span data-stu-id="e064d-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="e064d-152">**Пользователь** — на экспресс-вкладке **Оповестить кого** диалогового окна **Создать правило генерации оповещений** можно указать, какой пользователь должен получать сообщения оповещения.</span><span class="sxs-lookup"><span data-stu-id="e064d-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="e064d-153">По умолчанию, ваш идентификатор пользователя выбирается.</span><span class="sxs-lookup"><span data-stu-id="e064d-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e064d-154">Этот параметр ограничен администраторами организации.</span><span class="sxs-lookup"><span data-stu-id="e064d-154">This option is restricted to organization administrators.</span></span>

## <a name="email-notifications-from-alerts"></a><span data-ttu-id="e064d-155">Уведомления по электронной почте из оповещений</span><span class="sxs-lookup"><span data-stu-id="e064d-155">Email notifications from alerts</span></span>

<span data-ttu-id="e064d-156">Уведомления по электронной почте из оповещений еще не включены.</span><span class="sxs-lookup"><span data-stu-id="e064d-156">Email notifications from alerts are not yet enabled.</span></span> <span data-ttu-id="e064d-157">Это будет включено в будущем обновлении.</span><span class="sxs-lookup"><span data-stu-id="e064d-157">This will be enabled in a future update.</span></span>

## <a name="videos"></a><span data-ttu-id="e064d-158">Видео</span><span class="sxs-lookup"><span data-stu-id="e064d-158">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="e064d-159">Использование оповещений для отслеживания отфильтрованных данных</span><span class="sxs-lookup"><span data-stu-id="e064d-159">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="e064d-160">Видео [Использование оповещений для отслеживания отфильтрованных данных](https://youtu.be/ZYKMcv6kl9s) (показанное выше) включено в список воспроизведения [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), доступный на YouTube.</span><span class="sxs-lookup"><span data-stu-id="e064d-160">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="e064d-161">Параметры правила оповещения</span><span class="sxs-lookup"><span data-stu-id="e064d-161">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="e064d-162">Видео [Параметры правил оповещения](https://youtu.be/cpzimwOjicM) (показано выше) включено в список воспроизведения [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), доступный на сайте YouTube.</span><span class="sxs-lookup"><span data-stu-id="e064d-162">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


