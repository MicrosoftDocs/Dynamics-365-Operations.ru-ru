---
title: Планирование производственного заказа с помощью планирования операций и заданий
description: Эта статья рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903937"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Планирование производственного заказа с помощью планирования операций и заданий

[!include [banner](../../includes/banner.md)]

Эта статья рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий. Задания не создаются при планировании операций и создаются при планировании заданий. В качестве компании с демонстрационными данными для создания этой задачи используется USMF. Эта процедура предназначена для менеджера по производству, планировщика производства или начальника производственного участка, работающего в среде дискретного производства.


## <a name="create-a-production-order"></a>Создание производственного заказа
1. В области переходов выберите **Модули > Управление производством > Производственные заказы > Все производственные заказы**.
2. Выберите **Новый производственный заказ**.
3. В поле **Код номенклатуры** введите или выберите значение. Выберите код номенклатуры **D0001**.  
4. Выберите **Создать**.

## <a name="schedule-operations-for-the-production-order"></a>Планирование операций для производственного заказа
1. Пометьте только что созданную строку.      
2. На панели операций выберите **График**.
3. Выберите **Планирование операций**.
4. В поле **Направление планирования** выберите **Вперед от даты планирования**.
5. В поле **Дата планирования** введите дату. Выберите дату в будущем, например сегодня плюс одна неделя. При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.  
6. Нажмите **ОК**.
7. В списке пометьте выбранную строку. Обратите внимание, что статус изменяется на **Запланировано**. 
8. Выберите **Все задания**. Обратите внимание, что задания не создаются при планировании операций.  
9. Закройте страницу.

## <a name="schedule-jobs-for-the-production-order"></a>Планирование заданий для производственного заказа
1. На панели операций выберите **График**.
2. Выберите **Планирование заданий**.
3. В поле **Направление планирования** выберите **Вперед от даты планирования**.
4. В поле **Дата планирования** введите дату. Выберите дату в будущем, например сегодня плюс одна неделя. При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.  
5. Нажмите **ОК**.
6. На панели операций выберите **Производственный заказ**.
7. Выберите **Все задания**. Обратите внимание, что на основе активного маршрута создано 5 заданий с помощью планирования заданий.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]