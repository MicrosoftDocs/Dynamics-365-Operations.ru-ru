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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f41eb99b84bbc596e79b413971f9d92f2555b6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "324407"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="fe00c-103">Создание и назначение политик распределения затрат единицам управления затратами</span><span class="sxs-lookup"><span data-stu-id="fe00c-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe00c-104">Эта процедура используется для создания политики распределения затрат с соответствующими правилами и ее назначения единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="fe00c-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="fe00c-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="fe00c-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="fe00c-106">Создание политики</span><span class="sxs-lookup"><span data-stu-id="fe00c-106">Create a policy</span></span>
1. <span data-ttu-id="fe00c-107">Перейдите в раздел "Учет затрат" > "Политики" > "Политики распределения затрат".</span><span class="sxs-lookup"><span data-stu-id="fe00c-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="fe00c-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe00c-108">Click New.</span></span>
3. <span data-ttu-id="fe00c-109">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="fe00c-110">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fe00c-111">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="fe00c-111">Select Organization.</span></span>  
5. <span data-ttu-id="fe00c-112">В поле "Статистическая аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="fe00c-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe00c-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="fe00c-114">Создание правил распределения</span><span class="sxs-lookup"><span data-stu-id="fe00c-114">Create allocation rules</span></span>
1. <span data-ttu-id="fe00c-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe00c-115">Click New.</span></span>
2. <span data-ttu-id="fe00c-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fe00c-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="fe00c-117">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="fe00c-118">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="fe00c-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="fe00c-119">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="fe00c-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe00c-120">Click New.</span></span>
7. <span data-ttu-id="fe00c-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fe00c-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fe00c-122">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="fe00c-123">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="fe00c-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="fe00c-124">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="fe00c-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe00c-125">Click New.</span></span>
12. <span data-ttu-id="fe00c-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fe00c-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fe00c-127">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="fe00c-128">В поле "Поведение затрат" выберите вариант "Итог".</span><span class="sxs-lookup"><span data-stu-id="fe00c-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="fe00c-129">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="fe00c-130">Продолжайте, пока не будут созданы все правила.</span><span class="sxs-lookup"><span data-stu-id="fe00c-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="fe00c-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe00c-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="fe00c-132">Назначение политики единице управления затратами</span><span class="sxs-lookup"><span data-stu-id="fe00c-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="fe00c-133">Щелкните "Назначения политики для единицы управления затратами".</span><span class="sxs-lookup"><span data-stu-id="fe00c-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="fe00c-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe00c-134">Click New.</span></span>
3. <span data-ttu-id="fe00c-135">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fe00c-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fe00c-136">В поле "Действительно с даты учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="fe00c-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="fe00c-137">Правила вступают в силу по дате.</span><span class="sxs-lookup"><span data-stu-id="fe00c-137">The rules are date-effective.</span></span> <span data-ttu-id="fe00c-138">Пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.</span><span class="sxs-lookup"><span data-stu-id="fe00c-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="fe00c-139">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fe00c-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="fe00c-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe00c-140">Click Save.</span></span>

