---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 3)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565246"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="99777-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)</span><span class="sxs-lookup"><span data-stu-id="99777-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99777-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="99777-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="99777-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="99777-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="99777-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)".</span><span class="sxs-lookup"><span data-stu-id="99777-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="99777-108">Разработка отчета для представления финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="99777-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="99777-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="99777-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="99777-110">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="99777-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="99777-111">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="99777-112">В поле "Создать" введите "Формат, основанный на модели данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="99777-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="99777-113">Используйте модель, которая была создана заранее как источник данных для нового отчета.</span><span class="sxs-lookup"><span data-stu-id="99777-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="99777-114">В поле "Имя" введите "Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="99777-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="99777-115">В поле "Определение модели данных" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="99777-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="99777-116">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="99777-116">Click Create configuration.</span></span>
8. <span data-ttu-id="99777-117">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="99777-117">Click Designer.</span></span>
9. <span data-ttu-id="99777-118">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="99777-119">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="99777-120">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="99777-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="99777-121">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="99777-121">Click OK.</span></span>
13. <span data-ttu-id="99777-122">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="99777-123">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="99777-124">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="99777-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="99777-125">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="99777-125">Click OK.</span></span>
17. <span data-ttu-id="99777-126">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="99777-127">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="99777-128">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="99777-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="99777-129">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="99777-129">Click OK.</span></span>
21. <span data-ttu-id="99777-130">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="99777-131">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="99777-132">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="99777-133">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="99777-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="99777-134">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="99777-134">Click OK.</span></span>
26. <span data-ttu-id="99777-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="99777-136">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="99777-137">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="99777-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="99777-138">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="99777-138">Click OK.</span></span>
30. <span data-ttu-id="99777-139">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="99777-140">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="99777-141">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="99777-142">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="99777-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="99777-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-143">Click OK.</span></span>
35. <span data-ttu-id="99777-144">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="99777-145">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="99777-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="99777-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-146">Click OK.</span></span>
38. <span data-ttu-id="99777-147">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="99777-148">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="99777-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="99777-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-149">Click OK.</span></span>
41. <span data-ttu-id="99777-150">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="99777-151">В поле "Имя" введите "Дб".</span><span class="sxs-lookup"><span data-stu-id="99777-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="99777-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-152">Click OK.</span></span>
44. <span data-ttu-id="99777-153">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="99777-154">В поле "Имя" введите "Кр".</span><span class="sxs-lookup"><span data-stu-id="99777-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="99777-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-155">Click OK.</span></span>
47. <span data-ttu-id="99777-156">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="99777-157">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="99777-158">В поле "Имя" введите "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="99777-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="99777-159">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="99777-159">Click OK.</span></span>
51. <span data-ttu-id="99777-160">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="99777-161">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="99777-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="99777-162">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="99777-163">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="99777-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="99777-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-164">Click OK.</span></span>
56. <span data-ttu-id="99777-165">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="99777-166">В поле "Имя" введите "Значение".</span><span class="sxs-lookup"><span data-stu-id="99777-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="99777-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-167">Click OK.</span></span>
59. <span data-ttu-id="99777-168">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="99777-169">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="99777-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="99777-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="99777-170">Click OK.</span></span>
<span data-ttu-id="99777-171">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="99777-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="99777-172">Сопоставление элементов отчета с источниками данных</span><span class="sxs-lookup"><span data-stu-id="99777-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="99777-173">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="99777-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="99777-174">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="99777-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="99777-175">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="99777-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="99777-176">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="99777-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="99777-177">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="99777-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="99777-178">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Описание: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="99777-179">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Описание: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="99777-180">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-180">Click Bind.</span></span>
9. <span data-ttu-id="99777-181">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Значение: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="99777-182">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Код: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="99777-183">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-183">Click Bind.</span></span>
12. <span data-ttu-id="99777-184">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Код: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="99777-185">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Имя: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="99777-186">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-186">Click Bind.</span></span>
15. <span data-ttu-id="99777-187">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="99777-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="99777-188">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="99777-189">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-189">Click Bind.</span></span>
18. <span data-ttu-id="99777-190">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Кр: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="99777-191">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Кредит: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="99777-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="99777-192">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-192">Click Bind.</span></span>
21. <span data-ttu-id="99777-193">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дб: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="99777-194">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дебет: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="99777-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="99777-195">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-195">Click Bind.</span></span>
24. <span data-ttu-id="99777-196">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Валюта: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="99777-197">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Валюта: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="99777-198">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-198">Click Bind.</span></span>
27. <span data-ttu-id="99777-199">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дата: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="99777-200">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дата: дата".</span><span class="sxs-lookup"><span data-stu-id="99777-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="99777-201">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-201">Click Bind.</span></span>
30. <span data-ttu-id="99777-202">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Ваучер: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="99777-203">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Ваучер: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="99777-204">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-204">Click Bind.</span></span>
33. <span data-ttu-id="99777-205">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="99777-206">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="99777-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="99777-207">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-207">Click Bind.</span></span>
36. <span data-ttu-id="99777-208">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Партия: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="99777-209">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Партия: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="99777-210">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-210">Click Bind.</span></span>
39. <span data-ttu-id="99777-211">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="99777-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="99777-212">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="99777-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="99777-213">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-213">Click Bind.</span></span>
42. <span data-ttu-id="99777-214">В дереве выберите "Корень: XML-элемент\Компания: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="99777-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="99777-215">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Компания: строка".</span><span class="sxs-lookup"><span data-stu-id="99777-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="99777-216">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="99777-216">Click Bind.</span></span>
45. <span data-ttu-id="99777-217">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="99777-217">Click Save.</span></span>
46. <span data-ttu-id="99777-218">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="99777-218">Close the page.</span></span>
<span data-ttu-id="99777-219">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="99777-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]