---
title: "Управление запасами магазина"
description: "В этой статье описываются типы документов, которые можно использовать для управления запасами."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="fa2b6-103">Управление запасами магазина</span><span class="sxs-lookup"><span data-stu-id="fa2b6-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="fa2b6-104">В этой статье описываются типы документов, которые можно использовать для управления запасами.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="fa2b6-105">Для управления запасами организации можно использовать следующие типы документов.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="fa2b6-106">Заказы на покупку</span><span class="sxs-lookup"><span data-stu-id="fa2b6-106">Purchase orders</span></span>
<span data-ttu-id="fa2b6-107">Заказы на покупку создаются в головном офисе.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="fa2b6-108">Если розничный склад включен в заголовок заказа на покупку, то заказ можно получить в магазине путем использования Modern POS (MPOS) или Cloud POS в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="fa2b6-109">После ввода полученных в магазине количеств их можно локально сохранить для дополнительной модификации.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="fa2b6-110">Кроме того, эти количества можно утвердить и отправить в головной офис.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="fa2b6-111">В головном офисе полученные в магазине количества отображаются в Dynamics 365 for Retail в поле **Немедленное получение** заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="fa2b6-112">Заказы на перемещение</span><span class="sxs-lookup"><span data-stu-id="fa2b6-112">Transfer orders</span></span>
<span data-ttu-id="fa2b6-113">Заказ на перемещение может указывать, что тот или иной магазин является местоположением, откуда можно отгрузить номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="fa2b6-114">В этом случае заказ на перемещение отображается в магазине как запрос на комплектацию в MPOS или Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="fa2b6-115">После комплектации запрошенных количеств они утверждаются и отправляются в головной офис.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="fa2b6-116">В головном офисе скомплектованные в магазине количества отображаются в Dynamics 365 for Retail в поле **Отгрузить сейчас** заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="fa2b6-117">Заказ на перемещение может указывать, что тот или иной магазин является местоположением, куда можно отгрузить товары.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="fa2b6-118">В этом случае заказ на перемещение отображается в магазине как запрос на получение в MPOS или Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="fa2b6-119">После ввода полученных в магазине количеств их можно локально сохранить для дополнительной модификации.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="fa2b6-120">Кроме того, эти количества можно утвердить и отправить в головной офис.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="fa2b6-121">В головном офисе полученные в магазине количества отображаются в Dynamics 365 for Retail в поле **Немедленное получение** заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="fa2b6-122">Инвентаризация запасов</span><span class="sxs-lookup"><span data-stu-id="fa2b6-122">Stock counts</span></span>
<span data-ttu-id="fa2b6-123">Инвентаризация запасов может быть плановой или незапланированной.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="fa2b6-124">Плановая инвентаризация инициируется головным офисом, при этом головной офис определяет, для каких номенклатур следует провести инвентаризацию.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="fa2b6-125">Головной офис создает документ инвентаризации, который можно получить в магазине и в котором указывается фактическое количество запасов в наличии в MPOS или Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="fa2b6-126">Внеплановая инвентаризация инициируется магазином, количества фактически доступных запасов обновляются в MPOS или Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="fa2b6-127">В отличие от плановых инвентаризаций во время внеплановой инвентаризации не используется предопределенный список номенклатур.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="fa2b6-128">По завершении инвентаризации любого типа соответствующая документацию утверждается и отправляется в головной офис.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="fa2b6-129">В головном офисе выполняется проверка и разнесение инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="fa2b6-130">Поиск запасов</span><span class="sxs-lookup"><span data-stu-id="fa2b6-130">Inventory lookup</span></span>
<span data-ttu-id="fa2b6-131">Текущее количество продукта в наличии в нескольких магазинах и складах можно просмотреть на странице "Поиск запасов".</span><span class="sxs-lookup"><span data-stu-id="fa2b6-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="fa2b6-132">Помимо текущего количества в наличии, для каждого отдельного магазина можно просмотреть будущие доступные для заказа (ATP) количества.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="fa2b6-133">Чтобы это сделать, выберите магазин, для которого вы хотите просмотреть ATP, и щелкните **Показать доступность магазина**.</span><span class="sxs-lookup"><span data-stu-id="fa2b6-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





