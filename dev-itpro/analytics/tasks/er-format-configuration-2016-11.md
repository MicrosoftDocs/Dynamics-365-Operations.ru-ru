--- 
title: "Создание конфигурации формата для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать конфигурацию формата для электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="f90a4-103">Создание конфигурации формата для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="f90a4-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f90a4-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурацию формата для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f90a4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="f90a4-105">Эта конфигурация формата будет определять формат электронных документов, используемых для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="f90a4-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="f90a4-106">В этом примере вам предстоит создать конфигурацию формата для компании-образца Litware, Inc. Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Сопоставление модели с выбранными источникам данных".</span><span class="sxs-lookup"><span data-stu-id="f90a4-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f90a4-107">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="f90a4-107">Create a new format configuration</span></span>
1. <span data-ttu-id="f90a4-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="f90a4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f90a4-109">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="f90a4-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f90a4-110">В дереве выберите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="f90a4-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="f90a4-111">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="f90a4-112">В поле "Создать" введите "Формат, основанный на модели данных PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="f90a4-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="f90a4-113">В поле "Имя" введите "BACS (Великобритания, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="f90a4-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="f90a4-114">BACS (Великобритания, вымышленный)</span><span class="sxs-lookup"><span data-stu-id="f90a4-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="f90a4-115">В поле "Описание" введите "Формат платежа поставщикам BACS (Великобритания, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="f90a4-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="f90a4-116">Формат платежа поставщикам BACS (Великобритания, вымышленный)</span><span class="sxs-lookup"><span data-stu-id="f90a4-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="f90a4-117">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="f90a4-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="f90a4-118">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f90a4-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="f90a4-119">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="f90a4-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="f90a4-120">Можно определить конкретный формат электронного документа.</span><span class="sxs-lookup"><span data-stu-id="f90a4-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="f90a4-121">Оставьте это поле пустым, если вы хотите выбирать формат во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f90a4-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="f90a4-122">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f90a4-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="f90a4-123">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f90a4-123">Click Create configuration.</span></span>
    * <span data-ttu-id="f90a4-124">Новая конфигурация создана.</span><span class="sxs-lookup"><span data-stu-id="f90a4-124">A new configuration has been created.</span></span> <span data-ttu-id="f90a4-125">Черновую версию можно использовать для хранения разрабатываемого формата для управления электронными документами.</span><span class="sxs-lookup"><span data-stu-id="f90a4-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="f90a4-126">Разработка формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="f90a4-126">Design format of electronic document</span></span>
1. <span data-ttu-id="f90a4-127">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="f90a4-127">Click Designer.</span></span>
2. <span data-ttu-id="f90a4-128">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f90a4-129">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="f90a4-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="f90a4-130">В поле "Имя" введите "XML".</span><span class="sxs-lookup"><span data-stu-id="f90a4-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="f90a4-131">XML</span><span class="sxs-lookup"><span data-stu-id="f90a4-131">Xml</span></span>  
5. <span data-ttu-id="f90a4-132">В поле "Кодировка" введите "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="f90a4-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="f90a4-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="f90a4-133">UTF-8</span></span>  
6. <span data-ttu-id="f90a4-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-134">Click OK.</span></span>
7. <span data-ttu-id="f90a4-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="f90a4-136">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="f90a4-137">В поле "Имя" введите "Сообщение".</span><span class="sxs-lookup"><span data-stu-id="f90a4-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="f90a4-138">Сообщение</span><span class="sxs-lookup"><span data-stu-id="f90a4-138">Message</span></span>  
10. <span data-ttu-id="f90a4-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-139">Click OK.</span></span>
11. <span data-ttu-id="f90a4-140">В дереве выберите "Xml\Сообщение".</span><span class="sxs-lookup"><span data-stu-id="f90a4-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="f90a4-141">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-141">Click Add Element.</span></span>
13. <span data-ttu-id="f90a4-142">В поле "Имя" введите "ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="f90a4-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="f90a4-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="f90a4-143">ProcessingDate</span></span>  
14. <span data-ttu-id="f90a4-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-144">Click OK.</span></span>
15. <span data-ttu-id="f90a4-145">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-145">Click Add Element.</span></span>
16. <span data-ttu-id="f90a4-146">В поле "Имя" введите "MessageId".</span><span class="sxs-lookup"><span data-stu-id="f90a4-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="f90a4-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="f90a4-147">MessageId</span></span>  
17. <span data-ttu-id="f90a4-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-148">Click OK.</span></span>
18. <span data-ttu-id="f90a4-149">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-149">Click Add Element.</span></span>
19. <span data-ttu-id="f90a4-150">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="f90a4-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="f90a4-151">Оплаты</span><span class="sxs-lookup"><span data-stu-id="f90a4-151">Payments</span></span>  
20. <span data-ttu-id="f90a4-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-152">Click OK.</span></span>
21. <span data-ttu-id="f90a4-153">В дереве выберите "Xml\Сообщение\Платежи".</span><span class="sxs-lookup"><span data-stu-id="f90a4-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="f90a4-154">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-154">Click Add Element.</span></span>
23. <span data-ttu-id="f90a4-155">В поле "Имя" введите "Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="f90a4-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="f90a4-156">Раздел</span><span class="sxs-lookup"><span data-stu-id="f90a4-156">Item</span></span>  
24. <span data-ttu-id="f90a4-157">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-157">Click OK.</span></span>
25. <span data-ttu-id="f90a4-158">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="f90a4-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="f90a4-159">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="f90a4-160">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="f90a4-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="f90a4-161">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="f90a4-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="f90a4-162">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="f90a4-162">Id</span></span>  
29. <span data-ttu-id="f90a4-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-163">Click OK.</span></span>
30. <span data-ttu-id="f90a4-164">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="f90a4-165">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="f90a4-166">В поле "Имя" введите "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="f90a4-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="f90a4-167">Поставщик</span><span class="sxs-lookup"><span data-stu-id="f90a4-167">Vendor</span></span>  
33. <span data-ttu-id="f90a4-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-168">Click OK.</span></span>
34. <span data-ttu-id="f90a4-169">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик".</span><span class="sxs-lookup"><span data-stu-id="f90a4-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="f90a4-170">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-170">Click Add Element.</span></span>
36. <span data-ttu-id="f90a4-171">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="f90a4-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="f90a4-172">Наименование</span><span class="sxs-lookup"><span data-stu-id="f90a4-172">Name</span></span>  
37. <span data-ttu-id="f90a4-173">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-173">Click OK.</span></span>
38. <span data-ttu-id="f90a4-174">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-174">Click Add Element.</span></span>
39. <span data-ttu-id="f90a4-175">В поле "Имя" введите "Банк".</span><span class="sxs-lookup"><span data-stu-id="f90a4-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="f90a4-176">Денежные средства</span><span class="sxs-lookup"><span data-stu-id="f90a4-176">Bank</span></span>  
40. <span data-ttu-id="f90a4-177">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-177">Click OK.</span></span>
41. <span data-ttu-id="f90a4-178">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк".</span><span class="sxs-lookup"><span data-stu-id="f90a4-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="f90a4-179">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-179">Click Add Element.</span></span>
43. <span data-ttu-id="f90a4-180">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="f90a4-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="f90a4-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="f90a4-181">RoutingNumber</span></span>  
44. <span data-ttu-id="f90a4-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-182">Click OK.</span></span>
45. <span data-ttu-id="f90a4-183">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-183">Click Add Element.</span></span>
46. <span data-ttu-id="f90a4-184">В поле "Имя" введите "AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="f90a4-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="f90a4-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="f90a4-185">AccountNumber</span></span>  
47. <span data-ttu-id="f90a4-186">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-186">Click OK.</span></span>
48. <span data-ttu-id="f90a4-187">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик".</span><span class="sxs-lookup"><span data-stu-id="f90a4-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="f90a4-188">Щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="f90a4-188">Click Copy.</span></span>
50. <span data-ttu-id="f90a4-189">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="f90a4-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="f90a4-190">Щелкните "Вставить".</span><span class="sxs-lookup"><span data-stu-id="f90a4-190">Click Paste.</span></span>
52. <span data-ttu-id="f90a4-191">В поле "Имя" введите "Плательщик",</span><span class="sxs-lookup"><span data-stu-id="f90a4-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="f90a4-192">Плательщик</span><span class="sxs-lookup"><span data-stu-id="f90a4-192">Payer</span></span>  
53. <span data-ttu-id="f90a4-193">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="f90a4-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="f90a4-194">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-194">Click Add Element.</span></span>
55. <span data-ttu-id="f90a4-195">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="f90a4-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="f90a4-196">Валютное</span><span class="sxs-lookup"><span data-stu-id="f90a4-196">Currency</span></span>  
56. <span data-ttu-id="f90a4-197">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-197">Click OK.</span></span>
57. <span data-ttu-id="f90a4-198">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-198">Click Add Element.</span></span>
58. <span data-ttu-id="f90a4-199">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="f90a4-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="f90a4-200">описание</span><span class="sxs-lookup"><span data-stu-id="f90a4-200">Description</span></span>  
59. <span data-ttu-id="f90a4-201">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-201">Click OK.</span></span>
60. <span data-ttu-id="f90a4-202">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-202">Click Add Element.</span></span>
61. <span data-ttu-id="f90a4-203">В поле "Имя" введите "TransDate".</span><span class="sxs-lookup"><span data-stu-id="f90a4-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="f90a4-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="f90a4-204">TransDate</span></span>  
62. <span data-ttu-id="f90a4-205">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-205">Click OK.</span></span>
63. <span data-ttu-id="f90a4-206">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f90a4-206">Click Add Element.</span></span>
64. <span data-ttu-id="f90a4-207">В поле "Имя" введите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="f90a4-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="f90a4-208">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="f90a4-208">Amount</span></span>  
65. <span data-ttu-id="f90a4-209">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="f90a4-210">Подготовка компонентов формата для сопоставления с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="f90a4-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="f90a4-211">В дереве выберите "Xml\Сообщение\ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="f90a4-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="f90a4-212">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="f90a4-213">В дереве выберите "Текст\DateTime".</span><span class="sxs-lookup"><span data-stu-id="f90a4-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="f90a4-214">В поле "Формат" введите "yyyy-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="f90a4-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="f90a4-215">гггг-ММ-дд</span><span class="sxs-lookup"><span data-stu-id="f90a4-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="f90a4-216">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-216">Click OK.</span></span>
6. <span data-ttu-id="f90a4-217">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\TransDate".</span><span class="sxs-lookup"><span data-stu-id="f90a4-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="f90a4-218">Нажмите кнопку "Добавить DateTime".</span><span class="sxs-lookup"><span data-stu-id="f90a4-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="f90a4-219">В поле "Формат" введите "yyyy-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="f90a4-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="f90a4-220">гггг-ММ-дд</span><span class="sxs-lookup"><span data-stu-id="f90a4-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="f90a4-221">В поле "Тип DateTime" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="f90a4-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="f90a4-222">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f90a4-222">Click OK.</span></span>
11. <span data-ttu-id="f90a4-223">В дереве выберите "Xml\Сообщение\MessageId".</span><span class="sxs-lookup"><span data-stu-id="f90a4-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="f90a4-224">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90a4-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="f90a4-225">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="f90a4-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="f90a4-226">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-226">Click OK.</span></span>
15. <span data-ttu-id="f90a4-227">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя".</span><span class="sxs-lookup"><span data-stu-id="f90a4-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="f90a4-228">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-228">Click Add String.</span></span>
17. <span data-ttu-id="f90a4-229">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-229">Click OK.</span></span>
18. <span data-ttu-id="f90a4-230">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="f90a4-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="f90a4-231">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-231">Click Add String.</span></span>
20. <span data-ttu-id="f90a4-232">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-232">Click OK.</span></span>
21. <span data-ttu-id="f90a4-233">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="f90a4-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="f90a4-234">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-234">Click Add String.</span></span>
23. <span data-ttu-id="f90a4-235">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-235">Click OK.</span></span>
24. <span data-ttu-id="f90a4-236">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Имя".</span><span class="sxs-lookup"><span data-stu-id="f90a4-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="f90a4-237">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-237">Click Add String.</span></span>
26. <span data-ttu-id="f90a4-238">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-238">Click OK.</span></span>
27. <span data-ttu-id="f90a4-239">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="f90a4-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="f90a4-240">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-240">Click Add String.</span></span>
29. <span data-ttu-id="f90a4-241">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-241">Click OK.</span></span>
30. <span data-ttu-id="f90a4-242">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="f90a4-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="f90a4-243">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-243">Click Add String.</span></span>
32. <span data-ttu-id="f90a4-244">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-244">Click OK.</span></span>
33. <span data-ttu-id="f90a4-245">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Валюта".</span><span class="sxs-lookup"><span data-stu-id="f90a4-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="f90a4-246">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-246">Click Add String.</span></span>
35. <span data-ttu-id="f90a4-247">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-247">Click OK.</span></span>
36. <span data-ttu-id="f90a4-248">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Описание".</span><span class="sxs-lookup"><span data-stu-id="f90a4-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="f90a4-249">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-249">Click Add String.</span></span>
38. <span data-ttu-id="f90a4-250">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-250">Click OK.</span></span>
39. <span data-ttu-id="f90a4-251">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Сумма".</span><span class="sxs-lookup"><span data-stu-id="f90a4-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="f90a4-252">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f90a4-252">Click Add String.</span></span>
41. <span data-ttu-id="f90a4-253">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f90a4-253">Click OK.</span></span>
42. <span data-ttu-id="f90a4-254">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f90a4-254">Click Save.</span></span>
43. <span data-ttu-id="f90a4-255">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f90a4-255">Close the page.</span></span>


