---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570200"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="b5fd1-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)</span><span class="sxs-lookup"><span data-stu-id="b5fd1-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5fd1-105">В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b5fd1-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="b5fd1-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="b5fd1-108">Создание новой модели данных</span><span class="sxs-lookup"><span data-stu-id="b5fd1-108">Create a new data model</span></span>
1. <span data-ttu-id="b5fd1-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b5fd1-110">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="b5fd1-111">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="b5fd1-112">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b5fd1-113">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="b5fd1-114">В поле "Имя" введите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="b5fd1-115">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-115">Click Create configuration.</span></span>
6. <span data-ttu-id="b5fd1-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-116">Click Designer.</span></span>
7. <span data-ttu-id="b5fd1-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b5fd1-118">В поле "Имя" введите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="b5fd1-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-119">Click Add.</span></span>
10. <span data-ttu-id="b5fd1-120">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b5fd1-121">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="b5fd1-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-122">Click Add.</span></span>
    * <span data-ttu-id="b5fd1-123">Мы добавим к нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-123">We will add to our model a new record list.</span></span> <span data-ttu-id="b5fd1-124">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) настройки выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="b5fd1-125">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими настройку аналитики.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="b5fd1-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b5fd1-127">В поле "Имя" введите "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="b5fd1-128">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="b5fd1-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-129">Click Add.</span></span>
17. <span data-ttu-id="b5fd1-130">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="b5fd1-131">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="b5fd1-132">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="b5fd1-133">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-133">Click Add.</span></span>
21. <span data-ttu-id="b5fd1-134">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b5fd1-135">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="b5fd1-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-136">Click Add.</span></span>
24. <span data-ttu-id="b5fd1-137">В дереве выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="b5fd1-138">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="b5fd1-139">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="b5fd1-140">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="b5fd1-141">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-141">Click Add.</span></span>
29. <span data-ttu-id="b5fd1-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="b5fd1-143">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="b5fd1-144">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="b5fd1-145">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-145">Click Add.</span></span>
33. <span data-ttu-id="b5fd1-146">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="b5fd1-147">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="b5fd1-148">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="b5fd1-149">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-149">Click Add.</span></span>
37. <span data-ttu-id="b5fd1-150">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="b5fd1-151">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="b5fd1-152">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="b5fd1-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-153">Click Add.</span></span>
41. <span data-ttu-id="b5fd1-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b5fd1-155">В поле "Имя" введите "Дебет".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="b5fd1-156">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="b5fd1-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-157">Click Add.</span></span>
45. <span data-ttu-id="b5fd1-158">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b5fd1-159">В поле "Имя" введите "Кредит".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="b5fd1-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-160">Click Add.</span></span>
48. <span data-ttu-id="b5fd1-161">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="b5fd1-162">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="b5fd1-163">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="b5fd1-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-164">Click Add.</span></span>
52. <span data-ttu-id="b5fd1-165">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="b5fd1-166">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="b5fd1-167">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-167">Click Add.</span></span>
55. <span data-ttu-id="b5fd1-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="b5fd1-169">В поле "Имя" введите "Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="b5fd1-170">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="b5fd1-171">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-171">Click Add.</span></span>
    * <span data-ttu-id="b5fd1-172">Мы добавили в нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-172">We added to our model a new record list.</span></span> <span data-ttu-id="b5fd1-173">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) значения выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="b5fd1-174">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="b5fd1-175">Имя аналитики также будет представлено в этой записи в виде поле, которое будет использоваться, если это необходимо, для целей выбора.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="b5fd1-176">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b5fd1-177">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="b5fd1-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b5fd1-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-179">Click Add.</span></span>
63. <span data-ttu-id="b5fd1-180">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="b5fd1-181">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="b5fd1-182">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-182">Click Add.</span></span>
66. <span data-ttu-id="b5fd1-183">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="b5fd1-184">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="b5fd1-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="b5fd1-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-185">Click Add.</span></span>
69. <span data-ttu-id="b5fd1-186">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-186">Click Save.</span></span>
70. <span data-ttu-id="b5fd1-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b5fd1-187">Close the page.</span></span>

![Страница конструктора модели данных ER](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]