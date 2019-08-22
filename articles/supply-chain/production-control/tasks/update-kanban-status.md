---
title: Обновление статуса канбана
description: Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97b6eea4e93967dbe1eea5eac9fe3fbf6b336a49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838471"
---
# <a name="update-kanban-status"></a>Обновление статуса канбана

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

