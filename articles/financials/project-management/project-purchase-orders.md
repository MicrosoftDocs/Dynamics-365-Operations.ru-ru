---
title: "Заказы на покупку для проекта"
description: "В этой статье описывают различные методы, которые можно использовать для создания заказов на покупку для проекта. Используемый метод зависит от назначения заказа на покупку и времени, когда приобретенная номенклатура используется и выставляется проекту."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a900ae4c81a4dbb654a4c395cd62f0a19a4acd67
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="4db06-104">Заказы на покупку для проекта</span><span class="sxs-lookup"><span data-stu-id="4db06-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4db06-105">В этой статье описывают различные методы, которые можно использовать для создания заказов на покупку для проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="4db06-106">Используемый метод зависит от назначения заказа на покупку и времени, когда приобретенная номенклатура используется и выставляется проекту.</span><span class="sxs-lookup"><span data-stu-id="4db06-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="4db06-107">В Microsoft Dynamics 365 for Finance and Operations можно использовать несколько методов для создания заказов на покупку для проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="4db06-108">Используемый метод зависит от назначения заказа на покупку, времени использования приобретенной номенклатуры и времени, когда счет за приобретенные номенклатуры выставляется проекту.</span><span class="sxs-lookup"><span data-stu-id="4db06-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="4db06-109">Методы для создания заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="4db06-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="4db06-110">Можно использовать следующие методы, чтобы создать заказ на покупку в модуле "Управление и учет по проектам".</span><span class="sxs-lookup"><span data-stu-id="4db06-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="4db06-111">Назначение заказа на покупку определяет срок потребления заказа на покупку и, следовательно, срок выставления накладных по номенклатурам проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4db06-112">Метод</span><span class="sxs-lookup"><span data-stu-id="4db06-112">Method</span></span></th>
<th><span data-ttu-id="4db06-113">Назначение</span><span class="sxs-lookup"><span data-stu-id="4db06-113">Purpose</span></span></th>
<th><span data-ttu-id="4db06-114">Потребление номенклатур</span><span class="sxs-lookup"><span data-stu-id="4db06-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4db06-115">Создание заказа на покупку непосредственно из проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="4db06-116">Этот метод используется для покупки номенклатур у внешнего поставщика для потребления по проекту.</span><span class="sxs-lookup"><span data-stu-id="4db06-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="4db06-117">Заказ на покупку можно создать двумя способами.</span><span class="sxs-lookup"><span data-stu-id="4db06-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="4db06-118">Из самого проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-118">From the project itself.</span></span> <span data-ttu-id="4db06-119">В этом случае проект для заказа на покупку уже определен.</span><span class="sxs-lookup"><span data-stu-id="4db06-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="4db06-120">Перейдя к заказу на покупку проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="4db06-121">Необходимо выбрать как поставщика, так и проект, для которого создается заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="4db06-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="4db06-122">Номенклатуры потребляются при обновлении накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="4db06-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4db06-123">Создайте заказ на покупку из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4db06-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="4db06-124">Используйте этот метод для закупки номенклатур, когда создаете заказ на продажу из проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="4db06-125">Номенклатуры потребляются, когда клиенту выставляется накладная по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="4db06-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4db06-126">Создайте заказ на покупку из потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="4db06-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="4db06-127">Используйте этот метод для закупки номенклатур при создании потребности в номенклатуре из проекта.</span><span class="sxs-lookup"><span data-stu-id="4db06-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="4db06-128">Номенклатуры потребляются при обновлении отборочной накладной потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="4db06-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="4db06-129">При обновлении накладной или отборочной накладной поставщика будет предложено обновить отборочную накладную для потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="4db06-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="4db06-130">Дополнительные сведения см. в разделе [Получение номенклатур в заказе на покупку из потребности в номенклатуре](tasks/receive-items-purchase-order-item-requirement.md)</span><span class="sxs-lookup"><span data-stu-id="4db06-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


