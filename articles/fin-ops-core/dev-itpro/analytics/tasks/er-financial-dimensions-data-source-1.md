---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 1)
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
ms.openlocfilehash: 92d29d954debddd509eaba6b710f39b218da2c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092183"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="f90b4-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Разработка модели данных)</span><span class="sxs-lookup"><span data-stu-id="f90b4-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f90b4-105">В следующих шагах поясняется, как системный администратор или разработчик электронной отчетности может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f90b4-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f90b4-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="f90b4-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f90b4-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="f90b4-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="f90b4-108">Создание новой модели данных</span><span class="sxs-lookup"><span data-stu-id="f90b4-108">Create a new data model</span></span>
1. <span data-ttu-id="f90b4-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="f90b4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f90b4-110">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f90b4-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="f90b4-111">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="f90b4-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f90b4-112">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="f90b4-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f90b4-113">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f90b4-114">В поле "Имя" введите "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="f90b4-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="f90b4-115">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f90b4-115">Click Create configuration.</span></span>
6. <span data-ttu-id="f90b4-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="f90b4-116">Click Designer.</span></span>
7. <span data-ttu-id="f90b4-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="f90b4-118">В поле "Имя" введите "Запись".</span><span class="sxs-lookup"><span data-stu-id="f90b4-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="f90b4-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-119">Click Add.</span></span>
10. <span data-ttu-id="f90b4-120">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="f90b4-121">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="f90b4-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="f90b4-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-122">Click Add.</span></span>
    * <span data-ttu-id="f90b4-123">Мы добавим к нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="f90b4-123">We will add to our model a new record list.</span></span> <span data-ttu-id="f90b4-124">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) настройки выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="f90b4-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="f90b4-125">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими настройку аналитики.</span><span class="sxs-lookup"><span data-stu-id="f90b4-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="f90b4-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="f90b4-127">В поле "Имя" введите "Настройка аналитик".</span><span class="sxs-lookup"><span data-stu-id="f90b4-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="f90b4-128">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="f90b4-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="f90b4-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-129">Click Add.</span></span>
17. <span data-ttu-id="f90b4-130">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="f90b4-131">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="f90b4-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="f90b4-132">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="f90b4-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="f90b4-133">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-133">Click Add.</span></span>
21. <span data-ttu-id="f90b4-134">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="f90b4-135">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="f90b4-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="f90b4-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-136">Click Add.</span></span>
24. <span data-ttu-id="f90b4-137">В дереве выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="f90b4-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="f90b4-138">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="f90b4-139">В поле "Имя" введите "Журнал".</span><span class="sxs-lookup"><span data-stu-id="f90b4-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="f90b4-140">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="f90b4-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="f90b4-141">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-141">Click Add.</span></span>
29. <span data-ttu-id="f90b4-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="f90b4-143">В поле "Имя" введите "Партия".</span><span class="sxs-lookup"><span data-stu-id="f90b4-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="f90b4-144">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="f90b4-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="f90b4-145">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-145">Click Add.</span></span>
33. <span data-ttu-id="f90b4-146">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="f90b4-147">В поле "Имя" введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="f90b4-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="f90b4-148">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="f90b4-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="f90b4-149">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-149">Click Add.</span></span>
37. <span data-ttu-id="f90b4-150">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="f90b4-151">В поле "Имя" введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="f90b4-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="f90b4-152">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="f90b4-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="f90b4-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-153">Click Add.</span></span>
41. <span data-ttu-id="f90b4-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="f90b4-155">В поле "Имя" введите "Дебет".</span><span class="sxs-lookup"><span data-stu-id="f90b4-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="f90b4-156">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="f90b4-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="f90b4-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-157">Click Add.</span></span>
45. <span data-ttu-id="f90b4-158">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="f90b4-159">В поле "Имя" введите "Кредит".</span><span class="sxs-lookup"><span data-stu-id="f90b4-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="f90b4-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-160">Click Add.</span></span>
48. <span data-ttu-id="f90b4-161">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="f90b4-162">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="f90b4-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="f90b4-163">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="f90b4-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="f90b4-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-164">Click Add.</span></span>
52. <span data-ttu-id="f90b4-165">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="f90b4-166">В поле "Имя" введите "Ваучер".</span><span class="sxs-lookup"><span data-stu-id="f90b4-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="f90b4-167">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-167">Click Add.</span></span>
55. <span data-ttu-id="f90b4-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="f90b4-169">В поле "Имя" введите "Данные аналитик".</span><span class="sxs-lookup"><span data-stu-id="f90b4-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="f90b4-170">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="f90b4-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="f90b4-171">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-171">Click Add.</span></span>
    * <span data-ttu-id="f90b4-172">Мы добавили в нашу модель новый список записей.</span><span class="sxs-lookup"><span data-stu-id="f90b4-172">We added to our model a new record list.</span></span> <span data-ttu-id="f90b4-173">Этот список будет показывать (для любых отчетов электронной отчетности, которые используют эту модель в качестве источника данных) значения выбранных финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="f90b4-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="f90b4-174">Каждая финансовая аналитика в этом списке будет представлена как запись с соответствующими полями, представляющими значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="f90b4-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="f90b4-175">Имя аналитики также будет представлено в этой записи в виде поле, которое будет использоваться, если это необходимо, для целей выбора.</span><span class="sxs-lookup"><span data-stu-id="f90b4-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="f90b4-176">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="f90b4-177">В поле "Имя" введите "Код".</span><span class="sxs-lookup"><span data-stu-id="f90b4-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="f90b4-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="f90b4-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="f90b4-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-179">Click Add.</span></span>
63. <span data-ttu-id="f90b4-180">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="f90b4-181">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="f90b4-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="f90b4-182">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-182">Click Add.</span></span>
66. <span data-ttu-id="f90b4-183">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f90b4-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="f90b4-184">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="f90b4-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="f90b4-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-185">Click Add.</span></span>
69. <span data-ttu-id="f90b4-186">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="f90b4-186">Click Save.</span></span>
70. <span data-ttu-id="f90b4-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f90b4-187">Close the page.</span></span>

![Страница конструктора модели данных ER](../media/er-financial-dimensions-guides-data-model.png)

