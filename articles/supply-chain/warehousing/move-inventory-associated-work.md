---
title: "Перемещение запасов со связанной работой в Управлении складом"
description: "В этом разделе описывается, как настроить и применить поштучное подтверждение комплектации на мобильном устройстве."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2889f04017bdd20be05174146ba88a24cbefacbb
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="53ba3-103">Перемещение запасов со связанной работой в Управлении складом</span><span class="sxs-lookup"><span data-stu-id="53ba3-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53ba3-104">С помощью перемещения запасов можно решить, какие работники склада имеют доступ к перемещению зарезервированных запасов.</span><span class="sxs-lookup"><span data-stu-id="53ba3-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="53ba3-105">Это обеспечивает гибкость настройки склада, где можно принять решение не разрешать работнику выбирать новое местоположение комплектации для работы комплектации, которая уже создана.</span><span class="sxs-lookup"><span data-stu-id="53ba3-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="53ba3-106">Это также позволяет менеджеру склада управлять, какими навыками должны обладать некоторые менее опытные работники.</span><span class="sxs-lookup"><span data-stu-id="53ba3-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="53ba3-107">Гибкое управление повседневными операциями работников склада может быть полезно в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="53ba3-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="53ba3-108">Сценарий 1</span><span class="sxs-lookup"><span data-stu-id="53ba3-108">Scenario 1</span></span>
<span data-ttu-id="53ba3-109">У компании сравнительно небольшая зона приемки, которая перегружена палетами и ожидающими размещения коробками.</span><span class="sxs-lookup"><span data-stu-id="53ba3-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="53ba3-110">Ожидается крупная отгрузка в текущий день, поэтому принимающий сотрудник решает освободить зону приемки, переместив некоторые палеты в вторичные входящие зоны.</span><span class="sxs-lookup"><span data-stu-id="53ba3-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="53ba3-111">Сценарий 2</span><span class="sxs-lookup"><span data-stu-id="53ba3-111">Scenario 2</span></span>
<span data-ttu-id="53ba3-112">Опытный работник склада замечает возможность склада консолидировать номенклатуры в одном месте вместо их разделения по 3 близким местам с небольшим количеством в каждом.</span><span class="sxs-lookup"><span data-stu-id="53ba3-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="53ba3-113">Работник хочет объединить количество путем перемещения номенклатур из каждого из этих мест в одно место и для одного грузоместа.</span><span class="sxs-lookup"><span data-stu-id="53ba3-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="53ba3-114">Сценарий 3</span><span class="sxs-lookup"><span data-stu-id="53ba3-114">Scenario 3</span></span>
<span data-ttu-id="53ba3-115">Палета ожидает отгрузки в промежуточном местонахождении, например STAGE01, которое находится рядом с BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="53ba3-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="53ba3-116">Тем не менее, из-за изменения планов грузовик по плану прибывает в зону BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="53ba3-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="53ba3-117">Принимающий сотрудник знаете об этом и должен убедиться, что грузовику не придется ждать загрузки в STAGE01.</span><span class="sxs-lookup"><span data-stu-id="53ba3-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="53ba3-118">Принимающий сотрудник решает переместить номенклатуры в этой отгрузке из STAGE01 в зону STAGE04, которая ближе к новому месту назначения.</span><span class="sxs-lookup"><span data-stu-id="53ba3-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="53ba3-119">Текущие ограничения</span><span class="sxs-lookup"><span data-stu-id="53ba3-119">Current limitations</span></span>

<span data-ttu-id="53ba3-120">Резервирования работ, которые можно перемещать, ограничены заказом на продажу, выдачей по заказу на перемещение, приходом по заказу на перемещение, заказом на покупку и работой пополнения.</span><span class="sxs-lookup"><span data-stu-id="53ba3-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="53ba3-121">Перемещение номенклатур ограничено для предотвращения разбиения строк работы.</span><span class="sxs-lookup"><span data-stu-id="53ba3-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="53ba3-122">Это означает, что при наличии строки работы для 100 штук номенклатуры "A" из местонахождения Loc1, будет возможность переместить только 30 штук номенклатуры "A" из него в другое местонахождение.</span><span class="sxs-lookup"><span data-stu-id="53ba3-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="53ba3-123">Это приводит к разбивке существующей строки работы на 30 и 70, так как местонахождения теперь разные.</span><span class="sxs-lookup"><span data-stu-id="53ba3-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="53ba3-124">Для промежуточных сценариев, где грузоместо, из которого или в которое перемещаются товары, задается как целевое грузоместо для заказа работы, только перемещение всего грузоместа разрешено, чтобы не разбить целевое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="53ba3-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="53ba3-125">В настоящее время поддерживается только специальные перемещения.</span><span class="sxs-lookup"><span data-stu-id="53ba3-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="53ba3-126">Это означает, что вы не сможете переместить зарезервированные запасы посредством перемещения с помощью элементов меню мобильного устройства для шаблона.</span><span class="sxs-lookup"><span data-stu-id="53ba3-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="53ba3-127">Настройка разрешений для перемещения зарезервированных запасов для отдельных работников</span><span class="sxs-lookup"><span data-stu-id="53ba3-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="53ba3-128">Для работника, которому следует разрешить перемещение зарезервированных запасов, установите флажок **Разрешить перемещение запасов со связанной работой** в **Управление складом** > **Настройка** > **Работник**.</span><span class="sxs-lookup"><span data-stu-id="53ba3-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="53ba3-129">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="53ba3-129">Backported</span></span>

<span data-ttu-id="53ba3-130">Для этой функции поддерживается обратная совместимость с Microsoft Dynamics AX 2012 R3, она будет входить в состав CU12.</span><span class="sxs-lookup"><span data-stu-id="53ba3-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="53ba3-131">Ее можно также загрузить отдельно по номеру статьи базы знаний 3192548.</span><span class="sxs-lookup"><span data-stu-id="53ba3-131">It can also be downloaded individually through KB number 3192548.</span></span> 


