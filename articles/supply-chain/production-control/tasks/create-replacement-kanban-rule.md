---
title: Создание правила канбана замены
description: Эта процедура рассматривает замену существующего правила канбана на новое правило канбана на конкретную дату.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5aebd88dee9621d2c85af3a4fb5bf76ae8e6b80
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828954"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="e7373-103">Создание правила канбана замены</span><span class="sxs-lookup"><span data-stu-id="e7373-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7373-104">Эта процедура рассматривает замену существующего правила канбана на новое правило канбана на конкретную дату.</span><span class="sxs-lookup"><span data-stu-id="e7373-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="e7373-105">Это полезно, когда необходимо скоординировать и запланировать изменения в производственном потоке или правилах пополнения.</span><span class="sxs-lookup"><span data-stu-id="e7373-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="e7373-106">В качестве компании с демонстрационными данными для создания процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e7373-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="e7373-107">Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство измененного производственного потока или нового правила пополнения.</span><span class="sxs-lookup"><span data-stu-id="e7373-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="e7373-108">Эта задача заменяет правило канбана 000022 на новое правило и увеличивает максимальное количество с 48 до 100 для нового правила.</span><span class="sxs-lookup"><span data-stu-id="e7373-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="e7373-109">Выбор правила канбана для замены</span><span class="sxs-lookup"><span data-stu-id="e7373-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="e7373-110">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="e7373-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="e7373-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e7373-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7373-112">Выберите правило канбана 000022.</span><span class="sxs-lookup"><span data-stu-id="e7373-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="e7373-113">Создание правила канбана замены</span><span class="sxs-lookup"><span data-stu-id="e7373-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="e7373-114">Щелкните "Заменить правило канбана".</span><span class="sxs-lookup"><span data-stu-id="e7373-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="e7373-115">В поле "Действует с" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="e7373-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="e7373-116">Выберите дату в будущем, например одна неделя, начиная с сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="e7373-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="e7373-117">Это дата и время, когда новое правило канбана станет активным и заменит старое правило канбана.</span><span class="sxs-lookup"><span data-stu-id="e7373-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="e7373-118">Если правило канбана изменяет путь в производственном потоке, можно выбрать другое мероприятие.</span><span class="sxs-lookup"><span data-stu-id="e7373-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="e7373-119">В этой процедуре мероприятие не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e7373-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="e7373-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e7373-120">Click OK.</span></span>
    * <span data-ttu-id="e7373-121">Обратите внимание, что новое правило канбана создается для замены правила канбана 000022.</span><span class="sxs-lookup"><span data-stu-id="e7373-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="e7373-122">Дата вступления в силу настраивается в соответствии с датой, выбранной при замене правила канбана.</span><span class="sxs-lookup"><span data-stu-id="e7373-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="e7373-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e7373-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7373-124">Выберите замененное правило канбана 000022.</span><span class="sxs-lookup"><span data-stu-id="e7373-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="e7373-125">Обратите внимание, что дата замененного правила канбана совпадает с датой вступления в силу, поскольку это дата окончание его срока действия.</span><span class="sxs-lookup"><span data-stu-id="e7373-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="e7373-126">В списке выберите строку 1.</span><span class="sxs-lookup"><span data-stu-id="e7373-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="e7373-127">Выберите новое правило канбана вверху списка.</span><span class="sxs-lookup"><span data-stu-id="e7373-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="e7373-128">Это правило канбана с самым большим номером правила канбана.</span><span class="sxs-lookup"><span data-stu-id="e7373-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="e7373-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e7373-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e7373-130">Щелкните номер правила канбана, чтобы открыть правило канбана.</span><span class="sxs-lookup"><span data-stu-id="e7373-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="e7373-131">Изменение максимального количества для заменяющего правила канбана</span><span class="sxs-lookup"><span data-stu-id="e7373-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="e7373-132">Установите для параметра "Максимальное количество" значение "100".</span><span class="sxs-lookup"><span data-stu-id="e7373-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="e7373-133">Разверните экспресс-вкладку "Количества", чтобы просмотреть поле "Максимальное количество".</span><span class="sxs-lookup"><span data-stu-id="e7373-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="e7373-134">Изменение максимального количества на 100 позволит обрабатывать до 100 канбанов.</span><span class="sxs-lookup"><span data-stu-id="e7373-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="e7373-135">Это последний этап в этой задаче.</span><span class="sxs-lookup"><span data-stu-id="e7373-135">This is the last step in this task.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]