---
title: Создание выпущенного продукта для одной компании
description: Эта процедура представляет собой пошаговую демонстрацию создания одного выпущенного продукта в контексте одного юридического лица.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 371157aee389694d349ec4fe51af0d9bfbf08cb7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213269"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="f652a-103">Создание выпущенного продукта для одной компании</span><span class="sxs-lookup"><span data-stu-id="f652a-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f652a-104">Эта процедура представляет собой пошаговую демонстрацию создания одного выпущенного продукта в контексте одного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="f652a-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="f652a-105">После того как выпущенный продукт создан, он становится непосредственно доступен только в этом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="f652a-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="f652a-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="f652a-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="f652a-107">Обычно эта задача выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="f652a-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="f652a-108">Создание выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="f652a-108">Create a released product</span></span>
1. <span data-ttu-id="f652a-109">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="f652a-109">Go to Released products.</span></span>
2. <span data-ttu-id="f652a-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f652a-110">Click New.</span></span>
3. <span data-ttu-id="f652a-111">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f652a-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f652a-112">Если номер продукта не вводится в поле "Номер продукта" автоматически, введите уникальный номер продукта.</span><span class="sxs-lookup"><span data-stu-id="f652a-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="f652a-113">Этот шаг необходим, только если для номеров продуктов не была настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="f652a-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="f652a-114">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f652a-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="f652a-115">Имя продукта по умолчанию извлекается из имени поиска.</span><span class="sxs-lookup"><span data-stu-id="f652a-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="f652a-116">При необходимости имя поиска можно изменить.</span><span class="sxs-lookup"><span data-stu-id="f652a-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="f652a-117">В поле "Группа номенклатурных моделей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-118">В группах номенклатурных моделей содержатся настройки, определяющие порядок контроля и управления приходом и расходом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f652a-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="f652a-119">Параметры также определяют способ расчета потребления номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f652a-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="f652a-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f652a-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f652a-122">В поле "Номенклатурная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-123">Номенклатурные группы используются для управления запасами путем распределения складских номенклатур по группам на основании характеристик номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f652a-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="f652a-124">Например, для управления способом разноски сведений для счетов ГК можно создать ряд различных номенклатурных групп, связанных с определенными счетами ГК.</span><span class="sxs-lookup"><span data-stu-id="f652a-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="f652a-125">Это позволит отслеживать стоимость запасов для номенклатур на различных стадиях.</span><span class="sxs-lookup"><span data-stu-id="f652a-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="f652a-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f652a-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f652a-128">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-129">С помощью аналитик хранения можно управлять хранением и извлечением номенклатур из запасов.</span><span class="sxs-lookup"><span data-stu-id="f652a-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="f652a-130">Например, в качестве аналитики хранения может использоваться "Сайт" и "Склад".</span><span class="sxs-lookup"><span data-stu-id="f652a-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="f652a-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="f652a-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f652a-133">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-134">Группа аналитик отслеживания определяет, какие аналитики отслеживания можно добавить к продукту.</span><span class="sxs-lookup"><span data-stu-id="f652a-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="f652a-135">Например, номер партии и серийный номер используются для отслеживания складских номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f652a-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="f652a-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f652a-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f652a-138">В поле "Ед. изм. складского учета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-139">Единица измерения складского учета определяет количественное выражение продукта при хранении в запасах.</span><span class="sxs-lookup"><span data-stu-id="f652a-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="f652a-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="f652a-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="f652a-142">В поле "Ед. изм. покупки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-143">Единица измерения покупки определяет количественное выражение продукта при покупке у поставщика.</span><span class="sxs-lookup"><span data-stu-id="f652a-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="f652a-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="f652a-145">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="f652a-146">В поле "Ед. изм. продажи" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-147">Единица измерения продажи определяет количественное выражение продукта при продаже клиенту.</span><span class="sxs-lookup"><span data-stu-id="f652a-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="f652a-148">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="f652a-149">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="f652a-150">В поле "Единица измерения спецификации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-151">Единица измерения спецификации определяет количественное выражение продукта при его включении в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="f652a-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="f652a-152">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="f652a-153">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="f652a-154">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-155">Налоговая группа номенклатур в группе налогообложения продажи определяет способ расчета налога на продажу для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f652a-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="f652a-156">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="f652a-157">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="f652a-158">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f652a-159">Налоговая группа номенклатур в группе налогообложения покупки определяет способ расчета налога на покупку для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f652a-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="f652a-160">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f652a-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="f652a-161">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="f652a-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f652a-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="f652a-163">Добавление характеристик продукта</span><span class="sxs-lookup"><span data-stu-id="f652a-163">Add product characteristics</span></span>
1. <span data-ttu-id="f652a-164">Разверните или сверните раздел "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="f652a-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="f652a-165">В поле "Вес нетто" введите число.</span><span class="sxs-lookup"><span data-stu-id="f652a-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="f652a-166">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="f652a-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="f652a-167">В поле "Брутто-глубина" введите число.</span><span class="sxs-lookup"><span data-stu-id="f652a-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="f652a-168">В поле "Брутто-ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="f652a-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="f652a-169">В поле "Брутто-высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="f652a-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="f652a-170">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="f652a-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="f652a-171">Добавление финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="f652a-171">Add financial dimensions</span></span>
1. <span data-ttu-id="f652a-172">Разверните или сверните раздел "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="f652a-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="f652a-173">В поле "BusinessUnit" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f652a-174">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f652a-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f652a-175">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f652a-176">В поле "CostCenter" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f652a-177">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f652a-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f652a-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f652a-179">В поле "Подразделение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f652a-180">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f652a-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f652a-181">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f652a-182">В поле "ItemGroup" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f652a-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f652a-183">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f652a-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="f652a-184">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f652a-184">In the list, click the link in the selected row.</span></span>

