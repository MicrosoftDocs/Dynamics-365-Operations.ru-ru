---
title: Содержимое Power BI "Производительность склада"
description: В этой статье описывается, что входит в содержимое Power BI "Производительность склада".
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.form: WHSWarehousePerformancePowerBI
ms.openlocfilehash: 82f43f45b43df864cbda8ba372dbed46d8f4c7e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289857"
---
# <a name="warehouse-performance-power-bi-content"></a>Содержимое Power BI "Производительность склада"

[!include [banner](../includes/banner.md)]

В этой статье описывается, что входит в содержимое Microsoft Power BI **Производительность склада**. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые используются для построения пакета содержимого.

## <a name="overview"></a>Обзор

Содержимое Power BI **Производительность склада** было создано, чтобы менеджеры складов и операций могли контролировать важные показатели входящих потоков, исходящих потоков и запасов. В нем используются данные управления складом, данные продуктов и другие данные проводок из вашей системы и для формирования как агрегированного представления эффективности складских операций, так и разбивки по поставщикам, группам продуктов и продуктам, а также сайтам и складам.

Менеджеры склада могут использовать содержимое **Производительность склада** для Power BI для измерения следующих трех областей:

- **Производительность входящих операций** позволяет оценить выполнение поставщиком требований клиента (другими словами, измерить эффективность поставок) и измерить производительность размещения, чтобы вы могли выявлять проблемы, связанные с сотрудниками или номенклатурами за определенный период. Очень важно знать, выполняют ли поставщики поставку вовремя, раньше срока или с задержкой, чтобы можно было определить, как работа поставщика влияет на общую производительность размещения. Поставщик, который поставляет товары вне согласованных дат, может создавать дополнительные проблемы на складе из-за незапланированных работ, и может увеличить среднее время размещения.
- **Производительность отгрузки** позволяет оценить, производит ли склад отгрузку клиентам в полном объеме и вовремя (другими словами, измеряет производительность исходящей отгрузки и доставки), чтобы вы могли выявлять проблемы, связанные с продуктами, сайтами, складами или отдельными клиентами. Если вы обнаружите, что поставка в определенные области или города осуществляется с задержкой, вам может потребоваться уделять больше внимания управлению транспортировкой или работе с заказчиком.
- **Точность запасов в местонахождении**: точность запасов является важной составной частью внутренней складской бизнес-аналитики. Очень важно определить общую точность инвентаризации. Однако также важно определить, насколько точно вы храните номенклатуры в правильных местах, и выделить данные о несоответствии, чтобы можно было найти лучшие позиции для номенклатур или инициировать полную инвентаризацию для отдельных номенклатур. (В настоящее время новая функциональная возможность инвентаризации на основе номенклатур доставляется в виде исправления.) Если вы используете данное содержимое Power BI для определения правильности данных запасов в наличии по местоположению, также можно выявлять хищения в ваших магазинах. Также можно определить, нет ли в каких-либо местах количеств в наличии, которые отличаются от данных по планированию ресурсов предприятия (ERP). Эти места могут быть слишком большими или в них может быть невозможно провести инвентаризацию. Кроме того, часть физических расположений может быть плохой, поэтому трудно поддерживать синхронизацию одного типа номенклатуры с данными о запасах в наличии.

## <a name="accessing-the-power-bi-content-pack"></a>Доступ к пакету содержимого Power BI
Содержимое Power BI **Эффективность склада** отображается на странице **Эффективность склада** (**Управление складом** \> **Запросы и отчеты** \> **Анализ эффективности склада** \> **Эффективность склада**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Показатели, включенные в пакет содержимого Power BI
Содержимое **Производительность склада** Power BI включает отчет. Этот отчет состоит из набора показателей, которые отображаются в виде диаграмм, плиток и таблиц. В следующей таблице приводится обзор визуализации в содержимом Power BI **Производительность склада**.

| Страница отчета                 | Диаграммы                                   | описание |
|-----------------------------|------------------------------------------|-------------|
| Производительность входящих операций         | Всего размещений                          | Число строк работы размещения, обработанных в течение заданного времени. |
| Производительность входящих операций         | Среднее время размещения                    | Среднее время, в часах, для всех обработанных строк размещения заказов на покупку, от регистрации номенклатур до обработки последнего размещения. |
| Производительность входящих операций         | Получено с опережением                           | Количество строк заказа на покупку, которые были получены досрочно. |
| Производительность входящих операций         | Получено вовремя                         | Количество строк заказа на покупку, которые были получены вовремя. |
| Производительность входящих операций         | Получено с опозданием                            | Количество строк заказа на покупку, которые были получены с задержкой. |
| Производительность входящих операций         | Вовремя по поставщику                        | Представление процента строк заказа на покупку, которые получены от поставщика или группы поставщиков раньше времени, вовремя и с задержкой. |
| Производительность входящих операций         | Среднее время размещения от дебаркадера до запасов (в часах) | Среднее время размещения в часах с течением времени. |
| Производительность входящих операций         | Среднее значение размещения работником               | Среднее время в часах, которые работник тратит на обработку размещения строк заказа на покупку. |
| Производительность входящих операций         | Среднее значение размещения в часах по поставщикам          | Среднее время размещения в часах по поставщикам или группам поставщиков. |
| Производительность входящих операций         | Среднее значение размещения в часах по продуктам         | Среднее время размещения в часах по номенклатурам или группам номенклатур. |
| Точность местоположения запасов | Общее количество                              | Число строк работы инвентаризации, обработанных для заданного периода. |
| Точность местоположения запасов | Коэффициент расхождения                         | Общий коэффициент расхождения в процентах от всех строк, для которых выполняется инвентаризация за данный период. |
| Точность местоположения запасов | Количество без несоответствия                | Число строк, которые обрабатываются без каких-либо расхождения, в процентах от общего количества обработанных строк работы инвентаризации. |
| Точность местоположения запасов | Номенклатуры, для которых выполнена инвентаризация в зависимости от времени                  | Процент номенклатур, при инвентаризации которых были и не были выявлены расхождения, как функция времени. |
| Точность местоположения запасов | Несоответствие количества номенклатуры, превышающее % | Строки инвентаризации в табличном виде, расхождение в которых превышает указанный процент. Таблица содержит сведения о местонахождении, номенклатурах, среднем несоответствии, общем числе строк работы инвентаризации, общем числе строк инвентаризации, которые имеют несоответствия для местонахождения, среднем количестве по результатам инвентаризации, ожидаемом общем количестве по результатам инвентаризации и фактическом количестве номенклатуры, для которой проводится инвентаризация. |
| Точность местоположения запасов | Инвентаризация номенклатуру по работникам                     | Производительность инвентаризации по работникам. Производительность выражается в процентах от строк работы инвентаризации, в которых имеется и отсутствует несоответствие. |
| Точность местоположения запасов | Инвентаризация номенклатуры по площадкам/складам           | Производительность инвентаризации по количеству обработанных строк работы инвентаризации по сайтам или складам, на которых есть и на которых нет несоответствий. |
| Точность местоположения запасов | Коэффициент расхождения по продуктам              | Коэффициент расхождения для производительности инвентаризации. Коэффициент выражается в процентах от обработанные строк работы инвентаризации по номенклатурам или номенклатурным группам. |
| Производительность отгрузки        | Отгруженные строки                            | Общее число строк отгрузки, отгруженных за заданный период. |
| Производительность отгрузки        | С опережением                                    | Процент строк отгрузки, которые были отгружены раньше срока. |
| Производительность отгрузки        | Вовремя                                  | Процент строк отгрузки, которые были отгружены вовремя. |
| Производительность отгрузки        | С опозданием                                     | Процент строк отгрузки, которые были отгружены с задержкой. |
| Производительность отгрузки        | Отгрузки по времени                      | Процент строк отгрузки, которые отгружены вовремя, раньше срока или позже срока за данный период. Линия тенденции, которая показывает тенденцию для строк, которые были отгружены вовремя. |
| Производительность отгрузки        | Отгружены с задержкой по городам                     | Визуальная карта городов и областей, в которых отгрузка выполнялась с задержкой. |
| Производительность отгрузки        | Отгружено по продуктам                       | Процент, который был отгружен досрочно, своевременно или с задержкой, по номенклатурам или номенклатурным группам. |
| Производительность отгрузки        | Отгружено по клиентам                      | Процент, который был отгружен досрочно, своевременно или с задержкой, по клиентам или группам клиентов. |
| Производительность отгрузки        | Отгружено по сайтам/складам              | Процент, который был отгружен досрочно, своевременно или с задержкой, по сайтам или складам. |

## <a name="understanding-the-data-model-and-calculations"></a>Понимание модели данных и расчетов
Следующие данные используются для заполнения страниц отчета в содержимом Power BI **Производительность склада**. Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов. Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики. Дополнительные сведения см. в разделе [Интеграция Power BI с хранилищем объектов](power-bi-integration-entity-store.md).

Следующие ключевые агрегированные измерения используются в качестве основы содержимого.

| Страница отчета                 | Диаграммы                                   | Таблицы                                | Описание расчета |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Производительность входящих операций         | Всего размещений                          | WHSWorkLine                           | Количество строк работы, в которых тип работы имеет значение **складирование**. |
| Производительность входящих операций         | Среднее время размещения                    | WHSWorkLine                           | Сумма макс. времени строк работы, деленная на макс. время строк работы, где макс. время строк работы является максимальным промежутком между датой создания и датой закрытия работы. |
| Производительность входящих операций         | Получено с опережением                           | WHSWorkLine                           | Число строк работы, в которых дата создания работы раньше даты поставки, которая используется. Если подтвержденная дата поставки еще не задана, используется дата поставки по умолчанию. |
| Производительность входящих операций         | Получено вовремя                         | WHSWorkLine                           | Число строк работы, в которых дата создания работы равна дате поставки, которая используется. Если подтвержденная дата поставки еще не задана, используется дата поставки по умолчанию. |
| Производительность входящих операций         | Получено с опозданием                            | WHSWorkLine                           | Число строк работы, в которых дата создания работы позже даты поставки, которая используется. Если подтвержденная дата поставки еще не задана, используется дата поставки по умолчанию. |
| Производительность входящих операций         | Вовремя по поставщику                        | WHSWorkLine                           | Получено c опережением, получено вовремя и получено с опозданием (см. описания выше в этой таблице). |
| Производительность входящих операций         | Среднее время размещения от дебаркадера до запасов (в часах)   | WHSWorkLine                           | Среднее время размещения (см. описание выше в этой таблице). |
| Производительность входящих операций         | Среднее значение размещения работником               | WHSWorkLine                           | Среднее время размещения (см. описание выше в этой таблице). |
| Производительность входящих операций         | Среднее значение размещения в часах по поставщикам          | WHSWorkLine                           | Среднее время размещения (см. описание выше в этой таблице). |
| Производительность входящих операций         | Среднее значение размещения в часах по продуктам         | WHSWorkLine                           | Среднее время размещения (см. описание выше в этой таблице). |
| Точность местоположения запасов | Общее количество                              | WHSWorkLineCycleCount                 | Количество циклов инвентаризации, в которых абсолютное количество несоответствия равно или больше 0 (нуля). |
| Точность местоположения запасов | Коэффициент расхождения                         | WHSWorkLineCycleCount                 | Количество циклов инвентаризации, имеющих несоответствия, деленное на общее количество. Цикл инвентаризации считается имеющим несоответствия, если абсолютное количество несоответствия превышает 0 (ноль). |
| Точность местоположения запасов | Количество без несоответствия                | WHSWorkLineCycleCount                 | Количество циклов инвентаризации, в которых абсолютное количество несоответствия больше 0 (нуля). |
| Точность местоположения запасов | Количество с несоответствием                   | WHSWorkLineCycleCount                 | Количество циклов инвентаризации, в которых абсолютное количество несоответствия равно 0 (нуля). |
| Точность местоположения запасов | Номенклатуры, для которых выполнена инвентаризация в зависимости от времени                  | WHSWorkLineCycleCount                 | Количество без расхождения и количество с расхождением (см. описания выше в этой таблице). |
| Точность местоположения запасов | Несоответствие количества номенклатуры, превышающее % | WHSWorkLineCycleCount                 | Средняя несоответствие является абсолютным количеством расхождения, деленному на ожидаемое количество, где абсолютное значение несоответствия превышает 0 (ноль). Средняя количество несоответствия является средним абсолютным количеством расхождения, где абсолютное значение несоответствия превышает 0 (ноль). Количество с несоответствием, общее количество, ожидаемое количество и количество при инвентаризации, где общее количество сгруппировано по номенклатурам и местоположению (см. описания выше в этой таблице). |
| Точность местоположения запасов | Инвентаризация номенклатуру по работникам                     | WHSWorkLineCycleCount                 | Количество без несоответствия и количество с несоответствием (см. описания выше в этой таблице). |
| Точность местоположения запасов | Инвентаризация номенклатуры по площадкам/складам           | WHSWorkLineCycleCount                 | Количество без несоответствия и количество с несоответствием (см. описания выше в этой таблице). |
| Точность местоположения запасов | Коэффициент расхождения по продуктам              | WHSWorkLineCycleCount                 | Коэффициент несоответствия (см. описание выше в этой таблице). |
| Производительность отгрузки        | Отгруженные строки                            | SalesLine               | Число строк продаж, где строки продаж отгружены. |
| Производительность отгрузки        | С опережением                                    | CustPackingSlipOnTimeStatus           | Строки продаж, где статус даты отгрузки равен **1 (ранняя)**. Ранняя означает, что дата отгрузки по отборочной накладной раньше подтвержденной дата отгрузки для строки продажи. Если подтвержденная дата отгрузки не задана, используйте запрошенную дату отгрузки. |
| Производительность отгрузки        | Вовремя                                  | CustPackingSlipOnTimeStatus           | Строки продаж, где статус даты отгрузки равен **2 (вовремя)**. Вовремя означает, что дата отгрузки по отборочной накладной совпадает с подтвержденной датой отгрузки для строки продажи. Если подтвержденная дата отгрузки не задана, используйте запрошенную дату отгрузки. |
| Производительность отгрузки        | С опозданием                                     | CustPackingSlipOnTimeStatus           | Строки продаж, где статус даты отгрузки равен **3 (поздняя)**. Поздняя означает, что дата отгрузки по отборочной накладной позже подтвержденной дата отгрузки для строки продажи. Если подтвержденная дата отгрузки не задана, используйте запрошенную дату отгрузки. |
| Производительность отгрузки        | Отгрузки по времени                      | SalesLine CustPackingSlipOnTimeStatus | Полностью отгруженные заказы, в которых отгружено полное количество строки продажи, а также статус отгрузки: ранняя, своевременная или поздняя (см. описания выше в этой таблице). |
| Производительность отгрузки        | Отгружены с задержкой по городам                     | CustPackingSlipOnTimeStatus           | С опозданием (см. описания выше в этой таблице). |
| Производительность отгрузки        | Отгружено по продуктам                       | CustPackingSlipOnTimeStatus           | С опережением, вовремя и с опозданием (см. описания выше в этой таблице). |
| Производительность отгрузки        | Отгружено по клиентам                      | CustPackingSlipOnTimeStatus           | С опережением, вовремя и с опозданием (см. описания выше в этой таблице). |
| Производительность отгрузки        | Отгружено по сайтам/складам              | CustPackingSlipOnTimeStatus           | С опережением, вовремя и с опозданием (см. описания выше в этой таблице). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
