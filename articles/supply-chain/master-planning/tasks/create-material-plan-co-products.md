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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148086"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="64385-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="64385-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64385-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="64385-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="64385-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="64385-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="64385-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="64385-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="64385-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64385-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="64385-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="64385-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="64385-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="64385-109">Click New.</span></span>
4. <span data-ttu-id="64385-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="64385-110">Click Sales order.</span></span>
5. <span data-ttu-id="64385-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64385-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="64385-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="64385-112">Example: US-001</span></span>  
6. <span data-ttu-id="64385-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64385-113">Click OK.</span></span>
7. <span data-ttu-id="64385-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64385-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="64385-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="64385-115">Example: P6003</span></span>  
8. <span data-ttu-id="64385-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="64385-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="64385-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="64385-117">Example: 50000</span></span>  
9. <span data-ttu-id="64385-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64385-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="64385-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="64385-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="64385-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64385-120">Close the page.</span></span>
2. <span data-ttu-id="64385-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64385-121">Close the page.</span></span>
3. <span data-ttu-id="64385-122">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="64385-122">Click Master planning.</span></span>
4. <span data-ttu-id="64385-123">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="64385-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="64385-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64385-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="64385-125">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="64385-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="64385-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="64385-126">Click Run.</span></span>
7. <span data-ttu-id="64385-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="64385-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="64385-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="64385-128">Click Filter.</span></span>
9. <span data-ttu-id="64385-129">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="64385-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="64385-130">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64385-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="64385-131">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="64385-131">Example: P6003</span></span>  
11. <span data-ttu-id="64385-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64385-132">Click OK.</span></span>
12. <span data-ttu-id="64385-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64385-133">Click OK.</span></span>
13. <span data-ttu-id="64385-134">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="64385-134">Click Planned orders.</span></span>
14. <span data-ttu-id="64385-135">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="64385-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="64385-136">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="64385-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="64385-137">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="64385-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="64385-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="64385-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="64385-139">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="64385-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="64385-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64385-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="64385-141">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="64385-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="64385-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64385-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="64385-143">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="64385-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="64385-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64385-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="64385-145">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="64385-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="64385-146">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64385-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="64385-147">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="64385-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="64385-148">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="64385-148">Click New.</span></span>
4. <span data-ttu-id="64385-149">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="64385-149">Click Sales order.</span></span>
5. <span data-ttu-id="64385-150">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64385-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="64385-151">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="64385-151">Example: US-001</span></span>  
6. <span data-ttu-id="64385-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64385-152">Click OK.</span></span>
7. <span data-ttu-id="64385-153">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64385-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="64385-154">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="64385-154">Example: P6003</span></span>  
8. <span data-ttu-id="64385-155">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="64385-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="64385-156">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="64385-156">Example: 50000</span></span>  
9. <span data-ttu-id="64385-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64385-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="64385-158">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="64385-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="64385-159">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="64385-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="64385-160">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64385-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="64385-161">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="64385-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="64385-162">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="64385-162">Click Run.</span></span>
4. <span data-ttu-id="64385-163">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="64385-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="64385-164">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="64385-164">Click Filter.</span></span>
6. <span data-ttu-id="64385-165">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="64385-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="64385-166">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64385-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="64385-167">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="64385-167">Example: P6003</span></span>  
8. <span data-ttu-id="64385-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64385-168">Click OK.</span></span>
9. <span data-ttu-id="64385-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64385-169">Click OK.</span></span>
10. <span data-ttu-id="64385-170">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="64385-170">Click Planned orders.</span></span>
11. <span data-ttu-id="64385-171">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="64385-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="64385-172">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="64385-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="64385-173">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="64385-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="64385-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="64385-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="64385-175">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="64385-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="64385-176">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64385-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="64385-177">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="64385-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="64385-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64385-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="64385-179">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="64385-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="64385-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64385-180">Close the page.</span></span>
17. <span data-ttu-id="64385-181">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="64385-181">Click Master planning.</span></span>
18. <span data-ttu-id="64385-182">Перейдите в раздел "Сводное планирование" > "Настройка" > "Параметры сводного планирования".</span><span class="sxs-lookup"><span data-stu-id="64385-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="64385-183">Выберите "Нет" в поле "Отключить все процессы планирования".</span><span class="sxs-lookup"><span data-stu-id="64385-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="64385-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64385-184">Close the page.</span></span>

