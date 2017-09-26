--- 
title: "Обновление статуса канбана"
description: "Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: caf7dead2da14e1ff76e205e7477b1eb11a2ca52
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="update-kanban-status"></a>Обновление статуса канбана

[!include[task guide banner](../../includes/task-guide-banner.md)]

Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для начальника цеха.


## <a name="find-the-kanban"></a>Найдите канбан.
1. Перейдите в раздел "Управление производством" > "Канбан" > "Канбаны".
2. Откройте фильтр столбца статуса единицы обработки.
3. Щелкните "Очистить".
    * Это приведет к сбросу фильтров.  
4. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Номер карты" по значению "000149".

## <a name="change-emptied-status-to-received-status"></a>Изменение статуса "Освобождено" на "Получено"
1. Щелкните "Обращение пустой единицы обработки".
2. Нажмите кнопку "OК".
    * Обратите внимание, что единица обработки имеет статус "Получено".  

## <a name="change-received-status-to-emptied-status"></a>Изменение статуса "Получено" на "Освобождено"
1. Щелкните "Пустой канбан".
2. В списке пометьте выбранную строку.
    * Обратите внимание, что единица обработки имеет статус "Освобождено".  


