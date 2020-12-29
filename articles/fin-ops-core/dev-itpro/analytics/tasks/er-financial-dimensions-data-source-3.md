---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.
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
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684795"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="a9b88-103">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)</span><span class="sxs-lookup"><span data-stu-id="a9b88-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9b88-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a9b88-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a9b88-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="a9b88-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a9b88-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)".</span><span class="sxs-lookup"><span data-stu-id="a9b88-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a9b88-107">Разработка отчета для представления финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="a9b88-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a9b88-108">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="a9b88-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a9b88-109">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="a9b88-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a9b88-110">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a9b88-111">В поле "Создать" введите "Формат, основанный на модели данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="a9b88-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a9b88-112">Используйте модель, которая была создана заранее как источник данных для нового отчета.</span><span class="sxs-lookup"><span data-stu-id="a9b88-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a9b88-113">В поле "Имя" введите "Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a9b88-114">В поле "Определение модели данных" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="a9b88-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a9b88-115">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a9b88-115">Click Create configuration.</span></span>
8. <span data-ttu-id="a9b88-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="a9b88-116">Click Designer.</span></span>
9. <span data-ttu-id="a9b88-117">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a9b88-118">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a9b88-119">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="a9b88-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a9b88-120">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a9b88-120">Click OK.</span></span>
13. <span data-ttu-id="a9b88-121">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a9b88-122">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a9b88-123">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="a9b88-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a9b88-124">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a9b88-124">Click OK.</span></span>
17. <span data-ttu-id="a9b88-125">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a9b88-126">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a9b88-127">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="a9b88-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a9b88-128">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a9b88-128">Click OK.</span></span>
21. <span data-ttu-id="a9b88-129">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a9b88-130">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a9b88-131">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a9b88-132">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="a9b88-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a9b88-133">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a9b88-133">Click OK.</span></span>
26. <span data-ttu-id="a9b88-134">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a9b88-135">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a9b88-136">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a9b88-137">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a9b88-137">Click OK.</span></span>
30. <span data-ttu-id="a9b88-138">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a9b88-139">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a9b88-140">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a9b88-141">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="a9b88-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a9b88-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-142">Click OK.</span></span>
35. <span data-ttu-id="a9b88-143">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="a9b88-144">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="a9b88-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a9b88-145">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-145">Click OK.</span></span>
38. <span data-ttu-id="a9b88-146">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="a9b88-147">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="a9b88-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a9b88-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-148">Click OK.</span></span>
41. <span data-ttu-id="a9b88-149">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="a9b88-150">В поле "Имя" введите "Дб".</span><span class="sxs-lookup"><span data-stu-id="a9b88-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a9b88-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-151">Click OK.</span></span>
44. <span data-ttu-id="a9b88-152">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="a9b88-153">В поле "Имя" введите "Кр".</span><span class="sxs-lookup"><span data-stu-id="a9b88-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a9b88-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-154">Click OK.</span></span>
47. <span data-ttu-id="a9b88-155">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a9b88-156">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a9b88-157">В поле "Имя" введите "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="a9b88-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a9b88-158">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a9b88-158">Click OK.</span></span>
51. <span data-ttu-id="a9b88-159">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a9b88-160">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a9b88-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a9b88-161">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a9b88-162">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="a9b88-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a9b88-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-163">Click OK.</span></span>
56. <span data-ttu-id="a9b88-164">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="a9b88-165">В поле "Имя" введите "Значение".</span><span class="sxs-lookup"><span data-stu-id="a9b88-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a9b88-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-166">Click OK.</span></span>
59. <span data-ttu-id="a9b88-167">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="a9b88-168">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="a9b88-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a9b88-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9b88-169">Click OK.</span></span>
<span data-ttu-id="a9b88-170">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="a9b88-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a9b88-171">Сопоставление элементов отчета с источниками данных</span><span class="sxs-lookup"><span data-stu-id="a9b88-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="a9b88-172">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a9b88-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a9b88-173">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="a9b88-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a9b88-174">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="a9b88-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a9b88-175">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="a9b88-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a9b88-176">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="a9b88-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a9b88-177">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Описание: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a9b88-178">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Описание: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a9b88-179">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-179">Click Bind.</span></span>
9. <span data-ttu-id="a9b88-180">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Значение: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a9b88-181">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Код: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a9b88-182">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-182">Click Bind.</span></span>
12. <span data-ttu-id="a9b88-183">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Код: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a9b88-184">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Имя: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a9b88-185">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-185">Click Bind.</span></span>
15. <span data-ttu-id="a9b88-186">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="a9b88-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a9b88-187">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a9b88-188">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-188">Click Bind.</span></span>
18. <span data-ttu-id="a9b88-189">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Кр: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a9b88-190">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Кредит: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="a9b88-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a9b88-191">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-191">Click Bind.</span></span>
21. <span data-ttu-id="a9b88-192">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дб: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a9b88-193">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дебет: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="a9b88-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a9b88-194">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-194">Click Bind.</span></span>
24. <span data-ttu-id="a9b88-195">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Валюта: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a9b88-196">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Валюта: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a9b88-197">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-197">Click Bind.</span></span>
27. <span data-ttu-id="a9b88-198">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дата: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a9b88-199">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дата: дата".</span><span class="sxs-lookup"><span data-stu-id="a9b88-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a9b88-200">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-200">Click Bind.</span></span>
30. <span data-ttu-id="a9b88-201">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Ваучер: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a9b88-202">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Ваучер: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a9b88-203">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-203">Click Bind.</span></span>
33. <span data-ttu-id="a9b88-204">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a9b88-205">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="a9b88-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a9b88-206">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-206">Click Bind.</span></span>
36. <span data-ttu-id="a9b88-207">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Партия: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a9b88-208">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Партия: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a9b88-209">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-209">Click Bind.</span></span>
39. <span data-ttu-id="a9b88-210">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a9b88-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a9b88-211">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="a9b88-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a9b88-212">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-212">Click Bind.</span></span>
42. <span data-ttu-id="a9b88-213">В дереве выберите "Корень: XML-элемент\Компания: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a9b88-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a9b88-214">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Компания: строка".</span><span class="sxs-lookup"><span data-stu-id="a9b88-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a9b88-215">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a9b88-215">Click Bind.</span></span>
45. <span data-ttu-id="a9b88-216">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="a9b88-216">Click Save.</span></span>
46. <span data-ttu-id="a9b88-217">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9b88-217">Close the page.</span></span>
<span data-ttu-id="a9b88-218">![Страница конструктора операций электронной отчетности](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="a9b88-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

