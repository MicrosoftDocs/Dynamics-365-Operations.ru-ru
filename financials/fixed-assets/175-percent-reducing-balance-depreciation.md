---
title: "Амортизация с уменьшаемым остатком в 175%"
description: "Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 175 %."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 812fbb3cc3159783e9908e537c366ffc7f934092
ms.lasthandoff: 03/31/2017


---

# <a name="175-percent-reducing-balance-depreciation"></a>Амортизация с уменьшаемым остатком в 175%

Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 175 %.

После настройки профиля амортизации ОС и выбора значения **Уменьшаемое сальдо в 175%** в поле **Метод** на странице **Профили амортизации** процент амортизации ОС, назначенных профилю амортизации, одинаков во все периоды амортизации. 

Чтобы установить амортизацию с уменьшаемым сальдо в 175%, также необходимо выбрать параметры в полях **Год амортизации** и **Частота периода** на странице **Профили амортизации**. Варианты, которые доступны в поле **Частота периода**, зависят от значения, которое выбрано в поле **Год амортизации**.

## <a name="select-a-depreciation-year"></a>Выбор года амортизации
Вы можете выбрать **Календарь** или **Фискальный** в поле **Год амортизации** на странице **Методы амортизации**. Значение по умолчанию равно **Календарь**. 

Выбранный вариант определяет параметры, доступные в поле **Частота периода**. Это поле определяет даты и суммы разноски амортизационных начислений в течении календарного года.

### <a name="calendar"></a>Календарь

Можно сохранить значение по умолчанию в поле **Год амортизации**, **Календарь**. 

Параметр **Календарь** обновляет базу амортизации 1-го января каждого года. Обычно базой амортизации является остаточная стоимость минус ликвидационная стоимость. В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов. 

Если для года амортизации выбран вариант **Календарь**, в поле **Частота периода** доступны следующие параметры.

-   **Ежегодно** — разноска суммы 31-го декабря.
-   **Ежемесячно** — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.
-   **Ежеквартально** — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).
-   **Каждый полгода** — разноска суммы за полгода один раз в конце календарного полугодия (30 июня и 31 декабря).
-   **Ежедневно** — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.

### <a name="fiscal"></a>Финансовый

Если вы выберете **Финансовый** в поле **Год амортизации**, амортизация с уменьшаемым сальдо в 175% рассчитывается на основе финансового года для финансового календаря, заданного для книги, или по финансовому календарю, выбранному на странице **Книга учета**. Финансовые календари настраиваются на странице **Финансовые календари**. Подробные сведения см. на странице [Финансовые календари, финансовые годы и периоды.](\financials\budgeting\fiscal-calendars-fiscal-years-periods.md).

Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля. Финансовый год может быть длиннее или короче 12 месяцев. Амортизация автоматически регулируется для каждого финансового периода, а длительность следующего финансового года определяется на настройкой периодов на странице **Финансовые календари**. 

Если для года амортизации выбран вариант **Финансовый**, в поле **Частота периода** доступны следующие параметры.

-   **Ежегодно** — разноска общей суммы амортизации, рассчитанной для финансового года в последний день финансового года.
-   **Финансовый период** — высчитывает полную сумму амортизации за финансовый год. Это количество начисляется в фискальные периоды, которые определены на странице **Финансовые календари**.

## <a name="example-of-175-reducing-balance-depreciation"></a>Пример амортизации уменьшаемого сальдо в 175%
|                                |        |
|--------------------------------|--------|
| Стоимость приобретения               | 11 000 |
| Ликвидационная стоимость                  | 1,000  |
| База амортизации              | 10 000 |
| Срок службы в годах             | 5      |
| Процент ежегодной амортизации | 35%    |

В методе амортизации с уменьшаемым остатком 175% значение в 175 процентов делится на количество лет срока службы. Этот процент умножается на остаточную стоимость актива для определения суммы амортизационных начислений за год.

| Период | Расчет суммы амортизационных начислений за год | Остаточная стоимость                  | Остаточная стоимость на конец года |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| 1-й год | (11000 – 1000) × 35% = 3500                | 11000 – 3500 = 7500      | 11000 – 1000 – 3500 = 6500        |
| 2-й год | 6500 × 35% = 2275                           | 7500 – 2275 = 5225       | 6500 – 2275 = 4225                 |
| 3-й год | 4225 × 35% = 1478,75                        | 5225 – 1478,75 = 3746,25 | 4225 – 1478,75 = 2746,25           |

> [!NOTE] 
> Обычно если сумма, которая вычислена с помощью метода амортизации с уменьшаемым сальдо в 175%, становится меньше суммы, которая была бы получена при использовании метода прямой линии, производится переход на метод прямой линии на оставшийся срок службы.

