---
title: Обновление статуса канбана
description: Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 741a2a29e6b222c722e94db4e07dee6c8f4014030364753e3352fa30594dac0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715682"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]