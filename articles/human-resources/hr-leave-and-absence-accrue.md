---
title: Начислить планы отпусков и отсутствий
description: Можно начислять отпуск и отсутствие в Dynamics 365 Human Resources для нескольких сотрудников или для отдельных пользователей.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 348c8e5336854eb2a1c04a1f98a97a2c9dba7176
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464918"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="83ea6-103">Начислить планы отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="83ea6-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="83ea6-104">Можно начислять отпуск и отсутствие в Dynamics 365 Human Resources для нескольких сотрудников или для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="83ea6-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="83ea6-105">Начисление отпусков и отсутствия для нескольких сотрудников</span><span class="sxs-lookup"><span data-stu-id="83ea6-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="83ea6-106">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="83ea6-107">В **Управление отпуском** выберите **Начисление планов отпусков и отсутствий**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="83ea6-108">Будет открыто диалоговое окно **Начисление планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="83ea6-109">В поле **Начисление на** выберите **Сегодняшняя дата** или выберите **Настраиваемая дата** и введите настраиваемую дату.</span><span class="sxs-lookup"><span data-stu-id="83ea6-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="83ea6-110">Если необходимо выполнить начисления для всех компаний, выберите **Все компании**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="83ea6-111">Если необходимо обработать начисления для одного плана отпусков, выберите **Нет** для параметра **Все планы**, затем выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="83ea6-112">Если выбрать все компании, невозможно будет выбрать отдельный план отпусков.</span><span class="sxs-lookup"><span data-stu-id="83ea6-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="83ea6-113">Если необходимо выполнить процесс начисления в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83ea6-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="83ea6-114">Введите сведения для процесса начисления.</span><span class="sxs-lookup"><span data-stu-id="83ea6-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="83ea6-115">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="83ea6-116">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="83ea6-117">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-117">Select **OK**.</span></span> <span data-ttu-id="83ea6-118">Процесс начисления будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="83ea6-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="83ea6-119">Начисление отпусков и отсутствия для сотрудника</span><span class="sxs-lookup"><span data-stu-id="83ea6-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="83ea6-120">В записи сотрудника выберите **Отпуск**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="83ea6-121">Выберите **Начисление планов отпусков и отсутствий**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="83ea6-122">Будет открыто диалоговое окно **Начисление планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="83ea6-123">В поле **Начисление на** выберите **Сегодняшняя дата** или выберите **Настраиваемая дата** и введите настраиваемую дату.</span><span class="sxs-lookup"><span data-stu-id="83ea6-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="83ea6-124">Если необходимо выполнить начисления для всех компаний, выберите **Все компании**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="83ea6-125">Если необходимо обработать начисления для одного плана отпусков, выберите **Нет** для параметра **Все планы**, затем выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="83ea6-126">Если выбрать все компании, невозможно будет выбрать отдельный план отпусков.</span><span class="sxs-lookup"><span data-stu-id="83ea6-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="83ea6-127">Если необходимо выполнить процесс начисления в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83ea6-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="83ea6-128">Введите сведения для процесса начисления.</span><span class="sxs-lookup"><span data-stu-id="83ea6-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="83ea6-129">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="83ea6-130">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="83ea6-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-131">Select **OK**.</span></span> <span data-ttu-id="83ea6-132">Процесс начисления будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="83ea6-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="83ea6-133">Удаление начислений отпусков и отсутствия для нескольких сотрудников</span><span class="sxs-lookup"><span data-stu-id="83ea6-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="83ea6-134">Удаление записей начисления для определенного плана и диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="83ea6-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="83ea6-135">Даты начисления должны быть датированы сегодня или в будущем.</span><span class="sxs-lookup"><span data-stu-id="83ea6-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="83ea6-136">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="83ea6-137">В **Управление отпуском** выберите **Удалить начисления планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="83ea6-138">В диалоговом окне **Удаление начислений плана отпусков и отсутствия** выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="83ea6-139">Если применимо, выберите **Удалить корректировки сальдо**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="83ea6-140">Введите или выберите **Дата начисления отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="83ea6-141">Эта дата должна быть либо сегодняшней, либо будущей.</span><span class="sxs-lookup"><span data-stu-id="83ea6-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="83ea6-142">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-142">Select **OK**.</span></span> <span data-ttu-id="83ea6-143">Процесс начисления удалит начисления с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="83ea6-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="83ea6-144">Удаление начислений отпусков и отсутствия для одного сотрудника</span><span class="sxs-lookup"><span data-stu-id="83ea6-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="83ea6-145">В записи сотрудника выберите **Отпуск**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="83ea6-146">Выберите **Удалить начисления планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="83ea6-147">В диалоговом окне **Удаление начислений плана отпусков и отсутствия** выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="83ea6-148">Если применимо, выберите **Удалить корректировки сальдо**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="83ea6-149">Введите или выберите **Дата начисления отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="83ea6-150">Эта дата должна быть либо сегодняшней, либо будущей.</span><span class="sxs-lookup"><span data-stu-id="83ea6-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="83ea6-151">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-151">Select **OK**.</span></span> <span data-ttu-id="83ea6-152">Процесс начисления удалит начисления с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="83ea6-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="83ea6-153">Обзор процессов начисления и удаления отпусков</span><span class="sxs-lookup"><span data-stu-id="83ea6-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="83ea6-154">**Аудит начисления отпуска** отображается при каждом выполнении или удалении начисления для одного или всех сотрудников.</span><span class="sxs-lookup"><span data-stu-id="83ea6-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="83ea6-155">Также отображаются дата и лицо, которые выполнило действие.</span><span class="sxs-lookup"><span data-stu-id="83ea6-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="83ea6-156">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="83ea6-157">В **Управление отпуском** выберите **Аудит удаления начисления отпусков**.</span><span class="sxs-lookup"><span data-stu-id="83ea6-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="83ea6-158">См. также</span><span class="sxs-lookup"><span data-stu-id="83ea6-158">See also</span></span>

[<span data-ttu-id="83ea6-159">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="83ea6-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="83ea6-160">Создание плана отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="83ea6-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]