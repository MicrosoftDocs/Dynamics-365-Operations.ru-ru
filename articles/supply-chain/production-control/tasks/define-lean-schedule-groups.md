---
title: Определение групп графиков бережливого производства
description: Группы графиков бережливого производства определены для группировки и различения продуктов в планировании канбана.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54151e8afd1b6e0606d17b044f545314f7012079
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212074"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="5e49e-103">Определение групп графиков бережливого производства</span><span class="sxs-lookup"><span data-stu-id="5e49e-103">Define lean schedule groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e49e-104">Группы графиков бережливого производства определены для группировки и различения продуктов в планировании канбана.</span><span class="sxs-lookup"><span data-stu-id="5e49e-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="5e49e-105">Группирование может выполнить как универсальную связь на компанию или конкретно для производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="5e49e-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="5e49e-106">Каждая группа имеет цветовой код, назначенный для визуальной индикации на странице планирования канбана.</span><span class="sxs-lookup"><span data-stu-id="5e49e-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="5e49e-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5e49e-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="5e49e-108">Определение группы планирования бережливого производства</span><span class="sxs-lookup"><span data-stu-id="5e49e-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="5e49e-109">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Группы графиков бережливого производства".</span><span class="sxs-lookup"><span data-stu-id="5e49e-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="5e49e-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5e49e-110">Click New.</span></span>
3. <span data-ttu-id="5e49e-111">В поле "Группа планирования" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5e49e-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="5e49e-112">Группу планирования можно определить как глобальную группу или конкретную группу для производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="5e49e-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="5e49e-113">В этом примере определим глобальную группу, и производственная ячейка останется пустой.</span><span class="sxs-lookup"><span data-stu-id="5e49e-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="5e49e-114">Настройки этой группы применяются ко всем производственным ячейкам, которые не имеют определенных групп планирования.</span><span class="sxs-lookup"><span data-stu-id="5e49e-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="5e49e-115">Выберите цвет в списке цветов.</span><span class="sxs-lookup"><span data-stu-id="5e49e-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="5e49e-116">Цвета используются, чтобы выделить задания на странице списка планирования канбана или на панели процессов канбана.</span><span class="sxs-lookup"><span data-stu-id="5e49e-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="5e49e-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5e49e-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="5e49e-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5e49e-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="5e49e-119">Связь продукта</span><span class="sxs-lookup"><span data-stu-id="5e49e-119">Associate product</span></span>
1. <span data-ttu-id="5e49e-120">Связывание конкретного продукта</span><span class="sxs-lookup"><span data-stu-id="5e49e-120">Associate a specific product</span></span>
    * <span data-ttu-id="5e49e-121">Существует два способа связи продуктов с группами графиков бережливого производства: как конкретный продукт (тип связи номенклатуры = номенклатура) или как часть ключа распределения номенклатуры (тип связи номенклатуры = группа).</span><span class="sxs-lookup"><span data-stu-id="5e49e-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="5e49e-122">В поле "Тип связи номенклатуры" выберите "Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="5e49e-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="5e49e-123">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5e49e-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="5e49e-124">В поле "Коэффициент пропускной способности" введите число.</span><span class="sxs-lookup"><span data-stu-id="5e49e-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="5e49e-125">Коэффициент пропускной способности по умолчанию равняется 1, это означает, что связанные продукты потребляют точно такую мощность, какая указана в мероприятиях производственных потоков.</span><span class="sxs-lookup"><span data-stu-id="5e49e-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="5e49e-126">Коэффициент пропускной способности > 1 определяет более высокое потребление ресурсов, коэффициент пропускной способности < 1 определяет более низкое потребление ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e49e-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="5e49e-127">Коэффициент используется при вычислении затрат и в расчете потребления для задания канбана.</span><span class="sxs-lookup"><span data-stu-id="5e49e-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="5e49e-128">Связь ключа распределения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="5e49e-128">Associate item allocation key</span></span>
1. <span data-ttu-id="5e49e-129">Связь ключа распределения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="5e49e-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="5e49e-130">Добавьте связь с ключом распределения номенклатуры с помощью типа связи номенклатуры "группа".</span><span class="sxs-lookup"><span data-stu-id="5e49e-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="5e49e-131">Обратите внимание, что для этого процесса необходимо в данных определить ключ распределения номенклатуры прогноза.</span><span class="sxs-lookup"><span data-stu-id="5e49e-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="5e49e-132">В поле "Тип связи номенклатуры" выберите "Группа".</span><span class="sxs-lookup"><span data-stu-id="5e49e-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="5e49e-133">В поле "Ключ распределения номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="5e49e-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5e49e-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5e49e-134">In the list, click the link in the selected row.</span></span>

