---
title: Объекты затрат
description: В этой статье представлена информация об объектах затрат и описан порядок накопления затрат и количеств. Объект затрат — объект, для которого накапливаются затраты и количества. Объект объекта затрат может быть или продуктом или вариантами продукта, такими как варианты для стиля и цвета.
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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee7c170d5a330c0080931a67c1548eb0d3522bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232406"
---
# <a name="cost-objects"></a><span data-ttu-id="cd44b-105">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="cd44b-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd44b-106">В этой статье представлена информация об объектах затрат и описан порядок накопления затрат и количеств.</span><span class="sxs-lookup"><span data-stu-id="cd44b-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="cd44b-107">Объект затрат — объект, для которого накапливаются затраты и количества.</span><span class="sxs-lookup"><span data-stu-id="cd44b-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="cd44b-108">Объект объекта затрат может быть или продуктом или вариантами продукта, такими как варианты для стиля и цвета.</span><span class="sxs-lookup"><span data-stu-id="cd44b-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="cd44b-109">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="cd44b-109">Cost objects</span></span>

<span data-ttu-id="cd44b-110">На странице **Объекты затрат** перечислены все объекты затрат, зарегистрированные для продукта.</span><span class="sxs-lookup"><span data-stu-id="cd44b-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="cd44b-111">Объекты затрат определяются данными из следующих источников:</span><span class="sxs-lookup"><span data-stu-id="cd44b-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="cd44b-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="cd44b-112">Product</span></span>
-   <span data-ttu-id="cd44b-113">Группа аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="cd44b-113">Product dimension group</span></span>
-   <span data-ttu-id="cd44b-114">Группа аналитик хранения</span><span class="sxs-lookup"><span data-stu-id="cd44b-114">Storage dimension group</span></span>
-   <span data-ttu-id="cd44b-115">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="cd44b-115">Tracking dimension group</span></span>

<span data-ttu-id="cd44b-116">**Примечание.** Объект затрат представляет только элемент затрат типа **Основные материалы**.</span><span class="sxs-lookup"><span data-stu-id="cd44b-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="cd44b-117">Объект затрат и объект запасов отличаются тем, что объект затрат определяется складскими аналитиками, выбранными для финансовых запасов.</span><span class="sxs-lookup"><span data-stu-id="cd44b-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="cd44b-118">Например, номенклатура имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="cd44b-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="cd44b-119">**Сайт:** физические запасы = да, финансовые запасы = да</span><span class="sxs-lookup"><span data-stu-id="cd44b-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="cd44b-120">**Склад:** физические запасы = да, финансовые запасы = нет</span><span class="sxs-lookup"><span data-stu-id="cd44b-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="cd44b-121">**Партия №:** физические запасы = да, финансовые запасы = нет</span><span class="sxs-lookup"><span data-stu-id="cd44b-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="cd44b-122">В следующей таблице показано, что такое объект затрат и что такое объект запасов.</span><span class="sxs-lookup"><span data-stu-id="cd44b-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="cd44b-123">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="cd44b-123">Object type</span></span>      | <span data-ttu-id="cd44b-124">Номер номенклатуры</span><span class="sxs-lookup"><span data-stu-id="cd44b-124">Item number</span></span> | <span data-ttu-id="cd44b-125">Место</span><span class="sxs-lookup"><span data-stu-id="cd44b-125">Site</span></span> | <span data-ttu-id="cd44b-126">Склад</span><span class="sxs-lookup"><span data-stu-id="cd44b-126">Warehouse</span></span> | <span data-ttu-id="cd44b-127">Партия №</span><span class="sxs-lookup"><span data-stu-id="cd44b-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="cd44b-128">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="cd44b-128">Cost object</span></span>      | <span data-ttu-id="cd44b-129">х</span><span class="sxs-lookup"><span data-stu-id="cd44b-129">x</span></span>           | <span data-ttu-id="cd44b-130">х</span><span class="sxs-lookup"><span data-stu-id="cd44b-130">x</span></span>    |           |           |
| <span data-ttu-id="cd44b-131">Объект запасов</span><span class="sxs-lookup"><span data-stu-id="cd44b-131">Inventory object</span></span> | <span data-ttu-id="cd44b-132">х</span><span class="sxs-lookup"><span data-stu-id="cd44b-132">x</span></span>           | <span data-ttu-id="cd44b-133">х</span><span class="sxs-lookup"><span data-stu-id="cd44b-133">x</span></span>    |  <span data-ttu-id="cd44b-134">х</span><span class="sxs-lookup"><span data-stu-id="cd44b-134">x</span></span>        | <span data-ttu-id="cd44b-135">х</span><span class="sxs-lookup"><span data-stu-id="cd44b-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="cd44b-136">Накопление затрат и количеств</span><span class="sxs-lookup"><span data-stu-id="cd44b-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="cd44b-137">Значение в поле **Стоимость** — это сумма следующих значений:</span><span class="sxs-lookup"><span data-stu-id="cd44b-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="cd44b-138">Физ. сумма</span><span class="sxs-lookup"><span data-stu-id="cd44b-138">Physical cost amount</span></span>
    -   <span data-ttu-id="cd44b-139">Фин. сумма</span><span class="sxs-lookup"><span data-stu-id="cd44b-139">Financial cost amount</span></span>
    -   <span data-ttu-id="cd44b-140">Корректировки</span><span class="sxs-lookup"><span data-stu-id="cd44b-140">Adjustments</span></span>
-   <span data-ttu-id="cd44b-141">Значение в поле **Количество** — это сумма следующих значений:</span><span class="sxs-lookup"><span data-stu-id="cd44b-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="cd44b-142">Получено</span><span class="sxs-lookup"><span data-stu-id="cd44b-142">Received</span></span>
    -   <span data-ttu-id="cd44b-143">Отпущено</span><span class="sxs-lookup"><span data-stu-id="cd44b-143">Deducted</span></span>
    -   <span data-ttu-id="cd44b-144">Разнесенное количество</span><span class="sxs-lookup"><span data-stu-id="cd44b-144">Posted quantity</span></span>
-   <span data-ttu-id="cd44b-145">Поле **Средняя стоимость единицы** — это расчетное поле.</span><span class="sxs-lookup"><span data-stu-id="cd44b-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="cd44b-146">Значение рассчитывается путем деления значения **Стоимость** на значение **Количество**.</span><span class="sxs-lookup"><span data-stu-id="cd44b-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="cd44b-147">**Примечание.** Параметр **Включать физическую стоимость** не влияет на предшествующие расчеты.</span><span class="sxs-lookup"><span data-stu-id="cd44b-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cd44b-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cd44b-148">Additional resources</span></span>
--------

[<span data-ttu-id="cd44b-149">Группа аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="cd44b-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="cd44b-150">Группа аналитик хранения</span><span class="sxs-lookup"><span data-stu-id="cd44b-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="cd44b-151">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="cd44b-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="cd44b-152">Что нового и что изменилось</span><span class="sxs-lookup"><span data-stu-id="cd44b-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="cd44b-153">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="cd44b-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]