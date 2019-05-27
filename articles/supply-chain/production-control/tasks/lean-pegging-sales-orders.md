---
title: Бережливая фиксация из заказов на продажу
description: Эта процедура ориентирована на проверку дерева информации об источниках потребности из строки продаж, где номенклатура производится с использованием канбанов.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e2448dfd83304d4f7e5dfc8ce0d02cdac998779
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555635"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="226b3-103">Бережливая фиксация из заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="226b3-103">Lean pegging from sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="226b3-104">Эта процедура ориентирована на проверку дерева информации об источниках потребности из строки продаж, где номенклатура производится с использованием канбанов.</span><span class="sxs-lookup"><span data-stu-id="226b3-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="226b3-105">После проверки дерева информации об источниках потребности все задания канбана становятся запланированными.</span><span class="sxs-lookup"><span data-stu-id="226b3-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="226b3-106">Это полезно для сценариев заказов, получателю заказа важно, чтобы производство могла начаться сразу же.</span><span class="sxs-lookup"><span data-stu-id="226b3-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="226b3-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="226b3-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="226b3-108">Эта процедура предназначена для опытного получателя заказа, работающего в бережливой компании.</span><span class="sxs-lookup"><span data-stu-id="226b3-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="226b3-109">Создание заказа на продажу для номенклатуры, контролируемой канбаном</span><span class="sxs-lookup"><span data-stu-id="226b3-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="226b3-110">Перейдите в раздел "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="226b3-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="226b3-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="226b3-111">Click New.</span></span>
3. <span data-ttu-id="226b3-112">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="226b3-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="226b3-113">Используйте US-001.</span><span class="sxs-lookup"><span data-stu-id="226b3-113">Use US-001.</span></span>  
4. <span data-ttu-id="226b3-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="226b3-114">Click OK.</span></span>
5. <span data-ttu-id="226b3-115">В поле "Код номенклатуры" введите "L0001".</span><span class="sxs-lookup"><span data-stu-id="226b3-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="226b3-116">В поле "Количество" укажите "30".</span><span class="sxs-lookup"><span data-stu-id="226b3-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="226b3-117">Важно, чтобы количество было больше 24, чтобы активировалось правило канбана событий.</span><span class="sxs-lookup"><span data-stu-id="226b3-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="226b3-118">Открытие дерева информации об источниках потребности</span><span class="sxs-lookup"><span data-stu-id="226b3-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="226b3-119">Щелкните "Продукт и поставки".</span><span class="sxs-lookup"><span data-stu-id="226b3-119">Click Product and supply.</span></span>
2. <span data-ttu-id="226b3-120">Щелкните "Просмотр дерева информации об источниках потребности".</span><span class="sxs-lookup"><span data-stu-id="226b3-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="226b3-121">Обратите внимание, что в дереве информации об источниках потребности показаны все уровни информации об источниках потребности, необходимые для строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="226b3-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="226b3-122">В этом случае есть два уровня канбана и все необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="226b3-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="226b3-123">Планирование дерева информации об источниках потребности</span><span class="sxs-lookup"><span data-stu-id="226b3-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="226b3-124">В дереве выберите "Строка продаж 000832\Канбан 000558".</span><span class="sxs-lookup"><span data-stu-id="226b3-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="226b3-125">Разверните раздел "Задания канбана".</span><span class="sxs-lookup"><span data-stu-id="226b3-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="226b3-126">Обратите внимание, что статус задания для задания канбана — "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="226b3-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="226b3-127">Щелкните "Запланировать дерево информации об источниках потребности целиком".</span><span class="sxs-lookup"><span data-stu-id="226b3-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="226b3-128">Это запланирует все задания канбана в дереве информации об источниках потребности, а статуса заданий будет изменен с "Не запланировано" на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="226b3-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="226b3-129">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="226b3-129">Refresh the page.</span></span>
    * <span data-ttu-id="226b3-130">Обратите внимание, что статус задания канбана изменился с "Не запланировано" на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="226b3-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="226b3-131">В дереве выберите "Строка продаж 000832\Канбан 000558\Расход для L0001\Канбан 000559".</span><span class="sxs-lookup"><span data-stu-id="226b3-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="226b3-132">Задание для второго канбана также запланировано, поскольку запланировано все дерево информации об источниках потребности.</span><span class="sxs-lookup"><span data-stu-id="226b3-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="226b3-133">Обратите внимание, что статус задания канбана изменился с "Не запланировано" на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="226b3-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

