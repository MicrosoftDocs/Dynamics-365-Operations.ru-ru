---
title: Учет запасов на складе
description: Эта тема описывает процесс создания и разноски журнала инвентаризации запасов для подсчета конкретной номенклатуры в местонахождении на складе.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0909625f31d15fe6b1387ff9ab7fd5d9a9135f4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836464"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="a7e32-103">Учет запасов на складе</span><span class="sxs-lookup"><span data-stu-id="a7e32-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7e32-104">Эта тема описывает процесс создания и разноски журнала инвентаризации запасов для подсчета конкретной номенклатуры в местонахождении на складе.</span><span class="sxs-lookup"><span data-stu-id="a7e32-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="a7e32-105">Процедура применяется к функции базового управления складами, доступной в модуле управления запасами, но не к функции управления складами, которая доступна в модуле управления складом.</span><span class="sxs-lookup"><span data-stu-id="a7e32-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="a7e32-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="a7e32-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="a7e32-107">При использовании собственных данных убедитесь, что у вас есть продукты и местонахождения и что вы создали наименование журнала запасов для инвентаризации журналов.</span><span class="sxs-lookup"><span data-stu-id="a7e32-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="a7e32-108">Инвентаризация запасов обычно выполняется работником склада.</span><span class="sxs-lookup"><span data-stu-id="a7e32-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="a7e32-109">Создание журнала инвентаризации запасов</span><span class="sxs-lookup"><span data-stu-id="a7e32-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="a7e32-110">Перейдите в **Область переходов > Модули > Управление запасами > Записи журнала > Инвентаризация номенклатуры > Инвентаризация**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="a7e32-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-111">Select **New**.</span></span>
3. <span data-ttu-id="a7e32-112">В поле **Имя** выберите имя журнала инвентаризации запасов, который вы хотите использовать, из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="a7e32-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="a7e32-113">Некоторые другие поля будут заполнены на основе настройки выбранного наименования журнала инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="a7e32-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="a7e32-114">В поле **Работник** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a7e32-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a7e32-115">В списке **Выберите** работника, которого вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="a7e32-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="a7e32-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="a7e32-117">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="a7e32-117">Create journal lines</span></span>
1. <span data-ttu-id="a7e32-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-118">Select **New**.</span></span>
2. <span data-ttu-id="a7e32-119">В поле **Код номенклатуры** выберите требуемую запись из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="a7e32-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="a7e32-120">При использовании компании с демонстрационными данными USMF выберите **A0001**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="a7e32-121">В поле **Сайт** выберите требуемую запись из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="a7e32-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="a7e32-122">При использовании компании с демонстрационными данными USMF выберите сайт **2**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="a7e32-123">В поле **Склад** выберите требуемую запись из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="a7e32-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="a7e32-124">При использовании компании с демонстрационными данными USMF выберите склад **24**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="a7e32-125">В поле **Местоположение** выберите требуемую запись из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="a7e32-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="a7e32-126">При использовании компании с демонстрационными данными USMF выберите местонахождение **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="a7e32-127">В поле "Инвентаризовано" введите номер.</span><span class="sxs-lookup"><span data-stu-id="a7e32-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="a7e32-128">При вводе подсчитанного количества, которое отличается от числа, указанного в поле **В наличии**, поле **Количество** обновляется, чтобы отобразить несоответствие.</span><span class="sxs-lookup"><span data-stu-id="a7e32-128">If you enter a counted number that’s different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="a7e32-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="a7e32-130">Выполните разноску журнала инвентаризации запасов</span><span class="sxs-lookup"><span data-stu-id="a7e32-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="a7e32-131">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-131">Select **Post**.</span></span> <span data-ttu-id="a7e32-132">При разноске журнала инвентаризации запасов если подсчитанная сумма отличается от суммы, которая указана в поле **В наличии**, поступление на склад или отпуск разносится, уровень запасов и значение изменяются и проводки ГК создаются.</span><span class="sxs-lookup"><span data-stu-id="a7e32-132">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="a7e32-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="a7e32-134">Просмотр складских проводок</span><span class="sxs-lookup"><span data-stu-id="a7e32-134">View inventory transactions</span></span>
1. <span data-ttu-id="a7e32-135">Выберите **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="a7e32-136">Выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="a7e32-136">Select **Transactions**.</span></span> <span data-ttu-id="a7e32-137">Здесь можно просмотреть все связанные проводки, которые будут созданы при разноске журнала инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="a7e32-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

