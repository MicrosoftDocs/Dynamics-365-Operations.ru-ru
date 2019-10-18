---
title: Создание структур счетов
description: В этом руководства рассказывается о создании структуры счета.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186264"
---
# <a name="create-account-structures"></a><span data-ttu-id="15f6f-103">Создание структур счетов</span><span class="sxs-lookup"><span data-stu-id="15f6f-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15f6f-104">В этом руководства рассказывается о создании структуры счета.</span><span class="sxs-lookup"><span data-stu-id="15f6f-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="15f6f-105">Для выполнения шагов используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="15f6f-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="15f6f-106">Выберите **Область переходов > Модули > Главная книга > План счетов > Структуры > Настройка структур счетов**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="15f6f-107">На **Панели операций** щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="15f6f-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="15f6f-108">В поле **Структура счета** введите имя для описания назначения структуры счета.</span><span class="sxs-lookup"><span data-stu-id="15f6f-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="15f6f-109">В поле **Описание** введите описание для указания назначения структуры счета.</span><span class="sxs-lookup"><span data-stu-id="15f6f-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="15f6f-110">Щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-110">Click **Create**.</span></span>
6. <span data-ttu-id="15f6f-111">В области **Сегменты и допустимые значения** щелкните **Добавить сегмент**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="15f6f-112">В списке аналитик выберите аналитику для добавления в структуру счета.</span><span class="sxs-lookup"><span data-stu-id="15f6f-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="15f6f-113">В конце списка щелкните **Добавить сегмент**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="15f6f-114">При необходимости повторите шаги с 6 по 9.</span><span class="sxs-lookup"><span data-stu-id="15f6f-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="15f6f-115">В разделе **Подробные сведения о допустимых значениях** выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="15f6f-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="15f6f-116">Например, щелкните поле **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="15f6f-117">В поле **Оператор** выберите параметр, например "находится в диапазоне и включает".</span><span class="sxs-lookup"><span data-stu-id="15f6f-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="15f6f-118">В поле **Значение** введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="15f6f-119">Например, 600000.</span><span class="sxs-lookup"><span data-stu-id="15f6f-119">For example, 600000.</span></span>  
13. <span data-ttu-id="15f6f-120">В поле **через** введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-120">In the **through** field, type a value.</span></span> <span data-ttu-id="15f6f-121">Например, 699999.</span><span class="sxs-lookup"><span data-stu-id="15f6f-121">For example, 699999.</span></span>  
14. <span data-ttu-id="15f6f-122">В разделе **Подробные сведения о допустимых значениях** щелкните **Применить**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="15f6f-123">При необходимости повторите шаги с 10 по 15.</span><span class="sxs-lookup"><span data-stu-id="15f6f-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="15f6f-124">В разделе **Подробные сведения о допустимых значениях** щелкните **Добавить новые критерии**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="15f6f-125">В поле "Оператор" выберите параметр, например "находится в диапазоне и включает".</span><span class="sxs-lookup"><span data-stu-id="15f6f-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="15f6f-126">В поле **Значение** введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="15f6f-127">Например, 033.</span><span class="sxs-lookup"><span data-stu-id="15f6f-127">For example, 033.</span></span>  
19. <span data-ttu-id="15f6f-128">В поле **через** введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-128">In the **through** field, type a value.</span></span> <span data-ttu-id="15f6f-129">Например, 034.</span><span class="sxs-lookup"><span data-stu-id="15f6f-129">For example, 034.</span></span>  
20. <span data-ttu-id="15f6f-130">Нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-130">Click **Apply**.</span></span>
21. <span data-ttu-id="15f6f-131">В сетке выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="15f6f-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="15f6f-132">Например, "Место возникновения затрат".</span><span class="sxs-lookup"><span data-stu-id="15f6f-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="15f6f-133">В поле **CostCenter** введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="15f6f-134">Например, 007..021.</span><span class="sxs-lookup"><span data-stu-id="15f6f-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="15f6f-135">В области **Сегменты и допустимые значения** щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="15f6f-136">В поле **MainAccount** введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="15f6f-137">Например, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="15f6f-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="15f6f-138">В сетке выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="15f6f-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="15f6f-139">Например, "Отдел".</span><span class="sxs-lookup"><span data-stu-id="15f6f-139">For example, Department.</span></span>  
26. <span data-ttu-id="15f6f-140">В поле "Подразделение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-140">In the Department field, type a value.</span></span> <span data-ttu-id="15f6f-141">Например, 032.</span><span class="sxs-lookup"><span data-stu-id="15f6f-141">For example, 032.</span></span>  
27. <span data-ttu-id="15f6f-142">В поле CostCenter введите значение.</span><span class="sxs-lookup"><span data-stu-id="15f6f-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="15f6f-143">Например, 086.</span><span class="sxs-lookup"><span data-stu-id="15f6f-143">For example, 086.</span></span>  
28. <span data-ttu-id="15f6f-144">В области **Панель операций** щелкните **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="15f6f-145">В области **Панель операций** щелкните **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="15f6f-146">Нажмите кнопку **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="15f6f-146">Click **Activate**.</span></span>

