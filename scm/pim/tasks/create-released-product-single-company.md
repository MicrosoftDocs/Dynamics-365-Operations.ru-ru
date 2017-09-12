--- 
title: "Создание выпущенного продукта для одной компании"
description: "Эта процедура представляет собой пошаговую демонстрацию создания одного выпущенного продукта в контексте одного юридического лица."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 042eafc29e377e0ad6fb8dc1499daf8eb105b7ed
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="04333-103">Создание выпущенного продукта для одной компании</span><span class="sxs-lookup"><span data-stu-id="04333-103">Create a released product for a single company</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04333-104">Эта процедура представляет собой пошаговую демонстрацию создания одного выпущенного продукта в контексте одного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="04333-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="04333-105">После того как выпущенный продукт создан, он становится непосредственно доступен только в этом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="04333-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="04333-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="04333-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="04333-107">Обычно эта задача выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="04333-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="04333-108">Создание выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="04333-108">Create a released product</span></span>
1. <span data-ttu-id="04333-109">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="04333-109">Go to Released products.</span></span>
2. <span data-ttu-id="04333-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="04333-110">Click New.</span></span>
3. <span data-ttu-id="04333-111">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="04333-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="04333-112">Если номер продукта не вводится в поле "Номер продукта" автоматически, введите уникальный номер продукта.</span><span class="sxs-lookup"><span data-stu-id="04333-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="04333-113">Этот шаг необходим, только если для номеров продуктов не была настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="04333-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="04333-114">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="04333-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="04333-115">Имя продукта по умолчанию извлекается из имени поиска.</span><span class="sxs-lookup"><span data-stu-id="04333-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="04333-116">При необходимости имя поиска можно изменить.</span><span class="sxs-lookup"><span data-stu-id="04333-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="04333-117">В поле "Группа номенклатурных моделей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-118">В группах номенклатурных моделей содержатся настройки, определяющие порядок контроля и управления приходом и расходом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="04333-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="04333-119">Параметры также определяют способ расчета потребления номенклатур.</span><span class="sxs-lookup"><span data-stu-id="04333-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="04333-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="04333-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="04333-122">В поле "Номенклатурная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-123">Номенклатурные группы используются для управления запасами путем распределения складских номенклатур по группам на основании характеристик номенклатур.</span><span class="sxs-lookup"><span data-stu-id="04333-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="04333-124">Например, для управления способом разноски сведений для счетов ГК можно создать ряд различных номенклатурных групп, связанных с определенными счетами ГК.</span><span class="sxs-lookup"><span data-stu-id="04333-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="04333-125">Это позволит отслеживать стоимость запасов для номенклатур на различных стадиях.</span><span class="sxs-lookup"><span data-stu-id="04333-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="04333-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="04333-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="04333-128">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-129">С помощью аналитик хранения можно управлять хранением и извлечением номенклатур из запасов.</span><span class="sxs-lookup"><span data-stu-id="04333-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="04333-130">Например, в качестве аналитики хранения может использоваться "Сайт" и "Склад".</span><span class="sxs-lookup"><span data-stu-id="04333-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="04333-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="04333-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="04333-133">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-134">Группа аналитик отслеживания определяет, какие аналитики отслеживания можно добавить к продукту.</span><span class="sxs-lookup"><span data-stu-id="04333-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="04333-135">Например, номер партии и серийный номер используются для отслеживания складских номенклатур.</span><span class="sxs-lookup"><span data-stu-id="04333-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="04333-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="04333-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="04333-138">В поле "Ед. изм. складского учета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-139">Единица измерения складского учета определяет количественное выражение продукта при хранении в запасах.</span><span class="sxs-lookup"><span data-stu-id="04333-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="04333-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="04333-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="04333-142">В поле "Ед. изм. покупки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-143">Единица измерения покупки определяет количественное выражение продукта при покупке у поставщика.</span><span class="sxs-lookup"><span data-stu-id="04333-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="04333-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="04333-145">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="04333-146">В поле "Ед. изм. продажи" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-147">Единица измерения продажи определяет количественное выражение продукта при продаже клиенту.</span><span class="sxs-lookup"><span data-stu-id="04333-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="04333-148">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="04333-149">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="04333-150">В поле "Единица измерения спецификации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-151">Единица измерения спецификации определяет количественное выражение продукта при его включении в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="04333-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="04333-152">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="04333-153">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="04333-154">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-155">Налоговая группа номенклатур в группе налогообложения продажи определяет способ расчета налога на продажу для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="04333-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="04333-156">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="04333-157">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="04333-158">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04333-159">Налоговая группа номенклатур в группе налогообложения покупки определяет способ расчета налога на покупку для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="04333-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="04333-160">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="04333-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="04333-161">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="04333-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="04333-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="04333-163">Добавление характеристик продукта</span><span class="sxs-lookup"><span data-stu-id="04333-163">Add product characteristics</span></span>
1. <span data-ttu-id="04333-164">Разверните или сверните раздел "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="04333-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="04333-165">В поле "Вес нетто" введите число.</span><span class="sxs-lookup"><span data-stu-id="04333-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="04333-166">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="04333-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="04333-167">В поле "Брутто-глубина" введите число.</span><span class="sxs-lookup"><span data-stu-id="04333-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="04333-168">В поле "Брутто-ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="04333-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="04333-169">В поле "Брутто-высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="04333-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="04333-170">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="04333-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="04333-171">Добавление финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="04333-171">Add financial dimensions</span></span>
1. <span data-ttu-id="04333-172">Разверните или сверните раздел "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="04333-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="04333-173">В поле "BusinessUnit" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="04333-174">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="04333-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="04333-175">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="04333-176">В поле "CostCenter" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="04333-177">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="04333-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="04333-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="04333-179">В поле "Подразделение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="04333-180">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="04333-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="04333-181">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="04333-182">В поле "ItemGroup" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="04333-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="04333-183">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="04333-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="04333-184">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="04333-184">In the list, click the link in the selected row.</span></span>


