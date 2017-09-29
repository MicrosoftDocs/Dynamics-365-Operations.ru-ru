--- 
title: "Бережливая фиксация из заказов на продажу"
description: "Эта процедура ориентирована на проверку дерева информации об источниках потребности из строки продаж, где номенклатура производится с использованием канбанов."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3aa8cd2c0be56875904158f041cf120c466d9e9a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="f7006-103">Бережливая фиксация из заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="f7006-103">Lean pegging from sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7006-104">Эта процедура ориентирована на проверку дерева информации об источниках потребности из строки продаж, где номенклатура производится с использованием канбанов.</span><span class="sxs-lookup"><span data-stu-id="f7006-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="f7006-105">После проверки дерева информации об источниках потребности все задания канбана становятся запланированными.</span><span class="sxs-lookup"><span data-stu-id="f7006-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="f7006-106">Это полезно для сценариев заказов, получателю заказа важно, чтобы производство могла начаться сразу же.</span><span class="sxs-lookup"><span data-stu-id="f7006-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="f7006-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="f7006-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f7006-108">Эта процедура предназначена для опытного получателя заказа, работающего в бережливой компании.</span><span class="sxs-lookup"><span data-stu-id="f7006-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="f7006-109">Создание заказа на продажу для номенклатуры, контролируемой канбаном</span><span class="sxs-lookup"><span data-stu-id="f7006-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="f7006-110">Перейдите в раздел "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="f7006-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="f7006-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f7006-111">Click New.</span></span>
3. <span data-ttu-id="f7006-112">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f7006-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="f7006-113">Используйте US-001.</span><span class="sxs-lookup"><span data-stu-id="f7006-113">Use US-001.</span></span>  
4. <span data-ttu-id="f7006-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7006-114">Click OK.</span></span>
5. <span data-ttu-id="f7006-115">В поле "Код номенклатуры" введите "L0001".</span><span class="sxs-lookup"><span data-stu-id="f7006-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="f7006-116">В поле "Количество" укажите "30".</span><span class="sxs-lookup"><span data-stu-id="f7006-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="f7006-117">Важно, чтобы количество было больше 24, чтобы активировалось правило канбана событий.</span><span class="sxs-lookup"><span data-stu-id="f7006-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="f7006-118">Открытие дерева информации об источниках потребности</span><span class="sxs-lookup"><span data-stu-id="f7006-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="f7006-119">Щелкните "Продукт и поставки".</span><span class="sxs-lookup"><span data-stu-id="f7006-119">Click Product and supply.</span></span>
2. <span data-ttu-id="f7006-120">Щелкните "Просмотр дерева информации об источниках потребности".</span><span class="sxs-lookup"><span data-stu-id="f7006-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="f7006-121">Обратите внимание, что в дереве информации об источниках потребности показаны все уровни информации об источниках потребности, необходимые для строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7006-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="f7006-122">В этом случае есть два уровня канбана и все необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="f7006-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="f7006-123">Планирование дерева информации об источниках потребности</span><span class="sxs-lookup"><span data-stu-id="f7006-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="f7006-124">В дереве выберите "Строка продаж 000832\Канбан 000558".</span><span class="sxs-lookup"><span data-stu-id="f7006-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="f7006-125">Разверните раздел "Задания канбана".</span><span class="sxs-lookup"><span data-stu-id="f7006-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="f7006-126">Обратите внимание, что статус задания для задания канбана — "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="f7006-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="f7006-127">Щелкните "Запланировать дерево информации об источниках потребности целиком".</span><span class="sxs-lookup"><span data-stu-id="f7006-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="f7006-128">Это запланирует все задания канбана в дереве информации об источниках потребности, а статуса заданий будет изменен с "Не запланировано" на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="f7006-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="f7006-129">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="f7006-129">Refresh the page.</span></span>
    * <span data-ttu-id="f7006-130">Обратите внимание, что статус задания канбана изменился с "Не запланировано" на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="f7006-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="f7006-131">В дереве выберите "Строка продаж 000832\Канбан 000558\Расход для L0001\Канбан 000559".</span><span class="sxs-lookup"><span data-stu-id="f7006-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="f7006-132">Задание для второго канбана также запланировано, поскольку запланировано все дерево информации об источниках потребности.</span><span class="sxs-lookup"><span data-stu-id="f7006-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="f7006-133">Обратите внимание, что статус задания канбана изменился с "Не запланировано" на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="f7006-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


