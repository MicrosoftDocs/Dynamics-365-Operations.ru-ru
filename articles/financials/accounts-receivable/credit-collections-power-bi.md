---
title: "Содержимое Power BI \"Кредит и сборы\""
description: "В этой теме описывается, что входит в содержимое Power BI для кредита и сборов. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6ce0b7b35264c05555d8b3a18e70484202a289d6
ms.openlocfilehash: 3832cabb11d67eda7afd7f3d5322c005b36dc1f5
ms.contentlocale: ru-ru
ms.lasthandoff: 03/07/2018

---

# <a name="credit-and-collections-management-power-bi-content"></a>Содержимое Power BI "Кредит и сборы"

[!INCLUDE [banner](../includes/banner.md)]

В этой теме описывается, что входит в содержимое Microsoft Power BI **Управление кредитом и сбором задолженностей**. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

## <a name="overview"></a>Обзор

Содержимое Power BI **Управление кредитом и сбором задолженностей** было создано для менеджеров кредитов и сборов и клерков сборов. Оно обеспечивает ключевые показатели по кредитам и сборам, например по периоду погашения дебиторской задолженности (в днях), просроченному сальдо, использованию кредита, клиентов с превышенным кредитным лимитом. Оно использует данные проводок и предоставляет сводное представление о кредитах и сборах для всех компаний. Оно также предоставляет разбивку по компании, группе клиентов и клиенту.

Это содержимое Power BI состоит из 10 страниц отчета:

- Два страницы обзора (одна для обзора кредитов, другая для обзора сборов)
- Восемь страниц сведений о показателях кредитов и сборов, которые разбиты по различным аналитикам.

Все суммы показаны в валюте системы. Системную валюту можно задать на странице **Системные параметры**.

По умолчанию показаны данные кредитов и сборов для текущей компании. Чтобы просмотреть данные для всех компаний, назначьте полномочие **CustCollectionsBICrossCompany** для роли.

## <a name="accessing-the-power-bi-content"></a>Доступ к содержимому Power BI
Содержимое Power BI **Управление кредитом и сбором задолженностей** отображается в рабочей области **Кредит и сбор задолженностей клиента**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Отчеты, которые включены в содержимое Power BI

Содержимое Power BI **CustCollectionsBICrossCompany** включает отчет, состоящий из набора показателей. Эти показатели отображаются в виде диаграмм, плиток и таблиц. В следующей таблице приводится обзор визуализации в содержимом Power BI **CustCollectionsBICrossCompany**.

| Страница отчета                 | Визуализация |
|-----------------------------|---------------|
| Обзор сборов        | <ul><li>Необработанные клиенты</li><li>Клиенты с превышением кредитного лимита</li><li>DSO 30 дней</li><li>Открытые обращения</li><li>Среднее количество дней до закрытия обращения</li><li>Открытые мероприятия</li><li>Среднее количество дней до закрытия мероприятий</li><li>Открытые процент-ноты</li><li>Открытые письма-напоминания</li><li>Удержание клиента</li><li>Удержание продаж</li><li>Сальдо по срокам</li><li>Суммы статусов сбора задолженностей</li><li>Суммы кодов сбора задолженностей</li><li>Причина списания</li><li>Дебетовое сальдо по регионам</li><li>Ожидаемые платежи</li></ul> |
| Обзор кредитов             | <ul><li>Необработанные клиенты</li><li>Кредитный лимит в сравнении с дебетовым сальдо</li><li>Сетка клиентов с превышением кредитного лимита</li><li>Клиенты с превышением кредитного лимита по компаниям</li><li>Выбранный кредит в сравнении с общим кредитным лимитом</li><li>Кредитный лимит в сравнении с выбранным кредитом по регионам</li><li>Клиенты по кредитному рейтингу</li></ul> |
| Кредитный лимит                | <ul><li>Кредитный лимит</li><li>Сведения о кредитном лимите</li><li>Кредитный лимит по клиентам</li><li>Кредитный лимит по группам клиентов</li><li>Кредитный лимит по кредитному рейтингу по компаниям</li><li>Доля выбранного кредитного лимита по регионам</li></ul> |
| Клиенты с превышением кредитного лимита | <ul><li>Клиенты с превышением кредитного лимита</li><li>Сведения о клиентах с превышением кредитного лимита</li><li>Клиенты с превышением кредитного лимита по компаниям</li><li>Клиент с превышением кредитного лимита по группам клиентов</li><li>Клиенты с превышением кредитного лимита по регионам</li></ul> |
| Необработанные клиенты          | <ul><li>Необработанные клиенты</li><li>Сведения о клиентах с просрочками</li><li>Клиенты с просрочками по компаниям</li><li>Клиенты с просрочками по группам клиентов</li><li>Клиенты с просрочками по регионам</li></ul> |
| Сальдо по срокам               | <ul><li>Сальдо по срокам</li><li>Сведения о сальдо по срокам</li><li>Сальдо по срокам и по компаниям</li><li>Сальдо по срокам и по группам клиентов</li></ul> |
| Ожидаемые платежи           | <ul><li>Ожидаемые платежи</li><li>Сведения об ожидаемых платежах</li><li>Ожидаемые платежи по компаниям</li><li>Ожидаемые платежи по группам клиентов</li><li>Ожидаемые платежи по регионам</li></ul> |
| Списания                  | <ul><li>Списания по регионам</li><li>Сведения о списаниях</li><li>Списания по счету ГК</li><li>Списания по компаниям</li><li>Списания по группам клиентов</li><li>Списания по регионам</li></ul> |
| Статус инкассо          | <ul><li>Оспаривается</li><li>Обещание оплатить нарушено</li><li>Обещана оплата</li><li>Сведения о статусе сборов</li><li>Суммы статусов сбора задолженностей</li><li>Открытые обращения</li><li>Открытые мероприятия</li></ul> |
| Письма-напоминания         | <ul><li>Суммы кодов сбора задолженностей</li><li>Сведения о суммах кодов сбора задолженностей</li><li>Сумма писем-напоминаний по компаниям</li><li>Сумма писем-напоминаний по группам клиентов</li><li>Сумма писем-напоминаний по регионам</li></ul> |

Диаграммы и плитки во всех этих отчетах можно отфильтровать и закрепить на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Можно также использовать функцию экспорта базовых данных для экспорта базовых данных, сводка которых отображается в визуализации.

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов

Следующие данные используются для заполнения страниц отчета в содержимом **Управление кредитом и сбором задолженностей** Power BI. Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов. Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики. Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](../../dev-itpro/analytics/power-bi-integration-entity-store.md).


|                   Объект                    |      Ключевые сводные измерения      |             Иcточник данных              |                           Поле                            |                                    описание                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  |            smmActivities             | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) |     Число закрытых мероприятий и среднее время для закрытия этих мероприятий.     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           Число открытых мероприятий.                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             Сумма сальдо по срокам.                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           Просроченные суммы.                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases, CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        Число закрытых обращений и среднее время для закрытия этих обращений.        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              Число открытых обращений.                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       Число открытых писем-напоминаний.                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     Сальдо разнесенных писем-напоминаний.                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                Сальдо проводок со статусом сбора.                 |
|           CustCollectionsBICredit           | CreditExposed, AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed), Sum(AmountOverCreditLimit)       | Сумма используемого кредита и суммы превышения кредитного лимита клиентами. |
|         CustCollectionsBICustOnHold         |               Блокировано                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     Число клиентов, которые заблокированы.                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        Период погашения дебиторской задолженности 30 дней.                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 Сумма платежей, ожидаемых в течение следующего года.                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                Число созданных процент-нот.                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 Число общих заказов на продажу, которые заблокированы.                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                Сумма проводок, которые были списаны.                 |


