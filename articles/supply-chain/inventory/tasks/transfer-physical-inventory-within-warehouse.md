---
title: Перемещение физических запасов в пределах склада
description: Эта процедура описывает процесс создания и разноски журнала перемещения запасов для регистрации перемещения номенклатуры из одного местонахождения на складе в другое.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c00b6d18b036482cd96e2287119ddb7fd80bfa2d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011455"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="d48a7-103">Перемещение физических запасов в пределах склада</span><span class="sxs-lookup"><span data-stu-id="d48a7-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d48a7-104">Эта процедура описывает процесс создания и разноски журнала перемещения запасов для регистрации перемещения номенклатуры из одного местонахождения на складе в другое.</span><span class="sxs-lookup"><span data-stu-id="d48a7-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="d48a7-105">Необходимо настроить наименование журнала запасов для перемещения запасов перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d48a7-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="d48a7-106">Можно выполнить эту процедуру с помощью демонстрационных данных компании USMF, используя указанные значения из примеров, или можно использовать собственные данные, если настроены продукты и местонахождения.</span><span class="sxs-lookup"><span data-stu-id="d48a7-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="d48a7-107">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="d48a7-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="d48a7-108">Создание журнала перемещения запасов</span><span class="sxs-lookup"><span data-stu-id="d48a7-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="d48a7-109">В **области переходов** выберите **Управление запасами > Записи журнала > Номенклатуры > Перемещение**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="d48a7-110">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-110">Click **New**.</span></span>
3. <span data-ttu-id="d48a7-111">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="d48a7-112">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-112">Click **OK**.</span></span> <span data-ttu-id="d48a7-113">Есть параметр для указания аналитик "От" и "До" для каждой строки журнала.</span><span class="sxs-lookup"><span data-stu-id="d48a7-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="d48a7-114">Это необходимо для этого типа журнала.</span><span class="sxs-lookup"><span data-stu-id="d48a7-114">These are essential for this journal type.</span></span> <span data-ttu-id="d48a7-115">Можно перенести номенклатуры в местонахождения, используя различные правила.</span><span class="sxs-lookup"><span data-stu-id="d48a7-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="d48a7-116">В этом примере мы перенесем номенклатуру в пределах одного склада из местонахождения, контролируемого номерными знаком, в местонахождение, не контролируемое номерным знаком.</span><span class="sxs-lookup"><span data-stu-id="d48a7-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="d48a7-117">Создать строки журнала</span><span class="sxs-lookup"><span data-stu-id="d48a7-117">Create journal lines</span></span>
1. <span data-ttu-id="d48a7-118">На экспресс-вкладке **Строки журнала** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="d48a7-119">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-120">При использовании USMF можно выбрать "A0001".</span><span class="sxs-lookup"><span data-stu-id="d48a7-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="d48a7-121">В поле **С сайта** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-122">При использовании USMF можно выбрать "2".</span><span class="sxs-lookup"><span data-stu-id="d48a7-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="d48a7-123">В поле **На сайт** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-124">При использовании USMF можно выбрать "2".</span><span class="sxs-lookup"><span data-stu-id="d48a7-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="d48a7-125">В поле **Со склада** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-126">При использовании USMF можно выбрать "24".</span><span class="sxs-lookup"><span data-stu-id="d48a7-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="d48a7-127">В поле **На склад** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-128">При использовании USMF можно выбрать "24".</span><span class="sxs-lookup"><span data-stu-id="d48a7-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="d48a7-129">В поле **Из местонахождения** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-130">При использовании USMF можно выбрать "FL-001".</span><span class="sxs-lookup"><span data-stu-id="d48a7-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="d48a7-131">В поле **В местонахождение** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-132">При использовании USMF можно выбрать "BULK-001".</span><span class="sxs-lookup"><span data-stu-id="d48a7-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="d48a7-133">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="d48a7-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="d48a7-134">На экспресс-вкладке **Сведения по строке** откройте вкладку **Складские аналитики**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="d48a7-135">В разделе **Из складских аналитик** в поле **Номерной знак** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d48a7-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="d48a7-136">При использовании USMF можно выбрать "24".</span><span class="sxs-lookup"><span data-stu-id="d48a7-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="d48a7-137">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="d48a7-138">Разноска журнала перемещения запасов</span><span class="sxs-lookup"><span data-stu-id="d48a7-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="d48a7-139">В области **Панель операций** щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="d48a7-140">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="d48a7-141">Просмотр складских проводок</span><span class="sxs-lookup"><span data-stu-id="d48a7-141">View inventory transactions</span></span>
1. <span data-ttu-id="d48a7-142">Щелкните **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="d48a7-143">Щелкните **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="d48a7-143">Click **Transactions**.</span></span> <span data-ttu-id="d48a7-144">Здесь можно просмотреть проводки, созданные при разноске журнала.</span><span class="sxs-lookup"><span data-stu-id="d48a7-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

