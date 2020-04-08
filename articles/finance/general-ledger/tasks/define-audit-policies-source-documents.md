---
title: Определение политик аудита для документов-источников
description: В этой теме объясняется, как настроить и запустить правила политики аудита.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145037"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="12b0d-103">Определение политик аудита для документов-источников</span><span class="sxs-lookup"><span data-stu-id="12b0d-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12b0d-104">В этой теме объясняется, как настроить и запустить правила политики аудита.</span><span class="sxs-lookup"><span data-stu-id="12b0d-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="12b0d-105">В этом примере используются отчеты по расходам с типом расходов на проживание в гостинице.</span><span class="sxs-lookup"><span data-stu-id="12b0d-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="12b0d-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="12b0d-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="12b0d-107">Роль аудитора содержит правильные разрешения для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="12b0d-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="12b0d-108">В области переходов выберите **Модули > Рабочее место аудита > Настройка > Тип правила политики**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="12b0d-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-109">Select **New**.</span></span>
3. <span data-ttu-id="12b0d-110">В поле **Имя правила** введите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="12b0d-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="12b0d-112">В поле **Имя запроса** выберите строку **Отчет по расходам**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="12b0d-113">В поле **Тип запроса** выберите **Агрегировано**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="12b0d-114">В поле **Юридическое лицо** выберите **Юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="12b0d-115">В поле **Ссылка на дату документа** выберите **Дата и время изменения**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="12b0d-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-116">Select **Save**.</span></span>
10. <span data-ttu-id="12b0d-117">В области переходов выберите **Модули > Рабочее место аудита > Настройка > Политики аудита**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="12b0d-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-118">Select **New**.</span></span>
12. <span data-ttu-id="12b0d-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="12b0d-120">Разверните раздел **Организации политики**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="12b0d-121">В дереве выберите **Contoso Entertainment System USA**, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="12b0d-122">В дереве выберите **Contoso Consulting USA**, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="12b0d-123">В дереве выберите **Contoso Retail USA**, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="12b0d-124">Сверните раздел **Организации политики**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="12b0d-125">Разверните раздел **Правила политики**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="12b0d-126">Найдите в списке ранее созданное правило политики и выберите его.</span><span class="sxs-lookup"><span data-stu-id="12b0d-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="12b0d-127">Выберите **Создать правило политики**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="12b0d-128">В поле **Действует с** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12b0d-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="12b0d-129">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-129">Select **Filter**.</span></span>
23. <span data-ttu-id="12b0d-130">В списке выберите строку для **Категория расходов** и задайте для сведений значение **Гостиница**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="12b0d-131">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="12b0d-132">Выберите вкладку **Агрегировано**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="12b0d-133">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-133">Select **Add**.</span></span>
27. <span data-ttu-id="12b0d-134">В списке выберите значение поля **Сумма проводки**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="12b0d-135">В поле **Поле** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="12b0d-136">В поле **Функция расчета** выберите **Сумма**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="12b0d-137">Выберите вкладку **Группировать по**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="12b0d-138">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-138">Select **Add**.</span></span>
32. <span data-ttu-id="12b0d-139">В списке выберите значение **Сотрудник**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="12b0d-140">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-140">Select **Add**.</span></span>
34. <span data-ttu-id="12b0d-141">В списке выберите значение **Категория расходов**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="12b0d-142">В поле **Поле** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="12b0d-143">Выберите вкладку **Владение**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="12b0d-144">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-144">Select **Add**.</span></span>
38. <span data-ttu-id="12b0d-145">Выберите **Сумма проводки**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="12b0d-146">В поле **Поле** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="12b0d-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="12b0d-147">В поле **Функция расчета** выберите **Сумма**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="12b0d-148">В поле **Критерии** введите `>2000`.</span><span class="sxs-lookup"><span data-stu-id="12b0d-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="12b0d-149">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-149">Select **OK**.</span></span>
43. <span data-ttu-id="12b0d-150">Выберите **Проверка**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-150">Select **Test**.</span></span>
44. <span data-ttu-id="12b0d-151">В поле **Начальная дата выбора документов** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12b0d-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="12b0d-152">В поле **Конечная дата выбора документов** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12b0d-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="12b0d-153">Выберите **Запустить тест**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-153">Select **Run test**.</span></span>
47. <span data-ttu-id="12b0d-154">В области действий выберите **Политика аудита**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="12b0d-155">Выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="12b0d-156">В поле **Дата начала** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12b0d-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="12b0d-157">В поле **Дата окончания** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="12b0d-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="12b0d-158">Выберите **Партия**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-158">Select **Batch**.</span></span>
52. <span data-ttu-id="12b0d-159">Разверните раздел **Выполнять в фоновом режиме**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="12b0d-160">Выберите значение **Да** в поле **Пакетная обработка**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="12b0d-161">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-161">Select **OK**.</span></span>
55. <span data-ttu-id="12b0d-162">В области переходов выберите **Модули > Рабочее место аудита > Настройка > Обращения аудита**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="12b0d-163">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="12b0d-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="12b0d-164">Разверните раздел **Ассоциации**.</span><span class="sxs-lookup"><span data-stu-id="12b0d-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="12b0d-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="12b0d-165">In the list, find and select the desired record.</span></span>

