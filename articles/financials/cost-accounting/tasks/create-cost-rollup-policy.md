--- 
title: "Создание политики свертки затрат"
description: "Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 165d12efe1e3caf436a7573936e94203bad88330
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="1389d-103">Создание политики свертки затрат</span><span class="sxs-lookup"><span data-stu-id="1389d-103">Create a cost rollup policy</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1389d-104">Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики.</span><span class="sxs-lookup"><span data-stu-id="1389d-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="1389d-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="1389d-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="1389d-106">Создание политики</span><span class="sxs-lookup"><span data-stu-id="1389d-106">Create a policy</span></span>
1. <span data-ttu-id="1389d-107">Перейдите в раздел "Учет затрат" > "Политики" > "Политики свертки затрат".</span><span class="sxs-lookup"><span data-stu-id="1389d-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="1389d-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1389d-108">Click New.</span></span>
3. <span data-ttu-id="1389d-109">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="1389d-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1389d-111">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-112">Выберите "Cost rollup CC".</span><span class="sxs-lookup"><span data-stu-id="1389d-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="1389d-113">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-114">Выберите "Cost rollup CC".</span><span class="sxs-lookup"><span data-stu-id="1389d-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="1389d-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1389d-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="1389d-116">Создание правил для политики свертки затрат</span><span class="sxs-lookup"><span data-stu-id="1389d-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="1389d-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1389d-117">Click New.</span></span>
2. <span data-ttu-id="1389d-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1389d-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="1389d-119">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-120">Вы6ерите "007".</span><span class="sxs-lookup"><span data-stu-id="1389d-120">Select 007.</span></span>  
4. <span data-ttu-id="1389d-121">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-122">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="1389d-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="1389d-123">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-124">В этом примере сопоставьте элемент вторичных затрат CC-007 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="1389d-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="1389d-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1389d-125">Click New.</span></span>
7. <span data-ttu-id="1389d-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1389d-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1389d-127">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-128">Вы6ерите "008".</span><span class="sxs-lookup"><span data-stu-id="1389d-128">Select 008.</span></span>  
9. <span data-ttu-id="1389d-129">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-130">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="1389d-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="1389d-131">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-132">В этом примере сопоставьте элемент вторичных затрат CC-008 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="1389d-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="1389d-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1389d-133">Click New.</span></span>
12. <span data-ttu-id="1389d-134">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1389d-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1389d-135">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-136">Вы6ерите "009".</span><span class="sxs-lookup"><span data-stu-id="1389d-136">Select 009.</span></span>  
14. <span data-ttu-id="1389d-137">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-138">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="1389d-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="1389d-139">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1389d-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="1389d-140">В этом примере сопоставьте элемент вторичных затрат CC-009 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="1389d-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="1389d-141">Продолжайте, пока все центры затрат не будут сопоставлены соответствующим им элементам вторичных затрат.</span><span class="sxs-lookup"><span data-stu-id="1389d-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="1389d-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1389d-142">Click Save.</span></span>


