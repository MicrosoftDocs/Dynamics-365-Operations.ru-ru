---
title: Ввод табелей учета рабочего времени проекта
description: Эта процедура позволят создать табель учета рабочего времени с помощью пустой формы такого табеля.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 136efa1178089adb88820002a19e99ef83e1b47e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010369"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="740d2-103">Ввод табелей учета рабочего времени проекта</span><span class="sxs-lookup"><span data-stu-id="740d2-103">Enter project timesheets</span></span>



<span data-ttu-id="740d2-104">Эта процедура позволят создать табель учета рабочего времени с помощью пустой формы такого табеля.</span><span class="sxs-lookup"><span data-stu-id="740d2-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="740d2-105">Новый табель учета рабочего времени можно создать на основе сведений из предыдущего табеля или из назначений проекта и действий на странице **Избранное**.</span><span class="sxs-lookup"><span data-stu-id="740d2-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="740d2-106">По умолчанию на странице списка **Все табели учета рабочего времени** показаны все табели учета рабочего времени за текущий период.</span><span class="sxs-lookup"><span data-stu-id="740d2-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="740d2-107">Можно использовать раскрывающийся список в поле **Показать** на странице **Мои табели учета рабочего времени**, чтобы отфильтровать список табелей по периоду времени или проекту или для просмотра табелей, которые были созданы от имени других работников.</span><span class="sxs-lookup"><span data-stu-id="740d2-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="740d2-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USSI.</span><span class="sxs-lookup"><span data-stu-id="740d2-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="740d2-109">В **области переходов** выберите **Модули > Управление и учет по проектам > Табели учета рабочего времени > Мои табели учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="740d2-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="740d2-110">Чтобы ввести новый табель учета рабочего времени, щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="740d2-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="740d2-111">В раскрывающемся списке "Ресурса" отображается работник, по умолчанию назначенный текущему пользователю.</span><span class="sxs-lookup"><span data-stu-id="740d2-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="740d2-112">Если пользователь определен как представитель, здесь будут перечислены имена, чтобы пользователь мог ввести табель от их имени.</span><span class="sxs-lookup"><span data-stu-id="740d2-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="740d2-113">В поле **Дата** введите дату.</span><span class="sxs-lookup"><span data-stu-id="740d2-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="740d2-114">Если выбран этот параметр, новые строки табеля будут создаваться с использованием параметров табелей, которые были установлены как избранное.</span><span class="sxs-lookup"><span data-stu-id="740d2-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="740d2-115">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="740d2-115">Click **OK**.</span></span>
5. <span data-ttu-id="740d2-116">Щелкните **Новая строка**.</span><span class="sxs-lookup"><span data-stu-id="740d2-116">Click **New line**.</span></span>
6. <span data-ttu-id="740d2-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="740d2-117">In the list, mark the selected row.</span></span> <span data-ttu-id="740d2-118">В поле **Юридическое лицо** отображается текущее юридическое лицо по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="740d2-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="740d2-119">В поле **Проект** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="740d2-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="740d2-120">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="740d2-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="740d2-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="740d2-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="740d2-122">В поле **Номер мероприятия** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="740d2-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="740d2-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="740d2-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="740d2-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="740d2-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="740d2-125">В поле **Категория** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="740d2-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="740d2-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="740d2-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="740d2-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="740d2-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="740d2-128">Введите количество часов, отработанных в каждый из дней.</span><span class="sxs-lookup"><span data-stu-id="740d2-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="740d2-129">Вводите количество часов в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="740d2-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="740d2-130">Например, если вы проработали два часа и пятнадцать минут, введите значение 2,25.</span><span class="sxs-lookup"><span data-stu-id="740d2-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="740d2-131">В поле **Сведения по строке** доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="740d2-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="740d2-132">Добавьте информацию о налогах и финансовых аналитиках на вкладке **Общие** и **Финансовые аналитики**.</span><span class="sxs-lookup"><span data-stu-id="740d2-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="740d2-133">Добавьте комментарии к строке табеля на вкладке **Комментарии**.</span><span class="sxs-lookup"><span data-stu-id="740d2-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="740d2-134">На **Панели операций** щелкните **Рабочий процесс**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="740d2-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="740d2-135">Щелкните **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="740d2-135">Click **Submit**.</span></span>
22. <span data-ttu-id="740d2-136">Щелкните **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="740d2-136">Click **Submit**.</span></span>

