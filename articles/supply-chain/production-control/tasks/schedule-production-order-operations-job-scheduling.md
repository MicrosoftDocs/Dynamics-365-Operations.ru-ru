---
title: Планирование производственного заказа с помощью планирования операций и заданий
description: Эта тема рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий.
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841391"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="905e5-103">Планирование производственного заказа с помощью планирования операций и заданий</span><span class="sxs-lookup"><span data-stu-id="905e5-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="905e5-104">Эта тема рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий.</span><span class="sxs-lookup"><span data-stu-id="905e5-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="905e5-105">Задания не создаются при планировании операций и создаются при планировании заданий.</span><span class="sxs-lookup"><span data-stu-id="905e5-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="905e5-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="905e5-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="905e5-107">Эта процедура предназначена для менеджера по производству, планировщика производства или начальника производственного участка, работающего в среде дискретного производства.</span><span class="sxs-lookup"><span data-stu-id="905e5-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="905e5-108">Создание производственного заказа</span><span class="sxs-lookup"><span data-stu-id="905e5-108">Create a production order</span></span>
1. <span data-ttu-id="905e5-109">В области переходов выберите **Модули > Управление производством > Производственные заказы > Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="905e5-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="905e5-110">Выберите **Новый производственный заказ**.</span><span class="sxs-lookup"><span data-stu-id="905e5-110">Select **New production order**.</span></span>
3. <span data-ttu-id="905e5-111">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="905e5-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="905e5-112">Выберите код номенклатуры **D0001**.</span><span class="sxs-lookup"><span data-stu-id="905e5-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="905e5-113">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="905e5-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="905e5-114">Планирование операций для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="905e5-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="905e5-115">Пометьте только что созданную строку.</span><span class="sxs-lookup"><span data-stu-id="905e5-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="905e5-116">На панели операций выберите **График**.</span><span class="sxs-lookup"><span data-stu-id="905e5-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="905e5-117">Выберите **Планирование операций**.</span><span class="sxs-lookup"><span data-stu-id="905e5-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="905e5-118">В поле **Направление планирования** выберите **Вперед от даты планирования**.</span><span class="sxs-lookup"><span data-stu-id="905e5-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="905e5-119">В поле **Дата планирования** введите дату.</span><span class="sxs-lookup"><span data-stu-id="905e5-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="905e5-120">Выберите дату в будущем, например сегодня плюс одна неделя.</span><span class="sxs-lookup"><span data-stu-id="905e5-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="905e5-121">При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.</span><span class="sxs-lookup"><span data-stu-id="905e5-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="905e5-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="905e5-122">Select **OK**.</span></span>
7. <span data-ttu-id="905e5-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="905e5-123">In the list, mark the selected row.</span></span> <span data-ttu-id="905e5-124">Обратите внимание, что статус изменяется на **Запланировано**.</span><span class="sxs-lookup"><span data-stu-id="905e5-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="905e5-125">Выберите **Все задания**.</span><span class="sxs-lookup"><span data-stu-id="905e5-125">Select **All jobs**.</span></span> <span data-ttu-id="905e5-126">Обратите внимание, что задания не создаются при планировании операций.</span><span class="sxs-lookup"><span data-stu-id="905e5-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="905e5-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="905e5-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="905e5-128">Планирование заданий для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="905e5-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="905e5-129">На панели операций выберите **График**.</span><span class="sxs-lookup"><span data-stu-id="905e5-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="905e5-130">Выберите **Планирование заданий**.</span><span class="sxs-lookup"><span data-stu-id="905e5-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="905e5-131">В поле **Направление планирования** выберите **Вперед от даты планирования**.</span><span class="sxs-lookup"><span data-stu-id="905e5-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="905e5-132">В поле **Дата планирования** введите дату.</span><span class="sxs-lookup"><span data-stu-id="905e5-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="905e5-133">Выберите дату в будущем, например сегодня плюс одна неделя.</span><span class="sxs-lookup"><span data-stu-id="905e5-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="905e5-134">При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.</span><span class="sxs-lookup"><span data-stu-id="905e5-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="905e5-135">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="905e5-135">Select **OK**.</span></span>
6. <span data-ttu-id="905e5-136">На панели операций выберите **Производственный заказ**.</span><span class="sxs-lookup"><span data-stu-id="905e5-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="905e5-137">Выберите **Все задания**.</span><span class="sxs-lookup"><span data-stu-id="905e5-137">Select **All jobs**.</span></span> <span data-ttu-id="905e5-138">Обратите внимание, что на основе активного маршрута создано 5 заданий с помощью планирования заданий.</span><span class="sxs-lookup"><span data-stu-id="905e5-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]