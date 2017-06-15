---
title: "Содержимое Power BI &quot;Менеджер по методикам&quot;"
description: "В этом разделе описывается, что входит в содержимое Power BI &quot;Менеджер по методикам&quot;. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые используются для построения пакета содержимого."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Содержимое Power BI "Менеджер по методикам"

[!include[banner](../includes/banner.md)]


В этом разделе описывается, что входит в содержимое Microsoft Power BI **Менеджер по методикам**. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

## <a name="overview"></a>Обзор

Содержимое Power BI **Менеджер по методикам** создано для менеджеров по методикам и менеджеров проектов. Оно предоставляет ключевые показатели, связанные с проектами, над которыми работает организация. Панель мониторинга содержит общие сведения о проектах и связанных с ними клиентах. Фильтр уровня отчета можно использовать для получения отчета для конкретных юридических лиц. Это содержимое Power BI извлекает данные из сводных измерений учета проекта для Microsoft Dynamics 365 for Operations.

Содержимое Power BI **Менеджер по методикам** содержит пять страниц отчетов: одна сводная страница и четыре страницы, которые предоставляют подробные сведения о затратах по проекту, доходах, управлением вырученной стоимостью и почасовым показателям, которые разбиты по различным аналитикам.

Все суммы в содержимом отображаются в системной валюте. Системную валюту можно задать на странице **Системные параметры**.

## <a name="accessing-the-power-bi-content"></a>Доступ к содержимому Power BI

Содержимое Power BI **Менеджер по методикам** можно найти в библиотеке общих ресурсов в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения о том, как загрузить пакет содержимого и подключить его к данным Dynamics 365 for Operations, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).

Чтобы просмотреть демонстрацию, которая показывает, как реализовать содержимое Power BI, см. [Содержимое Power BI от Майкрософт и ваших партнеров в службах Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office mix).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Отчеты, которые включены в содержимое Power BI

В следующей таблице приводятся подробные сведения о показателях, которые находятся на каждой странице отчета, в содержимом Power BI **Менеджер по методикам**.

| Страница отчета                                          | Показатели               |
|------------------------------------------------------|-----------------------------------------------|
| Панель мониторинга  | Созданные проекты<br>Оцененные проекты<br>Выполняющиеся проекты<br>Число проектов по этапам<br>Число проектов по городам<br>Фактическая выручка по клиентам<br>Бюджетная валовая прибыль по проектам<br>Обзор управления вырученной стоимостью |
| Затраты                                                 | Фактические и бюджетные затраты по месяцам<br>Фактические и бюджетные затраты по годам<br>Фактические и бюджетные затраты по категориям<br>Фактические затраты по типам проводки       |
| Реализация                                              | Фактическая выручка по месяцам<br>Фактическая выручка по почтовому индексу<br>Фактическая и бюджетная выручка по категориям<br>Фактическая выручка по отрасли клиента        |
| EVM                                                  | Затраты и индекс выполнения графика по проектам                 |
| Часы                                                | Фактические оплачиваемые использованные часы, фактические оплачиваемые часы по накладным расходам и бюджетные часы<br>Фактические оплачиваемые использованные часы и фактические оплачиваемые часы по накладным расходам по проектам<br>Фактические оплачиваемые использованные часы и фактические оплачиваемые часы по накладным расходам по ресурсам<br>Отношение фактически оплачиваемых часов по проектам<br>Отношение фактически оплачиваемых часов по ресурсам |

Диаграммы и плитки во всех этих отчетах можно отфильтровать и закрепить на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Можно также использовать функцию экспорта базовых данных для экспорта базовых данных, сводка которых отображается в визуализации.

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов

Данные Dynamics 365 for Operations используются для заполнения страниц отчета в содержимом Power BI **Менеджер по методикам**. Эти данные представлены как агрегированные измерения, которые помещаются на временное хранение в хранилище объектов, которая представляет собой базу данных Microsoft SQL, оптимизированную для аналитики. Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md).

В следующих разделах рассматриваются сводные измерения, которые используются в каждом объекте.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Объект: ProjectAccountingCube_ActualHourUtilization
**Источник данных**: ProjEmplTrans

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Общее количество фактически оплачиваемых использованных часов |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Общий коэффициент фактических накладных расходов             |

### <a name="entity-projectaccountingcubeactuals"></a>Объект: ProjectAccountingCube_Actuals
**Источник данных**: ProjTransPosting

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Общая сумма разнесенной выручки для всех проводок |   
| ActualCost   |                             Sum(ActualCost)           |    Общая сумма разнесенных затрат для всех типов проводок    |

### <a name="entity-projectaccountingcubecustomer"></a>Объект: ProjectAccountingCube_Customer
**Источник данных**: CustTable

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Число проектов        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Число доступных проектов    |


### <a name="entity-projectaccountingcubeforecasts"></a>Объект: ProjectAccountingCube_Forecasts
**Источник данных**: ProjTransBudget

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Общая сумма прогнозируемых затрат для всех типов проводок     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Общая сумма прогнозируемой начисленной выручки/выручки по выставленным накладным         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Разница между суммой общей прогнозируемой выручки и суммой общих прогнозируемых затрат

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Объект: ProjectAccountingCube_ProjectPlanCostsView
**Источник данных**: Project

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Общая себестоимость в оценках для всех типов проводок проекта с запланированными задачами |

### <a name="entity-projectaccountingcubeprojects"></a>Объект: ProjectAccountingCube_Projects
**Источник данных**: Project

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Индекс показателей затрат  |ProjectAccountingCube_Projects[Вырученная стоимость] / ProjectAccountingCube_Projects[Общие фактические затраты на выполненные задачи] |     Расчет общей вырученной стоимости, деленной на общие фактические затраты|
|  Индекс выполнения графика |ProjectAccountingCube_Projects[Вырученная стоимость] / ProjectAccountingCube_Projects[Общие плановые затраты на выполненные задачи]|Расчет общей вырученной стоимости, деленной на общие плановые затраты |
|Процент завершения работы |Процент завершения работы = ProjectAccountingCube_Projects[Общие фактические затраты на выполненные задачи] / (ProjectAccountingCube_Projects[Общие фактические затраты на выполненные задачи] + ProjectAccountingCube_Projects[Общие плановые затраты на проект] - ProjectAccountingCube_Projects[Общие плановые затраты на выполненные задачи])|Общий процент выполненной работы на основе общих фактических затрат на выполненные задачи и запланированных затрат для проекта|
|Отношение фактически оплачиваемых часов по проекту|ProjectAccountingCube_Projects[Общие фактические оплачиваемые использованные часы по проекту] / (ProjectAccountingCube_Projects[Общие фактические оплачиваемые использованные часы по проекту] + ProjectAccountingCube_Projects[Общие фактические оплачиваемые часы по накладным расходам по проекту])|Общее количество фактических оплачиваемых часов на основе использованных часов + часов по накладным расходам|
|Вырученная стоимость|ProjectAccountingCube_Projects[Общие плановые затраты на проект] * ProjectAccountingCube_Projects[Процент выполненных работ]|Общие плановые затраты, умноженные на процент выполненных работ|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Объект: ProjectAccountingCube_TotalEstimatedCosts 
**Источник данных**: ProjTable

| Ключевое агрегированное измерение                | Поле                                | описание                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Общая себестоимость в оценках для всех типов проводок проекта с выполненными задачами|

## <a name="additional-resources"></a>Дополнительные ресурсы

Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

- [Информационные объекты](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Настройка интеграции с Power BI для рабочих областей](configure-power-bi-integration.md)
