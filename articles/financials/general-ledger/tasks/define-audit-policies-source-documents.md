--- 
title: "Определение политик аудита для документов-источников"
description: "В этой процедура показано, как настроить и запустить правила политики аудита."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 1bcea6257447cc1d1532f30acc2fb6bb4d524810
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="8125a-103">Определение политик аудита для документов-источников</span><span class="sxs-lookup"><span data-stu-id="8125a-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8125a-104">В этой процедура показано, как настроить и запустить правила политики аудита.</span><span class="sxs-lookup"><span data-stu-id="8125a-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="8125a-105">В этом примере используются отчеты по расходам с типом расходов на проживание в гостинице.</span><span class="sxs-lookup"><span data-stu-id="8125a-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="8125a-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="8125a-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="8125a-107">Роль аудитора содержит правильные разрешения для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="8125a-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="8125a-108">Перейдите в раздел "Рабочее место аудита" > "Настройка" > "Тип правила политики".</span><span class="sxs-lookup"><span data-stu-id="8125a-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="8125a-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8125a-109">Click New.</span></span>
3. <span data-ttu-id="8125a-110">В поле "Правило" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="8125a-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8125a-112">В поле "Имя запроса" выберите строку "Отчет по расходам".</span><span class="sxs-lookup"><span data-stu-id="8125a-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="8125a-113">В поле "Тип запроса" выберите "Агрегировано".</span><span class="sxs-lookup"><span data-stu-id="8125a-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="8125a-114">В поле "Юридическое лицо" выберите "Юридическое лицо".</span><span class="sxs-lookup"><span data-stu-id="8125a-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="8125a-115">В поле "Ссылка на дату документа" выберите "Дата и время изменения".</span><span class="sxs-lookup"><span data-stu-id="8125a-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="8125a-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8125a-116">Click Save.</span></span>
10. <span data-ttu-id="8125a-117">Перейдите в раздел "Рабочее место аудита" > "Настройка" > "Политики аудита".</span><span class="sxs-lookup"><span data-stu-id="8125a-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="8125a-118">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8125a-118">Click New.</span></span>
12. <span data-ttu-id="8125a-119">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="8125a-120">Разверните раздел "Организации политики".</span><span class="sxs-lookup"><span data-stu-id="8125a-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="8125a-121">В дереве выберите "Contoso Entertainment System USA".</span><span class="sxs-lookup"><span data-stu-id="8125a-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="8125a-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-122">Click Add.</span></span>
16. <span data-ttu-id="8125a-123">В дереве выберите "Contoso Consulting USA".</span><span class="sxs-lookup"><span data-stu-id="8125a-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="8125a-124">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-124">Click Add.</span></span>
18. <span data-ttu-id="8125a-125">В дереве выберите "Contoso Retail USA".</span><span class="sxs-lookup"><span data-stu-id="8125a-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="8125a-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-126">Click Add.</span></span>
20. <span data-ttu-id="8125a-127">Сверните раздел "Организации политики".</span><span class="sxs-lookup"><span data-stu-id="8125a-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="8125a-128">Разверните раздел "Правила политики".</span><span class="sxs-lookup"><span data-stu-id="8125a-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="8125a-129">Найдите в списке ранее созданное правило политики и выберите его.</span><span class="sxs-lookup"><span data-stu-id="8125a-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="8125a-130">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="8125a-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="8125a-131">В поле "Действует с" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8125a-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="8125a-132">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="8125a-132">Click Filter.</span></span>
26. <span data-ttu-id="8125a-133">В списке выберите строку для категории расходов и задайте для сведений значение "Гостиница".</span><span class="sxs-lookup"><span data-stu-id="8125a-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="8125a-134">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="8125a-135">Перейдите на вкладку "Агрегировано".</span><span class="sxs-lookup"><span data-stu-id="8125a-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="8125a-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-136">Click Add.</span></span>
30. <span data-ttu-id="8125a-137">В списке выберите значение поля "Сумма проводки".</span><span class="sxs-lookup"><span data-stu-id="8125a-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="8125a-138">В поле "Поле" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="8125a-139">В поле "Функция расчета" выберите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="8125a-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="8125a-140">Перейдите на вкладку "Группа".</span><span class="sxs-lookup"><span data-stu-id="8125a-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="8125a-141">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-141">Click Add.</span></span>
35. <span data-ttu-id="8125a-142">В списке выберите значение "Сотрудник".</span><span class="sxs-lookup"><span data-stu-id="8125a-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="8125a-143">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-143">Click Add.</span></span>
37. <span data-ttu-id="8125a-144">В списке выберите значение "Категория расходов".</span><span class="sxs-lookup"><span data-stu-id="8125a-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="8125a-145">В поле "Поле" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="8125a-146">Перейдите на вкладку "Владение".</span><span class="sxs-lookup"><span data-stu-id="8125a-146">Click the Having tab.</span></span>
40. <span data-ttu-id="8125a-147">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="8125a-147">Click Add.</span></span>
41. <span data-ttu-id="8125a-148">Выберите "Сумма проводки".</span><span class="sxs-lookup"><span data-stu-id="8125a-148">Select Transaction amount</span></span>
42. <span data-ttu-id="8125a-149">В поле "Поле" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8125a-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="8125a-150">В поле "Функция расчета" выберите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="8125a-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="8125a-151">В поле "Критерии" введите ">2000".</span><span class="sxs-lookup"><span data-stu-id="8125a-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="8125a-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8125a-152">Click OK.</span></span>
46. <span data-ttu-id="8125a-153">Щелкните Тест.</span><span class="sxs-lookup"><span data-stu-id="8125a-153">Click Test.</span></span>
47. <span data-ttu-id="8125a-154">В поле "Начальная дата выбора документов" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8125a-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="8125a-155">В поле "Конечная дата выбора документов" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8125a-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="8125a-156">Щелкните "Запустить тест".</span><span class="sxs-lookup"><span data-stu-id="8125a-156">Click Run test.</span></span>
50. <span data-ttu-id="8125a-157">В области действий щелкните "Политика аудита".</span><span class="sxs-lookup"><span data-stu-id="8125a-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="8125a-158">Щелкните "Дополнительные параметры".</span><span class="sxs-lookup"><span data-stu-id="8125a-158">Click Additional options.</span></span>
52. <span data-ttu-id="8125a-159">В поле "Дата начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8125a-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="8125a-160">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8125a-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="8125a-161">Щелкните "Партия".</span><span class="sxs-lookup"><span data-stu-id="8125a-161">Click Batch.</span></span>
55. <span data-ttu-id="8125a-162">Разверните раздел "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="8125a-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="8125a-163">Выберите значение "Да" в поле "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="8125a-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="8125a-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8125a-164">Click OK.</span></span>
58. <span data-ttu-id="8125a-165">Перейдите в раздел "Рабочее место аудита" > "Обращения аудита".</span><span class="sxs-lookup"><span data-stu-id="8125a-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="8125a-166">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8125a-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="8125a-167">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8125a-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="8125a-168">Разверните раздел "Ассоциации".</span><span class="sxs-lookup"><span data-stu-id="8125a-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="8125a-169">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8125a-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="8125a-170">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8125a-170">In the list, click the link in the selected row.</span></span>


