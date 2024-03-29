---
title: Консолидируйте отгрузки, выпущенные на склад, используя автоматический выпуск заказов на продажу
description: В этой статье представлен сценарий, в котором несколько заказов запущены на склад в одной периодической автоматической выпуске на склад.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ba8e9790a5b7eb00b20fba19f452118e1f05fed0
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428263"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Консолидируйте отгрузки, выпущенные на склад, используя автоматический выпуск заказов на продажу

[!include [banner](../includes/banner.md)]

В этой статье представлен сценарий, в котором несколько заказов запущены на склад в одной периодической автоматической выпуске на склад. Заказы будут автоматически консолидированы в отгрузки на основе правил, определенных как политики консолидации отгрузок.

В ходе сценария будут созданы наборы заказов на продажу, и каждый из них будет выпущен на склад. Затем будут просмотрены отгрузки, созданные или обновленные в ходе консолидации отгрузок на основе настроенных политик.

## <a name="make-demo-data-available"></a>Сделать демонстрационные данные доступными

Сценарий в этой статье ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management. Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Настройка политик консолидации отгрузок и фильтров продуктов

Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь. Обязательно выполните эти упражнения перед выполнением этого сценария.

## <a name="create-the-sales-orders-for-this-scenario"></a>Создание заказов на продажу для этого сценария

Начнем с создания набора заказов на продажу, с которыми можно работать. Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS). За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.

Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.

### <a name="create-order-set-1"></a>Создать набор заказов 1

#### <a name="sales-order-1-1"></a>Заказ на продажу 1-1

1. Создайте заказ на продажу со следующими параметрами:

    - **Счет клиента:** *US-001*
    - **Способ поставки:** *Airwa-Air*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

#### <a name="sales-order-1-2"></a>Заказ на продажу 1-2

1. Создайте заказ на продажу со следующими параметрами:

    - **Счет клиента:** *US-001*
    - **Способ поставки:** *Airwa-Air*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

#### <a name="sales-order-1-3"></a>Заказ на продажу 1-3

1. Создайте заказ на продажу со следующими параметрами:

    - **Счет клиента:** *US-001*
    - **Способ поставки:** *10*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

1. Добавьте вторую строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0002* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*
    - **Способ поставки:** *Airwa-Air*

### <a name="create-order-set-2"></a>Создать набор заказов 2

#### <a name="sales-orders-2-1-and-2-2"></a>Заказы на продажу 2-1 и 2-2

1. Создайте два одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-002*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)
    - **Количество:** *1.00*

1. Добавьте вторую строку заказа со следующими параметрами:

    - **Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)
    - **Количество:** *1.00*
    - **Способ поставки:** *Airwa-Air*

### <a name="create-order-set-3"></a>Создать набор заказов 3

#### <a name="sales-order-3-1"></a>Заказ на продажу 3-1

1. Создайте заказ на продажу со следующими параметрами:

    - **Счет клиента:** *US-002*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)
    - **Количество:** *1.00*

1. Добавьте вторую строку заказа со следующими параметрами:

    - **Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)
    - **Количество:** *1.00*
    - **Способ поставки:** *Airwa-Air*

> [!NOTE]
> Этот заказ идентичен двум заказам, созданным для набора заказов 2. Однако он указан как свой собственный порядок, так как он будет выводиться отдельно позже в этом сценарии.

### <a name="create-order-set-4"></a>Создать набор заказов 4

#### <a name="sales-order-4-1"></a>Заказ на продажу 4-1

1. Создайте заказ на продажу со следующими параметрами:

    - **Счет клиента:** *US-001*
    - **Заявка клиента:** *1*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

### <a name="create-order-set-5"></a>Создать набор заказов 5

#### <a name="sales-orders-5-1-and-5-2"></a>Заказы на продажу 5-1 и 5-2

1. Создайте два одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-001*
    - **Заявка клиента:** *2*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

#### <a name="sales-order-5-3"></a>Заказ на продажу 5-3

1. Создайте заказ на продажу со следующими параметрами:

    - **Счет клиента:** *US-001*
    - **Заявка клиента:** *1*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

### <a name="create-order-set-6"></a>Создать набор заказов 6

#### <a name="sales-orders-6-1-and-6-2"></a>Заказы на продажу 6-1 и 6-2

1. Создайте два одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-003*
    - **Заявка клиента:** *2*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Заказы на продажу 6-3 и 6-4

1. Создайте два одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-004*
    - **Заявка клиента:** *1*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Заказы на продажу 6-5 и 6-6

1. Создайте два одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-007*
    - **Сайт:** *6*
    - **Склад:** *61*
    - **Кластер:** *ShipCons*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Заказы на продажу 6-7 и 6-8

1. Создайте два одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-007*
    - **Сайт:** *6*
    - **Склад:** *61*
    - **Кластер:** Оставьте это поле пустым.

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Автоматический выпуск заказов на продажу на склад

Для каждого набора заказов на продажу, созданного ранее, необходимо выполнить процедуру автоматического запуска на склад. В каждом случае будет выполняться [базовая процедура запуска на склад](#release-procedure), предоставляемая здесь.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Обычная процедура запуска на склад

Для каждого набора заказов на продажу, созданного ранее, необходимо выполнить три процедуры, описанные в следующих подразделах.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Обновление шаблона волн, который будет использоваться в процессе запуска

1. Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.
1. Задайте в поле **Тип шаблона волн** значение *отгрузка*.
1. Найдите и выберите шаблон волн, связанный со складом, который использовался в наборах заказов, созданных для данного сценария. Например, если был использован склад *24*, выберите шаблон волн **24 Отгрузка по умолчанию**. Если был использован склад *61*, выберите шаблон волн **61 Отгрузка**.
1. На панели операций выберите **Правка**.
1. Установите для параметра **Обрабатывать волну перед запуском на склад** значение *Нет*.

#### <a name="release-to-the-warehouse"></a>Запуск на склад

1. Перейдите на **Управление складом \> Запуск на склад \> Автоматический выпуск заказов на продажу**.
1. В поле **количество к запуску** выберите *все*.
1. На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно запроса.
1. На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку со следующими настройками в сетку:

    - **Таблица:** *Заказ на продажу*
    - **Производная таблица:** *Заказ на продажу*
    - **Поля** — *заказ на продажу*
    - **Критерий:** Введите список номеров заказов на продажу через запятую из нужного набора заказов.

1. Нажмите кнопку **ОК** , чтобы сохранить запрос.
1. Нажмите кнопку **ОК** , чтобы запустить процедуру *Автоматический запуск в на склад*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Просмотр созданного или обновленного отгрузки

1. Выберите **Управление складом \> Отгрузки \> Все отгрузки**.
1. Найдите и выберите нужную отгрузку.
1. Если при создании или обновлении отгрузки была использована политика консолидации, ее можно увидеть в поле **Политика консолидации отгрузок**.

### <a name="release-sales-orders-from-order-set-1"></a>Запуск заказов на продажу из набора заказов 1

Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 1.

После завершения следует увидеть, что были созданы две отгрузки:

- Первая отгрузка содержит три строки и была создана с помощью политики консолидации отгрузок *CustomerMode*.
- Вторая отгрузка, которая не использует режим транспортировки *Airways* поставки, была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.

### <a name="release-sales-orders-from-order-set-2"></a>Запуск заказов на продажу из набора заказов 2

Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 2.

После завершения следует увидеть, что были созданы три отгрузки:

- Первая отгрузка содержит номенклатуры *Воспламеняющиеся*.
- Каждая из двух других отгрузок содержит одну строку, которая имеет номенклатуру *Взрывоопасные*.

### <a name="release-sales-orders-from-order-set-3"></a>Запуск заказов на продажу из набора заказов 3

Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 3.

После завершения вы увидите, что выполнены следующие действия:

- Была обновлена одна отгрузка (отгрузка, созданная, когда заказ на набор 2 был запущен на склад). Была добавлена строка с номенклатурой *Воспламеняющиеся*.
- Была создана одна новая отгрузка, содержащая номенклатуру *Взрывоопасные*.

### <a name="release-sales-orders-from-order-set-4"></a>Запуск заказов на продажу из набора заказов 4

Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 4.

После завершения следует увидеть, что одна существующая отгрузка (в поле **Заявка клиента** установлена на *1*) обновлена. К ней была добавлена одна новая строка.

### <a name="release-sales-orders-from-order-set-5"></a>Запуск заказов на продажу из набора заказов 5

Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 5.

После завершения вы увидите, что выполнены следующие действия:

- Обновлена одна существующая отгрузка (где в поле **заявки клиента** установлено значение *1*). В нее было добавлено строка из заказа на продажу 5-3 (где поле **Заявка клиента** установлено на *1*).
- Была создана одна новая отгрузка, в которой строки из заказов на продажу 5-1 и 5-2 группируются в одну отгрузку.

### <a name="release-sales-orders-from-order-set-6"></a>Запуск заказов на продажу из набора заказов 6

Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 6.

После завершения следует увидеть, что были созданы четыре отгрузки:

- Строки из двух заказов для клиента *US-003* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.
- Строки из двух заказов для клиента *US-004* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.
- Строки из заказов на продажу 6-5 и 6-6 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.
- Строки из заказов на продажу 6-7 и 6-8 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *CrossOrder*.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор политик консолидации отгрузок](about-shipment-consolidation-policies.md)
- [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]