---
title: "Содержимое Power BI \"Компетенции и развитие сотрудников\""
description: "В этом разделе рассматривается содержимое Finance and Operations — Компетенции и развитие сотрудников (Power BI). В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b2b3d96a64a552d1f0e0144dcbd809964fdf63c4
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="employee-competencies-and-development-power-bi-content"></a>Содержимое Power BI "Компетенции и развитие сотрудников"

[!include[banner](../includes/banner.md)]


В этом разделе рассматривается содержимое Finance and Operations — Компетенции и развитие сотрудников (Power BI). В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

<a name="accessing-the-content-pack"></a>Доступ к пакету содержимого
--------------------------

Пакет содержимого "Компетенции и развитие сотрудников" можно найти в библиотеке общих ресурсов в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения о том, как загрузить пакет содержимого и подключить его к данным Microsoft Dynamics 365 for Finance and Operations, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным Finance and Operations данные организации будут отображаться в отчетах. Если вы никогда не использовали Microsoft Power BI до этого, см. дополнительные сведения на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет                            | Содержание                                               |
|-----------------------------------|--------------------------------------------------------|
| Анализ компетенции и развития | Типы навыков членов группы и навыки членов группы по типу |
| Профиль навыков                     | Профиль навыков для выбранного сотрудника                |
| Анализ навыков                    | Навыки по типам и рейтингу                              |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Finance and Operations используются для заполнения отчетов в пакете содержимого "Компетенции и развитие сотрудников". В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                            | Содержание                                                                                                   | Связи с другими объектами                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Календарь корреспондирует с отчетами по секторам                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | Компании, по которым требуется фильтровать отчеты                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | Ставка и частота оплаты в зависимости от времени                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | Ставка оплаты и частота на текущую дату                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Должности по состоянию на текущую дату, эквивалент полной занятости (FTE), открытые вакансии и свободные должности | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Сотрудники по состоянию на текущую дату, возраст и численность сотрудников                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | Дни, недели, месяцы и годы                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | Дата рождения, пол, этническое происхождение и семейное положение                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | Дата начала, дата окончания и дата перехода                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | Город, район, почтовый индекс и область или край                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | Функция, тип и должность                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Важность, рейтинг, навык и уровень навыков                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | Причина назначения, дата начала, дата окончания и должность                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | Оценка, описание и модель оценки                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | Уровень, дата уровня и навык                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | Сертифицированный, уровень, дата уровня и навык                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Отдел, полная занятость, должность, тип должности и название должности                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Список занимаемых должностей по времени, полная занятость и должность                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Имя, фамилия и ФИО                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | Навык, типа навыка и рейтинг                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | Уволенные сотрудники, дата увольнения, название должности, должность и работа                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | Имя, фамилия и ФИО                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | Должность и дата трудового стажа                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Сотрудники по времени, численность сотрудников, компания и должность                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Эти объекты были использованы для создания вычисляемых мер в модели данных. Эти вычисляемые меры затем использовались для расчета ключевых показателей производительности (KPI) и отчетов, используемых в пакете содержимого. Если требуется включить дополнительные вычисления в отчеты и на панели мониторинга, можно загрузить и изменить файл CompetenciesandDevelopment.pbix из LCS. Этот файл является моделью данных по умолчанию, которая использовалась для создания пакета содержимого. После внесения изменений можно создать организационный пакет содержимого панель мониторинга, содержащие добавленные сведения.

## <a name="additional-resources"></a>Дополнительные ресурсы
Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

-   [Информационные объекты](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Добавление плиток Power BI в рабочие области](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





