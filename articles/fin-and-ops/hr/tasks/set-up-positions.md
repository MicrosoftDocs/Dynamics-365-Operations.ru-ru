---
title: Настройка должностей
description: Должности являются важным элементом нижнего уровня организационной иерархии.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fd355fb6c3d2742e046a616585ca349c623341d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "856838"
---
# <a name="set-up-positions"></a><span data-ttu-id="d35be-103">Настройка должностей</span><span class="sxs-lookup"><span data-stu-id="d35be-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d35be-104">Должности являются важным элементом нижнего уровня организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="d35be-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="d35be-105">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="d35be-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="d35be-106">Например, должность «Менеджер по продажам (восток)» — это одна из должностей, связанных с общей должностью, «Менеджер по продажам».</span><span class="sxs-lookup"><span data-stu-id="d35be-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="d35be-107">Должность существует в подразделении, и ей можно назначить только одного работника.</span><span class="sxs-lookup"><span data-stu-id="d35be-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="d35be-108">В этой задаче рассматриваются шаги, которые необходимо выполнить для создания должности.</span><span class="sxs-lookup"><span data-stu-id="d35be-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="d35be-109">Эта процедура предназначена для специалиста по управлению персоналом.</span><span class="sxs-lookup"><span data-stu-id="d35be-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="d35be-110">Щелкните "Управление трудовыми ресурсами".</span><span class="sxs-lookup"><span data-stu-id="d35be-110">Click Workforce management.</span></span>
2. <span data-ttu-id="d35be-111">Щелкните "Открытые позиции".</span><span class="sxs-lookup"><span data-stu-id="d35be-111">Click Open positions.</span></span>
3. <span data-ttu-id="d35be-112">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d35be-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="d35be-113">В поле "Задание" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="d35be-114">Должностные обязанности, должность и коэффициент занятости эквивалента полной занятости автоматически копируются из выбранного задания в должность.</span><span class="sxs-lookup"><span data-stu-id="d35be-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="d35be-115">Разрешить изменения задания.</span><span class="sxs-lookup"><span data-stu-id="d35be-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="d35be-116">Щелкните "Создать должность".</span><span class="sxs-lookup"><span data-stu-id="d35be-116">Click Create position.</span></span>
7. <span data-ttu-id="d35be-117">В поле "Подразделение" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="d35be-118">В поле "Тип должности" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="d35be-119">В поле "Регион компенсации" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="d35be-120">Поле "Регион компенсации" определяет правила приемлемости компенсации и бюджеты фиксированных увеличений, которые применяются к сотруднику на данной должности.</span><span class="sxs-lookup"><span data-stu-id="d35be-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="d35be-121">В поле "Доступна для назначения" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d35be-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="d35be-122">Разверните раздел "Период должности".</span><span class="sxs-lookup"><span data-stu-id="d35be-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="d35be-123">Период должности вводится по умолчанию на основании дат активации и выбытия, введенных ранее.</span><span class="sxs-lookup"><span data-stu-id="d35be-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="d35be-124">Разверните раздел "Отчитывается перед должностью".</span><span class="sxs-lookup"><span data-stu-id="d35be-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="d35be-125">При назначении работника на должность, подотчетную другой должности, создается связь непосредственного подчиненного между работниками, назначенными на две должности.</span><span class="sxs-lookup"><span data-stu-id="d35be-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="d35be-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d35be-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="d35be-127">В поле "Отчитывается перед" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="d35be-128">Щелкните Создать.</span><span class="sxs-lookup"><span data-stu-id="d35be-128">Click Create.</span></span>
16. <span data-ttu-id="d35be-129">Разверните раздел "Назначение работника".</span><span class="sxs-lookup"><span data-stu-id="d35be-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="d35be-130">Разверните раздел "Отношения".</span><span class="sxs-lookup"><span data-stu-id="d35be-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="d35be-131">Если ваша организация использует матричную иерархию или другую специальную иерархию, можно настроить типы иерархии должностей и затем добавить отношения подотчетности для должностей для каждого настроенного типа иерархии.</span><span class="sxs-lookup"><span data-stu-id="d35be-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="d35be-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d35be-132">Click Add.</span></span>
19. <span data-ttu-id="d35be-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d35be-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="d35be-134">В поле "Имя иерархии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="d35be-135">В поле "Отчитывается перед должностью" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="d35be-136">Разверните раздел "Заработная плата".</span><span class="sxs-lookup"><span data-stu-id="d35be-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="d35be-137">В поле "Цикл оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="d35be-138">В поле "Кем оплачивается" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="d35be-139">В поле "Обычные часы за год" введите число.</span><span class="sxs-lookup"><span data-stu-id="d35be-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="d35be-140">Это количество регулярно оплачиваемых часов, в течение которых работник на данной должности должен работать каждый год.</span><span class="sxs-lookup"><span data-stu-id="d35be-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="d35be-141">Разверните раздел "Профсоюз".</span><span class="sxs-lookup"><span data-stu-id="d35be-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="d35be-142">Сверните раздел "Профсоюз".</span><span class="sxs-lookup"><span data-stu-id="d35be-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="d35be-143">Разверните раздел "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="d35be-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="d35be-144">В поле "Шаблон распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="d35be-145">В поле "Подразделение" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d35be-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="d35be-146">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d35be-146">Click Save.</span></span>

