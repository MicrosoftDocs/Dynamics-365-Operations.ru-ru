---
title: Методы пополнения и изменение количества
description: В этой теме представлена информация о методах пополнения в оптимизации планирования. Она также объясняет, как количество нескольких заказов на продукт влияет на результат.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261704"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="d8823-104">Методы пополнения и изменение количества</span><span class="sxs-lookup"><span data-stu-id="d8823-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8823-105">В этой теме представлена информация о методах пополнения в оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="d8823-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="d8823-106">Она также объясняет, как количество нескольких заказов на продукт влияет на результат.</span><span class="sxs-lookup"><span data-stu-id="d8823-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="d8823-107">Методы пополнения также известны как методы покрытия и методы размера лота.</span><span class="sxs-lookup"><span data-stu-id="d8823-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="d8823-108">Коды покрытия</span><span class="sxs-lookup"><span data-stu-id="d8823-108">Coverage codes</span></span>

<span data-ttu-id="d8823-109">Оптимизация планирования может быть настроена для использования различных методов пополнения.</span><span class="sxs-lookup"><span data-stu-id="d8823-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="d8823-110">Методы пополнения являются методиками, которые система использует для расчета требований к продукту.</span><span class="sxs-lookup"><span data-stu-id="d8823-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="d8823-111">Методы пополнения определяются кодами покрытия, которые можно настроить как для группы покрытия, так и для продукта.</span><span class="sxs-lookup"><span data-stu-id="d8823-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="d8823-112">При оптимизации планирования можно использовать следующие коды покрытия:</span><span class="sxs-lookup"><span data-stu-id="d8823-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="d8823-113">**Период** — метод пополнения, объединяющий весь спрос за период в один заказ для продукта.</span><span class="sxs-lookup"><span data-stu-id="d8823-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="d8823-114">Заказ будет запланирован для первого дня периода, и его количество будет соответствовать требованиям нетто за установленный период.</span><span class="sxs-lookup"><span data-stu-id="d8823-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="d8823-115">Период начинается с первого спроса продукта и охватывает определенную продолжительность времени.</span><span class="sxs-lookup"><span data-stu-id="d8823-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="d8823-116">Следующий период начнется со следующих потребностей в продукте.</span><span class="sxs-lookup"><span data-stu-id="d8823-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="d8823-117">Код покрытия *Период* часто используется для непредсказуемого извлечения запасов, сезонных продуктов или продуктов с высокой стоимостью.</span><span class="sxs-lookup"><span data-stu-id="d8823-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="d8823-118">Следующая иллюстрация показывает пример.</span><span class="sxs-lookup"><span data-stu-id="d8823-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="d8823-119">![Пример использования кода покрытия периода](./media/coverage-code-period.png "Пример использования кода покрытия периода")</span><span class="sxs-lookup"><span data-stu-id="d8823-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="d8823-120">**Требование** — метод пополнения, при котором система создает запланированный заказ на покупку, перемещение или производство в соответствии с потребностью для данного продукта.</span><span class="sxs-lookup"><span data-stu-id="d8823-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="d8823-121">Этот метод используется для дорогих продуктов, которые имеют прерывистый спрос.</span><span class="sxs-lookup"><span data-stu-id="d8823-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="d8823-122">Код покрытия *Требование* часто используется для настраиваемых продуктов или сценариев "под заказ".</span><span class="sxs-lookup"><span data-stu-id="d8823-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="d8823-123">Следующая иллюстрация показывает пример.</span><span class="sxs-lookup"><span data-stu-id="d8823-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="d8823-124">![Пример использования кода покрытия требования](./media/coverage-code-requirement.png "Пример использования кода покрытия требования")</span><span class="sxs-lookup"><span data-stu-id="d8823-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="d8823-125">**Мин./Макс.**</span><span class="sxs-lookup"><span data-stu-id="d8823-125">**Min./Max.**</span></span> <span data-ttu-id="d8823-126">– Метод пополнения основан на уровне запасов.</span><span class="sxs-lookup"><span data-stu-id="d8823-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="d8823-127">Он определяет пополнение запасов до определенного уровня, когда прогнозируемый уровень в наличии находится ниже определенного порога.</span><span class="sxs-lookup"><span data-stu-id="d8823-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="d8823-128">Количество пополнения будет разницей между максимальным уровнем и прогнозируемым уровнем запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="d8823-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="d8823-129">*Мин./Макс.*</span><span class="sxs-lookup"><span data-stu-id="d8823-129">The *Min./Max.*</span></span> <span data-ttu-id="d8823-130">код покрытия часто используется для предсказуемого извлечения запасов, высоко ликвидного товара или менее дорогих продуктов.</span><span class="sxs-lookup"><span data-stu-id="d8823-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="d8823-131">Следующая иллюстрация показывает пример.</span><span class="sxs-lookup"><span data-stu-id="d8823-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="d8823-132">![Пример использования кода покрытия минимума/максимума](./media/coverage-code-min-max.png "Пример использования кода покрытия минимума/максимума")</span><span class="sxs-lookup"><span data-stu-id="d8823-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="d8823-133">**Вручную** — метод пополнения, в котором система не предлагает заказы на покупку, перемещение или производство для продукта.</span><span class="sxs-lookup"><span data-stu-id="d8823-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="d8823-134">Вместо этого планировщик продукта отвечает за создание необходимых заказов для пополнения продукта.</span><span class="sxs-lookup"><span data-stu-id="d8823-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="d8823-135">Код покрытия *Вручную* часто используется для продуктов, для которых не требуются созданные системой спланированные заказы.</span><span class="sxs-lookup"><span data-stu-id="d8823-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="d8823-136">Влияние настроек количества заказа из заказа по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d8823-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="d8823-137">На странице **Настройки заказа по умолчанию** для выпущенного продукта можно указать каждый из следующих параметров количества на экспресс-вкладках **Заказ на покупку**, **Запасы** и **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="d8823-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="d8823-138">(Экспресс-вкладка **Запасы** используется как для заказов на перемещение, так и для производственных заказов.)</span><span class="sxs-lookup"><span data-stu-id="d8823-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="d8823-139">**Несколько** — запланированные заказы будут кратными этому количеству.</span><span class="sxs-lookup"><span data-stu-id="d8823-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="d8823-140">Например, если поле **Несколько** задано как *5*, заказ может быть оформлен на количество 5, 10, 15, 20 и так далее.</span><span class="sxs-lookup"><span data-stu-id="d8823-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="d8823-141">**Мин. количество по заказу** — спланированные заказы не будут меньше указанного значения.</span><span class="sxs-lookup"><span data-stu-id="d8823-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="d8823-142">Например, если поле **Мин. количество по заказу** задано как *10*, будет создан спланированный заказ на количество 10, даже если для выполнения требования требуется только четыре.</span><span class="sxs-lookup"><span data-stu-id="d8823-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="d8823-143">**Макс. количество по заказу** — спланированные заказы не будут больше указанного значения.</span><span class="sxs-lookup"><span data-stu-id="d8823-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="d8823-144">Если спрос больше, чем значение **Макс. количество по заказу**, несколько спланированных заказов будут созданы для его покрытия.</span><span class="sxs-lookup"><span data-stu-id="d8823-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="d8823-145">Например, если поле **Макс. количество по заказу** задано как *100*, а спрос составляет 450, будет создано четыре спланированных заказа на количество 100 и один спланированный заказ на количество 50.</span><span class="sxs-lookup"><span data-stu-id="d8823-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="d8823-146">Примеры пополнения, которые используют минимум/максимум.</span><span class="sxs-lookup"><span data-stu-id="d8823-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="d8823-147">Код покрытия</span><span class="sxs-lookup"><span data-stu-id="d8823-147">coverage code</span></span>

<span data-ttu-id="d8823-148">Если вы не указали значение в поле **Несколько** для продукта на странице **Настройки заказа по умолчанию** и если вы используете метод пополнения *Мин/макс*</span><span class="sxs-lookup"><span data-stu-id="d8823-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="d8823-149">оптимизация планирования пополняет запасы до определенного уровня, когда прогнозируемый уровень в наличии находится ниже определенного порога.</span><span class="sxs-lookup"><span data-stu-id="d8823-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="d8823-150">Если вы определяете несколько количеств для продукта, метод пополнения *Мин./макс.*</span><span class="sxs-lookup"><span data-stu-id="d8823-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="d8823-151">изменяет свое поведение и учитывает значение **Несколько**.</span><span class="sxs-lookup"><span data-stu-id="d8823-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="d8823-152">Другими словами, оптимизация планирования по-прежнему пополняет запасы до определенного максимального уровня, когда прогнозируемый уровень в наличии меньше определенного минимального уровня.</span><span class="sxs-lookup"><span data-stu-id="d8823-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="d8823-153">Тем не менее, количество пополнения должно быть кратным значению **Несколько**.</span><span class="sxs-lookup"><span data-stu-id="d8823-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="d8823-154">Если количество пополнения (разница между максимальным уровнем и прогнозируемым уровнем в наличии) не кратно определенному количеству "несколько", оптимизация планирования использует первое возможное значение, которое вместе с прогнозируемым уровнем в наличии будет ниже максимального уровня.</span><span class="sxs-lookup"><span data-stu-id="d8823-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="d8823-155">Если сумма меньше минимального уровня, оптимизация планирования использует первое значение, которое вместе с прогнозом в наличии на руках будет выше максимального уровня.</span><span class="sxs-lookup"><span data-stu-id="d8823-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="d8823-156">Следующие подразделы содержат некоторые примеры, которые показывают, как количество заказов "несколько" для продукта влияет на результат *Мин/макс*</span><span class="sxs-lookup"><span data-stu-id="d8823-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="d8823-157">(метод пополнения).</span><span class="sxs-lookup"><span data-stu-id="d8823-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="d8823-158">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8823-158">Example 1</span></span>

<span data-ttu-id="d8823-159">Продукт имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="d8823-159">A product has the following configuration:</span></span>

- <span data-ttu-id="d8823-160">**Код покрытия:** *Мин/макс.*</span><span class="sxs-lookup"><span data-stu-id="d8823-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="d8823-161">**Минимум:** *15*</span><span class="sxs-lookup"><span data-stu-id="d8823-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="d8823-162">**Максимум:** *22*</span><span class="sxs-lookup"><span data-stu-id="d8823-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="d8823-163">**Кратный:** *0*</span><span class="sxs-lookup"><span data-stu-id="d8823-163">**Multiple:** *0*</span></span>

<span data-ttu-id="d8823-164">Есть 10 штук в запасах в наличии для продукта, и нет другого спроса или предложения.</span><span class="sxs-lookup"><span data-stu-id="d8823-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="d8823-165">При выполнении сводного планирования создается спланированный заказ на 12 штук для пополнения запасов до максимального количества.</span><span class="sxs-lookup"><span data-stu-id="d8823-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="d8823-166">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8823-166">Example 2</span></span>

<span data-ttu-id="d8823-167">Продукт имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="d8823-167">A product has the following configuration:</span></span>

- <span data-ttu-id="d8823-168">**Код покрытия:** *Мин/макс.*</span><span class="sxs-lookup"><span data-stu-id="d8823-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="d8823-169">**Минимум:** *15*</span><span class="sxs-lookup"><span data-stu-id="d8823-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="d8823-170">**Максимум:** *22*</span><span class="sxs-lookup"><span data-stu-id="d8823-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="d8823-171">**Кратный:** *5*</span><span class="sxs-lookup"><span data-stu-id="d8823-171">**Multiple:** *5*</span></span>

<span data-ttu-id="d8823-172">Есть 10 штук в запасах в наличии для продукта, и нет другого спроса или предложения.</span><span class="sxs-lookup"><span data-stu-id="d8823-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="d8823-173">При выполнении сводного планирования создается спланированный заказ на 10 штук (потому что 15 штук пополнения плюс 10 штук в запасах в наличии превысит максимальное количество).</span><span class="sxs-lookup"><span data-stu-id="d8823-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="d8823-174">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d8823-174">Example 3</span></span>

<span data-ttu-id="d8823-175">Продукт имеет следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="d8823-175">A product has the following configuration:</span></span>

- <span data-ttu-id="d8823-176">**Код покрытия:** *Мин/макс.*</span><span class="sxs-lookup"><span data-stu-id="d8823-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="d8823-177">**Минимум:** *21*</span><span class="sxs-lookup"><span data-stu-id="d8823-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="d8823-178">**Максимум:** *24*</span><span class="sxs-lookup"><span data-stu-id="d8823-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="d8823-179">**Кратный:** *5*</span><span class="sxs-lookup"><span data-stu-id="d8823-179">**Multiple:** *5*</span></span>

<span data-ttu-id="d8823-180">Есть 10 штук в запасах в наличии для продукта, и нет другого спроса или предложения.</span><span class="sxs-lookup"><span data-stu-id="d8823-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="d8823-181">При выполнении сводного планирования создается спланированный заказ на 15 штук (потому что 10 штук пополнения плюс 10 штук в запасах в наличии будет меньше минимального количества).</span><span class="sxs-lookup"><span data-stu-id="d8823-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
