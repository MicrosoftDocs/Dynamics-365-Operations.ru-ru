---
title: "Амортизация срока службы (прямолинейный метод)"
description: "Эта статья содержит обзор метода линейной амортизации."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: ae213018f5aeb24af21d95e4f0fbc1ca8e858fdc
ms.lasthandoff: 03/31/2017


---

# <a name="straight-line-service-life-depreciation"></a>Амортизация срока службы (прямолинейный метод)

[!include[banner](../includes/banner.md)]


Эта статья содержит обзор метода линейной амортизации.

Если при настройке профиля амортизации основных средств выбрано значение "Срок службы (прямолинейный метод)" в поле "Метод" на странице "Профили амортизации", амортизация основных средств, назначенных этому профилю амортизации, основывается на общем сроке службы основного средства. Обычно это одна и та же сумма амортизации в каждый период амортизации. 

Разницу между суммой амортизации, рассчитанной между оставшимся сроком службы (прямолинейный метод) и сроком службы (прямолинейный метод), составляет разнесенная в актив переоценка. 

Чтобы установить линейную амортизацию по сроку службы, также необходимо выбрать параметры в полях "Год амортизации" и "Частота периода" на странице "Профили амортизации".

## <a name="select-a-depreciation-year"></a>Выбор года амортизации
Вы можете выбрать "Календарь" или "Фискальный" в поле "Год амортизации" на странице "Методы амортизации". Выбранный вариант определяет параметры, доступные в поле "Частота периода". Значение по умолчанию — "Календарь".

### <a name="calendar"></a>Календарь

При выборе значения "Календарь" используется год с 1-го января по 31-е декабря, даже если финансовый календарь задан иначе. 

Параметр "Календарь" обновляет базу амортизации (обычно остаточная стоимость минус ликвидационная стоимость) 1-го января каждого года. В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов. 

Если выбран "Календарь", то в поле "Частота периода" имеются следующие параметры, которые определяют даты и суммы разноски амортизационных начислений в течение календарного года:
-   Ежегодно — разноска суммы 31-го декабря.
-   Ежемесячно — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.
-   Ежеквартально — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).
-   Полгода — разноска суммы за полгода один раз в конце каждого календарного полугодия (30 июня и 31 декабря).
-   Ежедневная — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.

Например, если выбрать параметр "Ежегодно", годовая амортизация разносится только один раз, каждый год 31 декабря. Если выбрать параметр "Ежемесячно", месячная амортизация разносится каждый месяц в сумме, равной 1/12 от суммы за год.

### <a name="fiscal"></a>Финансовый

При выборе параметра "Финансовый" в поле "Год амортизации" используется линейная амортизация по сроку службы. Эта сумма рассчитывается на основе финансового года, который определен финансовым календарем, указанным для книги, или финансовым календарем, выбранным на странице "Книга учета". Финансовые календари настраиваются на странице "Финансовые календари".

Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля. Финансовый год может быть длиннее или короче 12 месяцев. Амортизация корректируется автоматически для каждого финансового периода. Продолжительность следующего финансового года определяется по финансовым периодам, настроенным при создании нового финансового года в форме "Финансовые календари". 

Если выбрать "Финансовый" в поле "Частота периода", доступны следующие параметры частоты периода:
-   "Ежегодно" — разноска общей суммы амортизации, рассчитанной для финансового года как единая сумма в последний день финансового года.
-   "Финансовый период" — расчет общей суммы амортизации, вычисленной для финансового года, начисляемой в финансовые периоды, которые определяются в форме "Финансовые календари" для финансового календаря.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Пример: линейная амортизации неизменного основного средства
Предположим, что ОС обладает следующими характеристиками:

|                     |        |
|---------------------|--------|
| Стоимость приобретения    | 11 000 |
| Ликвидационная стоимость       | 1000  |
| База амортизации   | 10 000 |
| Годы срока службы  | 5      |
| Ежегодная амортизация | 2 000  |

Ежегодно вы получаете одну и ту же сумму амортизации. (Затраты на приобретение -стоимость ликвидации) / годы срока службы

| Период | Расчет суммы ежегодной амортизации | Остаточная стоимость в конце года |
|--------|-------------------------------------------|---------------------------------------|
| Год 1 | (11 000 – 1000) / 5 = 2000              | 9000                                 |
| Год 2 | (11 000 – 1000) / 5 = 2000              | 7 000                                 |
| Год 3 | (11 000 – 1000) / 5 = 2000              | 5 000                                 |
| Год 4 | (11 000 – 1000) / 5 = 2000              | 3 000                                 |
| Год 5 | (11 000 – 1000) / 5 = 2000              | 1000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Пример: Амортизация (прямолинейный метод) неизменного ОС

предположим, что вы добавили переоценку ввода в эксплуатацию, равную 4 000 в год 2 к тому же ОС. 

Срок службы переоценки ввода в эксплуатацию равен сроку службы ОС и начинается с момента ввода в эксплуатацию. Остаточная стоимость в конце года 5 соответствует остаточной стоимости переоценки приобретения. Способ расчета амортизации по периоду показан в следующей таблице.

| Период | Расчет суммы ежегодной амортизации | Остаточная стоимость в конце года |
|--------|-------------------------------------------|---------------------------------------|
| Год 1 | 10 000 / 5 = 2 000                        | 11 000 - 2 000 = 9 000                |
| Год 2 | 4 000 (Переоценка стоимости ввода в эксплуатацию)            | 9 000 + 4 000 =13 000                 |
| Год 2 | 14 000 / 5 = 2 800                        | 13 000 - 2 800 = 10 200               |
| Год 3 | 14 000 / 5 = 2 800                        | 10 200 - 2 800 = 7 400                |
| Год 4 | 14 000 / 5 = 2 800                        | 7 400 - 2 800 = 4 600                 |
| Год 5 | 14 000 / 5 = 2 800                        | 4 600 - 2 800 = 1 800                 |
| Год 6 | Остаток 800\*                           | 1 800 – 800 = 1 000                   |

\*Так как сумма остатка меньше суммы амортизации, в расчет берется только сумма остатка, которая меньше ликвидационной стоимости.





