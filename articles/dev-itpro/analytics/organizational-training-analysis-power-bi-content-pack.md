---
title: Содержимое Power BI "Организационное обучение"
description: В этом разделе рассматривается содержимое Power BI "Finance and Operations — организационное обучение".
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c1855013dc449950877f8727a5453942aeb75de
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545084"
---
# <a name="organizational-training-power-bi-content"></a>Содержимое Power BI "Организационное обучение"

[!include [banner](../includes/banner.md)]

В этом разделе рассматривается содержимое Power BI "Finance and Operations — организационное обучение".

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным Finance and Operations в отчетах будут отображаться данные вашей организации. Если вы до сих пор не использовали Microsoft Power BI, больше узнать о нем можно на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет          | Содержание                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Анализ курса | Регистрация по местонахождению, участники курса по статусам, а также список регистрации |
| Типы курсов    | Типы курсов по навыку                                                       |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Finance and Operations используются для заполнения отчетов в пакете содержимого организационного обучения. В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                    | Содержание                                                         | Связи с другими объектами |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Календарь корреспондирует с отчетами по секторам                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Company         | Компании, по которым требуется фильтровать отчеты                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Course          | Курс, описание, имя лектора, расположение, комната и статус | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Training\_CourseAgenda    | Программа, курс и время начала и окончания                          | Training\_Company, Training\_CalendarOffset, Training\_Date Training\_Course |
| Training\_CourseAttendees | Имя, статус, должность и дата регистрации                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Training\_CourseSkill     | Навык, типа навыка и уровень                                     | Training\_Course |
| Training\_Date            | Дни, недели, месяцы и годы                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Demographics    | Дата рождения, пол, этническое происхождение и семейное положение         | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Employment      | Дата начала, дата окончания и дата перехода                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Job             | Функция, тип и должность                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Position        | Должность, название и эквивалент полной занятости (FTE)                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_WorkerName      | Имя, фамилия и ФИО                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Должность и дата трудового стажа                                         | Training\_CourseAttendees |
