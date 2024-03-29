---
title: Амортизация с уменьшаемым остатком в 150%
description: Эта статья представляет обзор метода амортизации с уменьшаемым остатком в 150 %.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3bccb9d64851901d43b55887bb66c9b1b4e5a70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870230"
---
# <a name="150-percent-reducing-balance-depreciation"></a>Амортизация с уменьшаемым остатком в 150%

[!include [banner](../includes/banner.md)]

Эта статья представляет обзор метода амортизации с уменьшаемым остатком в 150 %.

После настройки профиля амортизации ОС и выбора значения **Уменьшаемое сальдо в 150%** в поле **Метод** на странице **Профили амортизации** процент амортизации ОС, назначенных профилю амортизации, одинаков во все периоды амортизации. Этот процент рассчитывается на основе срока службы актива. Например, если срок службы актива составляет пять лет, проценты будут рассчитаны как 30 процентов (150% ÷ 5). 

Чтобы установить амортизацию с уменьшаемым сальдо в 150%, также необходимо выбрать параметры в полях **Год амортизации** и **Частота периода** на странице **Профили амортизации**. Варианты, которые доступны в поле **Частота периода**, зависят от значения, которое выбрано в поле **Год амортизации**.

## <a name="selection-of-depreciation-year"></a>Выбор года амортизации
Вы можете выбрать **Календарь** или **Фискальный** в поле **Год амортизации** на странице **Методы амортизации**. 

Значение по умолчанию равно **Календарь**. Выбранный вариант определяет параметры, доступные в поле **Частота периода**. Это поле определяет даты и суммы разноски амортизационных начислений в течении календарного года.

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

Если вы выберете **Финансовый** в поле **Год амортизации**, амортизация с уменьшаемым сальдо в 150% рассчитывается на основе финансового года для финансового календаря, заданного для книги, или по финансовому календарю, выбранному на странице **Книга учета**. Финансовые календари настраиваются на странице **Финансовые календари**. 

Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля. Финансовый год может быть длиннее или короче 12 месяцев. Амортизация корректируется для каждого периода. Длительность следующего финансового года определяется на основе настройки периодов, которые определяются на странице **Финансовые календари**. 

Если для года амортизации выбран вариант **Финансовый**, в поле **Частота периода** доступны следующие параметры.

-   **Ежегодно** — разноска общей суммы амортизации, рассчитанной для финансового года в последний день финансового года.
-   **Финансовый период** разносит полную сумму амортизации, вычисленную за финансовый год. Это количество начисляется в фискальные периоды, которые определены на странице **Финансовые календари**.

## <a name="example-of-150-reducing-balance-depreciation"></a>Пример амортизации с уменьшаемым остатком в 150%

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Стоимость приобретения               | 11,000 |
| Ликвидационная стоимость                  | 1,000  |
| База амортизации              | 10,000 |
| Годы срока службы             | 5      |
| Процент ежегодной амортизации | 30%    |

В методе уменьшаемого остатка с коэффициентом 150% значение в 150 процентов делится на количество лет срока службы. Этот процент умножается на остаточную стоимость актива для определения суммы амортизационных начислений за год.

| Период | Расчет суммы амортизационных начислений за год | Остаточная стоимость             | Остаточная стоимость на конец года |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1-й год | (11000 – 1000) × 30% = 3000                | 11000 – 3000 = 8000 | 11000 – 1000 – 3000 = 7000        |
| 2-й год | 7000 × 30% = 2100                           | 8,000 – 2,100 = 5,900  | 7,000 – 2,100 = 4,900                 |
| 3-й год | 4900 × 30% = 1470                           | 5900 – 1470 = 4430  | 4900 – 1470 = 3430                 |

> [!NOTE]
> Обычно если сумма, которая вычислена с помощью метода амортизации с уменьшаемым сальдо в 150%, становится меньше суммы, которая была бы получена при использовании метода прямой линии, производится переход на метод прямой линии на оставшийся срок службы.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
