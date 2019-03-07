---
title: Проекты по массовому набору сотрудников
description: Проекты по массовому набору сотрудников позволяют специалисту по найму создавать нескольких должностей и эффективно нанимать сотрудников на эти должности.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4c1bd382fa803f90a251c8c45acc556bee627d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "361552"
---
# <a name="mass-hire-projects"></a><span data-ttu-id="b9f42-103">Проекты по массовому набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="b9f42-103">Mass hire projects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9f42-104">Проекты по массовому набору сотрудников позволяют специалисту по найму создавать нескольких должностей и эффективно нанимать сотрудников на эти должности.</span><span class="sxs-lookup"><span data-stu-id="b9f42-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

## <a name="overview"></a><span data-ttu-id="b9f42-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b9f42-105">Overview</span></span>

<span data-ttu-id="b9f42-106">Используйте проекты массового набора сотрудников, когда одновременно нанимается много работников, например, при найме для удовлетворения сезонного спроса.</span><span class="sxs-lookup"><span data-stu-id="b9f42-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="b9f42-107">Создание проекта массового набора сотрудников может быть полезным, так как оно позволяет одновременно создать записи должностей, записи работников и назначения работников.</span><span class="sxs-lookup"><span data-stu-id="b9f42-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="b9f42-108">При создании должностей для проекта массового набора сотрудников можно указать следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="b9f42-108">When you create positions for a mass hire project, you can specify the following information:</span></span>

- <span data-ttu-id="b9f42-109">Число создаваемых должностей</span><span class="sxs-lookup"><span data-stu-id="b9f42-109">The number of positions to create</span></span>
- <span data-ttu-id="b9f42-110">Тип работника для сотрудников, нанимаемых на должности</span><span class="sxs-lookup"><span data-stu-id="b9f42-110">The worker type of the people that you will hire for the positions</span></span>
- <span data-ttu-id="b9f42-111">Подразделение и должность, связанные с вакансиями</span><span class="sxs-lookup"><span data-stu-id="b9f42-111">The department and the job that are associated with the positions</span></span>
- <span data-ttu-id="b9f42-112">Аналог должности при полной занятости</span><span class="sxs-lookup"><span data-stu-id="b9f42-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="b9f42-113">Пример</span><span class="sxs-lookup"><span data-stu-id="b9f42-113">Example</span></span>

<span data-ttu-id="b9f42-114">В течение лета вы обычно нанимаете на частичную занятость 15-20 студентов, чтобы заполнить свободные должности стажеров в вашей компании.</span><span class="sxs-lookup"><span data-stu-id="b9f42-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="b9f42-115">В этом году вам необходимо нанять пять бухгалтеров, пять обработчиков заказов и пять кассиров.</span><span class="sxs-lookup"><span data-stu-id="b9f42-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="b9f42-116">Вместо создания каждой из записей должностей и работников по отдельности вы создаете один проект по массовому набору сотрудников под названием "SummerInterns" (Стажеры – лето).</span><span class="sxs-lookup"><span data-stu-id="b9f42-116">Instead of creating each position record and worker record separately, you create one mass hire project called "SummerInterns".</span></span> <span data-ttu-id="b9f42-117">Даты начала и конца проекта соответствуют датам начала и конца срока действия должностей, для которых создается проект по массовому набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b9f42-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span>

<span data-ttu-id="b9f42-118">На странице **Проекты по массовому набору сотрудников** выберите проект "SummerInterns", и после этого щелкните **Открыть проект**.</span><span class="sxs-lookup"><span data-stu-id="b9f42-118">In the **Mass hire projects** page, select the "SummerInterns" project and then click **Open project**.</span></span> <span data-ttu-id="b9f42-119">В открытом проекте массового набора сотрудников щелкните **Создание должностей** и введите сведения о должности бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="b9f42-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="b9f42-120">Можно указать, что требуется создать пять должностей бухгалтеров с теми же сведениями для каждой должности, и нажать кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="b9f42-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="b9f42-121">Повторите эту процедуру для должностей обработчиков заказов и кассиров.</span><span class="sxs-lookup"><span data-stu-id="b9f42-121">Repeat this process for the order processor and cashier positions.</span></span>

<span data-ttu-id="b9f42-122">После выбора студентов для найма на должности стажеров вы введете сведения о каждом из студентов в **Сведения по должностям** для должностей, по которым производится прием на работу.</span><span class="sxs-lookup"><span data-stu-id="b9f42-122">After selecting students to hire for the internship positions, you'll enter each student's information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="b9f42-123">После того, как будут введены все сведения по должностям, выберите должность на странице "Проекты по массовому набору сотрудников" и нажмите кнопку **Прием на работу**.</span><span class="sxs-lookup"><span data-stu-id="b9f42-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="b9f42-124">Для каждой из должностей будет создана запись должности, также для каждого из нанимаемых лиц будет создана и назначена соответствующей должности запись работника.</span><span class="sxs-lookup"><span data-stu-id="b9f42-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="b9f42-125">Статусы проектов по массовому набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="b9f42-125">Mass hire project statuses</span></span>

<span data-ttu-id="b9f42-126">Проект по массовому набору сотрудников может иметь один из следующих статусов.</span><span class="sxs-lookup"><span data-stu-id="b9f42-126">A mass hire project can have the following statuses.</span></span>

- <span data-ttu-id="b9f42-127">Создан</span><span class="sxs-lookup"><span data-stu-id="b9f42-127">Created</span></span>
- <span data-ttu-id="b9f42-128">Открытое</span><span class="sxs-lookup"><span data-stu-id="b9f42-128">Open</span></span>
- <span data-ttu-id="b9f42-129">Закрыт</span><span class="sxs-lookup"><span data-stu-id="b9f42-129">Closed</span></span>

<span data-ttu-id="b9f42-130">На странице **Проект по массовому набору сотрудников** щелкните **Открыть проект** или **Закрыть проект** для того, чтобы изменить статус проекта по массовому набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b9f42-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="b9f42-131">В следующей таблице приводятся сведения о том, какие действия над проектом возможны в зависимости от его статуса.</span><span class="sxs-lookup"><span data-stu-id="b9f42-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b9f42-132">Состояние</span><span class="sxs-lookup"><span data-stu-id="b9f42-132">Status</span></span></th>
<th><span data-ttu-id="b9f42-133">Описание</span><span class="sxs-lookup"><span data-stu-id="b9f42-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b9f42-134">Создан</span><span class="sxs-lookup"><span data-stu-id="b9f42-134">Created</span></span></td>
<td><span data-ttu-id="b9f42-135">Можно создавать и изменять информацию, но нельзя создавать должности для проекта.</span><span class="sxs-lookup"><span data-stu-id="b9f42-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="b9f42-136">Это статус по умолчанию для новых проектов.</span><span class="sxs-lookup"><span data-stu-id="b9f42-136">This is the default status for new projects.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b9f42-137">Открытое</span><span class="sxs-lookup"><span data-stu-id="b9f42-137">Open</span></span></td>
<td><span data-ttu-id="b9f42-138">Можно изменять сведения о проекте, создавать должности для проекта по массовому набору сотрудников, и нанимать людей на должности.</span><span class="sxs-lookup"><span data-stu-id="b9f42-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="b9f42-139">Этот статус имеют активные проекты.</span><span class="sxs-lookup"><span data-stu-id="b9f42-139">This is the status for active projects.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b9f42-140">Закрыт</span><span class="sxs-lookup"><span data-stu-id="b9f42-140">Closed</span></span></td>
<td><span data-ttu-id="b9f42-141">Добавлять должности в проект невозможно.</span><span class="sxs-lookup"><span data-stu-id="b9f42-141">You cannot add positions to the project.</span></span> <span data-ttu-id="b9f42-142">Для добавления должностей в проект по массовому набору сотрудников откройте проект повторно.</span><span class="sxs-lookup"><span data-stu-id="b9f42-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="b9f42-143">Этот статус используется для завершенных проектов.</span><span class="sxs-lookup"><span data-stu-id="b9f42-143">This is the status for completed projects.</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b9f42-144">Перед закрытием проекта по массовому набору сотрудников все должности в проекте должны иметь либо статус "Создано", либо статус "Закрыто".</span><span class="sxs-lookup"><span data-stu-id="b9f42-144">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></blockquote>
</td>
</tr>
</tbody>
</table>
