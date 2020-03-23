---
title: Распределение данных бюджетного планирования
description: Эта тема описывает методы распределения, доступные в Microsoft Dynamics 365 Finance, и порядок их возможного использования.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8bcfb4d3720d03ce84024766a66ccfc546767ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772084"
---
# <a name="budget-planning-data-allocation"></a>Распределение данных бюджетного планирования

[!include [banner](../includes/banner.md)]

Эта статья описывает методы распределения, доступные в Microsoft Dynamics 365 Finance, и порядок их возможного использования.  

Вы можете распределить данные в плане бюджета несколькими способами, чтобы точно изобразить запроектированные количества.

## <a name="allocation-methods"></a>Методы распределения
Три метода распределения (Распределять по нескольким периодам, Распределить по аналитикам и Использовать правила распределения ГК) могут создать строки бюджетного плана, которые основаны на строках в таком же бюджетном плане. Три других метода (Агрегировано, Распределить, и Копировать из бюджетного плана) могут создать строки бюджетного плана в других бюджетных плана. Для всех шести методов распределения вы определяете сценарий назначения. Исходный и конечный сценарии могут различаться или представлять собой один и тот же сценарий. Дополнительно, вы можете указать, добавляются ли новые строки к бюджетному плану или заменяют текущие строки в бюджетном плане.

[![Метод распределения "Распределять по нескольким периодам"](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Распределять по нескольким периодам** — Категория распределения по периодам используется, чтобы распределить строки бюджетного плана из исходного сценария бюджетного плана по периодам конечного сценария. Исходная сумма задана несколько линиям в сценарии назначения, основанном на проценте и дате, которые определены в категории распределения периода.         

[![Метод распределения "Распределить по аналитикам"](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Распределить по аналитикам** — Строки бюджетного плана распределяются из исходного сценария бюджетного планирования в одну или несколько строк конечного сценария, на основании процентов и финансовых аналитик, которые определены в выбранном условии распределения бюджета.           

![Диаграмма "Агрегировано"](./media/aggregatechart-300x230.png)
**Агрегировано** — строки бюджетного плана агрегируются из исходного сценария бюджетного плана в связанных (дочерних) бюджетных планах в конечный сценарий родительского бюджетного плана. Этот метод включает суммы бюджета, которые подготовлены на нижнем уровне в организации и должны быть консолидированными на более высоком уровне.          

[![Диаграмма "Распределение"](./media/distributechart-300x230.png)](./media/distributechart.png)
**Распределение** – Строки бюджетного плана распределяются из исходного сценария бюджетного планирования в родительском бюджетном плане в сценарии назначения в связанных (дочерних) бюджетных планах, на основании финансовых аналитик в организационных подразделениях соответствующих планов. Этот метод включает суммы бюджета, которые подготовлены на нижнем уровне в организации и должны быть распределены для более локализованного рассмотрения.           

[![Правила распределения ГК](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Использовать правила распределения ГК** — Строки бюджетного плана распределяются из исходного сценария бюджетного плана в конечный сценарий бюджетного планирования согласно выбранному правилу распределения главной книги. 

[![Копировать из бюджетного плана](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Копировать из бюджетного плана** — Как в методе распределить распределение, строки бюджетного плана создаются в назначении на основе строк в связанном бюджетном плане. Однако для этого метода, исходный план бюджета не должен быть родителем, но может находиться на любом более высоком уровне в иерархии плана бюджета. Этот метод распределения полезен, если консолидированные суммы первоначально бюджетированы на гораздо более высоком уровне, и должны быть перенесены на более низкий уровень организации для подробного обзора и корректировки, прежде чем они могут получить утверждение верхнего уровня.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Использование методов распределения в плане бюджета
Чтобы выполнить распределения на странице плана бюджета, выберите строки для распределения и после этого щелкните **Распределить бюджет**.

[![Кнопка "Распределить бюджет"](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Затем выберите метод распределения. Остальные поля после этого устанавливаются, на основе выбранного способа. Эти поля включают источник и назначение данных плана бюджета, и вариант, который позволяет вам умножить источник на определенный Коэффициент, когда создаются суммы назначения, чтобы упростить массовую корректировку. Вы можете также установить параметр **Присоединить к плану**. Выберите **Нет**, чтобы заменить существующие строки плана бюджета, или выберите **Да** для того, чтобы сохранить существующие строки плана бюджета и добавить новые строки для распределенных сумм.

## <a name="automating-allocations-during-a-workflow"></a>Автоматизация распределений во время workflow-процесса
Одна мощная функция позволяет распределению быть выполненным автоматически как часть workflow-процесса планирования бюджета. По мере того как план бюджета двигается через свой workflow-процесс, автоматизированные задачи могут вызывать распределение на определенной стадии планирования бюджета. 

Для того, чтобы настроить автоматизированное распределение, вам сперва создать необходимо график распределения на странице **Конфигурация бюджетного планирования**. График распределения определяет метод распределения, который будет использован, когда автоматизированное распределение выполняется, и значения различных вариантов распределения (см. описания в предыдущем разделе). 

Затем, вы создаете распределение стадии на странице **Конфигурация бюджетного планирования**. Распределение стадий назначает график распределения к workflow-процессу и стадии бюджетного планирования. 

В конце концов, добавьте автоматизированную задачу для распределения стадии планирования бюджета на желаемой стадии workflow-процесса. В следующем примере, два распределения стадии планирования бюджета (отмечены красным) были вставлены в workflow-процесс.

[![Распределения этапа планирования бюджета](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)


