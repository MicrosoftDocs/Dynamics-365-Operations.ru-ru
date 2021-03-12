---
title: Создание плана материалов для сопутствующих продуктов
description: Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8e9067cdd8851da31c07a92217001e447f400d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983399"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8fc4c-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="8fc4c-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fc4c-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="8fc4c-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8fc4c-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="8fc4c-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8fc4c-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8fc4c-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8fc4c-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-109">Click New.</span></span>
4. <span data-ttu-id="8fc4c-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-110">Click Sales order.</span></span>
5. <span data-ttu-id="8fc4c-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8fc4c-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="8fc4c-112">Example: US-001</span></span>  
6. <span data-ttu-id="8fc4c-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-113">Click OK.</span></span>
7. <span data-ttu-id="8fc4c-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8fc4c-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="8fc4c-115">Example: P6003</span></span>  
8. <span data-ttu-id="8fc4c-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8fc4c-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="8fc4c-117">Example: 50000</span></span>  
9. <span data-ttu-id="8fc4c-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8fc4c-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="8fc4c-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8fc4c-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-120">Close the page.</span></span>
2. <span data-ttu-id="8fc4c-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-121">Close the page.</span></span>
3. <span data-ttu-id="8fc4c-122">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-122">Click Master planning.</span></span>
4. <span data-ttu-id="8fc4c-123">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8fc4c-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8fc4c-125">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8fc4c-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="8fc4c-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-126">Click Run.</span></span>
7. <span data-ttu-id="8fc4c-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="8fc4c-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-128">Click Filter.</span></span>
9. <span data-ttu-id="8fc4c-129">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="8fc4c-130">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8fc4c-131">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="8fc4c-131">Example: P6003</span></span>  
11. <span data-ttu-id="8fc4c-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-132">Click OK.</span></span>
12. <span data-ttu-id="8fc4c-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-133">Click OK.</span></span>
13. <span data-ttu-id="8fc4c-134">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-134">Click Planned orders.</span></span>
14. <span data-ttu-id="8fc4c-135">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8fc4c-136">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8fc4c-137">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="8fc4c-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8fc4c-139">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="8fc4c-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="8fc4c-141">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="8fc4c-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8fc4c-143">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="8fc4c-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8fc4c-145">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="8fc4c-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8fc4c-146">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8fc4c-147">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8fc4c-148">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-148">Click New.</span></span>
4. <span data-ttu-id="8fc4c-149">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-149">Click Sales order.</span></span>
5. <span data-ttu-id="8fc4c-150">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8fc4c-151">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="8fc4c-151">Example: US-001</span></span>  
6. <span data-ttu-id="8fc4c-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-152">Click OK.</span></span>
7. <span data-ttu-id="8fc4c-153">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8fc4c-154">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="8fc4c-154">Example: P6003</span></span>  
8. <span data-ttu-id="8fc4c-155">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8fc4c-156">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="8fc4c-156">Example: 50000</span></span>  
9. <span data-ttu-id="8fc4c-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8fc4c-158">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="8fc4c-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8fc4c-159">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="8fc4c-160">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8fc4c-161">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8fc4c-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="8fc4c-162">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-162">Click Run.</span></span>
4. <span data-ttu-id="8fc4c-163">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="8fc4c-164">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-164">Click Filter.</span></span>
6. <span data-ttu-id="8fc4c-165">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="8fc4c-166">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8fc4c-167">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="8fc4c-167">Example: P6003</span></span>  
8. <span data-ttu-id="8fc4c-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-168">Click OK.</span></span>
9. <span data-ttu-id="8fc4c-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-169">Click OK.</span></span>
10. <span data-ttu-id="8fc4c-170">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-170">Click Planned orders.</span></span>
11. <span data-ttu-id="8fc4c-171">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8fc4c-172">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8fc4c-173">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="8fc4c-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8fc4c-175">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="8fc4c-176">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8fc4c-177">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="8fc4c-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8fc4c-179">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="8fc4c-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-180">Close the page.</span></span>
17. <span data-ttu-id="8fc4c-181">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-181">Click Master planning.</span></span>
18. <span data-ttu-id="8fc4c-182">Перейдите в раздел "Сводное планирование" > "Настройка" > "Параметры сводного планирования".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="8fc4c-183">Выберите "Нет" в поле "Отключить все процессы планирования".</span><span class="sxs-lookup"><span data-stu-id="8fc4c-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="8fc4c-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-184">Close the page.</span></span>

