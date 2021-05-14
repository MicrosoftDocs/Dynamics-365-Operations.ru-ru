---
title: Сообщения обработчика сообщений
description: В этом разделе представлены сведения о функции сообщений обработчика сообщений для рабочих нагрузок единиц масштабирования.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b1428e2e657e653874d4ec07605932a32bd803b2
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938258"
---
# <a name="message-processor-messages"></a><span data-ttu-id="b0eb2-103">Сообщения обработчика сообщений</span><span class="sxs-lookup"><span data-stu-id="b0eb2-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b0eb2-104">Сообщения обработчика сообщений используются при выполнении облачных и пограничных единиц масштабирования для [производственных рабочих нагрузок](cloud-edge-workload-manufacturing.md) и [рабочих нагрузок управления складом](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="b0eb2-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="b0eb2-105">Для их синхронизации идет обмен большим объемом данных между концентратором и средами развертывания единиц масштабирования, но *обработчиком сообщений* будет обработано всего несколько таких обменов данными.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="b0eb2-106">Сообщения, обрабатываемые обработчиком сообщений, можно просмотреть, перейдя на **Администрирование системы > Обработчик сообщений > Сообщения обработчика сообщений**.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="b0eb2-107">Столбцы и фильтры сетки сообщений</span><span class="sxs-lookup"><span data-stu-id="b0eb2-107">Message grid columns and filters</span></span>

<span data-ttu-id="b0eb2-108">Можно использовать поля в верхней части страницы **Сообщения обработчика сообщений**, чтобы найти все конкретные сообщения, которые вы ищете.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="b0eb2-109">Большинство из этих фильтров соответствуют заголовкам столбцов в сетке сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="b0eb2-110">Доступны следующие фильтры и заголовки столбцов:</span><span class="sxs-lookup"><span data-stu-id="b0eb2-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="b0eb2-111">**Тип сообщения** — задает тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="b0eb2-112">**Очередь сообщений** — указывает имя очереди, в которой должно быть обработано сообщение.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="b0eb2-113">Имеются следующие очереди:</span><span class="sxs-lookup"><span data-stu-id="b0eb2-113">The following queues are provided:</span></span>
  - <span data-ttu-id="b0eb2-114">*От единицы масштабирования к узлу*</span><span class="sxs-lookup"><span data-stu-id="b0eb2-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="b0eb2-115">*От узла к единице масштабирования управления складом*</span><span class="sxs-lookup"><span data-stu-id="b0eb2-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="b0eb2-116">*От узла к единице масштабирования управления производством*</span><span class="sxs-lookup"><span data-stu-id="b0eb2-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="b0eb2-117">**Состояние сообщения** — определяет состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="b0eb2-118">Существуют следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="b0eb2-118">The following states exists:</span></span>
  - <span data-ttu-id="b0eb2-119">*В очереди* — сообщение готово для обработки обработчиком сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="b0eb2-120">*Обработано* — сообщение успешно обработано обработчиком сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="b0eb2-121">*Отменено* — сообщение было обработано, но возникла ошибка обработки.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="b0eb2-122">**Содержимое сообщения** — этот фильтр выполняет полнотекстовый поиск содержимого сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="b0eb2-123">(Содержимое сообщения не показывается в сетке.) Фильтр обрабатывает большинство специальных символов (например, "-") как пробелы и обрабатывает все пробелы как логические операторы ИЛИ.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="b0eb2-124">T=Например, это означает, что при поиске конкретного значения `journalid`, равного "USMF-123456", система найдет все сообщения, содержащие "USMF" или "123456", то есть, скорее всего, список будет длинным.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="b0eb2-125">Таким образом, лучше ввести только "123456", поскольку это приведет к получению более конкретных результатов.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="b0eb2-126">Пример типа сообщения: запрос финансового обновления корректировки запасов</span><span class="sxs-lookup"><span data-stu-id="b0eb2-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="b0eb2-127">Например, **Тип сообщения** *Запрос финансового обновления корректировки запасов* используется для создания и разноски журнала учета в концентраторе, когда работник использует приложение склада для [регистрации корректировки запасов](cloud-edge-warehouse-inventory-adjustment.md) в рабочей нагрузке управления складом единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="b0eb2-128">Поскольку данный конкретный процесс происходит из единицы масштабирования шкалы, в поле **Очередь сообщений** будет отображена *Единица масштабирования для концентратора*.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="b0eb2-129">Для этого типа сообщений рабочая нагрузка единицы масштабирования записывает сообщение как часть операции корректировки запасов в приложении склада.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="b0eb2-130">Затем данные сообщения передаются в концентратор в рамках того же процесса, который используется для [Архитектура Commerce Data Exchange](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="b0eb2-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="b0eb2-131">Сообщение будет обновлено и покажет **Состояние сообщения** как *В очереди*.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="b0eb2-132">Затем обработчик сообщений пытается обработать сообщение и обновляет **Состояние сообщения** на *Обработано* в случае успеха или *Отменено* при сбое.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="b0eb2-133">Просмотр журнала сообщений, содержимого сообщения и сведений</span><span class="sxs-lookup"><span data-stu-id="b0eb2-133">View the message log, message content, and details</span></span>

<span data-ttu-id="b0eb2-134">Подробные сведения о сообщении можно найти, выбрав его в сетке, а затем открыв вкладки **Журнал** или **Содержимое сообщения** в сетке сообщения, где отображается каждое событие обработки.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="b0eb2-135">**Содержимое сообщения** зависит от **Тип сообщения**, поэтому у него различная длина текста.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="b0eb2-136">Текст сообщения в обычном режиме начинается с **{** и заканчивается на **}**, и если между ними имеются имена полей такие, как `journalId`, а затем **:** и значение как *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="b0eb2-137">Панель инструментов на вкладке **Журнал** содержит следующие кнопки:</span><span class="sxs-lookup"><span data-stu-id="b0eb2-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="b0eb2-138">**Журнал** — отображаются результаты обработки.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="b0eb2-139">Это особенно полезно для понимания причин сбоя обработки сообщений, со значением для **Результат обработки** как *Сбой*.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="b0eb2-140">**Набор** — несколько операций обработки сообщений могут быть выполнены в рамках одного пакетного процесса.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="b0eb2-141">Нажмите эту кнопку, чтобы просмотреть подробные данные.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="b0eb2-142">Например, можно просмотреть, существуют ли зависимости, которые требуют от системы обработки определенных сообщений в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="b0eb2-143">Пакетное задание обработчика сообщений</span><span class="sxs-lookup"><span data-stu-id="b0eb2-143">Message processor batch job</span></span>

<span data-ttu-id="b0eb2-144">При выполнении облачного и граничного развертывания пакетное задание *Обработчик сообщений* будет автоматически вызван при создании нового сообщения для обработки, поэтому не нужно планировать это задание вручную.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="b0eb2-145">При необходимости можно получить доступ к пакетному заданию, перейдя **Администрирование системы > Обработчик сообщений > Обработчик сообщений**.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="b0eb2-146">Обработка или отмена сообщения вручную</span><span class="sxs-lookup"><span data-stu-id="b0eb2-146">Manually process or cancel a message</span></span>

<span data-ttu-id="b0eb2-147">При необходимости можно вручную обработать или отменить сообщение, в зависимости от его текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="b0eb2-148">Для этого выберите сообщение в сетке, а затем выберите **Обработать** или **Отмена** на панели операций</span><span class="sxs-lookup"><span data-stu-id="b0eb2-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="b0eb2-149">Настройка бизнес-событий для доставки оповещений по невыполненным результатам обработки</span><span class="sxs-lookup"><span data-stu-id="b0eb2-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="b0eb2-150">В дополнение к фильтрации по значению **Состояние сообщения** *Отменено* для запроса сообщений со сбоями можно настроить [Бизнес-события](../../fin-ops-core/dev-itpro/business-events/home-page.md) в концентраторе, чтобы предупредить о невыполненных результатах обработки.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="b0eb2-151">Для этого активируйте бизнес-событие с именем *Сообщение обработчика сообщений обработано* на странице **Каталог бизнес-событий** (**Администрирование системы > Настройка > Бизнес-события > Каталог бизнес-событий**).</span><span class="sxs-lookup"><span data-stu-id="b0eb2-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="b0eb2-152">В ходе процесса активации вам необходимо указать, относится ли это событие к одному или всем юридическим лицам, и предоставить **Имя конечной точки**, которое должно быть определено первым.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="b0eb2-153">Если **Когда бизнес-событие происходит** задано как *Microsoft Power Automate* (а не *HTTPS*, например), **Имя конечной точки** будет автоматически создано в Supply Chain Management на основе настройки *Microsoft Power Automate*.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="b0eb2-154">Пример Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="b0eb2-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="b0eb2-155">В этом примере при использовании **Когда бизнес-событие происходит** со значением *Microsoft Power Automate* отправляет сообщения электронной почты, содержащие сообщения Infolog и гиперссылки, чтобы открыть страницу **Сообщения обработчика сообщений** для конкретного сообщения со сбоем в развертывании концентратора.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="b0eb2-156">При необходимости можно добавить дополнительную логику для отправки уведомлений параллельно, используя различные каналы, и управлять получателями на основе данных события.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="b0eb2-157">В [Power Automate](https://preview.flow.microsoft.com) создайте новый автоматический облачный поток для триггера потока **Когда бизнес-событие происходит — FIN & Ops (Dynamics 365)**, за которым следуют шаги **Анализ JSON** и **Отправить сообщение электронной почты**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Автоматизированный облачный поток Power Automate":::

1. <span data-ttu-id="b0eb2-159">На шаге **Когда бизнес-событие происходит** можно найти или ввести **Экземпляр** концентратора, затем **Категория**, а затем **Бизнес-событие** *Сообщение обработчика сообщений обработано*, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Шаг Power Automate — Когда бизнес-событие происходит":::

1. <span data-ttu-id="b0eb2-161">Для шага **Анализ JSON** введите **Схема**, определяющую расширенные поля.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="b0eb2-162">Можно использовать параметр *Загрузка схемы* на странице **Каталог бизнес-событий** в Supply Chain Management или начать с вставки текста схемы примера.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="b0eb2-163">Этот пример текста приведен на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Шаг Power Automate — Анализ JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="b0eb2-165">В шаге **Отправить сообщение электронной почты** можно выбрать отдельные поля или начать, вставив пример текста сообщения электронной почты в поле **Текст**.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="b0eb2-166">Этот пример приведен на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Шаг Power Automate — Отправка сообщения электронной почты":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="b0eb2-168">При сохранении бизнес-события оно автоматически активируется и становится активным для использования в рамках Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
