---
title: "Настройка курсов обучения"
description: "Администраторы и менеджеры по управлению персоналом могут использовать характеристики курсов для ведения информации об обучении, которое предложено работникам."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0ab79e85872c19e30f24e182ea483687ecc0bc09
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-training-courses"></a><span data-ttu-id="4d0e6-103">Настройка курсов обучения</span><span class="sxs-lookup"><span data-stu-id="4d0e6-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="4d0e6-104">Администраторы и менеджеры по управлению персоналом могут использовать характеристики курсов для ведения информации об обучении, которое предложено работникам.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="4d0e6-105">Предварительные условия настройки</span><span class="sxs-lookup"><span data-stu-id="4d0e6-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="4d0e6-106">Следующая информация необходима и должна быть настроена до создания курсов.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="4d0e6-107">**Типы курсов**</span><span class="sxs-lookup"><span data-stu-id="4d0e6-107">**Course types**</span></span>

<span data-ttu-id="4d0e6-108">Следующая информация не является обязательной информацией, но ее также можно определить для курсов.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="4d0e6-109">Если известно, что вы будете задавать эту информацию о курсах, необходимо определить ее до создания записей курсов.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="4d0e6-110">**Группы аудиторий**</span><span class="sxs-lookup"><span data-stu-id="4d0e6-110">**Classroom groups**</span></span>
-   <span data-ttu-id="4d0e6-111">**Группы курсов**</span><span class="sxs-lookup"><span data-stu-id="4d0e6-111">**Course groups**</span></span>
-   <span data-ttu-id="4d0e6-112">**Места проведения курсов**</span><span class="sxs-lookup"><span data-stu-id="4d0e6-112">**Course locations**</span></span>
-   <span data-ttu-id="4d0e6-113">**Аудитории**</span><span class="sxs-lookup"><span data-stu-id="4d0e6-113">**Classrooms**</span></span>
-   <span data-ttu-id="4d0e6-114">**Лекторы**</span><span class="sxs-lookup"><span data-stu-id="4d0e6-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="4d0e6-115">Типы курсов</span><span class="sxs-lookup"><span data-stu-id="4d0e6-115">Course types</span></span>
<span data-ttu-id="4d0e6-116">Курсы можно классифицировать по их структуре или содержимому, используя типы курсов.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="4d0e6-117">Вы можете создать типы курсов на странице **Типы курсов**.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="4d0e6-118">При создании записи курса необходимо выбрать тип курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="4d0e6-119">Тип настройки курса</span><span class="sxs-lookup"><span data-stu-id="4d0e6-119">Course setup type</span></span>
<span data-ttu-id="4d0e6-120">В следующей таблице перечислены три типа настройки для курсов.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="4d0e6-121">Типы настройки определяют структуру курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4d0e6-122">Тип настройки</span><span class="sxs-lookup"><span data-stu-id="4d0e6-122">Setup type</span></span></th>
<th><span data-ttu-id="4d0e6-123">Описание</span><span class="sxs-lookup"><span data-stu-id="4d0e6-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d0e6-124"><strong>Стандарт</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="4d0e6-125">Этот тип предназначен для курсов, у которых не ежедневного расписания.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="4d0e6-126">Это тип настройки по умолчанию, используемый при создании нового курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d0e6-127"><strong>План</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="4d0e6-128">Выберите этот тип для того, чтобы запланировать сведения о каждом дне курса, который занимает несколько дней.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d0e6-129"><strong>План + сессия</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="4d0e6-130">Этот тип предназначен для более сложных курсов.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="4d0e6-131">Например, вы можете расписание курса на программы и сессии.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="4d0e6-132"><strong>Программа</strong> — отслеживание конкретных предметных областей курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="4d0e6-133"><strong>Сессии</strong> — сессии являются частью программ и помогают идентифицировать конкретные процессы или технологии из соответствующей программы.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="4d0e6-134">Задачи курса</span><span class="sxs-lookup"><span data-stu-id="4d0e6-134">Course tasks</span></span>
<span data-ttu-id="4d0e6-135">Для каждого курса можно выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="4d0e6-136">Зарегистрировать слушателей</span><span class="sxs-lookup"><span data-stu-id="4d0e6-136">Register participants</span></span>
-   <span data-ttu-id="4d0e6-137">Определить крайний срок регистрации</span><span class="sxs-lookup"><span data-stu-id="4d0e6-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="4d0e6-138">Определить минимальный и максимальный номера слушателей</span><span class="sxs-lookup"><span data-stu-id="4d0e6-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="4d0e6-139">Назначить место проведения курсов и аудиторию</span><span class="sxs-lookup"><span data-stu-id="4d0e6-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="4d0e6-140">Рекомендовать гостиницы слушателям курсов</span><span class="sxs-lookup"><span data-stu-id="4d0e6-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="4d0e6-141">Создать описание курса, который можно затем рекламировать на портале самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="4d0e6-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="4d0e6-142">**Примечание.** Вы можете удалить курс, только если никто не зарегистрирован на него.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="4d0e6-143">Статусы курсов</span><span class="sxs-lookup"><span data-stu-id="4d0e6-143">Course statuses</span></span>
<span data-ttu-id="4d0e6-144">В следующей таблице перечислены возможные статусы курсов и действия, которые могут выполняться, когда курс имеет определенный статус.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4d0e6-145">Состояние</span><span class="sxs-lookup"><span data-stu-id="4d0e6-145">Status</span></span></th>
<th><span data-ttu-id="4d0e6-146">Действия</span><span class="sxs-lookup"><span data-stu-id="4d0e6-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d0e6-147"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="4d0e6-148">Ввод и изменение сведений о курсе.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="4d0e6-149">Измените статус курса на <strong>Открыто</strong>, чтобы сотрудники могли регистрироваться на него.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d0e6-150"><strong>Открыть</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="4d0e6-151">Регистрация слушателей курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="4d0e6-152">Удаление слушателей курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="4d0e6-153">Подтверждение слушателей курса.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="4d0e6-154">Изменение статуса курса на <strong>Закрыто</strong> или <strong>Отменено</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="4d0e6-155">Планирование анкет для участников, которым присвоен статус <strong>Подтверждено</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d0e6-156"><strong>Закрыто</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="4d0e6-157">Вы можете заново открыть курс.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d0e6-158"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="4d0e6-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="4d0e6-159">Вы можете заново открыть курс.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="4d0e6-160">Слушатели курса</span><span class="sxs-lookup"><span data-stu-id="4d0e6-160">Course participants</span></span>
<span data-ttu-id="4d0e6-161">Слушателями курсов являются работники, кандидаты или контактные лица, принимающие участие в курсе обучения или мероприятии.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="4d0e6-162">Слушателей можно регистрировать только на открытые курсы.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-162">You can only register participants for open courses.</span></span> <span data-ttu-id="4d0e6-163">Минимальное и максимальное количество слушателей, которое можно зарегистрировать на курс, определяется на экспресс-вкладке **Общие** на странице **Курсы**.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="4d0e6-164">Документооборот</span><span class="sxs-lookup"><span data-stu-id="4d0e6-164">Workflow</span></span>
--------

<span data-ttu-id="4d0e6-165">Для сотрудников, регистрирующихся для участия в курсах на странице **Самообслуживание сотрудников**, регистрация может направляться через workflow-процесс для утверждения.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="4d0e6-166">Workflow-процесс может быть назначен курсу на экспресс-вкладке **Общие** на странице **Курсы**.</span><span class="sxs-lookup"><span data-stu-id="4d0e6-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






