---
title: "Содержимое Power BI \"Кредит и сборы\""
description: "В этой теме описывается, что входит в содержимое Power BI для кредита и сборов. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c066e1a190a5536ad67368b4e059ab6bc66718e6
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Содержимое Power BI "Кредит и сборы"

В этой теме описывается, что входит в содержимое Microsoft Power BI **Управление кредитом и сбором задолженностей**. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

## <a name="overview"></a>Обзор

Содержимое Power BI **Управление кредитом и сбором задолженностей** было создано для менеджеров кредитов и сборов и клерков сборов. Оно обеспечивает ключевые показатели по кредитам и сборам, например по периоду погашения дебиторской задолженности (в днях), просроченному сальдо, использованию кредита, клиентов с превышенным кредитным лимитом. Оно использует данные проводок и предоставляет сводное представление о кредитах и сборах для всех компаний. Оно также предоставляет разбивку по компании, группе клиентов и клиенту.

Это содержимое Power BI состоит из 10 страниц отчета:

- Два страницы обзора (одна для обзора кредитов, другая для обзора сборов)
- Восемь страниц сведений о показателях кредитов и сборов, которые разбиты по различным аналитикам.

Все суммы показаны в валюте системы. Системную валюту можно задать на странице **Системные параметры**.

По умолчанию показаны данные кредитов и сборов для текущей компании. Чтобы просмотреть данные для всех компаний, назначьте полномочие **CustCollectionsBICrossCompany** для роли.

## <a name="accessing-the-power-bi-content"></a>Доступ к содержимому Power BI
При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, обновление от июля 2017 г. содержимое Power BI **Управление кредитом и сбором задолженностей** отображается в рабочей области **Кредит и сбор задолженностей клиента**.

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

## <a name="extending-the-power-bi-content"></a>Расширение содержимого Power BI
С помощью пакетов содержимого, доступных в Microsoft Dynamics Lifecycle Services (LCS), можно повысить эффективность аналитики для тех, кто не использует Finance and Operations. Эти пакеты содержимого можно изменить, чтобы они включали других отчеты или визуальные элементы, и затем опубликовать пакеты содержимого для владельца Power BI.com для анализа.

Содержимое **Управление кредитом и сбором задолженностей** Power BI можно найти в библиотеке общих ресурсов LCS. Дополнительные сведения о том, как загрузить содержимое и реализовать его в вашей организации, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Чтобы просмотреть демонстрацию, которая показывает, как реализовать содержимое Power BI, см. [Содержимое Power BI от Майкрософт и ваших партнеров в службах Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office mix).

Обязательно загрузите содержимое Power BI **Управление кредитом и сбором задолженностей**, которое применяется к версии Microsoft Dynamics 365 for Finance and Operations, которую вы используете.

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов

Следующие данные используются для заполнения страниц отчета в содержимом **Управление кредитом и сбором задолженностей** Power BI. Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов. Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики. Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-integration-entity-store).

| Объект                                      | Ключевые сводные измерения           | Иcточник данных                                 | Поле                                                      | описание |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Число закрытых мероприятий и среднее время для закрытия этих мероприятий. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Число открытых мероприятий. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Сумма сальдо по срокам. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Просроченные суммы. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Число закрытых обращений и среднее время для закрытия этих обращений. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Число открытых обращений. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Число открытых писем-напоминаний. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Сальдо разнесенных писем-напоминаний. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Сальдо проводок со статусом сбора. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Сумма используемого кредита и суммы превышения кредитного лимита клиентами. |
| CustCollectionsBICustOnHold                 | Блокировано                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Число клиентов, которые заблокированы. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Период погашения дебиторской задолженности 30 дней. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Сумма платежей, ожидаемых в течение следующего года. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Число созданных процент-нот. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Число общих заказов на продажу, которые заблокированы. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Сумма проводок, которые были списаны. |

