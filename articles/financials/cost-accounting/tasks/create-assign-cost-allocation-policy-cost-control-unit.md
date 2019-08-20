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
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841401"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="31f38-103">Создание и назначение политик распределения затрат единицам управления затратами</span><span class="sxs-lookup"><span data-stu-id="31f38-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31f38-104">Эта процедура используется для создания политики распределения затрат с соответствующими правилами и ее назначения единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="31f38-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="31f38-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="31f38-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="31f38-106">Создание политики</span><span class="sxs-lookup"><span data-stu-id="31f38-106">Create a policy</span></span>
1. <span data-ttu-id="31f38-107">Перейдите в раздел "Учет затрат" > "Политики" > "Политики распределения затрат".</span><span class="sxs-lookup"><span data-stu-id="31f38-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="31f38-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31f38-108">Click New.</span></span>
3. <span data-ttu-id="31f38-109">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="31f38-110">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="31f38-111">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="31f38-111">Select Organization.</span></span>  
5. <span data-ttu-id="31f38-112">В поле "Статистическая аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="31f38-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31f38-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="31f38-114">Создание правил распределения</span><span class="sxs-lookup"><span data-stu-id="31f38-114">Create allocation rules</span></span>
1. <span data-ttu-id="31f38-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31f38-115">Click New.</span></span>
2. <span data-ttu-id="31f38-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="31f38-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="31f38-117">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="31f38-118">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="31f38-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="31f38-119">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="31f38-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31f38-120">Click New.</span></span>
7. <span data-ttu-id="31f38-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="31f38-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="31f38-122">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="31f38-123">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="31f38-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="31f38-124">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="31f38-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31f38-125">Click New.</span></span>
12. <span data-ttu-id="31f38-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="31f38-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="31f38-127">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="31f38-128">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="31f38-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="31f38-129">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="31f38-130">Продолжайте, пока не будут созданы все правила.</span><span class="sxs-lookup"><span data-stu-id="31f38-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="31f38-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31f38-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="31f38-132">Назначение политики единице управления затратами</span><span class="sxs-lookup"><span data-stu-id="31f38-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="31f38-133">Щелкните "Назначения политики для единицы управления затратами".</span><span class="sxs-lookup"><span data-stu-id="31f38-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="31f38-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31f38-134">Click New.</span></span>
3. <span data-ttu-id="31f38-135">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="31f38-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="31f38-136">В поле "Действительно с даты учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="31f38-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="31f38-137">Правила вступают в силу по дате.</span><span class="sxs-lookup"><span data-stu-id="31f38-137">The rules are date-effective.</span></span> <span data-ttu-id="31f38-138">Пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.</span><span class="sxs-lookup"><span data-stu-id="31f38-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="31f38-139">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31f38-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="31f38-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31f38-140">Click Save.</span></span>

