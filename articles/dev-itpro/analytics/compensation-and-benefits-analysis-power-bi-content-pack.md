---
title: "Содержимое компенсации и льгот Power BI"
description: "В этом разделе рассматривается содержимое Finance and Operations — компенсации и льготы Power BI. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbffad24350ae4650cd0d4142799c5e641dcdbe3
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>Содержимое компенсации и льгот Power BI

[!include[banner](../includes/banner.md)]


В этом разделе рассматривается содержимое Finance and Operations — компенсации и льготы Power BI. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

<a name="accessing-the-content-pack"></a>Доступ к пакету содержимого
--------------------------

Пакет содержимого компенсаций и льгот можно найти в библиотеке общих ресурсов в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения о том, как загрузить пакет содержимого и подключить его к данным Microsoft Dynamics 365 for Finance and Operations, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным Finance and Operations данные организации будут отображаться в отчетах. Если вы никогда не использовали Microsoft Power BI до этого, см. дополнительные сведения на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет                     | Содержание                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Анализ компенсаций и льгот | Почасовые и постоянные сотрудники по компаниям, средняя почасовая оплата, средняя зарплата, сотрудники по типу занятости и о приеме на работу и регистрация плана |
| Льготы сотрудников          | Регистрация сотрудников по выбранным льготам                                                                                               |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Finance and Operations используются для заполнения отчетов в пакете содержимого компенсаций и льгот. В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                            | Содержание                                                                                                   | Связи с другими объектами                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Календарь корреспондирует с отчетами по секторам                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Workforce\_Company                | Компании, по которым требуется фильтровать отчеты                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_Compensation           | Ставка и частота оплаты в зависимости от времени                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_CurrentCompensation    | Ставка оплаты и частота на текущую дату                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Должности по состоянию на текущую дату, эквивалент полной занятости (FTE), открытые вакансии и свободные должности | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Workforce\_CurrentWorker          | Сотрудники по состоянию на текущую дату, возраст и численность сотрудников                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Workforce\_Date                   | Дни, недели, месяцы и годы                                                                             | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Workforce\_Demographics           | Дата рождения, пол, этническое происхождение и семейное положение                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Employment             | Дата начала, дата окончания и дата перехода                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_GeographicLocation     | Город, район, почтовый индекс и область или край                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Job                    | Функция, тип и должность                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PastPositionAssignment | Причина назначения, дата начала, дата окончания и должность                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | Оценка, описание и модель оценки                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Position               | Отдел, полная занятость, должность, тип должности и название должности                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | Список занимаемых должностей по времени, полная занятость и должность                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | Имя, фамилия и ФИО                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | Навык, типа навыка и рейтинг                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_TerminatedWorker       | Уволенные сотрудники, дата увольнения, название должности, должность и работа                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Дата вступления в силу, параметр льготы, план льгот и тип льготы                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | Имя, фамилия и ФИО                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerTitle            | Должность и дата трудового стажа                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Сотрудники по времени, численность сотрудников, компания и должность                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

Эти объекты были использованы для создания вычисляемых мер в модели данных. Эти вычисляемые меры затем использовались для расчета ключевых показателей производительности (KPI) и отчетов, используемых в пакете содержимого. Если требуется включить дополнительные вычисления в отчеты и на панели мониторинга, можно загрузить и изменить файл CompensationandBenefits.pbix из LCS. Этот файл является моделью данных по умолчанию, которая использовалась для создания пакета содержимого. После внесения изменений можно создать организационный пакет содержимого панель мониторинга, содержащие добавленные сведения.

## <a name="additional-resources"></a>Дополнительные ресурсы
Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

-   [Информационные объекты](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Добавление плиток Power BI в рабочие области](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





