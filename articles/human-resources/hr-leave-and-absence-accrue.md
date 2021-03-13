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
ms.openlocfilehash: aed36a38c5d50767b5ac14ae82ca424f0c835ae0
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5116100"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="86e33-103">Начислить планы отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="86e33-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="86e33-104">Можно начислять отпуск и отсутствие в Dynamics 365 Human Resources для нескольких сотрудников или для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="86e33-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="86e33-105">Начисление отпусков и отсутствия для нескольких сотрудников</span><span class="sxs-lookup"><span data-stu-id="86e33-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="86e33-106">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="86e33-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="86e33-107">В **Управление отпуском** выберите **Начисление планов отпусков и отсутствий**.</span><span class="sxs-lookup"><span data-stu-id="86e33-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="86e33-108">Будет открыто диалоговое окно **Начисление планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="86e33-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="86e33-109">В поле **Начисление на** выберите **Сегодняшняя дата** или выберите **Настраиваемая дата** и введите настраиваемую дату.</span><span class="sxs-lookup"><span data-stu-id="86e33-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="86e33-110">Если необходимо выполнить начисления для всех компаний, выберите **Все компании**.</span><span class="sxs-lookup"><span data-stu-id="86e33-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="86e33-111">Если необходимо обработать начисления для одного плана отпусков, выберите **Нет** для параметра **Все планы**, затем выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="86e33-112">Если выбрать все компании, невозможно будет выбрать отдельный план отпусков.</span><span class="sxs-lookup"><span data-stu-id="86e33-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="86e33-113">Если необходимо выполнить процесс начисления в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="86e33-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="86e33-114">Введите сведения для процесса начисления.</span><span class="sxs-lookup"><span data-stu-id="86e33-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="86e33-115">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="86e33-116">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="86e33-117">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-117">Select **OK**.</span></span> <span data-ttu-id="86e33-118">Процесс начисления будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="86e33-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="86e33-119">Начисление отпусков и отсутствия для сотрудника</span><span class="sxs-lookup"><span data-stu-id="86e33-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="86e33-120">В записи сотрудника выберите **Отпуск**.</span><span class="sxs-lookup"><span data-stu-id="86e33-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="86e33-121">Выберите **Начисление планов отпусков и отсутствий**.</span><span class="sxs-lookup"><span data-stu-id="86e33-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="86e33-122">Будет открыто диалоговое окно **Начисление планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="86e33-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="86e33-123">В поле **Начисление на** выберите **Сегодняшняя дата** или выберите **Настраиваемая дата** и введите настраиваемую дату.</span><span class="sxs-lookup"><span data-stu-id="86e33-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="86e33-124">Если необходимо выполнить начисления для всех компаний, выберите **Все компании**.</span><span class="sxs-lookup"><span data-stu-id="86e33-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="86e33-125">Если необходимо обработать начисления для одного плана отпусков, выберите **Нет** для параметра **Все планы**, затем выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="86e33-126">Если выбрать все компании, невозможно будет выбрать отдельный план отпусков.</span><span class="sxs-lookup"><span data-stu-id="86e33-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="86e33-127">Если необходимо выполнить процесс начисления в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="86e33-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="86e33-128">Введите сведения для процесса начисления.</span><span class="sxs-lookup"><span data-stu-id="86e33-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="86e33-129">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="86e33-130">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="86e33-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-131">Select **OK**.</span></span> <span data-ttu-id="86e33-132">Процесс начисления будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="86e33-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="86e33-133">Удаление начислений отпусков и отсутствия для нескольких сотрудников</span><span class="sxs-lookup"><span data-stu-id="86e33-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="86e33-134">Удаление записей начисления для определенного плана и диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="86e33-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="86e33-135">Даты начисления должны быть датированы сегодня или в будущем.</span><span class="sxs-lookup"><span data-stu-id="86e33-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="86e33-136">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="86e33-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="86e33-137">В **Управление отпуском** выберите **Удалить начисления планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="86e33-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="86e33-138">В диалоговом окне **Удаление начислений плана отпусков и отсутствия** выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="86e33-139">Если применимо, выберите **Удалить корректировки сальдо**.</span><span class="sxs-lookup"><span data-stu-id="86e33-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="86e33-140">Введите или выберите **Дата начисления отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="86e33-141">Эта дата должна быть либо сегодняшней, либо будущей.</span><span class="sxs-lookup"><span data-stu-id="86e33-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="86e33-142">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-142">Select **OK**.</span></span> <span data-ttu-id="86e33-143">Процесс начисления удалит начисления с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="86e33-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="86e33-144">Удаление начислений отпусков и отсутствия для одного сотрудника</span><span class="sxs-lookup"><span data-stu-id="86e33-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="86e33-145">В записи сотрудника выберите **Отпуск**.</span><span class="sxs-lookup"><span data-stu-id="86e33-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="86e33-146">Выберите **Удалить начисления планов отпусков и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="86e33-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="86e33-147">В диалоговом окне **Удаление начислений плана отпусков и отсутствия** выберите **План отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="86e33-148">Если применимо, выберите **Удалить корректировки сальдо**.</span><span class="sxs-lookup"><span data-stu-id="86e33-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="86e33-149">Введите или выберите **Дата начисления отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="86e33-150">Эта дата должна быть либо сегодняшней, либо будущей.</span><span class="sxs-lookup"><span data-stu-id="86e33-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="86e33-151">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86e33-151">Select **OK**.</span></span> <span data-ttu-id="86e33-152">Процесс начисления удалит начисления с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="86e33-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="86e33-153">Обзор процессов начисления и удаления отпусков</span><span class="sxs-lookup"><span data-stu-id="86e33-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="86e33-154">**Аудит начисления отпуска** отображается при каждом выполнении или удалении начисления для одного или всех сотрудников.</span><span class="sxs-lookup"><span data-stu-id="86e33-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="86e33-155">Также отображаются дата и лицо, которые выполнило действие.</span><span class="sxs-lookup"><span data-stu-id="86e33-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="86e33-156">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="86e33-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="86e33-157">В **Управление отпуском** выберите **Аудит удаления начисления отпусков**.</span><span class="sxs-lookup"><span data-stu-id="86e33-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="86e33-158">См. также</span><span class="sxs-lookup"><span data-stu-id="86e33-158">See also</span></span>

[<span data-ttu-id="86e33-159">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="86e33-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="86e33-160">Создание плана отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="86e33-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
