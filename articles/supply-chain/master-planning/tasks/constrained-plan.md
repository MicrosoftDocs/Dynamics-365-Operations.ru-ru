---
title: Создание плана с ограничениями
description: Эта тема объясняет, как создать план, в котором учитываются ограничения по материалам и мощности.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 126122d7be36cf1585f372adbae3ced8d6b15134
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150363"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="c0426-103">Создание плана с ограничениями</span><span class="sxs-lookup"><span data-stu-id="c0426-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0426-104">Эта тема объясняет, как создать план, в котором учитываются ограничения по материалам и мощности.</span><span class="sxs-lookup"><span data-stu-id="c0426-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="c0426-105">План гарантирует, что производство не начнется, пока не будут доступны материалы, и что ресурсы не будут зарезервированы с превышением.</span><span class="sxs-lookup"><span data-stu-id="c0426-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="c0426-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c0426-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c0426-107">Эта процедура предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="c0426-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="c0426-108">Настройка плана с ограничениями</span><span class="sxs-lookup"><span data-stu-id="c0426-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="c0426-109">На домашней странице выберите рабочую область **Сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="c0426-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="c0426-110">Выберите **Сводное планирование** в списке ссылок в самой правой части рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c0426-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="c0426-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c0426-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="c0426-112">Пример: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="c0426-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="c0426-113">Выберите значение **Да** в поле **Ограничение по мощности**.</span><span class="sxs-lookup"><span data-stu-id="c0426-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="c0426-114">В поле **Временная граница ограничения по мощности** введите значение `30`.</span><span class="sxs-lookup"><span data-stu-id="c0426-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="c0426-115">Разверните раздел **Временные границы в днях**.</span><span class="sxs-lookup"><span data-stu-id="c0426-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="c0426-116">Выберите значение **Да** в поле **Мощность**.</span><span class="sxs-lookup"><span data-stu-id="c0426-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="c0426-117">В поле **Временная граница планирования мощности (в днях)** введите число.</span><span class="sxs-lookup"><span data-stu-id="c0426-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="c0426-118">Пример: `60`</span><span class="sxs-lookup"><span data-stu-id="c0426-118">Example: `60`</span></span>  
9. <span data-ttu-id="c0426-119">Выберите значение **Да** в поле **Рассчитанные задержки**.</span><span class="sxs-lookup"><span data-stu-id="c0426-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="c0426-120">В поле **Временная граница расчета задержек (в днях)** введите число.</span><span class="sxs-lookup"><span data-stu-id="c0426-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="c0426-121">Пример: `60`</span><span class="sxs-lookup"><span data-stu-id="c0426-121">Example: `60`</span></span> 
11. <span data-ttu-id="c0426-122">Разверните раздел **Рассчитанные задержки**.</span><span class="sxs-lookup"><span data-stu-id="c0426-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="c0426-123">Выберите значение **Да** во всех полях **Добавить рассчитанную задержку к дате потребности**.</span><span class="sxs-lookup"><span data-stu-id="c0426-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="c0426-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c0426-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="c0426-125">Создание плана с ограничениями</span><span class="sxs-lookup"><span data-stu-id="c0426-125">Create a constrained plan</span></span>
1. <span data-ttu-id="c0426-126">Выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c0426-126">Select **Run**.</span></span>
2. <span data-ttu-id="c0426-127">В поле **Сводный план** введите или выберите план, для которого были настроены ограничения.</span><span class="sxs-lookup"><span data-stu-id="c0426-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="c0426-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c0426-128">Select **OK**.</span></span>
4. <span data-ttu-id="c0426-129">Выберите **Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="c0426-129">Select **Planned orders**.</span></span>

