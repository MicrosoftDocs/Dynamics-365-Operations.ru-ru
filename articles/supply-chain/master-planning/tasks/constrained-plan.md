--- 
title: "Создание плана с ограничениями"
description: "Следующая процедура используется для создания плана, в котором учитываются ограничения по материалам и мощности."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6dfda1664e487bb4d31cf3e9aaee191dc69d699a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="3cd65-103">Создание плана с ограничениями</span><span class="sxs-lookup"><span data-stu-id="3cd65-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3cd65-104">Следующая процедура используется для создания плана, в котором учитываются ограничения по материалам и мощности.</span><span class="sxs-lookup"><span data-stu-id="3cd65-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="3cd65-105">План гарантирует, что производство не начнется, пока не будут доступны материалы, и что ресурсы не будут зарезервированы с превышением.</span><span class="sxs-lookup"><span data-stu-id="3cd65-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="3cd65-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="3cd65-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3cd65-107">Эта процедура предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="3cd65-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="3cd65-108">Настройка плана с ограничениями</span><span class="sxs-lookup"><span data-stu-id="3cd65-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="3cd65-109">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="3cd65-109">Click Master planning.</span></span>
2. <span data-ttu-id="3cd65-110">Щелкните "Сводные планы".</span><span class="sxs-lookup"><span data-stu-id="3cd65-110">Click Master plans.</span></span>
3. <span data-ttu-id="3cd65-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3cd65-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3cd65-112">Пример: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="3cd65-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="3cd65-113">Выберите значение "Да" в поле "Ограничение по мощности".</span><span class="sxs-lookup"><span data-stu-id="3cd65-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="3cd65-114">В поле "Временная граница ограничения по мощности" введите значение "30".</span><span class="sxs-lookup"><span data-stu-id="3cd65-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="3cd65-115">Разверните раздел "Временные границы в днях".</span><span class="sxs-lookup"><span data-stu-id="3cd65-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="3cd65-116">Выберите значение "Да" в поле "Мощность".</span><span class="sxs-lookup"><span data-stu-id="3cd65-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="3cd65-117">В поле "Временная граница планирования мощности (в днях)" введите число.</span><span class="sxs-lookup"><span data-stu-id="3cd65-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="3cd65-118">Пример: 60</span><span class="sxs-lookup"><span data-stu-id="3cd65-118">Example: 60</span></span>  
9. <span data-ttu-id="3cd65-119">Выберите значение "Да" в поле "Рассчитанные задержки".</span><span class="sxs-lookup"><span data-stu-id="3cd65-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="3cd65-120">В поле "Временная граница расчета задержек (в днях)" введите число.</span><span class="sxs-lookup"><span data-stu-id="3cd65-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="3cd65-121">Пример: 60</span><span class="sxs-lookup"><span data-stu-id="3cd65-121">Example: 60</span></span>  
11. <span data-ttu-id="3cd65-122">Разверните раздел "Рассчитанные задержки".</span><span class="sxs-lookup"><span data-stu-id="3cd65-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="3cd65-123">Выберите значение"Да" в поле "Добавить рассчитанную задержку к дате потребности".</span><span class="sxs-lookup"><span data-stu-id="3cd65-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="3cd65-124">Выберите значение"Да" в поле "Добавить рассчитанную задержку к дате потребности".</span><span class="sxs-lookup"><span data-stu-id="3cd65-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="3cd65-125">Выберите значение"Да" в поле "Добавить рассчитанную задержку к дате потребности".</span><span class="sxs-lookup"><span data-stu-id="3cd65-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="3cd65-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3cd65-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="3cd65-127">Создание плана с ограничениями</span><span class="sxs-lookup"><span data-stu-id="3cd65-127">Create a constrained plan</span></span>
1. <span data-ttu-id="3cd65-128">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="3cd65-128">Click Run.</span></span>
2. <span data-ttu-id="3cd65-129">В поле "Сводный план" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3cd65-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="3cd65-130">Выберите план, для которого настроены ограничения.</span><span class="sxs-lookup"><span data-stu-id="3cd65-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="3cd65-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3cd65-131">Click OK.</span></span>
    * <span data-ttu-id="3cd65-132">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="3cd65-132">This may take a while.</span></span>  
4. <span data-ttu-id="3cd65-133">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="3cd65-133">Click Planned orders.</span></span>


