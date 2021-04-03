---
title: Разработка структуры компенсации
description: В этой статье рассматривается создание плана фиксированной компенсации и регистрации сотрудников в плане с помощью правил приемлемости.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5030203877ebdf885fb55c7946bfd4ee0c883c2e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465686"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="93b38-103">Разработка структуры компенсации</span><span class="sxs-lookup"><span data-stu-id="93b38-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="93b38-104">В этой статье рассматривается создание плана фиксированной компенсации и регистрации сотрудников в плане с помощью правил приемлемости.</span><span class="sxs-lookup"><span data-stu-id="93b38-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="93b38-105">В этой статье используются демонстрационные данные USMF и они применимы к менеджерам по компенсациям и льготам.</span><span class="sxs-lookup"><span data-stu-id="93b38-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="93b38-106">Создание плана фиксированных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="93b38-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="93b38-107">Выберите **Управление компенсациями**.</span><span class="sxs-lookup"><span data-stu-id="93b38-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="93b38-108">Выберите **Планы фиксированной компенсации**.</span><span class="sxs-lookup"><span data-stu-id="93b38-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="93b38-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="93b38-109">Select **New**.</span></span>

4. <span data-ttu-id="93b38-110">В поле **План** введите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="93b38-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="93b38-112">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="93b38-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="93b38-113">В поле **Тип** укажите, к какому типу принадлежит план фиксированной компенсации: **Диапазон**, **Уровень** или **Шаг**.</span><span class="sxs-lookup"><span data-stu-id="93b38-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="93b38-114">Флажок **Рекомендации разрешены** установлен по умолчанию для всех действий, добавляемых в данный план в событии процесса.</span><span class="sxs-lookup"><span data-stu-id="93b38-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="93b38-115">Разрешение рекомендаций позволяет переопределить рассчитанную рекомендованную сумму при обработке компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="93b38-116">С помощью поля **Вне допустимого диапазона** можно определить способ обработки сумм компенсации, которые выходят за пределы указанного диапазона структуры компенсации для данного уровня.</span><span class="sxs-lookup"><span data-stu-id="93b38-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="93b38-117">Значение поля **Вне допустимого диапазона** установленное на **Нет** позволяет использовать любую сумму компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="93b38-118">Параметр **Предварительный допуск** предупреждает пользователей, если сумма компенсации меньше минимальной суммы или больше максимальной суммы опорной точки для этого уровня.</span><span class="sxs-lookup"><span data-stu-id="93b38-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="93b38-119">Пользователи могут проигнорировать предупреждение и продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="93b38-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="93b38-120">Параметр **Окончательный допуск** выдаст ошибку, если компенсация сотрудника выходит за пределы минимальной и максимальной опорных точек для этого уровня, и автоматически скорректирует компенсацию сотрудника в соответствии с диапазоном.</span><span class="sxs-lookup"><span data-stu-id="93b38-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="93b38-121">Поле **Правило найма** вычисляет компенсацию сотрудника во время события процесса.</span><span class="sxs-lookup"><span data-stu-id="93b38-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="93b38-122">Если для параметра **Правило найма** задать значение **Процент**, будет рассчитываться увеличение, пропорционально продолжительности времени занятости работника в цикле.</span><span class="sxs-lookup"><span data-stu-id="93b38-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="93b38-123">В поле **Валюта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="93b38-124">В поле **Преобразование ставки оплаты** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="93b38-125">Разверните раздел **Матрица использования диапазона**.</span><span class="sxs-lookup"><span data-stu-id="93b38-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="93b38-126">При необходимости добавьте записи использования диапазона, чтобы сотрудники достигали средней точки быстрее, а максимума диапазона медленнее.</span><span class="sxs-lookup"><span data-stu-id="93b38-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="93b38-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="93b38-127">Select **Save**.</span></span> <span data-ttu-id="93b38-128">При этом активируется кнопка **настроить компенсацию** и продолжается определение структуры компенсаций для этого плана.</span><span class="sxs-lookup"><span data-stu-id="93b38-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="93b38-129">Выберите **настроить компенсацию**.</span><span class="sxs-lookup"><span data-stu-id="93b38-129">Select **Set up compensation**.</span></span> <span data-ttu-id="93b38-130">Можно создать структуру компенсации, используя один из этих трех методов:</span><span class="sxs-lookup"><span data-stu-id="93b38-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="93b38-131">Создайте полностью новую структуры, выбрав набор опорных точек и добавив уровни для создания собственной структуры.</span><span class="sxs-lookup"><span data-stu-id="93b38-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="93b38-132">Скопируйте структуру компенсации из существующего плана в качестве начальной точки и измените ее для нового плана.</span><span class="sxs-lookup"><span data-stu-id="93b38-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="93b38-133">Выберите существующую сетку компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-133">Select an existing compensation grid.</span></span> <span data-ttu-id="93b38-134">Если сетка компенсации уже используется в другом плане, другой план также отражает любые изменения, внесенные вами в сетку.</span><span class="sxs-lookup"><span data-stu-id="93b38-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="93b38-135">Выберите **Создать новую из существующей матрицы компенсации**.</span><span class="sxs-lookup"><span data-stu-id="93b38-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="93b38-136">В поле **Копировать из сетки** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="93b38-137">При необходимости можно изменить имя новой сетки компенсации, которая создается как копия выбранной сетки.</span><span class="sxs-lookup"><span data-stu-id="93b38-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="93b38-138">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="93b38-138">Select **OK**.</span></span>

19. <span data-ttu-id="93b38-139">Выберите **массовое изменение**.</span><span class="sxs-lookup"><span data-stu-id="93b38-139">Select **Mass change**.</span></span> <span data-ttu-id="93b38-140">**Массовое изменение** позволяет поддерживать суммы матрицы компенсации путем применения процента или фиксированное увеличение к одному или нескольким уровням или опорным точкам.</span><span class="sxs-lookup"><span data-stu-id="93b38-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="93b38-141">В поле **Сумма корректировки** введите число.</span><span class="sxs-lookup"><span data-stu-id="93b38-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="93b38-142">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="93b38-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="93b38-143">Щелкните **Применить к сетке**.</span><span class="sxs-lookup"><span data-stu-id="93b38-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="93b38-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="93b38-144">Close the page.</span></span> <span data-ttu-id="93b38-145">После создания структуры компенсации можно выбрать, какие опорные точки должны использоваться в качестве контрольной точки для плана фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="93b38-146">Контрольная точка используется для расчета относительного показателя сотрудника.</span><span class="sxs-lookup"><span data-stu-id="93b38-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="93b38-147">В поле **Контрольная точка** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="93b38-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="93b38-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="93b38-149">Создание правило приемлемости для плана фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="93b38-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="93b38-150">План фиксированной компенсации невозможно назначить сотруднику, пока для плана не будут определены правила приемлемости.</span><span class="sxs-lookup"><span data-stu-id="93b38-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="93b38-151">Выберите **правила приемлемости**.</span><span class="sxs-lookup"><span data-stu-id="93b38-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="93b38-152">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="93b38-152">Select **New**.</span></span>

3. <span data-ttu-id="93b38-153">В поле **Приемлемость** введите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="93b38-154">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="93b38-155">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="93b38-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="93b38-156">Как фиксированные, так и переменные планы компенсации используют правила приемлемости.</span><span class="sxs-lookup"><span data-stu-id="93b38-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="93b38-157">В поле **Тип** выберите тип плана.</span><span class="sxs-lookup"><span data-stu-id="93b38-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="93b38-158">В поле **План** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="93b38-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="93b38-159">Выберите критерии, которым должен отвечать сотрудник, чтобы иметь право на план компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="93b38-160">Критерии могут включать:</span><span class="sxs-lookup"><span data-stu-id="93b38-160">Criteria can include:</span></span>

    - <span data-ttu-id="93b38-161">**Отдел**</span><span class="sxs-lookup"><span data-stu-id="93b38-161">**Department**</span></span>
    - <span data-ttu-id="93b38-162">**Профсоюз**</span><span class="sxs-lookup"><span data-stu-id="93b38-162">**Labor union**</span></span>
    - <span data-ttu-id="93b38-163">**Местоположение** (**Регион компенсации**)</span><span class="sxs-lookup"><span data-stu-id="93b38-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="93b38-164">**Задание**</span><span class="sxs-lookup"><span data-stu-id="93b38-164">**Job**</span></span>
    - <span data-ttu-id="93b38-165">**Функция**</span><span class="sxs-lookup"><span data-stu-id="93b38-165">**Function**</span></span>
    - <span data-ttu-id="93b38-166">**Тип вакансии**</span><span class="sxs-lookup"><span data-stu-id="93b38-166">**Job type**</span></span>
    - <span data-ttu-id="93b38-167">**Уровень компенсации**</span><span class="sxs-lookup"><span data-stu-id="93b38-167">**Compensation level**</span></span>
    
    <span data-ttu-id="93b38-168">Сотрудник должен отвечать всем указанным критериям, чтобы иметь право на план компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="93b38-169">Если какие-либо критерии не указаны, все сотрудники будут иметь право на план компенсации.</span><span class="sxs-lookup"><span data-stu-id="93b38-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="93b38-170">Если сотрудник не отвечает критериям, указанным в правиле приемлемости, или правило приемлемости не указано для плана компенсации, план компенсации не будет отображаться в результатах поиска при создании записи фиксированной компенсации для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="93b38-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="93b38-171">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="93b38-171">Close the page.</span></span>

8. <span data-ttu-id="93b38-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="93b38-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]