---
title: События приложения склада
description: В этой теме описывается обработка событий приложения склада, используемая для обработки сообщений о событиях приложения склада в рамках пакетного задания.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988396"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="3a5f3-103">Обработка событий приложения склада</span><span class="sxs-lookup"><span data-stu-id="3a5f3-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a5f3-104">Пакетные задания, выполняемые в Supply Chain Management, могут использовать данные из очереди для обработки событий, выданных приложением склада, для необходимого реагирования на события из сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="3a5f3-105">Эта функция добавляет в очередь соответствующие события в ответ на определенные типы действий, выполняемых сотрудниками, использующими приложение.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="3a5f3-106">Пример, это когда при использовании функции **Создание и обработка заказов на перемещение из приложения склада**, заголовок и строки заказа на перемещение создаются и обновляются в серверной части, когда система запускает пакетное задание **Обработка событий приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="3a5f3-107">Включение функции обработки событий приложения склада</span><span class="sxs-lookup"><span data-stu-id="3a5f3-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="3a5f3-108">Прежде чем использовать эту функцию, необходимо включить ее в системе.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="3a5f3-109">Администраторы могут использовать страницу [управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения их при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="3a5f3-110">Функция обработки событий приложения склада перечислена как:</span><span class="sxs-lookup"><span data-stu-id="3a5f3-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="3a5f3-111">**Модуль** — Управление складом</span><span class="sxs-lookup"><span data-stu-id="3a5f3-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="3a5f3-112">**Имя функции** — обработка событий приложения склада</span><span class="sxs-lookup"><span data-stu-id="3a5f3-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="3a5f3-113">Настройка пакетного задания для обработки событий приложения склада</span><span class="sxs-lookup"><span data-stu-id="3a5f3-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="3a5f3-114">Обработка событий приложения склада</span><span class="sxs-lookup"><span data-stu-id="3a5f3-114">Process warehouse app events</span></span>

<span data-ttu-id="3a5f3-115">Настройка запланированного пакетного задания для обработки событий приложения склада для создания заказов на перемещение и обновлений строк.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="3a5f3-116">Перейдите **Управление складом \> Периодические задачи \> Обработка событий приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="3a5f3-117">Откроется диалоговое окно обработки событий приложения склада.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="3a5f3-118">Разверните экспресс-вкладку **Выполнять в фоновом режиме** и установите для параметра **Пакетная обработка** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="3a5f3-119">На экспресс-вкладке **Выполнять в фоновом режиме** выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="3a5f3-120">Откроется диалоговое окно **Определение повторения**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="3a5f3-121">Настройте расписание запуска в соответствии с потребностями компании.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="3a5f3-122">Выберите **ОК**, чтобы вернуться в диалоговое окно **Обработка событий приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="3a5f3-123">Выберите **ОК** в диалоговом окне **Обработка событий приложений склада**, чтобы добавить пакетное задание в очередь пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="3a5f3-124">Запрос событий приложения склада</span><span class="sxs-lookup"><span data-stu-id="3a5f3-124">Query warehouse app events</span></span>

<span data-ttu-id="3a5f3-125">Можно просмотреть очередь событий и сообщения о событиях, созданные приложением склада, перейдя в раздел **Управление складом \> Запросы и отчеты \> Журналы мобильных устройств \> События приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="3a5f3-126">Стандартный процесс очереди событий</span><span class="sxs-lookup"><span data-stu-id="3a5f3-126">The standard event queue process</span></span>

<span data-ttu-id="3a5f3-127">Очередь событий приложения склада обычно используется со следующим описанным потоком:</span><span class="sxs-lookup"><span data-stu-id="3a5f3-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="3a5f3-128">Событие добавляется в очередь с сообщением о событии.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="3a5f3-129">Новое сообщение первоначально имеет состояние события **Ожидание**, что означает, что пакетное задание **Обработка событий приложения склада** не будет отбирать и обрабатывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="3a5f3-130">Как только состояние сообщения изменится на **В очереди**, пакетное задание **Обработка событий приложения склада** будет выполнять выборку и обработку события.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="3a5f3-131">Пакетное задание обновляет состояния событий на **Завершено** или **Сбой** в зависимости от того, был ли возможен запрошенный процесс.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="3a5f3-132">После того как все соответствующие сообщений о событии будут в состояние **Завершено**, это событие удаляется из очереди.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="3a5f3-133">Подробный пример см. в разделе [Создание заказа на перемещение из процесса приложения склада](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="3a5f3-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="3a5f3-134">Обработка ошибок событий</span><span class="sxs-lookup"><span data-stu-id="3a5f3-134">Handle event errors</span></span>

<span data-ttu-id="3a5f3-135">В процессе обработки складских событий запрошенное действие сообщения могло не получать процессов из пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="3a5f3-136">В этом случае сообщение о событии изменится на **Сбой**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="3a5f3-137">Можно использовать сведения из **журнала пакетов**, чтобы узнать причину и предпринять необходимые действия по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="3a5f3-138">Подробный пример см. в разделе [Создание заказа на перемещение из приложения склада](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="3a5f3-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="3a5f3-139">Для сброса сбойного сообщения о событии приложения склада:</span><span class="sxs-lookup"><span data-stu-id="3a5f3-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="3a5f3-140">Перейдите в раздел **Управление складом \> Запросы и отчеты \> Журналы мобильного устройства \> События приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="3a5f3-141">На экспресс-вкладке **Сообщения о событиях приложения склада** найдите и выберите соответствующее событие, для которого отображается значение **Сбой** в столбце **Состояние события**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="3a5f3-142">Выберите **Сброс** на панели инструментов **Сообщения о событиях приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="3a5f3-143">Продолжайте работать, пока не будут сброшены все соответствующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="3a5f3-144">Кроме того, можно удалить сообщение о событии **Сбой**, используя команду **Удалить** на панели инструментов **Сообщения о событиях приложения склада**.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
