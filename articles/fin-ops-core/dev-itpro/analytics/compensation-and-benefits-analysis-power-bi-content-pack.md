---
title: Содержимое Power BI "Компенсации и льготы"
description: В этом разделе описывается содержимое Power BI "Компенсации и льготы".
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 69149f55371f64b4907f6040e9de03843fc11717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687214"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Содержимое Power BI "Компенсации и льготы"

[!include [banner](../includes/banner.md)]

В этом разделе описывается содержимое Power BI "Компенсации и льготы". 

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным в отчетах будут отображаться данные вашей организации. Если вы до сих пор не использовали Microsoft Power BI, больше узнать о нем можно на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет                     | Содержание                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Анализ компенсаций и льгот | Почасовые и постоянные сотрудники по компаниям, средняя почасовая оплата, средняя зарплата, сотрудники по типу занятости и о приеме на работу и регистрация плана |
| Льготы сотрудников          | Регистрация сотрудников по выбранным льготам                                                                                               |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные приложения используются для заполнения отчетов в пакете содержимого компенсаций и льгот. В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                            | Содержание                                                                                                   | Связи с другими объектами |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Календарь корреспондирует с отчетами по секторам                                                                          | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker |
| Workforce\_Company                | Компании, по которым требуется фильтровать отчеты                                                                             | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Compensation           | Ставка и частота оплаты в зависимости от времени                                                                           | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_CurrentCompensation    | Ставка оплаты и частота на текущую дату                                                              | Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Должности по состоянию на текущую дату, эквивалент полной занятости (FTE), открытые позиции и свободные должности | Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentWorker          | Сотрудники по состоянию на текущую дату, возраст и численность сотрудников                                                         | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_Date                   | Дни, недели, месяцы и годы                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | Дата рождения, пол, этническое происхождение и семейное положение                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Employment             | Дата начала, дата окончания и дата перехода                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_GeographicLocation     | Город, район, почтовый индекс и область или край                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Job                    | Функция, тип и должность                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | Причина назначения, дата начала, дата окончания и должность                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Оценка, описание и модель оценки                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Position               | Отдел, полная занятость, должность, тип должности и название должности                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Список занимаемых должностей по времени, полная занятость и должность                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Имя, фамилия и ФИО                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Skill                  | Навык, типа навыка и рейтинг                                                                              | |
| Workforce\_TerminatedWorker       | Уволенные сотрудники, дата увольнения, название должности, должность и работа                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Дата вступления в силу, параметр льготы, план льгот и тип льготы                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerName             | Имя, фамилия и ФИО                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTitle            | Должность и дата трудового стажа                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTrend            | Сотрудники по времени, численность сотрудников, компания и должность                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |
