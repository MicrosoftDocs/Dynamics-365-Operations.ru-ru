---
title: Конфигурация затрат для распределенного управления заказами (DOM)
description: В этом разделе описывается функциональность конфигурации затрат для распределенного управления заказами (DOM) в Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004236"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="1f81f-103">Конфигурация затрат для распределенного управления заказами (DOM)</span><span class="sxs-lookup"><span data-stu-id="1f81f-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f81f-104">Организации учитывают несколько компонентов затрат, чтобы определить оптимальную точку для выполнения заказа.</span><span class="sxs-lookup"><span data-stu-id="1f81f-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="1f81f-105">Некоторые из этих компонентов затрат представляют собой затраты на отгрузку, обработку и упаковку.</span><span class="sxs-lookup"><span data-stu-id="1f81f-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="1f81f-106">Сочетание этих затрат рассчитывается для определения точки выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="1f81f-107">Когда первая итерация распределенного управления заказами (DOM) в Dynamics 365 Commerce оптимизировала назначение заказов точкам выполнения, она учитывала только расстояние.</span><span class="sxs-lookup"><span data-stu-id="1f81f-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="1f81f-108">Хотя расстояние может быть связано с затратами, это не то же самое, что затраты.</span><span class="sxs-lookup"><span data-stu-id="1f81f-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="1f81f-109">Например, затраты на срочный способ доставки превышают затраты на доставку в течение трех или семи дней на то же расстояние.</span><span class="sxs-lookup"><span data-stu-id="1f81f-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="1f81f-110">Функция конфигурации затрат позволяет компаниям розничной торговли определять и настраивать дополнительные компоненты затрат, которые будут рассчитываться и учитываться для определения оптимальной точки выполнения строк заказов.</span><span class="sxs-lookup"><span data-stu-id="1f81f-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="1f81f-111">При настройке компонентов затрат решатель DOM использует только эти определения затрат для определения оптимальной точки выполнения заказа.</span><span class="sxs-lookup"><span data-stu-id="1f81f-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="1f81f-112">Он не будет учитывать компонент расстояния в качестве затрат.</span><span class="sxs-lookup"><span data-stu-id="1f81f-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="1f81f-113">Однако, если не настроен ни один компонент затрат, решатель DOM будет использовать компонент расстояния как затраты для определения оптимальной точки выполнения заказа.</span><span class="sxs-lookup"><span data-stu-id="1f81f-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="1f81f-114">Настройка компонентов затрат</span><span class="sxs-lookup"><span data-stu-id="1f81f-114">Set up cost components</span></span>

<span data-ttu-id="1f81f-115">В системе можно определить два основных типа компонентов затрат: **Отгрузка** и **Прочие**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="1f81f-116">Оба типа компонентов затрат поддерживают несколько баз расчета, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1f81f-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1f81f-117">Тип компонента затрат</span><span class="sxs-lookup"><span data-stu-id="1f81f-117">Cost component type</span></span></th>
<th><span data-ttu-id="1f81f-118">Основа расчета</span><span class="sxs-lookup"><span data-stu-id="1f81f-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1f81f-119">Отгрузка</span><span class="sxs-lookup"><span data-stu-id="1f81f-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1f81f-120">Простой</span><span class="sxs-lookup"><span data-stu-id="1f81f-120">Simple</span></span></li>
<li><span data-ttu-id="1f81f-121">Многоуровневый</span><span class="sxs-lookup"><span data-stu-id="1f81f-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1f81f-122">Прочие</span><span class="sxs-lookup"><span data-stu-id="1f81f-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1f81f-123">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="1f81f-123">Sales order</span></span></li>
<li><span data-ttu-id="1f81f-124">Строка продажи</span><span class="sxs-lookup"><span data-stu-id="1f81f-124">Sales line</span></span></li>
<li><span data-ttu-id="1f81f-125">Местонахождение</span><span class="sxs-lookup"><span data-stu-id="1f81f-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="1f81f-126">Тип компонента затрат "Отгрузка"</span><span class="sxs-lookup"><span data-stu-id="1f81f-126">Shipping cost component type</span></span>

<span data-ttu-id="1f81f-127">В этом разделе описывается, как настроить каждое сочетание типа компонента затрат **Отгрузка** и основу расчета для затрат на отгрузку.</span><span class="sxs-lookup"><span data-stu-id="1f81f-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="1f81f-128">В нем также объясняется, как решатель DOM использует каждое сочетание.</span><span class="sxs-lookup"><span data-stu-id="1f81f-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="1f81f-129">Тип компонента затрат = Отгрузка; Основа расчета = Простой</span><span class="sxs-lookup"><span data-stu-id="1f81f-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="1f81f-130">Если используется сочетание типа компонента затрат **Отгрузка** и основа расчета **Простой**, затраты на отгрузку для режима доставки основываются на себестоимости или расстоянии.</span><span class="sxs-lookup"><span data-stu-id="1f81f-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="1f81f-131">Для этого сочетания необходимо настроить следующие поля:</span><span class="sxs-lookup"><span data-stu-id="1f81f-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="1f81f-132">**Коэффициент стоимости** — введите уникальный идентификатор для коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="1f81f-133">**Описание** — введите имя и описание коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="1f81f-134">**Дата начала** и **Дата окончания** — эти поля можно использовать, чтобы ограничить коэффициент стоимости для конкретного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="1f81f-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="1f81f-135">Если оставить эти поля пустыми, коэффициент стоимости действителен в течение неопределенного периода.</span><span class="sxs-lookup"><span data-stu-id="1f81f-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="1f81f-136">**Активно** — указывает, активен ли коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="1f81f-137">DOM учитывает только активные коэффициенты стоимости, связанные с профилем выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="1f81f-138">**Компания** — укажите юридическое лицо, для которого настроен коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="1f81f-139">Все строки критериев расчета должны быть для одного и того же юридического лица.</span><span class="sxs-lookup"><span data-stu-id="1f81f-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="1f81f-140">**Режимы доставки** — укажите режимы доставки, для которых настроены затраты.</span><span class="sxs-lookup"><span data-stu-id="1f81f-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="1f81f-141">**Тип расчета** — укажите, как должны рассчитываться затраты для конкретного режима доставки.</span><span class="sxs-lookup"><span data-stu-id="1f81f-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="1f81f-142">Поддерживаются два типа расчета:</span><span class="sxs-lookup"><span data-stu-id="1f81f-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="1f81f-143">**Фиксированный** — для режима доставки используется себестоимость.</span><span class="sxs-lookup"><span data-stu-id="1f81f-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="1f81f-144">При выборе этого типа расчета поле **Стоимость** определяет себестоимость.</span><span class="sxs-lookup"><span data-stu-id="1f81f-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="1f81f-145">**На единицу расстояния** — стоимость режима доставки рассчитывается как себестоимость, указанная в поле **Стоимость**, умноженная на расстояние между адресом поставки и местонахождениями.</span><span class="sxs-lookup"><span data-stu-id="1f81f-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="1f81f-146">**Стоимость** — укажите себестоимость, используемую в сочетании с полем **Тип расчета** для расчета стоимости режима доставки.</span><span class="sxs-lookup"><span data-stu-id="1f81f-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="1f81f-147">Тип компонента затрат = Отгрузка; Основа расчета = Многоуровневый</span><span class="sxs-lookup"><span data-stu-id="1f81f-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="1f81f-148">Если используется сочетание типа компонента затрат **Отгрузка** и основа расчета **Многоуровневый**, затраты на отгрузку для режима доставки основываются на себестоимости или расстоянии.</span><span class="sxs-lookup"><span data-stu-id="1f81f-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="1f81f-149">Однако в этом сочетании расстояние основано на многоуровневом диапазоне расстояний.</span><span class="sxs-lookup"><span data-stu-id="1f81f-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="1f81f-150">Для этого сочетания необходимо настроить следующие поля:</span><span class="sxs-lookup"><span data-stu-id="1f81f-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="1f81f-151">**Коэффициент стоимости** — введите уникальный идентификатор для коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="1f81f-152">**Описание** — введите имя и описание коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="1f81f-153">**Стоимость по умолчанию** — укажите стоимость, которая должна использоваться для режима доставки, если расстояние между адресом поставки и местонахождением не соответствует ни одному из многоуровневых расстояний для режима доставки.</span><span class="sxs-lookup"><span data-stu-id="1f81f-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="1f81f-154">**Дата начала** и **Дата окончания** — эти поля можно использовать, чтобы ограничить коэффициент стоимости для конкретного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="1f81f-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="1f81f-155">Если оставить эти поля пустыми, коэффициент стоимости действителен в течение неопределенного периода.</span><span class="sxs-lookup"><span data-stu-id="1f81f-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="1f81f-156">**Активно** — указывает, активен ли коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="1f81f-157">DOM учитывает только активные коэффициенты стоимости, связанные с профилем выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="1f81f-158">**Компания** — укажите юридическое лицо, для которого настроен коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="1f81f-159">Все строки критериев расчета должны быть для одного и того же юридического лица.</span><span class="sxs-lookup"><span data-stu-id="1f81f-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="1f81f-160">**Режимы доставки** — укажите режимы доставки, для которых настроены затраты.</span><span class="sxs-lookup"><span data-stu-id="1f81f-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="1f81f-161">**Тип расстояния** — укажите, является ли определение многоуровневого расстояния расстоянием по воздуху или по дороге.</span><span class="sxs-lookup"><span data-stu-id="1f81f-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="1f81f-162">**Единицы расстояния** — укажите единицу измерения, в которой измеряется многоуровневое расстояние.</span><span class="sxs-lookup"><span data-stu-id="1f81f-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="1f81f-163">**Расстояние от** — укажите начальный диапазон для многоуровневого расстояния.</span><span class="sxs-lookup"><span data-stu-id="1f81f-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="1f81f-164">**Расстояние до** — укажите конечный диапазон для многоуровневого расстояния.</span><span class="sxs-lookup"><span data-stu-id="1f81f-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="1f81f-165">**Тип расчета** — укажите, как должны рассчитываться затраты для конкретного режима доставки и многоуровневого расстояния.</span><span class="sxs-lookup"><span data-stu-id="1f81f-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="1f81f-166">Поддерживаются два типа расчета:</span><span class="sxs-lookup"><span data-stu-id="1f81f-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="1f81f-167">**Фиксированный** — для режима доставки используется себестоимость.</span><span class="sxs-lookup"><span data-stu-id="1f81f-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="1f81f-168">При выборе этого типа расчета поле **Стоимость** определяет себестоимость.</span><span class="sxs-lookup"><span data-stu-id="1f81f-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="1f81f-169">**На единицу расстояния** — стоимость режима доставки и многоуровневого расстояния рассчитывается как себестоимость, указанная в поле **Стоимость**, умноженная на расстояние между адресом поставки и местонахождениями.</span><span class="sxs-lookup"><span data-stu-id="1f81f-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="1f81f-170">**Стоимость** — укажите себестоимость, используемую в сочетании с полем **Тип расчета** для расчета стоимости режима доставки.</span><span class="sxs-lookup"><span data-stu-id="1f81f-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="1f81f-171">При определении многоуровневых расстояний система проверяет, что нет отсутствующих или перекрывающихся расстояний.</span><span class="sxs-lookup"><span data-stu-id="1f81f-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="1f81f-172">Тип расстояния, используемый для режима доставки, должен быть одинаковым для всех многоуровневых расстояний.</span><span class="sxs-lookup"><span data-stu-id="1f81f-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="1f81f-173">Тип компонента затрат "Прочие"</span><span class="sxs-lookup"><span data-stu-id="1f81f-173">Other cost component type</span></span>

<span data-ttu-id="1f81f-174">В этом разделе описывается, как настроить каждое сочетание типа компонента затрат **Прочие** "и другого типа затрат для затрат, не связанных с отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="1f81f-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="1f81f-175">В нем также объясняется, как решатель DOM использует каждое сочетание.</span><span class="sxs-lookup"><span data-stu-id="1f81f-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="1f81f-176">Тип компонента затрат = Прочие; Тип затрат "Прочие" = Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="1f81f-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="1f81f-177">Сочетание типа компонента затрат **Прочие** и типа затрат "Прочие" **Заказ на продажу** используется для определения затрат, не связанных с отгрузкой, на уровне заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1f81f-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="1f81f-178">Для этого сочетания необходимо настроить следующие поля:</span><span class="sxs-lookup"><span data-stu-id="1f81f-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="1f81f-179">**Коэффициент стоимости** — введите уникальный идентификатор для коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="1f81f-180">**Описание** — введите имя и описание коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="1f81f-181">**Дата начала** и **Дата окончания** — эти поля можно использовать, чтобы ограничить коэффициент стоимости для конкретного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="1f81f-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="1f81f-182">Если оставить эти поля пустыми, коэффициент стоимости действителен в течение неопределенного периода.</span><span class="sxs-lookup"><span data-stu-id="1f81f-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="1f81f-183">**Активно** — указывает, активен ли коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="1f81f-184">DOM учитывает только активные коэффициенты стоимости, связанные с профилем выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="1f81f-185">**Стоимость** — укажите себестоимость для затрат, не связанных с отгрузкой, на уровне заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1f81f-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="1f81f-186">Тип компонента затрат = Прочие; Тип затрат "Прочие" = Строка продажи</span><span class="sxs-lookup"><span data-stu-id="1f81f-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="1f81f-187">Сочетание типа компонента затрат **Прочие** и типа затрат "Прочие" **Строка продажи** используется для определения затрат, не связанных с отгрузкой, на уровне строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1f81f-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="1f81f-188">Для этого сочетания необходимо настроить следующие поля:</span><span class="sxs-lookup"><span data-stu-id="1f81f-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="1f81f-189">**Коэффициент стоимости** — введите уникальный идентификатор для коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="1f81f-190">**Описание** — введите имя и описание коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="1f81f-191">**Дата начала** и **Дата окончания** — эти поля можно использовать, чтобы ограничить коэффициент стоимости для конкретного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="1f81f-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="1f81f-192">Если оставить эти поля пустыми, коэффициент стоимости действителен в течение неопределенного периода.</span><span class="sxs-lookup"><span data-stu-id="1f81f-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="1f81f-193">**Активно** — указывает, активен ли коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="1f81f-194">DOM учитывает только активные коэффициенты стоимости, связанные с профилем выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="1f81f-195">**Стоимость** — укажите себестоимость для затрат, не связанных с отгрузкой, на уровне строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1f81f-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="1f81f-196">Тип компонента затрат = Прочие; Тип затрат "Прочие" = Местонахождение</span><span class="sxs-lookup"><span data-stu-id="1f81f-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="1f81f-197">Сочетание типа компонента затрат **Прочие** и типа затрат "Прочие" **Местонахождение** используется для определения затрат, не связанных с отгрузкой, для группы местонахождений или отдельного местонахождения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="1f81f-198">Для этого сочетания необходимо настроить следующие поля:</span><span class="sxs-lookup"><span data-stu-id="1f81f-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="1f81f-199">**Коэффициент стоимости** — введите уникальный идентификатор для коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="1f81f-200">**Описание** — введите имя и описание коэффициента стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="1f81f-201">**Дата начала** и **Дата окончания** — эти поля можно использовать, чтобы ограничить коэффициент стоимости для конкретного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="1f81f-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="1f81f-202">Если оставить эти поля пустыми, коэффициент стоимости действителен в течение неопределенного периода.</span><span class="sxs-lookup"><span data-stu-id="1f81f-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="1f81f-203">**Активно** — указывает, активен ли коэффициент стоимости.</span><span class="sxs-lookup"><span data-stu-id="1f81f-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="1f81f-204">DOM учитывает только активные коэффициенты стоимости, связанные с профилем выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="1f81f-205">**Группа выполнения** — укажите группу местонахождений, для которой определены затраты, не связанные с отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="1f81f-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="1f81f-206">**Точка выполнения** — укажите местонахождение, для которого определены затраты, не связанные с отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="1f81f-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f81f-207">Невозможно указать группу выполнения и точку выполнения в одной строке для критериев расчета на основе местонахождения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="1f81f-208">**Стоимость** — укажите себестоимость для затрат, не связанных с отгрузкой, на уровне группы выполнение или на уровне точки выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f81f-209">Чтобы в DOM учитывались эти затраты при выполнении, необходимо добавить коэффициент стоимости в соответствующий профиль выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f81f-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
