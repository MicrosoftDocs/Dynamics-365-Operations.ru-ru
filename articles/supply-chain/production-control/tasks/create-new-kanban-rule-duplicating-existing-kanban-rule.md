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
ms.openlocfilehash: 0bc65dd80221cedd25890037afcb3d2617f22793
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149221"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a>Создание правила канбана путем копирования имеющегося правила канбана

[!include [banner](../../includes/banner.md)]

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

