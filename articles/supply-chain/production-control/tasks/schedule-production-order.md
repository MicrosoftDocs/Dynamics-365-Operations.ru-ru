--- 
title: "Планирование производственного заказа"
description: "Следующая процедура показывает планирование производственного заказа."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4aeb51fd2d9e916d5838b47c4a6b74800572a9ca
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order"></a><span data-ttu-id="2ec42-103">Планирование производственного заказа</span><span class="sxs-lookup"><span data-stu-id="2ec42-103">Schedule a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ec42-104">Следующая процедура показывает планирование производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="2ec42-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="2ec42-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="2ec42-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2ec42-106">Это третья из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="2ec42-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="2ec42-107">Планирование производственного заказа</span><span class="sxs-lookup"><span data-stu-id="2ec42-107">Schedule a production order</span></span>
1. <span data-ttu-id="2ec42-108">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="2ec42-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="2ec42-109">Выберите производственный заказ со статусом "Оценено".</span><span class="sxs-lookup"><span data-stu-id="2ec42-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="2ec42-110">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="2ec42-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="2ec42-111">Щелкните "Планирование заданий".</span><span class="sxs-lookup"><span data-stu-id="2ec42-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="2ec42-112">На этой странице задаются параметры планирования.</span><span class="sxs-lookup"><span data-stu-id="2ec42-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="2ec42-113">Вы можете настроить параметры для конкретных пользователей или всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="2ec42-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="2ec42-114">В поле "Направление планирования" выберите "Вперед от сегодняшнего дня".</span><span class="sxs-lookup"><span data-stu-id="2ec42-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="2ec42-115">В поле "Дата планирования" введите дату.</span><span class="sxs-lookup"><span data-stu-id="2ec42-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="2ec42-116">Установите или снимите флажок "Ограничение по мощности".</span><span class="sxs-lookup"><span data-stu-id="2ec42-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="2ec42-117">Установите или снимите флажок "Ограничение по материалам".</span><span class="sxs-lookup"><span data-stu-id="2ec42-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="2ec42-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2ec42-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="2ec42-119">Просмотр результатов планирования</span><span class="sxs-lookup"><span data-stu-id="2ec42-119">View the scheduling results</span></span>
1. <span data-ttu-id="2ec42-120">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="2ec42-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="2ec42-121">Щелкните "Все задания".</span><span class="sxs-lookup"><span data-stu-id="2ec42-121">Click All jobs.</span></span>
    * <span data-ttu-id="2ec42-122">На этой странице отображаются запланированные задания, которые вы только что создали.</span><span class="sxs-lookup"><span data-stu-id="2ec42-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="2ec42-123">Разверните или сверните раздел "Планирование".</span><span class="sxs-lookup"><span data-stu-id="2ec42-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="2ec42-124">На экспресс-вкладке "Планирование" можно просмотреть запланированные дату и время.</span><span class="sxs-lookup"><span data-stu-id="2ec42-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="2ec42-125">Щелкните Запросы.</span><span class="sxs-lookup"><span data-stu-id="2ec42-125">Click Inquiries.</span></span>
5. <span data-ttu-id="2ec42-126">Щелкните "Максимальная мощность".</span><span class="sxs-lookup"><span data-stu-id="2ec42-126">Click Capacity load.</span></span>
    * <span data-ttu-id="2ec42-127">На странице "Максимальная мощность" отображается мощность, зарезервированная при планировании заданий, общее число часов, которое в настоящее время зарезервировано для ресурса, и число часов, которой осталось доступным для планирования заданий этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ec42-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="2ec42-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2ec42-128">Close the page.</span></span>
7. <span data-ttu-id="2ec42-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2ec42-129">Close the page.</span></span>


