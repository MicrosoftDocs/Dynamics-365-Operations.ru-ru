--- 
title: "Создание спецификаций (только для версии от февраля 2016 г.)"
description: "Эта задача рассматривает создание структуры спецификации для готовой продукции и полуфабриката."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e089c105a48924d8cb42f34d711125b157c3af2e
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="1a9d2-103">Создание спецификаций (только для версии от февраля 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="1a9d2-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a9d2-104">Эта задача рассматривает создание структуры спецификации для готовой продукции и полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="1a9d2-105">Это четвертая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="1a9d2-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="1a9d2-107">Создание спецификации для полуфабриката</span><span class="sxs-lookup"><span data-stu-id="1a9d2-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="1a9d2-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="1a9d2-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1a9d2-110">Выберите код номенклатуры BOM_2.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="1a9d2-111">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="1a9d2-112">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-112">Click BOM versions.</span></span>
5. <span data-ttu-id="1a9d2-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-113">Click New.</span></span>
6. <span data-ttu-id="1a9d2-114">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="1a9d2-115">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1a9d2-116">Например, введите BOM_2.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="1a9d2-117">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="1a9d2-118">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="1a9d2-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-119">Click OK.</span></span>
10. <span data-ttu-id="1a9d2-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-120">Click New.</span></span>
11. <span data-ttu-id="1a9d2-121">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1a9d2-122">В этом примере введите "ITEM_C".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="1a9d2-123">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1a9d2-124">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="1a9d2-125">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-125">Click Header.</span></span>
14. <span data-ttu-id="1a9d2-126">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="1a9d2-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-127">Click OK.</span></span>
16. <span data-ttu-id="1a9d2-128">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-128">Click Approve.</span></span>
    * <span data-ttu-id="1a9d2-129">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="1a9d2-130">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="1a9d2-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-131">Click OK.</span></span>
18. <span data-ttu-id="1a9d2-132">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-132">Click Activate.</span></span>
19. <span data-ttu-id="1a9d2-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-133">Close the page.</span></span>
20. <span data-ttu-id="1a9d2-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-134">Close the page.</span></span>
21. <span data-ttu-id="1a9d2-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="1a9d2-136">Создание спецификации для готовой продукции</span><span class="sxs-lookup"><span data-stu-id="1a9d2-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="1a9d2-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1a9d2-138">Выберите код номенклатуры BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="1a9d2-139">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="1a9d2-140">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-140">Click BOM versions.</span></span>
4. <span data-ttu-id="1a9d2-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-141">Click New.</span></span>
5. <span data-ttu-id="1a9d2-142">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="1a9d2-143">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1a9d2-144">Например, введите BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="1a9d2-145">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="1a9d2-146">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="1a9d2-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-147">Click OK.</span></span>
9. <span data-ttu-id="1a9d2-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-148">Click New.</span></span>
10. <span data-ttu-id="1a9d2-149">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1a9d2-150">В этом примере введите "ITEM_A".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="1a9d2-151">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1a9d2-152">В этом примере выберите "11".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="1a9d2-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-153">Click New.</span></span>
13. <span data-ttu-id="1a9d2-154">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1a9d2-155">В этом примере введите "ITEM_B".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="1a9d2-156">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1a9d2-157">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="1a9d2-158">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-158">Click New.</span></span>
16. <span data-ttu-id="1a9d2-159">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1a9d2-160">В этом примере введите "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="1a9d2-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="1a9d2-162">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1a9d2-163">В этом примере введите или выберите склад 11.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="1a9d2-164">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-164">Click Header.</span></span>
20. <span data-ttu-id="1a9d2-165">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="1a9d2-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-166">Click OK.</span></span>
22. <span data-ttu-id="1a9d2-167">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-167">Click Approve.</span></span>
    * <span data-ttu-id="1a9d2-168">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="1a9d2-169">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="1a9d2-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1a9d2-170">Click OK.</span></span>
24. <span data-ttu-id="1a9d2-171">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-171">Click Activate.</span></span>
25. <span data-ttu-id="1a9d2-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-172">Close the page.</span></span>
26. <span data-ttu-id="1a9d2-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-173">Close the page.</span></span>
27. <span data-ttu-id="1a9d2-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a9d2-174">Close the page.</span></span>


