---
title: Стратегии упаковки в контейнеры
description: В этой теме описываются различия между стратегиями упаковки контейнеров и даны примеры.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292769"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="61051-103">Стратегии упаковки в контейнеры</span><span class="sxs-lookup"><span data-stu-id="61051-103">Container packing strategies</span></span>

<span data-ttu-id="61051-104">*Стратегия упаковки контейнера* является стратегией, которую можно использовать для определения распределений номенклатур между контейнерами.</span><span class="sxs-lookup"><span data-stu-id="61051-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="61051-105">В этой теме объясняется различие между стратегиями *Упаковать во все открытые контейнеры* и *Упаковать только в текущий контейнер*.</span><span class="sxs-lookup"><span data-stu-id="61051-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="61051-106">**Упаковать во все открытые контейнеры** — система должна проверить все открытые контейнеры, которые уже были созданы в ходе цикла организации контейнеров, чтобы убедиться, что номенклатура поместится в один из них.</span><span class="sxs-lookup"><span data-stu-id="61051-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="61051-107">Во время упаковки система проверяет каждую номенклатуру, чтобы определить, сможет ли она поместиться в любой из ранее созданных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="61051-108">Если номенклатура не помещается в существующий контейнер, система создает новый контейнер и продолжает работу до тех пор, пока он не завершит упаковку всего заказа.</span><span class="sxs-lookup"><span data-stu-id="61051-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="61051-109">Например, *n* заказанных номенклатур требуют использования контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="61051-110">В худшем случае каждый раз, когда система обрабатывает номенклатуру, которая не поместится в какой-либо существующий контейнер, будет выполнена итоговая проверка (\[(*n* – 1) × (*n* + 1)\] ÷ 2), чтобы оценить, помещается ли номенклатура в существующие контейнеры.</span><span class="sxs-lookup"><span data-stu-id="61051-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="61051-111">**Упаковать только в текущий контейнер** — система должна проверить только последний созданный контейнер, чтобы убедиться, что номенклатура в него поместится.</span><span class="sxs-lookup"><span data-stu-id="61051-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="61051-112">Во время упаковки система проверяет каждую номенклатуру, чтобы определить, сможет ли она поместиться в последний созданный контейнер.</span><span class="sxs-lookup"><span data-stu-id="61051-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="61051-113">Если номенклатура не помещается в этот контейнер, система создает новый контейнер и продолжает работу до тех пор, пока он не завершит упаковку всего заказа.</span><span class="sxs-lookup"><span data-stu-id="61051-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="61051-114">Например, *n* заказанных номенклатур требуют использования контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="61051-115">В худшем случае система выполнит итоговые проверки (*n* – 1), чтобы определить, помещается ли номенклатура в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="61051-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="61051-116">Пример потока для стратегий упаковки контейнера</span><span class="sxs-lookup"><span data-stu-id="61051-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="61051-117">Для контейнеров настраиваются следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="61051-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="61051-118">Номенклатура</span><span class="sxs-lookup"><span data-stu-id="61051-118">Item</span></span> | <span data-ttu-id="61051-119">Физические размеры (ширина × глубина × высота)</span><span class="sxs-lookup"><span data-stu-id="61051-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="61051-120">Вес</span><span class="sxs-lookup"><span data-stu-id="61051-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="61051-121">Кабель HDMI 6 футов</span><span class="sxs-lookup"><span data-stu-id="61051-121">HDMI Cable 6'</span></span> | <span data-ttu-id="61051-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="61051-122">1 × 1 × 1</span></span> | <span data-ttu-id="61051-123">1</span><span class="sxs-lookup"><span data-stu-id="61051-123">1</span></span> |
| <span data-ttu-id="61051-124">Кабель HDMI 12 футов</span><span class="sxs-lookup"><span data-stu-id="61051-124">HDMI Cable 12'</span></span> | <span data-ttu-id="61051-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="61051-125">2 × 1 × 1</span></span> | <span data-ttu-id="61051-126">1</span><span class="sxs-lookup"><span data-stu-id="61051-126">1</span></span> |
| <span data-ttu-id="61051-127">Кабель HDMI 18 футов</span><span class="sxs-lookup"><span data-stu-id="61051-127">HDMI Cable 18'</span></span> | <span data-ttu-id="61051-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="61051-128">3 × 1 × 1</span></span> | <span data-ttu-id="61051-129">2</span><span class="sxs-lookup"><span data-stu-id="61051-129">2</span></span> |

<span data-ttu-id="61051-130">Кроме того, необходимо настроить следующее поле, которое будет использоваться для упаковки.</span><span class="sxs-lookup"><span data-stu-id="61051-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="61051-131">Контейнер</span><span class="sxs-lookup"><span data-stu-id="61051-131">Container</span></span> | <span data-ttu-id="61051-132">Физические размеры (длина × ширина × высота)</span><span class="sxs-lookup"><span data-stu-id="61051-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="61051-133">Вес</span><span class="sxs-lookup"><span data-stu-id="61051-133">Weight</span></span> | <span data-ttu-id="61051-134">Объем</span><span class="sxs-lookup"><span data-stu-id="61051-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="61051-135">Средний ящик</span><span class="sxs-lookup"><span data-stu-id="61051-135">Medium Box</span></span> | <span data-ttu-id="61051-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="61051-136">6 × 3 × 2</span></span> | <span data-ttu-id="61051-137">10</span><span class="sxs-lookup"><span data-stu-id="61051-137">10</span></span> | <span data-ttu-id="61051-138">100</span><span class="sxs-lookup"><span data-stu-id="61051-138">100</span></span> |

<span data-ttu-id="61051-139">В заключение можно настроить заказ со следующими продуктами и количествами.</span><span class="sxs-lookup"><span data-stu-id="61051-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="61051-140">Строка заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="61051-140">Sales order line</span></span> | <span data-ttu-id="61051-141">Количество</span><span class="sxs-lookup"><span data-stu-id="61051-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="61051-142">Кабель HDMI 12 футов</span><span class="sxs-lookup"><span data-stu-id="61051-142">HDMI Cable 12'</span></span> | <span data-ttu-id="61051-143">9</span><span class="sxs-lookup"><span data-stu-id="61051-143">9</span></span> |
| <span data-ttu-id="61051-144">Кабель HDMI 18 футов</span><span class="sxs-lookup"><span data-stu-id="61051-144">HDMI Cable 18'</span></span> | <span data-ttu-id="61051-145">8</span><span class="sxs-lookup"><span data-stu-id="61051-145">8</span></span> |
| <span data-ttu-id="61051-146">Кабель HDMI 6 футов</span><span class="sxs-lookup"><span data-stu-id="61051-146">HDMI Cable 6'</span></span> | <span data-ttu-id="61051-147">13</span><span class="sxs-lookup"><span data-stu-id="61051-147">13</span></span> |

<span data-ttu-id="61051-148">В следующей таблице приведены сводные данные о том, как работа с контейнерами выполняется при использовании стратегии *Упаковать во все открытые контейнеры* и при использовании стратегии *Упаковать только в текущий контейнер*.</span><span class="sxs-lookup"><span data-stu-id="61051-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="61051-149">Упаковать во все открытые контейнеры</span><span class="sxs-lookup"><span data-stu-id="61051-149">Pack into all open containers</span></span> | <span data-ttu-id="61051-150">Упаковать в текущий контейнер</span><span class="sxs-lookup"><span data-stu-id="61051-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="61051-151">Кабель HDMI 12 футов:</span><span class="sxs-lookup"><span data-stu-id="61051-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="61051-152">Создать новый контейнер, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="61051-153">Поместить 9 шт. в контейнер CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="61051-154">Кабель HDMI 12 футов:</span><span class="sxs-lookup"><span data-stu-id="61051-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="61051-155">Создать новый контейнер, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="61051-156">Поместить 9 шт. в контейнер CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="61051-157">Кабель HDMI 18 футов:</span><span class="sxs-lookup"><span data-stu-id="61051-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="61051-158">Проверить, может ли номенклатура поместиться в контейнер CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="61051-159">Создать новый контейнер, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="61051-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="61051-160">Поместить 5 шт. в контейнер CONT0002.</span><span class="sxs-lookup"><span data-stu-id="61051-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="61051-161">Создать новый контейнер, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="61051-162">Поместить 3 шт. в контейнер CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="61051-163">Кабель HDMI 18 футов:</span><span class="sxs-lookup"><span data-stu-id="61051-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="61051-164">Проверить, может ли номенклатура поместиться в контейнер CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="61051-165">Создать новый контейнер, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="61051-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="61051-166">Поместить 5 шт. в контейнер CONT0002.</span><span class="sxs-lookup"><span data-stu-id="61051-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="61051-167">Создать новый контейнер, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="61051-168">Поместить 3 шт. в контейнер CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="61051-169">Кабель HDMI 6 футов:</span><span class="sxs-lookup"><span data-stu-id="61051-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="61051-170">Проверить, может ли номенклатура поместиться в контейнер CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="61051-171">Поместить 1 шт. в контейнер CONT0001.</span><span class="sxs-lookup"><span data-stu-id="61051-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="61051-172">Проверить, может ли номенклатура поместиться в контейнер CONT0002.</span><span class="sxs-lookup"><span data-stu-id="61051-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="61051-173">Проверить, может ли номенклатура поместиться в контейнер CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="61051-174">Поместить 4 шт. в контейнер CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="61051-175">Создать новый контейнер, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="61051-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="61051-176">Поместить 8 шт. в контейнер CONT0004.</span><span class="sxs-lookup"><span data-stu-id="61051-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="61051-177">Кабель HDMI 6 футов:</span><span class="sxs-lookup"><span data-stu-id="61051-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="61051-178">Проверить, может ли номенклатура поместиться в контейнер CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="61051-179">Поместить 4 шт. в контейнер CONT0003.</span><span class="sxs-lookup"><span data-stu-id="61051-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="61051-180">Создать новый контейнер, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="61051-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="61051-181">Поместить 9 шт. в контейнер CONT0004.</span><span class="sxs-lookup"><span data-stu-id="61051-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="61051-182">Пример сценария: упаковка одиночных заказов на контейнер</span><span class="sxs-lookup"><span data-stu-id="61051-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="61051-183">В этом разделе представлен сценарий, в котором система настроена для консолидации нескольких заказов в одну отгрузку.</span><span class="sxs-lookup"><span data-stu-id="61051-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="61051-184">Таким образом, контейнер будет выполнен из заказа на продажу для того, чтобы упаковать каждый заказ, содержащий несколько продуктов, в свой собственный контейнер.</span><span class="sxs-lookup"><span data-stu-id="61051-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="61051-185">Эта функция позволяет обрабатывать сценарии, в которых необходимо упаковать в каждый контейнер только один заказ на продажу, чтобы центр распределения мог выполнить переброску полных контейнеров между розничными магазинами.</span><span class="sxs-lookup"><span data-stu-id="61051-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="61051-186">В дополнение к розничным сценариям (заказ на розничные магазины и отгрузка в центр распределения для кросс-докинга) этот прием также обычно используется в цепочках экономичных поставок (заказ на продажу по строке производства JIT).</span><span class="sxs-lookup"><span data-stu-id="61051-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="61051-187">Этот сценарий показывает, как можно уменьшить число контейнеров, оцениваемых во время упаковки, используя стратегию *Упаковать только в текущий контейнер* контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="61051-188">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="61051-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="61051-189">Включите функцию консолидации отгрузок в вашей системе</span><span class="sxs-lookup"><span data-stu-id="61051-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="61051-190">В этом сценарии используется функция *Консолидировать отгрузки*.</span><span class="sxs-lookup"><span data-stu-id="61051-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="61051-191">Если эта функция недоступна в системе, ее необходимо включить с помощью [управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="61051-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="61051-192">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="61051-192">Make demo data available</span></span>

<span data-ttu-id="61051-193">Этот сценарий ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="61051-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="61051-194">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="61051-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="61051-195">Проверка или создание типов контейнеров</span><span class="sxs-lookup"><span data-stu-id="61051-195">Inspect or create container types</span></span>

<span data-ttu-id="61051-196">Чтобы проверить типы контейнеров или создать новые типы контейнеров, если это необходимо, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="61051-197">Перейдите в раздел **Управление складом** \> **Настройка** \> **Контейнеры** \> **Типы контейнеров**.</span><span class="sxs-lookup"><span data-stu-id="61051-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="61051-198">Убедитесь, что в демонстрационных данных доступен каждый из следующих типов контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="61051-199">При необходимости измените или создайте типы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="61051-200">Тип контейнера 1:</span><span class="sxs-lookup"><span data-stu-id="61051-200">Container type 1:</span></span>

        - <span data-ttu-id="61051-201">**Код типа контейнера:** *Ящик-крупный*</span><span class="sxs-lookup"><span data-stu-id="61051-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="61051-202">**Описание:** *Ящик-крупный*</span><span class="sxs-lookup"><span data-stu-id="61051-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="61051-203">**Максимальный вес нетто:** *100*</span><span class="sxs-lookup"><span data-stu-id="61051-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="61051-204">**Объем:** *400*</span><span class="sxs-lookup"><span data-stu-id="61051-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="61051-205">**Длина:** *4*</span><span class="sxs-lookup"><span data-stu-id="61051-205">**Length:** *4*</span></span>
        - <span data-ttu-id="61051-206">**Ширина:** *10*</span><span class="sxs-lookup"><span data-stu-id="61051-206">**Width:** *10*</span></span>
        - <span data-ttu-id="61051-207">**Высота:** *10*</span><span class="sxs-lookup"><span data-stu-id="61051-207">**Height:** *10*</span></span>

    - <span data-ttu-id="61051-208">Тип контейнера 2:</span><span class="sxs-lookup"><span data-stu-id="61051-208">Container type 2:</span></span>

        - <span data-ttu-id="61051-209">**Код типа контейнера:** *Ящик-средний*</span><span class="sxs-lookup"><span data-stu-id="61051-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="61051-210">**Описание:** *Ящик средний*</span><span class="sxs-lookup"><span data-stu-id="61051-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="61051-211">**Максимальный вес нетто:** *50*</span><span class="sxs-lookup"><span data-stu-id="61051-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="61051-212">**Объем:** *200*</span><span class="sxs-lookup"><span data-stu-id="61051-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="61051-213">**Длина:** *2*</span><span class="sxs-lookup"><span data-stu-id="61051-213">**Length:** *2*</span></span>
        - <span data-ttu-id="61051-214">**Ширина:** *10*</span><span class="sxs-lookup"><span data-stu-id="61051-214">**Width:** *10*</span></span>
        - <span data-ttu-id="61051-215">**Высота:** *10*</span><span class="sxs-lookup"><span data-stu-id="61051-215">**Height:** *10*</span></span>

    - <span data-ttu-id="61051-216">Тип контейнера 3:</span><span class="sxs-lookup"><span data-stu-id="61051-216">Container type 3:</span></span>

        - <span data-ttu-id="61051-217">**Код типа контейнера:** *Ящик-малый*</span><span class="sxs-lookup"><span data-stu-id="61051-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="61051-218">**Описание:** *Ящик малый*</span><span class="sxs-lookup"><span data-stu-id="61051-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="61051-219">**Максимальный вес нетто:** *20*</span><span class="sxs-lookup"><span data-stu-id="61051-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="61051-220">**Объем:** *100*</span><span class="sxs-lookup"><span data-stu-id="61051-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="61051-221">**Длина:** *1*</span><span class="sxs-lookup"><span data-stu-id="61051-221">**Length:** *1*</span></span>
        - <span data-ttu-id="61051-222">**Ширина:** *10*</span><span class="sxs-lookup"><span data-stu-id="61051-222">**Width:** *10*</span></span>
        - <span data-ttu-id="61051-223">**Высота:** *10*</span><span class="sxs-lookup"><span data-stu-id="61051-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="61051-224">Проверка или создание групп контейнеров</span><span class="sxs-lookup"><span data-stu-id="61051-224">Inspect or create container groups</span></span>

<span data-ttu-id="61051-225">Чтобы проверить группы контейнеров или создать новые группы контейнеров, если это необходимо, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="61051-226">Перейдите в раздел **Управление складом** \> **Настройка** \> **Контейнеры** \> **Группы контейнеров**.</span><span class="sxs-lookup"><span data-stu-id="61051-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="61051-227">Убедитесь, что в демонстрационных данных доступен каждая из следующих групп контейнеров.</span><span class="sxs-lookup"><span data-stu-id="61051-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="61051-228">Если она недоступна, выберите **Создать**, чтобы создать ее.</span><span class="sxs-lookup"><span data-stu-id="61051-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="61051-229">**Код группы контейнеров:** *Ящики*</span><span class="sxs-lookup"><span data-stu-id="61051-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="61051-230">**Описание:** *Размеры ящиков*</span><span class="sxs-lookup"><span data-stu-id="61051-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="61051-231">Убедитесь, что на экспресс-вкладке **Сведения** для группы контейнеров *Ящики* есть следующие строки.</span><span class="sxs-lookup"><span data-stu-id="61051-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="61051-232">Если нет, выберите **Создать**, чтобы добавить их.</span><span class="sxs-lookup"><span data-stu-id="61051-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="61051-233">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="61051-233">Line 1:</span></span>

        - <span data-ttu-id="61051-234">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="61051-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="61051-235">**Тип контейнера:** *Ящик-крупный*</span><span class="sxs-lookup"><span data-stu-id="61051-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="61051-236">**Процент загрузки контейнера:** *100*</span><span class="sxs-lookup"><span data-stu-id="61051-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="61051-237">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="61051-237">Line 2:</span></span>

        - <span data-ttu-id="61051-238">**Порядковый номер**: *2*</span><span class="sxs-lookup"><span data-stu-id="61051-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="61051-239">**Тип контейнера:** *Ящик-средний*</span><span class="sxs-lookup"><span data-stu-id="61051-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="61051-240">**Процент загрузки контейнера:** *100*</span><span class="sxs-lookup"><span data-stu-id="61051-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="61051-241">Строка 3:</span><span class="sxs-lookup"><span data-stu-id="61051-241">Line 3:</span></span>

        - <span data-ttu-id="61051-242">**Порядковый номер**: *3*</span><span class="sxs-lookup"><span data-stu-id="61051-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="61051-243">**Тип контейнера:** *Ящик-малый*</span><span class="sxs-lookup"><span data-stu-id="61051-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="61051-244">**Процент загрузки контейнера:** *100*</span><span class="sxs-lookup"><span data-stu-id="61051-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="61051-245">Создайте новый шаблон сборки контейнера</span><span class="sxs-lookup"><span data-stu-id="61051-245">Create a new container build template</span></span>

<span data-ttu-id="61051-246">Чтобы создать шаблон сборки контейнера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="61051-247">Перейдите в раздел **Управление складом** \> **Настройка** \> **Контейнеры** \> **Шаблон создания контейнера**.</span><span class="sxs-lookup"><span data-stu-id="61051-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="61051-248">Выберите **Создать**, чтобы создать шаблон сборки контейнера со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="61051-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="61051-249">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="61051-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="61051-250">**Код шаблона контейнера:** *Ящик*</span><span class="sxs-lookup"><span data-stu-id="61051-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="61051-251">**Код группы контейнеров:** *Ящики*</span><span class="sxs-lookup"><span data-stu-id="61051-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="61051-252">**Типы базовых запросов:** *Строка распределения продаж*</span><span class="sxs-lookup"><span data-stu-id="61051-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="61051-253">**Код шага волны:** *234*</span><span class="sxs-lookup"><span data-stu-id="61051-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="61051-254">**Разрешить разделение комплектации:** *Да*</span><span class="sxs-lookup"><span data-stu-id="61051-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="61051-255">**Стратегия упаковки контейнера:** *Упаковать только в текущий контейнер*</span><span class="sxs-lookup"><span data-stu-id="61051-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="61051-256">**Упаковывать по единице директивы:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="61051-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="61051-257">Когда строка для нового шаблона все еще выбрана, выберите **Изменить запрос** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="61051-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="61051-258">Появляется диалоговое стандартного редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="61051-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="61051-259">На вкладке **Сортировка** выберите **Добавить**, чтобы добавить строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="61051-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="61051-260">**Таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="61051-261">**Производная таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="61051-262">**Поле:** *Номер заказа*</span><span class="sxs-lookup"><span data-stu-id="61051-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="61051-263">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="61051-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="61051-264">Чтобы избежать циклического переключения всех других открытых контейнеров и ускорения процесса путем проверки одного контейнера за один раз, используйте стратегию *Pack into current container only* в дополнение к сортировке только по номеру заказа.</span><span class="sxs-lookup"><span data-stu-id="61051-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="61051-265">Это сочетание будет работать как перерыв в работе в рабочем шаблоне.</span><span class="sxs-lookup"><span data-stu-id="61051-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="61051-266">Выберите **ОК**, чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="61051-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="61051-267">Пока строка для нового шаблона все еще выбрана, следует выбрать **Ограничения на смешивание контейнера** на панели действий.</span><span class="sxs-lookup"><span data-stu-id="61051-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="61051-268">Теперь можно добавить ограничение, которое поместит номенклатуры из одного заказа в один контейнер.</span><span class="sxs-lookup"><span data-stu-id="61051-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="61051-269">Номенклатуры из любого другого заказа будут помещаться в отдельный контейнер.</span><span class="sxs-lookup"><span data-stu-id="61051-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="61051-270">Выберите **Создать**, чтобы создать ограничение смешивания со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="61051-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="61051-271">**Таблица:** *Заказы на продажу*</span><span class="sxs-lookup"><span data-stu-id="61051-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="61051-272">**Выберите поле:** *SalesId* (Поле появится в сетке как *Заказ на продажу*.)</span><span class="sxs-lookup"><span data-stu-id="61051-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="61051-273">Нажмите **ОК**, чтобы добавить ограничение.</span><span class="sxs-lookup"><span data-stu-id="61051-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="61051-274">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="61051-275">Настройка шаблона волны для контейнеризации</span><span class="sxs-lookup"><span data-stu-id="61051-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="61051-276">Чтобы настроить шаблон волны, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="61051-277">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="61051-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="61051-278">В панели списка задайте в поле **Тип шаблона волн** значение *Отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="61051-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="61051-279">Выберите шаблон **63 Контейнеризация** в списке.</span><span class="sxs-lookup"><span data-stu-id="61051-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="61051-280">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="61051-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="61051-281">На экспресс-вкладке **Методы** в столбце **Выбранные методы** найдите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="61051-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="61051-282">**Имя метода:** *контейнеризация*</span><span class="sxs-lookup"><span data-stu-id="61051-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="61051-283">**Имя:** *Контейнеризация*</span><span class="sxs-lookup"><span data-stu-id="61051-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="61051-284">Задайте в поле **Код этапа волны** для строки значение *234*.</span><span class="sxs-lookup"><span data-stu-id="61051-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="61051-285">Настройка шаблона работы</span><span class="sxs-lookup"><span data-stu-id="61051-285">Set up a work template</span></span>

<span data-ttu-id="61051-286">Чтобы настроить шаблон работы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="61051-287">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="61051-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="61051-288">В поле **Тип заказа на работу** задайте значение *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="61051-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="61051-289">В сетке **Обзора** найдите и выберите рабочий шаблон, который должен использоваться для упаковки отдельных заказов на контейнер.</span><span class="sxs-lookup"><span data-stu-id="61051-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="61051-290">Для этого сценария выберите шаблон **63 Скомплектовать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="61051-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="61051-291">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="61051-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="61051-292">Появляется диалоговое стандартного редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="61051-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="61051-293">На вкладке **Сортировка** добавьте следующие строки:</span><span class="sxs-lookup"><span data-stu-id="61051-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="61051-294">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="61051-294">Line 1:</span></span>

        - <span data-ttu-id="61051-295">**Таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="61051-296">**Производная таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="61051-297">**Поле:** *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="61051-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="61051-298">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="61051-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="61051-299">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="61051-299">Line 2:</span></span>

        - <span data-ttu-id="61051-300">**Таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="61051-301">**Производная таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="61051-302">**Поле:** *Номер заказа*</span><span class="sxs-lookup"><span data-stu-id="61051-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="61051-303">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="61051-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="61051-304">Строка 3:</span><span class="sxs-lookup"><span data-stu-id="61051-304">Line 3:</span></span>

        - <span data-ttu-id="61051-305">**Таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="61051-306">**Производная таблица:** *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="61051-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="61051-307">**Поле:** *Код контейнера*</span><span class="sxs-lookup"><span data-stu-id="61051-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="61051-308">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="61051-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="61051-309">Выберите **ОК**, чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="61051-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="61051-310">Появится следующее сообщение: "Группирование будет сброшено, продолжить?"</span><span class="sxs-lookup"><span data-stu-id="61051-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="61051-311">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="61051-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="61051-312">Пока шаблон **63 Скомплектовать в контейнер** еще выбран, в области действий выберите **Разрывы заголовка работы**.</span><span class="sxs-lookup"><span data-stu-id="61051-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="61051-313">Теперь будут применены настройки для разбиения работы таким образом, чтобы каждый контейнер в заказе был связан с одним заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="61051-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="61051-314">Установите флажок **Группировать по этому полю** для каждой строки на странице **Разрывы заголовка работы** (**код отгрузки**, **номер заказа** и **код контейнера**).</span><span class="sxs-lookup"><span data-stu-id="61051-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="61051-315">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="61051-316">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="61051-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="61051-317">Чтобы настроить политику консолидации отгрузок, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="61051-318">Перейдите на страницу **Управление складом \> Настройка \> Запуск на склад \> политики консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="61051-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="61051-319">В области списка задайте в поле **Тип политики** значение *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="61051-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="61051-320">Выберите политику **По умолчанию** в списке.</span><span class="sxs-lookup"><span data-stu-id="61051-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="61051-321">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="61051-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="61051-322">На экспресс-вкладке **поля консолидации** в списке **Выбранные поля** выберите строку, где поле **Имя поля** установлено на значение *Номер заказа*.</span><span class="sxs-lookup"><span data-stu-id="61051-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="61051-323">Выберите кнопку **Удалить** ![Стрелка влево](media/backward-button.png), чтобы переместить поле в список **Оставшиеся поля**.</span><span class="sxs-lookup"><span data-stu-id="61051-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="61051-324">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="61051-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="61051-325">Настрого физических аналитик для продукта</span><span class="sxs-lookup"><span data-stu-id="61051-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="61051-326">Чтобы настроить физические аналитики для продуктов, которые будут использоваться в этом сценарии, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="61051-327">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="61051-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="61051-328">Выберите продукт, для которого коле **Код номенклатуры** задано как *A0001*.</span><span class="sxs-lookup"><span data-stu-id="61051-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="61051-329">На панели действий на вкладке **Управление складскими запасами** в группе **Склад** выберите **Физические размеры**.</span><span class="sxs-lookup"><span data-stu-id="61051-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="61051-330">На странице **Физические аналитики** должна отобразиться следующая строка в сетке:</span><span class="sxs-lookup"><span data-stu-id="61051-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="61051-331">**Единица измерения:** *шт*</span><span class="sxs-lookup"><span data-stu-id="61051-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="61051-332">**Вес брутто:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="61051-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="61051-333">**Ширина:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="61051-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="61051-334">**Глубина:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="61051-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="61051-335">**Высота:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="61051-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="61051-336">**Объем:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="61051-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="61051-337">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-337">Close the page.</span></span>
1. <span data-ttu-id="61051-338">Выберите продукт, для которого коле **Код номенклатуры** задано как *A0002*.</span><span class="sxs-lookup"><span data-stu-id="61051-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="61051-339">На панели действий на вкладке **Управление складскими запасами** в группе **Склад** выберите **Физические размеры**.</span><span class="sxs-lookup"><span data-stu-id="61051-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="61051-340">На странице **Физические аналитики** должна отобразиться следующая строка в сетке:</span><span class="sxs-lookup"><span data-stu-id="61051-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="61051-341">**Единица измерения:** *шт*</span><span class="sxs-lookup"><span data-stu-id="61051-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="61051-342">**Вес брутто:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="61051-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="61051-343">**Ширина:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="61051-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="61051-344">**Глубина:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="61051-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="61051-345">**Высота:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="61051-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="61051-346">**Объем:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="61051-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="61051-347">Создание заказа на продажу 1</span><span class="sxs-lookup"><span data-stu-id="61051-347">Create sales order 1</span></span>

<span data-ttu-id="61051-348">Чтобы создать заказ на продажу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61051-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="61051-349">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="61051-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="61051-350">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="61051-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61051-351">Появится диалоговое окно для создания нового заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="61051-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="61051-352">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="61051-352">Set the following values:</span></span>

    - <span data-ttu-id="61051-353">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="61051-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="61051-354">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="61051-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="61051-355">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="61051-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="61051-356">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="61051-356">The new sales order is opened.</span></span> <span data-ttu-id="61051-357">На экспресс-вкладке **Строки заказа на продажу** добавьте следующие строки продажи:</span><span class="sxs-lookup"><span data-stu-id="61051-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="61051-358">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="61051-358">Line 1:</span></span>

        - <span data-ttu-id="61051-359">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="61051-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="61051-360">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="61051-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="61051-361">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="61051-361">Line 2:</span></span>

        - <span data-ttu-id="61051-362">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="61051-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="61051-363">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="61051-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="61051-364">Выберите первую строку, а затем выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="61051-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="61051-365">На странице **Резервирование** выберите **Зарезервировать лот**.</span><span class="sxs-lookup"><span data-stu-id="61051-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="61051-366">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-366">Then close the page.</span></span>
1. <span data-ttu-id="61051-367">Повторите предыдущие два шага для второй строки.</span><span class="sxs-lookup"><span data-stu-id="61051-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="61051-368">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="61051-369">Создание заказа на продажу 2</span><span class="sxs-lookup"><span data-stu-id="61051-369">Create sales order 2</span></span>

<span data-ttu-id="61051-370">Выполните эти действия, чтобы создать второй заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="61051-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="61051-371">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="61051-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="61051-372">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="61051-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="61051-373">Появится диалоговое окно для создания нового заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="61051-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="61051-374">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="61051-374">Set the following values:</span></span>

    - <span data-ttu-id="61051-375">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="61051-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="61051-376">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="61051-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="61051-377">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="61051-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="61051-378">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="61051-378">The new sales order is opened.</span></span> <span data-ttu-id="61051-379">На экспресс-вкладке **Строки заказа на продажу** добавьте следующие строки продажи:</span><span class="sxs-lookup"><span data-stu-id="61051-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="61051-380">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="61051-380">Line 1:</span></span>

        - <span data-ttu-id="61051-381">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="61051-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="61051-382">**Количество:** *4*</span><span class="sxs-lookup"><span data-stu-id="61051-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="61051-383">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="61051-383">Line 2:</span></span>

        - <span data-ttu-id="61051-384">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="61051-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="61051-385">**Количество:** *4*</span><span class="sxs-lookup"><span data-stu-id="61051-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="61051-386">Выберите первую строку, а затем выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="61051-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="61051-387">На странице **Резервирование** выберите **Зарезервировать лот**.</span><span class="sxs-lookup"><span data-stu-id="61051-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="61051-388">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-388">Then close the page.</span></span>
1. <span data-ttu-id="61051-389">Повторите предыдущие два шага для второй строки.</span><span class="sxs-lookup"><span data-stu-id="61051-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="61051-390">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61051-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="61051-391">Создание загрузки</span><span class="sxs-lookup"><span data-stu-id="61051-391">Create the load</span></span>

<span data-ttu-id="61051-392">Выполните следующие действия, чтобы создать загрузку для каждого заказа, созданного для этого сценария, а затем выпустить на склад.</span><span class="sxs-lookup"><span data-stu-id="61051-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="61051-393">Перейдите в раздел **Управление складом \> Загрузки \> Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="61051-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="61051-394">На вкладке **строки продаж** найдите и выберите все строки заказа на продажу из заказов на продажу, созданных для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="61051-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="61051-395">В области действий на вкладке **Поставки и спрос** в группе **Добавить** выберите **В новую загрузку**.</span><span class="sxs-lookup"><span data-stu-id="61051-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="61051-396">Выбранные строки заказа добавляются к новой загрузке.</span><span class="sxs-lookup"><span data-stu-id="61051-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="61051-397">В диалоговом окне **Назначение шаблона загрузки** в поле **Код шаблона загрузки** выберите шаблон загрузки, например *40-футовый контейнер*.</span><span class="sxs-lookup"><span data-stu-id="61051-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="61051-398">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="61051-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="61051-399">В разделе **Загрузки** найдите и выберите только что созданную загрузку.</span><span class="sxs-lookup"><span data-stu-id="61051-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="61051-400">Выберите **Выпуск \> Выпуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="61051-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="61051-401">В диалоговом окне **Выпуск на склад** выберите **ОК**, чтобы выпустить выбранную загрузку на склад.</span><span class="sxs-lookup"><span data-stu-id="61051-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="61051-402">Проверка отгрузок и контейнеров</span><span class="sxs-lookup"><span data-stu-id="61051-402">Verify the shipments and containers</span></span>

<span data-ttu-id="61051-403">Следующая процедура позволяет проверить созданные отгрузки.</span><span class="sxs-lookup"><span data-stu-id="61051-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="61051-404">Используйте ее для просмотра заказа, созданного для этого сценария, чтобы убедиться, что получены ожидаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="61051-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="61051-405">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="61051-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="61051-406">Найдите и выберите отгрузку, которая была создана для только что выпущенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="61051-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="61051-407">На панели действий на вкладке **Транспортировка** и выберите **Просмотреть контейнеры**.</span><span class="sxs-lookup"><span data-stu-id="61051-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="61051-408">Убедитесь, что номенклатуры из заказов на продажу были помещены в два разных контейнера.</span><span class="sxs-lookup"><span data-stu-id="61051-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61051-409">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="61051-409">Additional resources</span></span>

- [<span data-ttu-id="61051-410">Контейнеризация</span><span class="sxs-lookup"><span data-stu-id="61051-410">Containerization</span></span>](wave-containerization.md)
