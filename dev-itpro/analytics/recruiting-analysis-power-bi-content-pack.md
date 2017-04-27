---
title: "Содержимое Power BI по набору сотрудников"
description: "В этом разделе рассматривается содержимое Power BI Dynamics 365 for Operations - Recruiting. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Содержимое Power BI по набору сотрудников

[!include[banner](../includes/banner.md)]


В этом разделе рассматривается содержимое Power BI Dynamics 365 for Operations - Recruiting. В нем описывается порядок доступа к отчетам, входящим в пакет содержимого, и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

<a name="accessing-the-content-pack"></a>Доступ к пакету содержимого
--------------------------

Пакет содержимого "Набор сотрудников" можно найти в библиотеке общих ресурсов в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения о том, как загрузить пакет содержимого и подключить его к данным Microsoft Dynamics 365 for Operations, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Отчеты, включенные в пакет содержимого
После подключения пакета содержимого к данным Dynamics 365 for Operations данные организации будут отображаться в отчетах. Если вы никогда не использовали Microsoft Power BI до этого, см. дополнительные сведения на [странице интерактивного обучения по Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Отчеты, включенные в пакет содержимого, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет                       | Содержание                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Анализ кандидата           | Кандидаты по должностям, источники кандидатов, кандидаты по местоположению и общее число кандидатов           |
| Статус кандидата             | Кандидаты по типу и статусу и статус кандидата                                                    |
| Демографические данные кандидата       | Кандидаты по возрасту и полу и кандидаты по уровню и статусу образования                             |
| Анализ набора кадров          | Чистый коэффициент найма, среднее число дней для найма, процент неудачного найма и затраты на набор сотрудников                    |
| Анализ проектов по набору сотрудников | Число проектов по набору сотрудников, вакансии по проектам по набору сотрудников или кандидаты по проектам по набору сотрудников |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Данные Dynamics 365 for Operations используются для заполнения отчетов в пакете содержимого по набору сотрудников. В следующей таблице показаны объекты, на которых основан пакет содержимого.

| Объект                          | Содержание                                                         | Связи с другими объектами                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | Кандидаты, принятые кандидаты, чистый коэффициент найма и затраты          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Имя, фамилия и ФИО кандидата                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Календарь корреспондирует с отчетами по секторам                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Компании, по которым требуется фильтровать отчеты                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Дни, недели, месяцы и годы                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Дата рождения, пол, этническое происхождение и семейное положение         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Кандидат, производительность, дата начала и тип кандидата           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Дата начала, дата окончания и дата перехода                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Город, район, почтовый индекс и область или край                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Функция, тип и должность                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Источник кандидатов                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Оценка, описание и модель оценки                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Описание проекта, статус проекта и вакансии                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Уволенные кандидаты, причины, производительность и дата увольнения | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Эти объекты были использованы для создания вычисляемых мер. Эти вычисляемые меры затем использовались для расчета ключевых показателей производительности (KPI) и отчетов, используемых в пакете содержимого. Если требуется включить дополнительные вычисления в отчеты и на панели мониторинга, можно загрузить и изменить файл Recruiting.pbix из LCS. Этот файл является моделью данных по умолчанию, которая использовалась для создания пакета содержимого. После внесения изменений можно создать организационный пакет содержимого панель мониторинга, содержащие добавленные сведения.

## <a name="additional-resources"></a>Дополнительные ресурсы
Ниже приведено несколько полезных ссылок, связанных с объектами и построением содержимого Power BI:

-   [Информационные объекты](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Создание организационных пакетов содержимого](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Моделирование данных с помощью Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Добавление плиток Power BI в рабочие области](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





