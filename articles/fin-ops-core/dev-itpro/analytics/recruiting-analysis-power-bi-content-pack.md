---
title: Содержимое Power BI "Набор сотрудников"
description: В этой статье описывается содержимое Power BI "Набор сотрудников".
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.form: HcmRecruitmentWorkspace
ms.openlocfilehash: 412a1225544bb73649c9f0e703ec7b9a0d2613e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276607"
---
# <a name="recruiting-power-bi-content"></a>Содержимое Power BI "Набор сотрудников"

[!include [banner](../includes/banner.md)]

В этой статье описывается содержимое Microsoft Power BI **Набор сотрудников**. В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

## <a name="accessing-the-power-bi-content"></a>Доступ к содержимому Power BI
Содержимое Power BI **Набор сотрудников** отображается в рабочей области **Управление набором сотрудников**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Отчеты и визуализации в рабочей области "Управление набором сотрудников"
Рабочая область **Управление набором сотрудников** содержит вкладку **Аналитика**. На этой вкладке содержится интегрированное содержимое Power BI по набору сотрудников. Содержимое состоит из обзорной вкладки и дополнительных вкладок с подробными сведениями. В следующей таблице приводится описание отчетов на каждой вкладке.

| Отчет               | Содержание |
|----------------------|----------|
| Обзор набора сотрудников | Сводка по другим отчетам |
| Анализ кандидата   | Общее число кандидатов, кандидаты по должностям, источники кандидатов, соотношение кандидатов-женщин и кандидатов-мужчин и кандидаты по местоположению |
| Статус кандидата     | Кандидаты по типу и статусу и статус кандидата |
| Анализ набора кадров  | Чистый коэффициент найма, среднее число дней для найма, процент неудачного найма, затраты на набор сотрудников, число проектов по набору сотрудников, отношение числа принятых кандидатов к общему числу кандидатов и соотношение кандидатов и открытых вакансий по проектам набора сотрудников |

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

В следующей таблице показаны объекты, на которых основано содержимое Power BI **Набор сотрудников**.

| Объект               | Содержание                                                         | Связи с другими объектами |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Кандидат            | Кандидаты, принятые кандидаты, чистый коэффициент найма и затраты          | Имя кандидата, компания, смещение календаря, дата, географическое местоположение, демографические данные, должность, источник, проект по набору сотрудников |
| Имя кандидата       | Имя, фамилия и ФИО кандидата                   | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Смещение календаря      | Календарь корреспондирует с отчетами по секторам                                | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Организация              | Компании, по которым требуется фильтровать отчеты                                   | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Дата                 | Дни, недели, месяцы и годы                                   | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Демографические данные         | Дата рождения, пол, этническое происхождение и семейное положение         | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Принятый на работу кандидат   | Кандидат, производительность, дата начала и тип кандидата           | Компания, смещение календаря, дата, географическое местоположение, имя кандидата, занятость, производительность труда, должность, источник, проект по набору сотрудников |
| Занятость           | Дата начала, дата окончания и дата перехода                        | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Географическое местоположение  | Город, район, почтовый индекс и область или край                 | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Задание                  | Функция, тип и должность                                        | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Источники                | Источник кандидатов                                             | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Производительность          | Оценка, описание и модель оценки                            | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Проект по набору сотрудников  | Описание проекта, статус проекта и вакансии                | Кандидат, принятый на работу кандидат, уволенный кандидат |
| Уволенный кандидат | Уволенные кандидаты, причины, производительность и дата увольнения | Компания, смещение календаря, дата, географическое местоположение, имя кандидата, демографические данные, занятость, источник, проект по набору сотрудников, имя кандидата |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
