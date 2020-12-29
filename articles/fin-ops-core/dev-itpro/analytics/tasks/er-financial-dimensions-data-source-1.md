---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)
description: В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35c4a05fb15a7e3166c6d075569debcf9cbc3cc3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681717"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="cb257-103">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)</span><span class="sxs-lookup"><span data-stu-id="cb257-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb257-104">В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="cb257-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="cb257-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="cb257-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="cb257-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="cb257-106">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="cb257-107">Создание новой модели данных</span><span class="sxs-lookup"><span data-stu-id="cb257-107">Create a new data model</span></span>
1. <span data-ttu-id="cb257-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="cb257-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="cb257-109">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="cb257-109">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="cb257-110">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="cb257-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="cb257-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="cb257-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="cb257-112">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="cb257-113">В поле "Имя" введите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="cb257-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="cb257-114">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="cb257-114">Click Create configuration.</span></span>
6. <span data-ttu-id="cb257-115">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="cb257-115">Click Designer.</span></span>
7. <span data-ttu-id="cb257-116">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="cb257-117">В поле "Имя" введите "Запись".</span><span class="sxs-lookup"><span data-stu-id="cb257-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="cb257-118">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-118">Click Add.</span></span>
10. <span data-ttu-id="cb257-119">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="cb257-120">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="cb257-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="cb257-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-121">Click Add.</span></span>
    * <span data-ttu-id="cb257-122">Мы добавим к нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="cb257-122">We will add to our model a new record list.</span></span> <span data-ttu-id="cb257-123">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) настройки выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="cb257-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="cb257-124">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими настройку аналитики.</span><span class="sxs-lookup"><span data-stu-id="cb257-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="cb257-125">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="cb257-126">В поле "Имя" введите "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="cb257-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="cb257-127">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="cb257-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="cb257-128">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-128">Click Add.</span></span>
17. <span data-ttu-id="cb257-129">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="cb257-130">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="cb257-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="cb257-131">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="cb257-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="cb257-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-132">Click Add.</span></span>
21. <span data-ttu-id="cb257-133">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="cb257-134">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="cb257-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="cb257-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-135">Click Add.</span></span>
24. <span data-ttu-id="cb257-136">В дереве выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="cb257-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="cb257-137">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="cb257-138">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="cb257-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="cb257-139">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="cb257-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="cb257-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-140">Click Add.</span></span>
29. <span data-ttu-id="cb257-141">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="cb257-142">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="cb257-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="cb257-143">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="cb257-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="cb257-144">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-144">Click Add.</span></span>
33. <span data-ttu-id="cb257-145">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="cb257-146">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="cb257-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="cb257-147">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="cb257-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="cb257-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-148">Click Add.</span></span>
37. <span data-ttu-id="cb257-149">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="cb257-150">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="cb257-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="cb257-151">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="cb257-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="cb257-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-152">Click Add.</span></span>
41. <span data-ttu-id="cb257-153">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="cb257-154">В поле "Имя" введите "Дебет".</span><span class="sxs-lookup"><span data-stu-id="cb257-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="cb257-155">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="cb257-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="cb257-156">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-156">Click Add.</span></span>
45. <span data-ttu-id="cb257-157">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="cb257-158">В поле "Имя" введите "Кредит".</span><span class="sxs-lookup"><span data-stu-id="cb257-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="cb257-159">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-159">Click Add.</span></span>
48. <span data-ttu-id="cb257-160">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="cb257-161">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="cb257-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="cb257-162">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="cb257-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="cb257-163">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-163">Click Add.</span></span>
52. <span data-ttu-id="cb257-164">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="cb257-165">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="cb257-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="cb257-166">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-166">Click Add.</span></span>
55. <span data-ttu-id="cb257-167">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="cb257-168">В поле "Имя" введите "Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="cb257-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="cb257-169">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="cb257-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="cb257-170">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-170">Click Add.</span></span>
    * <span data-ttu-id="cb257-171">Мы добавили в нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="cb257-171">We added to our model a new record list.</span></span> <span data-ttu-id="cb257-172">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) значения выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="cb257-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="cb257-173">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="cb257-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="cb257-174">Имя аналитики также будет представлено в этой записи в виде поле, которое будет использоваться, если это необходимо, для целей выбора.</span><span class="sxs-lookup"><span data-stu-id="cb257-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="cb257-175">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="cb257-176">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="cb257-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="cb257-177">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="cb257-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="cb257-178">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-178">Click Add.</span></span>
63. <span data-ttu-id="cb257-179">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="cb257-180">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="cb257-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="cb257-181">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-181">Click Add.</span></span>
66. <span data-ttu-id="cb257-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb257-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="cb257-183">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="cb257-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="cb257-184">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cb257-184">Click Add.</span></span>
69. <span data-ttu-id="cb257-185">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="cb257-185">Click Save.</span></span>
70. <span data-ttu-id="cb257-186">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cb257-186">Close the page.</span></span>

![Страница конструктора модели данных ER](../media/er-financial-dimensions-guides-data-model.png)

