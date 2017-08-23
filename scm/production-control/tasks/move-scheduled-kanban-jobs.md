--- 
title: "Перемещение запланированных заданий канбана"
description: "В этой процедуре описывается перемещение запланированных заданий обработки канбана в другой период."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5f101a097643fa027a667b9d6577fbe5d24ecd27
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Перемещение запланированных заданий канбана

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре описывается перемещение запланированных заданий обработки канбана в другой период. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для начальника цеха или планировщика производства, работающего с канбанами.


## <a name="select-scheduled-kanban-jobs"></a>Выбор запланированных заданий канбана
1. Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".
2. В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск. áçêìõý !
3. Markér den valgte række på listen.
    * Выберите производственную ячейку 1250.  
4. Нажмите кнопку "Выбрать".
5. Vælg 'Planlagt' i feltet Display job status.
    * В результате будет отфильтрован список заданий для отображения только запланированных заданий канбана.  

## <a name="move-kanban-jobs-to-a-different-period"></a>Перемещение заданий канбана в другой период
1. Find og vælg den ønskede post på listen.
    * Выберите задание со статусом "Запланировано", например задание, запланированное на 20 декабря 2012 г., в поле "Запланированный период". Затем переместите задание в предыдущий период.  
2. Щелкните "Предыдущий период".
3. Щелкните "Конец".
    * В результате задание переместится в конец списка заданий как последнее задание в предыдущем периоде.  
4. Find og vælg den ønskede post på listen.
    * Выберите задание со статусом "Запланировано", например задание, запланированное на 18 декабря 2012 г., в поле "Запланированный период". Затем переместите задание в следующий период.  
5. Щелкните "Следующий период".
6. Щелкните "Начало".
    * В результате задание переместится в начало списка заданий как первое задание в предыдущем периоде.  

## <a name="task-move-a-job-within-a-period"></a>Задача: перемещение задания в пределах периода
1. Find og vælg den ønskede post på listen.
    * Выберите задание со статусом "Запланировано", например второе задание, запланированное на 19 декабря 2012 г., в поле "Запланированный период". Затем переместите задание в запланированном периоде.  
2. Щелкните "Вперед".
    * Обратите внимание, что задание переместится на одну строку вниз в списке.  
3. Щелкните "Назад".
    * Обратите внимание, что задание переместится на одну строку вверх в списке.  

