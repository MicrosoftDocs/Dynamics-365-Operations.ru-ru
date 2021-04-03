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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251034"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="169e4-104">Уровень расчета затрат</span><span class="sxs-lookup"><span data-stu-id="169e4-104">Cost calculation level</span></span>

<span data-ttu-id="169e4-105">Уровень спецификации (BOM) с именем **Уровень расчета затрат** исключает производственные заказы и партионные заказы из их расчетов.</span><span class="sxs-lookup"><span data-stu-id="169e4-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="169e4-106">Этот уровень используется системой при выполнении расчетов затрат в версиях учета затрат.</span><span class="sxs-lookup"><span data-stu-id="169e4-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="169e4-107">В процессах, таких как пересчет и закрытие запасов, вместо этого система использует уровень спецификации **Уровень расчета себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="169e4-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="169e4-108">В следующем простом сценарии показаны различия между уровнем спецификации **Уровень расчета затрат** и уровнем спецификации **Уровень расчета себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="169e4-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="169e4-109">Имеется три продукта: A, B и C. Продукт C — это компонент продукта B, а продукт B — компонент продукта A.</span><span class="sxs-lookup"><span data-stu-id="169e4-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="169e4-110">**Уровень расчета себестоимости** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="169e4-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="169e4-111">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="169e4-111">**Product A:** 0</span></span>
    - <span data-ttu-id="169e4-112">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="169e4-112">**Product B:** 1</span></span>
    - <span data-ttu-id="169e4-113">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="169e4-113">**Product C:** 2</span></span>

- <span data-ttu-id="169e4-114">**Уровень расчета затрат** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="169e4-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="169e4-115">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="169e4-115">**Product A:** 0</span></span>
    - <span data-ttu-id="169e4-116">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="169e4-116">**Product B:** 1</span></span>
    - <span data-ttu-id="169e4-117">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="169e4-117">**Product C:** 2</span></span>

<span data-ttu-id="169e4-118">Затем создается производственный заказ для продукта C, а продукт А добавляется в спецификацию производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="169e4-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="169e4-119">После оценки заказа уровни спецификации обновляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="169e4-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="169e4-120">**Уровень расчета себестоимости** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="169e4-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="169e4-121">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="169e4-121">**Product B:** 1</span></span>
    - <span data-ttu-id="169e4-122">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="169e4-122">**Product C:** 2</span></span>
    - <span data-ttu-id="169e4-123">**Продукт A:** 3</span><span class="sxs-lookup"><span data-stu-id="169e4-123">**Product A:** 3</span></span>

- <span data-ttu-id="169e4-124">**Уровень расчета затрат** назначает следующие уровни спецификации:</span><span class="sxs-lookup"><span data-stu-id="169e4-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="169e4-125">**Продукт A:** 0</span><span class="sxs-lookup"><span data-stu-id="169e4-125">**Product A:** 0</span></span>
    - <span data-ttu-id="169e4-126">**Продукт B:** 1</span><span class="sxs-lookup"><span data-stu-id="169e4-126">**Product B:** 1</span></span>
    - <span data-ttu-id="169e4-127">**Продукт C:** 2</span><span class="sxs-lookup"><span data-stu-id="169e4-127">**Product C:** 2</span></span>

<span data-ttu-id="169e4-128">Такое поведение гарантирует, что изменения спецификаций производственного заказа не повлияют на последующие расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="169e4-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]