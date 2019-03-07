---
title: Определение политик аудита для документов-источников
description: В этой процедура показано, как настроить и запустить правила политики аудита.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "336804"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="12d54-103">Определение политик аудита для документов-источников</span><span class="sxs-lookup"><span data-stu-id="12d54-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12d54-104">В этой процедура показано, как настроить и запустить правила политики аудита.</span><span class="sxs-lookup"><span data-stu-id="12d54-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="12d54-105">В этом примере используются отчеты по расходам с типом расходов на проживание в гостинице.</span><span class="sxs-lookup"><span data-stu-id="12d54-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="12d54-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="12d54-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="12d54-107">Роль аудитора содержит правильные разрешения для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="12d54-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="12d54-108">Перейдите в раздел "Рабочее место аудита" > "Настройка" > "Тип правила политики".</span><span class="sxs-lookup"><span data-stu-id="12d54-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="12d54-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="12d54-109">Click New.</span></span>
3. <span data-ttu-id="12d54-110">В поле "Правило" введите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="12d54-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="12d54-112">В поле "Имя запроса" выберите строку "Отчет по расходам".</span><span class="sxs-lookup"><span data-stu-id="12d54-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="12d54-113">В поле "Тип запроса" выберите "Агрегировано".</span><span class="sxs-lookup"><span data-stu-id="12d54-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="12d54-114">В поле "Юридическое лицо" выберите "Юридическое лицо".</span><span class="sxs-lookup"><span data-stu-id="12d54-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="12d54-115">В поле "Ссылка на дату документа" выберите "Дата и время изменения".</span><span class="sxs-lookup"><span data-stu-id="12d54-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="12d54-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="12d54-116">Click Save.</span></span>
10. <span data-ttu-id="12d54-117">Перейдите в раздел "Рабочее место аудита" > "Настройка" > "Политики аудита".</span><span class="sxs-lookup"><span data-stu-id="12d54-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="12d54-118">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="12d54-118">Click New.</span></span>
12. <span data-ttu-id="12d54-119">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="12d54-120">Разверните раздел "Организации политики".</span><span class="sxs-lookup"><span data-stu-id="12d54-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="12d54-121">В дереве выберите "Contoso Entertainment System USA".</span><span class="sxs-lookup"><span data-stu-id="12d54-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="12d54-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-122">Click Add.</span></span>
16. <span data-ttu-id="12d54-123">В дереве выберите "Contoso Consulting USA".</span><span class="sxs-lookup"><span data-stu-id="12d54-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="12d54-124">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-124">Click Add.</span></span>
18. <span data-ttu-id="12d54-125">В дереве выберите "Contoso Retail USA".</span><span class="sxs-lookup"><span data-stu-id="12d54-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="12d54-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-126">Click Add.</span></span>
20. <span data-ttu-id="12d54-127">Сверните раздел "Организации политики".</span><span class="sxs-lookup"><span data-stu-id="12d54-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="12d54-128">Разверните раздел "Правила политики".</span><span class="sxs-lookup"><span data-stu-id="12d54-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="12d54-129">Найдите в списке ранее созданное правило политики и выберите его.</span><span class="sxs-lookup"><span data-stu-id="12d54-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="12d54-130">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="12d54-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="12d54-131">В поле "Действует с" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12d54-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="12d54-132">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="12d54-132">Click Filter.</span></span>
26. <span data-ttu-id="12d54-133">В списке выберите строку для категории расходов и задайте для сведений значение "Гостиница".</span><span class="sxs-lookup"><span data-stu-id="12d54-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="12d54-134">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="12d54-135">Перейдите на вкладку "Агрегировано".</span><span class="sxs-lookup"><span data-stu-id="12d54-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="12d54-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-136">Click Add.</span></span>
30. <span data-ttu-id="12d54-137">В списке выберите значение поля "Сумма проводки".</span><span class="sxs-lookup"><span data-stu-id="12d54-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="12d54-138">В поле "Поле" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="12d54-139">В поле "Функция расчета" выберите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="12d54-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="12d54-140">Перейдите на вкладку "Группа".</span><span class="sxs-lookup"><span data-stu-id="12d54-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="12d54-141">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-141">Click Add.</span></span>
35. <span data-ttu-id="12d54-142">В списке выберите значение "Сотрудник".</span><span class="sxs-lookup"><span data-stu-id="12d54-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="12d54-143">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-143">Click Add.</span></span>
37. <span data-ttu-id="12d54-144">В списке выберите значение "Категория расходов".</span><span class="sxs-lookup"><span data-stu-id="12d54-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="12d54-145">В поле "Поле" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="12d54-146">Перейдите на вкладку "Владение".</span><span class="sxs-lookup"><span data-stu-id="12d54-146">Click the Having tab.</span></span>
40. <span data-ttu-id="12d54-147">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="12d54-147">Click Add.</span></span>
41. <span data-ttu-id="12d54-148">Выберите "Сумма проводки".</span><span class="sxs-lookup"><span data-stu-id="12d54-148">Select Transaction amount</span></span>
42. <span data-ttu-id="12d54-149">В поле "Поле" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12d54-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="12d54-150">В поле "Функция расчета" выберите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="12d54-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="12d54-151">В поле "Критерии" введите ">2000".</span><span class="sxs-lookup"><span data-stu-id="12d54-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="12d54-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="12d54-152">Click OK.</span></span>
46. <span data-ttu-id="12d54-153">Щелкните Тест.</span><span class="sxs-lookup"><span data-stu-id="12d54-153">Click Test.</span></span>
47. <span data-ttu-id="12d54-154">В поле "Начальная дата выбора документов" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12d54-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="12d54-155">В поле "Конечная дата выбора документов" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12d54-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="12d54-156">Щелкните "Запустить тест".</span><span class="sxs-lookup"><span data-stu-id="12d54-156">Click Run test.</span></span>
50. <span data-ttu-id="12d54-157">В области действий щелкните "Политика аудита".</span><span class="sxs-lookup"><span data-stu-id="12d54-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="12d54-158">Щелкните "Дополнительные параметры".</span><span class="sxs-lookup"><span data-stu-id="12d54-158">Click Additional options.</span></span>
52. <span data-ttu-id="12d54-159">В поле "Дата начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12d54-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="12d54-160">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12d54-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="12d54-161">Щелкните "Партия".</span><span class="sxs-lookup"><span data-stu-id="12d54-161">Click Batch.</span></span>
55. <span data-ttu-id="12d54-162">Разверните раздел "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="12d54-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="12d54-163">Выберите значение "Да" в поле "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="12d54-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="12d54-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="12d54-164">Click OK.</span></span>
58. <span data-ttu-id="12d54-165">Перейдите в раздел "Рабочее место аудита" > "Обращения аудита".</span><span class="sxs-lookup"><span data-stu-id="12d54-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="12d54-166">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="12d54-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="12d54-167">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="12d54-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="12d54-168">Разверните раздел "Ассоциации".</span><span class="sxs-lookup"><span data-stu-id="12d54-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="12d54-169">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="12d54-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="12d54-170">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="12d54-170">In the list, click the link in the selected row.</span></span>

