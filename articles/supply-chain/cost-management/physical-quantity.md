---
title: Значения объекта запасов
description: В этой статье представлена информация о том, как рассчитываются значения объекта запасов.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff3a21e87b9cb0bb371b0772c948cb62a4cb36b1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214627"
---
# <a name="inventory-object-values"></a><span data-ttu-id="1d257-103">Значения объекта запасов</span><span class="sxs-lookup"><span data-stu-id="1d257-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d257-104">В этой статье представлена информация о том, как рассчитываются значения объекта запасов.</span><span class="sxs-lookup"><span data-stu-id="1d257-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="1d257-105">Новая функция **Физическое количество** позволяет просматривать значения определенного объекта запасов.</span><span class="sxs-lookup"><span data-stu-id="1d257-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="1d257-106">Объект затрат представляет уровень объекта, на котором выполняется учет запасов.</span><span class="sxs-lookup"><span data-stu-id="1d257-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="1d257-107">Дополнительные сведения об объектах затрат см. в разделе [Объекты затрат](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="1d257-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="1d257-108">Чтобы просмотреть значения определенного объекта запасов, щелкните **Физическое количество** на странице **Объект затрат**.</span><span class="sxs-lookup"><span data-stu-id="1d257-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="1d257-109">Вот как вычисляется значение объекта запасов:</span><span class="sxs-lookup"><span data-stu-id="1d257-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="1d257-110">Объект запасов.Значение = Объект затрат.Средняя себестоимость единицы × Объект запасов.Количество</span><span class="sxs-lookup"><span data-stu-id="1d257-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="1d257-111">В следующем примере показано, как вычисляются значения объекта запасов и объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="1d257-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="1d257-112">Два события поступления продуктов зарегистрированы в номенклатуре А:</span><span class="sxs-lookup"><span data-stu-id="1d257-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="1d257-113">Поступление продуктов 1: количество = 100 шт., сумма = 1000,00 долларов США, сайт = 1, склад =11, номер партии</span><span class="sxs-lookup"><span data-stu-id="1d257-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="1d257-114">= B1</span><span class="sxs-lookup"><span data-stu-id="1d257-114">= B1</span></span>
-   <span data-ttu-id="1d257-115">Поступление продуктов 2: количество = 50 шт., сумма = 800,00 долларов США, сайт = 1, склад =11, номер партии</span><span class="sxs-lookup"><span data-stu-id="1d257-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="1d257-116">= B2</span><span class="sxs-lookup"><span data-stu-id="1d257-116">= B2</span></span>

<span data-ttu-id="1d257-117">В следующей таблицы показан результат расчета для объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="1d257-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="1d257-118">Результат можно просмотреть на странице **Объект затрат**.</span><span class="sxs-lookup"><span data-stu-id="1d257-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="1d257-119">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="1d257-119">Object type</span></span></th>
<th><span data-ttu-id="1d257-120">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1d257-120">Item number</span></span></th>
<th><span data-ttu-id="1d257-121">Место</span><span class="sxs-lookup"><span data-stu-id="1d257-121">Site</span></span></th>
<th><span data-ttu-id="1d257-122">Количество</span><span class="sxs-lookup"><span data-stu-id="1d257-122">Quantity</span></span></th>
<th><span data-ttu-id="1d257-123">Ед. изм. складского учета</span><span class="sxs-lookup"><span data-stu-id="1d257-123">Inventory unit</span></span></th>
<th><span data-ttu-id="1d257-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1d257-124">Value</span></span></th>
<th><span data-ttu-id="1d257-125">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="1d257-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d257-126">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1d257-126">Cost object</span></span></td>
<td><span data-ttu-id="1d257-127">A</span><span class="sxs-lookup"><span data-stu-id="1d257-127">A</span></span></td>
<td><span data-ttu-id="1d257-128">1</span><span class="sxs-lookup"><span data-stu-id="1d257-128">1</span></span></td>
<td><span data-ttu-id="1d257-129">150</span><span class="sxs-lookup"><span data-stu-id="1d257-129">150</span></span></td>
<td><span data-ttu-id="1d257-130">Шт.</span><span class="sxs-lookup"><span data-stu-id="1d257-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="1d257-131">1800,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="1d257-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="1d257-132">12,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="1d257-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d257-133">В следующей таблицы показан результат расчета для объекта запасов.</span><span class="sxs-lookup"><span data-stu-id="1d257-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="1d257-134">Результат можно просмотреть на странице **Объект затрат**, щелкнув **Физическое количество**.</span><span class="sxs-lookup"><span data-stu-id="1d257-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="1d257-135">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="1d257-135">Object type</span></span></th>
<th><span data-ttu-id="1d257-136">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1d257-136">Item number</span></span></th>
<th><span data-ttu-id="1d257-137">Сайт</span><span class="sxs-lookup"><span data-stu-id="1d257-137">Site</span></span></th>
<th><span data-ttu-id="1d257-138">Склад</span><span class="sxs-lookup"><span data-stu-id="1d257-138">Warehouse</span></span></th>
<th><span data-ttu-id="1d257-139">Партия №</span><span class="sxs-lookup"><span data-stu-id="1d257-139">Batch No.</span></span></th>
<th><span data-ttu-id="1d257-140">Количество</span><span class="sxs-lookup"><span data-stu-id="1d257-140">Quantity</span></span></th>
<th><span data-ttu-id="1d257-141">Ед. изм. складского учета</span><span class="sxs-lookup"><span data-stu-id="1d257-141">Inventory unit</span></span></th>
<th><span data-ttu-id="1d257-142">Значение</span><span class="sxs-lookup"><span data-stu-id="1d257-142">Value</span></span></th>
<th><span data-ttu-id="1d257-143">Средняя стоимость единицы</span><span class="sxs-lookup"><span data-stu-id="1d257-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d257-144">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="1d257-144">Inventory object</span></span></td>
<td><span data-ttu-id="1d257-145">A</span><span class="sxs-lookup"><span data-stu-id="1d257-145">A</span></span></td>
<td><span data-ttu-id="1d257-146">1</span><span class="sxs-lookup"><span data-stu-id="1d257-146">1</span></span></td>
<td><span data-ttu-id="1d257-147">11</span><span class="sxs-lookup"><span data-stu-id="1d257-147">11</span></span></td>
<td><span data-ttu-id="1d257-148">B1</span><span class="sxs-lookup"><span data-stu-id="1d257-148">B1</span></span></td>
<td><span data-ttu-id="1d257-149">100</span><span class="sxs-lookup"><span data-stu-id="1d257-149">100</span></span></td>
<td><span data-ttu-id="1d257-150">Шт.</span><span class="sxs-lookup"><span data-stu-id="1d257-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="1d257-151">1200,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="1d257-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="1d257-152">12,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="1d257-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d257-153">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="1d257-153">Inventory object</span></span></td>
<td><span data-ttu-id="1d257-154">A</span><span class="sxs-lookup"><span data-stu-id="1d257-154">A</span></span></td>
<td><span data-ttu-id="1d257-155">1</span><span class="sxs-lookup"><span data-stu-id="1d257-155">1</span></span></td>
<td><span data-ttu-id="1d257-156">11</span><span class="sxs-lookup"><span data-stu-id="1d257-156">11</span></span></td>
<td><span data-ttu-id="1d257-157">B2</span><span class="sxs-lookup"><span data-stu-id="1d257-157">B2</span></span></td>
<td><span data-ttu-id="1d257-158">50</span><span class="sxs-lookup"><span data-stu-id="1d257-158">50</span></span></td>
<td><span data-ttu-id="1d257-159">Шт.</span><span class="sxs-lookup"><span data-stu-id="1d257-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="1d257-160">600,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="1d257-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="1d257-161">12,00 долларов США</span><span class="sxs-lookup"><span data-stu-id="1d257-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="1d257-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d257-162">Additional resources</span></span>
--------

[<span data-ttu-id="1d257-163">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="1d257-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="1d257-164">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="1d257-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="1d257-165">Что нового и что изменилось</span><span class="sxs-lookup"><span data-stu-id="1d257-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



