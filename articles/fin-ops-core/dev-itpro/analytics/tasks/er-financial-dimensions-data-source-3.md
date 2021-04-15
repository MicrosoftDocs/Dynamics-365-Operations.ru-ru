---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 3)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752420"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="8a94b-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)</span><span class="sxs-lookup"><span data-stu-id="8a94b-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a94b-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="8a94b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="8a94b-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="8a94b-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="8a94b-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)".</span><span class="sxs-lookup"><span data-stu-id="8a94b-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="8a94b-108">Разработка отчета для представления финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="8a94b-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="8a94b-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="8a94b-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8a94b-110">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="8a94b-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8a94b-111">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8a94b-112">В поле "Создать" введите "Формат, основанный на модели данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="8a94b-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="8a94b-113">Используйте модель, которая была создана заранее как источник данных для нового отчета.</span><span class="sxs-lookup"><span data-stu-id="8a94b-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="8a94b-114">В поле "Имя" введите "Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="8a94b-115">В поле "Определение модели данных" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="8a94b-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="8a94b-116">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="8a94b-116">Click Create configuration.</span></span>
8. <span data-ttu-id="8a94b-117">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="8a94b-117">Click Designer.</span></span>
9. <span data-ttu-id="8a94b-118">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="8a94b-119">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="8a94b-120">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="8a94b-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="8a94b-121">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8a94b-121">Click OK.</span></span>
13. <span data-ttu-id="8a94b-122">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="8a94b-123">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="8a94b-124">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="8a94b-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="8a94b-125">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8a94b-125">Click OK.</span></span>
17. <span data-ttu-id="8a94b-126">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="8a94b-127">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="8a94b-128">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="8a94b-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="8a94b-129">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8a94b-129">Click OK.</span></span>
21. <span data-ttu-id="8a94b-130">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="8a94b-131">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="8a94b-132">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="8a94b-133">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="8a94b-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="8a94b-134">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8a94b-134">Click OK.</span></span>
26. <span data-ttu-id="8a94b-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="8a94b-136">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="8a94b-137">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="8a94b-138">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8a94b-138">Click OK.</span></span>
30. <span data-ttu-id="8a94b-139">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="8a94b-140">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="8a94b-141">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="8a94b-142">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="8a94b-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="8a94b-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-143">Click OK.</span></span>
35. <span data-ttu-id="8a94b-144">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="8a94b-145">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="8a94b-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="8a94b-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-146">Click OK.</span></span>
38. <span data-ttu-id="8a94b-147">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="8a94b-148">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="8a94b-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="8a94b-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-149">Click OK.</span></span>
41. <span data-ttu-id="8a94b-150">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="8a94b-151">В поле "Имя" введите "Дб".</span><span class="sxs-lookup"><span data-stu-id="8a94b-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="8a94b-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-152">Click OK.</span></span>
44. <span data-ttu-id="8a94b-153">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="8a94b-154">В поле "Имя" введите "Кр".</span><span class="sxs-lookup"><span data-stu-id="8a94b-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="8a94b-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-155">Click OK.</span></span>
47. <span data-ttu-id="8a94b-156">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="8a94b-157">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="8a94b-158">В поле "Имя" введите "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="8a94b-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="8a94b-159">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8a94b-159">Click OK.</span></span>
51. <span data-ttu-id="8a94b-160">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="8a94b-161">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a94b-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="8a94b-162">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="8a94b-163">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="8a94b-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="8a94b-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-164">Click OK.</span></span>
56. <span data-ttu-id="8a94b-165">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="8a94b-166">В поле "Имя" введите "Значение".</span><span class="sxs-lookup"><span data-stu-id="8a94b-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="8a94b-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-167">Click OK.</span></span>
59. <span data-ttu-id="8a94b-168">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="8a94b-169">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="8a94b-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="8a94b-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a94b-170">Click OK.</span></span>
<span data-ttu-id="8a94b-171">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="8a94b-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="8a94b-172">Сопоставление элементов отчета с источниками данных</span><span class="sxs-lookup"><span data-stu-id="8a94b-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="8a94b-173">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="8a94b-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8a94b-174">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="8a94b-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8a94b-175">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="8a94b-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="8a94b-176">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="8a94b-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="8a94b-177">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="8a94b-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="8a94b-178">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Описание: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="8a94b-179">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Описание: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="8a94b-180">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-180">Click Bind.</span></span>
9. <span data-ttu-id="8a94b-181">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Значение: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="8a94b-182">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Код: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="8a94b-183">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-183">Click Bind.</span></span>
12. <span data-ttu-id="8a94b-184">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Код: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="8a94b-185">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Имя: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="8a94b-186">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-186">Click Bind.</span></span>
15. <span data-ttu-id="8a94b-187">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="8a94b-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="8a94b-188">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="8a94b-189">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-189">Click Bind.</span></span>
18. <span data-ttu-id="8a94b-190">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Кр: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="8a94b-191">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Кредит: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="8a94b-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="8a94b-192">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-192">Click Bind.</span></span>
21. <span data-ttu-id="8a94b-193">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дб: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="8a94b-194">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дебет: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="8a94b-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="8a94b-195">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-195">Click Bind.</span></span>
24. <span data-ttu-id="8a94b-196">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Валюта: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="8a94b-197">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Валюта: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="8a94b-198">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-198">Click Bind.</span></span>
27. <span data-ttu-id="8a94b-199">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дата: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="8a94b-200">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дата: дата".</span><span class="sxs-lookup"><span data-stu-id="8a94b-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="8a94b-201">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-201">Click Bind.</span></span>
30. <span data-ttu-id="8a94b-202">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Ваучер: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="8a94b-203">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Ваучер: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="8a94b-204">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-204">Click Bind.</span></span>
33. <span data-ttu-id="8a94b-205">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="8a94b-206">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="8a94b-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="8a94b-207">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-207">Click Bind.</span></span>
36. <span data-ttu-id="8a94b-208">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Партия: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="8a94b-209">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Партия: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="8a94b-210">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-210">Click Bind.</span></span>
39. <span data-ttu-id="8a94b-211">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="8a94b-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="8a94b-212">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="8a94b-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="8a94b-213">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-213">Click Bind.</span></span>
42. <span data-ttu-id="8a94b-214">В дереве выберите "Корень: XML-элемент\Компания: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="8a94b-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="8a94b-215">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Компания: строка".</span><span class="sxs-lookup"><span data-stu-id="8a94b-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="8a94b-216">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8a94b-216">Click Bind.</span></span>
45. <span data-ttu-id="8a94b-217">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="8a94b-217">Click Save.</span></span>
46. <span data-ttu-id="8a94b-218">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8a94b-218">Close the page.</span></span>
<span data-ttu-id="8a94b-219">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="8a94b-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]