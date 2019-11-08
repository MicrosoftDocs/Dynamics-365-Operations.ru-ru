---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77f1f2d6390a1d99b22d6eab9f0cae30f9760cc8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550587"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="b693c-103">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)</span><span class="sxs-lookup"><span data-stu-id="b693c-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b693c-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="b693c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b693c-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="b693c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b693c-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)".</span><span class="sxs-lookup"><span data-stu-id="b693c-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="b693c-107">Разработка отчета для представления финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="b693c-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="b693c-108">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="b693c-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b693c-109">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="b693c-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b693c-110">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="b693c-111">В поле "Создать" введите "Формат, основанный на модели данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="b693c-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="b693c-112">Используйте модель, которая была создана заранее как источник данных для нового отчета.</span><span class="sxs-lookup"><span data-stu-id="b693c-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="b693c-113">В поле "Имя" введите "Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="b693c-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="b693c-114">В поле "Определение модели данных" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b693c-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="b693c-115">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b693c-115">Click Create configuration.</span></span>
8. <span data-ttu-id="b693c-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b693c-116">Click Designer.</span></span>
9. <span data-ttu-id="b693c-117">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="b693c-118">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="b693c-119">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="b693c-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="b693c-120">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b693c-120">Click OK.</span></span>
13. <span data-ttu-id="b693c-121">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="b693c-122">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="b693c-123">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="b693c-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="b693c-124">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b693c-124">Click OK.</span></span>
17. <span data-ttu-id="b693c-125">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="b693c-126">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="b693c-127">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="b693c-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="b693c-128">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b693c-128">Click OK.</span></span>
21. <span data-ttu-id="b693c-129">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="b693c-130">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="b693c-131">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="b693c-132">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="b693c-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="b693c-133">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b693c-133">Click OK.</span></span>
26. <span data-ttu-id="b693c-134">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="b693c-135">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="b693c-136">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="b693c-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="b693c-137">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b693c-137">Click OK.</span></span>
30. <span data-ttu-id="b693c-138">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="b693c-139">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="b693c-140">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="b693c-141">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="b693c-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="b693c-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-142">Click OK.</span></span>
35. <span data-ttu-id="b693c-143">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="b693c-144">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="b693c-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="b693c-145">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-145">Click OK.</span></span>
38. <span data-ttu-id="b693c-146">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="b693c-147">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="b693c-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="b693c-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-148">Click OK.</span></span>
41. <span data-ttu-id="b693c-149">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="b693c-150">В поле "Имя" введите "Дб".</span><span class="sxs-lookup"><span data-stu-id="b693c-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="b693c-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-151">Click OK.</span></span>
44. <span data-ttu-id="b693c-152">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="b693c-153">В поле "Имя" введите "Кр".</span><span class="sxs-lookup"><span data-stu-id="b693c-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="b693c-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-154">Click OK.</span></span>
47. <span data-ttu-id="b693c-155">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="b693c-156">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="b693c-157">В поле "Имя" введите "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="b693c-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="b693c-158">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b693c-158">Click OK.</span></span>
51. <span data-ttu-id="b693c-159">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="b693c-160">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b693c-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="b693c-161">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="b693c-162">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="b693c-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="b693c-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-163">Click OK.</span></span>
56. <span data-ttu-id="b693c-164">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="b693c-165">В поле "Имя" введите "Значение".</span><span class="sxs-lookup"><span data-stu-id="b693c-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="b693c-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-166">Click OK.</span></span>
59. <span data-ttu-id="b693c-167">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="b693c-168">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="b693c-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="b693c-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b693c-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="b693c-170">Сопоставление элементов отчета с источниками данных</span><span class="sxs-lookup"><span data-stu-id="b693c-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="b693c-171">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="b693c-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="b693c-172">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="b693c-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b693c-173">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="b693c-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="b693c-174">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="b693c-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="b693c-175">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="b693c-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="b693c-176">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Описание: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="b693c-177">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Описание: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="b693c-178">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-178">Click Bind.</span></span>
9. <span data-ttu-id="b693c-179">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Значение: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="b693c-180">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Код: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="b693c-181">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-181">Click Bind.</span></span>
12. <span data-ttu-id="b693c-182">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Код: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="b693c-183">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Имя: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="b693c-184">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-184">Click Bind.</span></span>
15. <span data-ttu-id="b693c-185">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="b693c-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="b693c-186">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="b693c-187">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-187">Click Bind.</span></span>
18. <span data-ttu-id="b693c-188">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Кр: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="b693c-189">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Кредит: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="b693c-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="b693c-190">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-190">Click Bind.</span></span>
21. <span data-ttu-id="b693c-191">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дб: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="b693c-192">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дебет: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="b693c-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="b693c-193">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-193">Click Bind.</span></span>
24. <span data-ttu-id="b693c-194">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Валюта: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="b693c-195">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Валюта: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="b693c-196">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-196">Click Bind.</span></span>
27. <span data-ttu-id="b693c-197">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дата: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="b693c-198">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дата: дата".</span><span class="sxs-lookup"><span data-stu-id="b693c-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="b693c-199">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-199">Click Bind.</span></span>
30. <span data-ttu-id="b693c-200">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Ваучер: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="b693c-201">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Ваучер: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="b693c-202">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-202">Click Bind.</span></span>
33. <span data-ttu-id="b693c-203">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="b693c-204">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="b693c-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="b693c-205">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-205">Click Bind.</span></span>
36. <span data-ttu-id="b693c-206">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Партия: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="b693c-207">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Партия: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="b693c-208">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-208">Click Bind.</span></span>
39. <span data-ttu-id="b693c-209">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="b693c-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="b693c-210">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="b693c-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="b693c-211">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-211">Click Bind.</span></span>
42. <span data-ttu-id="b693c-212">В дереве выберите "Корень: XML-элемент\Компания: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="b693c-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="b693c-213">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Компания: строка".</span><span class="sxs-lookup"><span data-stu-id="b693c-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="b693c-214">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="b693c-214">Click Bind.</span></span>
45. <span data-ttu-id="b693c-215">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b693c-215">Click Save.</span></span>
46. <span data-ttu-id="b693c-216">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b693c-216">Close the page.</span></span>

