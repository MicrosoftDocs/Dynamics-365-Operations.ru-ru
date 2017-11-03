---
title: "Объекты затрат"
description: "В этой статье представлена информация об объектах затрат и описан порядок накопления затрат и количеств. Объект затрат — объект, для которого накапливаются затраты и количества. Объект объекта затрат может быть или продуктом или вариантами продукта, такими как варианты для стиля и цвета."
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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1a1c964a890c0c59a01700a6987bfbdfe5a17ccb
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="cost-objects"></a><span data-ttu-id="015be-105">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="015be-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="015be-106">В этой статье представлена информация об объектах затрат и описан порядок накопления затрат и количеств.</span><span class="sxs-lookup"><span data-stu-id="015be-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="015be-107">Объект затрат — объект, для которого накапливаются затраты и количества.</span><span class="sxs-lookup"><span data-stu-id="015be-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="015be-108">Объект объекта затрат может быть или продуктом или вариантами продукта, такими как варианты для стиля и цвета.</span><span class="sxs-lookup"><span data-stu-id="015be-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="015be-109">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="015be-109">Cost objects</span></span>

<span data-ttu-id="015be-110">На странице **Объекты затрат** перечислены все объекты затрат, зарегистрированные для продукта.</span><span class="sxs-lookup"><span data-stu-id="015be-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="015be-111">Объекты затрат определяются данными из следующих источников:</span><span class="sxs-lookup"><span data-stu-id="015be-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="015be-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="015be-112">Product</span></span>
-   <span data-ttu-id="015be-113">Группа аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="015be-113">Product dimension group</span></span>
-   <span data-ttu-id="015be-114">Группа аналитик хранения</span><span class="sxs-lookup"><span data-stu-id="015be-114">Storage dimension group</span></span>
-   <span data-ttu-id="015be-115">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="015be-115">Tracking dimension group</span></span>

<span data-ttu-id="015be-116">**Примечание.** Объект затрат представляет только элемент затрат типа **Основные материалы**.</span><span class="sxs-lookup"><span data-stu-id="015be-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="015be-117">Объект затрат и объект запасов отличаются тем, что объект затрат определяется складскими аналитиками, выбранными для финансовых запасов.</span><span class="sxs-lookup"><span data-stu-id="015be-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="015be-118">Например, номенклатура имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="015be-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="015be-119">**Сайт:** физические запасы = да, финансовые запасы = да</span><span class="sxs-lookup"><span data-stu-id="015be-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="015be-120">**Склад:** физические запасы = да, финансовые запасы = нет</span><span class="sxs-lookup"><span data-stu-id="015be-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="015be-121">**Партия №:** физические запасы = да, финансовые запасы = нет</span><span class="sxs-lookup"><span data-stu-id="015be-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="015be-122">В следующей таблице показано, что такое объект затрат и что такое объект запасов.</span><span class="sxs-lookup"><span data-stu-id="015be-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="015be-123">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="015be-123">Object type</span></span>      | <span data-ttu-id="015be-124">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="015be-124">Item number</span></span> | <span data-ttu-id="015be-125">Место</span><span class="sxs-lookup"><span data-stu-id="015be-125">Site</span></span> | <span data-ttu-id="015be-126">Склад</span><span class="sxs-lookup"><span data-stu-id="015be-126">Warehouse</span></span> | <span data-ttu-id="015be-127">Партия №</span><span class="sxs-lookup"><span data-stu-id="015be-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="015be-128">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="015be-128">Cost object</span></span>      | <span data-ttu-id="015be-129">х</span><span class="sxs-lookup"><span data-stu-id="015be-129">x</span></span>           | <span data-ttu-id="015be-130">х</span><span class="sxs-lookup"><span data-stu-id="015be-130">x</span></span>    |           |           |
| <span data-ttu-id="015be-131">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="015be-131">Inventory object</span></span> | <span data-ttu-id="015be-132">х</span><span class="sxs-lookup"><span data-stu-id="015be-132">x</span></span>           | <span data-ttu-id="015be-133">х</span><span class="sxs-lookup"><span data-stu-id="015be-133">x</span></span>    |  <span data-ttu-id="015be-134">х</span><span class="sxs-lookup"><span data-stu-id="015be-134">x</span></span>        | <span data-ttu-id="015be-135">х</span><span class="sxs-lookup"><span data-stu-id="015be-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="015be-136">Накопление затрат и количеств</span><span class="sxs-lookup"><span data-stu-id="015be-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="015be-137">Значение в поле **Стоимость** — это сумма следующих значений:</span><span class="sxs-lookup"><span data-stu-id="015be-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="015be-138">Физ. сумма</span><span class="sxs-lookup"><span data-stu-id="015be-138">Physical cost amount</span></span>
    -   <span data-ttu-id="015be-139">Фин. сумма</span><span class="sxs-lookup"><span data-stu-id="015be-139">Financial cost amount</span></span>
    -   <span data-ttu-id="015be-140">Корректировки</span><span class="sxs-lookup"><span data-stu-id="015be-140">Adjustments</span></span>
-   <span data-ttu-id="015be-141">Значение в поле **Количество** — это сумма следующих значений:</span><span class="sxs-lookup"><span data-stu-id="015be-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="015be-142">Получено</span><span class="sxs-lookup"><span data-stu-id="015be-142">Received</span></span>
    -   <span data-ttu-id="015be-143">Отпущено</span><span class="sxs-lookup"><span data-stu-id="015be-143">Deducted</span></span>
    -   <span data-ttu-id="015be-144">Разнесенное количество</span><span class="sxs-lookup"><span data-stu-id="015be-144">Posted quantity</span></span>
-   <span data-ttu-id="015be-145">Поле **Средняя стоимость единицы** — это расчетное поле.</span><span class="sxs-lookup"><span data-stu-id="015be-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="015be-146">Значение рассчитывается путем деления значения **Стоимость** на значение **Количество**.</span><span class="sxs-lookup"><span data-stu-id="015be-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="015be-147">**Примечание.** Параметр **Включать физическую стоимость** не влияет на предшествующие расчеты.</span><span class="sxs-lookup"><span data-stu-id="015be-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="015be-148">См. также</span><span class="sxs-lookup"><span data-stu-id="015be-148">See also</span></span>
--------

[<span data-ttu-id="015be-149">Группа аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="015be-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="015be-150">Группа аналитик хранения</span><span class="sxs-lookup"><span data-stu-id="015be-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="015be-151">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="015be-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="015be-152">Что нового и что изменилось</span><span class="sxs-lookup"><span data-stu-id="015be-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="015be-153">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="015be-153">Cost entries</span></span>](cost-entries.md)




