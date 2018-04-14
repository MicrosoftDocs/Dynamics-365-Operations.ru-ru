--- 
title: "Ввод табелей учета рабочего времени проекта"
description: "Эта процедура позволят создать табель учета рабочего времени с помощью пустой формы такого табеля."
author: kherr75
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fdc9567040a2ea4e50325c98a2da19da039586bb
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="enter-project-timesheets"></a><span data-ttu-id="7d2ad-103">Ввод табелей учета рабочего времени проекта</span><span class="sxs-lookup"><span data-stu-id="7d2ad-103">Enter project timesheets</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d2ad-104">Эта процедура позволят создать табель учета рабочего времени с помощью пустой формы такого табеля.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="7d2ad-105">Новый табель учета рабочего времени можно создать на основе сведений из предыдущего табеля или из назначений проекта и действий на странице "Избранное".</span><span class="sxs-lookup"><span data-stu-id="7d2ad-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="7d2ad-106">По умолчанию на странице списка "Все табели учета рабочего времени" показаны все табели учета рабочего времени за текущий период.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="7d2ad-107">Можно использовать раскрывающийся список в поле "Показать" на странице "Мои табели учета рабочего времени", чтобы отфильтровать список табелей по периоду времени или проекту или для просмотра табелей, которые были созданы от имени других работников.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="7d2ad-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USSI.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="7d2ad-109">Чтобы начать эту процедуру, перейдите в раздел "Управление и учет по проектам" > "Табели учета рабочего времени" > "Мои табели учета рабочего времени".</span><span class="sxs-lookup"><span data-stu-id="7d2ad-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="7d2ad-110">Чтобы ввести новый табель учета рабочего времени, щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7d2ad-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="7d2ad-111">В раскрывающемся списке "Ресурса" отображается работник, по умолчанию назначенный текущему пользователю.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="7d2ad-112">Если пользователь определен как представитель, здесь будут перечислены имена, чтобы пользователь мог ввести табель от их имени.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="7d2ad-113">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="7d2ad-114">Если выбран этот параметр, новые строки табеля будут создаваться с использованием параметров табелей, которые были установлены как избранное.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="7d2ad-115">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="7d2ad-115">Click OK.</span></span>
4. <span data-ttu-id="7d2ad-116">Щелкните "Новая строка".</span><span class="sxs-lookup"><span data-stu-id="7d2ad-116">Click New line.</span></span>
5. <span data-ttu-id="7d2ad-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d2ad-118">В поле "Юридическое лицо" отображается текущее юридическое лицо по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="7d2ad-119">В поле "Проект" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7d2ad-120">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7d2ad-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7d2ad-122">В поле "Мероприятие" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="7d2ad-123">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="7d2ad-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="7d2ad-125">В поле "Категория" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="7d2ad-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="7d2ad-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="7d2ad-128">Введите количество часов, отработанных в каждый из дней.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="7d2ad-129">Часы должны быть введены в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="7d2ad-130">Например, если вы проработали два часа и пятнадцать минут, введите значение 2,25.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="7d2ad-131">Введите количество часов, отработанных в каждый из дней.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="7d2ad-132">Часы должны быть введены в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="7d2ad-133">Например, если вы проработали два часа и пятнадцать минут, введите значение 2,25.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="7d2ad-134">Введите количество часов, отработанных в каждый из дней.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="7d2ad-135">Часы должны быть введены в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="7d2ad-136">Например, если вы проработали два часа и пятнадцать минут, введите значение 2,25.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="7d2ad-137">Введите количество часов, отработанных в каждый из дней.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="7d2ad-138">Часы должны быть введены в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="7d2ad-139">Например, если вы проработали два часа и пятнадцать минут, введите значение 2,25.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="7d2ad-140">Введите количество часов, отработанных в каждый из дней.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="7d2ad-141">Часы должны быть введены в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="7d2ad-142">Например, если вы проработали два часа и пятнадцать минут, введите значение 2,25.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="7d2ad-143">В сведениях о строке доступны следующие параметры:  o  Добавить сведения о налогах и финансовых аналитиках.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="7d2ad-144">o    Добавить комментарии о строке табеля.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="7d2ad-145">Щелкните "Документооборот", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="7d2ad-146">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-146">Click Submit.</span></span>
22. <span data-ttu-id="7d2ad-147">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="7d2ad-147">Click Submit.</span></span>


