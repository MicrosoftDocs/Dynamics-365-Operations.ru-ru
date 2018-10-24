--- 
title: "Создание полуфабриката (февраль 2016 г.)"
description: "Эта задача рассматривает создание полуфабриката."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9caeae552471eed1cb1d8630f387ca31107fcece
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="944c1-103">Создание полуфабриката (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="944c1-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="944c1-104">Эта задача рассматривает создание полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="944c1-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="944c1-105">Это вторая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="944c1-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="944c1-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="944c1-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="944c1-107">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="944c1-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="944c1-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="944c1-108">Click New.</span></span>
3. <span data-ttu-id="944c1-109">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="944c1-110">В этом примере введите "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="944c1-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="944c1-111">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-112">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="944c1-112">Select STD.</span></span> <span data-ttu-id="944c1-113">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="944c1-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="944c1-114">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-115">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="944c1-115">For example, select Audio.</span></span> <span data-ttu-id="944c1-116">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="944c1-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="944c1-117">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-118">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="944c1-118">Select SiteWH.</span></span> <span data-ttu-id="944c1-119">Только сайт и склад будут использоваться в этом примере.</span><span class="sxs-lookup"><span data-stu-id="944c1-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="944c1-120">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-121">Аналитики отслеживания не будут использоваться для данного примера, выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="944c1-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="944c1-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="944c1-122">Click OK.</span></span>
9. <span data-ttu-id="944c1-123">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="944c1-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="944c1-124">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="944c1-124">Click Default order settings.</span></span>
11. <span data-ttu-id="944c1-125">В поле "Тип заказа по умолчанию" выберите "Производство".</span><span class="sxs-lookup"><span data-stu-id="944c1-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="944c1-126">Поскольку это полуфабрикат, который будет произведен, выберите "Производство".</span><span class="sxs-lookup"><span data-stu-id="944c1-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="944c1-127">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-128">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="944c1-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="944c1-129">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-130">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="944c1-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="944c1-131">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-132">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="944c1-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="944c1-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="944c1-133">Close the page.</span></span>
16. <span data-ttu-id="944c1-134">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="944c1-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="944c1-135">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="944c1-135">Click Item price.</span></span>
18. <span data-ttu-id="944c1-136">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="944c1-136">Click New.</span></span>
19. <span data-ttu-id="944c1-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="944c1-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="944c1-138">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-139">В этом примере выберите "Версия 10".</span><span class="sxs-lookup"><span data-stu-id="944c1-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="944c1-140">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-141">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="944c1-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="944c1-142">Задайте цену "10".</span><span class="sxs-lookup"><span data-stu-id="944c1-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="944c1-143">В этом примере введите себестоимость "10".</span><span class="sxs-lookup"><span data-stu-id="944c1-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="944c1-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="944c1-144">Click Save.</span></span>
24. <span data-ttu-id="944c1-145">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="944c1-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="944c1-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="944c1-146">Close the page.</span></span>
26. <span data-ttu-id="944c1-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="944c1-147">Close the page.</span></span>
27. <span data-ttu-id="944c1-148">Щелкните BOM_2, чтобы открыть ее.</span><span class="sxs-lookup"><span data-stu-id="944c1-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="944c1-149">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="944c1-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="944c1-150">В поле "Группа затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="944c1-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="944c1-151">В этом примере выберите "Группа затрат M1".</span><span class="sxs-lookup"><span data-stu-id="944c1-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="944c1-152">Используйте этот ярлык для сохранения записи.</span><span class="sxs-lookup"><span data-stu-id="944c1-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="944c1-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="944c1-153">Close the page.</span></span>


