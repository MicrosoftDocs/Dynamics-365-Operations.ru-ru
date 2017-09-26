---
title: "Содержимое управления затратами в Power BI"
description: "В этой теме описывается, что входит в содержимое Power BI для управления затратами. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 387b804cb20ffdc17ad74dac5d927ecbaf421bae
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017

---

# <a name="cost-management-power-bi-content"></a>Содержимое управления затратами в Power BI

[!include[banner](../includes/banner.md)]


В этой теме описывается, что входит в содержимое Power BI для управления затратами. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

# <a name="overview"></a>Обзор

Содержимое **Управление затратами** Microsoft Power BI предназначено для бухгалтеров, работающих с запасами, или отдельных лиц в организации, ответственных за запасы. Содержимое Power BI **Управление затратами** предоставляет управленческие сведения о запасах и запасах по незавершенному производству (НЗП), а также о потоках затрат через них по категориям с течением времени. Информация может также использоваться как подробное приложение к финансовой отчетности.

## <a name="key-measures"></a>Ключевые меры

+ Начальное сальдо
+ Конечное сальдо
+ Чистое изменение
+ Чистое изменение в %
+ Распределение по срокам

## <a name="key-performance-indicators"></a>Ключевые показатели эффективности
+ Оборот запасов
+ Точность запасов

Первичный источник данных для CostAggregatedCostStatementEntryEntity является таблицей CostStatementCache. Эта таблица управляется структурой кэш-памяти набора данных. По умолчанию таблица обновляется каждые 24 часа, но можно включить возможность ручного обновления в конфигурации кэш-памяти данных. Затем можно выполнить обновление вручную в рабочей области **Управление затратами** или **Анализ затрат**. После запуска обновления CostStatementCache необходимо обновить подключение OData на сайте Power BI.com, чтобы увидеть обновленные данные на сайте. Меры отклонения (покупка, производство) в данном содержимом Power BI относятся только к элементам, которые оцениваются методом оценки стандартной себестоимости. Отклонение производственных затрат рассчитывается как разница между активными затратами и реализованными затратами. Отклонение производственных затрат рассчитывается, когда производственный заказ имеет статус **Завершено**. Дополнительные сведения о типах производственных отклонений и о порядке расчета для каждого типа см. в разделе [Об анализе расхождений в выполненном производственном заказе](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Доступ к содержимому Power BI
Содержимое Power BI **Управление затратами** доступно на сайте PowerBI.com. Дополнительные сведения о том, как подключить и загрузить данные Microsoft Dynamics 365 Finance and Operations, см. в разделе [Доступ к содержимому Power BI с сайта PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Показатели, которые включены в содержимое Power BI
Содержимое включает в себя набор страниц отчета. Каждая страница состоит из набора показателей, которые отображаются в виде диаграмм, плиток и таблиц. В следующей таблице приводится обзор визуализации в содержимом Power BI **Управление затратами**.

| Страница отчетности | Диаграммы | Обращения |
|---|---|---|
|Общие запасы (по умолчанию за текущий период) |Точность |Меры запасов:<br>Конечное сальдо запасов<br>Чистое изменение запасов<br>Чистое изменение запасов, %<br>|
| |Оборот запасов | |
| |Конечное сальдо запасов по группам ресурсов | |
| |Чистое изменение запасов по именам категорий уровня 1 и именам категорий уровня 2| |
| |Отклонения закупочных цен по группам ресурсов и именам категорий уровня 3 | |
|Запасы по сайтам (по умолчанию за текущий период) |Конечное сальдо запасов по именам сайтов и группам ресурсов | |
| |Оборот запасов по именам сайтов и группам ресурсов | |
| |Конечное сальдо запасов по городам и группам ресурсов | |
|Запасы по группам ресурсов (по умолчанию за текущий период) |Меры запасов | |
| |Точность запасов по суммам по группам ресурсов | |
| |Оборот запасов по суммам по группам ресурсов | |
|Годовые запасы (по умолчанию: в текущем году по сравнению с предыдущим годом) |Меры запасов | |
| |Ключевые показатели эффективности запасов:<br>Оборот запасов<br>Точность запасов | |
| |Конечное сальдо запасов по годам и группам ресурсов | |
| |Отклонения закупочных цен по годам и именам категорий уровня 3 | |
|Распределение по срокам запасов (по умолчанию на текущий год) |Распределение по срокам запасов по кварталам и группам ресурсов | |
| |Распределение по срокам запасов по кварталам и имени сайта | |
|Общее НЗП (по умолчанию: за текущий период) |Чистое изменение НЗП по именам категорий уровня 1 и именам категорий уровня 2 |Меры незавершенного производства:<br>Конечное сальдо НЗП<br>Чистое изменение НЗП<br>Чистое изменение НЗП, %<br> |
| |Отклонения производства по группам ресурсов и именам категорий уровня 3 | |
| |Чистое изменение НЗП по группам ресурсов | |
|НЗП по сайтам (по умолчанию: за текущий период) |Меры незавершенного производства | |
| |Чистое изменение НЗП по именам сайтов и именам категорий уровня 2 | |
| |Отклонения производства по именам сайтов и именам категорий уровня 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Finance and Operations используются для заполнения страниц отчета в содержимом Power BI **Управление затратами**. Эти данные представлены как агрегированные измерения, которые помещаются на временное хранение в хранилище объектов, которая представляет собой базу данных Microsoft SQL, оптимизированную для аналитики. Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md). Следующие ключевые агрегированные измерения используются в качестве основы содержимого.

| Объект            | Ключевое агрегированное измерение | Источником данных является Finance and Operations | Поле             | описание                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Записи выписки | Чистое изменение                | CostAggregatedCostStatementEntryEntity      | sum(\[Сумма\])   | Сумма в валюте учета |
| Записи выписки | Количество чистого изменения       | CostAggregatedCostStatementEntryEntity      | sum(\[Количество\]) |                                   |

В следующей таблице показано, как ключевые агрегированные измерения используются для создания нескольких вычисляемых мер в наборе данных содержимого.

| Мера                                 | Как вычисляется мера                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Начальное сальдо                       | \[Конечное сальдо\]-\[Чистое изменение\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Количество начального сальдо              | \[Количество конечного сальдо\]-\[Количество чистого изменения\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Конечное сальдо                          | CALCULATE(SUM(\[Сумма\]), FILTER(ALLEXCEPT('Финансовые календари', 'Финансовые календари'\[LedgerRecId\], 'объекты'\[ID\], 'объекты'\[Имя\], 'Книги учета'\[Валюта\], 'Книги учета'\[Описание\], 'Книги учета'\[Имя\]), 'Финансовые календари'\[Дата\] &lt;= MAX('Финансовые календари'\[Дата\])))                                                                                                                                                                                           |
| Конечное сальдо по количеству                 | CALCULATE(SUM(\[Количество\]), FILTER(ALLEXCEPT('Финансовые календари', 'Финансовые календари'\[LedgerRecId\], 'объекты'\[ID\], 'объекты'\[Имя\], 'Книги учета'\[Валюта\], 'Книги учета'\[Описание\], 'Книги учета'\[Имя\]), 'Финансовые календари'\[Дата\] &lt;= MAX('Финансовые календари'\[Дата\])))                                                                                                                                                                                         |
| Начальное сальдо запасов             | CALCULATE(\[Начальное сальдо\], 'Записи выписки'\[Тип выписки\] = "Запасы")                                                                                                                                                                                                                                                                                                                                                                                      |
| Конечное сальдо запасов                | CALCULATE(\[Конечное сальдо\], 'Записи выписки'\[Тип выписки\] = "Запасы")                                                                                                                                                                                                                                                                                                                                                                                         |
| Чистое изменение запасов                    | CALCULATE(\[Чистое изменение\], 'Записи выписки'\[Тип выписки\] = "Запасы")                                                                                                                                                                                                                                                                                                                                                                                             |
| Чистое изменение запасов по количеству           | CALCULATE(\[Чистое изменение по количеству\], 'Записи выписки'\[Тип выписки\] = "Запасы")                                                                                                                                                                                                                                                                                                                                                                                    |
| Чистое изменение запасов, %                  | IF(\[Конечное сальдо запасов\] = 0, 0, \[Чистое изменение запасов\] / \[Конечное сальдо запасов\])                                                                                                                                                                                                                                                                                                                                                                           |
| Оборот запасов по сумме                | if(OR(\[Среднее сальдо запасов\] &lt;= 0, \[Проданные или израсходованные запасы\] &gt;= 0), 0, ABS(\[Проданные или израсходованные запасы\])/\[Среднее сальдо запасов\])                                                                                                                                                                                                                                                                                                  |
| Среднее сальдо запасов               | (\[Конечное сальдо запасов\] + \[Начальное сальдо запасов\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Проданные или израсходованные запасы       | \[Проданные запасы\] + \[Материальные затраты для израсходованных запасов\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Материальные затраты для израсходованных запасов        | CALCULATE(\[Чистое изменение запасов\], 'Записи выписки'\[Имя категории - уровень 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Проданные запасы                          | CALCULATE(\[Чистое изменение запасов\], 'Записи выписки'\[Имя категории - уровень 2\_\] = "Продано")                                                                                                                                                                                                                                                                                                                                                                             |
| Точность запасов по сумме            | IF(\[Конечное сальдо запасов\] &lt;= 0, IF(OR(\[Подсчитанная сумма запасов\] &lt;&gt; 0, \[Конечное сальдо запасов\] &lt; 0), 0, 1), MAX(0, (\[Конечное сальдо запасов\] - ABS(\[Подсчитанная сумма запасов\]))/\[Конечное сальдо запасов\]))                                                                                                                                                                                                                              |
| Подсчитанная сумма запасов                | CALCULATE(\[Чистое изменение запасов\], 'Записи выписки'\[Имя категории - уровень 3\_\] = "Инвентаризация")                                                                                                                                                                                                                                                                                                                                                                         |
| Распределение запасов по срокам                         | if(ISBLANK(max('Финансовые календари'\[Дата\])), blank(), MAX(0, MIN(\[Приходы распределения запасов по срокам по количеству\], \[Конечное сальдо распределения запасов по срокам по количеству\] - \[Приходы распределения запасов по срокам по количеству в будущем\]))) \* \[Средние затраты на единицу запасов\]                                                                                                                                                                                                                                |
| Приходы распределения запасов по срокам по количеству       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Чистое изменение запасов по количеству\], 'Записи выписки'\[Количество\] &gt; 0, FILTER(ALLEXCEPT('Финансовые календари', 'Финансовые календари'\[LedgerRecId\], 'объекты'\[ID\], 'объекты'\[Имя\], 'Книги учета'\[Валюта\], 'Книги учета'\[Описание\], 'Книги учета'\[Имя\]), 'Финансовые календари'\[Дата\] &lt;= MAX('Финансовые календари'\[Дата\]))), CALCULATE(\[Чистое изменение запасов по количеству\], 'Записи выписки'\[Количество\] &gt; 0)) |
| Конечное сальдо распределения запасов по срокам по количеству | \[Конечное сальдо запасов по количеству\] + CALCULATE(\[Чистое изменение запасов по количеству\], FILTER(ALLEXCEPT('Финансовые календари', 'Финансовые календари'\[LedgerRecId\], 'объекты'\[ID\], 'объекты'\[Имя\], 'Книги учета'\[Валюта\], 'Книги учета'\[Описание\], 'Книги учета'\[Имя\]), 'Финансовые календари'\[Дата\] &gt; max('Финансовые календари'\[Дата\]) ))                                                                                                                                 |
| Приходы распределения запасов по срокам в будущем  | CALCULATE(\[Чистое изменение запасов\], 'Записи выписки'\[Сумма\] &gt; 0, FILTER(ALLEXCEPT('Финансовые календари', 'Финансовые календари'\[LedgerRecId\], 'объекты'\[ID\], 'объекты'\[Имя\], 'Книги учета'\[Валюта\], 'Книги учета'\[Описание\], 'Книги учета'\[Имя\]), 'Финансовые календари'\[Дата\] &gt; MAX('Финансовые календари'\[Дата\])))                                                                                                                                             |
| Средние затраты на единицу запасов                 | CALCULATE(\[Конечное сальдо запасов\] / \[Конечное сальдо запасов по количеству\],ALLEXCEPT('Финансовые календари', 'Финансовые календари'\[LedgerRecId\], 'объекты'\[ID\], 'объекты'\[Имя\], 'Книги учета'\[Валюта\], 'Книги учета'\[Описание\], 'Книги учета'\[Имя\]))                                                                                                                                                                                                                 |
| Расхождение по закупкам                      | CALCULATE(SUM(\[Сумма\]), 'Записи выписки'\[Имя категории - уровень 2\_\] = "Приобретено", 'Записи выписки'\[Тип выписки\] = "Отклонение")                                                                                                                                                                                                                                                                                                                              |
| Начальное сальдо НЗП                   | CALCULATE(\[Начальное сальдо\], 'Записи выписки'\[Тип выписки\] = "НЗП")                                                                                                                                                                                                                                                                                                                                                                                            |
| Конечное сальдо НЗП                      | CALCULATE(\[Конечное сальдо\], 'Записи выписки'\[Тип выписки\] = "НЗП")                                                                                                                                                                                                                                                                                                                                                                                               |
| Чистое изменение НЗП                          | CALCULATE(\[Чистое изменение\], 'Записи выписки'\[Тип выписки\] = "НЗП")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Чистое изменение НЗП, %                        | IF(\[Конечное сальдо НЗП\] = 0, 0, \[Чистое изменение НЗП\] / \[Конечное сальдо НЗП\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Отклонения в производстве                    | CALCULATE(SUM(\[Сумма\]), 'Записи выписки'\[Имя категории - уровень 2\_\] = "ManufacturedCost", 'Записи выписки'\[Тип выписки\] = "Отклонение")                                                                                                                                                                                                                                                                                                                      |
| Имя категории - уровень 1                 | switch(\[Имя категории - уровень 1\_\], "None", "Нет", "NetSourcing", "Чистые источники", "NetUsage", "Чистое потребление", "NetConversionCost", "Чистая стоимость преобразования", "NetCostOfGoodsManufactured", "Чистая стоимость произведенных товаров", "BeginningBalance", "Начальное сальдо")                                                                                                                                                                                                         |
| Имя категории - уровень 2                 | switch(\[Имя категории - уровень 2\_\], "None", "Нет", "Procured", "Приобретено", "Disposed", "Выбыло", "Transferred", "Перенесено", "Sold", "Продано", "ConsumedMaterialsCost", "Стоимость потребленных материалов", "ConsumedManufacturingCost", "Понесенные производственные затраты", "ConsumedOutsourcingCost", "Понесенные затраты на аутсорсинг", "ConsumedIndirectCost", "Понесенные косвенные затраты", "ManufacturedCost", "Стоимость производства", "Variances", "Отклонения")                            |
| Имя категории - уровень 3                 | switch(\[Имя категории - уровень 3\_\], "None", "Нет", "Counting", "Нет", "ProductionPriceVariance", "Цена производства", "QuantityVariance", "Количество", "SubstitutionVariance", "Замена", "ScrapVariance", "Отходы", "LotSizeVariance", "Размер партии", "RevaluationVariance", "Переоценка", "PurchasePriceVariance", "Цена закупки", "CostChangeVariance", "Изменение себестоимости", "RoundingVariance", "Округление расхождения")                                                   |

Следующие ключевые измерения используются в качестве фильтров, чтобы разделить агрегированные измерения, достичь большей детализации и получить более глубокое аналитическое представление.

| Объект           | Примеры атрибутов                       |
|------------------|----------------------------------------------|
| Объекты         | Код, Имя                                     |
| Финансовые календари | Календарь, Месяц, Период, Квартал, Год       |
| Цели ключевого показателя эффективности        | Цель точности запасов, цель оборота запасов |
| Главные книги          | Валюта, Имя, Описание                  |
| Сайты            | Код, Имя, Страна, Город                      |

## <a name="additional-resources"></a>Дополнительные ресурсы
Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

-   [Информационные объекты](..\data-entities\data-entities.md)
-   [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Добавление плиток Power BI в рабочие области](configure-power-bi-integration.md)




