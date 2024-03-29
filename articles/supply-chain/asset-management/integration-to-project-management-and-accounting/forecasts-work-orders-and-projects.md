---
title: Прогнозы, заказы на работу и проекты
description: В этой статье рассматривается интеграция прогнозов и заказов на работу с модулем "Управление и учет по проектам" в управлении активами.
author: johanhoffmann
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: df1e1fe352add8361309df54b2178ec27752466d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016807"
---
# <a name="forecasts-work-orders-and-projects"></a>Прогнозы, заказы на работу и проекты

[!include [banner](../../includes/banner.md)]

 

В управлении активами интеграция с модулем **Управление и учет по проектам** помогает оптимизировать управление затратами, чтобы пользователи могли отслеживать затраты по прогнозам для типов заданий обслуживания и заданиям заказов на работу.

Для отслеживания прогнозов типов заданий обслуживания требуются два параметра:

1. Выберите проект в разделе **Управление активами** > **Настройка** > **Параметры управления активами**, затем на вкладке **Активы** > на экспресс-вкладке **Проект** в поле **Проект прогноза обслуживания** выберите проект.

2. При создании строки по умолчанию для типа задания обслуживания автоматически создается номер мероприятия для строки на странице **Значения по умолчанию для типа заданий обслуживания** (**Управление активами** > **Настройка** > **Задания** > **Значения по умолчанию для типа заданий обслуживания**).

Прогнозы типа задания обслуживания служат двум целям: 

- Можно отслеживать затраты по прогнозам типа заданий обслуживания в модуле **Управление и учет по проектам**. 
- Прогнозы автоматически переносятся в проект задания заказа на работу при выборе типа задания обслуживания в задании заказа на работу.

Для отслеживания затрат по заданиям заказов на работу необходимо сначала настроить проекты заказов на работу. Дополнительные сведения см. в разделе [Настройка заказа на работу по проекту](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Проекты заданий заказов на работу

При создании задания заказа на работу в заказе на работу проект заказа на работу определяется настройкой родительского проекта для заказов на работу на странице **Настройка заказа на работу по проекту** (**Управление активами** > **Настройка** > **Заказы на работу** > **Настройка проекта**).

Проекты заданий заказов на работу создаются с помощью комбинации следующих сведений о заказе на работу:

- Тип заказа на работу, выбранный в заказе на работу 
- Функциональное местоположение, относящееся к активу в задании заказа на работу
- Тип актива, относящейся к активу в задании заказа на работу  
- Ожидаемые значения времени начала и окончания, заданные в заказе на работу  

Некоторые из этих сведений могут отсутствовать в заказе на работу. Поэтому поиск родительского проекта заказа на работу осуществляется с использованием доступного сочетания данных и выбора кода проекта, соответствующего данным заказа на работу.

Например, на следующем рисунке из-за способа настройки типа актива **Двигатель грузовика** каждое задание заказа на работу, которое создается с типом актива **Двигатель грузовика**, будет являться подпроектом кода проекта 000186.

![Рисунок 1.](media/01-integration-to-pma.png)

Целью кода проекта в задании заказа на работу и связанного с ним номера деятельности является отслеживание затрат, связанных с заданием заказа на работу и выбранным в нем активом, в модуле **Управление и учет по проектам**. (Чтобы просмотреть код проекта и номер деятельности, выберите **Управление активами** > **Заказы на работу** > **Все заказы на работу**, затем выберите заказ на работу. На экспресс-вкладке **Сведения по строке** в поле **Код проекта** отображается код проекта, а в поле **Номер мероприятия** отображается номер мероприятия.) Дополнительные сведения об управлении затратами в модуле управления активами см. в разделе [Контроль затрат и дат](../controlling-and-reporting/cost-and-date-control.md).

На следующей иллюстрации показан графический обзор проектов заказов на работу и связанных мероприятий по проекту.

![Рисунок 2.](media/02-integration-to-pma.png)

При создании нового задания заказа на работу в заказе на работу для задания автоматически создается проект заказа на работу. Финансовые аналитики для актива, связанного с заданием заказа на работу, автоматически переносятся в проект заказа на работу.

Мероприятие по проекту, созданное для задания заказа на работу, имеет связанную с ним сопутствующую информацию. Эта информация о типе задания обслуживания, варианте типа задания обслуживания и специальности. Она полезна, если, например, вы создаете заказ на покупку из заказа на работу (см. раздел [Закупки](../work-orders/procurement.md)) или используете модуль **Управление и учет по проектам** для регистрации времени.

Если актив был установлен в функциональном местоположении, но позже устанавливается в другом функциональном местоположении, финансовые аналитики, связанные с новым функциональным местоположением, автоматически обновляются для актива. Затем, при создании задания заказа на работу для актива, проект заказа на работу для этого задания заказа на работу автоматически получает финансовые аналитики, которые теперь связаны с активом. Поэтому при использовании функциональных местоположений затраты всегда могут отслеживаться в функциональных местоположениях, в которых актив был установлен в любой конкретный момент времени. Автоматическое обновление финансовых аналитик помогает гарантировать полную трассировку затрат для контроля и отчетности по проекту.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Проекты заказов на работу, состояния жизненного цикла заказов на работу, этапы проектов и типы проектов

Чтобы помочь гарантировать правильное использование состояний жизненного цикла заказов на работу и соответствующих этапов проекта в заказах на работу, следует учесть зависимости в отношении модуля **Управление и учет по проектам**:

- В модуле **Управление и учет по проектам** этапы проекта настраиваются для типов проектов на странице **Параметры модуля "Управление и учет по проектам"**.  
- На странице **Параметры модуля "Управление и учет по проектам"** используйте флажки для выбора соответствующих этапов проекта для всех типов проектов, которые будут использоваться. На следующих иллюстрациях пять этапов (**Создано**, **Оценено**, **Запланировано**, **В работе** и **Завершено**) были выбраны для типов проектов **Время и расходы** и **Внутренний**. Эти пять этапов относятся как к заданиям внутреннего обслуживания, так и к заданиям сервисного обслуживания.
- В модуле **Управление активами** типы проектов определяются группами проектов, настроенными на странице **Настройка заказа на работу по проекту** > вкладке **Группа проектов** (**Управление активами** > **Настройка** > **Заказы на работу** > **Настройки проектов**).  
- Группы проектов, которые настроены на странице **Настройка заказа на работу по проекту**, используются при создании заказов на работу. При создании заказа на работу автоматически создается проект заказа на работу для заказа на работу.  
- Каждое состояние жизненного цикла заказов на работу должно иметь связанный этап проекта.  
- Этап проекта, связанный с состоянием жизненного цикла заказа на работу, должен быть определен как активный этап для группы проектов, определенной в проекте заказа на работу. Проект заказа на работу создается автоматически в заказе на работу.
- При создании нового заказа на работу автоматическое выделение проекта заказа на работу основано на настройке на странице **Настройка заказа на работу по проекту**.  

На приведенных ниже рисунках показаны связи между группами проектов заказов на работу, связанными типами проектов, этапами проекта и состояниями жизненного цикла заказов на работу.

![Рисунок 3.](media/03-integration-to-pma.png)

![Рисунок 4.](media/04-integration-to-pma.png)

![Рисунок 5.](media/05-integration-to-pma.png)

Для получения информации о том, как настроить проекты заказов на работу, см. раздел [Настройка заказа на работу по проекту](../setup-for-work-orders/work-order-project-setup.md). Сведения о порядке создания состояний жизненного цикла заказов на работу и этапах проекта см . в разделе [Состояния жизненного цикла заказов на работу](../setup-for-work-orders/work-order-lifecycle-states.md).

На следующем рисунке показан графический обзор различных проектов, созданных в модуле **Управление активами** для включения интеграции с модулем **Управление и учет по проектам**. На нем также показаны рабочие процессы, с которыми связаны проекты.

![Рисунок 6.](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]