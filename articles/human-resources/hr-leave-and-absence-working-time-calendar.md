---
title: Создание календаря рабочего времени
description: Определите календарь рабочего времени, праздники и отсутствие в Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/01/2020
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
ms.openlocfilehash: ecabac54134629074ac01944963a037c2cdc63c9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467177"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="99e99-103">Создание календаря рабочего времени</span><span class="sxs-lookup"><span data-stu-id="99e99-103">Create a working time calendar</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="99e99-104">Календарь рабочего времени в Dynamics 365 Human Resources отображает дни и часы, которые сотрудники работают в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="99e99-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="99e99-105">Когда сотрудник отправит запрос об отсутствии, ему не придется беспокоиться о праздниках и нерабочих днях.</span><span class="sxs-lookup"><span data-stu-id="99e99-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="99e99-106">Чтобы упростить запросы отсутствия, настройте эти элементы для организации:</span><span class="sxs-lookup"><span data-stu-id="99e99-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="99e99-107">Календарь рабочего времени</span><span class="sxs-lookup"><span data-stu-id="99e99-107">Working time calendar</span></span>
- <span data-ttu-id="99e99-108">Праздники и нерабочие дни</span><span class="sxs-lookup"><span data-stu-id="99e99-108">Holidays and closures</span></span>
- <span data-ttu-id="99e99-109">Нерабочее время</span><span class="sxs-lookup"><span data-stu-id="99e99-109">Non-work time</span></span>

<span data-ttu-id="99e99-110">Можно добавить последние два элемента во время настройки календаря рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="99e99-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="99e99-111">Можно также настраивать и обновлять их отдельно.</span><span class="sxs-lookup"><span data-stu-id="99e99-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="99e99-112">Настройка календаря рабочего времени</span><span class="sxs-lookup"><span data-stu-id="99e99-112">Set up a working time calendar</span></span>

<span data-ttu-id="99e99-113">Настройте по крайней мере один календарь рабочего времени, который показывает дни и часы работы.</span><span class="sxs-lookup"><span data-stu-id="99e99-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="99e99-114">Если имеются местоположения в нескольких странах и регионах, может потребоваться настроить календарь рабочего времени для каждой области.</span><span class="sxs-lookup"><span data-stu-id="99e99-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="99e99-115">На странице **Администрирование организации** щелкните **Календари**.</span><span class="sxs-lookup"><span data-stu-id="99e99-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="99e99-116">Выберите **Создать**, а затем введите название и описание календаря.</span><span class="sxs-lookup"><span data-stu-id="99e99-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="99e99-117">В **Параметры создания** выберите рабочие дни для организации и введите рабочее время.</span><span class="sxs-lookup"><span data-stu-id="99e99-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="99e99-118">Чтобы добавить праздник или нерабочий день, нажмите кнопку **Добавить** рядом **Праздники и нерабочие дни**.</span><span class="sxs-lookup"><span data-stu-id="99e99-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="99e99-119">Чтобы добавить время, не являющееся рабочим временем, например обеды или перерывы, выберите **Добавить** в **НЕРАБОЧЕЕ ВРЕМЯ** и введите имя и диапазон времени.</span><span class="sxs-lookup"><span data-stu-id="99e99-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="99e99-120">В **Дни** выберите **Создать**, чтобы сформировать дни в вашем календаре.</span><span class="sxs-lookup"><span data-stu-id="99e99-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="99e99-121">Введите диапазон дат для календаря, а затем выберите **Создать дни**.</span><span class="sxs-lookup"><span data-stu-id="99e99-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="99e99-122">Чтобы добавить рабочие расписания в **График работы**, выберите **Добавить**, а затем введите значения времени для каждого графика работы.</span><span class="sxs-lookup"><span data-stu-id="99e99-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="99e99-123">Настройка праздников и нерабочих дней</span><span class="sxs-lookup"><span data-stu-id="99e99-123">Configure holidays and closures</span></span>

<span data-ttu-id="99e99-124">Праздники и нерабочие дни можно добавлять или изменять отдельно от календаря рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="99e99-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="99e99-125">На странице **Администрирование организации** щелкните **Праздники и нерабочие дни**.</span><span class="sxs-lookup"><span data-stu-id="99e99-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="99e99-126">Выберите **Создать**, а затем введите название и дату праздника или нерабочего дня.</span><span class="sxs-lookup"><span data-stu-id="99e99-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="99e99-127">Настройка нерабочего времени</span><span class="sxs-lookup"><span data-stu-id="99e99-127">Configure non-work time</span></span>

<span data-ttu-id="99e99-128">Нерабочее время можно добавлять или изменять отдельно от календаря рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="99e99-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="99e99-129">На странице **Администрирование организации** щелкните **Нерабочее время**.</span><span class="sxs-lookup"><span data-stu-id="99e99-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="99e99-130">Выберите **Создать** и введите имя и диапазон времени для нерабочего времени.</span><span class="sxs-lookup"><span data-stu-id="99e99-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="99e99-131">Если вы включили функцию предварительного просмотра корректировок для государственных праздников для отпуска и отсутствия, Human Resources даты праздников и нерабочих дней для определения количества дней для корректировки для сотрудников, зарегистрированных в календаре.</span><span class="sxs-lookup"><span data-stu-id="99e99-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="99e99-132">См. также</span><span class="sxs-lookup"><span data-stu-id="99e99-132">See also</span></span>

- [<span data-ttu-id="99e99-133">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="99e99-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="99e99-134">Настройка типов отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="99e99-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]