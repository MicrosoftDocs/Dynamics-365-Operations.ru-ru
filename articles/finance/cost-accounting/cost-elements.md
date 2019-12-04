---
title: Аналитики элемента затрат
description: В качестве одного из ключевых столпов в модуле учета затрат, аналитики элементов затрат используются для классификации и отслеживания направления потока затрат.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 44d404aaafd124a5d5a9d92cac8add51f1ee846a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771992"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="21345-103">Аналитики элемента затрат</span><span class="sxs-lookup"><span data-stu-id="21345-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21345-104">В качестве одного из ключевых столпов в модуле учета затрат, аналитики элементов затрат используются для классификации и отслеживания направления потока затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="21345-105">Элемент затрат соответствует связанному с затратами элементу в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="21345-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="21345-106">По существу, это может быть элемент любого типа на самом низком уровне в компании, в который направлен поток затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="21345-107">Понятие элементов затрат покрывает диапазон от счетов ГК до всех ресурсов, связанных с затратами.</span><span class="sxs-lookup"><span data-stu-id="21345-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="21345-108">В данный момент учет затрат поддерживает счета ГК.</span><span class="sxs-lookup"><span data-stu-id="21345-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="21345-109">Два типа элементов затрат</span><span class="sxs-lookup"><span data-stu-id="21345-109">Two types of cost elements</span></span>
<span data-ttu-id="21345-110">Имеется два типа элементов затрат: элементы первичных затрат и элементы вторичных затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="21345-111">Следующая таблица содержит описание различия между двумя типами.</span><span class="sxs-lookup"><span data-stu-id="21345-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21345-112"><strong>Элементы первичных затрат</strong></span><span class="sxs-lookup"><span data-stu-id="21345-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="21345-113"><strong>Элементы вторичных затрат</strong></span><span class="sxs-lookup"><span data-stu-id="21345-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21345-114">Элементы первичных затрат представляют поток затрат из финансового учета в учет затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="21345-115">Структура элемента затрат соответствует структуре счета прибылей и убытков в ГК, где элемент затрат может соответствовать счету ГК.</span><span class="sxs-lookup"><span data-stu-id="21345-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="21345-116">Не все счета ГК могут обязательно представляться в виде элементов затрат, в зависимости от требований компании.</span><span class="sxs-lookup"><span data-stu-id="21345-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="21345-117">Примеры элементов первичных затрат включают:</span><span class="sxs-lookup"><span data-stu-id="21345-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="21345-118">Затраты на проданные товары (COG)</span><span class="sxs-lookup"><span data-stu-id="21345-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="21345-119">Косвенные затраты на материалы</span><span class="sxs-lookup"><span data-stu-id="21345-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="21345-120">Затраты на персонал</span><span class="sxs-lookup"><span data-stu-id="21345-120">Personnel costs</span></span></li>
<li><span data-ttu-id="21345-121">Затраты на энергию</span><span class="sxs-lookup"><span data-stu-id="21345-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="21345-122">Элементы вторичных затрат представляют внутренний поток затрат, поскольку эти затраты создаются и используются только в модуле учета затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="21345-123">Они используются, чтобы обеспечить возможность отслеживания источника затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="21345-124">Эти элементы затрат используются в распределениях затрат и расчетах накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="21345-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="21345-125">Примеры элементов вторичных затрат включают:</span><span class="sxs-lookup"><span data-stu-id="21345-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="21345-126">Производственные затраты</span><span class="sxs-lookup"><span data-stu-id="21345-126">Production costs</span></span></li>
<li><span data-ttu-id="21345-127">Накладные расходы на производство, материалы и маркетинг</span><span class="sxs-lookup"><span data-stu-id="21345-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="21345-128">Аналитики элементов затрат и членов аналитик элементов затрат</span><span class="sxs-lookup"><span data-stu-id="21345-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="21345-129">Элементы затрат называются *аналитиками элемента затрат*.</span><span class="sxs-lookup"><span data-stu-id="21345-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="21345-130">Отдельные значения аналитики называются *членами аналитики элемента затрат*.</span><span class="sxs-lookup"><span data-stu-id="21345-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="21345-131">Например, вы имеете структуру плана счетов США (COA), которая служит основой для вашей предписанной законом отчетности.</span><span class="sxs-lookup"><span data-stu-id="21345-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="21345-132">Этот план счетов COA используется как аналитика элемента затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="21345-133">Счета, которые являются элементами первичных затрат, представлены как члены аналитики элемента затрат в модуле учета затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="21345-134">Следующий снимок экрана показывает пример счетов ГК как аналитики элемента затрат со своими фактическими счетами ГК в качестве членов аналитики элемента затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="21345-135">[![Снимок экрана счетов ГК как аналитики элемента затрат](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="21345-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="21345-136">Импорт членов аналитика элемента затрат через соединители данных</span><span class="sxs-lookup"><span data-stu-id="21345-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="21345-137">Чтобы упростить настройку членов аналитики элемента затрат в модуле учета затрат, можно использовать соединители данных, которые предварительно подготовлены или специально собраны, чтобы восстановить извлечь элементы первичных затрат из одной или нескольких исходных систем.</span><span class="sxs-lookup"><span data-stu-id="21345-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="21345-138">Вопросы реализации</span><span class="sxs-lookup"><span data-stu-id="21345-138">Implementation considerations</span></span>
<span data-ttu-id="21345-139">Так как элементы затрат представляют самый низший уровень сведений о затратах, необходимо убедиться, что все элементы затрат, необходимые для подготовки распорядительской отчетности, включены при реализации структуры элементов затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="21345-140">Это может быть проблемой, найти требуемое число подходящих элементов издержек для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="21345-141">Если имеются тысячи элементов затрат, может быть трудно контролировать каждый элемент затрат.</span><span class="sxs-lookup"><span data-stu-id="21345-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="21345-142">В качестве альтернативы можно группировать элементы затрат и управлять затратами на суммированном уровне.</span><span class="sxs-lookup"><span data-stu-id="21345-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>



