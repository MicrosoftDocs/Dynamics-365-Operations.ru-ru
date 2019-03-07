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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "333216"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="994a9-103">Создание спецификации (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="994a9-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="994a9-104">Эта задача рассматривает создание структуры спецификации для готовой продукции и полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="994a9-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="994a9-105">Это четвертая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="994a9-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="994a9-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="994a9-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="994a9-107">Создание спецификации для полуфабриката</span><span class="sxs-lookup"><span data-stu-id="994a9-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="994a9-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="994a9-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="994a9-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="994a9-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="994a9-110">Выберите код номенклатуры BOM_2.</span><span class="sxs-lookup"><span data-stu-id="994a9-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="994a9-111">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="994a9-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="994a9-112">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="994a9-112">Click BOM versions.</span></span>
5. <span data-ttu-id="994a9-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994a9-113">Click New.</span></span>
6. <span data-ttu-id="994a9-114">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="994a9-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="994a9-115">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="994a9-116">Например, введите BOM_2.</span><span class="sxs-lookup"><span data-stu-id="994a9-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="994a9-117">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="994a9-118">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="994a9-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="994a9-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="994a9-119">Click OK.</span></span>
10. <span data-ttu-id="994a9-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994a9-120">Click New.</span></span>
11. <span data-ttu-id="994a9-121">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="994a9-122">В этом примере введите "ITEM_C".</span><span class="sxs-lookup"><span data-stu-id="994a9-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="994a9-123">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="994a9-124">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="994a9-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="994a9-125">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="994a9-125">Click Header.</span></span>
14. <span data-ttu-id="994a9-126">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="994a9-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="994a9-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="994a9-127">Click OK.</span></span>
16. <span data-ttu-id="994a9-128">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="994a9-128">Click Approve.</span></span>
    * <span data-ttu-id="994a9-129">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="994a9-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="994a9-130">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="994a9-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="994a9-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="994a9-131">Click OK.</span></span>
18. <span data-ttu-id="994a9-132">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="994a9-132">Click Activate.</span></span>
19. <span data-ttu-id="994a9-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="994a9-133">Close the page.</span></span>
20. <span data-ttu-id="994a9-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="994a9-134">Close the page.</span></span>
21. <span data-ttu-id="994a9-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="994a9-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="994a9-136">Создание спецификации для готовой продукции</span><span class="sxs-lookup"><span data-stu-id="994a9-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="994a9-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="994a9-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="994a9-138">Выберите код номенклатуры BOM_1.</span><span class="sxs-lookup"><span data-stu-id="994a9-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="994a9-139">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="994a9-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="994a9-140">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="994a9-140">Click BOM versions.</span></span>
4. <span data-ttu-id="994a9-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994a9-141">Click New.</span></span>
5. <span data-ttu-id="994a9-142">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="994a9-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="994a9-143">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="994a9-144">Например, введите BOM_1.</span><span class="sxs-lookup"><span data-stu-id="994a9-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="994a9-145">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="994a9-146">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="994a9-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="994a9-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="994a9-147">Click OK.</span></span>
9. <span data-ttu-id="994a9-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994a9-148">Click New.</span></span>
10. <span data-ttu-id="994a9-149">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="994a9-150">В этом примере введите "ITEM_A".</span><span class="sxs-lookup"><span data-stu-id="994a9-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="994a9-151">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="994a9-152">В этом примере выберите "11".</span><span class="sxs-lookup"><span data-stu-id="994a9-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="994a9-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994a9-153">Click New.</span></span>
13. <span data-ttu-id="994a9-154">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="994a9-155">В этом примере введите "ITEM_B".</span><span class="sxs-lookup"><span data-stu-id="994a9-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="994a9-156">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="994a9-157">В этом примере введите или выберите "11".</span><span class="sxs-lookup"><span data-stu-id="994a9-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="994a9-158">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994a9-158">Click New.</span></span>
16. <span data-ttu-id="994a9-159">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="994a9-160">В этом примере введите "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="994a9-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="994a9-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="994a9-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="994a9-162">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="994a9-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="994a9-163">В этом примере введите или выберите склад 11.</span><span class="sxs-lookup"><span data-stu-id="994a9-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="994a9-164">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="994a9-164">Click Header.</span></span>
20. <span data-ttu-id="994a9-165">Щелкните "Утвердить" для утверждения спецификаций.</span><span class="sxs-lookup"><span data-stu-id="994a9-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="994a9-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="994a9-166">Click OK.</span></span>
22. <span data-ttu-id="994a9-167">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="994a9-167">Click Approve.</span></span>
    * <span data-ttu-id="994a9-168">Кнопка "Утвердить" расположена на панели инструментов в разделе "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="994a9-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="994a9-169">Если она не отображается, щелкните заголовок в верхнем правом углу страницы "Спецификации" для отображения кнопки "Утвердить".</span><span class="sxs-lookup"><span data-stu-id="994a9-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="994a9-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="994a9-170">Click OK.</span></span>
24. <span data-ttu-id="994a9-171">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="994a9-171">Click Activate.</span></span>
25. <span data-ttu-id="994a9-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="994a9-172">Close the page.</span></span>
26. <span data-ttu-id="994a9-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="994a9-173">Close the page.</span></span>
27. <span data-ttu-id="994a9-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="994a9-174">Close the page.</span></span>

