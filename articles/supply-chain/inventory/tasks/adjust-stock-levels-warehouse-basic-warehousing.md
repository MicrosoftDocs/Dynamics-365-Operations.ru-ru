---
title: Корректировка уровней запасов на складе (базовая работа со складом)
description: Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c617517109146b96075d03b6f3549639a99d7d1c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146085"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="d3023-103">Корректировка уровней запасов на складе (базовая работа со складом)</span><span class="sxs-lookup"><span data-stu-id="d3023-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3023-104">Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе.</span><span class="sxs-lookup"><span data-stu-id="d3023-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="d3023-105">Необходимо настроить наименование журнала запасов для корректировки запасов перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d3023-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="d3023-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="d3023-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="d3023-107">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="d3023-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="d3023-108">Создание журнала коррекции запасов</span><span class="sxs-lookup"><span data-stu-id="d3023-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="d3023-109">Перейдите "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Корректировка запасов".</span><span class="sxs-lookup"><span data-stu-id="d3023-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="d3023-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d3023-110">Click New.</span></span>
3. <span data-ttu-id="d3023-111">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d3023-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d3023-112">В списке щелкните наименование журнала коррекции запасов, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="d3023-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="d3023-113">Некоторые другие поля будут заполнены на основе настройки выбранного наименования журнала коррекции запасов.</span><span class="sxs-lookup"><span data-stu-id="d3023-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="d3023-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d3023-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="d3023-115">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="d3023-115">Create journal lines</span></span>
1. <span data-ttu-id="d3023-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d3023-116">Click New.</span></span>
2. <span data-ttu-id="d3023-117">Отметьте поле кода номенклатуры в списке.</span><span class="sxs-lookup"><span data-stu-id="d3023-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="d3023-118">В поле "Код номенклатуры" выберите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="d3023-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="d3023-119">При использовании компании с демонстрационными данными USMF введите "D0001".</span><span class="sxs-lookup"><span data-stu-id="d3023-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="d3023-120">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d3023-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d3023-121">Выберите сайт в списке.</span><span class="sxs-lookup"><span data-stu-id="d3023-121">In the list, select a site.</span></span>
6. <span data-ttu-id="d3023-122">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d3023-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d3023-123">Выберите склад в списке.</span><span class="sxs-lookup"><span data-stu-id="d3023-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="d3023-124">Если выбрана номенклатура с местонахождением как обязательная аналитика, здесь необходимо указать местонахождение.</span><span class="sxs-lookup"><span data-stu-id="d3023-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="d3023-125">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="d3023-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d3023-126">В поле себестоимости указывается стоимость на единицу для поступлений на склад.</span><span class="sxs-lookup"><span data-stu-id="d3023-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="d3023-127">Если для кода номенклатуры не указана себестоимость или ее нужно изменить вручную, это делается здесь.</span><span class="sxs-lookup"><span data-stu-id="d3023-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="d3023-128">Проверка и разноска журнала коррекции запасов</span><span class="sxs-lookup"><span data-stu-id="d3023-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="d3023-129">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="d3023-129">Click Validate.</span></span>
2. <span data-ttu-id="d3023-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d3023-130">Click OK.</span></span>
3. <span data-ttu-id="d3023-131">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="d3023-131">Click Post.</span></span>
    * <span data-ttu-id="d3023-132">При разноске этого типа журнала разносится приход на склад или расход со склада, изменяются уровень и величина запаса и создаются проводки ГК.</span><span class="sxs-lookup"><span data-stu-id="d3023-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="d3023-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d3023-133">Click OK.</span></span>
5. <span data-ttu-id="d3023-134">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="d3023-134">Close the form.</span></span>
6. <span data-ttu-id="d3023-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d3023-135">Close the page.</span></span>

