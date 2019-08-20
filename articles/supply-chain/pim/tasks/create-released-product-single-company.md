---
title: Создание выпущенного продукта для одной компании
description: Эта процедура представляет собой пошаговую демонстрацию создания одного выпущенного продукта в контексте одного юридического лица.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4a34a03dc5bb3cec37bbccdf913bee5088af6a0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844617"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="4e952-103">Создание выпущенного продукта для одной компании</span><span class="sxs-lookup"><span data-stu-id="4e952-103">Create a released product for a single company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e952-104">Эта процедура представляет собой пошаговую демонстрацию создания одного выпущенного продукта в контексте одного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="4e952-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="4e952-105">После того как выпущенный продукт создан, он становится непосредственно доступен только в этом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="4e952-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="4e952-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="4e952-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="4e952-107">Обычно эта задача выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="4e952-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="4e952-108">Создание выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="4e952-108">Create a released product</span></span>
1. <span data-ttu-id="4e952-109">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="4e952-109">Go to Released products.</span></span>
2. <span data-ttu-id="4e952-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4e952-110">Click New.</span></span>
3. <span data-ttu-id="4e952-111">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4e952-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4e952-112">Если номер продукта не вводится в поле "Номер продукта" автоматически, введите уникальный номер продукта.</span><span class="sxs-lookup"><span data-stu-id="4e952-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="4e952-113">Этот шаг необходим, только если для номеров продуктов не была настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="4e952-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="4e952-114">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4e952-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="4e952-115">Имя продукта по умолчанию извлекается из имени поиска.</span><span class="sxs-lookup"><span data-stu-id="4e952-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="4e952-116">При необходимости имя поиска можно изменить.</span><span class="sxs-lookup"><span data-stu-id="4e952-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="4e952-117">В поле "Группа номенклатурных моделей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-118">В группах номенклатурных моделей содержатся настройки, определяющие порядок контроля и управления приходом и расходом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4e952-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="4e952-119">Параметры также определяют способ расчета потребления номенклатур.</span><span class="sxs-lookup"><span data-stu-id="4e952-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="4e952-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4e952-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4e952-122">В поле "Номенклатурная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-123">Номенклатурные группы используются для управления запасами путем распределения складских номенклатур по группам на основании характеристик номенклатур.</span><span class="sxs-lookup"><span data-stu-id="4e952-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="4e952-124">Например, для управления способом разноски сведений для счетов ГК можно создать ряд различных номенклатурных групп, связанных с определенными счетами ГК.</span><span class="sxs-lookup"><span data-stu-id="4e952-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="4e952-125">Это позволит отслеживать стоимость запасов для номенклатур на различных стадиях.</span><span class="sxs-lookup"><span data-stu-id="4e952-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="4e952-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4e952-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4e952-128">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-129">С помощью аналитик хранения можно управлять хранением и извлечением номенклатур из запасов.</span><span class="sxs-lookup"><span data-stu-id="4e952-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="4e952-130">Например, в качестве аналитики хранения может использоваться "Сайт" и "Склад".</span><span class="sxs-lookup"><span data-stu-id="4e952-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="4e952-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="4e952-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4e952-133">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-134">Группа аналитик отслеживания определяет, какие аналитики отслеживания можно добавить к продукту.</span><span class="sxs-lookup"><span data-stu-id="4e952-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="4e952-135">Например, номер партии и серийный номер используются для отслеживания складских номенклатур.</span><span class="sxs-lookup"><span data-stu-id="4e952-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="4e952-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="4e952-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="4e952-138">В поле "Ед. изм. складского учета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-139">Единица измерения складского учета определяет количественное выражение продукта при хранении в запасах.</span><span class="sxs-lookup"><span data-stu-id="4e952-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="4e952-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="4e952-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="4e952-142">В поле "Ед. изм. покупки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-143">Единица измерения покупки определяет количественное выражение продукта при покупке у поставщика.</span><span class="sxs-lookup"><span data-stu-id="4e952-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="4e952-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="4e952-145">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="4e952-146">В поле "Ед. изм. продажи" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-147">Единица измерения продажи определяет количественное выражение продукта при продаже клиенту.</span><span class="sxs-lookup"><span data-stu-id="4e952-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="4e952-148">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="4e952-149">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="4e952-150">В поле "Единица измерения спецификации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-151">Единица измерения спецификации определяет количественное выражение продукта при его включении в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="4e952-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="4e952-152">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="4e952-153">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="4e952-154">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-155">Налоговая группа номенклатур в группе налогообложения продажи определяет способ расчета налога на продажу для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4e952-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="4e952-156">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="4e952-157">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="4e952-158">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4e952-159">Налоговая группа номенклатур в группе налогообложения покупки определяет способ расчета налога на покупку для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4e952-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="4e952-160">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e952-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="4e952-161">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="4e952-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4e952-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="4e952-163">Добавление характеристик продукта</span><span class="sxs-lookup"><span data-stu-id="4e952-163">Add product characteristics</span></span>
1. <span data-ttu-id="4e952-164">Разверните или сверните раздел "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="4e952-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="4e952-165">В поле "Вес нетто" введите число.</span><span class="sxs-lookup"><span data-stu-id="4e952-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="4e952-166">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="4e952-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="4e952-167">В поле "Брутто-глубина" введите число.</span><span class="sxs-lookup"><span data-stu-id="4e952-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="4e952-168">В поле "Брутто-ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="4e952-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="4e952-169">В поле "Брутто-высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="4e952-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="4e952-170">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="4e952-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="4e952-171">Добавление финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="4e952-171">Add financial dimensions</span></span>
1. <span data-ttu-id="4e952-172">Разверните или сверните раздел "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="4e952-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="4e952-173">В поле "BusinessUnit" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4e952-174">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4e952-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="4e952-175">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4e952-176">В поле "CostCenter" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4e952-177">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4e952-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4e952-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4e952-179">В поле "Подразделение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4e952-180">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4e952-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4e952-181">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4e952-182">В поле "ItemGroup" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4e952-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4e952-183">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4e952-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="4e952-184">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e952-184">In the list, click the link in the selected row.</span></span>

