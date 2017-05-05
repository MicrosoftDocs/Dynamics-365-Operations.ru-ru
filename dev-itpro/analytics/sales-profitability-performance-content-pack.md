---
title: "Содержимое &quot;Показатели продаж и прибыльности&quot; для Power BI"
description: "В этой теме описывается содержание пакета содержимого Dynamics 365 for Operations - Показатели продаж и прибыльности для Microsoft Power BI. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые используются для построения пакета содержимого."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Содержимое "Показатели продаж и прибыльности" для Power BI

В этой теме описывается содержание пакета содержимого Dynamics 365 for Operations - Показатели продаж и прибыльности для Microsoft Power BI. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые используются для построения пакета содержимого.

<a name="overview"></a>Обзор
--------

Этот пакет содержимого создан для менеджеров по продажам для отслеживания ключевых показателей продаж для выручки, валовой прибыли и маржи прибыли. В нем используются данные о проводках продажи из Microsoft Dynamics 365 for Operations, и предоставляется как сводное представление сумм продаж по всей компании, так и эффективность продаж для клиентов и продуктов. Выделения изменений в росте доходов и прибыли с течением времени, отчеты могут использоваться для оповещения менеджеров о положительных и отрицательных тенденциях для отдельных клиентов и продуктов. Менеджерам категорий и региональным менеджерам будет полезно получать диаграммы, которые сравнивают прибыльность и рентабельность разных категорий продуктов и групп клиентов друг с другом для выделения отстающих и лидеров. Полный отчет, который отображает доходы по отдельным клиентам относительно рентабельности продаж, обеспечивает менеджеров по счетам основу для настройки своих усилий по продажам и маркетингу в соответствии с профилем каждого клиента. Пакет содержимого "Показатели продаж и прибыльности" позволяет менеджерам по продажам анализировать результаты продаж по следующим параметрам:

-   Выручка, с начала года (по группам клиентов и отдельным клиентам, категориям продаж и отдельным продуктам и географическим регионам)
-   Изменение выручки, по годам (по регионам клиентов и категориям продаж)

Прибыльность можно анализировать по следующим параметрам:

-   Валовая прибыль и рентабельность продаж (по группам клиентов и категориям продаж продуктов)
-   Изменение валовой прибыли, по годам
-   Рентабельность клиента (по выручке в сравнении с валовой прибылью)

## <a name="accessing-the-content-pack"></a>Доступ к пакету содержимого
Пакет содержимого Power BI "Показатели продаж и прибыльности" публикуется как ресурс реализации в Lifecycle Services (LCS), и доступ к нему возможен из Dynamics 365 for Operations. Дополнительные сведения о способах доступа и запуска отчетов Power BI см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Показатели, включенные в пакет содержимого
Пакет содержимого включает отчет, состоящий из набора показателей, отображаемых в виде диаграмм, плиток и таблиц. В следующей таблице приводится обзор визуализации в пакете содержимого.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Страница отчета**        | **Диаграммы**                                 | **Плитки**                                               |
| Выручка по клиентам    | Первые 10 клиентов по выручке                | Итого выручка                                           |
|                        | Общая выручка по группам клиентов            | Рост выручки по годам                                      |
|                        | Средняя выручка на клиента по группам клиентов | Валовая прибыль                                            |
|                        | Выручка и валовая прибыль по группам клиентов   |                                                         |
| Выручка по продуктам     | Выручка и валовая прибыль по категориям продаж   | Общее \# продуктов                                    |
|                        | Первые 10 продуктов по выручке                 | Общее число активных продуктов и процент от общего числа |
|                        | Общая выручка по категориям продаж            | Число продуктов, на которые приходится 80% выручки           |
| Выручка по периодам\*    | Выручка по месяцам                           | Рост выручки по годам                                      |
|                        | Конечное отклонение выручки, по годам             | Рост выручки по годам, %                                    |
|                        | Отклонение общих продаж по регионам клиентов    |                                                         |
| Выручка по местонахождению    | Выручка от продаж по городам                      |                                                         |
|                        | Рост выручки по годам, %                       |                                                         |
|                        | Выручка от продаж по регионам                    |                                                         |
| Рентабельность клиента | Валовая прибыль и выручка, по клиентам   | Валовая прибыль, валовая прибыль, рост выручки по годам          |
| Анализ рентабельности | Выручка и валовая прибыль по месяцам          |                                                         |
|                        | Первые 15 клиентов по валовой прибыли           |                                                         |
|                        | Валовая прибыль по месяцам, по годам                 |                                                         |

\* Выручка за этот год и прошлый год, а также рост по категориям продаж.

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Dynamics 365 for Operations используются для заполнения отчета в пакете содержимого "Показатели продаж и прибыльности". Эти данные представлены как агрегированные измерения, которые помещаются на временное хранение в хранилище объектов, которая представляет собой базу данных Microsoft SQL, оптимизированную для аналитики. Дополнительные сведения см. в блоге [Интеграция Power BI с хранилищем объектов в Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Сводные измерения в этом пакете содержимого являются подмножеством сводных измерений, которые были доступны в кубе продаж в Dynamics AX 2012 и AX 2012 R3. Для временного размещения сводных измерений куба в хранилище объектов необходимо сделать их развертываемыми. Дополнительные сведения см. в процедуре порядка временного размещения сводных изменений в хранилище объектов в блоге [Интеграция Power BI с хранилищем объектов в Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Следующие ключевые сводные измерения объекта строк накладной используются в качестве основы для пакета содержимого.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Объект**    | **Ключевые сводные измерения**               | **Источник данных для Dynamics 365 for Operations** | **Поле**                                    | **Описание**                          |
| Строки накладной | Реализация                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Сумма в валюте учета            |
|               | Стоимость проданных товаров                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Сумма затрат + корректировка                 |
|               | Сумма по строке комиссии — валюта учета | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Сумма комиссии в валюте учета |

В следующей таблице показаны ключевые сводные измерения объекта строк накладной, которые используются для создания нескольких вычисляемых мер в наборе данных пакета содержимого.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Мера**       | **Как рассчитывается**                                                                                |
| Валовая прибыль      | SUM(Выручка – себестоимость проданных товаров – комиссия – налог (включен в сумму строки накладной клиента))          |
| Валовая прибыль      | SUM(Валовая выручка / (Выручка – налог (включен в сумму строки накладной клиента)))             |
| Выручка за прошлый год | Выручка за прошлый год = CALCULATE(SUM('Строки накладной'\[Выручка\]), SAMEPERIODLASTYEAR(Даты\[Дата\])) |

Следующие ключевые измерения в **Куб продаж** используются в качестве фильтров, чтобы разделить агрегированные измерения, достичь большей детализации и получить более глубокое аналитическое представление.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Объект**       | **Примеры атрибутов**                           |
| Клиенты        | Группы клиентов, регионы клиентов, адрес, отрасль |
| Товары         | Номер продукта, Название продукта, Название групп номенклатур       |
| Категории продаж | Наименования категорий продаж                                 |
| Юридические лица   | Названия юридических лиц                                   |
| Даты            | Даты                                                |

По умолчанию пакет содержимого отображает данные для текущего календарного года, но можно открыть раздел фильтров отчета и изменить фильтр даты. Можно также изменить фильтр компаний.

## <a name="additional-resources"></a>Дополнительные ресурсы
Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

-   [Информационные объекты](..\data-entities\data-entities.md)
-   [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Добавление плиток Power BI в рабочие области](configure-power-bi-integration.md)


