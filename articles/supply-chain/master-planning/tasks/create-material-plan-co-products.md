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
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920737"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a1cad-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="a1cad-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1cad-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="a1cad-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="a1cad-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="a1cad-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="a1cad-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="a1cad-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="a1cad-107">Перейдите **Продажи и маркетинг \> Рабочие области \> Обработка и запрос заказов на продажу**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="a1cad-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-108">Select **New**.</span></span>
1. <span data-ttu-id="a1cad-109">Выберите **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="a1cad-110">В поле **Счет клиента** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a1cad-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="a1cad-111">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="a1cad-111">Example: US-001</span></span>  
1. <span data-ttu-id="a1cad-112">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-112">Select **OK**.</span></span>
1. <span data-ttu-id="a1cad-113">В поле **Код номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a1cad-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="a1cad-114">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="a1cad-114">Example: P6003</span></span>  
1. <span data-ttu-id="a1cad-115">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="a1cad-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="a1cad-116">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="a1cad-116">Example: 50000</span></span>  
1. <span data-ttu-id="a1cad-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a1cad-118">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="a1cad-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="a1cad-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-119">Close the page.</span></span>
1. <span data-ttu-id="a1cad-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-120">Close the page.</span></span>
1. <span data-ttu-id="a1cad-121">Выберите **Сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="a1cad-122">В поле **План** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a1cad-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="a1cad-123">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a1cad-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="a1cad-124">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="a1cad-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="a1cad-125">Выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-125">Select **Run**.</span></span>
1. <span data-ttu-id="a1cad-126">Разверните или сверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="a1cad-127">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-127">Select **Filter**.</span></span>
1. <span data-ttu-id="a1cad-128">Выберите в списке строку, где **Поле** = *Номер номенклатуры*.</span><span class="sxs-lookup"><span data-stu-id="a1cad-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="a1cad-129">В поле **Критерии** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a1cad-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="a1cad-130">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="a1cad-130">Example: P6003</span></span>  
1. <span data-ttu-id="a1cad-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-131">Select **OK**.</span></span>
1. <span data-ttu-id="a1cad-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-132">Select **OK**.</span></span>
1. <span data-ttu-id="a1cad-133">Выберите **Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="a1cad-134">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="a1cad-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a1cad-135">Например, отфильтруйте поле **Номер номенклатуры** по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="a1cad-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="a1cad-136">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="a1cad-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a1cad-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a1cad-138">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="a1cad-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="a1cad-139">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a1cad-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="a1cad-140">Разверните раздел **Информация об источниках потребности**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="a1cad-141">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a1cad-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="a1cad-142">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="a1cad-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="a1cad-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="a1cad-144">Создание второй потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="a1cad-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="a1cad-145">Перейдите **Продажи и маркетинг \> Рабочие области \> Обработка и запрос заказов на продажу**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="a1cad-146">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-146">Select **New**.</span></span>
1. <span data-ttu-id="a1cad-147">Выберите **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="a1cad-148">В поле **Счет клиента** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a1cad-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="a1cad-149">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="a1cad-149">Example: US-001</span></span>  
1. <span data-ttu-id="a1cad-150">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-150">Select **OK**.</span></span>
1. <span data-ttu-id="a1cad-151">В поле **Код номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a1cad-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="a1cad-152">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="a1cad-152">Example: P6003</span></span>  
1. <span data-ttu-id="a1cad-153">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="a1cad-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="a1cad-154">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="a1cad-154">Example: 50000</span></span>  
1. <span data-ttu-id="a1cad-155">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="a1cad-156">Создание второго плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="a1cad-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="a1cad-157">В поле **План** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a1cad-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a1cad-158">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a1cad-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="a1cad-159">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="a1cad-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="a1cad-160">Выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-160">Select **Run**.</span></span>
4. <span data-ttu-id="a1cad-161">Разверните или сверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="a1cad-162">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-162">Select **Filter**.</span></span>
6. <span data-ttu-id="a1cad-163">Выберите в списке строку, где **Поле** = *Номер номенклатуры*.</span><span class="sxs-lookup"><span data-stu-id="a1cad-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="a1cad-164">В поле *Критерии* введите значение.</span><span class="sxs-lookup"><span data-stu-id="a1cad-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="a1cad-165">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="a1cad-165">Example: P6003</span></span>  
8. <span data-ttu-id="a1cad-166">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-166">Select **OK**.</span></span>
9. <span data-ttu-id="a1cad-167">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-167">Select **OK**.</span></span>
10. <span data-ttu-id="a1cad-168">Выберите **Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="a1cad-169">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="a1cad-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a1cad-170">Например, отфильтруйте поле **Номер номенклатуры** по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="a1cad-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="a1cad-171">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="a1cad-172">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a1cad-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a1cad-173">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="a1cad-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="a1cad-174">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a1cad-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="a1cad-175">Разверните или сверните раздел **Информация об источниках потребности**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="a1cad-176">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a1cad-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="a1cad-177">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="a1cad-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="a1cad-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-178">Close the page.</span></span>
17. <span data-ttu-id="a1cad-179">Выберите **Сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="a1cad-180">Перейдите в раздел **Сводное планирование \> Настройка \> Параметры сводного планирования**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="a1cad-181">Выберите *Нет* в поле **Отключить все процессы планирования**.</span><span class="sxs-lookup"><span data-stu-id="a1cad-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="a1cad-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1cad-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]