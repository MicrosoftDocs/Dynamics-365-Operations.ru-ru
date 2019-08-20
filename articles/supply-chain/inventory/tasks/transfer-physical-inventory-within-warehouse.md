---
title: Перемещение физических запасов в пределах склада
description: Эта процедура описывает процесс создания и разноски журнала перемещения запасов для регистрации перемещения номенклатуры из одного местонахождения на складе в другое.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7344bfa3be0d7345d3ac68202c7bc26bcac8ebb9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845265"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="76908-103">Перемещение физических запасов в пределах склада</span><span class="sxs-lookup"><span data-stu-id="76908-103">Transfer physical inventory within the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76908-104">Эта процедура описывает процесс создания и разноски журнала перемещения запасов для регистрации перемещения номенклатуры из одного местонахождения на складе в другое.</span><span class="sxs-lookup"><span data-stu-id="76908-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="76908-105">Необходимо настроить наименование журнала запасов для перемещения запасов перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="76908-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="76908-106">Можно выполнить эту процедуру с помощью демонстрационных данных компании USMF, используя указанные значения из примеров, или можно использовать собственные данные, если настроены продукты и местонахождения.</span><span class="sxs-lookup"><span data-stu-id="76908-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="76908-107">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="76908-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="76908-108">Создание журнала перемещения запасов</span><span class="sxs-lookup"><span data-stu-id="76908-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="76908-109">Перейдите к "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="76908-109">Go to Transfer.</span></span>
2. <span data-ttu-id="76908-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="76908-110">Click New.</span></span>
3. <span data-ttu-id="76908-111">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="76908-112">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76908-112">Click OK.</span></span>
    * <span data-ttu-id="76908-113">Есть параметр для указания аналитик "От" и "До" для каждой строки журнала.</span><span class="sxs-lookup"><span data-stu-id="76908-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="76908-114">Это необходимо для этого типа журнала.</span><span class="sxs-lookup"><span data-stu-id="76908-114">These are essential for this journal type.</span></span> <span data-ttu-id="76908-115">Можно перенести номенклатуры в местонахождения, используя различные правила.</span><span class="sxs-lookup"><span data-stu-id="76908-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="76908-116">В этом примере мы перенесем номенклатуру в пределах одного склада из местонахождения, контролируемого номерными знаком, в местонахождение, не контролируемое номерным знаком.</span><span class="sxs-lookup"><span data-stu-id="76908-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="76908-117">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="76908-117">Create journal lines</span></span>
1. <span data-ttu-id="76908-118">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="76908-118">Click New.</span></span>
2. <span data-ttu-id="76908-119">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-120">При использовании USMF можно выбрать "A0001".</span><span class="sxs-lookup"><span data-stu-id="76908-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="76908-121">В поле "С сайта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-122">При использовании USMF можно выбрать "2".</span><span class="sxs-lookup"><span data-stu-id="76908-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="76908-123">В поле "На сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-124">При использовании USMF можно выбрать "2".</span><span class="sxs-lookup"><span data-stu-id="76908-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="76908-125">В поле "Со склада" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-126">При использовании USMF можно выбрать "24".</span><span class="sxs-lookup"><span data-stu-id="76908-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="76908-127">В поле "На склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-128">При использовании USMF можно выбрать "24".</span><span class="sxs-lookup"><span data-stu-id="76908-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="76908-129">В поле "Из местонахождения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-130">При использовании USMF можно выбрать "FL-001".</span><span class="sxs-lookup"><span data-stu-id="76908-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="76908-131">В поле "В местонахождения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-132">При использовании USMF можно выбрать "BULK-001".</span><span class="sxs-lookup"><span data-stu-id="76908-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="76908-133">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="76908-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="76908-134">Перейдите на вкладку "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="76908-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="76908-135">В поле "Номерной знак" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="76908-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="76908-136">При использовании USMF можно выбрать "24".</span><span class="sxs-lookup"><span data-stu-id="76908-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="76908-137">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="76908-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="76908-138">Разноска журнала перемещения запасов</span><span class="sxs-lookup"><span data-stu-id="76908-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="76908-139">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="76908-139">Click Post.</span></span>
2. <span data-ttu-id="76908-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76908-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="76908-141">Просмотр складских проводок</span><span class="sxs-lookup"><span data-stu-id="76908-141">View inventory transactions</span></span>
1. <span data-ttu-id="76908-142">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="76908-142">Click Inventory.</span></span>
2. <span data-ttu-id="76908-143">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="76908-143">Click Transactions.</span></span>
    * <span data-ttu-id="76908-144">Здесь можно просмотреть проводки, созданные при разноске журнала.</span><span class="sxs-lookup"><span data-stu-id="76908-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

