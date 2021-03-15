---
title: Удаление задания канбана из плана
description: В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на "Не запланировано".
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcd9247e24323ba606377d7e51bd4447ab51c905
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961623"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Удаление задания канбана из плана

[!include [banner](../../includes/banner.md)]

В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на "Не запланировано". В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для начальника цеха или планировщика производства.


## <a name="find-a-planned-kanban-job"></a>Поиск запланированного задания канбана
1. Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".
2. В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
3. В списке перейдите по ссылке в выбранной строке.
    * Выберите производственную ячейку 1250.  
4. Щелкните Выбрать.
5. В поле "Показать статус задания" выберите "Запланировано".

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Удаление запланированного задания канбана из плана
1. В списке найдите и выберите требуемую запись.
    * Выберите задание со статусом "Запланировано", например задание, запланированное на 19 декабря 2012 г.  
2. В области действий щелкните "План".
3. Щелкните "Вернуть статус задания".
4. Нажмите кнопку "OК".
    * В результате текущий статус задания будет изменен с "Запланировано" на "Не запланировано" и задание будет удалено с панели процессов.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]