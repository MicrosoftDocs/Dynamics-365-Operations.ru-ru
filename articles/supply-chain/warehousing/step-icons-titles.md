---
title: Назначение значков и названий шагов для мобильного приложения Warehouse Management
description: В этом разделе описывается, как назначать значки и названия шагов для новых или настроенных потоков задач для мобильного приложения Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049372"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="7ddf6-103">Назначение значков и названий шагов для мобильного приложения Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="7ddf6-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ddf6-104">В этом разделе описывается, как назначать значки шагов и названия шагов для новых или настроенных потоков задач для мобильного приложения Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="7ddf6-105">На следующем рисунке показано, как будут отображаться значки и названия шагов в мобильном приложении Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="7ddf6-106">![Пример значка шага и названия шага в мобильном приложении Warehouse Management](media/step-icon-example.png "Пример значка шага и названия шага в мобильном приложении Warehouse Management")</span><span class="sxs-lookup"><span data-stu-id="7ddf6-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="7ddf6-107">Включение этой функции в системе</span><span class="sxs-lookup"><span data-stu-id="7ddf6-107">Turn on this feature in your system</span></span>

<span data-ttu-id="7ddf6-108">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="7ddf6-109">Администраторы могут использовать параметры [Управление компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="7ddf6-110">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7ddf6-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7ddf6-111">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="7ddf6-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7ddf6-112">**Название компонента:** *Параметры пользователя, значки и названия шагов для нового приложения склада*</span><span class="sxs-lookup"><span data-stu-id="7ddf6-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="7ddf6-113">Идентификаторы, классы и значки стандартных шагов</span><span class="sxs-lookup"><span data-stu-id="7ddf6-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="7ddf6-114">Каждый шаг в потоке задач определяется с помощью идентификатора шага, и у каждого идентификатора шага имеется соответствующий класс шага.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="7ddf6-115">Значок и заголовок шага указаны в каждом из классов шагов.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="7ddf6-116">Идентификаторы шагов и классы шагов</span><span class="sxs-lookup"><span data-stu-id="7ddf6-116">Step IDs and step classes</span></span>

<span data-ttu-id="7ddf6-117">В следующей таблице перечислены все доступные идентификаторы шагов, а также соответствующий класс шага.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="7ddf6-118">В качестве идентификатора шага используется имя элемента управления первичного поля ввода.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="7ddf6-119">Пример использования этих идентификаторов шагов и классов см. в реализации метода `WHSMobileAppStepInfoBuilder.stepId()` в разделе [Пример: назначение значков и заголовков шагов для настраиваемого потока](#example) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="7ddf6-120">Идентификатор шага</span><span class="sxs-lookup"><span data-stu-id="7ddf6-120">Step ID</span></span> | <span data-ttu-id="7ddf6-121">Класс шага</span><span class="sxs-lookup"><span data-stu-id="7ddf6-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="7ddf6-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-122">BatchDisposition</span></span> | <span data-ttu-id="7ddf6-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="7ddf6-124">Перевозчик</span><span class="sxs-lookup"><span data-stu-id="7ddf6-124">Carrier</span></span> | <span data-ttu-id="7ddf6-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="7ddf6-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="7ddf6-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-126">CatchWeight</span></span> | <span data-ttu-id="7ddf6-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="7ddf6-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="7ddf6-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="7ddf6-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="7ddf6-130">CatchWeightTag</span></span> | <span data-ttu-id="7ddf6-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="7ddf6-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="7ddf6-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="7ddf6-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="7ddf6-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="7ddf6-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="7ddf6-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="7ddf6-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="7ddf6-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="7ddf6-136">CheckDigit</span></span> | <span data-ttu-id="7ddf6-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="7ddf6-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="7ddf6-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-138">ClusterId</span></span> | <span data-ttu-id="7ddf6-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="7ddf6-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="7ddf6-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="7ddf6-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-142">ClusterPosition</span></span> | <span data-ttu-id="7ddf6-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="7ddf6-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-144">ConfigId</span></span> | <span data-ttu-id="7ddf6-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="7ddf6-146">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="7ddf6-146">Confirmation</span></span> | <span data-ttu-id="7ddf6-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="7ddf6-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="7ddf6-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="7ddf6-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="7ddf6-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="7ddf6-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="7ddf6-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="7ddf6-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="7ddf6-154">ContainerType</span></span> | <span data-ttu-id="7ddf6-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="7ddf6-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="7ddf6-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="7ddf6-156">CountingReasonCode</span></span> | <span data-ttu-id="7ddf6-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="7ddf6-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="7ddf6-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="7ddf6-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="7ddf6-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="7ddf6-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="7ddf6-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="7ddf6-160">CycleCountQty1</span></span> | <span data-ttu-id="7ddf6-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="7ddf6-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="7ddf6-162">CycleCountQty2</span></span> | <span data-ttu-id="7ddf6-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="7ddf6-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="7ddf6-164">CycleCountQty3</span></span> | <span data-ttu-id="7ddf6-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="7ddf6-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="7ddf6-166">CycleCountQty4</span></span> | <span data-ttu-id="7ddf6-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="7ddf6-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-168">Disposition</span></span> | <span data-ttu-id="7ddf6-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="7ddf6-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="7ddf6-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="7ddf6-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-172">DriverCheckInId</span></span> | <span data-ttu-id="7ddf6-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="7ddf6-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="7ddf6-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="7ddf6-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-176">DriverCheckOutId</span></span> | <span data-ttu-id="7ddf6-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="7ddf6-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="7ddf6-178">ExpDate</span></span> | <span data-ttu-id="7ddf6-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="7ddf6-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="7ddf6-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-180">FromBatchDisposition</span></span> | <span data-ttu-id="7ddf6-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="7ddf6-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="7ddf6-182">FromInventoryStatus</span></span> | <span data-ttu-id="7ddf6-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="7ddf6-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="7ddf6-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-184">FullQty</span></span> | <span data-ttu-id="7ddf6-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="7ddf6-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-186">InboundPut</span></span> | <span data-ttu-id="7ddf6-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="7ddf6-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-188">InventBatchId</span></span> | <span data-ttu-id="7ddf6-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="7ddf6-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="7ddf6-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-190">InventColorId</span></span> | <span data-ttu-id="7ddf6-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="7ddf6-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-192">InventLocation</span></span> | <span data-ttu-id="7ddf6-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="7ddf6-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-194">InventLocationId</span></span> | <span data-ttu-id="7ddf6-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="7ddf6-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="7ddf6-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-196">InventSerialId</span></span> | <span data-ttu-id="7ddf6-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="7ddf6-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-198">InventSizeId</span></span> | <span data-ttu-id="7ddf6-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="7ddf6-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-200">InventStatusId</span></span> | <span data-ttu-id="7ddf6-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="7ddf6-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="7ddf6-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-202">InventStyleId</span></span> | <span data-ttu-id="7ddf6-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="7ddf6-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-204">InventVersionId</span></span> | <span data-ttu-id="7ddf6-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="7ddf6-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-206">ItemId</span></span> | <span data-ttu-id="7ddf6-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="7ddf6-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="7ddf6-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-208">ITMContainerID</span></span> | <span data-ttu-id="7ddf6-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="7ddf6-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-210">ITMShipmentID</span></span> | <span data-ttu-id="7ddf6-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="7ddf6-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-212">KanbanCardId</span></span> | <span data-ttu-id="7ddf6-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="7ddf6-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="7ddf6-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="7ddf6-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="7ddf6-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-216">KanbanOrCardId</span></span> | <span data-ttu-id="7ddf6-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="7ddf6-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="7ddf6-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-218">LicensePlateId</span></span> | <span data-ttu-id="7ddf6-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="7ddf6-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="7ddf6-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-220">LoadId</span></span> | <span data-ttu-id="7ddf6-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="7ddf6-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="7ddf6-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="7ddf6-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-224">LocOrLP</span></span> | <span data-ttu-id="7ddf6-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="7ddf6-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="7ddf6-226">LocOrLP_From</span></span> | <span data-ttu-id="7ddf6-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="7ddf6-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="7ddf6-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="7ddf6-228">LocOrLP_To</span></span> | <span data-ttu-id="7ddf6-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="7ddf6-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="7ddf6-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="7ddf6-230">LocOrLPCheck</span></span> | <span data-ttu-id="7ddf6-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="7ddf6-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="7ddf6-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-232">LocVerification</span></span> | <span data-ttu-id="7ddf6-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="7ddf6-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="7ddf6-234">LPAdjustIn</span></span> | <span data-ttu-id="7ddf6-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="7ddf6-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="7ddf6-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-236">LPBreakChildLP</span></span> | <span data-ttu-id="7ddf6-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="7ddf6-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-238">LPBreakParentLP</span></span> | <span data-ttu-id="7ddf6-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="7ddf6-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-240">LPBuildChildLP</span></span> | <span data-ttu-id="7ddf6-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="7ddf6-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-242">LPBuildParentLP</span></span> | <span data-ttu-id="7ddf6-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="7ddf6-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-244">LPVerification</span></span> | <span data-ttu-id="7ddf6-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="7ddf6-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-246">MergeContainerId</span></span> | <span data-ttu-id="7ddf6-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="7ddf6-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-248">MixedLPLineNum</span></span> | <span data-ttu-id="7ddf6-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="7ddf6-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="7ddf6-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="7ddf6-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="7ddf6-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="7ddf6-252">MovementConfirmCancel</span></span> | <span data-ttu-id="7ddf6-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="7ddf6-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="7ddf6-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-254">NewCaptureWeight</span></span> | <span data-ttu-id="7ddf6-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="7ddf6-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-256">NewQty</span></span> | <span data-ttu-id="7ddf6-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="7ddf6-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="7ddf6-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="7ddf6-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="7ddf6-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="7ddf6-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-260">OutboundPut</span></span> | <span data-ttu-id="7ddf6-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="7ddf6-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-262">OutboundWeight</span></span> | <span data-ttu-id="7ddf6-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="7ddf6-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-264">OverridePutNewLocation</span></span> | <span data-ttu-id="7ddf6-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="7ddf6-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="7ddf6-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="7ddf6-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-268">POLineNum</span></span> | <span data-ttu-id="7ddf6-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="7ddf6-270">Номер заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="7ddf6-270">PONum</span></span> | <span data-ttu-id="7ddf6-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="7ddf6-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="7ddf6-272">PositionFull</span></span> | <span data-ttu-id="7ddf6-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="7ddf6-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="7ddf6-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-274">PositionFullQty</span></span> | <span data-ttu-id="7ddf6-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="7ddf6-276">Доля</span><span class="sxs-lookup"><span data-stu-id="7ddf6-276">Potency</span></span> | <span data-ttu-id="7ddf6-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="7ddf6-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="7ddf6-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="7ddf6-278">PrinterName</span></span> | <span data-ttu-id="7ddf6-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="7ddf6-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="7ddf6-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-280">ProdId</span></span> | <span data-ttu-id="7ddf6-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="7ddf6-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="7ddf6-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="7ddf6-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-284">ProductConfirmation</span></span> | <span data-ttu-id="7ddf6-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="7ddf6-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="7ddf6-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="7ddf6-288">Поместить</span><span class="sxs-lookup"><span data-stu-id="7ddf6-288">Put</span></span> | <span data-ttu-id="7ddf6-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="7ddf6-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-290">PutawayClusterId</span></span> | <span data-ttu-id="7ddf6-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="7ddf6-292">Кол-во</span><span class="sxs-lookup"><span data-stu-id="7ddf6-292">Qty</span></span> | <span data-ttu-id="7ddf6-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="7ddf6-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="7ddf6-294">QtyAdjust</span></span> | <span data-ttu-id="7ddf6-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="7ddf6-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="7ddf6-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="7ddf6-296">QtyShort</span></span> | <span data-ttu-id="7ddf6-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="7ddf6-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="7ddf6-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="7ddf6-298">QtyToConsume</span></span> | <span data-ttu-id="7ddf6-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="7ddf6-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="7ddf6-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="7ddf6-300">QtyToPick</span></span> | <span data-ttu-id="7ddf6-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="7ddf6-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="7ddf6-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-302">QtyToPut</span></span> | <span data-ttu-id="7ddf6-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="7ddf6-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="7ddf6-304">QtyToScrap</span></span> | <span data-ttu-id="7ddf6-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="7ddf6-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="7ddf6-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-306">QtyVerification</span></span> | <span data-ttu-id="7ddf6-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="7ddf6-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="7ddf6-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="7ddf6-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="7ddf6-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="7ddf6-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="7ddf6-310">ReasonString</span></span> | <span data-ttu-id="7ddf6-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="7ddf6-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="7ddf6-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-312">RecvLocationId</span></span> | <span data-ttu-id="7ddf6-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="7ddf6-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-314">RemoveContainerId</span></span> | <span data-ttu-id="7ddf6-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="7ddf6-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="7ddf6-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="7ddf6-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-318">RMANum</span></span> | <span data-ttu-id="7ddf6-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="7ddf6-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="7ddf6-320">ShortPickReason</span></span> | <span data-ttu-id="7ddf6-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="7ddf6-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="7ddf6-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-322">SortConOrLP</span></span> | <span data-ttu-id="7ddf6-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="7ddf6-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-324">SortLicensePlateId</span></span> | <span data-ttu-id="7ddf6-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="7ddf6-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-326">SortPositionId</span></span> | <span data-ttu-id="7ddf6-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="7ddf6-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-328">SortVerification</span></span> | <span data-ttu-id="7ddf6-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="7ddf6-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="7ddf6-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-330">StartLocationId</span></span> | <span data-ttu-id="7ddf6-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="7ddf6-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="7ddf6-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="7ddf6-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-334">TargetLicensePlateId</span></span> | <span data-ttu-id="7ddf6-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="7ddf6-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-336">TOLineNum</span></span> | <span data-ttu-id="7ddf6-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="7ddf6-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-338">ToLocation</span></span> | <span data-ttu-id="7ddf6-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="7ddf6-340">TONum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-340">TONum</span></span> | <span data-ttu-id="7ddf6-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="7ddf6-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="7ddf6-342">ToWarehouse</span></span> | <span data-ttu-id="7ddf6-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="7ddf6-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="7ddf6-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-344">TransportLoadId</span></span> | <span data-ttu-id="7ddf6-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="7ddf6-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-346">WaveLabelId</span></span> | <span data-ttu-id="7ddf6-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="7ddf6-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-348">WaveLblQty</span></span> | <span data-ttu-id="7ddf6-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="7ddf6-350">Вес</span><span class="sxs-lookup"><span data-stu-id="7ddf6-350">Weight</span></span> | <span data-ttu-id="7ddf6-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="7ddf6-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="7ddf6-352">WeightToConsume</span></span> | <span data-ttu-id="7ddf6-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="7ddf6-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="7ddf6-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="7ddf6-354">WHSAdjustmentType</span></span> | <span data-ttu-id="7ddf6-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="7ddf6-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="7ddf6-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="7ddf6-356">WHSReceivingException</span></span> | <span data-ttu-id="7ddf6-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="7ddf6-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="7ddf6-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="7ddf6-358">WHSWorkException</span></span> | <span data-ttu-id="7ddf6-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="7ddf6-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="7ddf6-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="7ddf6-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="7ddf6-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-362">WMSLocationId</span></span> | <span data-ttu-id="7ddf6-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="7ddf6-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-364">WorkId</span></span> | <span data-ttu-id="7ddf6-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="7ddf6-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="7ddf6-366">WorkIdToCancel</span></span> | <span data-ttu-id="7ddf6-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="7ddf6-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="7ddf6-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="7ddf6-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="7ddf6-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="7ddf6-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="7ddf6-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-370">WorkPoolId</span></span> | <span data-ttu-id="7ddf6-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="7ddf6-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-372">ZoneId</span></span> | <span data-ttu-id="7ddf6-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="7ddf6-374">Доступные значки шагов</span><span class="sxs-lookup"><span data-stu-id="7ddf6-374">Available step icons</span></span>

<span data-ttu-id="7ddf6-375">В системе имеется набор стандартных значков шагов, которые также можно использовать для пользовательских шагов.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="7ddf6-376">Сейчас вы не можете отправлять значки пользовательских шагов.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="7ddf6-377">Поэтому следует всегда выбирать один из стандартных значков шагов.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="7ddf6-378">В следующей таблице представлен каждый стандартный значок шагов, который в настоящее время доступен, и его имя.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Значок шага описания"><br><span data-ttu-id="7ddf6-380">О программе</span><span class="sxs-lookup"><span data-stu-id="7ddf6-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Значок шага добавления грузоместа или номенклатуры"><br><span data-ttu-id="7ddf6-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="7ddf6-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Значок этапа обработки партии"><br><span data-ttu-id="7ddf6-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Значок шага перевозчика"><br><span data-ttu-id="7ddf6-386">Перевозчик</span><span class="sxs-lookup"><span data-stu-id="7ddf6-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Значок шага тега учета в двух единицах измерения"><br><span data-ttu-id="7ddf6-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="7ddf6-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Значок шага веса тега учета в двух единицах измерения"><br><span data-ttu-id="7ddf6-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Значок шага контрольного разряда"><br><span data-ttu-id="7ddf6-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="7ddf6-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Значок шага кода получения или возврата"><br><span data-ttu-id="7ddf6-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Значок шага дочернего грузоместа"><br><span data-ttu-id="7ddf6-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Значок шага идентификатора кластера"><br><span data-ttu-id="7ddf6-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Значок шага положения кластера"><br><span data-ttu-id="7ddf6-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Значок шага идентификатора конфигурации"><br><span data-ttu-id="7ddf6-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Значок шага настраиваемого поля"><br><span data-ttu-id="7ddf6-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="7ddf6-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Значок шага контейнера или грузоместа"><br><span data-ttu-id="7ddf6-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Значок шага консолидации из кода грузоместа"><br><span data-ttu-id="7ddf6-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Значок шага консолидации в код грузоместа"><br><span data-ttu-id="7ddf6-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Значок шага типа контейнера"><br><span data-ttu-id="7ddf6-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="7ddf6-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Значок шага инвентаризации"><br><span data-ttu-id="7ddf6-414">Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="7ddf6-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Значок шага кода причины инвентаризации"><br><span data-ttu-id="7ddf6-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="7ddf6-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Значок шага кода страны происхождения"><br><span data-ttu-id="7ddf6-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="7ddf6-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Значок шага обработки"><br><span data-ttu-id="7ddf6-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Значок шага завершения"><br><span data-ttu-id="7ddf6-422">Выполнено</span><span class="sxs-lookup"><span data-stu-id="7ddf6-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Значок шага подтверждения прибытия водителя"><br><span data-ttu-id="7ddf6-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Значок шага кода прибытия водителя"><br><span data-ttu-id="7ddf6-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Значок шага кода отбытия водителя"><br><span data-ttu-id="7ddf6-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Значок шага даты окончания срока действия"><br><span data-ttu-id="7ddf6-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="7ddf6-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Значок шага поля"><br><span data-ttu-id="7ddf6-432">Поле</span><span class="sxs-lookup"><span data-stu-id="7ddf6-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Значок шага обработки из партии"><br><span data-ttu-id="7ddf6-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Значок шага статуса из запасов"><br><span data-ttu-id="7ddf6-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="7ddf6-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Значок шага атрибута идентификатора"><br><span data-ttu-id="7ddf6-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="7ddf6-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Значок шага кода складской партии"><br><span data-ttu-id="7ddf6-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Значок шага кода цвета запасов"><br><span data-ttu-id="7ddf6-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Значок шага местоположения запасов"><br><span data-ttu-id="7ddf6-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Значок шага кода серийного номера запасов"><br><span data-ttu-id="7ddf6-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Значок шага кода размера запасов"><br><span data-ttu-id="7ddf6-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Значок шага кода статуса запасов"><br><span data-ttu-id="7ddf6-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Значок шага кода стиля запасов"><br><span data-ttu-id="7ddf6-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Значок шага кода версии запасов"><br><span data-ttu-id="7ddf6-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Значок шага идентификатора номенклатуры"><br><span data-ttu-id="7ddf6-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Значок шага кода контейнера ITM"><br><span data-ttu-id="7ddf6-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Значок шага кода отгрузки ITM"><br><span data-ttu-id="7ddf6-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Значок шага кода карты канбана"><br><span data-ttu-id="7ddf6-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Значок шага кода канбана или карточки"><br><span data-ttu-id="7ddf6-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Значок шага кода грузоместа"><br><span data-ttu-id="7ddf6-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Значок шага идентификатора загрузки"><br><span data-ttu-id="7ddf6-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Значок шага позиции грузоместа в местонахождении"><br><span data-ttu-id="7ddf6-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="7ddf6-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Значок шага местоположения или грузоместа"><br><span data-ttu-id="7ddf6-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Значок шага проверки местоположения или грузоместа"><br><span data-ttu-id="7ddf6-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="7ddf6-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Значок шага исходного местоположения или грузоместа"><br><span data-ttu-id="7ddf6-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="7ddf6-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Значок шага целевого местоположения или грузоместа"><br><span data-ttu-id="7ddf6-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="7ddf6-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Значок шага завершения продолжительной обработки"><br><span data-ttu-id="7ddf6-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="7ddf6-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Значок шага разбиения грузоместа родительского грузоместа"><br><span data-ttu-id="7ddf6-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Значок шага кода объединения контейнера"><br><span data-ttu-id="7ddf6-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Значок шага нумерации строк смешанного грузоместа"><br><span data-ttu-id="7ddf6-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Значок шага исходящего веса"><br><span data-ttu-id="7ddf6-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="7ddf6-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Значок шага владельца"><br><span data-ttu-id="7ddf6-490">Ответственный</span><span class="sxs-lookup"><span data-stu-id="7ddf6-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Значок шага родительского грузоместа"><br><span data-ttu-id="7ddf6-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="7ddf6-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Значок шага подтверждения"><br><span data-ttu-id="7ddf6-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="7ddf6-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Значок шага номера строки заказа на продажу"><br><span data-ttu-id="7ddf6-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Значок шага номера заказа на продажу"><br><span data-ttu-id="7ddf6-498">Номер заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="7ddf6-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Значок шага заполненной позиции"><br><span data-ttu-id="7ddf6-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="7ddf6-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Значок шага доли"><br><span data-ttu-id="7ddf6-502">Доля</span><span class="sxs-lookup"><span data-stu-id="7ddf6-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Значок шага имени принтера"><br><span data-ttu-id="7ddf6-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="7ddf6-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Значок шага идентификатора продукта"><br><span data-ttu-id="7ddf6-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Значок шага подтверждения продукта"><br><span data-ttu-id="7ddf6-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Значок шага размещения"><br><span data-ttu-id="7ddf6-510">Поместить</span><span class="sxs-lookup"><span data-stu-id="7ddf6-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Значок шага идентификатора кластера размещения"><br><span data-ttu-id="7ddf6-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Значок шага количества"><br><span data-ttu-id="7ddf6-514">Кол-во</span><span class="sxs-lookup"><span data-stu-id="7ddf6-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Значок шага корректировки количества"><br><span data-ttu-id="7ddf6-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="7ddf6-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Значок шага недостающего количества"><br><span data-ttu-id="7ddf6-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="7ddf6-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Значок шага количества для потребления"><br><span data-ttu-id="7ddf6-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="7ddf6-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Значок шага количества для размещения"><br><span data-ttu-id="7ddf6-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="7ddf6-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Значок шага количества для списания в отходы"><br><span data-ttu-id="7ddf6-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="7ddf6-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Значок шага подтверждения количества"><br><span data-ttu-id="7ddf6-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Значок шага приемки завершенного задания"><br><span data-ttu-id="7ddf6-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="7ddf6-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Значок шага идентификатора местоположения получения"><br><span data-ttu-id="7ddf6-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Значок шага удаления кода контейнера"><br><span data-ttu-id="7ddf6-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Значок шага номера RMA"><br><span data-ttu-id="7ddf6-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Значок шага выбора заказа"><br><span data-ttu-id="7ddf6-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="7ddf6-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Значок шага причины недоукомплектования"><br><span data-ttu-id="7ddf6-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="7ddf6-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Значок шага кода позиции сортировки"><br><span data-ttu-id="7ddf6-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Значок шага кода целевого грузоместа"><br><span data-ttu-id="7ddf6-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Значок шага номера целевой строки"><br><span data-ttu-id="7ddf6-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Значок шага целевого местоположения"><br><span data-ttu-id="7ddf6-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="7ddf6-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Значок шага целевого номера"><br><span data-ttu-id="7ddf6-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="7ddf6-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Значок шага целевого склада"><br><span data-ttu-id="7ddf6-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="7ddf6-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Значок шага идентификатора транспортной загрузки"><br><span data-ttu-id="7ddf6-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Значок шага кода партии поставщика"><br><span data-ttu-id="7ddf6-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Значок шага кода метки волны"><br><span data-ttu-id="7ddf6-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Значок шага количества метки волны"><br><span data-ttu-id="7ddf6-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="7ddf6-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Значок шага веса"><br><span data-ttu-id="7ddf6-560">Вес</span><span class="sxs-lookup"><span data-stu-id="7ddf6-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Значок шага веса для потребления"><br><span data-ttu-id="7ddf6-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="7ddf6-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Значок шага типа корректировки WHS"><br><span data-ttu-id="7ddf6-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="7ddf6-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Значок шага исключения приемки WHS"><br><span data-ttu-id="7ddf6-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="7ddf6-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Значок шага кода местоположения WHS"><br><span data-ttu-id="7ddf6-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Значок шага идентификатора работы"><br><span data-ttu-id="7ddf6-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Значок шага кода работы для отмены"><br><span data-ttu-id="7ddf6-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="7ddf6-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Значок шага кода грузоместа работы"><br><span data-ttu-id="7ddf6-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="7ddf6-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Значок шага кластера размещения кода грузоместа работы"><br><span data-ttu-id="7ddf6-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="7ddf6-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Значок шага идентификатора пула работ"><br><span data-ttu-id="7ddf6-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Значок шага идентификатора зоны"><br><span data-ttu-id="7ddf6-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="7ddf6-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="7ddf6-581">Пример: назначение значков и заголовков шагов для настраиваемого потока</span><span class="sxs-lookup"><span data-stu-id="7ddf6-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="7ddf6-582">В этом примере объясняется, как настроить значки и названия шагов для настраиваемого потока задач.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="7ddf6-583">Сценарий создан на примере пользовательского потока задач, который более подробно представлен и изучен в следующей записи блога: [Настройка складских приложений для мобильных устройств](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="7ddf6-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="7ddf6-584">Поток задач выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7ddf6-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="7ddf6-585">Приложение отображает страницу, которая предлагает сотруднику указать идентификатор контейнера (например, путем сканирования штрих-кода).</span><span class="sxs-lookup"><span data-stu-id="7ddf6-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="7ddf6-586">Если код контейнера допустим, приложение открывает новую страницу, которая предлагает сотруднику ввести вес.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="7ddf6-587">(Если код контейнера недействителен, сотрудник возвращается на первую страницу.)</span><span class="sxs-lookup"><span data-stu-id="7ddf6-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="7ddf6-588">Когда работник вводит допустимый вес, система сохраняет вес и возвращает сотрудника на первую страницу.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="7ddf6-589">Следующая иллюстрация показывает этот поток задач.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="7ddf6-590">![Схема потока задач](media/step-icons-example-task-flow.png "Схема потока задач")</span><span class="sxs-lookup"><span data-stu-id="7ddf6-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="7ddf6-591">Создание класса шага для страницы ввода контейнера</span><span class="sxs-lookup"><span data-stu-id="7ddf6-591">Create a step class for the container input page</span></span>

<span data-ttu-id="7ddf6-592">Страница ввода контейнера позволяет работнику сканировать или вводить идентификатор контейнера.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="7ddf6-593">![Страница ввода контейнера](media/step-icons-example-container-input.png "Страница ввода контейнера")</span><span class="sxs-lookup"><span data-stu-id="7ddf6-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="7ddf6-594">На странице ввода контейнера имя элемента управления для поля ввода будет `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="7ddf6-595">Поскольку это имя элемента управления не отображается в [списке кодов шагов](#step-ids-classes), вы не найдете существующего шага, основанного на нем.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="7ddf6-596">Поэтому необходимо создать класс шага, представляющий этот шаг.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="7ddf6-597">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="7ddf6-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="7ddf6-598">Идентификатор значка шага хранится в участнике класса `defaultStepIcon`, а заголовок шага сохраняется в участнике класса `defaultStepTitle`.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="7ddf6-599">Чтобы назначить значок шага, установите `defaultStepIcon` на один из кодов значков, которые указаны в разделе [Доступные значки шагов](#step-icons) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="7ddf6-600">Использование стандартного или пользовательского значка и заголовка шага для ввода веса</span><span class="sxs-lookup"><span data-stu-id="7ddf6-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="7ddf6-601">Страница ввода веса позволяет сотруднику ввести вес.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="7ddf6-602">![Страница ввода веса](media/step-icons-example-weight-input.png "Страница ввода веса")</span><span class="sxs-lookup"><span data-stu-id="7ddf6-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="7ddf6-603">На странице ввода веса имя элемента управления поля ввода равно `Weight`, которое находится в [списке кодов шагов](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="7ddf6-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="7ddf6-604">Таким образом, если значок и заголовок шага, заданные в классе `WHSMobileAppStepWeight`, являются приемлемыми для вас, вам не придется ничего изменять для этого шага.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="7ddf6-605">Однако, если вы предпочитаете использовать для этого шага другие значок или заголовок, можно переопределить метод `stepId()` или метод `stepInfo()` в классе конструктора.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="7ddf6-606">У каждого потока задач имеется свой собственный конструктор информации о шаге.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="7ddf6-607">Переопределение метода stepId()</span><span class="sxs-lookup"><span data-stu-id="7ddf6-607">Override the stepId() method</span></span>

<span data-ttu-id="7ddf6-608">В следующем примере показан один из способов изменения класса конструктора путем переопределения метода `stepId()`.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="7ddf6-609">Затем создается класс шага для шага `NewWeight`.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="7ddf6-610">Код должен походить на код для примера `ContainerId`, приведенного ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="7ddf6-611">Переопределение метода stepInfo()</span><span class="sxs-lookup"><span data-stu-id="7ddf6-611">Override the stepInfo() method</span></span>

<span data-ttu-id="7ddf6-612">В следующем примере показан один из способов изменения класса конструктора путем переопределения метода `stepInfo()`.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="7ddf6-613">После этого создается объект `WHSMobileAppStepInfo` и устанавливается значок и/или заголовок непосредственно.</span><span class="sxs-lookup"><span data-stu-id="7ddf6-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ddf6-614">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7ddf6-614">Additional resources</span></span>

- [<span data-ttu-id="7ddf6-615">Установка и подключение мобильного приложения "Управление складом"</span><span class="sxs-lookup"><span data-stu-id="7ddf6-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="7ddf6-616">Параметры пользователя мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="7ddf6-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
