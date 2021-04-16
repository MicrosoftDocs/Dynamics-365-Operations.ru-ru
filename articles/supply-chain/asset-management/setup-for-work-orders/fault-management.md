---
title: Управление ошибками
description: В этом разделе описывается управление ошибками в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87bfa057fd2808551674f2acb9d654ad47e9a42
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825670"
---
# <a name="fault-management"></a><span data-ttu-id="2fc15-103">Управление ошибками</span><span class="sxs-lookup"><span data-stu-id="2fc15-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2fc15-104">В управлении активами можно использовать конструктор неисправностей для настройки симптомов проблем, областей проблем и типов проблем в типах актива.</span><span class="sxs-lookup"><span data-stu-id="2fc15-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="2fc15-105">Таким образом можно управлять ошибками, обнаруженными в активах.</span><span class="sxs-lookup"><span data-stu-id="2fc15-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="2fc15-106">Кроме того, в заказе на работу могут регистрироваться причины неисправности и предложения по устранению неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="2fc15-107">Процесс регистрации неисправностей и управления ими состоит из следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="2fc15-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="2fc15-108">Создайте список симптомов проблемы, областей неисправностей и типов неисправностей, которые могут встретиться в типах активов.</span><span class="sxs-lookup"><span data-stu-id="2fc15-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="2fc15-109">В конструкторе неисправностей настройте признаки, области неисправностей и типы неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="2fc15-110">Ниже приведены некоторые примеры, которые помогут понять различие между симптомами проблемы, областями проблем и типами неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="2fc15-111">**Симптомы ошибки:**</span><span class="sxs-lookup"><span data-stu-id="2fc15-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="2fc15-112">Несбалансированное напряжение</span><span class="sxs-lookup"><span data-stu-id="2fc15-112">Unbalanced voltages</span></span>
- <span data-ttu-id="2fc15-113">Короткое замыкание</span><span class="sxs-lookup"><span data-stu-id="2fc15-113">Short circuit</span></span>
- <span data-ttu-id="2fc15-114">Шум</span><span class="sxs-lookup"><span data-stu-id="2fc15-114">Noise</span></span>
- <span data-ttu-id="2fc15-115">Утечка</span><span class="sxs-lookup"><span data-stu-id="2fc15-115">Leak</span></span>
- <span data-ttu-id="2fc15-116">Вибрации</span><span class="sxs-lookup"><span data-stu-id="2fc15-116">Vibrations</span></span>

<span data-ttu-id="2fc15-117">**Области ошибки:**</span><span class="sxs-lookup"><span data-stu-id="2fc15-117">**Fault areas:**</span></span>

- <span data-ttu-id="2fc15-118">Электрическая</span><span class="sxs-lookup"><span data-stu-id="2fc15-118">Electrical</span></span>
- <span data-ttu-id="2fc15-119">Механическая</span><span class="sxs-lookup"><span data-stu-id="2fc15-119">Mechanical</span></span>
- <span data-ttu-id="2fc15-120">Гидравлическая</span><span class="sxs-lookup"><span data-stu-id="2fc15-120">Hydraulic</span></span>
- <span data-ttu-id="2fc15-121">Пневматика</span><span class="sxs-lookup"><span data-stu-id="2fc15-121">Pneumatic</span></span>

<span data-ttu-id="2fc15-122">**Типы ошибки:**</span><span class="sxs-lookup"><span data-stu-id="2fc15-122">**Fault types:**</span></span>

- <span data-ttu-id="2fc15-123">Неисправность основной обмотки статора</span><span class="sxs-lookup"><span data-stu-id="2fc15-123">Faulty main stator winding</span></span>
- <span data-ttu-id="2fc15-124">Неисправный диод</span><span class="sxs-lookup"><span data-stu-id="2fc15-124">Faulty diode</span></span>
- <span data-ttu-id="2fc15-125">Грязные обмотки</span><span class="sxs-lookup"><span data-stu-id="2fc15-125">Dirty windings</span></span>
- <span data-ttu-id="2fc15-126">Бракованный генератор</span><span class="sxs-lookup"><span data-stu-id="2fc15-126">Defective generator</span></span>
- <span data-ttu-id="2fc15-127">Дефектный датчик</span><span class="sxs-lookup"><span data-stu-id="2fc15-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="2fc15-128">Создание симптомов неисправностей</span><span class="sxs-lookup"><span data-stu-id="2fc15-128">Create fault symptoms</span></span>

<span data-ttu-id="2fc15-129">Выполните следующие действия, чтобы создать список симптомов, которые могут использоваться в конструкторе неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="2fc15-130">Выберите **Управление активами** \> **Настройка** \> **Неисправность** \> **Признаки неисправности**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="2fc15-131">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="2fc15-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2fc15-132">В поле **Признак неисправности** введите имя симптома отказа.</span><span class="sxs-lookup"><span data-stu-id="2fc15-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="2fc15-133">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2fc15-134">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="2fc15-135">Создание областей неисправностей</span><span class="sxs-lookup"><span data-stu-id="2fc15-135">Create fault areas</span></span>

<span data-ttu-id="2fc15-136">Выполните следующие действия, чтобы создать список областей или мест, которые могут использоваться в конструкторе неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="2fc15-137">Выберите **Управление активами** \> **Настройка** \> **Неисправность** \> **Области неисправности**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="2fc15-138">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="2fc15-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2fc15-139">В поле **Область неисправности** введите имя области отказа.</span><span class="sxs-lookup"><span data-stu-id="2fc15-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="2fc15-140">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2fc15-141">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="2fc15-142">Создание типов неисправностей</span><span class="sxs-lookup"><span data-stu-id="2fc15-142">Create fault types</span></span>

<span data-ttu-id="2fc15-143">Выполните следующие действия, чтобы создать список типов неисправностей, которые могут использоваться в конструкторе неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="2fc15-144">Выберите **Управление активами** \> **Настройка** \> **Неисправность** \> **Типы неисправностей**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="2fc15-145">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="2fc15-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2fc15-146">В поле **Тип неисправности** введите имя для типа неисправности.</span><span class="sxs-lookup"><span data-stu-id="2fc15-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="2fc15-147">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2fc15-148">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="2fc15-149">Настройка конструктора неисправностей</span><span class="sxs-lookup"><span data-stu-id="2fc15-149">Set up the fault designer</span></span>

<span data-ttu-id="2fc15-150">В конструкторе неисправностей настраиваются данные о неисправностях для типов активов.</span><span class="sxs-lookup"><span data-stu-id="2fc15-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="2fc15-151">Выберите **Управление активами** \> **Настройка** \> **Неисправность** \> **Конструктор неисправностей**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="2fc15-152">В левой области выберите тип актива, для которого необходимо настроить запись неисправности.</span><span class="sxs-lookup"><span data-stu-id="2fc15-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="2fc15-153">На экспресс-вкладке **Симптом отказа** выберите **Добавить строку**, затем в поле **Симптом отказа** выберите симптом отказа.</span><span class="sxs-lookup"><span data-stu-id="2fc15-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="2fc15-154">На экспресс-вкладке **Область отказа** выберите **Добавить строку**, затем в поле **Область отказа** выберите область отказа.</span><span class="sxs-lookup"><span data-stu-id="2fc15-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="2fc15-155">На экспресс-вкладке **Тип отказа** выберите **Добавить строку**, затем в поле **Тип отказа** выберите тип отказа.</span><span class="sxs-lookup"><span data-stu-id="2fc15-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="2fc15-156">Чтобы быстро создать комбинации всех существующих симптомов, областей и типов отказов для выбранного типа актива, выберите **Создать комбинации отказов**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="2fc15-157">Эта функция полезна, если добавлено множество признаков, областей и типов отказов.</span><span class="sxs-lookup"><span data-stu-id="2fc15-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="2fc15-158">Проще удалять строки для любых комбинаций, не имеющих отношения к типу актива, чем создавать новые строки вручную.</span><span class="sxs-lookup"><span data-stu-id="2fc15-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fc15-159">Чтобы скопировать настройку симптомов, областей и типов отказов из одного типа активов в выбранный тип актива, выберите **Копировать из типа актива**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="2fc15-160">Выберите **Сохранить** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="2fc15-160">Select **Save** to save your changes.</span></span>

![Страница конструктора неисправностей](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="2fc15-162">Создание причин неисправностей</span><span class="sxs-lookup"><span data-stu-id="2fc15-162">Create fault causes</span></span>

<span data-ttu-id="2fc15-163">Выполните следующие действия, чтобы создать список известных причин неисправности, которые могут быть добавлены к рабочему заказу или к запросу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="2fc15-164">Выберите **Управление активами** \> **Настройка** \> **Неисправность** \> **Причины неисправностей**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="2fc15-165">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="2fc15-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2fc15-166">В поле **Причина неисправности** введите имя для причины неисправности.</span><span class="sxs-lookup"><span data-stu-id="2fc15-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="2fc15-167">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2fc15-168">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="2fc15-169">Создание способов устранения неисправностей</span><span class="sxs-lookup"><span data-stu-id="2fc15-169">Create fault remedies</span></span>

<span data-ttu-id="2fc15-170">Выполните следующие действия, чтобы создать список предложений по устранению и ремонту, которые могут быть добавлены к рабочему заказу или к запросу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="2fc15-171">Выберите **Управление активами** \> **Настройка** \> **Неисправность** \> **Способы устранения неисправности**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="2fc15-172">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="2fc15-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="2fc15-173">В поле **Способ устранения неисправности** введите имя способа устранения отказа.</span><span class="sxs-lookup"><span data-stu-id="2fc15-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="2fc15-174">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="2fc15-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2fc15-175">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="2fc15-176">При необходимости можно изменить имена признаков, областей, типов, причин и способов устранения неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="2fc15-177">Изменения имен автоматически отражаются в соответствующих регистрациях неисправностей.</span><span class="sxs-lookup"><span data-stu-id="2fc15-177">The name changes are automatically reflected in the related fault registrations.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]