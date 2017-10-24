---
title: "Содержимое Power BI \"Организационное обучение\""
description: "В этом разделе рассматривается содержимое Finance and Operations — организационное обучение Power BI. В нем описывается порядок доступа к пакету содержимого и модель данных и объекты, которые использовались для построения пакета содержимого."
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
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e49d9af8b8bd8d5edb977c49742861199c6964fd
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="organizational-training-power-bi-content"></a>Содержимое Power BI "Организационное обучение"

[!include[banner](../includes/banner.md)]


В этом разделе рассматривается содержимое Finance and Operations — организационное обучение Power BI. В нем описывается порядок доступа к пакету содержимого и модель данных и объекты, которые использовались для построения пакета содержимого.

<a name="accessing-the-content-pack"></a>Доступ к пакету содержимого
--------------------------

Пакет содержимого организационного обучения можно найти в библиотеке общих ресурсов в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения о том, как загрузить пакет содержимого и подключить его к данным Microsoft Dynamics 365 for Finance and Operations, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным Finance and Operations данные организации будут отображаться в отчетах. Если вы никогда не использовали Microsoft Power BI до этого, см. дополнительные сведения на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет          | Содержание                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Анализ курса | Регистрация по местонахождению, участники курса по статусам, а также список регистрации |
| Типы курсов    | Типы курсов по навыку                                                       |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Finance and Operations используются для заполнения отчетов в пакете содержимого организационного обучения. В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                    | Содержание                                                         | Связи с другими объектами                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Календарь корреспондирует с отчетами по секторам                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Компании, по которым требуется фильтровать отчеты                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Курс, описание, имя лектора, расположение, комната и статус | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Программа, курс и время начала и окончания                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Имя, статус, должность и дата регистрации                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Навык, типа навыка и уровень                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Дни, недели, месяцы и годы                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Дата рождения, пол, этническое происхождение и семейное положение         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Дата начала, дата окончания и дата перехода                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Функция, тип и должность                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Должность, название и эквивалент полной занятости (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Имя, фамилия и ФИО                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Должность и дата трудового стажа                                         | Training\_CourseAttendees                                                                                                                                                                          |

Эти объекты были использованы для создания вычисляемых мер в модели данных. Эти вычисляемые меры затем использовались для расчета ключевых показателей производительности (KPI) и отчетов, используемых в пакете содержимого. Если требуется включить дополнительные вычисления в отчеты и на панели мониторинга, можно загрузить и изменить файл Training.pbix из LCS. Этот файл является моделью данных по умолчанию, которая использовалась для создания пакета содержимого. После внесения изменений можно создать организационный пакет содержимого панель мониторинга, содержащие добавленные сведения.

## <a name="additional-resources"></a>Дополнительные ресурсы
Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

-   [Информационные объекты](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Добавление плиток Power BI в рабочие области](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





