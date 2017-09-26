--- 
title: "Планирование производственного заказа с помощью планирования операций и заданий"
description: "Эта процедура рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 10ccb4ac1088e27f3f5771bcb964bf3cc0a509ab
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Планирование производственного заказа с помощью планирования операций и заданий

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий. Задания не создаются при планировании операций и создаются при планировании заданий. В качестве компании с демонстрационными данными для создания этой задачи используется USMF. Эта процедура предназначена для менеджера по производству, планировщика производства или начальника производственного участка, работающего в среде дискретного производства.


## <a name="create-a-production-order"></a>Создание производственного заказа
1. Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".
2. Щелкните "Новый производственный заказ".
3. В поле "Код номенклатуры" введите или выберите значение.
    * Выберите код номенклатуры D0001.  
4. Щелкните "Создать".

## <a name="schedule-operations-for-the-production-order"></a>Планирование операций для производственного заказа
1. В списке пометьте выбранную строку.
    * Выберите производственный заказ, который вы только что создали. Он должен находиться вверху списка.      
2. В области действий щелкните "План".
3. Щелкните "Планирование операций".
4. В поле "Направление планирования" выберите "Вперед от даты планирования".
5. В поле "Дата планирования" введите дату.
    * Выберите дату в будущем, например сегодня плюс одна неделя. При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.  
6. Нажмите кнопку "OК".
7. В списке пометьте выбранную строку.
    * Обратите внимание, что статус изменяется на "Запланировано".  
8. В списке перейдите по ссылке в выбранной строке.
9. Щелкните "Все задания".
    * Обратите внимание, что задания не создаются при планировании операций.  
10. Закройте страницу.

## <a name="schedule-jobs-for-the-production-order"></a>Планирование заданий для производственного заказа
1. В области действий щелкните "План".
2. Щелкните "Планирование заданий".
3. В поле "Направление планирования" выберите "Вперед от даты планирования".
4. В поле "Дата планирования" введите дату.
    * Выберите дату в будущем, например сегодня плюс одна неделя. При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.  
5. Нажмите кнопку "OК".
6. В области действий щелкните "Производственный заказ".
7. Щелкните "Все задания".
    * Обратите внимание, что на основе активного маршрута создано 5 заданий с помощью планирования заданий.  

