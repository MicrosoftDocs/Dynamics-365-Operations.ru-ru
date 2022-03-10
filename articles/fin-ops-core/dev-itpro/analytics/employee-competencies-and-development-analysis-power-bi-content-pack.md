---
title: Содержимое Power BI "Компетенции и развитие сотрудников"
description: В этом разделе описывается содержимое Power BI "Компетенции и развитие сотрудников".
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 572f6bcfa202995d90080e1a31476122f7ec23d71214d5ff0dd44ed919859c57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726317"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Содержимое Power BI "Компетенции и развитие сотрудников"

[!include [banner](../includes/banner.md)]

В этом разделе описывается содержимое Power BI "Компетенции и развитие сотрудников". 

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным в отчетах будут отображаться данные вашей организации. Если вы до сих пор не использовали Microsoft Power BI, больше узнать о нем можно на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет                            | Содержание                                               |
|-----------------------------------|--------------------------------------------------------|
| Анализ компетенции и развития | Типы навыков членов группы и навыки членов группы по типу |
| Профиль навыков                     | Профиль навыков для выбранного сотрудника                |
| Анализ навыков                    | Навыки по типам и рейтингу                              |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные приложения используются для заполнения отчетов в пакете содержимого компетенции и развития сотрудников. В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                            | Содержание                                                                                                   | Связи с другими объектами |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Календарь корреспондирует с отчетами по секторам                                                                          | |
| Workforce\_Company                | Компании, по которым требуется фильтровать отчеты                                                                             | |
| Workforce\_Compensation           | Ставка и частота оплаты в зависимости от времени                                                                           | |
| Workforce\_CurrentCompensation    | Ставка оплаты и частота на текущую дату                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Должности по состоянию на текущую дату, эквивалент полной занятости (FTE), открытые позиции и свободные должности | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Сотрудники по состоянию на текущую дату, возраст и численность сотрудников                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Дни, недели, месяцы и годы                                                                             | |
| Workforce\_Demographics           | Дата рождения, пол, этническое происхождение и семейное положение                                                   | |
| Workforce\_Employment             | Дата начала, дата окончания и дата перехода                                                                  | |
| Workforce\_GeographicLocation     | Город, район, почтовый индекс и область или край                                                           | |
| Workforce\_Job                    | Функция, тип и должность                                                                                  | |
| Workforce\_JobPreferredSkill      | Важность, рейтинг, навык и уровень навыков                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Причина назначения, дата начала, дата окончания и должность                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Оценка, описание и модель оценки                                                                      | |
| Workforce\_PersonSkill            | Уровень, дата уровня и навык                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Сертифицированный, уровень, дата уровня и навык                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Отдел, полная занятость, должность, тип должности и название должности                                                        | |
| Workforce\_PositionTrend          | Список занимаемых должностей по времени, полная занятость и должность                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Имя, фамилия и ФИО                                                                       | |
| Workforce\_Skill                  | Навык, типа навыка и рейтинг                                                                              | |
| Workforce\_TerminatedWorker       | Уволенные сотрудники, дата увольнения, название должности, должность и работа                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Имя, фамилия и ФИО                                                                       | |
| Workforce\_WorkerTitle            | Должность и дата трудового стажа                                                                                   | |
| Workorce\_WorkerTrend             | Сотрудники по времени, численность сотрудников, компания и должность                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]