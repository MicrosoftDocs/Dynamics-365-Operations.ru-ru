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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568566"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="91b9b-103">Создание спецификации (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="91b9b-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91b9b-104">Эта задача рассматривает создание структуры спецификации для готовой продукции и полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="91b9b-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="91b9b-105">Это четвертая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="91b9b-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="91b9b-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="91b9b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="91b9b-107">Создание спецификации для полуфабриката</span><span class="sxs-lookup"><span data-stu-id="91b9b-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="91b9b-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="91b9b-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="91b9b-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91b9b-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="91b9b-110">Выберите код номенклатуры BOM_2.</span><span class="sxs-lookup"><span data-stu-id="91b9b-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="91b9b-111">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="91b9b-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="91b9b-112">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="91b9b-112">Click BOM versions.</span></span>
5. <span data-ttu-id="91b9b-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91b9b-113">Click New.</span></span>
6. <span data-ttu-id="91b9b-114">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="91b9b-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="91b9b-115">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="91b9b-116">Например, введите BOM_2.</span><span class="sxs-lookup"><span data-stu-id="91b9b-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="91b9b-117">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="91b9b-118">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="91b9b-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="91b9b-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91b9b-119">Click OK.</span></span>
10. <span data-ttu-id="91b9b-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91b9b-120">Click New.</span></span>
11. <span data-ttu-id="91b9b-121">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="91b9b-122">В этом примере введите "ITEM_C".</span><span class="sxs-lookup"><span data-stu-id="91b9b-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="91b9b-123">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="91b9b-124">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="91b9b-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="91b9b-125">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="91b9b-125">Click Header.</span></span>
14. <span data-ttu-id="91b9b-126">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="91b9b-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="91b9b-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91b9b-127">Click OK.</span></span>
16. <span data-ttu-id="91b9b-128">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="91b9b-128">Click Approve.</span></span>
    * <span data-ttu-id="91b9b-129">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="91b9b-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="91b9b-130">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="91b9b-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="91b9b-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91b9b-131">Click OK.</span></span>
18. <span data-ttu-id="91b9b-132">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="91b9b-132">Click Activate.</span></span>
19. <span data-ttu-id="91b9b-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91b9b-133">Close the page.</span></span>
20. <span data-ttu-id="91b9b-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91b9b-134">Close the page.</span></span>
21. <span data-ttu-id="91b9b-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91b9b-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="91b9b-136">Создание спецификации для готовой продукции</span><span class="sxs-lookup"><span data-stu-id="91b9b-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="91b9b-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91b9b-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="91b9b-138">Выберите код номенклатуры BOM_1.</span><span class="sxs-lookup"><span data-stu-id="91b9b-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="91b9b-139">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="91b9b-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="91b9b-140">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="91b9b-140">Click BOM versions.</span></span>
4. <span data-ttu-id="91b9b-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91b9b-141">Click New.</span></span>
5. <span data-ttu-id="91b9b-142">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="91b9b-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="91b9b-143">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="91b9b-144">Например, введите BOM_1.</span><span class="sxs-lookup"><span data-stu-id="91b9b-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="91b9b-145">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="91b9b-146">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="91b9b-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="91b9b-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91b9b-147">Click OK.</span></span>
9. <span data-ttu-id="91b9b-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91b9b-148">Click New.</span></span>
10. <span data-ttu-id="91b9b-149">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="91b9b-150">В этом примере введите "ITEM_A".</span><span class="sxs-lookup"><span data-stu-id="91b9b-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="91b9b-151">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="91b9b-152">В этом примере выберите "11".</span><span class="sxs-lookup"><span data-stu-id="91b9b-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="91b9b-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91b9b-153">Click New.</span></span>
13. <span data-ttu-id="91b9b-154">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="91b9b-155">В этом примере введите "ITEM_B".</span><span class="sxs-lookup"><span data-stu-id="91b9b-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="91b9b-156">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="91b9b-157">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="91b9b-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="91b9b-158">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91b9b-158">Click New.</span></span>
16. <span data-ttu-id="91b9b-159">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="91b9b-160">В этом примере введите "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="91b9b-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="91b9b-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="91b9b-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="91b9b-162">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="91b9b-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="91b9b-163">В этом примере введите или выберите склад 11.</span><span class="sxs-lookup"><span data-stu-id="91b9b-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="91b9b-164">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="91b9b-164">Click Header.</span></span>
20. <span data-ttu-id="91b9b-165">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="91b9b-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="91b9b-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91b9b-166">Click OK.</span></span>
22. <span data-ttu-id="91b9b-167">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="91b9b-167">Click Approve.</span></span>
    * <span data-ttu-id="91b9b-168">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="91b9b-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="91b9b-169">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="91b9b-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="91b9b-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91b9b-170">Click OK.</span></span>
24. <span data-ttu-id="91b9b-171">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="91b9b-171">Click Activate.</span></span>
25. <span data-ttu-id="91b9b-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91b9b-172">Close the page.</span></span>
26. <span data-ttu-id="91b9b-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91b9b-173">Close the page.</span></span>
27. <span data-ttu-id="91b9b-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91b9b-174">Close the page.</span></span>

