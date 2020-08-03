---
title: Примеры и логика отчетов о распределении запасов по срокам
description: В этом разделе представлено несколько примеров, демонстрирующих способы интерпретации результатов отчетов о распределении запасов по срокам.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb7b7a055c26b53ee3acc3b872acf04fcf089eca
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597248"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="045de-103">Примеры и логика отчетов о распределении запасов по срокам</span><span class="sxs-lookup"><span data-stu-id="045de-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="045de-104">В этом разделе представлено несколько примеров, демонстрирующих способы интерпретации результатов отчетов о **распределении запасов по срокам**.</span><span class="sxs-lookup"><span data-stu-id="045de-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="045de-105">Этот отчет распределяет количество в наличии и значения запасов для выбранной номенклатуры или номенклатурной группы по нескольким периодам.</span><span class="sxs-lookup"><span data-stu-id="045de-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="045de-106">В этом разделе также представлена внутренняя логика отчета.</span><span class="sxs-lookup"><span data-stu-id="045de-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="045de-107">В примерах этого раздела показаны результаты, представленные в стандартном отчете о **распределении запасов по срокам**.</span><span class="sxs-lookup"><span data-stu-id="045de-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="045de-108">Однако в общем случае рекомендуется использовать версию этого отчета [Хранилище отчетов о распределении запасов по срокам](inventory-aging-report-storage.md), особенно если имеется много номенклатур и складов, которые должны быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="045de-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="045de-109">Хранилище отчетов о распределении запасов по срокам сохраняет каждый созданный отчет, отображает результаты в виде интерактивной страницы и диаграммы и позволяет экспортировать любой сохраненный отчет.</span><span class="sxs-lookup"><span data-stu-id="045de-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="045de-110">Образцы данных, используемые в этих примерах</span><span class="sxs-lookup"><span data-stu-id="045de-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="045de-111">Примеры в этом разделе основаны на примере данных складских проводок, которые описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="045de-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="045de-112">Настройка аналитики хранения</span><span class="sxs-lookup"><span data-stu-id="045de-112">Storage dimension setup</span></span>

<span data-ttu-id="045de-113">В примере системы содержится следующая настройка аналитик хранения.</span><span class="sxs-lookup"><span data-stu-id="045de-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="045de-114">Наименование</span><span class="sxs-lookup"><span data-stu-id="045de-114">Name</span></span>      | <span data-ttu-id="045de-115">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="045de-115">Active</span></span> | <span data-ttu-id="045de-116">Физические запасы</span><span class="sxs-lookup"><span data-stu-id="045de-116">Physical inventory</span></span> | <span data-ttu-id="045de-117">Финансовые запасы</span><span class="sxs-lookup"><span data-stu-id="045de-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="045de-118">Сайт</span><span class="sxs-lookup"><span data-stu-id="045de-118">Site</span></span>      | <span data-ttu-id="045de-119">Да</span><span class="sxs-lookup"><span data-stu-id="045de-119">Yes</span></span>    | <span data-ttu-id="045de-120">Да</span><span class="sxs-lookup"><span data-stu-id="045de-120">Yes</span></span>                | <span data-ttu-id="045de-121">Да</span><span class="sxs-lookup"><span data-stu-id="045de-121">Yes</span></span>                 |
| <span data-ttu-id="045de-122">Склад</span><span class="sxs-lookup"><span data-stu-id="045de-122">Warehouse</span></span> | <span data-ttu-id="045de-123">Да</span><span class="sxs-lookup"><span data-stu-id="045de-123">Yes</span></span>    | <span data-ttu-id="045de-124">Да</span><span class="sxs-lookup"><span data-stu-id="045de-124">Yes</span></span>                | <span data-ttu-id="045de-125">Нет</span><span class="sxs-lookup"><span data-stu-id="045de-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="045de-126">Складская модель</span><span class="sxs-lookup"><span data-stu-id="045de-126">Inventory model</span></span>

<span data-ttu-id="045de-127">Для примера системы складской моделью для выпущенных продуктов является *FIFO*, а настройка **Себестоимость** для складской модели имеет значение *Включение физической стоимости*.</span><span class="sxs-lookup"><span data-stu-id="045de-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="045de-128">Складские проводки</span><span class="sxs-lookup"><span data-stu-id="045de-128">Inventory transactions</span></span>

<span data-ttu-id="045de-129">Пример системы содержит следующие складские проводки для выпущенного продукта с номером номенклатуры *1000*.</span><span class="sxs-lookup"><span data-stu-id="045de-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="045de-130">Справка</span><span class="sxs-lookup"><span data-stu-id="045de-130">Reference</span></span>      | <span data-ttu-id="045de-131">Сайт</span><span class="sxs-lookup"><span data-stu-id="045de-131">Site</span></span> | <span data-ttu-id="045de-132">Склад</span><span class="sxs-lookup"><span data-stu-id="045de-132">Warehouse</span></span> | <span data-ttu-id="045de-133">Чек</span><span class="sxs-lookup"><span data-stu-id="045de-133">Receipt</span></span>   | <span data-ttu-id="045de-134">Расход</span><span class="sxs-lookup"><span data-stu-id="045de-134">Issue</span></span> | <span data-ttu-id="045de-135">Физ. дата</span><span class="sxs-lookup"><span data-stu-id="045de-135">Physical date</span></span> | <span data-ttu-id="045de-136">Финанс. дата</span><span class="sxs-lookup"><span data-stu-id="045de-136">Financial date</span></span> | <span data-ttu-id="045de-137">Количество</span><span class="sxs-lookup"><span data-stu-id="045de-137">Quantity</span></span> | <span data-ttu-id="045de-138">Сумма стоимости</span><span class="sxs-lookup"><span data-stu-id="045de-138">Cost amount</span></span> | <span data-ttu-id="045de-139">Физ. сумма</span><span class="sxs-lookup"><span data-stu-id="045de-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="045de-140">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="045de-140">Purchase order</span></span> | <span data-ttu-id="045de-141">1</span><span class="sxs-lookup"><span data-stu-id="045de-141">1</span></span>    | <span data-ttu-id="045de-142">11</span><span class="sxs-lookup"><span data-stu-id="045de-142">11</span></span>        | <span data-ttu-id="045de-143">Куплено</span><span class="sxs-lookup"><span data-stu-id="045de-143">Purchased</span></span> |       | <span data-ttu-id="045de-144">15 марта</span><span class="sxs-lookup"><span data-stu-id="045de-144">March 15</span></span>      | <span data-ttu-id="045de-145">15 марта</span><span class="sxs-lookup"><span data-stu-id="045de-145">March 15</span></span>       | <span data-ttu-id="045de-146">10</span><span class="sxs-lookup"><span data-stu-id="045de-146">10</span></span>       | <span data-ttu-id="045de-147">1000</span><span class="sxs-lookup"><span data-stu-id="045de-147">1,000</span></span>       | <span data-ttu-id="045de-148">1000</span><span class="sxs-lookup"><span data-stu-id="045de-148">1,000</span></span>                |
| <span data-ttu-id="045de-149">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="045de-149">Purchase order</span></span> | <span data-ttu-id="045de-150">2</span><span class="sxs-lookup"><span data-stu-id="045de-150">2</span></span>    | <span data-ttu-id="045de-151">21</span><span class="sxs-lookup"><span data-stu-id="045de-151">21</span></span>        | <span data-ttu-id="045de-152">Куплено</span><span class="sxs-lookup"><span data-stu-id="045de-152">Purchased</span></span> |       | <span data-ttu-id="045de-153">15 марта</span><span class="sxs-lookup"><span data-stu-id="045de-153">March 15</span></span>      | <span data-ttu-id="045de-154">15 марта</span><span class="sxs-lookup"><span data-stu-id="045de-154">March 15</span></span>       | <span data-ttu-id="045de-155">10</span><span class="sxs-lookup"><span data-stu-id="045de-155">10</span></span>       | <span data-ttu-id="045de-156">2,000</span><span class="sxs-lookup"><span data-stu-id="045de-156">2,000</span></span>       | <span data-ttu-id="045de-157">2,000</span><span class="sxs-lookup"><span data-stu-id="045de-157">2,000</span></span>                |
| <span data-ttu-id="045de-158">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="045de-158">Purchase order</span></span> | <span data-ttu-id="045de-159">1</span><span class="sxs-lookup"><span data-stu-id="045de-159">1</span></span>    | <span data-ttu-id="045de-160">11</span><span class="sxs-lookup"><span data-stu-id="045de-160">11</span></span>        | <span data-ttu-id="045de-161">Получено</span><span class="sxs-lookup"><span data-stu-id="045de-161">Received</span></span>  |       | <span data-ttu-id="045de-162">Апрель 15 г.</span><span class="sxs-lookup"><span data-stu-id="045de-162">April 15</span></span>      |                | <span data-ttu-id="045de-163">5</span><span class="sxs-lookup"><span data-stu-id="045de-163">5</span></span>        |             | <span data-ttu-id="045de-164">375</span><span class="sxs-lookup"><span data-stu-id="045de-164">375</span></span>                  |
| <span data-ttu-id="045de-165">Заказ на перемещение</span><span class="sxs-lookup"><span data-stu-id="045de-165">Transfer order</span></span> | <span data-ttu-id="045de-166">1</span><span class="sxs-lookup"><span data-stu-id="045de-166">1</span></span>    | <span data-ttu-id="045de-167">11</span><span class="sxs-lookup"><span data-stu-id="045de-167">11</span></span>        |           | <span data-ttu-id="045de-168">Продано</span><span class="sxs-lookup"><span data-stu-id="045de-168">Sold</span></span>  | <span data-ttu-id="045de-169">2 мая</span><span class="sxs-lookup"><span data-stu-id="045de-169">May 2</span></span>         | <span data-ttu-id="045de-170">2 мая</span><span class="sxs-lookup"><span data-stu-id="045de-170">May 2</span></span>          | <span data-ttu-id="045de-171">-5</span><span class="sxs-lookup"><span data-stu-id="045de-171">-5</span></span>       | <span data-ttu-id="045de-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="045de-172">-458.33</span></span>     | <span data-ttu-id="045de-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="045de-173">-458.33</span></span>              |
| <span data-ttu-id="045de-174">Заказ на перемещение</span><span class="sxs-lookup"><span data-stu-id="045de-174">Transfer order</span></span> | <span data-ttu-id="045de-175">1</span><span class="sxs-lookup"><span data-stu-id="045de-175">1</span></span>    | <span data-ttu-id="045de-176">12</span><span class="sxs-lookup"><span data-stu-id="045de-176">12</span></span>        | <span data-ttu-id="045de-177">Куплено</span><span class="sxs-lookup"><span data-stu-id="045de-177">Purchased</span></span> |       | <span data-ttu-id="045de-178">2 мая</span><span class="sxs-lookup"><span data-stu-id="045de-178">May 2</span></span>         | <span data-ttu-id="045de-179">2 мая</span><span class="sxs-lookup"><span data-stu-id="045de-179">May 2</span></span>          | <span data-ttu-id="045de-180">5</span><span class="sxs-lookup"><span data-stu-id="045de-180">5</span></span>        | <span data-ttu-id="045de-181">458.33</span><span class="sxs-lookup"><span data-stu-id="045de-181">458.33</span></span>      | <span data-ttu-id="045de-182">458.33</span><span class="sxs-lookup"><span data-stu-id="045de-182">458.33</span></span>               |
| <span data-ttu-id="045de-183">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="045de-183">Sales order</span></span>    | <span data-ttu-id="045de-184">1</span><span class="sxs-lookup"><span data-stu-id="045de-184">1</span></span>    | <span data-ttu-id="045de-185">12</span><span class="sxs-lookup"><span data-stu-id="045de-185">12</span></span>        |           | <span data-ttu-id="045de-186">Продано</span><span class="sxs-lookup"><span data-stu-id="045de-186">Sold</span></span>  | <span data-ttu-id="045de-187">3 мая</span><span class="sxs-lookup"><span data-stu-id="045de-187">May 3</span></span>         | <span data-ttu-id="045de-188">3 мая</span><span class="sxs-lookup"><span data-stu-id="045de-188">May 3</span></span>          | <span data-ttu-id="045de-189">-1</span><span class="sxs-lookup"><span data-stu-id="045de-189">-1</span></span>       | <span data-ttu-id="045de-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="045de-190">-91.67</span></span>      | <span data-ttu-id="045de-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="045de-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="045de-192">Расчет количества и сумм в каждом из сегментов периода</span><span class="sxs-lookup"><span data-stu-id="045de-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="045de-193">Используя образцы данных, описанные в предыдущих разделах, можно выполнить отчет **Распределение запасов по срокам**, который имеет следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="045de-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="045de-194">**По состоянию на дату:** *9 мая 2020 г.*</span><span class="sxs-lookup"><span data-stu-id="045de-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="045de-195">**Сайт:** *Вид*</span><span class="sxs-lookup"><span data-stu-id="045de-195">**Site:** *View*</span></span>
- <span data-ttu-id="045de-196">**Склад:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="045de-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="045de-197">**Код номенклатуры:** *Итого*</span><span class="sxs-lookup"><span data-stu-id="045de-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="045de-198">**Период распределения по срокам:** Настройте это поле для создания месячных периодов.</span><span class="sxs-lookup"><span data-stu-id="045de-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="045de-199">В этом случае содержание созданного отчета будет аналогично следующему примеру:</span><span class="sxs-lookup"><span data-stu-id="045de-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="045de-200">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="045de-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-201">Сайт</span><span class="sxs-lookup"><span data-stu-id="045de-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-202">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="045de-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-203">Стоимость запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="045de-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-204">Количество для стоимости запасов</span><span class="sxs-lookup"><span data-stu-id="045de-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-205">Стоимость запасов</span><span class="sxs-lookup"><span data-stu-id="045de-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-206">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="045de-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-207">08.05.2020 – 01.05.2020</span><span class="sxs-lookup"><span data-stu-id="045de-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-208">30.04.2020 – 01.04.2020</span><span class="sxs-lookup"><span data-stu-id="045de-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-209">31.03.2020 – 01.03.2020</span><span class="sxs-lookup"><span data-stu-id="045de-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="045de-210">P1:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="045de-211">P1:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="045de-212">P2:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="045de-213">P2:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="045de-214">P3:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="045de-215">P3:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="045de-216">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-216">1000</span></span></td>
    <td><span data-ttu-id="045de-217">1</span><span class="sxs-lookup"><span data-stu-id="045de-217">1</span></span></td>
    <td><span data-ttu-id="045de-218">14</span><span class="sxs-lookup"><span data-stu-id="045de-218">14</span></span></td>
    <td><span data-ttu-id="045de-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="045de-219">1,283.33</span></span></td>
    <td><span data-ttu-id="045de-220">14</span><span class="sxs-lookup"><span data-stu-id="045de-220">14</span></span></td>
    <td><span data-ttu-id="045de-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="045de-221">1,283.33</span></span></td>
    <td><span data-ttu-id="045de-222">91.67</span><span class="sxs-lookup"><span data-stu-id="045de-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-223">5.00</span><span class="sxs-lookup"><span data-stu-id="045de-223">5.00</span></span></td>
    <td><span data-ttu-id="045de-224">458.33</span><span class="sxs-lookup"><span data-stu-id="045de-224">458.33</span></span></td>
    <td><span data-ttu-id="045de-225">9.00</span><span class="sxs-lookup"><span data-stu-id="045de-225">9.00</span></span></td>
    <td><span data-ttu-id="045de-226">825.00</span><span class="sxs-lookup"><span data-stu-id="045de-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="045de-227">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-227">1000</span></span></td>
    <td><span data-ttu-id="045de-228">2</span><span class="sxs-lookup"><span data-stu-id="045de-228">2</span></span></td>
    <td><span data-ttu-id="045de-229">10</span><span class="sxs-lookup"><span data-stu-id="045de-229">10</span></span></td>
    <td><span data-ttu-id="045de-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-230">2,000.00</span></span></td>
    <td><span data-ttu-id="045de-231">10</span><span class="sxs-lookup"><span data-stu-id="045de-231">10</span></span></td>
    <td><span data-ttu-id="045de-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-232">2,000.00</span></span></td>
    <td><span data-ttu-id="045de-233">200.00</span><span class="sxs-lookup"><span data-stu-id="045de-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-234">10.00</span><span class="sxs-lookup"><span data-stu-id="045de-234">10.00</span></span></td>
    <td><span data-ttu-id="045de-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="045de-236"><strong>Итого 1000</strong></span><span class="sxs-lookup"><span data-stu-id="045de-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="045de-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="045de-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="045de-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="045de-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="045de-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="045de-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="045de-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="045de-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="045de-243">Обратите внимание на следующие детали в этом примере отчета:</span><span class="sxs-lookup"><span data-stu-id="045de-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="045de-244">Значения **Количество стоимости запасов**, **Стоимость запасов** и **Средняя стоимость единицы**, отображаемые в отчете, являются значениями складской аналитики (**Сайт**, в данном случае).</span><span class="sxs-lookup"><span data-stu-id="045de-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="045de-245">Например, для сайта 1 в отчете отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="045de-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="045de-246">Значение **Количество стоимости запасов** равно *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="045de-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="045de-247">Значение **Стоимость запасов** равно *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="045de-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="045de-248">Значение **Средняя стоимость единицы** равно *91,67*.</span><span class="sxs-lookup"><span data-stu-id="045de-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="045de-249">Значение **Стоимость запасов в наличии** и значение **Сумма** в каждом из сегментов периода рассчитываются с использованием значения **Средняя стоимость единицы**.</span><span class="sxs-lookup"><span data-stu-id="045de-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="045de-250">Отчет определяет количество в наличии для каждого сегмента периода, суммируя общее полученное количество запасов для каждого из сегментов периода.</span><span class="sxs-lookup"><span data-stu-id="045de-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="045de-251">Затем применяется принцип ФИФО ("первым пришел, первым ушел"), чтобы вычесть итоговое выпущенное количество, независимо от складской модели, используемой номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="045de-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="045de-252">Если повторно выполнить один и тот же отчет, но на этот раз задать в полях **Сайт** и **Склад** значение *Вид*, новый отчет будет похож на следующий пример.</span><span class="sxs-lookup"><span data-stu-id="045de-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="045de-253">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="045de-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-254">Сайт</span><span class="sxs-lookup"><span data-stu-id="045de-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-255">Склад</span><span class="sxs-lookup"><span data-stu-id="045de-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-256">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="045de-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-257">Стоимость запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="045de-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-258">Количество для стоимости запасов</span><span class="sxs-lookup"><span data-stu-id="045de-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-259">Стоимость запасов</span><span class="sxs-lookup"><span data-stu-id="045de-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-260">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="045de-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-261">08.05.2020 – 01.05.2020</span><span class="sxs-lookup"><span data-stu-id="045de-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-262">30.04.2020 – 01.04.2020</span><span class="sxs-lookup"><span data-stu-id="045de-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-263">31.03.2020 – 01.03.2020</span><span class="sxs-lookup"><span data-stu-id="045de-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="045de-264">P1:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="045de-265">P1:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="045de-266">P2:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="045de-267">P2:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="045de-268">P3:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="045de-269">P3:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="045de-270">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-270">1000</span></span></td>
    <td><span data-ttu-id="045de-271">1</span><span class="sxs-lookup"><span data-stu-id="045de-271">1</span></span></td>
    <td><span data-ttu-id="045de-272">11</span><span class="sxs-lookup"><span data-stu-id="045de-272">11</span></span></td>
    <td><span data-ttu-id="045de-273">10</span><span class="sxs-lookup"><span data-stu-id="045de-273">10</span></span></td>
    <td><span data-ttu-id="045de-274">916.67</span><span class="sxs-lookup"><span data-stu-id="045de-274">916.67</span></span></td>
    <td><span data-ttu-id="045de-275">14</span><span class="sxs-lookup"><span data-stu-id="045de-275">14</span></span></td>
    <td><span data-ttu-id="045de-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="045de-276">1,283.33</span></span></td>
    <td><span data-ttu-id="045de-277">91.67</span><span class="sxs-lookup"><span data-stu-id="045de-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-278">5.00</span><span class="sxs-lookup"><span data-stu-id="045de-278">5.00</span></span></td>
    <td><span data-ttu-id="045de-279">458.33</span><span class="sxs-lookup"><span data-stu-id="045de-279">458.33</span></span></td>
    <td><span data-ttu-id="045de-280">5.00</span><span class="sxs-lookup"><span data-stu-id="045de-280">5.00</span></span></td>
    <td><span data-ttu-id="045de-281">458.33</span><span class="sxs-lookup"><span data-stu-id="045de-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="045de-282">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-282">1000</span></span></td>
    <td><span data-ttu-id="045de-283">1</span><span class="sxs-lookup"><span data-stu-id="045de-283">1</span></span></td>
    <td><span data-ttu-id="045de-284">12</span><span class="sxs-lookup"><span data-stu-id="045de-284">12</span></span></td>
    <td><span data-ttu-id="045de-285">4</span><span class="sxs-lookup"><span data-stu-id="045de-285">4</span></span></td>
    <td><span data-ttu-id="045de-286">366.67</span><span class="sxs-lookup"><span data-stu-id="045de-286">366.67</span></span></td>
    <td><span data-ttu-id="045de-287">14</span><span class="sxs-lookup"><span data-stu-id="045de-287">14</span></span></td>
    <td><span data-ttu-id="045de-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="045de-288">1,283.33</span></span></td>
    <td><span data-ttu-id="045de-289">91.67</span><span class="sxs-lookup"><span data-stu-id="045de-289">91.67</span></span></td>
    <td><span data-ttu-id="045de-290">4.00</span><span class="sxs-lookup"><span data-stu-id="045de-290">4.00</span></span></td>
    <td><span data-ttu-id="045de-291">366.67</span><span class="sxs-lookup"><span data-stu-id="045de-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="045de-292">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-292">1000</span></span></td>
    <td><span data-ttu-id="045de-293">2</span><span class="sxs-lookup"><span data-stu-id="045de-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="045de-294">10</span><span class="sxs-lookup"><span data-stu-id="045de-294">10</span></span></td>
    <td><span data-ttu-id="045de-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-295">2,000.00</span></span></td>
    <td><span data-ttu-id="045de-296">10</span><span class="sxs-lookup"><span data-stu-id="045de-296">10</span></span></td>
    <td><span data-ttu-id="045de-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-297">2,000.00</span></span></td>
    <td><span data-ttu-id="045de-298">200.00</span><span class="sxs-lookup"><span data-stu-id="045de-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-299">10.00</span><span class="sxs-lookup"><span data-stu-id="045de-299">10.00</span></span></td>
    <td><span data-ttu-id="045de-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="045de-301"><strong>Итого 1000</strong></span><span class="sxs-lookup"><span data-stu-id="045de-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="045de-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="045de-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="045de-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="045de-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="045de-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="045de-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="045de-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="045de-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="045de-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="045de-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="045de-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="045de-310">На этот раз сайт 1 разбивается на две строки, одну для склада 11, и одну для склада 12.</span><span class="sxs-lookup"><span data-stu-id="045de-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="045de-311">Однако значение **Количество стоимости запасов**, **Стоимость запасов** и **Средняя стоимость единицы** будут теми же, поскольку **Склад** не является складской аналитикой.</span><span class="sxs-lookup"><span data-stu-id="045de-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="045de-312">Кроме того, обратите внимание, что распределение количества на сайте 1 является другим.</span><span class="sxs-lookup"><span data-stu-id="045de-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="045de-313">В первом запущенном отчете система проигнорировала заказ на перемещение, который был выполнен на том же сайте, и вычитала количество из счета на продажу из периода **31.03.2020–01.03.2020** на сайте 1.</span><span class="sxs-lookup"><span data-stu-id="045de-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="045de-314">Однако в новом отчете система вычитает количество по счету продажи из сегмента периода **08.05.2020–01.05.2020** на складе 12.</span><span class="sxs-lookup"><span data-stu-id="045de-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="045de-315">Эффекты закрытия запасов</span><span class="sxs-lookup"><span data-stu-id="045de-315">Effects of inventory closing</span></span>

<span data-ttu-id="045de-316">Если вы запустите закрытие запасов для мая, а затем снова запустите предыдущий отчет, но зададите в поле **По состоянию на дату** значение *31 мая 2020*, вы увидите следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="045de-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="045de-317">Значения **Стоимость запасов** и **Средняя стоимость за единицу** обновляются.</span><span class="sxs-lookup"><span data-stu-id="045de-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="045de-318">Значение **Стоимость запасов в наличии** и все значения **Сумма** в каждом из сегментов периода соответственно обновляются.</span><span class="sxs-lookup"><span data-stu-id="045de-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="045de-319">Новый отчет будет похож на следующий пример.</span><span class="sxs-lookup"><span data-stu-id="045de-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="045de-320">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="045de-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-321">Сайт</span><span class="sxs-lookup"><span data-stu-id="045de-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-322">Склад</span><span class="sxs-lookup"><span data-stu-id="045de-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-323">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="045de-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-324">Стоимость запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="045de-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-325">Количество для стоимости запасов</span><span class="sxs-lookup"><span data-stu-id="045de-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-326">Стоимость запасов</span><span class="sxs-lookup"><span data-stu-id="045de-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="045de-327">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="045de-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-328">31.05.2020 – 01.05.2020</span><span class="sxs-lookup"><span data-stu-id="045de-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-329">30.04.2020 – 01.04.2020</span><span class="sxs-lookup"><span data-stu-id="045de-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="045de-330">31.03.2020 – 01.03.2020</span><span class="sxs-lookup"><span data-stu-id="045de-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="045de-331">P1:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="045de-332">P1:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="045de-333">P2:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="045de-334">P2:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="045de-335">P3:Количество</span><span class="sxs-lookup"><span data-stu-id="045de-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="045de-336">P3:Сумма</span><span class="sxs-lookup"><span data-stu-id="045de-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="045de-337">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-337">1000</span></span></td>
    <td><span data-ttu-id="045de-338">1</span><span class="sxs-lookup"><span data-stu-id="045de-338">1</span></span></td>
    <td><span data-ttu-id="045de-339">11</span><span class="sxs-lookup"><span data-stu-id="045de-339">11</span></span></td>
    <td><span data-ttu-id="045de-340">10</span><span class="sxs-lookup"><span data-stu-id="045de-340">10</span></span></td>
    <td><span data-ttu-id="045de-341">910.70</span><span class="sxs-lookup"><span data-stu-id="045de-341">910.70</span></span></td>
    <td><span data-ttu-id="045de-342">14</span><span class="sxs-lookup"><span data-stu-id="045de-342">14</span></span></td>
    <td><span data-ttu-id="045de-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="045de-343">1,275.00</span></span></td>
    <td><span data-ttu-id="045de-344">91.07</span><span class="sxs-lookup"><span data-stu-id="045de-344">91.07</span></span></td>
    <td><span data-ttu-id="045de-345">0.00</span><span class="sxs-lookup"><span data-stu-id="045de-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="045de-346">5.00</span><span class="sxs-lookup"><span data-stu-id="045de-346">5.00</span></span></td>
    <td><span data-ttu-id="045de-347">455.36</span><span class="sxs-lookup"><span data-stu-id="045de-347">455.36</span></span></td>
    <td><span data-ttu-id="045de-348">5.00</span><span class="sxs-lookup"><span data-stu-id="045de-348">5.00</span></span></td>
    <td><span data-ttu-id="045de-349">455.36</span><span class="sxs-lookup"><span data-stu-id="045de-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="045de-350">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-350">1000</span></span></td>
    <td><span data-ttu-id="045de-351">1</span><span class="sxs-lookup"><span data-stu-id="045de-351">1</span></span></td>
    <td><span data-ttu-id="045de-352">12</span><span class="sxs-lookup"><span data-stu-id="045de-352">12</span></span></td>
    <td><span data-ttu-id="045de-353">4</span><span class="sxs-lookup"><span data-stu-id="045de-353">4</span></span></td>
    <td><span data-ttu-id="045de-354">364.29</span><span class="sxs-lookup"><span data-stu-id="045de-354">364.29</span></span></td>
    <td><span data-ttu-id="045de-355">14</span><span class="sxs-lookup"><span data-stu-id="045de-355">14</span></span></td>
    <td><span data-ttu-id="045de-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="045de-356">1,275.00</span></span></td>
    <td><span data-ttu-id="045de-357">91.07</span><span class="sxs-lookup"><span data-stu-id="045de-357">91.07</span></span></td>
    <td><span data-ttu-id="045de-358">4.00</span><span class="sxs-lookup"><span data-stu-id="045de-358">4.00</span></span></td>
    <td><span data-ttu-id="045de-359">364.29</span><span class="sxs-lookup"><span data-stu-id="045de-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="045de-360">В тысячах</span><span class="sxs-lookup"><span data-stu-id="045de-360">1000</span></span></td>
    <td><span data-ttu-id="045de-361">2</span><span class="sxs-lookup"><span data-stu-id="045de-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="045de-362">10</span><span class="sxs-lookup"><span data-stu-id="045de-362">10</span></span></td>
    <td><span data-ttu-id="045de-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-363">2,000.00</span></span></td>
    <td><span data-ttu-id="045de-364">10</span><span class="sxs-lookup"><span data-stu-id="045de-364">10</span></span></td>
    <td><span data-ttu-id="045de-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-365">2,000.00</span></span></td>
    <td><span data-ttu-id="045de-366">200.00</span><span class="sxs-lookup"><span data-stu-id="045de-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-367">10.00</span><span class="sxs-lookup"><span data-stu-id="045de-367">10.00</span></span></td>
    <td><span data-ttu-id="045de-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="045de-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="045de-369"><strong>Итого 1000</strong></span><span class="sxs-lookup"><span data-stu-id="045de-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="045de-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="045de-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="045de-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="045de-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="045de-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="045de-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="045de-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="045de-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="045de-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="045de-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="045de-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="045de-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>