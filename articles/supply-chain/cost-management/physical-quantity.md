---
title: "Значения объекта запасов"
description: "В этой статье представлена информация о том, как рассчитываются значения объекта запасов."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 60f39b19a627e9c3288f30872d237b8c0ccd8ac4
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="inventory-object-values"></a><span data-ttu-id="77092-103">Значения объекта запасов</span><span class="sxs-lookup"><span data-stu-id="77092-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77092-104">В этой статье представлена информация о том, как рассчитываются значения объекта запасов.</span><span class="sxs-lookup"><span data-stu-id="77092-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="77092-105">Новая функция **Физическое количество** позволяет просматривать значения определенного объекта запасов.</span><span class="sxs-lookup"><span data-stu-id="77092-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="77092-106">Объект затрат представляет уровень объекта, на котором выполняется учет запасов.</span><span class="sxs-lookup"><span data-stu-id="77092-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="77092-107">Дополнительные сведения об объектах затрат см. в разделе [Объекты затрат](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="77092-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="77092-108">Чтобы просмотреть значения определенного объекта запасов, щелкните **Физическое количество** на странице **Объект затрат**.</span><span class="sxs-lookup"><span data-stu-id="77092-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="77092-109">Вот как вычисляется значение объекта запасов:</span><span class="sxs-lookup"><span data-stu-id="77092-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="77092-110">Объект запасов.Значение = Объект затрат.Средняя себестоимость единицы × Объект запасов.Количество</span><span class="sxs-lookup"><span data-stu-id="77092-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="77092-111">В следующем примере показано, как вычисляются значения объекта запасов и объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="77092-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="77092-112">Два события поступления продуктов зарегистрированы в номенклатуре А:</span><span class="sxs-lookup"><span data-stu-id="77092-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="77092-113">Поступление продуктов 1: количество = 100 шт., сумма = 1000,00 долларов США, сайт = 1, склад =11, номер партии</span><span class="sxs-lookup"><span data-stu-id="77092-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="77092-114">= B1</span><span class="sxs-lookup"><span data-stu-id="77092-114">= B1</span></span>
-   <span data-ttu-id="77092-115">Поступление продуктов 2: количество = 50 шт., сумма = 800,00 долларов США, сайт = 1, склад =11, номер партии</span><span class="sxs-lookup"><span data-stu-id="77092-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="77092-116">= B2</span><span class="sxs-lookup"><span data-stu-id="77092-116">= B2</span></span>

<span data-ttu-id="77092-117">В следующей таблицы показан результат расчета для объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="77092-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="77092-118">Результат можно просмотреть на странице **Объект затрат**.</span><span class="sxs-lookup"><span data-stu-id="77092-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77092-119">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="77092-119">Object type</span></span></th>
<th><span data-ttu-id="77092-120">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="77092-120">Item number</span></span></th>
<th><span data-ttu-id="77092-121">Место</span><span class="sxs-lookup"><span data-stu-id="77092-121">Site</span></span></th>
<th><span data-ttu-id="77092-122">Количество</span><span class="sxs-lookup"><span data-stu-id="77092-122">Quantity</span></span></th>
<th><span data-ttu-id="77092-123">Ед. изм. складского учета</span><span class="sxs-lookup"><span data-stu-id="77092-123">Inventory unit</span></span></th>
<th><span data-ttu-id="77092-124">Значение</span><span class="sxs-lookup"><span data-stu-id="77092-124">Value</span></span></th>
<th><span data-ttu-id="77092-125">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="77092-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77092-126">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="77092-126">Cost object</span></span></td>
<td><span data-ttu-id="77092-127">A</span><span class="sxs-lookup"><span data-stu-id="77092-127">A</span></span></td>
<td><span data-ttu-id="77092-128">1</span><span class="sxs-lookup"><span data-stu-id="77092-128">1</span></span></td>
<td><span data-ttu-id="77092-129">150</span><span class="sxs-lookup"><span data-stu-id="77092-129">150</span></span></td>
<td><span data-ttu-id="77092-130">Шт.</span><span class="sxs-lookup"><span data-stu-id="77092-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="77092-131">1800,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="77092-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="77092-132">12,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="77092-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="77092-133">В следующей таблицы показан результат расчета для объекта запасов.</span><span class="sxs-lookup"><span data-stu-id="77092-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="77092-134">Результат можно просмотреть на странице **Объект затрат**, щелкнув **Физическое количество**.</span><span class="sxs-lookup"><span data-stu-id="77092-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77092-135">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="77092-135">Object type</span></span></th>
<th><span data-ttu-id="77092-136">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="77092-136">Item number</span></span></th>
<th><span data-ttu-id="77092-137">Сайт</span><span class="sxs-lookup"><span data-stu-id="77092-137">Site</span></span></th>
<th><span data-ttu-id="77092-138">Склад</span><span class="sxs-lookup"><span data-stu-id="77092-138">Warehouse</span></span></th>
<th><span data-ttu-id="77092-139">Партия №</span><span class="sxs-lookup"><span data-stu-id="77092-139">Batch No.</span></span></th>
<th><span data-ttu-id="77092-140">Количество</span><span class="sxs-lookup"><span data-stu-id="77092-140">Quantity</span></span></th>
<th><span data-ttu-id="77092-141">Ед. изм. складского учета</span><span class="sxs-lookup"><span data-stu-id="77092-141">Inventory unit</span></span></th>
<th><span data-ttu-id="77092-142">Значение</span><span class="sxs-lookup"><span data-stu-id="77092-142">Value</span></span></th>
<th><span data-ttu-id="77092-143">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="77092-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77092-144">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="77092-144">Inventory object</span></span></td>
<td><span data-ttu-id="77092-145">A</span><span class="sxs-lookup"><span data-stu-id="77092-145">A</span></span></td>
<td><span data-ttu-id="77092-146">1</span><span class="sxs-lookup"><span data-stu-id="77092-146">1</span></span></td>
<td><span data-ttu-id="77092-147">11</span><span class="sxs-lookup"><span data-stu-id="77092-147">11</span></span></td>
<td><span data-ttu-id="77092-148">B1</span><span class="sxs-lookup"><span data-stu-id="77092-148">B1</span></span></td>
<td><span data-ttu-id="77092-149">100</span><span class="sxs-lookup"><span data-stu-id="77092-149">100</span></span></td>
<td><span data-ttu-id="77092-150">Шт.</span><span class="sxs-lookup"><span data-stu-id="77092-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="77092-151">1200,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="77092-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="77092-152">12,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="77092-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77092-153">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="77092-153">Inventory object</span></span></td>
<td><span data-ttu-id="77092-154">A</span><span class="sxs-lookup"><span data-stu-id="77092-154">A</span></span></td>
<td><span data-ttu-id="77092-155">1</span><span class="sxs-lookup"><span data-stu-id="77092-155">1</span></span></td>
<td><span data-ttu-id="77092-156">11</span><span class="sxs-lookup"><span data-stu-id="77092-156">11</span></span></td>
<td><span data-ttu-id="77092-157">B2</span><span class="sxs-lookup"><span data-stu-id="77092-157">B2</span></span></td>
<td><span data-ttu-id="77092-158">50</span><span class="sxs-lookup"><span data-stu-id="77092-158">50</span></span></td>
<td><span data-ttu-id="77092-159">Шт.</span><span class="sxs-lookup"><span data-stu-id="77092-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="77092-160">600,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="77092-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="77092-161">12,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="77092-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="77092-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77092-162">Additional resources</span></span>
--------

[<span data-ttu-id="77092-163">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="77092-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="77092-164">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="77092-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="77092-165">Что нового и что изменилось</span><span class="sxs-lookup"><span data-stu-id="77092-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)




