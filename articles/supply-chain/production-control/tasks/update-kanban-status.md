---
title: Обновление статуса канбана
description: Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436205"
---
# <a name="update-kanban-status"></a>Обновление статуса канбана

[!include [banner](../../includes/banner.md)]

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

