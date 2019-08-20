---
title: Создание политики свертки затрат
description: Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841233"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="4ee6e-103">Создание политики свертки затрат</span><span class="sxs-lookup"><span data-stu-id="4ee6e-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ee6e-104">Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="4ee6e-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="4ee6e-106">Создание политики</span><span class="sxs-lookup"><span data-stu-id="4ee6e-106">Create a policy</span></span>
1. <span data-ttu-id="4ee6e-107">Перейдите в раздел "Учет затрат" > "Политики" > "Политики свертки затрат".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="4ee6e-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-108">Click New.</span></span>
3. <span data-ttu-id="4ee6e-109">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4ee6e-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4ee6e-111">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-112">Выберите "Cost rollup CC".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="4ee6e-113">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-114">Выберите "Cost rollup CC".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="4ee6e-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="4ee6e-116">Создание правил для политики свертки затрат</span><span class="sxs-lookup"><span data-stu-id="4ee6e-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="4ee6e-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-117">Click New.</span></span>
2. <span data-ttu-id="4ee6e-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4ee6e-119">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-120">Вы6ерите "007".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-120">Select 007.</span></span>  
4. <span data-ttu-id="4ee6e-121">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-122">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="4ee6e-123">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-124">В этом примере сопоставьте элемент вторичных затрат CC-007 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="4ee6e-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-125">Click New.</span></span>
7. <span data-ttu-id="4ee6e-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4ee6e-127">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-128">Вы6ерите "008".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-128">Select 008.</span></span>  
9. <span data-ttu-id="4ee6e-129">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-130">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="4ee6e-131">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-132">В этом примере сопоставьте элемент вторичных затрат CC-008 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="4ee6e-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-133">Click New.</span></span>
12. <span data-ttu-id="4ee6e-134">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="4ee6e-135">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-136">Вы6ерите "009".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-136">Select 009.</span></span>  
14. <span data-ttu-id="4ee6e-137">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-138">Выберите "Cost rollup CE".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="4ee6e-139">В поле "Элемент вторичных затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="4ee6e-140">В этом примере сопоставьте элемент вторичных затрат CC-009 центру затрат.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="4ee6e-141">Продолжайте, пока все центры затрат не будут сопоставлены соответствующим им элементам вторичных затрат.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="4ee6e-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4ee6e-142">Click Save.</span></span>

