--- 
title: "Разработка отчетов для использования финансовых аналитик как источников данных"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="a64d6-103">Разработка отчетов для использования финансовых аналитик как источников данных</span><span class="sxs-lookup"><span data-stu-id="a64d6-103">Design reports to use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a64d6-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a64d6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a64d6-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="a64d6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a64d6-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)".</span><span class="sxs-lookup"><span data-stu-id="a64d6-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a64d6-107">Разработка отчета для представления финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="a64d6-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a64d6-108">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="a64d6-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a64d6-109">В дереве выберите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="a64d6-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a64d6-110">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a64d6-111">В поле "Создать" введите "Формат, основанный на модели данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="a64d6-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a64d6-112">Используйте модель, которая была создана заранее как источник данных для нового отчета.</span><span class="sxs-lookup"><span data-stu-id="a64d6-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a64d6-113">В поле "Имя" введите "Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a64d6-114">В поле "Определение модели данных" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="a64d6-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a64d6-115">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a64d6-115">Click Create configuration.</span></span>
8. <span data-ttu-id="a64d6-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="a64d6-116">Click Designer.</span></span>
9. <span data-ttu-id="a64d6-117">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a64d6-118">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a64d6-119">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="a64d6-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a64d6-120">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a64d6-120">Click OK.</span></span>
13. <span data-ttu-id="a64d6-121">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a64d6-122">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a64d6-123">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="a64d6-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a64d6-124">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a64d6-124">Click OK.</span></span>
17. <span data-ttu-id="a64d6-125">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a64d6-126">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a64d6-127">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="a64d6-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a64d6-128">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a64d6-128">Click OK.</span></span>
21. <span data-ttu-id="a64d6-129">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a64d6-130">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a64d6-131">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a64d6-132">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="a64d6-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a64d6-133">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a64d6-133">Click OK.</span></span>
26. <span data-ttu-id="a64d6-134">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a64d6-135">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a64d6-136">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a64d6-137">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a64d6-137">Click OK.</span></span>
30. <span data-ttu-id="a64d6-138">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a64d6-139">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a64d6-140">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a64d6-141">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="a64d6-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a64d6-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-142">Click OK.</span></span>
35. <span data-ttu-id="a64d6-143">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="a64d6-144">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="a64d6-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a64d6-145">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-145">Click OK.</span></span>
38. <span data-ttu-id="a64d6-146">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="a64d6-147">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="a64d6-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a64d6-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-148">Click OK.</span></span>
41. <span data-ttu-id="a64d6-149">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="a64d6-150">В поле "Имя" введите "Дб".</span><span class="sxs-lookup"><span data-stu-id="a64d6-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a64d6-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-151">Click OK.</span></span>
44. <span data-ttu-id="a64d6-152">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="a64d6-153">В поле "Имя" введите "Кр".</span><span class="sxs-lookup"><span data-stu-id="a64d6-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a64d6-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-154">Click OK.</span></span>
47. <span data-ttu-id="a64d6-155">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a64d6-156">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a64d6-157">В поле "Имя" введите "Аналитики".</span><span class="sxs-lookup"><span data-stu-id="a64d6-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a64d6-158">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a64d6-158">Click OK.</span></span>
51. <span data-ttu-id="a64d6-159">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a64d6-160">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a64d6-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a64d6-161">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a64d6-162">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="a64d6-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a64d6-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-163">Click OK.</span></span>
56. <span data-ttu-id="a64d6-164">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="a64d6-165">В поле "Имя" введите "Значение".</span><span class="sxs-lookup"><span data-stu-id="a64d6-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a64d6-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-166">Click OK.</span></span>
59. <span data-ttu-id="a64d6-167">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="a64d6-168">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="a64d6-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a64d6-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a64d6-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a64d6-170">Сопоставление элементов отчета с источниками данных</span><span class="sxs-lookup"><span data-stu-id="a64d6-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="a64d6-171">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a64d6-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a64d6-172">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="a64d6-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a64d6-173">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="a64d6-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a64d6-174">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="a64d6-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a64d6-175">В дереве разверните узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="a64d6-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a64d6-176">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Описание: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a64d6-177">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Описание: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a64d6-178">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-178">Click Bind.</span></span>
9. <span data-ttu-id="a64d6-179">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Значение: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a64d6-180">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Код: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a64d6-181">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-181">Click Bind.</span></span>
12. <span data-ttu-id="a64d6-182">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент\Код: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a64d6-183">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей\Имя: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a64d6-184">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-184">Click Bind.</span></span>
15. <span data-ttu-id="a64d6-185">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Данные аналитик: список записей".</span><span class="sxs-lookup"><span data-stu-id="a64d6-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a64d6-186">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Аналитики: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a64d6-187">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-187">Click Bind.</span></span>
18. <span data-ttu-id="a64d6-188">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Кр: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a64d6-189">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Кредит: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="a64d6-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a64d6-190">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-190">Click Bind.</span></span>
21. <span data-ttu-id="a64d6-191">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дб: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a64d6-192">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дебет: вещественное число".</span><span class="sxs-lookup"><span data-stu-id="a64d6-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a64d6-193">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-193">Click Bind.</span></span>
24. <span data-ttu-id="a64d6-194">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Валюта: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a64d6-195">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Валюта: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a64d6-196">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-196">Click Bind.</span></span>
27. <span data-ttu-id="a64d6-197">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Дата: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a64d6-198">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Дата: дата".</span><span class="sxs-lookup"><span data-stu-id="a64d6-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a64d6-199">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-199">Click Bind.</span></span>
30. <span data-ttu-id="a64d6-200">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент\Ваучер: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a64d6-201">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей\Ваучер: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a64d6-202">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-202">Click Bind.</span></span>
33. <span data-ttu-id="a64d6-203">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Проводка: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a64d6-204">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Проводка: список записей".</span><span class="sxs-lookup"><span data-stu-id="a64d6-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a64d6-205">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-205">Click Bind.</span></span>
36. <span data-ttu-id="a64d6-206">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент\Партия: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a64d6-207">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей\Партия: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a64d6-208">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-208">Click Bind.</span></span>
39. <span data-ttu-id="a64d6-209">В дереве выберите "Корень: XML-элемент\Журнал: XML-элемент".</span><span class="sxs-lookup"><span data-stu-id="a64d6-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a64d6-210">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Журнал: список записей".</span><span class="sxs-lookup"><span data-stu-id="a64d6-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a64d6-211">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-211">Click Bind.</span></span>
42. <span data-ttu-id="a64d6-212">В дереве выберите "Корень: XML-элемент\Компания: XML-атрибут".</span><span class="sxs-lookup"><span data-stu-id="a64d6-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a64d6-213">В дереве выберите узел "модель: модель данных примера модели финансовых аналитик\Компания: строка".</span><span class="sxs-lookup"><span data-stu-id="a64d6-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a64d6-214">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a64d6-214">Click Bind.</span></span>
45. <span data-ttu-id="a64d6-215">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a64d6-215">Click Save.</span></span>
46. <span data-ttu-id="a64d6-216">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a64d6-216">Close the page.</span></span>


