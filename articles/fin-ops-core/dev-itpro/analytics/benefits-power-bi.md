---
title: Содержимое Power BI "Льготы"
description: В этой статье описывается содержимое Power BI "Льготы".
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.search.form: HcmBenefitWorkspace
ms.openlocfilehash: ed1fd0b86e44d022a4858e3b5bc61c83a8efd395
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206668"
---
# <a name="benefits-power-bi-content"></a>Содержимое Power BI "Льготы"

[!include [banner](../includes/banner.md)]

В этой статье описывается содержимое Microsoft Power BI **Льготы**. В нем описывается порядок доступа к включенным отчетам и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.

## <a name="accessing-the-power-bi-content"></a>Доступ к содержимому Power BI
Содержимое Power BI **Льготы** показано в рабочей области **Управление льготами** при использовании одного из следующих продуктов:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Отчеты, включенные в содержимое Power BI
Отчеты, включенные в содержимое Power BI **Льготы**, включают диаграммы и таблицы, которые содержат дополнительные сведения. В следующей таблице приводится описание отчетов.

| Отчет                      | Содержание                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Общие сведения о регистрации льготы | Все планы регистрации, регистрация по группе сотрудников и выбранные параметры плана льготы |
| Льготы сотрудников           | Регистрация сотрудников по выбранным льготам                                                        |

Можно фильтровать диаграммы и плитки в этих отчетах, а также закреплять диаграммы и плитки на панели мониторинга. Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Понимание модели данных и объектов
Следующая информация используется для заполнения отчетов содержимом **Льготы** Power BI. В этой таблице показаны объекты, на которых основано содержимое.

| Объект                   | Содержание                                                                                                   | Связи с другими объектами |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Смещение календаря          | Календарь корреспондирует с отчетами по секторам                                                                          | После назначения на должность, тенденция должностей, тенденция сотрудников, увольнение сотрудника |
| Организация                  | Компании, по которым требуется фильтровать отчеты                                                                             | Текущая компенсация, текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Компенсация             | Ставка и частота оплаты в зависимости от времени                                                                           | Текущая компенсация, текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Текущая компенсация     | Ставка оплаты и частота на текущую дату                                                              | Компания, компенсация, демографические показатели, задание, должность |
| Текущая должность         | Должности по состоянию на текущую дату, эквивалент полной занятости (FTE), открытые позиции и свободные должности | Задание, должность |
| Текущий сотрудник         | Сотрудники по состоянию на текущую дату, возраст и численность сотрудников                                                         | Компания, компенсация, географическое местоположение, имя сотрудника, отчитывается перед, должность сотрудника, демографические показатели, задание, занятость, должность, льготы |
| Дата                     | Дни, недели, месяцы и годы                                                                             | Последнее назначение на должность, тенденция должностей, увольнение сотрудника, тенденция сотрудников |
| Демографические данные             | Дата рождения, пол, этническое происхождение и семейное положение                                                   | Текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Занятость               | Дата начала, дата окончания и дата перехода                                                                  | Текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Географическое местоположение      | Город, район, почтовый индекс и область или край                                                           | Текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Задание                      | Функция, тип и должность                                                                                  | Текущая должность, текущий сотрудник |
| Последнее назначение на должность | Причина назначения, дата начала, дата окончания и должность                                                           | Смещение календаря, дата, задание, должность |
| Занимаемая должность                 | Отдел, полная занятость, должность, тип должности и название должности                                                        | Текущая должность, текущий сотрудник |
| Тенденция должности           | Список занимаемых должностей по времени, полная занятость и должность                                                                          | Смещение календаря, дата, задание, должность |
| Отчитывается перед               | Имя, фамилия и ФИО                                                                       | Текущий работник, уволенный сотрудник, тенденция сотрудников |
| Уволенный сотрудник      | Уволенные сотрудники, дата увольнения, название должности, должность и работа                                           | Компания, компенсация, географическое местоположение, имя сотрудника, отчитывается перед, смещение календаря, дата, должность сотрудника, демографические показатели, занятость, задание, должность, льготы |
| Льготы                 | Дата вступления в силу, параметр льготы, план льгот и тип льготы                                             | Текущее имя, уволенный сотрудник, тенденция сотрудников |
| Имя сотрудника            | Имя, фамилия и ФИО                                                                       | Текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Должность сотрудника           | Должность и дата трудового стажа                                                                                   | Текущий сотрудник, уволенный сотрудник, тенденция сотрудников |
| Тенденция сотрудника           | Сотрудники по времени, численность сотрудников, компания и должность                                                        | Компания, компенсация, географическое местоположение, имя сотрудника, отчитывается перед, смещение календаря, дата, должность сотрудника, демографические показатели, занятость, задание, льготы |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
