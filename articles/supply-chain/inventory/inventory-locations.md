---
title: Места хранения
description: Места хранения используются с базовым управлением складом (WMS I), чтобы определить, где хранятся номенклатуры и где комплектуются номенклатуры внутри склада WMS I.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ba83113b03ef122090da0c356c85b3f1b6f62c7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978021"
---
# <a name="inventory-locations"></a><span data-ttu-id="6e09b-103">Места хранения</span><span class="sxs-lookup"><span data-stu-id="6e09b-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e09b-104">Места хранения используются с базовым управлением складом (WMS I), чтобы определить, где хранятся номенклатуры и где комплектуются номенклатуры внутри склада WMS I.</span><span class="sxs-lookup"><span data-stu-id="6e09b-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="6e09b-105">Этот раздел относится к функциям в модуле "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="6e09b-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="6e09b-106">Он не применяется к функциям в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="6e09b-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="6e09b-107">Термин местонахождение определяется как то место, в котором хранятся и откуда извлекаются номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6e09b-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="6e09b-108">Для каждой ячейки может быть также указано то место, куда помещается номенклатура.</span><span class="sxs-lookup"><span data-stu-id="6e09b-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="6e09b-109">По умолчанию это одно и то же место.</span><span class="sxs-lookup"><span data-stu-id="6e09b-109">By default, they are the same.</span></span> <span data-ttu-id="6e09b-110">Номенклатуры обычно, но не всегда, вставляются и извлекаются с одной и той же стороны ячейки.</span><span class="sxs-lookup"><span data-stu-id="6e09b-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="6e09b-111">Например, номенклатуры, хранящиеся на стеллажах склада текущего расхода, помещаются туда из одного прохода, а извлекаются из другого прохода.</span><span class="sxs-lookup"><span data-stu-id="6e09b-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="6e09b-112">Основной вход задается именем ячейки, которое обычно определяется ее координатами: склад, проход, стеллаж, полка и позиция.</span><span class="sxs-lookup"><span data-stu-id="6e09b-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="6e09b-113">Это наименование или код могут быть введены вручную или сформированы с использованием координат местоположения, например, 01-02-03-4 для прохода 1, стеллажа 2, полки 3, позиции 4 на странице "Места хранения".</span><span class="sxs-lookup"><span data-stu-id="6e09b-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="6e09b-114">Свойства местоположения</span><span class="sxs-lookup"><span data-stu-id="6e09b-114">Location properties</span></span>

<span data-ttu-id="6e09b-115">Для местоположения имеются следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="6e09b-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="6e09b-116">Размер (высота, ширина, глубина и, таким образом, объем)</span><span class="sxs-lookup"><span data-stu-id="6e09b-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="6e09b-117">Склад, проход, стеллаж, полка и ячейка</span><span class="sxs-lookup"><span data-stu-id="6e09b-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="6e09b-118">Тип местонахождения (буферная ячейка, ячейка комплектации, зона приемки, зона отгрузки, местонахождение поступлений на производство, местонахождение проверки или супермаркет канбана)</span><span class="sxs-lookup"><span data-stu-id="6e09b-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="6e09b-119">В интерактивной системе может использоваться проверочный текст, чтобы убедиться, что оператор выбрал правильную ячейку для определенной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6e09b-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="6e09b-120">Этот проверочный текст может быть создан вручную или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6e09b-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="6e09b-121">Коды сортировки</span><span class="sxs-lookup"><span data-stu-id="6e09b-121">Sort codes</span></span>
<span data-ttu-id="6e09b-122">Коды сортировки используются для оптимизации обработки строк комплектации, которые детализируют информацию, требуемую для комплектации номенклатур со склада, включая порядок комплектации.</span><span class="sxs-lookup"><span data-stu-id="6e09b-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="6e09b-123">Коды сортировки могут быть определены проходом и другими координатами или назначаться ячейке вручную.</span><span class="sxs-lookup"><span data-stu-id="6e09b-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="6e09b-124">Блокированные ячейки</span><span class="sxs-lookup"><span data-stu-id="6e09b-124">Blocked locations</span></span>
<span data-ttu-id="6e09b-125">Иногда может потребоваться указать, что местонахождение заблокировано на определенное время, например для проведения ремонта.</span><span class="sxs-lookup"><span data-stu-id="6e09b-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="6e09b-126">Кроме того, может потребоваться указать блокировку только на вход или только на выход.</span><span class="sxs-lookup"><span data-stu-id="6e09b-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="6e09b-127">Структура в виде дерева</span><span class="sxs-lookup"><span data-stu-id="6e09b-127">Tree structure</span></span>

<span data-ttu-id="6e09b-128">На странице "Места хранения" вы можете просмотреть план склада в древовидной структуре, основанной на координатах мест хранения в определенном формате отображения.</span><span class="sxs-lookup"><span data-stu-id="6e09b-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="6e09b-129">Поддержка мест хранения через форму склада</span><span class="sxs-lookup"><span data-stu-id="6e09b-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="6e09b-130">Можно копировать местонахождения из одного склада в другой и создавать местонахождения с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="6e09b-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="6e09b-131">Перед запуском мастера вы должны убедиться, что вы определили имена местонахождения по умолчанию на странице "Склад".</span><span class="sxs-lookup"><span data-stu-id="6e09b-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="6e09b-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6e09b-132">Additional resources</span></span>
--------

[<span data-ttu-id="6e09b-133">Создание нового макета склада</span><span class="sxs-lookup"><span data-stu-id="6e09b-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)
