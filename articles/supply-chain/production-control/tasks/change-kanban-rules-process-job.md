---
title: Изменение правил канбана для задания обработки
description: Эта процедура нацелена на изменение используемого правила канбана для данного канбана.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435768"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Изменение правил канбана для задания обработки

[!include [banner](../../includes/banner.md)]

Эта процедура нацелена на изменение используемого правила канбана для данного канбана. Это бывает полезно для выравнивания загрузки ресурсов или в случае разбиения работ. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для планировщика, который работает в компании, использующей бережливое производство, и отвечает за поток создания ценности.


## <a name="copy-kanban-rule"></a>Копирование правила канбана
1. Перейти к правилам канбана.
2. В списке найдите и выберите требуемую запись.
    * Выберите правило канбана событий 000022 для L0001.  
3. Щелкните "Дублировать правило канбана".
4. Нажмите кнопку "OК".

## <a name="change-kanban-rule"></a>Изменение правила канбана
1. Закройте страницу.
2. Перейдите в раздел "Планирование заданий канбана".
3. В списке пометьте выбранную строку.
    * Выберите строку с канбаном 000177.  
4. Щелкните "Использовать альтернативное правило канбана".
5. Щелкните Далее.
6. В поле "Правило канбана" введите или выберите значение.
    * Выберите правило канбана, созданное ранее. Это правило канбана с самым большим номером.  
7. Нажмите кнопку Готово.
    * Теперь задание канбана использует другое правило канбана. Это может быть полезно для выравнивание загрузки производственных ячеек.  

