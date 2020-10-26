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
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982217"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="52597-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="52597-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52597-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="52597-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="52597-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="52597-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="52597-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="52597-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="52597-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52597-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="52597-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="52597-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="52597-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="52597-109">Click New.</span></span>
4. <span data-ttu-id="52597-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="52597-110">Click Sales order.</span></span>
5. <span data-ttu-id="52597-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52597-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="52597-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="52597-112">Example: US-001</span></span>  
6. <span data-ttu-id="52597-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52597-113">Click OK.</span></span>
7. <span data-ttu-id="52597-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52597-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="52597-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="52597-115">Example: P6003</span></span>  
8. <span data-ttu-id="52597-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="52597-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="52597-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="52597-117">Example: 50000</span></span>  
9. <span data-ttu-id="52597-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="52597-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="52597-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="52597-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="52597-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52597-120">Close the page.</span></span>
2. <span data-ttu-id="52597-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52597-121">Close the page.</span></span>
3. <span data-ttu-id="52597-122">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="52597-122">Click Master planning.</span></span>
4. <span data-ttu-id="52597-123">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="52597-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="52597-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52597-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52597-125">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="52597-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="52597-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="52597-126">Click Run.</span></span>
7. <span data-ttu-id="52597-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="52597-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="52597-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="52597-128">Click Filter.</span></span>
9. <span data-ttu-id="52597-129">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="52597-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="52597-130">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52597-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="52597-131">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="52597-131">Example: P6003</span></span>  
11. <span data-ttu-id="52597-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52597-132">Click OK.</span></span>
12. <span data-ttu-id="52597-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52597-133">Click OK.</span></span>
13. <span data-ttu-id="52597-134">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="52597-134">Click Planned orders.</span></span>
14. <span data-ttu-id="52597-135">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="52597-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="52597-136">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="52597-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="52597-137">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="52597-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="52597-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="52597-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="52597-139">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="52597-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="52597-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52597-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="52597-141">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="52597-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="52597-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52597-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52597-143">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="52597-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="52597-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52597-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="52597-145">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="52597-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="52597-146">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52597-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="52597-147">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="52597-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="52597-148">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="52597-148">Click New.</span></span>
4. <span data-ttu-id="52597-149">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="52597-149">Click Sales order.</span></span>
5. <span data-ttu-id="52597-150">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52597-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="52597-151">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="52597-151">Example: US-001</span></span>  
6. <span data-ttu-id="52597-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52597-152">Click OK.</span></span>
7. <span data-ttu-id="52597-153">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52597-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="52597-154">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="52597-154">Example: P6003</span></span>  
8. <span data-ttu-id="52597-155">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="52597-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="52597-156">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="52597-156">Example: 50000</span></span>  
9. <span data-ttu-id="52597-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="52597-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="52597-158">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="52597-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="52597-159">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="52597-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="52597-160">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52597-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52597-161">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="52597-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="52597-162">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="52597-162">Click Run.</span></span>
4. <span data-ttu-id="52597-163">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="52597-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="52597-164">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="52597-164">Click Filter.</span></span>
6. <span data-ttu-id="52597-165">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="52597-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="52597-166">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52597-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="52597-167">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="52597-167">Example: P6003</span></span>  
8. <span data-ttu-id="52597-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52597-168">Click OK.</span></span>
9. <span data-ttu-id="52597-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52597-169">Click OK.</span></span>
10. <span data-ttu-id="52597-170">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="52597-170">Click Planned orders.</span></span>
11. <span data-ttu-id="52597-171">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="52597-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="52597-172">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="52597-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="52597-173">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="52597-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="52597-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="52597-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="52597-175">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="52597-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="52597-176">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52597-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="52597-177">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="52597-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="52597-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52597-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52597-179">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="52597-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="52597-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52597-180">Close the page.</span></span>
17. <span data-ttu-id="52597-181">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="52597-181">Click Master planning.</span></span>
18. <span data-ttu-id="52597-182">Перейдите в раздел "Сводное планирование" > "Настройка" > "Параметры сводного планирования".</span><span class="sxs-lookup"><span data-stu-id="52597-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="52597-183">Выберите "Нет" в поле "Отключить все процессы планирования".</span><span class="sxs-lookup"><span data-stu-id="52597-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="52597-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52597-184">Close the page.</span></span>

