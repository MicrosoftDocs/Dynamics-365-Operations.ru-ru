---
title: Планирование с отрицательными количествами в наличии
description: В этом разделе объясняется, как отрицательные запасы в наличии обрабатываются при использовании оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983474"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="d82d1-103">Планирование с отрицательными количествами в наличии</span><span class="sxs-lookup"><span data-stu-id="d82d1-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d82d1-104">Если в системе отображается отрицательное агрегированное количество в наличии, механизм планирования рассматривает количество как 0 (ноль), чтобы избежать избыточного запаса.</span><span class="sxs-lookup"><span data-stu-id="d82d1-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="d82d1-105">Вот как работают эти функции:</span><span class="sxs-lookup"><span data-stu-id="d82d1-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="d82d1-106">Функция оптимизации планирования объединяет количества в наличии на самом нижнем уровне аналитик покрытия.</span><span class="sxs-lookup"><span data-stu-id="d82d1-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="d82d1-107">(Например, если *местоположение* не является аналитикой покрытия, оптимизация по планированию объединяет количества в наличии на уровне *склада*.)</span><span class="sxs-lookup"><span data-stu-id="d82d1-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="d82d1-108">Если агрегированное количество в наличии на самом нижнем уровне аналитик покрытия имеет отрицательное значение, система предполагает, что количество в наличии действительно равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="d82d1-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d82d1-109">Система планирования может точно соответствовать входным данным.</span><span class="sxs-lookup"><span data-stu-id="d82d1-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="d82d1-110">Если введенные данные неточны, отрицательные записи в наличии будут указывать на то, что сведения о запасах в Microsoft Dynamics 365 Supply Chain Management не синхронизированы с реальным миром.</span><span class="sxs-lookup"><span data-stu-id="d82d1-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="d82d1-111">Таким образом, результат планирования будет ошибочным.</span><span class="sxs-lookup"><span data-stu-id="d82d1-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="d82d1-112">Чтобы получить точные результаты планирования, следует свести к минимуму число записей, которое будет показывать отрицательное количество в наличии.</span><span class="sxs-lookup"><span data-stu-id="d82d1-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="d82d1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d82d1-113">Example 1</span></span>

<span data-ttu-id="d82d1-114">Склад 13 настраивается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d82d1-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="d82d1-115">**Код покрытия:** Мин/макс.</span><span class="sxs-lookup"><span data-stu-id="d82d1-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="d82d1-116">**Минимум:** 15 штук (шт.)</span><span class="sxs-lookup"><span data-stu-id="d82d1-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="d82d1-117">**Максимум:** 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="d82d1-118">Самый нижний уровень аналитик покрытия — *склад*, а следующие количества в наличии записываются на уровне *местоположения*:</span><span class="sxs-lookup"><span data-stu-id="d82d1-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="d82d1-119">**Узел 1, Склад 13, местоположение 1:** 20 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="d82d1-120">**Узел 1, Склад 13, местоположение 2:** &minus;8 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="d82d1-121">Таким образом, агрегированное количество в наличии для склада 13 равно 12 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="d82d1-122">(= 20 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-122">(= 20 pcs.</span></span> <span data-ttu-id="d82d1-123">&minus; 8 шт.).</span><span class="sxs-lookup"><span data-stu-id="d82d1-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="d82d1-124">В этом случае механизм планирования использует совокупное количество в наличии, равное 12 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="d82d1-125">для склада 13.</span><span class="sxs-lookup"><span data-stu-id="d82d1-125">for warehouse 13.</span></span>

<span data-ttu-id="d82d1-126">В результате будет создан спланированный заказ на 13 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="d82d1-127">(= 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-127">(= 25 pcs.</span></span> <span data-ttu-id="d82d1-128">&minus; 12 шт.) для пополнения на складе 13 с 12 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="d82d1-129">до 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="d82d1-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d82d1-130">Example 2</span></span>

<span data-ttu-id="d82d1-131">Склад 13 настраивается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d82d1-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="d82d1-132">**Код покрытия:** Мин/макс.</span><span class="sxs-lookup"><span data-stu-id="d82d1-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="d82d1-133">**Минимум:** 15 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="d82d1-134">**Максимум:** 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="d82d1-135">Самый нижний уровень аналитик покрытия — *склад*, а следующие количества в наличии записываются на уровне *местоположения*:</span><span class="sxs-lookup"><span data-stu-id="d82d1-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="d82d1-136">**Узел 1, Склад 13, местоположение 1:** 4 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="d82d1-137">**Узел 1, Склад 13, местоположение 2:** &minus;8 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="d82d1-138">Таким образом, агрегированное количество в наличии для склада 13 равно &minus;4 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="d82d1-139">(= 4 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-139">(= 4 pcs.</span></span> <span data-ttu-id="d82d1-140">&minus; 8 шт.).</span><span class="sxs-lookup"><span data-stu-id="d82d1-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="d82d1-141">Другими словами, это меньше 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="d82d1-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="d82d1-142">В этом случае механизм планирования предполагает, что количество в наличии для склада 13 равно 0 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="d82d1-143">вместо &minus;4 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="d82d1-144">В результате будет создан спланированный заказ на 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="d82d1-145">(= 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-145">(= 25 pcs.</span></span> <span data-ttu-id="d82d1-146">&minus; 0 шт.) для пополнения на складе 13 с 0 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="d82d1-147">до 25 шт.</span><span class="sxs-lookup"><span data-stu-id="d82d1-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d82d1-148">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d82d1-148">Related resources</span></span>

[<span data-ttu-id="d82d1-149">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="d82d1-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="d82d1-150">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="d82d1-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="d82d1-151">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="d82d1-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="d82d1-152">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="d82d1-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="d82d1-153">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="d82d1-153">Cancel a planning job</span></span>](cancel-planning-job.md)
