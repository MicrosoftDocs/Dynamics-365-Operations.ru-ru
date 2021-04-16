---
title: Уведомления о выполнении волны
description: В этой теме описываются уведомления о выполнении волны и объясняется, как их настроить.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838090"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="55a47-103">Уведомления о выполнении волны</span><span class="sxs-lookup"><span data-stu-id="55a47-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="55a47-104">Функция *Уведомления о выполнении волны* использует бизнес-события и центр уведомлений для доставки уведомлений, которые относятся к выполнению волн.</span><span class="sxs-lookup"><span data-stu-id="55a47-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="55a47-105">Она позволяет указать типы событий, создающих уведомления, склады, которые их создают, и пользователей, которые их получают.</span><span class="sxs-lookup"><span data-stu-id="55a47-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="55a47-106">Кнопка **Показать сообщения** (символ колокольчика) в правой части панели переходов показывает, что сообщение центра уведомлений доступно текущему пользователю.</span><span class="sxs-lookup"><span data-stu-id="55a47-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="55a47-107">Пользователь может выбрать кнопку **Показать сообщения**, чтобы открыть центр уведомлений и просмотреть сообщения.</span><span class="sxs-lookup"><span data-stu-id="55a47-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="55a47-108">Бизнес-события возникают при выполнении бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="55a47-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="55a47-109">Бизнес-процессы состоят из задач.</span><span class="sxs-lookup"><span data-stu-id="55a47-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="55a47-110">Во время бизнес-процесса пользователи, участвующие в нем, выполняют бизнес-действия для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="55a47-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="55a47-111">Бизнес-события обеспечивают механизм, который позволяет внешним системам получать уведомления от приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="55a47-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="55a47-112">Таким образом, системы могут выполнять бизнес-действия в ответ на бизнес-события.</span><span class="sxs-lookup"><span data-stu-id="55a47-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="55a47-113">Дополнительные сведения см. в разделе [Обзор бизнес-событий](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="55a47-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="55a47-114">Включение функции уведомлений о выполнении волны</span><span class="sxs-lookup"><span data-stu-id="55a47-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="55a47-115">Прежде чем использовать функцию *Уведомления о выполнении волны*, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="55a47-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="55a47-116">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="55a47-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="55a47-117">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55a47-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="55a47-118">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="55a47-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="55a47-119">**Имя функции:** *Уведомления о выполнении волны*</span><span class="sxs-lookup"><span data-stu-id="55a47-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="55a47-120">Сценарий: отправка уведомлений о пакетном выполнении волн в центр уведомлений</span><span class="sxs-lookup"><span data-stu-id="55a47-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="55a47-121">Этот сценарий показывает сквозной поток для отправки уведомлений об ошибках пакетного выполнения волны определенной роли через центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="55a47-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="55a47-122">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="55a47-122">Make demo data available</span></span>

<span data-ttu-id="55a47-123">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="55a47-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="55a47-124">Убедитесь, что волны выполняются в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="55a47-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="55a47-125">Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="55a47-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="55a47-126">На экспресс-вкладке **Обработка волн** установите для параметра **Обрабатывать волны в партии** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="55a47-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="55a47-127">Если вы хотите отключить уведомления о пакетном выполнении волн, установите для параметра **Отключить пакетные уведомления об обработке волн** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="55a47-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="55a47-128">Настройка политики уведомлений о волнах</span><span class="sxs-lookup"><span data-stu-id="55a47-128">Configure a wave notification policy</span></span>

<span data-ttu-id="55a47-129">Политики уведомления о волнах определяют типы отправляемых уведомлений и пользователей, которые получают уведомление.</span><span class="sxs-lookup"><span data-stu-id="55a47-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="55a47-130">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Политики уведомления о волнах**.</span><span class="sxs-lookup"><span data-stu-id="55a47-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="55a47-131">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="55a47-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="55a47-132">**Политика уведомления о волнах:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="55a47-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="55a47-133">**Описание:** *Ошибка пакетной обработки волны для склада 24*</span><span class="sxs-lookup"><span data-stu-id="55a47-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="55a47-134">**Отправлять уведомление:** *Только ошибка*</span><span class="sxs-lookup"><span data-stu-id="55a47-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="55a47-135">**Для роли:** *Системный администратор*</span><span class="sxs-lookup"><span data-stu-id="55a47-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="55a47-136">Поскольку в этом сценарии используются демонстрационные данные, роль *Системный администратор* выбрана для простоты.</span><span class="sxs-lookup"><span data-stu-id="55a47-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="55a47-137">Таким образом, поскольку вы вошли в систему как системный администратор, вы будете получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="55a47-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="55a47-138">Однако на практике обычно следует выбрать более конкретную роль для уведомления об ошибках пакетного выполнения волн, такую как *Менеджер склада*.</span><span class="sxs-lookup"><span data-stu-id="55a47-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="55a47-139">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="55a47-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="55a47-140">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="55a47-140">Configure a wave template</span></span>

<span data-ttu-id="55a47-141">Шаблоны волн позволяют связывать отдельные экземпляры методов волны с соответствующими шаблонами этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="55a47-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="55a47-142">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="55a47-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="55a47-143">В области списка задайте для поля **Тип шаблона волны** значение *Отгрузка*, затем выберите шаблон волны *24 Отгрузка по умолчанию* для склада 24.</span><span class="sxs-lookup"><span data-stu-id="55a47-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="55a47-144">На экспресс-вкладке **Общие** задайте в поле **Политика уведомлений и волне** значение *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="55a47-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="55a47-145">Настройка шаблона работы</span><span class="sxs-lookup"><span data-stu-id="55a47-145">Configure a work template</span></span>

<span data-ttu-id="55a47-146">Шаблоны работы используются во время выполнения волны для создания работы.</span><span class="sxs-lookup"><span data-stu-id="55a47-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="55a47-147">Для этого сценария выполнение волны должно вызывать ошибку.</span><span class="sxs-lookup"><span data-stu-id="55a47-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="55a47-148">Задав для запроса шаблона работы использование несуществующего склада, можно гарантировать, что выполнение волны завершиться сбоем и, таким образом, будет отправлено уведомление.</span><span class="sxs-lookup"><span data-stu-id="55a47-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="55a47-149">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="55a47-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="55a47-150">В области списка задайте для поля **Тип шаблона работы** значение *Заказы на продажу*, затем выберите шаблон работы *24 Этап заказа на продажу* для склада 24.</span><span class="sxs-lookup"><span data-stu-id="55a47-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="55a47-151">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="55a47-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="55a47-152">В диалоговом окне редактора запросов на вкладке **Диапазон** измените следующую строку (или добавьте ее, если она не существует):</span><span class="sxs-lookup"><span data-stu-id="55a47-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="55a47-153">**Таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="55a47-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="55a47-154">**Производная таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="55a47-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="55a47-155">**Поле:** *Склад*</span><span class="sxs-lookup"><span data-stu-id="55a47-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="55a47-156">**Критерии:** измените значение с *24* на *Ошибка*.</span><span class="sxs-lookup"><span data-stu-id="55a47-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="55a47-157">Выберите **ОК** и подтвердите изменение.</span><span class="sxs-lookup"><span data-stu-id="55a47-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="55a47-158">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="55a47-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="55a47-159">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="55a47-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="55a47-160">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="55a47-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="55a47-161">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="55a47-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="55a47-162">**Склад:** *24*</span><span class="sxs-lookup"><span data-stu-id="55a47-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="55a47-163">На экспресс-вкладке **Строки заказа на продажу** добавьте строку заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="55a47-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="55a47-164">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="55a47-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="55a47-165">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="55a47-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="55a47-166">Эти номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="55a47-166">These items and quantities are only examples.</span></span> <span data-ttu-id="55a47-167">На указанном складе должно быть достаточно запасов.</span><span class="sxs-lookup"><span data-stu-id="55a47-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="55a47-168">Пока новая строка все еще выбрана на экспресс-вкладке **Строки заказа на продажу**, выберите **Запасы \> Резервирование** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="55a47-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="55a47-169">На странице **Резервирование** в области действий выберите **Зарезервировать лот**.</span><span class="sxs-lookup"><span data-stu-id="55a47-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="55a47-170">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="55a47-170">Then close the page.</span></span>
1. <span data-ttu-id="55a47-171">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="55a47-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="55a47-172">Уведомления из выполнения пакетного задания волны</span><span class="sxs-lookup"><span data-stu-id="55a47-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="55a47-173">В зависимости от настройки бизнес-событий в конечном итоге вы получите уведомление о сбое выполнения волны.</span><span class="sxs-lookup"><span data-stu-id="55a47-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="55a47-174">Сообщение центра уведомлений будет выглядеть примерно так, как показано в следующем примере, и будет содержать ссылку на волну со сбоем.</span><span class="sxs-lookup"><span data-stu-id="55a47-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="55a47-175">**Ошибка при выполнении волны**</span><span class="sxs-lookup"><span data-stu-id="55a47-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="55a47-176">Произошла ошибка при выполнении волны USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="55a47-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="55a47-177">Последние сообщения: никакая работа для волны USMF-000000001 не была создана.</span><span class="sxs-lookup"><span data-stu-id="55a47-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="55a47-178">**СТАТУС**</span><span class="sxs-lookup"><span data-stu-id="55a47-178">**STATUS**</span></span>  
> <span data-ttu-id="55a47-179">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="55a47-179">Active</span></span>
>
> <span data-ttu-id="55a47-180">Открыть сведения о волне</span><span class="sxs-lookup"><span data-stu-id="55a47-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
