---
title: Учет запасов на складе
description: Эта процедура позволяет создать и разнести журнал инвентаризации запасов для подсчета конкретной номенклатуры в местонахождении на складе.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "353479"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="78455-103">Учет запасов на складе</span><span class="sxs-lookup"><span data-stu-id="78455-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78455-104">Эта процедура позволяет создать и разнести журнал инвентаризации запасов для подсчета конкретной номенклатуры в местонахождении на складе.</span><span class="sxs-lookup"><span data-stu-id="78455-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="78455-105">Процедура применяется к функции базового управления складами, доступной в модуле управления запасами, но не к функции управления складами, которая доступна в модуле управления складом.</span><span class="sxs-lookup"><span data-stu-id="78455-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="78455-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="78455-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="78455-107">При использовании собственных данных убедитесь, что у вас есть продукты и местонахождения и что вы создали наименование журнала запасов для инвентаризации журналов.</span><span class="sxs-lookup"><span data-stu-id="78455-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="78455-108">Инвентаризация запасов обычно выполняется работником склада.</span><span class="sxs-lookup"><span data-stu-id="78455-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="78455-109">Создание журнала инвентаризации запасов</span><span class="sxs-lookup"><span data-stu-id="78455-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="78455-110">Перейдите "Управление запасами" > "Записи журнала" > "Инвентаризация номенклатуры" > "Инвентаризация".</span><span class="sxs-lookup"><span data-stu-id="78455-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="78455-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78455-111">Click New.</span></span>
3. <span data-ttu-id="78455-112">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="78455-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="78455-113">В списке щелкните наименование журнала инвентаризации запасов, который необходимо использовать</span><span class="sxs-lookup"><span data-stu-id="78455-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="78455-114">Некоторые другие поля будут заполнены на основе настройки выбранного наименования журнала инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="78455-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="78455-115">В поле "Работник" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="78455-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="78455-116">Выберите в списке работника, которого вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="78455-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="78455-117">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="78455-117">Click Select.</span></span>
8. <span data-ttu-id="78455-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="78455-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="78455-119">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="78455-119">Create journal lines</span></span>
1. <span data-ttu-id="78455-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78455-120">Click New.</span></span>
2. <span data-ttu-id="78455-121">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="78455-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="78455-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="78455-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78455-123">При использовании компании с демонстрационными данными USMF выберите "A0001".</span><span class="sxs-lookup"><span data-stu-id="78455-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="78455-124">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="78455-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78455-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="78455-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78455-126">При использовании компании с демонстрационными данными USMF выберите сайт "2".</span><span class="sxs-lookup"><span data-stu-id="78455-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="78455-127">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="78455-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="78455-128">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="78455-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78455-129">При использовании компании с демонстрационными данными USMF выберите склад "24".</span><span class="sxs-lookup"><span data-stu-id="78455-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="78455-130">В поле "Местонахождение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="78455-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="78455-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="78455-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78455-132">При использовании компании с демонстрационными данными USMF выберите местонахождение "BULK-001".</span><span class="sxs-lookup"><span data-stu-id="78455-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="78455-133">В поле "Инвентаризовано" введите номер.</span><span class="sxs-lookup"><span data-stu-id="78455-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="78455-134">При вводе подсчитанного количества, которое отличается от числа, указанного в поле "В наличии", поле "Количество" обновляется, чтобы отобразить несоответствие.</span><span class="sxs-lookup"><span data-stu-id="78455-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="78455-135">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="78455-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="78455-136">Выполните разноску журнала инвентаризации запасов</span><span class="sxs-lookup"><span data-stu-id="78455-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="78455-137">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="78455-137">Click Post.</span></span>
    * <span data-ttu-id="78455-138">При разноске журнала инвентаризации запасов если подсчитанная сумма отличается от суммы, которая указана в поле "В наличии", поступление на склад или отпуск разносится, уровень запасов и значение изменяются и проводки ГК создаются.</span><span class="sxs-lookup"><span data-stu-id="78455-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="78455-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="78455-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="78455-140">Просмотр складских проводок</span><span class="sxs-lookup"><span data-stu-id="78455-140">View inventory transactions</span></span>
1. <span data-ttu-id="78455-141">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="78455-141">Click Inventory.</span></span>
2. <span data-ttu-id="78455-142">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="78455-142">Click Transactions.</span></span>
    * <span data-ttu-id="78455-143">Здесь можно просмотреть все связанные проводки, которые будут созданы при разноске журнала инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="78455-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

