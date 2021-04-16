---
title: Создание плана материалов для сопутствующих продуктов
description: Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d910b89330865b0bcf3f6cd05b761506f339a45f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841679"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="61812-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="61812-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61812-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="61812-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="61812-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="61812-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="61812-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="61812-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="61812-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61812-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="61812-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="61812-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="61812-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="61812-109">Click New.</span></span>
4. <span data-ttu-id="61812-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="61812-110">Click Sales order.</span></span>
5. <span data-ttu-id="61812-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61812-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="61812-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="61812-112">Example: US-001</span></span>  
6. <span data-ttu-id="61812-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="61812-113">Click OK.</span></span>
7. <span data-ttu-id="61812-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61812-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="61812-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="61812-115">Example: P6003</span></span>  
8. <span data-ttu-id="61812-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="61812-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="61812-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="61812-117">Example: 50000</span></span>  
9. <span data-ttu-id="61812-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="61812-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="61812-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="61812-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="61812-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61812-120">Close the page.</span></span>
2. <span data-ttu-id="61812-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61812-121">Close the page.</span></span>
3. <span data-ttu-id="61812-122">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="61812-122">Click Master planning.</span></span>
4. <span data-ttu-id="61812-123">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61812-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="61812-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61812-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="61812-125">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="61812-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="61812-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="61812-126">Click Run.</span></span>
7. <span data-ttu-id="61812-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="61812-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="61812-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="61812-128">Click Filter.</span></span>
9. <span data-ttu-id="61812-129">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="61812-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="61812-130">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61812-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="61812-131">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="61812-131">Example: P6003</span></span>  
11. <span data-ttu-id="61812-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="61812-132">Click OK.</span></span>
12. <span data-ttu-id="61812-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="61812-133">Click OK.</span></span>
13. <span data-ttu-id="61812-134">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="61812-134">Click Planned orders.</span></span>
14. <span data-ttu-id="61812-135">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="61812-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="61812-136">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="61812-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="61812-137">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="61812-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="61812-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="61812-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61812-139">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="61812-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="61812-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61812-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="61812-141">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="61812-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="61812-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61812-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="61812-143">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="61812-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="61812-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61812-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="61812-145">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="61812-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="61812-146">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61812-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="61812-147">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="61812-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="61812-148">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="61812-148">Click New.</span></span>
4. <span data-ttu-id="61812-149">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="61812-149">Click Sales order.</span></span>
5. <span data-ttu-id="61812-150">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61812-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="61812-151">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="61812-151">Example: US-001</span></span>  
6. <span data-ttu-id="61812-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="61812-152">Click OK.</span></span>
7. <span data-ttu-id="61812-153">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61812-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="61812-154">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="61812-154">Example: P6003</span></span>  
8. <span data-ttu-id="61812-155">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="61812-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="61812-156">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="61812-156">Example: 50000</span></span>  
9. <span data-ttu-id="61812-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="61812-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="61812-158">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="61812-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="61812-159">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61812-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="61812-160">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61812-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="61812-161">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="61812-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="61812-162">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="61812-162">Click Run.</span></span>
4. <span data-ttu-id="61812-163">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="61812-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="61812-164">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="61812-164">Click Filter.</span></span>
6. <span data-ttu-id="61812-165">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="61812-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="61812-166">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61812-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="61812-167">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="61812-167">Example: P6003</span></span>  
8. <span data-ttu-id="61812-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="61812-168">Click OK.</span></span>
9. <span data-ttu-id="61812-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="61812-169">Click OK.</span></span>
10. <span data-ttu-id="61812-170">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="61812-170">Click Planned orders.</span></span>
11. <span data-ttu-id="61812-171">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="61812-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="61812-172">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="61812-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="61812-173">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="61812-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="61812-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="61812-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61812-175">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="61812-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="61812-176">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61812-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="61812-177">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="61812-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="61812-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61812-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="61812-179">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="61812-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="61812-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61812-180">Close the page.</span></span>
17. <span data-ttu-id="61812-181">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="61812-181">Click Master planning.</span></span>
18. <span data-ttu-id="61812-182">Перейдите в раздел "Сводное планирование" > "Настройка" > "Параметры сводного планирования".</span><span class="sxs-lookup"><span data-stu-id="61812-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="61812-183">Выберите "Нет" в поле "Отключить все процессы планирования".</span><span class="sxs-lookup"><span data-stu-id="61812-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="61812-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61812-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]