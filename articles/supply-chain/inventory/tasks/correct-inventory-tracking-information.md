---
title: Исправление сведений об отслеживании запасов
description: Эта процедура содержит пошаговые инструкции по созданию и разноске журнала перемещения запасов для исправления данных отслеживания запасов.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145786"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="15f34-103">Исправление сведений об отслеживании запасов</span><span class="sxs-lookup"><span data-stu-id="15f34-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15f34-104">Эта процедура содержит пошаговые инструкции по созданию и разноске журнала перемещения запасов для исправления данных отслеживания запасов.</span><span class="sxs-lookup"><span data-stu-id="15f34-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="15f34-105">В этом примере мы обновим информацию о номенклатуре, контролируемой по партиям, изменив неправильно зарегистрированную партию на другую партию.</span><span class="sxs-lookup"><span data-stu-id="15f34-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="15f34-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USPI или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="15f34-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="15f34-107">При использовании собственных данных необходимо иметь номенклатуру, для которой включено отслеживание по партиям, и которая не контролируется по местонахождению.</span><span class="sxs-lookup"><span data-stu-id="15f34-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="15f34-108">Кроме того, необходимо настроить имя журнала запасов было для перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="15f34-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="15f34-109">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="15f34-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="15f34-110">Создание журнала перемещения запасов</span><span class="sxs-lookup"><span data-stu-id="15f34-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="15f34-111">Перейдите к "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="15f34-111">Go to Transfer.</span></span>
2. <span data-ttu-id="15f34-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="15f34-112">Click New.</span></span>
3. <span data-ttu-id="15f34-113">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="15f34-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="15f34-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="15f34-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="15f34-115">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="15f34-115">Create journal lines</span></span>
1. <span data-ttu-id="15f34-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="15f34-116">Click New.</span></span>
2. <span data-ttu-id="15f34-117">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="15f34-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="15f34-118">При использовании USPI выберите номенклатуру M5003.</span><span class="sxs-lookup"><span data-stu-id="15f34-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="15f34-119">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="15f34-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="15f34-120">Перейдите на вкладку "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="15f34-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="15f34-121">В поле "Номер партии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="15f34-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="15f34-122">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="15f34-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="15f34-123">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="15f34-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="15f34-124">В поле "Номер партии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="15f34-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="15f34-125">Разноска журнала</span><span class="sxs-lookup"><span data-stu-id="15f34-125">Post the journal</span></span>
1. <span data-ttu-id="15f34-126">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="15f34-126">Click Post.</span></span>
2. <span data-ttu-id="15f34-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="15f34-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="15f34-128">Проверка сведений о трассировке</span><span class="sxs-lookup"><span data-stu-id="15f34-128">Check tracing information</span></span>
1. <span data-ttu-id="15f34-129">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="15f34-129">Click Inventory.</span></span>
2. <span data-ttu-id="15f34-130">Щелкните "Трассировка".</span><span class="sxs-lookup"><span data-stu-id="15f34-130">Click Trace.</span></span>
3. <span data-ttu-id="15f34-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="15f34-131">Click OK.</span></span>
    * <span data-ttu-id="15f34-132">Используя эти данные трассировки можно отследить исходную партию в запасах, которая была исправлена.</span><span class="sxs-lookup"><span data-stu-id="15f34-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="15f34-133">Для просмотра этих данных также можно использовать страницу "Трассировка номенклатур".</span><span class="sxs-lookup"><span data-stu-id="15f34-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="15f34-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="15f34-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="15f34-135">Проверка проводок по запасам</span><span class="sxs-lookup"><span data-stu-id="15f34-135">Check inventory transactions</span></span>
1. <span data-ttu-id="15f34-136">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="15f34-136">Click Inventory.</span></span>
2. <span data-ttu-id="15f34-137">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="15f34-137">Click Transactions.</span></span>
    * <span data-ttu-id="15f34-138">Здесь можно просмотреть проводки, созданные при разноске журнала.</span><span class="sxs-lookup"><span data-stu-id="15f34-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

