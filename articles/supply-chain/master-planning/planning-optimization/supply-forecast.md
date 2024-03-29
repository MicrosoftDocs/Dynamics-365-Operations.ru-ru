---
title: Сводное планирование с прогнозами поставок
description: В этой статье описывается, как учитываются прогнозы поставок при сводном планировании.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2bac9355bb1ac00f697ec459f494a64553e0eacc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740150"
---
# <a name="master-planning-with-supply-forecasts"></a>Сводное планирование с прогнозами поставок

[!include [banner](../../includes/banner.md)]

Прогнозы поставок позволяют указать поставки, который, как ожидается, потребуются в течение некоторого будущего периода. Обычно оценка будет основана на истории продаж предыдущего года, а затем используется прогноз для целей бюджетирования. Можно также настроить сводный план для рассмотрения прогнозов во время планирования.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Настройка сводного плана для учета прогнозов поставок

Можно указать, следует ли каждому сводному плану учитывать прогнозы во время выполнения. Чтобы настроить параметры прогнозирования для каждого плана, необходимо выполнить следующие действия

1. Выберите **Сводное планирование \> Настройка \> Планы \> Сводные планы**.
1. Выберите существующий сводный план в области списка или выберите **Создать** в области действий, чтобы создать новый.
1. На экспресс-вкладке **Общие** настройте следующие поля:

    - **Прогнозная модель** — выберите модель, которая содержит прогнозы поставок и/или спроса, которые должны учитываться сводным планом.
    - **Включить прогноз поставки** — установите для этого параметра значение *Да*, если сводный план должен учитывать прогнозы поставок.
    - **Включить прогноз спроса** — установите для этого параметра значение *Да*, если сводный план должен учитывать прогнозы спроса. Хотя этот параметр не зависит от параметра **Включить прогноз поставок**, некоторые другие параметры на странице применяются как к прогнозам поставок, так и к прогнозам спроса. Дополнительные сведения о планировании, которое учитывает прогнозы спроса, см. в разделе [Сводное планирование с прогнозами спроса](demand-forecast.md).
    - **Метод, используемый для сокращения потребностей по прогнозу** — выберите метод, который должен использоваться для снижения требований прогноза во время сводного планирования.

        - *Нет* — требования прогноза не будут уменьшаться при сводном планировании.
        - *Процент — ключ сокращения* — требования прогноза будут снижаться в соответствии с процентами и периодами времени, определенными в ключе сокращения.
        - *Проводки — ключ сокращения* — требования прогноза будут снижены по проводкам, которые имеют место во время временных периодов, определенных в ключе сокращения.
        - *Проводки - динамический период* — требования прогноза будут уменьшены на проводки заказов, которые возникают в динамический период. Динамический период охватывает даты текущего прогноза и заканчивается, когда начинается следующий прогноз. Метод *Проводки – динамический период* не использует или не требует ключа сокращения, и при использовании этого метода действуют следующие условия:

            - Если прогноз полностью уменьшен, требования прогноза для текущего прогноза будут равно 0 (нулю).
            - Если будущие прогнозы отсутствуют, сокращаются прогнозируемые требования из последнего введенного прогноза.
            - Временные границы включаются в расчеты уменьшения прогноза.
            - Положительные дни включаются в расчеты уменьшения прогноза.
            - Если фактические проводки по заказам превышают прогнозированные требования, то остальные проводки не передаются в следующий период прогноза.

        > [!NOTE]
        > Параметр **Метод, используемый для сокращения потребностей по прогнозу** также применяется к прогнозам спроса, если они включены для сводного плана, и повлияет на них аналогичным образом. Для получения дополнительных сведений см. [Сводное планирование с прогнозами спроса](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Задание параметров сокращения для групп покрытия

Чтобы настроить параметры, управляющие тем, как группа покрытия снизит ее требования прогноза для сводных планов, использующих снижение на основе транзакций, выполните следующие действия.

1. Выберите **Сводное планирование \> Настройка \> Планы \> Группы покрытия**.
1. Выберите существующую группу покрытия в области списка или выберите **Создать** на панели операций, чтобы создать новую.
1. На экспресс-вкладке **Прочее** в поле **Уменьшить прогноз по** укажите, как потребности по прогнозу должны сокращаться для номенклатур в группе покрытия для сводных планов, в которых в поле **Метод, используемый для сокращения потребностей по прогнозу** задано значение *Проводки — ключ сокращения* или *Проводки — динамический период*. Выберите одно из следующих значений:

    - *Все проводки* — все проводки должны уменьшать прогноз.
    - *Заказы* — только заказы одного типа должны сокращать прогноз.

    Например, настройки заказа по умолчанию для номенклатуры указывают, что она должна быть произведена. Имеется строка прогноза поставок для количества 50, и уже имеется заказ на покупку на количество 20. Если в поле **Уменьшить прогноз по** указано значение *Заказы*, для количества 50 будет создан спланированный производственный заказ. Если в нем установлено значение *Все проводки*, запланированный производственный заказ будет уменьшен до количества, равного 30.

    Эта настройка также применяется для уменьшения прогнозирования спроса. Для получения дополнительных сведений см. [Сводное планирование с прогнозами спроса](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Ввод прогноза поставок для продукта

Чтобы ввести прогноз поставок для продукта, выполните следующие действия.

1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.
1. Выберите продукт, для которого необходимо ввести прогноз.
1. В области действий на вкладке **План** выберите **Прогноз поставки**.
1. На странице **Прогноз поставки** в области действий выберите **Создать**, чтобы добавить прогноз в сетку.
1. Введите сведения о новой строке, необходимые для указания прогноза.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>План для номенклатуры со строками прогноза поставки

При выполнении сводного плана, который включает номенклатуру, для которой существует прогноз поставок, система создает заказ на покупку для введенных строк поставки. Учитываются настройки заказа по умолчанию для данной номенклатуры. Если эти настройки заказа по умолчанию определяют значение **Тип заказа по умолчанию** для *Заказа на покупку*, а счет поставщика не указан в строке прогноза поставок, система будет использовать поставщика по умолчанию для данной номенклатуры.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Проверка, является ли спланированный заказ заказом прогноза поставки

Используйте следующую процедуру, чтобы узнать, был ли создан спланированный заказ в результате прогноза поставок.

1. Перейдите в раздел **Сводное планирование \> Сводное планирование \> Спланированные заказы**.
1. Откройте спланированный заказ, который хотите проверить.
1. На экспресс-вкладке **Общее** посмотрите на значение в поле **Прогноз поставки**. Если заказ был создан для покрытия прогноза поставок, в этом поле будет установлено значение *Да*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Примеры сводного планирования с прогнозами поставок

В этом разделе представлено несколько примеров, демонстрирующих влияние прогнозирования поставок на сводное планирование.

### <a name="example-1-supply-forecast-for-an-item"></a>Пример 1. Прогноз поставки для номенклатуры

Имеется номенклатура, где типом заказа по умолчанию является *Заказ на покупку*, а поставщиком по умолчанию является *US-002*. Она имеет следующую строку прогноза поставок.

| Модель    | Дата     | Счет поставщика | Группа Поставщиков | Количество | Единица измерения | Сайт | Склад |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                |              | 35       | шт.   | 1    | 11        |

При выполнении сводного планирования будет создан спланированный заказ на покупку для *35 шт.* у поставщика *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Пример 2. Несколько строк прогноза поставок с поставщиком и без него

Имеется номенклатура, где типом заказа по умолчанию является *Заказ на покупку*, а поставщиком по умолчанию является *US-002*. Она имеет следующие строки прогноза поставок.

| Модель    | Дата     | Счет поставщика | Группа Поставщиков | Количество | Единица измерения | Сайт | Склад |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                |              | 35       | шт.   | 1    | 11        |
| CurrentF | 10.10.22 | US-101         |              | 25       | шт.   | 1    | 11        |

В этом случае система обрабатывает строку, не определяющую поставщика, в качестве общего прогноза, и предполагается, что строка, в которой указывается поставщик, должна вычитаться из общего прогноза. Поэтому при сводном планировании будут созданы следующие спланированные заказы на покупку для данной номенклатуры:

- Спланированный заказ на покупку для количества, равного *25 шт.*, у поставщика *US-101* (Используются поставщик и количество, указанные в строке прогноза.)
- Спланированный заказ на покупку в количестве *10 шт.* у поставщика *US-002* (Так как в другой строке прогноза не указан поставщик, используется поставщик по умолчанию, а количество этой строки прогноза уменьшается на количество в строке прогноза, относящейся к конкретному поставщику.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Пример 3. Планы, использующие метод сокращения "Проводки — динамический период" в один прогнозный период

Для сводных планов, использующих метод *Проводки — динамический период* в качестве метода сокращения прогнозов, сводное планирование будет снижать количество прогнозов, если имеются существующие проводки, соответствующие этим характеристикам поставок.

Например, имеется номенклатура, где типом заказа по умолчанию является *Заказ на покупку*. Она имеет следующую строку прогноза поставок.

| Модель    | Дата     | Счет поставщика | Группа Поставщиков | Количество | Единица измерения | Сайт | Склад |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | шт.   | 1    | 11        |

Поскольку имеется только одна строка прогноза поставок, имеется только один прогнозный период.

При запуске сводного плана, настроенного для использования *Проводки - динамический период* в качестве метода сокращения, могут появиться следующие результаты:

- Если заказ на покупку существует для поставщика *US-101* с количеством *10 шт.*, и в поле **Прогноз поставки** указано значение *Да*, сводное планирование создает новый спланированный заказ на покупку для оставшегося количества, равного *10 шт*. Строка прогноза будет уменьшена, поскольку поставщик соответствует существующему заказу на покупку.
- Если заказ на покупку существует для поставщика *US-102*, сайта *1*, склада *11* с количеством *10 шт.*, и в поле **Прогноз поставки** указано значение *Да*, сводное планирование создает новый спланированный заказ на покупку для полного количества, равного *25 шт*. Строка прогноза не может быть уменьшена, так как у нее имеется поставщик, отличный от поставщика существующего заказа на покупку.

> [!NOTE]
> Эта ситуация может возникнуть для спланированных заказов на покупку, так как с ними связан поставщик. Однако для заказов на перемещение и производственных заказов суммы прогнозов поставок всегда будут уменьшаться по существующим заказам, поскольку для этих типов заказов не указан поставщик.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Пример 4. Планы, использующие метод сокращения "Проводки — динамический период" за несколько прогнозных периодов

У вас имеется номенклатура, где типом заказа по умолчанию является *Заказ на покупку*. Она имеет следующие строки прогноза поставок.

| Модель    | Дата     | Счет поставщика | Группа Поставщиков | Количество | Единица измерения | Сайт | Склад |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | шт.   | 1    | 11        |
| CurrentF | 15.10.22 | US-101         |              | 25       | шт.   | 1    | 11        |

В этом примере имеются две строки прогноза, каждая из которых имеет свою дату. Таким образом, даты формируют границы прогнозных периодов. Первый период — с 10 октября по 14 октября 2022 года (10.10.22 – 14.10.22). Второй — с 15 октября 2022 года (15.10.22) и далее.

Имеется существующий заказ на покупку для поставщика *US-101* в количестве *10 шт.* и дата *12.10.22* (12 октября 2022 года). При запуске сводного плана, настроенного для использования *Проводки - динамический период* в качестве метода сокращения, и создаст следующие заказы:

- Спланированный заказ для количества, равного *15 шт.*, и датой *10.10.22* (Количество уменьшается на существующий заказ на покупку, датированный в том же прогнозном периоде.)
- Спланированный заказ для количества, равного *25 шт.*, и датой *15.10.22* (Количество представляет собой полное количество прогноза.)

### <a name="example-5-plans-that-use-no-reduction"></a>Пример 5. Планы, которые не используют сокращение

При выполнении плана, в котором метод сокращения прогнозов имеет значение *Нет*, сводное планирование всегда будет создавать запланированную поставку для всех строк прогноза поставок. После утверждения запланированной поставки она сокращает будущие спланированные заказы. Однако заказы на покупку не уменьшают строки прогноза поставок.

Например, имеется номенклатура, где типом заказа по умолчанию является *Заказ на покупку*. Она имеет следующую строку прогноза поставок.

| Модель    | Дата     | Счет поставщика | Группа Поставщиков | Количество | Единица измерения | Сайт | Склад |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | шт.   | 1    | 11        |

Имеется существующий заказ на покупку для поставщика *US-101*, сайта *1*, склада *11* в количестве *25 шт.* и датой *10.10.22*. 

При выполнении сводного плана, настроенного для использования метода сокращения *Нет*, создается запланированный заказ на покупку для поставщика *US-101*, сайта *1*, склада *11*, количества, равного *25 шт.* и датой *10.10.22*. Другими словами, существующий заказ на покупку не будет уменьшен, так как метод сокращения прогнозов имеет значение *Нет*.

Теперь можно изменить спланированный заказ на покупку, созданный после последнего выполнения планирования, и изменить количество на *15 шт*. Затем вы утверждаете заказ. При следующем запуске сводного плана будет создан спланированный заказ на покупку для поставщика *US-101*, сайта *1*, склада *11*, на количество, равное *10 шт.*, и с датой *10.10.22*. На этот раз количество будет уменьшено, чтобы отразится количество существующего утвержденного заказа из предыдущего выполнения планирования.

## <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Различия между оптимизацией планирования и устаревшей подсистемой сводного планирования

Прогнозы поставок работают немного по-разному в зависимости от того, какая подсистема планирования используется (оптимизация планирования или устаревшая подсистема сводного планирования). В этом разделе описываются различия.

### <a name="vendor-groups"></a>Группы поставщиков

При добавлении строки прогноза можно указать поставщика и группу поставщиков. В устаревшей подсистеме планирования создаваемые спланированные заказы группируются по комбинациям значений поставщиков и групп поставщиков. В оптимизации планирования спланированные заказы группируются по поставщикам.

В следующей таблице приводятся некоторые примеры строк прогноза поставок для номенклатуры.

| Модель    | Дата     | Счет поставщика | Группа Поставщиков | Количество | Единица измерения | Сайт | Склад |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                | VendorGroupA | 5        | шт.   | 1    | 11        |
| CurrentF | 10.10.22 |                | VendorGroupA | 6        | шт.   | 1    | 11        |
| CurrentF | 10.10.22 |                |              | 7        | шт.   | 1    | 11        |

Поставщик *VendorA* — это поставщик по умолчанию для группы поставщиков *VendorGroupA*. Это также поставщик по умолчанию для номенклатуры.

Устаревшая подсистема сводного планирования создаст следующие заказы:

- Спланированный заказ на покупку для поставщика *VendorA*, группы поставщиков *VendorGroupA* и количества *11*
- Спланированный заказ на покупку для поставщика *VendorA* и количества *7*

Оптимизация планирования создастся только один заказ:

- Спланированный заказ на покупку для поставщика *VendorA*, группы поставщиков *VendorGroupA* и количества *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Сокращение общих прогнозов за счет более конкретных прогнозов

В устаревшей подсистеме сводного планирования результат будет непредсказуемым, если у некоторых прогнозов имеется поставщик, но у других — нет.

В оптимизации планирования общие прогнозы всегда уменьшаются более конкретными прогнозам, как показано в следующем примере.

В следующей таблице приводятся некоторые примеры строк прогноза поставок для номенклатуры.

| Дата       | Количество | Поставщик   | Группа Поставщиков  |
|------------|----------|----------|---------------|
| 11.02.2022 | 5.00     | Vendor-A | VendorGroup-A |
| 11.02.2022 | 6,00     | Vendor-A | VendorGroup-A |
| 11.02.2022 | 15.00    |          |               |

Общий прогноз (на 15,00 штук) уменьшается на более конкретные прогнозы (на 5,00 + 6,00 = 11,00 штук). Остаток назначается поставщику по умолчанию. В следующей таблице показаны спланированные заказы.

| Дата       | Количество | Поставщик   | Группа Поставщиков  |
|------------|----------|----------|---------------|
| 11.02.2022 | 11.00    | Vendor-A | VendorGroup-A |
| 11.02.2022 | 4.00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Учет настроек заказа по умолчанию при создании спланированных заказов

У каждой номенклатуры могут быть настройки заказа по умолчанию, например, минимальное количество заказа на покупку. Устаревшая подсистема сводного планирования игнорирует эти настройки и, таким образом, транслирует прогнозы в спланированные заказы с одинаковым количеством. Оптимизация планирования уважает эти параметры при создании спланированных заказов из прогнозов поставок. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Агрегирование спланированных заказов в результате уменьшения по утвержденным заказам

Устаревшая подсистема сводного планирования предполагает, что только один заказ будет уменьшать существующий прогноз поставок. Таким образом, если несколько заказов соответствуют строке прогноза поставок, то она будет уменьшена только в первом заказе. При оптимизации планирования все заказы, которые соответствуют строке прогноза поставок, будут уменьшены.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Сокращение прогнозов только за счет соответствующих поставщиков

Когда устаревшая подсистема сводного планирования уменьшает прогноз по существующим выпущенным заказам на покупку, она не гарантирует, что поставщик в заказе на покупку соответствует поставщику из прогноза. Оптимизация планирования сокращает прогнозы только по заказам на покупку, которые имеют соответствующее значение в поле поставщика.

Для заказов на перемещение и на производство поле поставщика всегда игнорируется, поскольку оно не применяется для этих типов заказов.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Уменьшение прогнозов по заказам на перемещение

Если типом заказа по умолчанию для номенклатуры является *Перемещение*, прогнозы могут быть сокращены только существующими запланированными заказами на перемещение. Однако для производственных заказов и заказов на покупку только выпущенные заказы уменьшают прогноз поставок.

Устаревшая подсистема сводного планирования сокращает для всех состояний заказов на перемещение, в то время как оптимизация планирования сокращает прогноз только по заказам на перемещение, которые находятся в состоянии *Выпущен*.
