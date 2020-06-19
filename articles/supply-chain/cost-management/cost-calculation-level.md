---
title: Уровень расчета затрат
description: В этом разделе описывается уровень спецификации (BOM), который называется уровнем расчета затрат. Этот уровень спецификации исключает производственные и партионные заказы из их расчетов.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410978"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="6bec9-104">Уровень расчета затрат</span><span class="sxs-lookup"><span data-stu-id="6bec9-104">Cost calculation level</span></span>

<span data-ttu-id="6bec9-105">Уровень спецификации (BOM) с именем **Уровень расчета затрат** исключает производственные заказы и партионные заказы из их расчетов.</span><span class="sxs-lookup"><span data-stu-id="6bec9-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="6bec9-106">Этот уровень используется системой при выполнении расчетов затрат в версиях учета затрат.</span><span class="sxs-lookup"><span data-stu-id="6bec9-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="6bec9-107">В процессах, таких как пересчет и закрытие запасов, вместо этого система использует уровень спецификации **Уровень расчета себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="6bec9-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="6bec9-108">В следующем простом сценарии показаны различия между уровнем спецификации **Уровень расчета затрат** и уровнем спецификации **Уровень расчета себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="6bec9-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="6bec9-109">Имеется три продукта: A, B и C. Продукт C — это компонент продукта B, а продукт B — компонент продукта A.</span><span class="sxs-lookup"><span data-stu-id="6bec9-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="6bec9-110">**Уровень расчета себестоимости** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="6bec9-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6bec9-111">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="6bec9-111">**Product A:** 0</span></span>
    - <span data-ttu-id="6bec9-112">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="6bec9-112">**Product B:** 1</span></span>
    - <span data-ttu-id="6bec9-113">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="6bec9-113">**Product C:** 2</span></span>

- <span data-ttu-id="6bec9-114">**Уровень расчета затрат** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="6bec9-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6bec9-115">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="6bec9-115">**Product A:** 0</span></span>
    - <span data-ttu-id="6bec9-116">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="6bec9-116">**Product B:** 1</span></span>
    - <span data-ttu-id="6bec9-117">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="6bec9-117">**Product C:** 2</span></span>

<span data-ttu-id="6bec9-118">Затем создается производственный заказ для продукта C, а продукт А добавляется в спецификацию производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="6bec9-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="6bec9-119">После оценки заказа уровни спецификации обновляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6bec9-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="6bec9-120">**Уровень расчета себестоимости** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="6bec9-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6bec9-121">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="6bec9-121">**Product B:** 1</span></span>
    - <span data-ttu-id="6bec9-122">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="6bec9-122">**Product C:** 2</span></span>
    - <span data-ttu-id="6bec9-123">**Продукт A:** 3</span><span class="sxs-lookup"><span data-stu-id="6bec9-123">**Product A:** 3</span></span>

- <span data-ttu-id="6bec9-124">**Уровень расчета затрат** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="6bec9-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6bec9-125">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="6bec9-125">**Product A:** 0</span></span>
    - <span data-ttu-id="6bec9-126">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="6bec9-126">**Product B:** 1</span></span>
    - <span data-ttu-id="6bec9-127">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="6bec9-127">**Product C:** 2</span></span>

<span data-ttu-id="6bec9-128">Такое поведение гарантирует, что изменения спецификаций производственного заказа не повлияют на последующие расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="6bec9-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
