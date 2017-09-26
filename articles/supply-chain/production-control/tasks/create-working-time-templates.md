--- 
title: "Создание шаблонов рабочего времени"
description: "Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Создание шаблонов рабочего времени

[!include[task guide banner](../../includes/task-guide-banner.md)]

Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени. Эта процедура описывает определение шаблона рабочего времени с помощью свойств планирования рабочего времени для классификации интервалов рабочего времени. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.

1. Перейдите в раздел "Все рабочие области" > "Управление жизненным циклом ресурса".
2. Щелкните "Шаблоны расписания".

## <a name="create-working-time-template"></a>Создание шаблона рабочего времени
1. Щелкните "Создать".
2. В поле "Шаблон рабочего времени" введите значение.
3. В поле "Имя" введите значение.
4. Разверните раздел "Понедельник".
5. Нажмите кнопку Добавить.
6. В поле "С" введите время.
    * Укажите время, когда работа начинается утром.  
7. В поле "По" введите время.
    * Укажите время, когда работники уходят на обед.  
8. Нажмите кнопку Добавить.
9. В поле "С" введите время.
    * Укажите время, когда работа возобновляется после обеда.  
10. В поле "По" введите время.
    * Укажите конец работы за день.  

## <a name="replicate-working-times-to-all-week-days"></a>Дублирование рабочего времени на все дни недели
1. Щелкните "Копировать день".
    * Скопируйте определения рабочего времени с понедельника по вторник.  
2. Нажмите кнопку "OК".
3. Щелкните "Копировать день".
    * Скопируйте определения рабочего времени с понедельника по среду.  
4. В поле "В день недели" выберите вариант.
5. Нажмите кнопку "OК".
6. Щелкните "Копировать день".
    * Скопируйте определения рабочего времени с понедельника по четверг.  
7. В поле "В день недели" выберите вариант.
8. Нажмите кнопку "OК".
9. Щелкните "Копировать день".
    * Скопируйте определения рабочего времени с понедельника по пятницу.  
10. В поле "В день недели" выберите вариант.
11. Нажмите кнопку "OК".

## <a name="define-time-slots-for-special-operations"></a>Определение временных интервалов для специальных операций
1. Разверните раздел "Пятница".
2. В списке найдите и выберите требуемую запись.
3. В поле "Свойство" введите или выберите значение.
4. В списке найдите и выберите требуемую запись.
5. В поле "Свойство" введите или выберите значение.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Отметка выходных дней как закрытых для отправки
1. Разверните раздел "Суббота".
2. Выберите "Да" в поле "Закрыто для отправки".
3. Разверните раздел "Воскресенье".
4. Выберите "Да" в поле "Закрыто для отправки".

