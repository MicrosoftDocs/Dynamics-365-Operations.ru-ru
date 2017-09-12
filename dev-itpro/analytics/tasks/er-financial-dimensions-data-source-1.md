--- 
title: "Разработка модели данных для использования финансовых аналитик как источника данных для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0953ffb3a98d4f2852caecc3a59792698d1c9d9b
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="b95e7-103">Разработка модели данных для использования финансовых аналитик как источника данных для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="b95e7-103">Design data model to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b95e7-104">В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="b95e7-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b95e7-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="b95e7-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b95e7-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="b95e7-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="b95e7-107">Создание новой модели данных</span><span class="sxs-lookup"><span data-stu-id="b95e7-107">Create a new data model</span></span>
1. <span data-ttu-id="b95e7-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="b95e7-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b95e7-109">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b95e7-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="b95e7-110">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="b95e7-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="b95e7-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="b95e7-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b95e7-112">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="b95e7-113">В поле "Имя" введите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="b95e7-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="b95e7-114">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b95e7-114">Click Create configuration.</span></span>
6. <span data-ttu-id="b95e7-115">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b95e7-115">Click Designer.</span></span>
7. <span data-ttu-id="b95e7-116">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b95e7-117">В поле "Имя" введите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b95e7-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="b95e7-118">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-118">Click Add.</span></span>
10. <span data-ttu-id="b95e7-119">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b95e7-120">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="b95e7-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="b95e7-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-121">Click Add.</span></span>
    * <span data-ttu-id="b95e7-122">Мы добавим к нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="b95e7-122">We will add to our model a new record list.</span></span> <span data-ttu-id="b95e7-123">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) настройки выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b95e7-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="b95e7-124">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими настройку аналитики.</span><span class="sxs-lookup"><span data-stu-id="b95e7-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="b95e7-125">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b95e7-126">В поле "Имя" введите "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="b95e7-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="b95e7-127">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b95e7-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="b95e7-128">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-128">Click Add.</span></span>
17. <span data-ttu-id="b95e7-129">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="b95e7-130">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="b95e7-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="b95e7-131">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b95e7-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="b95e7-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-132">Click Add.</span></span>
21. <span data-ttu-id="b95e7-133">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b95e7-134">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="b95e7-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="b95e7-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-135">Click Add.</span></span>
24. <span data-ttu-id="b95e7-136">В дереве выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b95e7-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="b95e7-137">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="b95e7-138">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="b95e7-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="b95e7-139">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b95e7-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="b95e7-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-140">Click Add.</span></span>
29. <span data-ttu-id="b95e7-141">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="b95e7-142">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="b95e7-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="b95e7-143">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b95e7-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="b95e7-144">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-144">Click Add.</span></span>
33. <span data-ttu-id="b95e7-145">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="b95e7-146">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="b95e7-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="b95e7-147">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b95e7-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="b95e7-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-148">Click Add.</span></span>
37. <span data-ttu-id="b95e7-149">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="b95e7-150">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="b95e7-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="b95e7-151">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="b95e7-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="b95e7-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-152">Click Add.</span></span>
41. <span data-ttu-id="b95e7-153">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b95e7-154">В поле "Имя" введите "Дебет".</span><span class="sxs-lookup"><span data-stu-id="b95e7-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="b95e7-155">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="b95e7-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="b95e7-156">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-156">Click Add.</span></span>
45. <span data-ttu-id="b95e7-157">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b95e7-158">В поле "Имя" введите "Кредит".</span><span class="sxs-lookup"><span data-stu-id="b95e7-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="b95e7-159">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-159">Click Add.</span></span>
48. <span data-ttu-id="b95e7-160">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="b95e7-161">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="b95e7-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="b95e7-162">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b95e7-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="b95e7-163">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-163">Click Add.</span></span>
52. <span data-ttu-id="b95e7-164">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="b95e7-165">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="b95e7-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="b95e7-166">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-166">Click Add.</span></span>
55. <span data-ttu-id="b95e7-167">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="b95e7-168">В поле "Имя" введите "Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="b95e7-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="b95e7-169">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b95e7-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="b95e7-170">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-170">Click Add.</span></span>
    * <span data-ttu-id="b95e7-171">Мы добавили в нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="b95e7-171">We added to our model a new record list.</span></span> <span data-ttu-id="b95e7-172">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) значения выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b95e7-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="b95e7-173">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="b95e7-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="b95e7-174">Имя аналитики также будет представлено в этой записи в виде поле, которое будет использоваться, если это необходимо, для целей выбора.</span><span class="sxs-lookup"><span data-stu-id="b95e7-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="b95e7-175">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b95e7-176">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="b95e7-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="b95e7-177">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b95e7-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b95e7-178">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-178">Click Add.</span></span>
63. <span data-ttu-id="b95e7-179">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="b95e7-180">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="b95e7-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="b95e7-181">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-181">Click Add.</span></span>
66. <span data-ttu-id="b95e7-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b95e7-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="b95e7-183">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="b95e7-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="b95e7-184">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b95e7-184">Click Add.</span></span>
69. <span data-ttu-id="b95e7-185">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b95e7-185">Click Save.</span></span>
70. <span data-ttu-id="b95e7-186">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b95e7-186">Close the page.</span></span>


