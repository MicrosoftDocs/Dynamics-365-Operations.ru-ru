--- 
title: "Изменение правил канбана для задания обработки"
description: "Эта процедура нацелена на изменение используемого правила канбана для данного канбана."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="219a8-103">Изменение правил канбана для задания обработки</span><span class="sxs-lookup"><span data-stu-id="219a8-103">Change kanban rules for a process job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="219a8-104">Эта процедура нацелена на изменение используемого правила канбана для данного канбана.</span><span class="sxs-lookup"><span data-stu-id="219a8-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="219a8-105">Это бывает полезно для выравнивания загрузки ресурсов или в случае разбиения работ.</span><span class="sxs-lookup"><span data-stu-id="219a8-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="219a8-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="219a8-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="219a8-107">Эта процедура предназначена для планировщика, который работает в компании, использующей бережливое производство, и отвечает за поток создания ценности.</span><span class="sxs-lookup"><span data-stu-id="219a8-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="219a8-108">Копирование правила канбана</span><span class="sxs-lookup"><span data-stu-id="219a8-108">Copy kanban rule</span></span>
1. <span data-ttu-id="219a8-109">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="219a8-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="219a8-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="219a8-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="219a8-111">Выберите правило канбана событий 000022 для L0001.</span><span class="sxs-lookup"><span data-stu-id="219a8-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="219a8-112">Щелкните "Дублировать правило канбана".</span><span class="sxs-lookup"><span data-stu-id="219a8-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="219a8-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="219a8-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="219a8-114">Изменение правила канбана</span><span class="sxs-lookup"><span data-stu-id="219a8-114">Change kanban rule</span></span>
1. <span data-ttu-id="219a8-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="219a8-115">Close the page.</span></span>
2. <span data-ttu-id="219a8-116">Перейдите в раздел "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="219a8-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="219a8-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="219a8-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="219a8-118">Выберите строку с канбаном 000177.</span><span class="sxs-lookup"><span data-stu-id="219a8-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="219a8-119">Щелкните "Использовать альтернативное правило канбана".</span><span class="sxs-lookup"><span data-stu-id="219a8-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="219a8-120">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="219a8-120">Click Next.</span></span>
6. <span data-ttu-id="219a8-121">В поле "Правило канбана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="219a8-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="219a8-122">Выберите правило канбана, созданное ранее.</span><span class="sxs-lookup"><span data-stu-id="219a8-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="219a8-123">Это правило канбана с самым большим номером.</span><span class="sxs-lookup"><span data-stu-id="219a8-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="219a8-124">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="219a8-124">Click Finish.</span></span>
    * <span data-ttu-id="219a8-125">Теперь задание канбана использует другое правило канбана.</span><span class="sxs-lookup"><span data-stu-id="219a8-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="219a8-126">Это может быть полезно для выравнивание загрузки производственных ячеек.</span><span class="sxs-lookup"><span data-stu-id="219a8-126">This can be useful to level load work cells.</span></span>  


