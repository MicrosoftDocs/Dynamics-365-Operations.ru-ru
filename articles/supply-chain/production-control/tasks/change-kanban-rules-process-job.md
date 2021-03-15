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
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0e1989bcc4ca02d097f9ebff40f21158f26546
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981364"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]