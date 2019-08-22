---
title: Создание правила канбана путем копирования имеющегося правила канбана
description: Эта процедура описывает создание дубликата существующего правила канбана.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3aef2725152d39e49070f33d0c56089200c94353
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837814"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a>Создание правила канбана путем копирования имеющегося правила канбана

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура описывает создание дубликата существующего правила канбана. Это полезно, если нужно создать новые правила канбана на основе существующих правил канбана. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство измененного производственного потока нового или нового правила пополнения.


## <a name="select-a-kanban-rule"></a>Выберите правило канбана
1. Перейти к правилам канбана.
2. В списке найдите и выберите требуемую запись.
    * Выберите правило канбана 000017 для продукта M0006.  

## <a name="duplicate-a-kanban-rule"></a>Дублировать правило канбана
1. Щелкните "Дублировать правило канбана".
    * Дублируя правило канбана, можно изменить тип, даты, мероприятия и выбор продукта. Изменение продукта для этой процедуры выполняется на следующем этапе.  
2. В поле "Продукт" введите или выберите значение.
    * Выберите M0007.  
3. Нажмите кнопку "OК".
    * Обратите внимание, что создается дубликат правила канбана 000017.    

