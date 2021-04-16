---
title: Корректировка уровней запасов на складе (базовая работа со складом)
description: Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834153"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="044f2-103">Корректировка уровней запасов на складе (базовая работа со складом)</span><span class="sxs-lookup"><span data-stu-id="044f2-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="044f2-104">Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе.</span><span class="sxs-lookup"><span data-stu-id="044f2-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="044f2-105">Необходимо настроить наименование журнала запасов для корректировки запасов перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="044f2-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="044f2-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="044f2-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="044f2-107">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="044f2-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="044f2-108">Создание журнала коррекции запасов</span><span class="sxs-lookup"><span data-stu-id="044f2-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="044f2-109">Перейдите "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Корректировка запасов".</span><span class="sxs-lookup"><span data-stu-id="044f2-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="044f2-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="044f2-110">Click New.</span></span>
3. <span data-ttu-id="044f2-111">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="044f2-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="044f2-112">В списке щелкните наименование журнала коррекции запасов, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="044f2-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="044f2-113">Некоторые другие поля будут заполнены на основе настройки выбранного наименования журнала коррекции запасов.</span><span class="sxs-lookup"><span data-stu-id="044f2-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="044f2-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="044f2-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="044f2-115">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="044f2-115">Create journal lines</span></span>
1. <span data-ttu-id="044f2-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="044f2-116">Click New.</span></span>
2. <span data-ttu-id="044f2-117">Отметьте поле кода номенклатуры в списке.</span><span class="sxs-lookup"><span data-stu-id="044f2-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="044f2-118">В поле "Код номенклатуры" выберите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="044f2-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="044f2-119">При использовании компании с демонстрационными данными USMF введите "D0001".</span><span class="sxs-lookup"><span data-stu-id="044f2-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="044f2-120">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="044f2-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="044f2-121">Выберите сайт в списке.</span><span class="sxs-lookup"><span data-stu-id="044f2-121">In the list, select a site.</span></span>
6. <span data-ttu-id="044f2-122">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="044f2-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="044f2-123">Выберите склад в списке.</span><span class="sxs-lookup"><span data-stu-id="044f2-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="044f2-124">Если выбрана номенклатура с местонахождением как обязательная аналитика, здесь необходимо указать местонахождение.</span><span class="sxs-lookup"><span data-stu-id="044f2-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="044f2-125">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="044f2-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="044f2-126">В поле себестоимости указывается стоимость на единицу для поступлений на склад.</span><span class="sxs-lookup"><span data-stu-id="044f2-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="044f2-127">Если для кода номенклатуры не указана себестоимость или ее нужно изменить вручную, это делается здесь.</span><span class="sxs-lookup"><span data-stu-id="044f2-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="044f2-128">Проверка и разноска журнала коррекции запасов</span><span class="sxs-lookup"><span data-stu-id="044f2-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="044f2-129">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="044f2-129">Click Validate.</span></span>
2. <span data-ttu-id="044f2-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="044f2-130">Click OK.</span></span>
3. <span data-ttu-id="044f2-131">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="044f2-131">Click Post.</span></span>
    * <span data-ttu-id="044f2-132">При разноске этого типа журнала разносится приход на склад или расход со склада, изменяются уровень и величина запаса и создаются проводки ГК.</span><span class="sxs-lookup"><span data-stu-id="044f2-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="044f2-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="044f2-133">Click OK.</span></span>
5. <span data-ttu-id="044f2-134">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="044f2-134">Close the form.</span></span>
6. <span data-ttu-id="044f2-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="044f2-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]