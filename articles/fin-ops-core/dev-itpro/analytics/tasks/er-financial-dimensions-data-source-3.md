---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092308"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="6dc51-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)</span><span class="sxs-lookup"><span data-stu-id="6dc51-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6dc51-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="6dc51-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="6dc51-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="6dc51-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="6dc51-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)".</span><span class="sxs-lookup"><span data-stu-id="6dc51-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="6dc51-108">Разработка отчета для представления финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="6dc51-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="6dc51-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="6dc51-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6dc51-110">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="6dc51-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6dc51-111">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="6dc51-112">В поле "Создать" введите "Формат, основанный на модели данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="6dc51-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="6dc51-113">Используйте модель, которая была создана заранее как источник данных для нового отчета.</span><span class="sxs-lookup"><span data-stu-id="6dc51-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="6dc51-114">В поле "Имя" введите "Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="6dc51-115">В поле "Определение модели данных" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="6dc51-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="6dc51-116">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="6dc51-116">Click Create configuration.</span></span>
8. <span data-ttu-id="6dc51-117">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="6dc51-117">Click Designer.</span></span>
9. <span data-ttu-id="6dc51-118">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="6dc51-119">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="6dc51-120">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="6dc51-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="6dc51-121">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6dc51-121">Click OK.</span></span>
13. <span data-ttu-id="6dc51-122">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="6dc51-123">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="6dc51-124">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="6dc51-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="6dc51-125">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6dc51-125">Click OK.</span></span>
17. <span data-ttu-id="6dc51-126">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="6dc51-127">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="6dc51-128">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="6dc51-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="6dc51-129">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6dc51-129">Click OK.</span></span>
21. <span data-ttu-id="6dc51-130">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="6dc51-131">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6dc51-132">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="6dc51-133">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="6dc51-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="6dc51-134">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6dc51-134">Click OK.</span></span>
26. <span data-ttu-id="6dc51-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="6dc51-136">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="6dc51-137">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="6dc51-138">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6dc51-138">Click OK.</span></span>
30. <span data-ttu-id="6dc51-139">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="6dc51-140">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="6dc51-141">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="6dc51-142">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="6dc51-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="6dc51-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-143">Click OK.</span></span>
35. <span data-ttu-id="6dc51-144">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="6dc51-145">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="6dc51-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="6dc51-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-146">Click OK.</span></span>
38. <span data-ttu-id="6dc51-147">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="6dc51-148">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="6dc51-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="6dc51-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-149">Click OK.</span></span>
41. <span data-ttu-id="6dc51-150">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="6dc51-151">В поле "Имя" введите "Дб".</span><span class="sxs-lookup"><span data-stu-id="6dc51-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="6dc51-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-152">Click OK.</span></span>
44. <span data-ttu-id="6dc51-153">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="6dc51-154">В поле "Имя" введите "Кр".</span><span class="sxs-lookup"><span data-stu-id="6dc51-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="6dc51-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-155">Click OK.</span></span>
47. <span data-ttu-id="6dc51-156">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="6dc51-157">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="6dc51-158">В поле "Имя" введите "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="6dc51-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="6dc51-159">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6dc51-159">Click OK.</span></span>
51. <span data-ttu-id="6dc51-160">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="6dc51-161">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6dc51-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="6dc51-162">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="6dc51-163">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="6dc51-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="6dc51-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-164">Click OK.</span></span>
56. <span data-ttu-id="6dc51-165">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="6dc51-166">В поле "Имя" введите "Значение".</span><span class="sxs-lookup"><span data-stu-id="6dc51-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="6dc51-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-167">Click OK.</span></span>
59. <span data-ttu-id="6dc51-168">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="6dc51-169">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="6dc51-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="6dc51-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6dc51-170">Click OK.</span></span>
<span data-ttu-id="6dc51-171">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="6dc51-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="6dc51-172">Сопоставление элементов отчета с источниками данных</span><span class="sxs-lookup"><span data-stu-id="6dc51-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="6dc51-173">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="6dc51-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="6dc51-174">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="6dc51-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6dc51-175">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="6dc51-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="6dc51-176">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="6dc51-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="6dc51-177">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="6dc51-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="6dc51-178">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Описание: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="6dc51-179">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Описание: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="6dc51-180">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-180">Click Bind.</span></span>
9. <span data-ttu-id="6dc51-181">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Значение: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="6dc51-182">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Код: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="6dc51-183">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-183">Click Bind.</span></span>
12. <span data-ttu-id="6dc51-184">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Код: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="6dc51-185">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Имя: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="6dc51-186">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-186">Click Bind.</span></span>
15. <span data-ttu-id="6dc51-187">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="6dc51-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="6dc51-188">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="6dc51-189">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-189">Click Bind.</span></span>
18. <span data-ttu-id="6dc51-190">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Кр: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="6dc51-191">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Кредит: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="6dc51-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="6dc51-192">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-192">Click Bind.</span></span>
21. <span data-ttu-id="6dc51-193">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дб: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="6dc51-194">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дебет: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="6dc51-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="6dc51-195">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-195">Click Bind.</span></span>
24. <span data-ttu-id="6dc51-196">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Валюта: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="6dc51-197">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Валюта: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="6dc51-198">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-198">Click Bind.</span></span>
27. <span data-ttu-id="6dc51-199">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дата: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="6dc51-200">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дата: дата".</span><span class="sxs-lookup"><span data-stu-id="6dc51-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="6dc51-201">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-201">Click Bind.</span></span>
30. <span data-ttu-id="6dc51-202">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Ваучер: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="6dc51-203">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Ваучер: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="6dc51-204">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-204">Click Bind.</span></span>
33. <span data-ttu-id="6dc51-205">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="6dc51-206">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="6dc51-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="6dc51-207">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-207">Click Bind.</span></span>
36. <span data-ttu-id="6dc51-208">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Партия: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="6dc51-209">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Партия: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="6dc51-210">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-210">Click Bind.</span></span>
39. <span data-ttu-id="6dc51-211">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="6dc51-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="6dc51-212">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="6dc51-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="6dc51-213">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-213">Click Bind.</span></span>
42. <span data-ttu-id="6dc51-214">В дереве выберите "Корень: XML-элемент\Компания: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="6dc51-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="6dc51-215">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Компания: строка".</span><span class="sxs-lookup"><span data-stu-id="6dc51-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="6dc51-216">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="6dc51-216">Click Bind.</span></span>
45. <span data-ttu-id="6dc51-217">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="6dc51-217">Click Save.</span></span>
46. <span data-ttu-id="6dc51-218">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6dc51-218">Close the page.</span></span>
<span data-ttu-id="6dc51-219">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="6dc51-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

