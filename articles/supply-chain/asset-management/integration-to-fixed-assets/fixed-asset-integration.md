---
title: Интеграция управления активами с основными средствами
description: В этой теме объясняется, как интегрировать модули управления активами и основных средств, чтобы можно было связывать основные средства с обслуживаемыми средствами.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276957"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="7e5b5-103">Интеграция управления активами с основными средствами</span><span class="sxs-lookup"><span data-stu-id="7e5b5-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e5b5-104">Путем интеграции модулей **Управление активами** и **Основные средства** можно связывать основные средства с обслуживаемыми средствами.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="7e5b5-105">Пользователи основных средств могут создать обслуживаемый актив из нового или существующего основного средства, а пользователи управления активами могут связать актив обслуживания с существующими основными средствами.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="7e5b5-106">Эта функция также упрощает для пользователей основных средств просмотр затрат, разнесенных из заказов на работу для соответствующих обслуживаемых активов.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="7e5b5-107">В этом разделе *обслуживаемые активы* означают активы из модуля **Управление активами**, а *основные средства* ссылаются на активы из модуля **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="7e5b5-108">Задание местоположения по умолчанию для новых обслуживаемых активов, которые создаются из основных средств (дополнительно)</span><span class="sxs-lookup"><span data-stu-id="7e5b5-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="7e5b5-109">Эта необязательная конфигурация позволяет задать функциональное местоположение по умолчанию для новых обслуживаемых активов, которые создаются из основных средств.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="7e5b5-110">Обычно эта конфигурация выполняется только один раз, если вообще выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="7e5b5-111">Чтобы завершить эту конфигурацию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-112">Перейдите в раздел **Управление активами \> Настройка \> Параметры управления активами**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="7e5b5-113">На вкладке **Основные средства** в поле **Функциональное местоположение** выберите местонахождение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="7e5b5-114">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="7e5b5-115">Работа с интегрированными обслуживаемыми активами и основными средствами</span><span class="sxs-lookup"><span data-stu-id="7e5b5-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="7e5b5-116">В этом разделе содержится набор процедур, в которых показаны различные возможные способы работы с интегрированными функциями управления активами и основными средствами.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="7e5b5-117">Связывание существующего обслуживаемого актива с основным средством</span><span class="sxs-lookup"><span data-stu-id="7e5b5-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="7e5b5-118">Чтобы связать существующий обслуживаемый актив с основным средством, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-119">Перейдите к пункту **Управление активами \> Активы \> Все активы** (или **Активные активы**).</span><span class="sxs-lookup"><span data-stu-id="7e5b5-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="7e5b5-120">Выберите актив.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-120">Select an asset.</span></span>
1. <span data-ttu-id="7e5b5-121">На экспресс-вкладке **Основное средство** в поле **Инвентарный номер ОС** выберите существующее ОС.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="7e5b5-122">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="7e5b5-123">Просмотр основного средства, связанного с выбранным обслуживаемым активом</span><span class="sxs-lookup"><span data-stu-id="7e5b5-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="7e5b5-124">Для просмотра основного средства, связанного с выбранным обслуживаемым активом, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-125">Перейдите к пункту **Управление активами \> Активы \> Все активы** (или **Активные активы**).</span><span class="sxs-lookup"><span data-stu-id="7e5b5-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="7e5b5-126">Выберите актив.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-126">Select an asset.</span></span>
1. <span data-ttu-id="7e5b5-127">На экспресс-вкладке **Основное средство** в поле **Инвентарный номер ОС** выберите ссылку.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="7e5b5-128">Будет открыта страница **Основные средства** для выбранного актива.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="7e5b5-129">(Как правило, эта страница находится по пути **Основные средства \> Основные средства \> Основные средства**.)</span><span class="sxs-lookup"><span data-stu-id="7e5b5-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="7e5b5-130">Просмотр обслуживаемого актива связанного с выбранным основным средством</span><span class="sxs-lookup"><span data-stu-id="7e5b5-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="7e5b5-131">Для просмотра обслуживаемого актива, связанного с выбранным основным средством, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-132">Перейдите в раздел **Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="7e5b5-133">Выберите актив.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-133">Select an asset.</span></span>
1. <span data-ttu-id="7e5b5-134">В области действий на вкладке **Управление активами**, в группе **Просмотр** выберите **Обслуживаемый актив**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="7e5b5-135">Открывается страница **Обслуживаемый актив** для актива, связанного с выбранным основным средством.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="7e5b5-136">(Как правило, эта страница находится по пути **Управление активами \> Активы \> Все активы**.)</span><span class="sxs-lookup"><span data-stu-id="7e5b5-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="7e5b5-137">Просмотр затрат на обслуживание, связанных с основным средством</span><span class="sxs-lookup"><span data-stu-id="7e5b5-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="7e5b5-138">Заказы на работу управления активами могут разноситься для обслуживаемых активов, и каждый из этих заказов на работу обычно имеет затраты.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="7e5b5-139">Когда основное средство связано с обслуживаемым активом, можно перейти непосредственно из ОС для просмотра связанных затрат.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="7e5b5-140">Для просмотра затрат на обслуживание, связанных с основным средством, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-141">Перейдите в раздел **Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="7e5b5-142">Выберите актив.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-142">Select an asset.</span></span>
1. <span data-ttu-id="7e5b5-143">В области действий на вкладке **Управление активами**, в группе **Просмотр** выберите **Затраты на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="7e5b5-144">Открывается страница **Затраты на обслуживание**, на которой отображаются соответствующие затраты.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="7e5b5-145">Создание нового обслуживаемого актива для существующего основного средства</span><span class="sxs-lookup"><span data-stu-id="7e5b5-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="7e5b5-146">Чтобы создать новый обслуживаемый актив для существующего основного средства, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-147">Перейдите в раздел **Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="7e5b5-148">Выберите актив.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-148">Select an asset.</span></span>
1. <span data-ttu-id="7e5b5-149">В области действий на вкладке **Управление активами**, в группе **Создать** выберите **Создать обслуживаемый актив**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="7e5b5-150">(Если этот параметр недоступен, обслуживаемый актив может уже быть связан с выбранным ОС.)</span><span class="sxs-lookup"><span data-stu-id="7e5b5-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="7e5b5-151">Завершите создание актива, как описано в разделе [Создание актива](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="7e5b5-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="7e5b5-152">Создание нового основного средства и добавление нового обслуживаемого актива для него</span><span class="sxs-lookup"><span data-stu-id="7e5b5-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="7e5b5-153">Чтобы создать новое основное средство и добавить новый обслуживаемый актив для него, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-154">Перейдите в раздел **Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="7e5b5-155">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7e5b5-156">Завершите создание основного средства, как описано в разделе [Создание основного средства](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="7e5b5-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="7e5b5-157">В области действий на вкладке **Управление активами**, в группе **Создать** выберите **Создать обслуживаемый актив**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="7e5b5-158">Завершите создание актива, как описано в разделе [Создание актива](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="7e5b5-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="7e5b5-159">Удаление связи между двумя активами</span><span class="sxs-lookup"><span data-stu-id="7e5b5-159">Remove the association between two assets</span></span>

<span data-ttu-id="7e5b5-160">В некоторых случаях может возникнуть необходимость отсоединить обслуживаемый актив от основного средства.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="7e5b5-161">Например, если необходимо [создать новый обслуживаемый актив](#new-maintenance-from-fixed) из основного средства, необходимо сначала удалить все существующие связи.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="7e5b5-162">Чтобы удалить существующую связь между обслуживаемым активом и основным средством, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="7e5b5-163">Перейдите к пункту **Управление активами \> Активы \> Все активы** (или **Активные активы**).</span><span class="sxs-lookup"><span data-stu-id="7e5b5-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="7e5b5-164">Найдите и откройте основное средство.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="7e5b5-165">На экспресс-вкладке **Основное средство** удалите значение из поля **Функциональное местоположение**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="7e5b5-166">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7e5b5-166">On the Action Pane, select **Save**.</span></span>
