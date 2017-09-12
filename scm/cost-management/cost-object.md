---
title: "Объекты затрат"
description: "В этой статье представлена информация об объектах затрат и описан порядок накопления затрат и количеств. Объект затрат — объект, для которого накапливаются затраты и количества. Объект объекта затрат может быть или продуктом или вариантами продукта, такими как варианты для стиля и цвета."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d43ea6c0d80a1602f298bbbedb88dd8f7decca4e
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="cost-objects"></a><span data-ttu-id="4993a-105">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="4993a-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4993a-106">В этой статье представлена информация об объектах затрат и описан порядок накопления затрат и количеств.</span><span class="sxs-lookup"><span data-stu-id="4993a-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="4993a-107">Объект затрат — объект, для которого накапливаются затраты и количества.</span><span class="sxs-lookup"><span data-stu-id="4993a-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="4993a-108">Объект объекта затрат может быть или продуктом или вариантами продукта, такими как варианты для стиля и цвета.</span><span class="sxs-lookup"><span data-stu-id="4993a-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

<a name="cost-objects"></a><span data-ttu-id="4993a-109">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="4993a-109">Cost objects</span></span>
------------

<span data-ttu-id="4993a-110">На странице **Объекты затрат** перечислены все объекты затрат, зарегистрированные для продукта.</span><span class="sxs-lookup"><span data-stu-id="4993a-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="4993a-111">Объекты затрат определяются данными из следующих источников:</span><span class="sxs-lookup"><span data-stu-id="4993a-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="4993a-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="4993a-112">Product</span></span>
-   <span data-ttu-id="4993a-113">Группа аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="4993a-113">Product dimension group</span></span>
-   <span data-ttu-id="4993a-114">Группа аналитик хранения</span><span class="sxs-lookup"><span data-stu-id="4993a-114">Storage dimension group</span></span>
-   <span data-ttu-id="4993a-115">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="4993a-115">Tracking dimension group</span></span>

<span data-ttu-id="4993a-116">**Примечание.** Объект затрат представляет только элемент затрат типа **Основные материалы**.</span><span class="sxs-lookup"><span data-stu-id="4993a-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="4993a-117">Объект затрат и объект запасов отличаются тем, что объект затрат определяется складскими аналитиками, выбранными для финансовых запасов.</span><span class="sxs-lookup"><span data-stu-id="4993a-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="4993a-118">Например, номенклатура имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="4993a-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="4993a-119">**Сайт:** физические запасы = да, финансовые запасы = да</span><span class="sxs-lookup"><span data-stu-id="4993a-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="4993a-120">**Склад:** физические запасы = да, финансовые запасы = нет</span><span class="sxs-lookup"><span data-stu-id="4993a-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="4993a-121">**Партия №:** физические запасы = да, финансовые запасы = нет</span><span class="sxs-lookup"><span data-stu-id="4993a-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="4993a-122">В следующей таблице показано, что такое объект затрат и что такое объект запасов.</span><span class="sxs-lookup"><span data-stu-id="4993a-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="4993a-123">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="4993a-123">Object type</span></span>      | <span data-ttu-id="4993a-124">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="4993a-124">Item number</span></span> | <span data-ttu-id="4993a-125">Место</span><span class="sxs-lookup"><span data-stu-id="4993a-125">Site</span></span> | <span data-ttu-id="4993a-126">Склад</span><span class="sxs-lookup"><span data-stu-id="4993a-126">Warehouse</span></span> | <span data-ttu-id="4993a-127">Партия №</span><span class="sxs-lookup"><span data-stu-id="4993a-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="4993a-128">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4993a-128">Cost object</span></span>      | <span data-ttu-id="4993a-129">х</span><span class="sxs-lookup"><span data-stu-id="4993a-129">x</span></span>           | <span data-ttu-id="4993a-130">х</span><span class="sxs-lookup"><span data-stu-id="4993a-130">x</span></span>    |           |           |
| <span data-ttu-id="4993a-131">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="4993a-131">Inventory object</span></span> | <span data-ttu-id="4993a-132">х</span><span class="sxs-lookup"><span data-stu-id="4993a-132">x</span></span>           | <span data-ttu-id="4993a-133">х</span><span class="sxs-lookup"><span data-stu-id="4993a-133">x</span></span>    |  <span data-ttu-id="4993a-134">х</span><span class="sxs-lookup"><span data-stu-id="4993a-134">x</span></span>        | <span data-ttu-id="4993a-135">х</span><span class="sxs-lookup"><span data-stu-id="4993a-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="4993a-136">Накопление затрат и количеств</span><span class="sxs-lookup"><span data-stu-id="4993a-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="4993a-137">Значение в поле **Стоимость** — это сумма следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4993a-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="4993a-138">Физ. сумма</span><span class="sxs-lookup"><span data-stu-id="4993a-138">Physical cost amount</span></span>
    -   <span data-ttu-id="4993a-139">Фин. сумма</span><span class="sxs-lookup"><span data-stu-id="4993a-139">Financial cost amount</span></span>
    -   <span data-ttu-id="4993a-140">Корректировки</span><span class="sxs-lookup"><span data-stu-id="4993a-140">Adjustments</span></span>
-   <span data-ttu-id="4993a-141">Значение в поле **Количество** — это сумма следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4993a-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="4993a-142">Получено</span><span class="sxs-lookup"><span data-stu-id="4993a-142">Received</span></span>
    -   <span data-ttu-id="4993a-143">Отпущено</span><span class="sxs-lookup"><span data-stu-id="4993a-143">Deducted</span></span>
    -   <span data-ttu-id="4993a-144">Разнесенное количество</span><span class="sxs-lookup"><span data-stu-id="4993a-144">Posted quantity</span></span>
-   <span data-ttu-id="4993a-145">Поле **Средняя стоимость единицы** — это расчетное поле.</span><span class="sxs-lookup"><span data-stu-id="4993a-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="4993a-146">Значение рассчитывается путем деления значения **Стоимость** на значение **Количество**.</span><span class="sxs-lookup"><span data-stu-id="4993a-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="4993a-147">**Примечание.** Параметр **Включать физическую стоимость** не влияет на предшествующие расчеты.</span><span class="sxs-lookup"><span data-stu-id="4993a-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="4993a-148">См. также</span><span class="sxs-lookup"><span data-stu-id="4993a-148">See also</span></span>
--------

[<span data-ttu-id="4993a-149">Группа аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="4993a-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="4993a-150">Группа аналитик хранения</span><span class="sxs-lookup"><span data-stu-id="4993a-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="4993a-151">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="4993a-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="4993a-152">Что нового и что изменилось</span><span class="sxs-lookup"><span data-stu-id="4993a-152">What's new or changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[<span data-ttu-id="4993a-153">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="4993a-153">Cost entries</span></span>](cost-entries.md)




