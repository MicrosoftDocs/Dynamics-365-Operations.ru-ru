---
title: Сообщения обработчика сообщений
description: В этом разделе представлены сведения о функции сообщений обработчика сообщений для рабочих нагрузок единиц масштабирования.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 685c8951b7c0d8524091cf06306388736d894f58
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471652"
---
# <a name="message-processor-messages"></a>Сообщения обработчика сообщений

[!include [banner](../includes/banner.md)]

Сообщения обработчика сообщений используются при выполнении облачных и пограничных единиц масштабирования для [производственных рабочих нагрузок](cloud-edge-workload-manufacturing.md) и [рабочих нагрузок управления складом](cloud-edge-workload-warehousing.md).

Для их синхронизации идет обмен большим объемом данных между концентратором и средами развертывания единиц масштабирования, но *обработчиком сообщений* будет обработано всего несколько таких обменов данными. Сообщения, обрабатываемые обработчиком сообщений, можно просмотреть, перейдя на **Администрирование системы > Обработчик сообщений > Сообщения обработчика сообщений**.

## <a name="message-grid-columns-and-filters"></a>Столбцы и фильтры сетки сообщений

Можно использовать поля в верхней части страницы **Сообщения обработчика сообщений**, чтобы найти все конкретные сообщения, которые вы ищете. Большинство из этих фильтров соответствуют заголовкам столбцов в сетке сообщений. Доступны следующие фильтры и заголовки столбцов:

- **Тип сообщения** — задает тип сообщения.
- **Очередь сообщений** — указывает имя очереди, в которой должно быть обработано сообщение. Имеются следующие очереди:
  - *От единицы масштабирования к узлу*
  - *От узла к единице масштабирования управления складом*
  - *От узла к единице масштабирования управления производством*
- **Состояние сообщения** — определяет состояние сообщения. Существуют следующие состояния:
  - *В очереди* — сообщение готово для обработки обработчиком сообщений.
  - *Обработано* — сообщение успешно обработано обработчиком сообщений.
  - *Отменено* — сообщение было обработано, но возникла ошибка обработки.
- **Содержимое сообщения** — этот фильтр выполняет полнотекстовый поиск содержимого сообщения. (Содержимое сообщения не показывается в сетке.) Фильтр обрабатывает большинство специальных символов (например, "-") как пробелы и обрабатывает все пробелы как логические операторы ИЛИ. Например, это означает, что при поиске конкретного значения `journalid`, равного "USMF-123456", система найдет все сообщения, содержащие "USMF" или "123456", то есть, скорее всего, список будет длинным. Таким образом, лучше ввести только "123456", поскольку это приведет к получению более конкретных результатов.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Пример типа сообщения: запрос финансового обновления корректировки запасов

Например, **Тип сообщения** *Запрос финансового обновления корректировки запасов* используется для создания и разноски журнала учета в концентраторе, когда работник использует приложение склада для [регистрации корректировки запасов](cloud-edge-warehouse-inventory-adjustment.md) в рабочей нагрузке управления складом единицы масштабирования. Поскольку данный конкретный процесс происходит из единицы масштабирования шкалы, в поле **Очередь сообщений** будет отображена *Единица масштабирования для концентратора*.

Для этого типа сообщений рабочая нагрузка единицы масштабирования записывает сообщение как часть операции корректировки запасов в приложении склада. Затем данные сообщения передаются в концентратор в рамках того же процесса, который используется для [Архитектура Commerce Data Exchange](../../commerce/commerce-architecture.md). Сообщение будет обновлено и покажет **Состояние сообщения** как *В очереди*. Затем обработчик сообщений пытается обработать сообщение и обновляет **Состояние сообщения** на *Обработано* в случае успеха или *Отменено* при сбое.

## <a name="view-the-message-log-message-content-and-details"></a>Просмотр журнала сообщений, содержимого сообщения и сведений

Подробные сведения о сообщении можно найти, выбрав его в сетке, а затем открыв вкладки **Журнал** или **Содержимое сообщения** в сетке сообщения, где отображается каждое событие обработки.

**Содержимое сообщения** зависит от **Тип сообщения**, поэтому у него различная длина текста. Текст сообщения в обычном режиме начинается с **{** и заканчивается на **}**, и если между ними имеются имена полей такие, как `journalId`, а затем **:** и значение как *USMF-123456*.

Панель инструментов на вкладке **Журнал** содержит следующие кнопки:

- **Журнал** — отображаются результаты обработки. Это особенно полезно для понимания причин сбоя обработки сообщений, со значением для **Результат обработки** как *Сбой*.
- **Набор** — несколько операций обработки сообщений могут быть выполнены в рамках одного пакетного процесса. Нажмите эту кнопку, чтобы просмотреть подробные данные. Например, можно просмотреть, существуют ли зависимости, которые требуют от системы обработки определенных сообщений в определенной последовательности.

## <a name="message-processor-batch-job"></a>Пакетное задание обработчика сообщений

При выполнении распределенной гибридной топологии с масштабируемыми единицами пакетное задание *Обработчик сообщений* будет автоматически вызван при создании нового сообщения для обработки, поэтому не нужно планировать это задание вручную.

При необходимости можно получить доступ к пакетному заданию, перейдя **Администрирование системы > Обработчик сообщений > Обработчик сообщений**.

## <a name="manually-process-or-cancel-a-message"></a>Обработка или отмена сообщения вручную

При необходимости можно вручную обработать или отменить сообщение, в зависимости от его текущего состояния. Для этого выберите сообщение в сетке, а затем выберите **Обработать** или **Отмена** на панели операций

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Настройка бизнес-событий для доставки оповещений по невыполненным результатам обработки

В дополнение к фильтрации по значению **Состояние сообщения** *Отменено* для запроса сообщений со сбоями можно настроить [Бизнес-события](../../fin-ops-core/dev-itpro/business-events/home-page.md) в концентраторе, чтобы предупредить о невыполненных результатах обработки. Для этого активируйте бизнес-событие с именем *Сообщение обработчика сообщений обработано* на странице **Каталог бизнес-событий** (**Администрирование системы > Настройка > Бизнес-события > Каталог бизнес-событий**).

В ходе процесса активации вам необходимо указать, относится ли это событие к одному или всем юридическим лицам, и предоставить **Имя конечной точки**, которое должно быть определено первым.

>[!NOTE]
> Если **Когда бизнес-событие происходит** задано как *Microsoft Power Automate* (а не *HTTPS*, например), **Имя конечной точки** будет автоматически создано в Supply Chain Management на основе настройки *Microsoft Power Automate*.

### <a name="microsoft-power-automate-example"></a>Пример Microsoft Power Automate

В этом примере при использовании **Когда бизнес-событие происходит** со значением *Microsoft Power Automate* отправляет сообщения электронной почты, содержащие сообщения Infolog и гиперссылки, чтобы открыть страницу **Сообщения обработчика сообщений** для конкретного сообщения со сбоем в развертывании концентратора. При необходимости можно добавить дополнительную логику для отправки уведомлений параллельно, используя различные каналы, и управлять получателями на основе данных события.

1. В [Power Automate](https://preview.flow.microsoft.com) создайте новый автоматический облачный поток для триггера потока **Когда бизнес-событие происходит — FIN & Ops (Dynamics 365)**, за которым следуют шаги **Анализ JSON** и **Отправить сообщение электронной почты**, как показано на следующем рисунке.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Автоматизированный облачный поток Power Automate.":::

1. На шаге **Когда бизнес-событие происходит** можно найти или ввести **Экземпляр** концентратора, затем **Категория**, а затем **Бизнес-событие** *Сообщение обработчика сообщений обработано*, как показано на следующем рисунке.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Шаг Power Automate — Когда бизнес-событие происходит.":::

1. Для шага **Анализ JSON** введите **Схема**, определяющую расширенные поля. Можно использовать параметр *Загрузка схемы* на странице **Каталог бизнес-событий** в Supply Chain Management или начать с вставки текста схемы примера. Этот пример текста приведен на следующем рисунке.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Шаг Power Automate — Анализ JSON.":::

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

1. В шаге **Отправить сообщение электронной почты** можно выбрать отдельные поля или начать, вставив пример текста сообщения электронной почты в поле **Текст**. Этот пример приведен на следующем рисунке.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Шаг Power Automate — Отправка сообщения электронной почты.":::

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

1. При сохранении бизнес-события оно автоматически активируется и становится активным для использования в рамках Supply Chain Management.
