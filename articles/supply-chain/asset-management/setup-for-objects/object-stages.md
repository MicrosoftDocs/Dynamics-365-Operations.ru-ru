---
title: Состояния жизненного цикла активов
description: В этом разделе объясняются состояния жизненного цикла активов и модели жизненного цикла в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435944"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="83882-103">Состояния жизненного цикла активов</span><span class="sxs-lookup"><span data-stu-id="83882-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="83882-104">В этом разделе объясняются состояния жизненного цикла активов и модели жизненного цикла в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="83882-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="83882-105">Состояния жизненного цикла актива используются для определения того, активен актив или нет.</span><span class="sxs-lookup"><span data-stu-id="83882-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="83882-106">Например, можно настроить состояния жизненного цикла актива, такие как **Создано**, **Активно** и **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="83882-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="83882-107">Состояния жизненного цикла запроса связаны с состояниями жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="83882-108">Поэтому при изменении запроса на новое состояние жизненного цикла запроса, актив, приложенный к запросу, изменяется на новое состояние жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="83882-109">Например, если состояние жизненного цикла запроса изменено на **Входящие**, состояние жизненного цикла прилагаемого актива изменяется на состояние жизненного цикла, выбранное в поле **Входящее состояние жизненного цикла** на экспресс-вкладке **Состояние жизненного цикла актива** страницы **Модели состояния жизненного цикла актива**.</span><span class="sxs-lookup"><span data-stu-id="83882-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="83882-110">Состояния жизненного цикла актива могут быть настроены в моделях жизненного цикла актива, где можно определить требуемые состояния жизненного цикла для различных типов активов.</span><span class="sxs-lookup"><span data-stu-id="83882-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="83882-111">Сначала необходимо настроить состояния жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-111">You first set up lifecycle states.</span></span> <span data-ttu-id="83882-112">Затем создать модель жизненного цикла и выбрать для нее состояния жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="83882-113">Выберите **Управление активами** \> **Настройка** \> **Активы** \> **Состояния жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="83882-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="83882-114">Выберите **Создать**, чтобы создать новое состояние жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="83882-115">В поле **Состояние жизненного цикла** введите идентификатор состояния жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="83882-116">В поле **Имя** введите описание.</span><span class="sxs-lookup"><span data-stu-id="83882-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="83882-117">Поле **Модели жизненного цикла** показывает количество моделей жизненного цикла актива, которые используют состояние жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="83882-118">Установите параметр **Активно** на **Да**, если это состояние жизненного цикла должно быть активным состоянием жизненного цикла (другими словами, если заказы на работу могут быть созданы для активов, находящихся в этом состоянии жизненного цикла).</span><span class="sxs-lookup"><span data-stu-id="83882-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="83882-119">Установите параметр **Удалить открытые строки календаря** на **Да**, если открытые строки календаря актива, имеющие состояние жизненного цикла актива **Создано** следует исключить, когда они находятся в этом состоянии жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="83882-120">Эта настройка полезна, если требуется очистить все открытые графики обслуживания, которые больше не актуальны для актива (например, если актив больше не активен).</span><span class="sxs-lookup"><span data-stu-id="83882-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="83882-121">Состояния жизненного цикла актива, модели жизненного цикла актива и типы актива взаимосвязаны.</span><span class="sxs-lookup"><span data-stu-id="83882-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="83882-122">Они используются так же, как состояния жизненного цикла заказа на работу, модели жизненного цикла заказа на работу и типы заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="83882-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="83882-123">После создания требуемых состояний жизненного цикла актива можно настроить состояния жизненного цикла в моделях жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="83882-124">Выберите **Управление активами** \> **Настройка** \> **Активы** \> **Модели жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="83882-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="83882-125">Выберите **Создать**, чтобы создать новую модель жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="83882-126">В поле **Модель жизненного цикла** введите идентификатор модели жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="83882-127">В поле **Имя** введите описание.</span><span class="sxs-lookup"><span data-stu-id="83882-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="83882-128">Поле **Состояния жизненного цикла** показывает количество состояний жизненного цикла актива, которые выбраны в модели жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="83882-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="83882-129">Поле **Типы актива** показывает количество типов актива, которые используют модель жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="83882-130">На экспресс-вкладке **Состояния жизненного цикла** выберите состояния жизненного цикла актива, которые должны быть включены в модель жизненного цикла актива:</span><span class="sxs-lookup"><span data-stu-id="83882-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="83882-131">Чтобы использовать состояние жизненного цикла для модели, выберите его в разделе **Осталось состояний жизненного цикла**, а затем выберите кнопку со стрелкой вправо ![Стрелка вправо](media/15-setup-for-objects.png), чтобы переместить его в раздел **Выбранные состояния жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="83882-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="83882-132">Чтобы использовать все доступные состояния жизненного цикла для модели, выберите кнопку **Все доступные состояния жизненного цикла** ![Все доступные состояния жизненного цикла](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="83882-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="83882-133">Все состояния жизненного цикла перемещаются в раздел **Выбранные состояния жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="83882-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="83882-134">Чтобы удалить состояние жизненного цикла из модели, выберите его в разделе **Выбранные состояния жизненного цикла**, а затем выберите кнопку со стрелкой влево ![Стрелка влево](media/16-setup-for-objects.png), чтобы переместить его в раздел **Осталось состояний жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="83882-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="83882-135">Выберите **Обновления состояния жизненного цикла** для определения состояний жизненного цикла актива, которые могут следовать выбранноому состоянию жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="83882-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="83882-136">Вы используете экспресс-вкладку **Состояние актива** при обработке активов, которые вы получаете для ремонта.</span><span class="sxs-lookup"><span data-stu-id="83882-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="83882-137">В разделе **Входящие/Исходящие** можно выбрать состояния жизненного цикла актива, чтобы указать workflow-процесс актива, который вы получаете для ремонта.</span><span class="sxs-lookup"><span data-stu-id="83882-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="83882-138">Если вы предлагаете кредитные активы клиентам или подразделениям, в разделе **Временное пользование** вы можете выбрать состояния жизненного цикла для кредитных активов.</span><span class="sxs-lookup"><span data-stu-id="83882-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
