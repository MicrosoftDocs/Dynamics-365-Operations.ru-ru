---
title: Уровень расчета затрат
description: В этом разделе описывается уровень спецификации (BOM), который называется уровнем расчета затрат. Этот уровень спецификации исключает производственные и партионные заказы из их расчетов.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839495"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="76cce-104">Уровень расчета затрат</span><span class="sxs-lookup"><span data-stu-id="76cce-104">Cost calculation level</span></span>

<span data-ttu-id="76cce-105">Уровень спецификации (BOM) с именем **Уровень расчета затрат** исключает производственные заказы и партионные заказы из их расчетов.</span><span class="sxs-lookup"><span data-stu-id="76cce-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="76cce-106">Этот уровень используется системой при выполнении расчетов затрат в версиях учета затрат.</span><span class="sxs-lookup"><span data-stu-id="76cce-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="76cce-107">В процессах, таких как пересчет и закрытие запасов, вместо этого система использует уровень спецификации **Уровень расчета себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="76cce-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="76cce-108">В следующем простом сценарии показаны различия между уровнем спецификации **Уровень расчета затрат** и уровнем спецификации **Уровень расчета себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="76cce-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="76cce-109">Имеется три продукта: A, B и C. Продукт C — это компонент продукта B, а продукт B — компонент продукта A.</span><span class="sxs-lookup"><span data-stu-id="76cce-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="76cce-110">**Уровень расчета себестоимости** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="76cce-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="76cce-111">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="76cce-111">**Product A:** 0</span></span>
    - <span data-ttu-id="76cce-112">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="76cce-112">**Product B:** 1</span></span>
    - <span data-ttu-id="76cce-113">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="76cce-113">**Product C:** 2</span></span>

- <span data-ttu-id="76cce-114">**Уровень расчета затрат** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="76cce-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="76cce-115">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="76cce-115">**Product A:** 0</span></span>
    - <span data-ttu-id="76cce-116">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="76cce-116">**Product B:** 1</span></span>
    - <span data-ttu-id="76cce-117">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="76cce-117">**Product C:** 2</span></span>

<span data-ttu-id="76cce-118">Затем создается производственный заказ для продукта C, а продукт А добавляется в спецификацию производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="76cce-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="76cce-119">После оценки заказа уровни спецификации обновляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="76cce-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="76cce-120">**Уровень расчета себестоимости** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="76cce-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="76cce-121">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="76cce-121">**Product B:** 1</span></span>
    - <span data-ttu-id="76cce-122">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="76cce-122">**Product C:** 2</span></span>
    - <span data-ttu-id="76cce-123">**Продукт A:** 3</span><span class="sxs-lookup"><span data-stu-id="76cce-123">**Product A:** 3</span></span>

- <span data-ttu-id="76cce-124">**Уровень расчета затрат** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="76cce-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="76cce-125">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="76cce-125">**Product A:** 0</span></span>
    - <span data-ttu-id="76cce-126">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="76cce-126">**Product B:** 1</span></span>
    - <span data-ttu-id="76cce-127">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="76cce-127">**Product C:** 2</span></span>

<span data-ttu-id="76cce-128">Такое поведение гарантирует, что изменения спецификаций производственного заказа не повлияют на последующие расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="76cce-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]