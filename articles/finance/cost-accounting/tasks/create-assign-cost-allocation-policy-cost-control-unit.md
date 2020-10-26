---
title: Создание и назначение политик распределения затрат единицам управления затратами
description: Эта процедура используется для создания политики распределения затрат с соответствующими правилами и ее назначения единице управления затратами.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad95752ce40faaa84747dac9bfbf2887f7a5af42
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976219"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="fbc93-103">Создание и назначение политик распределения затрат единицам управления затратами</span><span class="sxs-lookup"><span data-stu-id="fbc93-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbc93-104">Эта процедура используется для создания политики распределения затрат с соответствующими правилами и ее назначения единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="fbc93-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="fbc93-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="fbc93-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="fbc93-106">Создание политики</span><span class="sxs-lookup"><span data-stu-id="fbc93-106">Create a policy</span></span>
1. <span data-ttu-id="fbc93-107">Перейдите в раздел "Учет затрат" > "Политики" > "Политики распределения затрат".</span><span class="sxs-lookup"><span data-stu-id="fbc93-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="fbc93-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fbc93-108">Click New.</span></span>
3. <span data-ttu-id="fbc93-109">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="fbc93-110">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fbc93-111">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="fbc93-111">Select Organization.</span></span>  
5. <span data-ttu-id="fbc93-112">В поле "Статистическая аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="fbc93-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fbc93-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="fbc93-114">Создание правил распределения</span><span class="sxs-lookup"><span data-stu-id="fbc93-114">Create allocation rules</span></span>
1. <span data-ttu-id="fbc93-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fbc93-115">Click New.</span></span>
2. <span data-ttu-id="fbc93-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fbc93-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="fbc93-117">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="fbc93-118">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="fbc93-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="fbc93-119">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="fbc93-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fbc93-120">Click New.</span></span>
7. <span data-ttu-id="fbc93-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fbc93-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fbc93-122">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="fbc93-123">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="fbc93-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="fbc93-124">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="fbc93-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fbc93-125">Click New.</span></span>
12. <span data-ttu-id="fbc93-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fbc93-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fbc93-127">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="fbc93-128">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="fbc93-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="fbc93-129">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="fbc93-130">Продолжайте, пока не будут созданы все правила.</span><span class="sxs-lookup"><span data-stu-id="fbc93-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="fbc93-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fbc93-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="fbc93-132">Назначение политики единице управления затратами</span><span class="sxs-lookup"><span data-stu-id="fbc93-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="fbc93-133">Щелкните "Назначения политики для единицы управления затратами".</span><span class="sxs-lookup"><span data-stu-id="fbc93-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="fbc93-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fbc93-134">Click New.</span></span>
3. <span data-ttu-id="fbc93-135">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fbc93-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fbc93-136">В поле "Действительно с даты учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="fbc93-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="fbc93-137">Правила вступают в силу по дате.</span><span class="sxs-lookup"><span data-stu-id="fbc93-137">The rules are date-effective.</span></span> <span data-ttu-id="fbc93-138">Пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.</span><span class="sxs-lookup"><span data-stu-id="fbc93-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="fbc93-139">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fbc93-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="fbc93-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fbc93-140">Click Save.</span></span>

