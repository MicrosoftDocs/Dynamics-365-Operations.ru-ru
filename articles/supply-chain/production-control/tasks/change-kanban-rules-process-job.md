---
title: Изменение правил канбана для задания обработки
description: Эта процедура нацелена на изменение используемого правила канбана для данного канбана.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554284"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="29a3f-103">Изменение правил канбана для задания обработки</span><span class="sxs-lookup"><span data-stu-id="29a3f-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29a3f-104">Эта процедура нацелена на изменение используемого правила канбана для данного канбана.</span><span class="sxs-lookup"><span data-stu-id="29a3f-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="29a3f-105">Это бывает полезно для выравнивания загрузки ресурсов или в случае разбиения работ.</span><span class="sxs-lookup"><span data-stu-id="29a3f-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="29a3f-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="29a3f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="29a3f-107">Эта процедура предназначена для планировщика, который работает в компании, использующей бережливое производство, и отвечает за поток создания ценности.</span><span class="sxs-lookup"><span data-stu-id="29a3f-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="29a3f-108">Копирование правила канбана</span><span class="sxs-lookup"><span data-stu-id="29a3f-108">Copy kanban rule</span></span>
1. <span data-ttu-id="29a3f-109">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="29a3f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="29a3f-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="29a3f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="29a3f-111">Выберите правило канбана событий 000022 для L0001.</span><span class="sxs-lookup"><span data-stu-id="29a3f-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="29a3f-112">Щелкните "Дублировать правило канбана".</span><span class="sxs-lookup"><span data-stu-id="29a3f-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="29a3f-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="29a3f-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="29a3f-114">Изменение правила канбана</span><span class="sxs-lookup"><span data-stu-id="29a3f-114">Change kanban rule</span></span>
1. <span data-ttu-id="29a3f-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29a3f-115">Close the page.</span></span>
2. <span data-ttu-id="29a3f-116">Перейдите в раздел "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="29a3f-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="29a3f-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="29a3f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="29a3f-118">Выберите строку с канбаном 000177.</span><span class="sxs-lookup"><span data-stu-id="29a3f-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="29a3f-119">Щелкните "Использовать альтернативное правило канбана".</span><span class="sxs-lookup"><span data-stu-id="29a3f-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="29a3f-120">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="29a3f-120">Click Next.</span></span>
6. <span data-ttu-id="29a3f-121">В поле "Правило канбана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="29a3f-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="29a3f-122">Выберите правило канбана, созданное ранее.</span><span class="sxs-lookup"><span data-stu-id="29a3f-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="29a3f-123">Это правило канбана с самым большим номером.</span><span class="sxs-lookup"><span data-stu-id="29a3f-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="29a3f-124">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="29a3f-124">Click Finish.</span></span>
    * <span data-ttu-id="29a3f-125">Теперь задание канбана использует другое правило канбана.</span><span class="sxs-lookup"><span data-stu-id="29a3f-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="29a3f-126">Это может быть полезно для выравнивание загрузки производственных ячеек.</span><span class="sxs-lookup"><span data-stu-id="29a3f-126">This can be useful to level load work cells.</span></span>  

