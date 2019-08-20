---
title: Создание спецификации (февраль 2016 г.)
description: Эта задача рассматривает создание структуры спецификации для готовой продукции и полуфабриката.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0087c53d9cdc3bb65e6fa446c193c752d0f9b4fc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845097"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="8f669-103">Создание спецификации (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="8f669-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f669-104">Эта задача рассматривает создание структуры спецификации для готовой продукции и полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="8f669-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="8f669-105">Это четвертая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="8f669-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="8f669-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="8f669-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="8f669-107">Создание спецификации для полуфабриката</span><span class="sxs-lookup"><span data-stu-id="8f669-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="8f669-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="8f669-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="8f669-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8f669-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8f669-110">Выберите код номенклатуры BOM_2.</span><span class="sxs-lookup"><span data-stu-id="8f669-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="8f669-111">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="8f669-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="8f669-112">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="8f669-112">Click BOM versions.</span></span>
5. <span data-ttu-id="8f669-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f669-113">Click New.</span></span>
6. <span data-ttu-id="8f669-114">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="8f669-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="8f669-115">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8f669-116">Например, введите BOM_2.</span><span class="sxs-lookup"><span data-stu-id="8f669-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="8f669-117">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="8f669-118">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="8f669-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="8f669-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8f669-119">Click OK.</span></span>
10. <span data-ttu-id="8f669-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f669-120">Click New.</span></span>
11. <span data-ttu-id="8f669-121">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8f669-122">В этом примере введите "ITEM_C".</span><span class="sxs-lookup"><span data-stu-id="8f669-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="8f669-123">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8f669-124">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="8f669-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="8f669-125">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="8f669-125">Click Header.</span></span>
14. <span data-ttu-id="8f669-126">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="8f669-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="8f669-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8f669-127">Click OK.</span></span>
16. <span data-ttu-id="8f669-128">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="8f669-128">Click Approve.</span></span>
    * <span data-ttu-id="8f669-129">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="8f669-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="8f669-130">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="8f669-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="8f669-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8f669-131">Click OK.</span></span>
18. <span data-ttu-id="8f669-132">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="8f669-132">Click Activate.</span></span>
19. <span data-ttu-id="8f669-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f669-133">Close the page.</span></span>
20. <span data-ttu-id="8f669-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f669-134">Close the page.</span></span>
21. <span data-ttu-id="8f669-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f669-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="8f669-136">Создание спецификации для готовой продукции</span><span class="sxs-lookup"><span data-stu-id="8f669-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="8f669-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8f669-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8f669-138">Выберите код номенклатуры BOM_1.</span><span class="sxs-lookup"><span data-stu-id="8f669-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="8f669-139">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="8f669-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="8f669-140">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="8f669-140">Click BOM versions.</span></span>
4. <span data-ttu-id="8f669-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f669-141">Click New.</span></span>
5. <span data-ttu-id="8f669-142">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="8f669-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="8f669-143">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8f669-144">Например, введите BOM_1.</span><span class="sxs-lookup"><span data-stu-id="8f669-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="8f669-145">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="8f669-146">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="8f669-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="8f669-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8f669-147">Click OK.</span></span>
9. <span data-ttu-id="8f669-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f669-148">Click New.</span></span>
10. <span data-ttu-id="8f669-149">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8f669-150">В этом примере введите "ITEM_A".</span><span class="sxs-lookup"><span data-stu-id="8f669-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="8f669-151">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8f669-152">В этом примере выберите "11".</span><span class="sxs-lookup"><span data-stu-id="8f669-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="8f669-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f669-153">Click New.</span></span>
13. <span data-ttu-id="8f669-154">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8f669-155">В этом примере введите "ITEM_B".</span><span class="sxs-lookup"><span data-stu-id="8f669-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="8f669-156">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8f669-157">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="8f669-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="8f669-158">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f669-158">Click New.</span></span>
16. <span data-ttu-id="8f669-159">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8f669-160">В этом примере введите "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="8f669-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="8f669-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8f669-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="8f669-162">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8f669-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8f669-163">В этом примере введите или выберите склад 11.</span><span class="sxs-lookup"><span data-stu-id="8f669-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="8f669-164">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="8f669-164">Click Header.</span></span>
20. <span data-ttu-id="8f669-165">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="8f669-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="8f669-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8f669-166">Click OK.</span></span>
22. <span data-ttu-id="8f669-167">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="8f669-167">Click Approve.</span></span>
    * <span data-ttu-id="8f669-168">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="8f669-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="8f669-169">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="8f669-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="8f669-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8f669-170">Click OK.</span></span>
24. <span data-ttu-id="8f669-171">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="8f669-171">Click Activate.</span></span>
25. <span data-ttu-id="8f669-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f669-172">Close the page.</span></span>
26. <span data-ttu-id="8f669-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f669-173">Close the page.</span></span>
27. <span data-ttu-id="8f669-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f669-174">Close the page.</span></span>

