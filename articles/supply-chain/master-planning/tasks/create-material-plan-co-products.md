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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209682"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="25d9d-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="25d9d-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25d9d-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="25d9d-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="25d9d-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="25d9d-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="25d9d-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="25d9d-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="25d9d-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25d9d-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="25d9d-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="25d9d-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="25d9d-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="25d9d-109">Click New.</span></span>
4. <span data-ttu-id="25d9d-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="25d9d-110">Click Sales order.</span></span>
5. <span data-ttu-id="25d9d-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="25d9d-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="25d9d-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="25d9d-112">Example: US-001</span></span>  
6. <span data-ttu-id="25d9d-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="25d9d-113">Click OK.</span></span>
7. <span data-ttu-id="25d9d-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="25d9d-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="25d9d-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="25d9d-115">Example: P6003</span></span>  
8. <span data-ttu-id="25d9d-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="25d9d-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="25d9d-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="25d9d-117">Example: 50000</span></span>  
9. <span data-ttu-id="25d9d-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="25d9d-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="25d9d-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="25d9d-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="25d9d-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-120">Close the page.</span></span>
2. <span data-ttu-id="25d9d-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-121">Close the page.</span></span>
3. <span data-ttu-id="25d9d-122">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="25d9d-122">Click Master planning.</span></span>
4. <span data-ttu-id="25d9d-123">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="25d9d-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="25d9d-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="25d9d-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25d9d-125">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="25d9d-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="25d9d-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="25d9d-126">Click Run.</span></span>
7. <span data-ttu-id="25d9d-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="25d9d-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="25d9d-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="25d9d-128">Click Filter.</span></span>
9. <span data-ttu-id="25d9d-129">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="25d9d-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="25d9d-130">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="25d9d-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="25d9d-131">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="25d9d-131">Example: P6003</span></span>  
11. <span data-ttu-id="25d9d-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="25d9d-132">Click OK.</span></span>
12. <span data-ttu-id="25d9d-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="25d9d-133">Click OK.</span></span>
13. <span data-ttu-id="25d9d-134">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="25d9d-134">Click Planned orders.</span></span>
14. <span data-ttu-id="25d9d-135">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="25d9d-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="25d9d-136">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="25d9d-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="25d9d-137">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="25d9d-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="25d9d-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="25d9d-139">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="25d9d-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="25d9d-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="25d9d-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="25d9d-141">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="25d9d-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="25d9d-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="25d9d-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25d9d-143">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="25d9d-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="25d9d-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="25d9d-145">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="25d9d-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="25d9d-146">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25d9d-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="25d9d-147">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="25d9d-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="25d9d-148">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="25d9d-148">Click New.</span></span>
4. <span data-ttu-id="25d9d-149">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="25d9d-149">Click Sales order.</span></span>
5. <span data-ttu-id="25d9d-150">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="25d9d-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="25d9d-151">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="25d9d-151">Example: US-001</span></span>  
6. <span data-ttu-id="25d9d-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="25d9d-152">Click OK.</span></span>
7. <span data-ttu-id="25d9d-153">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="25d9d-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="25d9d-154">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="25d9d-154">Example: P6003</span></span>  
8. <span data-ttu-id="25d9d-155">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="25d9d-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="25d9d-156">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="25d9d-156">Example: 50000</span></span>  
9. <span data-ttu-id="25d9d-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="25d9d-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="25d9d-158">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="25d9d-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="25d9d-159">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="25d9d-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="25d9d-160">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="25d9d-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25d9d-161">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="25d9d-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="25d9d-162">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="25d9d-162">Click Run.</span></span>
4. <span data-ttu-id="25d9d-163">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="25d9d-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="25d9d-164">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="25d9d-164">Click Filter.</span></span>
6. <span data-ttu-id="25d9d-165">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="25d9d-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="25d9d-166">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="25d9d-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="25d9d-167">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="25d9d-167">Example: P6003</span></span>  
8. <span data-ttu-id="25d9d-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="25d9d-168">Click OK.</span></span>
9. <span data-ttu-id="25d9d-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="25d9d-169">Click OK.</span></span>
10. <span data-ttu-id="25d9d-170">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="25d9d-170">Click Planned orders.</span></span>
11. <span data-ttu-id="25d9d-171">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="25d9d-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="25d9d-172">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="25d9d-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="25d9d-173">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="25d9d-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="25d9d-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="25d9d-175">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="25d9d-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="25d9d-176">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="25d9d-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="25d9d-177">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="25d9d-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="25d9d-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="25d9d-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25d9d-179">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="25d9d-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="25d9d-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-180">Close the page.</span></span>
17. <span data-ttu-id="25d9d-181">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="25d9d-181">Click Master planning.</span></span>
18. <span data-ttu-id="25d9d-182">Перейдите в раздел "Сводное планирование" > "Настройка" > "Параметры сводного планирования".</span><span class="sxs-lookup"><span data-stu-id="25d9d-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="25d9d-183">Выберите "Нет" в поле "Отключить все процессы планирования".</span><span class="sxs-lookup"><span data-stu-id="25d9d-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="25d9d-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="25d9d-184">Close the page.</span></span>

