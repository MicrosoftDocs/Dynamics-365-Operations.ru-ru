---
title: Расчет спецификации с помощью одноуровневой структуры (февраль 2016 г.)
description: В этой процедуре показано, как рассчитать затраты на готовую продукцию с помощью одноуровневого развертывания, основанного на схеме калькуляции.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f74f8e4efc4474693f0a5b543c1300c3b64ecda0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "361598"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="1bc08-103">Расчет спецификации с помощью одноуровневой структуры (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="1bc08-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bc08-104">В этой процедуре показано, как рассчитать затраты на готовую продукцию с помощью одноуровневого развертывания, основанного на схеме калькуляции.</span><span class="sxs-lookup"><span data-stu-id="1bc08-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="1bc08-105">Это шестая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="1bc08-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="1bc08-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="1bc08-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="1bc08-107">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="1bc08-107">Go to Released products.</span></span>
2. <span data-ttu-id="1bc08-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1bc08-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1bc08-109">Выберите продукт BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1bc08-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="1bc08-110">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="1bc08-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="1bc08-111">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="1bc08-111">Click Item price.</span></span>
5. <span data-ttu-id="1bc08-112">Щелкните "Расчет себестоимости номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="1bc08-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="1bc08-113">Может потребоваться нажать кнопку с многоточием (...), чтобы увидеть этот параметр в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="1bc08-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="1bc08-114">В поле "Версия стоимости" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="1bc08-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1bc08-115">В этом примере выберите "10".</span><span class="sxs-lookup"><span data-stu-id="1bc08-115">For this demo, select 10.</span></span> <span data-ttu-id="1bc08-116">Это та же версия учета затрат, которая использовалась для добавления себестоимости в компоненты.</span><span class="sxs-lookup"><span data-stu-id="1bc08-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="1bc08-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1bc08-117">Click OK.</span></span>
8. <span data-ttu-id="1bc08-118">Щелкните "Просмотреть сведения расчета".</span><span class="sxs-lookup"><span data-stu-id="1bc08-118">Click View calculation details.</span></span>
    * <span data-ttu-id="1bc08-119">Может потребоваться нажать кнопку с многоточием (...), чтобы увидеть этот параметр в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="1bc08-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="1bc08-120">Вот состав стоимости::  •   10 является производным значением от ITEM_A, 10 — от ITEM_B, 10 — от BOM_2.</span><span class="sxs-lookup"><span data-stu-id="1bc08-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="1bc08-121">В этом случае нет сведений для BOM_2, так как она была введена как стандартная себестоимость 10, но не была получена с помощью расчета.</span><span class="sxs-lookup"><span data-stu-id="1bc08-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="1bc08-122">•  7 является производным значением от времени настройки, которое является постоянными затратами, а дополнительные 7 получены в результате операции времени выполнения (процесс).</span><span class="sxs-lookup"><span data-stu-id="1bc08-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="1bc08-123">•   Существуют также другие суммы, которые образуют косвенные затраты.</span><span class="sxs-lookup"><span data-stu-id="1bc08-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="1bc08-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="1bc08-124">@SysTaskRecorder:_RequestClose</span></span>

