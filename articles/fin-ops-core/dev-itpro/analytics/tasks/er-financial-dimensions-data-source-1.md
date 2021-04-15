---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 1)
author: NickSelin
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
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752468"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="45557-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)</span><span class="sxs-lookup"><span data-stu-id="45557-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45557-105">В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="45557-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="45557-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="45557-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="45557-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="45557-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="45557-108">Создание новой модели данных</span><span class="sxs-lookup"><span data-stu-id="45557-108">Create a new data model</span></span>
1. <span data-ttu-id="45557-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="45557-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="45557-110">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="45557-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="45557-111">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="45557-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="45557-112">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="45557-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="45557-113">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="45557-114">В поле "Имя" введите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="45557-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="45557-115">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="45557-115">Click Create configuration.</span></span>
6. <span data-ttu-id="45557-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="45557-116">Click Designer.</span></span>
7. <span data-ttu-id="45557-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="45557-118">В поле "Имя" введите "Запись".</span><span class="sxs-lookup"><span data-stu-id="45557-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="45557-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-119">Click Add.</span></span>
10. <span data-ttu-id="45557-120">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="45557-121">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="45557-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="45557-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-122">Click Add.</span></span>
    * <span data-ttu-id="45557-123">Мы добавим к нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="45557-123">We will add to our model a new record list.</span></span> <span data-ttu-id="45557-124">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) настройки выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="45557-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="45557-125">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими настройку аналитики.</span><span class="sxs-lookup"><span data-stu-id="45557-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="45557-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="45557-127">В поле "Имя" введите "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="45557-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="45557-128">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="45557-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="45557-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-129">Click Add.</span></span>
17. <span data-ttu-id="45557-130">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="45557-131">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="45557-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="45557-132">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="45557-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="45557-133">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-133">Click Add.</span></span>
21. <span data-ttu-id="45557-134">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="45557-135">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="45557-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="45557-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-136">Click Add.</span></span>
24. <span data-ttu-id="45557-137">В дереве выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="45557-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="45557-138">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="45557-139">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="45557-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="45557-140">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="45557-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="45557-141">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-141">Click Add.</span></span>
29. <span data-ttu-id="45557-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="45557-143">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="45557-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="45557-144">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="45557-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="45557-145">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-145">Click Add.</span></span>
33. <span data-ttu-id="45557-146">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="45557-147">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="45557-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="45557-148">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="45557-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="45557-149">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-149">Click Add.</span></span>
37. <span data-ttu-id="45557-150">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="45557-151">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="45557-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="45557-152">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="45557-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="45557-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-153">Click Add.</span></span>
41. <span data-ttu-id="45557-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="45557-155">В поле "Имя" введите "Дебет".</span><span class="sxs-lookup"><span data-stu-id="45557-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="45557-156">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="45557-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="45557-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-157">Click Add.</span></span>
45. <span data-ttu-id="45557-158">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="45557-159">В поле "Имя" введите "Кредит".</span><span class="sxs-lookup"><span data-stu-id="45557-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="45557-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-160">Click Add.</span></span>
48. <span data-ttu-id="45557-161">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="45557-162">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="45557-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="45557-163">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="45557-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="45557-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-164">Click Add.</span></span>
52. <span data-ttu-id="45557-165">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="45557-166">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="45557-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="45557-167">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-167">Click Add.</span></span>
55. <span data-ttu-id="45557-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="45557-169">В поле "Имя" введите "Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="45557-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="45557-170">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="45557-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="45557-171">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-171">Click Add.</span></span>
    * <span data-ttu-id="45557-172">Мы добавили в нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="45557-172">We added to our model a new record list.</span></span> <span data-ttu-id="45557-173">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) значения выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="45557-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="45557-174">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="45557-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="45557-175">Имя аналитики также будет представлено в этой записи в виде поле, которое будет использоваться, если это необходимо, для целей выбора.</span><span class="sxs-lookup"><span data-stu-id="45557-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="45557-176">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="45557-177">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="45557-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="45557-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="45557-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="45557-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-179">Click Add.</span></span>
63. <span data-ttu-id="45557-180">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="45557-181">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="45557-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="45557-182">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-182">Click Add.</span></span>
66. <span data-ttu-id="45557-183">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45557-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="45557-184">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="45557-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="45557-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45557-185">Click Add.</span></span>
69. <span data-ttu-id="45557-186">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="45557-186">Click Save.</span></span>
70. <span data-ttu-id="45557-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45557-187">Close the page.</span></span>

![Страница конструктора модели данных ER](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]