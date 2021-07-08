---
title: Допуск задержки (отрицательные дни)
description: В этой теме приводятся сведения о расчете допуска задержки и его влиянии на создание спланированных заказов при оптимизации планирования.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306471"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="83f2f-103">Допуск задержки (отрицательные дни)</span><span class="sxs-lookup"><span data-stu-id="83f2f-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="83f2f-104">Функция допуска задержки позволяет оптимизировать планирование, чтобы учесть значение **Отрицательные дни**, заданное для групп покрытия.</span><span class="sxs-lookup"><span data-stu-id="83f2f-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="83f2f-105">Она используется для продления периода допуска задержки, который применяется при сводном планировании.</span><span class="sxs-lookup"><span data-stu-id="83f2f-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="83f2f-106">Таким образом можно избежать создания новых заказов на поставку, если существующие поставки смогут покрыть спрос после короткой задержки.</span><span class="sxs-lookup"><span data-stu-id="83f2f-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="83f2f-107">Целью функциональности является определение наличия смысла создания нового заказа на поставку для данного спроса.</span><span class="sxs-lookup"><span data-stu-id="83f2f-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="83f2f-108">Включите функцию в системе</span><span class="sxs-lookup"><span data-stu-id="83f2f-108">Turn on the feature in your system</span></span>

<span data-ttu-id="83f2f-109">Чтобы функция допуска задержки была доступна в системе, перейдите [Управление функциями](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите функцию *Отрицательные дни для оптимизации планирования*.</span><span class="sxs-lookup"><span data-stu-id="83f2f-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="83f2f-110">Допуск задержки при оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="83f2f-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="83f2f-111">Допуск задержки в днях представляет количество дней, превышающее время упреждения, в течение которого вы хотите ожидать, прежде чем заказ нового пополнения уже запланирован.</span><span class="sxs-lookup"><span data-stu-id="83f2f-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="83f2f-112">Допуск задержки определяется с помощью календарных дней, а не бизнес-дней.</span><span class="sxs-lookup"><span data-stu-id="83f2f-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="83f2f-113">Во время сводного планирования, когда система рассчитывает допуск задержки, она учитывает параметр **Отрицательные дни**.</span><span class="sxs-lookup"><span data-stu-id="83f2f-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="83f2f-114">Можно указать значение **Отрицательные дни** на странице **Группы покрытия** или **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="83f2f-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="83f2f-115">Система связывает расчет допуска задержки с *самой ранней датой пополнения*, которая равен сегодняшней дате плюс время упреждения.</span><span class="sxs-lookup"><span data-stu-id="83f2f-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="83f2f-116">Допуск задержки вычисляется с использованием следующей формулы, где *max()* обнаруживает большее из двух значений:</span><span class="sxs-lookup"><span data-stu-id="83f2f-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="83f2f-117">*max(самая ранняя дата пополнения, срок выполнения спроса)* – *Дата выполнения спроса* + *отрицательные дни*</span><span class="sxs-lookup"><span data-stu-id="83f2f-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="83f2f-118">Эта формула гарантирует, что сводное планирование не будет создавать новые заказы на поставку при наличии достаточных поставок в течение времени упреждения продуктов.</span><span class="sxs-lookup"><span data-stu-id="83f2f-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="83f2f-119">При расчете допуска задержки в оптимизации планирования всегда используется расчет динамических отрицательных дней из встроенного сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="83f2f-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="83f2f-120">Значение параметра **Использовать распространение отрицательных дней** на странице **Параметры сводного планирования** не оказывает влияния на эту работу.</span><span class="sxs-lookup"><span data-stu-id="83f2f-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="83f2f-121">Если существующие поставки подразумевают задержку спроса, которая меньше или равна вычисленному допуску задержки, оптимизация планирования сопоставляет существующие поставки со спросом.</span><span class="sxs-lookup"><span data-stu-id="83f2f-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="83f2f-122">В некоторых случаях лучше отложить спрос, а не выполнить перепоставку.</span><span class="sxs-lookup"><span data-stu-id="83f2f-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="83f2f-123">В следующих подразделах представлены примеры, демонстрирующие влияние допуска задержки на создание спланированных заказов при оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="83f2f-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="83f2f-124">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83f2f-124">Example 1</span></span>

<span data-ttu-id="83f2f-125">Продукт имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="83f2f-125">A product has the following configuration:</span></span>

- <span data-ttu-id="83f2f-126">**Время упреждения:** *10*</span><span class="sxs-lookup"><span data-stu-id="83f2f-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="83f2f-127">**Отрицательные дни:** *2*</span><span class="sxs-lookup"><span data-stu-id="83f2f-127">**Negative days:** *2*</span></span>

<span data-ttu-id="83f2f-128">Для продукта существуют следующие поставки и спрос:</span><span class="sxs-lookup"><span data-stu-id="83f2f-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="83f2f-129">**Спрос сегодня:** заказ на продажу для количества 10</span><span class="sxs-lookup"><span data-stu-id="83f2f-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="83f2f-130">**Поставка через 12 дней:** заказ на покупку для количества 10</span><span class="sxs-lookup"><span data-stu-id="83f2f-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="83f2f-131">Существующие поставки могут охватывать спрос в течение 12 дней, а этот период равен допуску задержки.</span><span class="sxs-lookup"><span data-stu-id="83f2f-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="83f2f-132">Таким образом, при выполнении сводного планирования спланированные заказы не создаются.</span><span class="sxs-lookup"><span data-stu-id="83f2f-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="83f2f-133">Пример 2</span><span class="sxs-lookup"><span data-stu-id="83f2f-133">Example 2</span></span>

<span data-ttu-id="83f2f-134">Продукт имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="83f2f-134">A product has the following configuration:</span></span>

- <span data-ttu-id="83f2f-135">**Время упреждения:** *10*</span><span class="sxs-lookup"><span data-stu-id="83f2f-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="83f2f-136">**Отрицательные дни:** *0*</span><span class="sxs-lookup"><span data-stu-id="83f2f-136">**Negative days:** *0*</span></span>

<span data-ttu-id="83f2f-137">Для продукта существуют следующие поставки и спрос:</span><span class="sxs-lookup"><span data-stu-id="83f2f-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="83f2f-138">**Спрос сегодня:** заказ на продажу для количества 10</span><span class="sxs-lookup"><span data-stu-id="83f2f-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="83f2f-139">**Поставка через 12 дней:** заказ на покупку для количества 10</span><span class="sxs-lookup"><span data-stu-id="83f2f-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="83f2f-140">Существующие поставки могут охватывать спрос только через 12 дней.</span><span class="sxs-lookup"><span data-stu-id="83f2f-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="83f2f-141">Однако допуск задержки составляет 10 дней.</span><span class="sxs-lookup"><span data-stu-id="83f2f-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="83f2f-142">Таким образом, при запуске сводного планирования создается спланированный заказ для количества 10.</span><span class="sxs-lookup"><span data-stu-id="83f2f-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="83f2f-143">Пример 3</span><span class="sxs-lookup"><span data-stu-id="83f2f-143">Example 3</span></span>

<span data-ttu-id="83f2f-144">Продукт имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="83f2f-144">A product has the following configuration:</span></span>

- <span data-ttu-id="83f2f-145">**Время упреждения:** *10*</span><span class="sxs-lookup"><span data-stu-id="83f2f-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="83f2f-146">**Отрицательные дни:** *2*</span><span class="sxs-lookup"><span data-stu-id="83f2f-146">**Negative days:** *2*</span></span>

<span data-ttu-id="83f2f-147">Для продукта существуют следующие поставки и спрос:</span><span class="sxs-lookup"><span data-stu-id="83f2f-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="83f2f-148">**Спрос через 11 дней:** заказ на продажу для количества 10</span><span class="sxs-lookup"><span data-stu-id="83f2f-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="83f2f-149">**Поставка через 14 дней:** заказ на покупку для количества 10</span><span class="sxs-lookup"><span data-stu-id="83f2f-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="83f2f-150">Существующие поставки могут охватывать спрос только через три дня.</span><span class="sxs-lookup"><span data-stu-id="83f2f-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="83f2f-151">Однако допуск задержки составляет два дня.</span><span class="sxs-lookup"><span data-stu-id="83f2f-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="83f2f-152">(В этом случае допуск задержки включает только два отрицательных дня.</span><span class="sxs-lookup"><span data-stu-id="83f2f-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="83f2f-153">Дата спроса не включена, поскольку она позже времени упреждения продукта.) Таким образом, при запуске сводного планирования создается спланированный заказ для количества 10.</span><span class="sxs-lookup"><span data-stu-id="83f2f-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
