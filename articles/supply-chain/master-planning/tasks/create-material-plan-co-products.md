---
title: Создание плана материалов для сопутствующих продуктов
description: Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556008"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="2af25-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="2af25-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2af25-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="2af25-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="2af25-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="2af25-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="2af25-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="2af25-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="2af25-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2af25-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="2af25-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="2af25-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="2af25-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="2af25-109">Click New.</span></span>
4. <span data-ttu-id="2af25-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="2af25-110">Click Sales order.</span></span>
5. <span data-ttu-id="2af25-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2af25-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="2af25-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="2af25-112">Example: US-001</span></span>  
6. <span data-ttu-id="2af25-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2af25-113">Click OK.</span></span>
7. <span data-ttu-id="2af25-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2af25-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2af25-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="2af25-115">Example: P6003</span></span>  
8. <span data-ttu-id="2af25-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="2af25-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2af25-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="2af25-117">Example: 50000</span></span>  
9. <span data-ttu-id="2af25-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2af25-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="2af25-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="2af25-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="2af25-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2af25-120">Close the page.</span></span>
2. <span data-ttu-id="2af25-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2af25-121">Close the page.</span></span>
3. <span data-ttu-id="2af25-122">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="2af25-122">Click Master planning.</span></span>
4. <span data-ttu-id="2af25-123">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2af25-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2af25-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2af25-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2af25-125">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="2af25-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="2af25-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="2af25-126">Click Run.</span></span>
7. <span data-ttu-id="2af25-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="2af25-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="2af25-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="2af25-128">Click Filter.</span></span>
9. <span data-ttu-id="2af25-129">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="2af25-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="2af25-130">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2af25-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="2af25-131">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="2af25-131">Example: P6003</span></span>  
11. <span data-ttu-id="2af25-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2af25-132">Click OK.</span></span>
12. <span data-ttu-id="2af25-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2af25-133">Click OK.</span></span>
13. <span data-ttu-id="2af25-134">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="2af25-134">Click Planned orders.</span></span>
14. <span data-ttu-id="2af25-135">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="2af25-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2af25-136">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="2af25-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="2af25-137">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="2af25-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="2af25-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2af25-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2af25-139">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="2af25-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="2af25-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2af25-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2af25-141">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="2af25-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="2af25-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2af25-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2af25-143">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="2af25-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="2af25-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2af25-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="2af25-145">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="2af25-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="2af25-146">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2af25-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="2af25-147">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="2af25-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="2af25-148">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="2af25-148">Click New.</span></span>
4. <span data-ttu-id="2af25-149">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="2af25-149">Click Sales order.</span></span>
5. <span data-ttu-id="2af25-150">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2af25-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="2af25-151">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="2af25-151">Example: US-001</span></span>  
6. <span data-ttu-id="2af25-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2af25-152">Click OK.</span></span>
7. <span data-ttu-id="2af25-153">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2af25-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2af25-154">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="2af25-154">Example: P6003</span></span>  
8. <span data-ttu-id="2af25-155">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="2af25-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2af25-156">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="2af25-156">Example: 50000</span></span>  
9. <span data-ttu-id="2af25-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2af25-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="2af25-158">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="2af25-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="2af25-159">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2af25-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="2af25-160">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2af25-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2af25-161">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="2af25-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="2af25-162">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="2af25-162">Click Run.</span></span>
4. <span data-ttu-id="2af25-163">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="2af25-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="2af25-164">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="2af25-164">Click Filter.</span></span>
6. <span data-ttu-id="2af25-165">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="2af25-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="2af25-166">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2af25-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="2af25-167">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="2af25-167">Example: P6003</span></span>  
8. <span data-ttu-id="2af25-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2af25-168">Click OK.</span></span>
9. <span data-ttu-id="2af25-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2af25-169">Click OK.</span></span>
10. <span data-ttu-id="2af25-170">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="2af25-170">Click Planned orders.</span></span>
11. <span data-ttu-id="2af25-171">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="2af25-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2af25-172">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="2af25-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="2af25-173">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="2af25-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="2af25-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2af25-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2af25-175">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="2af25-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="2af25-176">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2af25-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2af25-177">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="2af25-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="2af25-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2af25-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2af25-179">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="2af25-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="2af25-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2af25-180">Close the page.</span></span>
17. <span data-ttu-id="2af25-181">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="2af25-181">Click Master planning.</span></span>
18. <span data-ttu-id="2af25-182">Перейдите в раздел "Сводное планирование" > "Настройка" > "Параметры сводного планирования".</span><span class="sxs-lookup"><span data-stu-id="2af25-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="2af25-183">Выберите "Нет" в поле "Отключить все процессы планирования".</span><span class="sxs-lookup"><span data-stu-id="2af25-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="2af25-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2af25-184">Close the page.</span></span>

