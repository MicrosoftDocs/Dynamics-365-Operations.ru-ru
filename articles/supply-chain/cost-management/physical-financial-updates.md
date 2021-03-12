---
title: Физические и финансовые обновления
description: В этом разделе содержится обзор того, какие типы проводок увеличивают, а какие уменьшают количество запасов.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b29c1c0727487992a478552d94b5bbe8684d0550
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967466"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="22ffa-103">Физические и финансовые обновления</span><span class="sxs-lookup"><span data-stu-id="22ffa-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22ffa-104">В этом разделе содержится обзор того, какие типы проводок увеличивают, а какие уменьшают количество запасов.</span><span class="sxs-lookup"><span data-stu-id="22ffa-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="22ffa-105">Проводки по запасам можно физически обновить и финансово обновить в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="22ffa-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="22ffa-106">Некоторые типы физических и финансовых проводок увеличивают количество запасов, тогда как другие уменьшают количество.</span><span class="sxs-lookup"><span data-stu-id="22ffa-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="22ffa-107">Физический прирост</span><span class="sxs-lookup"><span data-stu-id="22ffa-107">Physical increases</span></span>
<span data-ttu-id="22ffa-108">При разноске физической проводки запись проводки имеет статус **Получено**.</span><span class="sxs-lookup"><span data-stu-id="22ffa-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="22ffa-109">Следующие проводки рассматриваются как физический прирост:</span><span class="sxs-lookup"><span data-stu-id="22ffa-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="22ffa-110">Приход по заказу на покупку</span><span class="sxs-lookup"><span data-stu-id="22ffa-110">Purchase order receipt</span></span>
-   <span data-ttu-id="22ffa-111">Возврат по отборочной накладной заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="22ffa-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="22ffa-112">Сообщение о завершении производственного заказа</span><span class="sxs-lookup"><span data-stu-id="22ffa-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="22ffa-113">Побочный продукт по отгрузочной накладной производственного заказа</span><span class="sxs-lookup"><span data-stu-id="22ffa-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="22ffa-114">Финансовый прирост</span><span class="sxs-lookup"><span data-stu-id="22ffa-114">Financial increases</span></span>
<span data-ttu-id="22ffa-115">При разноске проводки финансового прихода запись проводки, увеличивающей количество, имеет статус **Приобретено**.</span><span class="sxs-lookup"><span data-stu-id="22ffa-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="22ffa-116">Следующие проводки рассматриваются как финансовый прирост:</span><span class="sxs-lookup"><span data-stu-id="22ffa-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="22ffa-117">Накладная поставщика</span><span class="sxs-lookup"><span data-stu-id="22ffa-117">Vendor invoice</span></span>
-   <span data-ttu-id="22ffa-118">Накладная на возврат по заказу на продажу</span><span class="sxs-lookup"><span data-stu-id="22ffa-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="22ffa-119">Калькуляция затрат по производственному заказу</span><span class="sxs-lookup"><span data-stu-id="22ffa-119">Production order costing</span></span>
-   <span data-ttu-id="22ffa-120">Журналы положительного количества запасов, такие как журналы перемещения, прибылей и убытков, инвентаризации, спецификаций и переноса</span><span class="sxs-lookup"><span data-stu-id="22ffa-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="22ffa-121">Проводки, увеличивающие количество</span><span class="sxs-lookup"><span data-stu-id="22ffa-121">Transactions that increase quantity</span></span>
<span data-ttu-id="22ffa-122">Проводки, увеличивающие количество, разносятся с использованием скользящей средней себестоимости.</span><span class="sxs-lookup"><span data-stu-id="22ffa-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="22ffa-123">Расчетная скользящая средняя себестоимость номенклатуры основана на стоимости каждой из этих проводок для каждой складской аналитики, в отношении которых осуществляется финансовый контроль.</span><span class="sxs-lookup"><span data-stu-id="22ffa-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="22ffa-124">Информацию о значениях скользящей средней себестоимости см. [Скользящая средняя себестоимость](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="22ffa-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="22ffa-125">Проводки, уменьшающие количество</span><span class="sxs-lookup"><span data-stu-id="22ffa-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="22ffa-126">Расчетная вычисленная скользящая себестоимость используется при разноске проводки, уменьшающей количество, независимо от того, какая складская модель связана с данным запасом.</span><span class="sxs-lookup"><span data-stu-id="22ffa-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="22ffa-127">Проводка, которая уменьшает количество, не должна быть ранее помечена для другой проводки перед разноской.</span><span class="sxs-lookup"><span data-stu-id="22ffa-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="22ffa-128">Если физические запасы в наличии становятся отрицательными, используется стоимость запасов, которая определена для номенклатуры на странице **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="22ffa-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="22ffa-129">Если включена возможность работать с несколькими сайтами, эта стоимость будет стоимостью запасов, которая определена для сайта на странице **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="22ffa-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="22ffa-130">Физические и финансовые расходы</span><span class="sxs-lookup"><span data-stu-id="22ffa-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="22ffa-131">При разноске проводки физического расхода запись проводки имеет статус **Списано**.</span><span class="sxs-lookup"><span data-stu-id="22ffa-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="22ffa-132">Следующие проводки рассматриваются как физический расход:</span><span class="sxs-lookup"><span data-stu-id="22ffa-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="22ffa-133">Журнал отгрузочных накладных по производственному заказу</span><span class="sxs-lookup"><span data-stu-id="22ffa-133">Production order picking list journal</span></span>
-   <span data-ttu-id="22ffa-134">Отборочная накладная по заказу на продажу</span><span class="sxs-lookup"><span data-stu-id="22ffa-134">Sales order packing slip</span></span>
-   <span data-ttu-id="22ffa-135">Возврат по отборочной накладной заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="22ffa-135">Purchase order packing slip return</span></span>

<span data-ttu-id="22ffa-136">При разноске финансовой проводки запись проводки имеет статус **Продано**.</span><span class="sxs-lookup"><span data-stu-id="22ffa-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="22ffa-137">Следующие проводки рассматриваются как финансовый расход:</span><span class="sxs-lookup"><span data-stu-id="22ffa-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="22ffa-138">Завершение производственного заказа</span><span class="sxs-lookup"><span data-stu-id="22ffa-138">Ending a production order</span></span>
-   <span data-ttu-id="22ffa-139">Накладная по заказу на продажу</span><span class="sxs-lookup"><span data-stu-id="22ffa-139">Sales order invoice</span></span>
-   <span data-ttu-id="22ffa-140">Возврат по накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="22ffa-140">Vendor invoice return</span></span>
-   <span data-ttu-id="22ffa-141">Журналы отрицательного количества запасов, такие как журналы перемещения, прибылей и убытков, инвентаризации, спецификаций и переноса</span><span class="sxs-lookup"><span data-stu-id="22ffa-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="22ffa-142">Проводки, уменьшающие количество, разносятся с использованием скользящей средней себестоимости.</span><span class="sxs-lookup"><span data-stu-id="22ffa-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="22ffa-143">Таким образом, требуется процедура закрытия запасов для сопоставления проводок расхода с проводками прихода на основе складской модели, назначенной каждой номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="22ffa-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>
