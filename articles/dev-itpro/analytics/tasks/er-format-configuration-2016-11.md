--- 
title: "Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать конфигурацию формата для электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="1401c-103">Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="1401c-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1401c-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурацию формата для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="1401c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="1401c-105">Эта конфигурация формата будет определять формат электронных документов, используемых для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="1401c-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="1401c-106">В этом примере вам предстоит создать конфигурацию формата для компании-образца Litware, Inc. Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Сопоставление модели с выбранными источникам данных".</span><span class="sxs-lookup"><span data-stu-id="1401c-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="1401c-107">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="1401c-107">Create a new format configuration</span></span>
1. <span data-ttu-id="1401c-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="1401c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1401c-109">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="1401c-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1401c-110">В дереве выберите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="1401c-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="1401c-111">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="1401c-112">В поле "Создать" введите "Формат, основанный на модели данных PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="1401c-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="1401c-113">В поле "Имя" введите "BACS (Великобритания, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="1401c-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="1401c-114">BACS (Великобритания, вымышленный)</span><span class="sxs-lookup"><span data-stu-id="1401c-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="1401c-115">В поле "Описание" введите "Формат платежа поставщикам BACS (Великобритания, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="1401c-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="1401c-116">Формат платежа поставщикам BACS (Великобритания, вымышленный)</span><span class="sxs-lookup"><span data-stu-id="1401c-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="1401c-117">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="1401c-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="1401c-118">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1401c-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="1401c-119">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="1401c-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="1401c-120">Можно определить конкретный формат электронного документа.</span><span class="sxs-lookup"><span data-stu-id="1401c-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="1401c-121">Оставьте это поле пустым, если вы хотите выбирать формат во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1401c-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="1401c-122">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1401c-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="1401c-123">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1401c-123">Click Create configuration.</span></span>
    * <span data-ttu-id="1401c-124">Новая конфигурация создана.</span><span class="sxs-lookup"><span data-stu-id="1401c-124">A new configuration has been created.</span></span> <span data-ttu-id="1401c-125">Черновую версию можно использовать для хранения разрабатываемого формата для управления электронными документами.</span><span class="sxs-lookup"><span data-stu-id="1401c-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="1401c-126">Разработка формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="1401c-126">Design format of electronic document</span></span>
1. <span data-ttu-id="1401c-127">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="1401c-127">Click Designer.</span></span>
2. <span data-ttu-id="1401c-128">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="1401c-129">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="1401c-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="1401c-130">В поле "Имя" введите "XML".</span><span class="sxs-lookup"><span data-stu-id="1401c-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="1401c-131">XML</span><span class="sxs-lookup"><span data-stu-id="1401c-131">Xml</span></span>  
5. <span data-ttu-id="1401c-132">В поле "Кодировка" введите "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="1401c-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="1401c-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="1401c-133">UTF-8</span></span>  
6. <span data-ttu-id="1401c-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-134">Click OK.</span></span>
7. <span data-ttu-id="1401c-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="1401c-136">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="1401c-137">В поле "Имя" введите "Сообщение".</span><span class="sxs-lookup"><span data-stu-id="1401c-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="1401c-138">Сообщение</span><span class="sxs-lookup"><span data-stu-id="1401c-138">Message</span></span>  
10. <span data-ttu-id="1401c-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-139">Click OK.</span></span>
11. <span data-ttu-id="1401c-140">В дереве выберите "Xml\Сообщение".</span><span class="sxs-lookup"><span data-stu-id="1401c-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="1401c-141">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-141">Click Add Element.</span></span>
13. <span data-ttu-id="1401c-142">В поле "Имя" введите "ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="1401c-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="1401c-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="1401c-143">ProcessingDate</span></span>  
14. <span data-ttu-id="1401c-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-144">Click OK.</span></span>
15. <span data-ttu-id="1401c-145">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-145">Click Add Element.</span></span>
16. <span data-ttu-id="1401c-146">В поле "Имя" введите "MessageId".</span><span class="sxs-lookup"><span data-stu-id="1401c-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="1401c-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="1401c-147">MessageId</span></span>  
17. <span data-ttu-id="1401c-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-148">Click OK.</span></span>
18. <span data-ttu-id="1401c-149">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-149">Click Add Element.</span></span>
19. <span data-ttu-id="1401c-150">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="1401c-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="1401c-151">Оплаты</span><span class="sxs-lookup"><span data-stu-id="1401c-151">Payments</span></span>  
20. <span data-ttu-id="1401c-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-152">Click OK.</span></span>
21. <span data-ttu-id="1401c-153">В дереве выберите "Xml\Сообщение\Платежи".</span><span class="sxs-lookup"><span data-stu-id="1401c-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="1401c-154">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-154">Click Add Element.</span></span>
23. <span data-ttu-id="1401c-155">В поле "Имя" введите "Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="1401c-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="1401c-156">Раздел</span><span class="sxs-lookup"><span data-stu-id="1401c-156">Item</span></span>  
24. <span data-ttu-id="1401c-157">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-157">Click OK.</span></span>
25. <span data-ttu-id="1401c-158">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="1401c-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="1401c-159">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="1401c-160">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="1401c-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="1401c-161">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="1401c-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="1401c-162">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="1401c-162">Id</span></span>  
29. <span data-ttu-id="1401c-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-163">Click OK.</span></span>
30. <span data-ttu-id="1401c-164">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="1401c-165">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="1401c-166">В поле "Имя" введите "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="1401c-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="1401c-167">Поставщик</span><span class="sxs-lookup"><span data-stu-id="1401c-167">Vendor</span></span>  
33. <span data-ttu-id="1401c-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-168">Click OK.</span></span>
34. <span data-ttu-id="1401c-169">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик".</span><span class="sxs-lookup"><span data-stu-id="1401c-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="1401c-170">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-170">Click Add Element.</span></span>
36. <span data-ttu-id="1401c-171">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="1401c-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="1401c-172">Наименование</span><span class="sxs-lookup"><span data-stu-id="1401c-172">Name</span></span>  
37. <span data-ttu-id="1401c-173">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-173">Click OK.</span></span>
38. <span data-ttu-id="1401c-174">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-174">Click Add Element.</span></span>
39. <span data-ttu-id="1401c-175">В поле "Имя" введите "Банк".</span><span class="sxs-lookup"><span data-stu-id="1401c-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="1401c-176">Денежные средства</span><span class="sxs-lookup"><span data-stu-id="1401c-176">Bank</span></span>  
40. <span data-ttu-id="1401c-177">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-177">Click OK.</span></span>
41. <span data-ttu-id="1401c-178">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк".</span><span class="sxs-lookup"><span data-stu-id="1401c-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="1401c-179">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-179">Click Add Element.</span></span>
43. <span data-ttu-id="1401c-180">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="1401c-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="1401c-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="1401c-181">RoutingNumber</span></span>  
44. <span data-ttu-id="1401c-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-182">Click OK.</span></span>
45. <span data-ttu-id="1401c-183">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-183">Click Add Element.</span></span>
46. <span data-ttu-id="1401c-184">В поле "Имя" введите "AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="1401c-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="1401c-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="1401c-185">AccountNumber</span></span>  
47. <span data-ttu-id="1401c-186">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-186">Click OK.</span></span>
48. <span data-ttu-id="1401c-187">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик".</span><span class="sxs-lookup"><span data-stu-id="1401c-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="1401c-188">Щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="1401c-188">Click Copy.</span></span>
50. <span data-ttu-id="1401c-189">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="1401c-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="1401c-190">Щелкните "Вставить".</span><span class="sxs-lookup"><span data-stu-id="1401c-190">Click Paste.</span></span>
52. <span data-ttu-id="1401c-191">В поле "Имя" введите "Плательщик",</span><span class="sxs-lookup"><span data-stu-id="1401c-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="1401c-192">Плательщик</span><span class="sxs-lookup"><span data-stu-id="1401c-192">Payer</span></span>  
53. <span data-ttu-id="1401c-193">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="1401c-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="1401c-194">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-194">Click Add Element.</span></span>
55. <span data-ttu-id="1401c-195">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="1401c-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="1401c-196">Валютное</span><span class="sxs-lookup"><span data-stu-id="1401c-196">Currency</span></span>  
56. <span data-ttu-id="1401c-197">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-197">Click OK.</span></span>
57. <span data-ttu-id="1401c-198">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-198">Click Add Element.</span></span>
58. <span data-ttu-id="1401c-199">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="1401c-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="1401c-200">описание</span><span class="sxs-lookup"><span data-stu-id="1401c-200">Description</span></span>  
59. <span data-ttu-id="1401c-201">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-201">Click OK.</span></span>
60. <span data-ttu-id="1401c-202">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-202">Click Add Element.</span></span>
61. <span data-ttu-id="1401c-203">В поле "Имя" введите "TransDate".</span><span class="sxs-lookup"><span data-stu-id="1401c-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="1401c-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="1401c-204">TransDate</span></span>  
62. <span data-ttu-id="1401c-205">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-205">Click OK.</span></span>
63. <span data-ttu-id="1401c-206">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="1401c-206">Click Add Element.</span></span>
64. <span data-ttu-id="1401c-207">В поле "Имя" введите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="1401c-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="1401c-208">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1401c-208">Amount</span></span>  
65. <span data-ttu-id="1401c-209">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="1401c-210">Подготовка компонентов формата для сопоставления с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="1401c-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="1401c-211">В дереве выберите "Xml\Сообщение\ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="1401c-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="1401c-212">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="1401c-213">В дереве выберите "Текст\DateTime".</span><span class="sxs-lookup"><span data-stu-id="1401c-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="1401c-214">В поле "Формат" введите "yyyy-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="1401c-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="1401c-215">гггг-ММ-дд</span><span class="sxs-lookup"><span data-stu-id="1401c-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="1401c-216">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-216">Click OK.</span></span>
6. <span data-ttu-id="1401c-217">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\TransDate".</span><span class="sxs-lookup"><span data-stu-id="1401c-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="1401c-218">Нажмите кнопку "Добавить DateTime".</span><span class="sxs-lookup"><span data-stu-id="1401c-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="1401c-219">В поле "Формат" введите "yyyy-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="1401c-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="1401c-220">гггг-ММ-дд</span><span class="sxs-lookup"><span data-stu-id="1401c-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="1401c-221">В поле "Тип DateTime" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="1401c-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="1401c-222">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1401c-222">Click OK.</span></span>
11. <span data-ttu-id="1401c-223">В дереве выберите "Xml\Сообщение\MessageId".</span><span class="sxs-lookup"><span data-stu-id="1401c-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="1401c-224">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1401c-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="1401c-225">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="1401c-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="1401c-226">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-226">Click OK.</span></span>
15. <span data-ttu-id="1401c-227">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя".</span><span class="sxs-lookup"><span data-stu-id="1401c-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="1401c-228">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-228">Click Add String.</span></span>
17. <span data-ttu-id="1401c-229">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-229">Click OK.</span></span>
18. <span data-ttu-id="1401c-230">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="1401c-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="1401c-231">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-231">Click Add String.</span></span>
20. <span data-ttu-id="1401c-232">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-232">Click OK.</span></span>
21. <span data-ttu-id="1401c-233">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="1401c-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="1401c-234">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-234">Click Add String.</span></span>
23. <span data-ttu-id="1401c-235">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-235">Click OK.</span></span>
24. <span data-ttu-id="1401c-236">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Имя".</span><span class="sxs-lookup"><span data-stu-id="1401c-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="1401c-237">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-237">Click Add String.</span></span>
26. <span data-ttu-id="1401c-238">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-238">Click OK.</span></span>
27. <span data-ttu-id="1401c-239">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="1401c-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="1401c-240">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-240">Click Add String.</span></span>
29. <span data-ttu-id="1401c-241">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-241">Click OK.</span></span>
30. <span data-ttu-id="1401c-242">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="1401c-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="1401c-243">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-243">Click Add String.</span></span>
32. <span data-ttu-id="1401c-244">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-244">Click OK.</span></span>
33. <span data-ttu-id="1401c-245">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Валюта".</span><span class="sxs-lookup"><span data-stu-id="1401c-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="1401c-246">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-246">Click Add String.</span></span>
35. <span data-ttu-id="1401c-247">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-247">Click OK.</span></span>
36. <span data-ttu-id="1401c-248">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Описание".</span><span class="sxs-lookup"><span data-stu-id="1401c-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="1401c-249">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-249">Click Add String.</span></span>
38. <span data-ttu-id="1401c-250">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-250">Click OK.</span></span>
39. <span data-ttu-id="1401c-251">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Сумма".</span><span class="sxs-lookup"><span data-stu-id="1401c-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="1401c-252">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1401c-252">Click Add String.</span></span>
41. <span data-ttu-id="1401c-253">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="1401c-253">Click OK.</span></span>
42. <span data-ttu-id="1401c-254">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1401c-254">Click Save.</span></span>
43. <span data-ttu-id="1401c-255">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1401c-255">Close the page.</span></span>


