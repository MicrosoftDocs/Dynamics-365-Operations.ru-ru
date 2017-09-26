---
title: "Ручная амортизация"
description: "Эта статья содержит обзор метода ручной амортизации."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 75d176623b4fdf2198440becd0345628f873f6da
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017

---

# <a name="manual-depreciation"></a>Ручная амортизация

[!include[banner](../includes/banner.md)]


Эта статья содержит обзор метода ручной амортизации.

Если вы настроите профиль амортизации основных средств и выберете **Вручную** в поле **Метод** на странице **Профили амортизации**, то амортизация основных средств, назначенная этому профилю амортизации, будет определяться процентом, введенным для каждого интервала календарного года. Интервалы, для которых вы настраиваете проценты, разносятся согласно значению, которое вы выбираете в поле **Частота периода** на экспресс-вкладке **Общие** на странице **Профили амортизации**. Могут быть выбраны следующие значения:

-   Ежегодно
-   Помесячная
-   Ежеквартально
-   Полгода
-   Ежедневно

После того, как вы выбираете частоту периода, щелкните **Графики ручных операций**, и настройте проценты для каждого интервала разноски. Графики списания и интервалы разноски вместе определяют сумму амортизации, как показано в приведенном ниже примере. При амортизации вручную величина амортизации всегда рассчитывается как процент от цены приобретения. При расчете амортизации вручную проценты, введенные для интервалов амортизации, в сумме могут не составлять 100 процентов. Ручная амортизация — это гибкий метод амортизации, который часто используется для определения нестандартных профилей амортизации на странице **Книги**, например для нерегулярного расчета амортизации в связи с особыми целями (например, связанными с расчетом налогов).

## <a name="examples"></a>Примеры
Цена приобретения: 11 000,00 Ожидаемая ликвидационная стоимость: 1000,00 В следующей таблице показаны интервалы и проценты, настроенные на странице **Графики профилей амортизации основных средств**.

| Номер интервала | Процент |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Способ расчета амортизации каждому по интервалу показан в следующей таблице.

|  Номер интервала | Расчет суммы амортизационных начислений за год | Остаточная стоимость на конец интервала |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11000 – 1000) × 10% = 1000                | 10000 (11000 – 1000)                   |
| 2                | (11000 – 1000) × 50% = 5000                | 5000 (10000 – 5000)                    |
| 3                | (11000 – 1000) × 8% = 800                   | 4200 (5000 – 800)                       |

Если выбрать **Ежемесячно** в поле **Частота периода**, необходимо будет вручную настроить 12 интервалов графика списания. Суммы амортизации для первых двух интервалов показаны в следующей таблице.

| Диапазон | Сумма начисленной амортизации            |
|----------|--------------------------------|
| Январь  | (11000 – 1000) × 10% = 1000 |
| Февраль | (11000 – 1000) × 50% = 5000 |

Если выбрать **Полгода** в поле ****Частота периода****, необходимо будет вручную настроить два интервала графика списания. Суммы амортизации для таких двух интервалов показаны в следующей таблице.

| Диапазон    | Сумма начисленной амортизации            |
|-------------|--------------------------------|
| 30 июня     | (11000 – 1000) × 10% = 1000 |
| 31 декабря | (11000 – 1000) × 50% = 5000 |

Общая сумма процентов для всех интервалов не должна быть обязательно равна 100. Однако вы получите сообщение, если значение в поле **Суммарный процент** на странице **Графики профилей амортизации основных средств** не равно **100**.



