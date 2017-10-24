---
title: "Пополнение"
description: "В этой теме описываются стратегии пополнения, доступные для складов, использующих функциональные возможности, предусмотренные в модуле \"Управление складом\"."
author: Mirzaab
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 67e361aedf77166e01d9e7a5b9dcb19d08ea26bd
ms.openlocfilehash: 872fbe41ed8137c1e7bec24656d4f132e170ae7f
ms.contentlocale: ru-ru
ms.lasthandoff: 10/05/2017

---

# <a name="replenishment"></a><span data-ttu-id="972b9-103">Пополнение</span><span class="sxs-lookup"><span data-stu-id="972b9-103">Replenishment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="972b9-104">В этой теме описываются стратегии пополнения, доступные для складов, использующих функциональные возможности, предусмотренные в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="972b9-104">This topic describes the replenishment strategies that are available for warehouses that use the functionality that is available in Warehouse management.</span></span> <span data-ttu-id="972b9-105">Информация в этой теме не относится к решению складирования, доступному в модуле "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="972b9-105">The information in this topic doesn't apply to the warehousing solution that is available in Inventory management.</span></span>

<span data-ttu-id="972b9-106">Доступны следующие стратегии пополнения:</span><span class="sxs-lookup"><span data-stu-id="972b9-106">The following replenishment strategies are available:</span></span>

- <span data-ttu-id="972b9-107">**Пополнение, основанное на спросе волны** — эта стратегия создает работу пополнения для исходящих заказов или загрузок, если запасы недоступны при создании работы в волне.</span><span class="sxs-lookup"><span data-stu-id="972b9-107">**Wave demand replenishment** – This strategy creates replenishment work for outbound orders or loads if inventory isn't available when the wave creates work.</span></span> <span data-ttu-id="972b9-108">Например, работу пополнения можно создать, если количество, необходимое для заказа на продажу, недоступно при обработке волны.</span><span class="sxs-lookup"><span data-stu-id="972b9-108">For example, replenishment work can be created if the quantity that is required for a sales order isn't available when a wave is processed.</span></span>
- <span data-ttu-id="972b9-109">**Пополнение, основанное на минимальном и максимальном количествах** — эта стратегия использует минимальные и максимальные лимиты хранения для определения времени пополнения местонахождений.</span><span class="sxs-lookup"><span data-stu-id="972b9-109">**Min/Max replenishment** – This strategy uses minimum and maximum stocking limits to determine when locations should be replenished.</span></span> <span data-ttu-id="972b9-110">Критерии номенклатур и местонахождений определяют запасы, которые оцениваются для пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-110">The item and location criteria define the inventory that is evaluated for replenishment.</span></span> <span data-ttu-id="972b9-111">Шаблоны пополнения, основанного на минимальном и максимальном количествах, являются основным механизмом для поддержания оптимального уровня в ячейках комплектации.</span><span class="sxs-lookup"><span data-stu-id="972b9-111">Min/Max replenishment templates are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="972b9-112">Чтобы гарантировать доступность достаточного количества запасов для комплектации для удовлетворения спроса, можно использовать пополнение спроса как дополнение между циклами пополнения, основанного на минимальном и максимальном количествах.</span><span class="sxs-lookup"><span data-stu-id="972b9-112">To help guarantee that enough pick face inventory is available to meet wave demand, you can use demand replenishment as a supplement between Min/Max replenishment cycles.</span></span>
- <span data-ttu-id="972b9-113">**Пополнение, основанное на спросе загрузки** — эта стратегия суммирует спрос для нескольких загрузок и создает работу пополнения, необходимую для пополнения запасов в соответствующих ячейках комплектации.</span><span class="sxs-lookup"><span data-stu-id="972b9-113">**Load demand replenishment** – This strategy sums the demand for several loads and creates the replenishment work that is required in order to stock the relevant picking locations.</span></span> <span data-ttu-id="972b9-114">Эта стратегия гарантирует, что создаваемые загрузки можно скомплектовать на складе после их выпуска.</span><span class="sxs-lookup"><span data-stu-id="972b9-114">This strategy helps guarantee that the loads that are created can be picked in the warehouse after they are released.</span></span>
- <span data-ttu-id="972b9-115">**Немедленное пополнение** — эта стратегия предполагает пополнение запасов перед выполнением волны, если не удается выполнить распределение для строки директивы местонахождения, у которой есть шаблон пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-115">**Immediate replenishment** – This strategy replenishes inventory before a wave is run if allocation fails for a location directive line that has a replenishment template.</span></span> 

<span data-ttu-id="972b9-116">Все четыре стратегии создают работу пополнения, основанную на шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-116">All four strategies create replenishment work, based on a replenishment template.</span></span>

## <a name="wave-demand-replenishment"></a><span data-ttu-id="972b9-117">Пополнение, основанное на спросе волны</span><span class="sxs-lookup"><span data-stu-id="972b9-117">Wave demand replenishment</span></span>
<span data-ttu-id="972b9-118">Пополнение, основанное на спросе волны, создает работу пополнения на основании спроса, если количество, необходимое для производственных заказов, канбанов, исходящих заказов или загрузок не доступно при создании работы в волне.</span><span class="sxs-lookup"><span data-stu-id="972b9-118">Wave demand replenishment creates replenishment work, based on demand, if the quantity that is required for production orders, kanbans, outbound orders, or loads isn't available when a wave creates work.</span></span> <span data-ttu-id="972b9-119">Шаблон пополнения содержит сведения о критериях номенклатуры, единице измерения, увеличении спроса и местонахождении.</span><span class="sxs-lookup"><span data-stu-id="972b9-119">The replenishment template contains information about the item criteria, the unit of measure, the demand increment, and the location.</span></span> 

<span data-ttu-id="972b9-120">Директивы местонахождений используются для определения того, какие местонахождения следует пополнять.</span><span class="sxs-lookup"><span data-stu-id="972b9-120">Location directives are used to determine which location should be replenished.</span></span> <span data-ttu-id="972b9-121">Эти директивы местонахождений можно связать с шаблоном пополнения с помощью поля **Код директивы**.</span><span class="sxs-lookup"><span data-stu-id="972b9-121">You link these location directives to the replenishment template by using the **Directive code** field.</span></span> <span data-ttu-id="972b9-122">Если в поле **Код директивы** не задано значение, используются запросы для определения того, какие директивы местонахождений должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="972b9-122">If the **Directive code** field isn't set, queries are used to determine which location directive should be used.</span></span> <span data-ttu-id="972b9-123">Обратите внимание, что если код директивы не указан в шаблоне пополнения и директива местонахождения имеет код директивы, директива местонахождения будет игнорироваться, даже если запрос в директиве местонахождения правильный.</span><span class="sxs-lookup"><span data-stu-id="972b9-123">Note that if a directive code isn't specified in the replenishment template, and the location directive has a directive code, the location directive will be ignored, even if the query on the location directive is correct.</span></span> <span data-ttu-id="972b9-124">Директивы местонахождений комплектации используются для определения того, откуда можно получить запасы для пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-124">Pick location directives are used to determine where to get inventory for the replenishment.</span></span> 

<span data-ttu-id="972b9-125">Помимо создания шаблона необходимо указать некоторые параметры пополнения в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="972b9-125">In addition to creating a template, you must specify some replenishment settings in the wave template.</span></span> <span data-ttu-id="972b9-126">Шаблон волны должен содержать шаг волны для пополнения, который выполняется, только если номенклатуру не удалось успешно распределить.</span><span class="sxs-lookup"><span data-stu-id="972b9-126">The wave template should contain a wave step for replenishment that is run only if an item isn't successfully allocated.</span></span> <span data-ttu-id="972b9-127">Этот шаг волны пополнения использует код шага волны для определения шаблона пополнения, который следует использовать.</span><span class="sxs-lookup"><span data-stu-id="972b9-127">This replenishment wave step uses a wave step code to determine which replenishment template should be used.</span></span> <span data-ttu-id="972b9-128">Помимо шага волны для пополнения необходимо убедиться в том, **Пополнение** выбрано в разделе **Методы** шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="972b9-128">In addition to having a wave step for replenishment, you must make sure that **Replenish** is selected in the **Methods** section of the wave template.</span></span> 

<span data-ttu-id="972b9-129">Страница **Шаблон пополнения** включает флажок **Разрешить волне спроса использовать незарезервированные количества**.</span><span class="sxs-lookup"><span data-stu-id="972b9-129">The **Replenishment template** page includes an **Allow wave demand to use unreserved quantities** check box.</span></span> <span data-ttu-id="972b9-130">Этот флажок следует установить, если нужно, чтобы при пополнении спроса вычитались незарезервированные количества из работы, созданной на основе выбранного шаблона пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-130">Select this check box if demand replenishment should be able to deduct unreserved quantities from work that is generated from the selected replenishment template.</span></span> <span data-ttu-id="972b9-131">Чтобы использовать эту логику в шаблонах пополнения на основании спроса, установите этот флажок для всех существующих шаблонов пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-131">To enable demand replenishment templates to use this logic, select this check box for every existing replenishment template.</span></span> <span data-ttu-id="972b9-132">Когда пополнение спроса запускается на складе, спрос вычитается из существующей работы пополнения с незарезервированными количествами, если эта работа создана на основе шаблонов пополнения с установленным флажком **Разрешить волне спроса использовать незарезервированные количества**.</span><span class="sxs-lookup"><span data-stu-id="972b9-132">When demand replenishment is triggered in the warehouse, it will deduct the demand from existing replenishment work that has unreserved quantities, if the work originates from replenishment templates where the **Allow wave demand to use unreserved quantities** check box is selected.</span></span>

<span data-ttu-id="972b9-133">Пополнение на основании спроса поддерживается для заказов на продажу, заказов на перемещение, производственных заказов и канбанов.</span><span class="sxs-lookup"><span data-stu-id="972b9-133">Demand replenishment is supported for sales orders, transfer orders, production orders, and kanbans.</span></span> 

## <a name="minmax-replenishment"></a><span data-ttu-id="972b9-134">Пополнение, основанное на минимальном и максимальном количествах</span><span class="sxs-lookup"><span data-stu-id="972b9-134">Min/Max replenishment</span></span>
<span data-ttu-id="972b9-135">В пополнении, основанном на минимальном и максимальном количествах, запасы пополняются таким образом, чтобы они находились в заданных пределах между минимальным и максимальным количествами.</span><span class="sxs-lookup"><span data-stu-id="972b9-135">In Min/Max replenishment, stock is replenished so that it's between the minimum and maximum limits that have been set.</span></span> <span data-ttu-id="972b9-136">Обычно этот процесс происходит один раз в день, чтобы гарантировать, что все ячейки комплектации заполняются до максимального уровня перед началом комплектации.</span><span class="sxs-lookup"><span data-stu-id="972b9-136">Typically, this process occurs one time every day, to help guarantee that all picking locations are filled to the maximum level before picking starts.</span></span> 

<span data-ttu-id="972b9-137">Минимальная и максимальная суммы задаются в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-137">The minimum and maximum amounts are set in a replenishment template.</span></span> <span data-ttu-id="972b9-138">Многие другие параметры в шаблоне напоминают параметры в шаблонах, используемых в пополнении, основанном на спросе волны.</span><span class="sxs-lookup"><span data-stu-id="972b9-138">Many of the other settings in the template resemble the settings in templates that are used in Wave demand replenishment.</span></span> <span data-ttu-id="972b9-139">Шаблон должен включать одну строку для каждой номенклатуры и местонахождения.</span><span class="sxs-lookup"><span data-stu-id="972b9-139">The template should contain one line for each item and location.</span></span> <span data-ttu-id="972b9-140">При выполнении пополнения с помощью пакетного задания Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition оценивает, требуется ли пополнение, в последовательности, в которой организованы строки.</span><span class="sxs-lookup"><span data-stu-id="972b9-140">When you run replenishment by using the batch job, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, evaluates whether replenishment is required by using the sequence that the lines are organized in.</span></span> 

<span data-ttu-id="972b9-141">Обратите внимание, что при использовании стратегии пополнения, основанной на минимальном и максимальном количествах, невозможно пополнить пустое местонахождение, если оно не задано как фиксированное местонахождение для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="972b9-141">Note that the Min/Max replenishment strategy can't replenish an empty location unless the location is set as the fixed location for the item.</span></span> <span data-ttu-id="972b9-142">Если местонахождение, которое необходимо пополнить, не является фиксированным местонахождением, система не может определить, какую номенклатуру пополнять.</span><span class="sxs-lookup"><span data-stu-id="972b9-142">If the location that must be replenished isn't a fixed location, the system can't determine which item should be replenished.</span></span> <span data-ttu-id="972b9-143">Таким образом, необходимо по крайней мере какое-то количество в запасе до выполнения пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-143">Therefore, at least some on-hand quantity is required before replenishment occurs.</span></span>

## <a name="load-demand-replenishment"></a><span data-ttu-id="972b9-144">Пополнение спроса загрузки</span><span class="sxs-lookup"><span data-stu-id="972b9-144">Load demand replenishment</span></span>
<span data-ttu-id="972b9-145">Пополнение, основанное на спросе загрузки, суммирует спрос для нескольких загрузок и создает работу пополнения, необходимую для пополнения запасов в соответствующих ячейках комплектации.</span><span class="sxs-lookup"><span data-stu-id="972b9-145">Load demand replenishment sums the demand for several loads and creates the replenishment work that is required in order to stock the relevant picking locations.</span></span> <span data-ttu-id="972b9-146">Пополнение, основанное на спросе загрузки, похоже на пополнение, основанное на спросе волны, во многих отношениях.</span><span class="sxs-lookup"><span data-stu-id="972b9-146">Load demand replenishment resembles Wave demand replenishment in many ways.</span></span> <span data-ttu-id="972b9-147">Основное различие состоит в том, как и когда выполняется пополнение в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="972b9-147">The main difference is how and when Load demand replenishment and Wave demand replenishment are run.</span></span> <span data-ttu-id="972b9-148">Как и при пополнении, основанном на минимальном и максимальном количестве, пополнение, во основанное на спросе загрузки, выполняется с помощью пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="972b9-148">Like Min/Max replenishment, Load demand replenishment is run by using a batch job.</span></span> <span data-ttu-id="972b9-149">Чтобы настроить пакетное задание, на странице **Пополнение, основанное на спросе загрузки** выберите шаблон пополнения для использования и задайте запрос фильтра, чтобы указать, какие загрузки используются для определения спроса.</span><span class="sxs-lookup"><span data-stu-id="972b9-149">To set up the batch job, on the **Load demand replenishment** page, select the replenishment template to use, and set a filter query to specify which loads are used to determine the demand.</span></span> <span data-ttu-id="972b9-150">Запрос местонахождения определяет местонахождения, из которых будет вычитаться все доступное количество для удовлетворения агрегированного спроса загрузок.</span><span class="sxs-lookup"><span data-stu-id="972b9-150">The location query defines the locations that any available quantity will be subtracted from to meet the aggregated demand of the loads.</span></span>

## <a name="immediate-replenishment"></a><span data-ttu-id="972b9-151">Немедленное пополнение</span><span class="sxs-lookup"><span data-stu-id="972b9-151">Immediate replenishment</span></span>
<span data-ttu-id="972b9-152">Вместо того чтобы суммировать спрос в конце процесса распределения и выполнять пополнение на основании полученного суммарного количества, можно применить стратегию немедленного пополнения.</span><span class="sxs-lookup"><span data-stu-id="972b9-152">Instead of having to sum demand at the end of an allocation process and do replenishment on the basis of the summed up quantity, you can apply the Immediate replenishment strategy.</span></span> <span data-ttu-id="972b9-153">При использовании этой стратегии запасы могут быть пополнены сразу же после того, как строка директивы местонахождения не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="972b9-153">When you use this strategy, the inventory can be replenished immediately after a location directive line fails.</span></span> <span data-ttu-id="972b9-154">Следовательно, можно настроить пополнение так, чтобы оно было ограничено конкретными номенклатурами и чтобы в нем использовались количества, заданные для конкретных местонахождений.</span><span class="sxs-lookup"><span data-stu-id="972b9-154">Therefore, you can set up the replenishment so that it's restricted by specific units, and so that it uses quantities that are set for specific locations.</span></span>

## <a name="replenishment-prerequisites"></a><span data-ttu-id="972b9-155">Необходимые условия для пополнения</span><span class="sxs-lookup"><span data-stu-id="972b9-155">Replenishment prerequisites</span></span>
| <span data-ttu-id="972b9-156">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="972b9-156">Prerequisite</span></span>            | <span data-ttu-id="972b9-157">описание</span><span class="sxs-lookup"><span data-stu-id="972b9-157">Description</span></span> |
|-------------------------|-------------|
| <span data-ttu-id="972b9-158">Товар</span><span class="sxs-lookup"><span data-stu-id="972b9-158">Item</span></span>                    | <span data-ttu-id="972b9-159">Для процессов управления складом должна быть включена номенклатура.</span><span class="sxs-lookup"><span data-stu-id="972b9-159">The item must be enabled for warehouse management processes.</span></span> |
| <span data-ttu-id="972b9-160">Склад</span><span class="sxs-lookup"><span data-stu-id="972b9-160">Warehouse</span></span>               | <span data-ttu-id="972b9-161">Для процессов управления складом должен быть включен склад.</span><span class="sxs-lookup"><span data-stu-id="972b9-161">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="972b9-162">Чтобы включить склад для использования процессов управления складом, на странице **Склады** выберите склад и установите флажок **Использовать процессы управления складом**.</span><span class="sxs-lookup"><span data-stu-id="972b9-162">To enable a warehouse for warehouse management processes, on the **Warehouses** page, select the warehouse, and then select the **Use warehouse management processes** option.</span></span> |
| <span data-ttu-id="972b9-163">Шаблоны пополнения</span><span class="sxs-lookup"><span data-stu-id="972b9-163">Replenishment templates</span></span> | <span data-ttu-id="972b9-164">Необходимо настроить хотя бы один шаблон пополнения для пополнения, основанного на минимальном и максимальном количествах, пополнения, основанного на спросе загрузки, или пополнения, основанного на спросе загрузки.</span><span class="sxs-lookup"><span data-stu-id="972b9-164">At least one replenishment template must be set up for Min/Max replenishment, Wave demand replenishment, or Load demand replenishment.</span></span> |
| <span data-ttu-id="972b9-165">Местоположения</span><span class="sxs-lookup"><span data-stu-id="972b9-165">Locations</span></span>               | <span data-ttu-id="972b9-166">Необходимо создать местонахождения и подключить их к профилю местонахождения.</span><span class="sxs-lookup"><span data-stu-id="972b9-166">Locations must be created and connected to a location profile.</span></span> |
| <span data-ttu-id="972b9-167">Профили местонахождения</span><span class="sxs-lookup"><span data-stu-id="972b9-167">Location profiles</span></span>       | <span data-ttu-id="972b9-168">Для создания местонахождений требуются профили местонахождений.</span><span class="sxs-lookup"><span data-stu-id="972b9-168">Location profiles are required in order to create locations.</span></span> |
| <span data-ttu-id="972b9-169">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="972b9-169">Location directives</span></span>     | <span data-ttu-id="972b9-170">Директивы местонахождений являются обязательными для направления работы в местонахождения, в которых требуется пополнение, и местонахождения, из которых берутся запасы.</span><span class="sxs-lookup"><span data-stu-id="972b9-170">Location directives are required in order to guide work to the locations where replenishment is required and to the locations that inventory is sourced from.</span></span> |
| <span data-ttu-id="972b9-171">Шаблоны работ</span><span class="sxs-lookup"><span data-stu-id="972b9-171">Work templates</span></span>          | <span data-ttu-id="972b9-172">Шаблоны работы типа **Пополнение** являются обязательными для создания работы пополнения, чтобы запасы можно было переместить в нужные местонахождения.</span><span class="sxs-lookup"><span data-stu-id="972b9-172">Work templates of the **Replenishment** type are required in order to create replenishment work so that inventory can be moved to the desired locations.</span></span> |
