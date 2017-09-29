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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="41ff1-103">Создание политики свертки затрат</span><span class="sxs-lookup"><span data-stu-id="41ff1-103">Create a cost rollup policy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41ff1-104">Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики.</span><span class="sxs-lookup"><span data-stu-id="41ff1-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="41ff1-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="41ff1-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="41ff1-106">Создание политики</span><span class="sxs-lookup"><span data-stu-id="41ff1-106">Create a policy</span></span>
1. <span data-ttu-id="41ff1-107">Перейдите в раздел "Учет затрат" > "Политики" > "Политики свертки затрат".</span><span class="sxs-lookup"><span data-stu-id="41ff1-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="41ff1-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="41ff1-108">Click New.</span></span>
3. <span data-ttu-id="41ff1-109">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="41ff1-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="41ff1-111">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-112">Выберите "Cost rollup CC".</span><span class="sxs-lookup"><span data-stu-id="41ff1-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="41ff1-113">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-114">Выберите "Cost rollup CC".</span><span class="sxs-lookup"><span data-stu-id="41ff1-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="41ff1-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="41ff1-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="41ff1-116">Создание правил для политики свертки затрат</span><span class="sxs-lookup"><span data-stu-id="41ff1-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="41ff1-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="41ff1-117">Click New.</span></span>
2. <span data-ttu-id="41ff1-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="41ff1-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="41ff1-119">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-120">Вы6ерите "007".</span><span class="sxs-lookup"><span data-stu-id="41ff1-120">Select 007.</span></span>  
4. <span data-ttu-id="41ff1-121">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-122">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="41ff1-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="41ff1-123">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-124">В этом примере сопоставьте элемент вторичных затрат CC-007 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="41ff1-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="41ff1-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="41ff1-125">Click New.</span></span>
7. <span data-ttu-id="41ff1-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="41ff1-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="41ff1-127">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-128">Вы6ерите "008".</span><span class="sxs-lookup"><span data-stu-id="41ff1-128">Select 008.</span></span>  
9. <span data-ttu-id="41ff1-129">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-130">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="41ff1-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="41ff1-131">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-132">В этом примере сопоставьте элемент вторичных затрат CC-008 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="41ff1-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="41ff1-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="41ff1-133">Click New.</span></span>
12. <span data-ttu-id="41ff1-134">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="41ff1-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="41ff1-135">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-136">Вы6ерите "009".</span><span class="sxs-lookup"><span data-stu-id="41ff1-136">Select 009.</span></span>  
14. <span data-ttu-id="41ff1-137">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-138">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="41ff1-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="41ff1-139">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="41ff1-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="41ff1-140">В этом примере сопоставьте элемент вторичных затрат CC-009 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="41ff1-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="41ff1-141">Продолжайте, пока все центры затрат не будут сопоставлены соответствующим им элементам вторичных затрат.</span><span class="sxs-lookup"><span data-stu-id="41ff1-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="41ff1-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="41ff1-142">Click Save.</span></span>


