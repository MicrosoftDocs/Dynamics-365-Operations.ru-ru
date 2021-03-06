---
title: Создание шаблонов рабочего времени
description: Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920937"
---
# <a name="create-working-time-templates"></a>Создание шаблонов рабочего времени

[!include [banner](../../includes/banner.md)]

Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени. Эта процедура описывает определение шаблона рабочего времени с помощью свойств планирования рабочего времени для классификации интервалов рабочего времени. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.

1. Перейдите в раздел **Рабочие области > Управление жизненным циклом ресурса**.
1. Выберите **Шаблоны рабочего времени**.

## <a name="create-working-time-template"></a>Создание шаблона рабочего времени

1. Выберите **Создать**.
1. В поле **Шаблон рабочего времени** введите значение.
1. В поле **Имя** введите значение.
1. Разверните раздел **Понедельник**.
1. Выберите **Добавить**.
1. В поле **С** введите время.
    * Укажите время, когда работа начинается утром.  
1. В поле **По** введите время.
    * Укажите время, когда работники уходят на обед.  
1. Выберите **Добавить**.
1. В поле **С** введите время.
    * Укажите время, когда работа возобновляется после обеда.  
1. В поле **По** введите время.
    * Укажите конец работы за день.  

## <a name="replicate-working-times-to-all-week-days"></a>Дублирование рабочего времени на все дни недели

1. Выберите **Копировать день**.
    * Скопируйте определения рабочего времени с понедельника по вторник.  
1. Нажмите **ОК**.
1. Выберите **Копировать день**.
    * Скопируйте определения рабочего времени с понедельника по среду.  
1. В поле **В день недели** выберите вариант.
1. Нажмите **ОК**.
1. Выберите **Копировать день**.
    * Скопируйте определения рабочего времени с понедельника по четверг.  
1. В поле **В день недели** выберите вариант.
1. Нажмите **ОК**.
1. Выберите **Копировать день**.
    * Скопируйте определения рабочего времени с понедельника по пятницу.  
1. В поле **В день недели** выберите вариант.
1. Нажмите **ОК**.

## <a name="define-time-slots-for-special-operations"></a>Определение временных интервалов для специальных операций

1. Разверните раздел **Пятница**.
1. В списке найдите и выберите требуемую запись.
1. В поле **Свойство** введите или выберите значение.
1. В списке найдите и выберите требуемую запись.
1. В поле **Свойство** введите или выберите значение.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Отметка выходных дней как закрытых для отправки

1. Разверните раздел **Суббота**.
1. Выберите *Да* в поле **Закрыто для отправки**.
1. Разверните раздел **Воскресенье**.
1. Выберите *Да* в поле **Закрыто для отправки**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]