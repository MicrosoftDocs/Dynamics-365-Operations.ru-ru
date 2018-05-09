---
title: "Корректировка уровней запасов на складе (базовая работа со складом)"
description: "Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 890d501bf8b111ccd0698372f9df1dd63c2039a0
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="aefa3-103">Корректировка уровней запасов на складе (базовая работа со складом)</span><span class="sxs-lookup"><span data-stu-id="aefa3-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aefa3-104">Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе.</span><span class="sxs-lookup"><span data-stu-id="aefa3-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="aefa3-105">Необходимо настроить наименование журнала запасов для корректировки запасов перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="aefa3-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="aefa3-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="aefa3-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="aefa3-107">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="aefa3-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="aefa3-108">Создание журнала коррекции запасов</span><span class="sxs-lookup"><span data-stu-id="aefa3-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="aefa3-109">Перейдите "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Корректировка запасов".</span><span class="sxs-lookup"><span data-stu-id="aefa3-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="aefa3-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="aefa3-110">Click New.</span></span>
3. <span data-ttu-id="aefa3-111">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aefa3-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aefa3-112">В списке щелкните наименование журнала коррекции запасов, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="aefa3-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="aefa3-113">Некоторые другие поля будут заполнены на основе настройки выбранного наименования журнала коррекции запасов.</span><span class="sxs-lookup"><span data-stu-id="aefa3-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="aefa3-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aefa3-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="aefa3-115">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="aefa3-115">Create journal lines</span></span>
1. <span data-ttu-id="aefa3-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="aefa3-116">Click New.</span></span>
2. <span data-ttu-id="aefa3-117">Отметьте поле кода номенклатуры в списке.</span><span class="sxs-lookup"><span data-stu-id="aefa3-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="aefa3-118">В поле "Код номенклатуры" выберите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="aefa3-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="aefa3-119">При использовании компании с демонстрационными данными USMF введите "D0001".</span><span class="sxs-lookup"><span data-stu-id="aefa3-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="aefa3-120">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aefa3-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="aefa3-121">Выберите сайт в списке.</span><span class="sxs-lookup"><span data-stu-id="aefa3-121">In the list, select a site.</span></span>
6. <span data-ttu-id="aefa3-122">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aefa3-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aefa3-123">Выберите склад в списке.</span><span class="sxs-lookup"><span data-stu-id="aefa3-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="aefa3-124">Если выбрана номенклатура с местонахождением как обязательная аналитика, здесь необходимо указать местонахождение.</span><span class="sxs-lookup"><span data-stu-id="aefa3-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="aefa3-125">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="aefa3-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="aefa3-126">В поле себестоимости указывается стоимость на единицу для поступлений на склад.</span><span class="sxs-lookup"><span data-stu-id="aefa3-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="aefa3-127">Если для кода номенклатуры не указана себестоимость или ее нужно изменить вручную, это делается здесь.</span><span class="sxs-lookup"><span data-stu-id="aefa3-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="aefa3-128">Проверка и разноска журнала коррекции запасов</span><span class="sxs-lookup"><span data-stu-id="aefa3-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="aefa3-129">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="aefa3-129">Click Validate.</span></span>
2. <span data-ttu-id="aefa3-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aefa3-130">Click OK.</span></span>
3. <span data-ttu-id="aefa3-131">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="aefa3-131">Click Post.</span></span>
    * <span data-ttu-id="aefa3-132">При разноске этого типа журнала разносится приход на склад или расход со склада, изменяются уровень и величина запаса и создаются проводки ГК.</span><span class="sxs-lookup"><span data-stu-id="aefa3-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="aefa3-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aefa3-133">Click OK.</span></span>
5. <span data-ttu-id="aefa3-134">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="aefa3-134">Close the form.</span></span>
6. <span data-ttu-id="aefa3-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="aefa3-135">Close the page.</span></span>

