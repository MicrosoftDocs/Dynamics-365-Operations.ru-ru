---
title: Распространенные источники производственных отклонений
description: Эта статья описывает различные стандартные источники каждого типа отклонения цены производства от себестоимости.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50f8cd7904e1d32175edd321fbd6533e985fb324
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "308698"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="3f600-103">Распространенные источники производственных отклонений</span><span class="sxs-lookup"><span data-stu-id="3f600-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f600-104">Эта статья описывает различные стандартные источники каждого типа отклонения цены производства от себестоимости.</span><span class="sxs-lookup"><span data-stu-id="3f600-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="3f600-105">Ниже приведены несколько типичные источники расхождения **размера лота**:</span><span class="sxs-lookup"><span data-stu-id="3f600-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="3f600-106">Верное количество для производственного заказа отличается от рассчитанного количества, которое используется при вычислении стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="3f600-107">Данное количество представляет собой основу для амортизации постоянных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="3f600-108">Величина постоянных затрат в рамках производственного заказа отличается от постоянных затрат, которые использованы при вычислении стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="3f600-109">Постоянные затраты в рамках производственного заказа могут отличаться по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="3f600-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="3f600-110">Например, постоянные затраты могут отражать следующие факторы:</span><span class="sxs-lookup"><span data-stu-id="3f600-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="3f600-111">Изменения, вносимые вручную в спецификации производства или маршрут</span><span class="sxs-lookup"><span data-stu-id="3f600-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="3f600-112">Выбор другой версии спецификации или версии маршрута при создании производственного заказа</span><span class="sxs-lookup"><span data-stu-id="3f600-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="3f600-113">Спланированные изменения разработок в версии спецификации или версии маршрута, назначенной номенклатуре</span><span class="sxs-lookup"><span data-stu-id="3f600-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="3f600-114">Ниже приведены несколько типичные источники расхождения **Производственная цена**:</span><span class="sxs-lookup"><span data-stu-id="3f600-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="3f600-115">Категория затрат (и соответствующая цена категории затрат) для фактически подтвержденного потребления по операции маршрута отличается от категории затрат, которая используется при вычислении стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="3f600-116">Активные затраты для цены категории затрат отличаются от цены категории затрат, которая используется при вычислении стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="3f600-117">Ниже приведены несколько типичные источники расхождения **Производственное количество**:</span><span class="sxs-lookup"><span data-stu-id="3f600-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="3f600-118">Выполняется Перерасход или недорасход материального компонента.</span><span class="sxs-lookup"><span data-stu-id="3f600-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="3f600-119">Сообщается Завышенное время или заниженное время выполнения операции маршрута.</span><span class="sxs-lookup"><span data-stu-id="3f600-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="3f600-120">Вы переполучаете или недополучаете Количество правильных товаров родительской номенклатуры по сравнению с количеством заказа.</span><span class="sxs-lookup"><span data-stu-id="3f600-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="3f600-121">Однако вы выдаете полные операции компонентов и отчетов на основе количества заказа для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="3f600-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="3f600-122">Ниже приведены несколько типичных источников расхождения **производственного замещения**:</span><span class="sxs-lookup"><span data-stu-id="3f600-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="3f600-123">Вы отпускаете материальный компонент, который не входит в спецификацию производства.</span><span class="sxs-lookup"><span data-stu-id="3f600-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="3f600-124">Вы вручную Добавляете компонента в спецификацию производства вручную и его регистрируете как потребленного.</span><span class="sxs-lookup"><span data-stu-id="3f600-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="3f600-125">Вы сообщаете номенклатуру как потребленную без ее добавления вручную в спецификацию производства.</span><span class="sxs-lookup"><span data-stu-id="3f600-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="3f600-126">Вы Добавляете вручную операции в маршрут производства и регистрируете потребление по данной операции.</span><span class="sxs-lookup"><span data-stu-id="3f600-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="3f600-127">При создании производственного заказа, вы выбираете версию спецификации, которая отличается от той, которая используется при вычислении стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="3f600-128">При создании производственного заказа, вы выбираете версию маршрута, которая отличается от той, которая используется при вычислении стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="3f600-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




