---
title: Создание календаря рабочего времени
description: Определите календарь рабочего времени, праздники и отсутствие в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ea55ad7f86e0c7d5ccc6e6de0af475299b05639
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052441"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="f8678-103">Создание календаря рабочего времени</span><span class="sxs-lookup"><span data-stu-id="f8678-103">Create a working time calendar</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f8678-104">Календарь рабочего времени в Dynamics 365 Human Resources отображает дни и часы, которые сотрудники работают в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f8678-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="f8678-105">Когда сотрудник отправит запрос об отсутствии, ему не придется беспокоиться о праздниках и нерабочих днях.</span><span class="sxs-lookup"><span data-stu-id="f8678-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="f8678-106">Чтобы упростить запросы отсутствия, настройте эти элементы для организации:</span><span class="sxs-lookup"><span data-stu-id="f8678-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="f8678-107">Календарь рабочего времени</span><span class="sxs-lookup"><span data-stu-id="f8678-107">Working time calendar</span></span>
- <span data-ttu-id="f8678-108">Праздники и нерабочие дни</span><span class="sxs-lookup"><span data-stu-id="f8678-108">Holidays and closures</span></span>
- <span data-ttu-id="f8678-109">Нерабочее время</span><span class="sxs-lookup"><span data-stu-id="f8678-109">Non-work time</span></span>

<span data-ttu-id="f8678-110">Можно добавить последние два элемента во время настройки календаря рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="f8678-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="f8678-111">Можно также настраивать и обновлять их отдельно.</span><span class="sxs-lookup"><span data-stu-id="f8678-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="f8678-112">Настройка календаря рабочего времени</span><span class="sxs-lookup"><span data-stu-id="f8678-112">Set up a working time calendar</span></span>

<span data-ttu-id="f8678-113">Настройте по крайней мере один календарь рабочего времени, который показывает дни и часы работы.</span><span class="sxs-lookup"><span data-stu-id="f8678-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="f8678-114">Если имеются местоположения в нескольких странах и регионах, может потребоваться настроить календарь рабочего времени для каждой области.</span><span class="sxs-lookup"><span data-stu-id="f8678-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="f8678-115">На странице **Администрирование организации** щелкните **Календари**.</span><span class="sxs-lookup"><span data-stu-id="f8678-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="f8678-116">Выберите **Создать**, а затем введите название и описание календаря.</span><span class="sxs-lookup"><span data-stu-id="f8678-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="f8678-117">В **Параметры создания** выберите рабочие дни для организации и введите рабочее время.</span><span class="sxs-lookup"><span data-stu-id="f8678-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="f8678-118">Чтобы добавить праздник или нерабочий день, нажмите кнопку **Добавить** рядом **Праздники и нерабочие дни**.</span><span class="sxs-lookup"><span data-stu-id="f8678-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="f8678-119">Чтобы добавить время, не являющееся рабочим временем, например обеды или перерывы, выберите **Добавить** в **НЕРАБОЧЕЕ ВРЕМЯ** и введите имя и диапазон времени.</span><span class="sxs-lookup"><span data-stu-id="f8678-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="f8678-120">В **Дни** выберите **Создать**, чтобы сформировать дни в вашем календаре.</span><span class="sxs-lookup"><span data-stu-id="f8678-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="f8678-121">Введите диапазон дат для календаря, а затем выберите **Создать дни**.</span><span class="sxs-lookup"><span data-stu-id="f8678-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="f8678-122">Чтобы добавить рабочие расписания в **График работы**, выберите **Добавить**, а затем введите значения времени для каждого графика работы.</span><span class="sxs-lookup"><span data-stu-id="f8678-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="f8678-123">Настройка праздников и нерабочих дней</span><span class="sxs-lookup"><span data-stu-id="f8678-123">Configure holidays and closures</span></span>

<span data-ttu-id="f8678-124">Праздники и нерабочие дни можно добавлять или изменять отдельно от календаря рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="f8678-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="f8678-125">На странице **Администрирование организации** щелкните **Праздники и нерабочие дни**.</span><span class="sxs-lookup"><span data-stu-id="f8678-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="f8678-126">Выберите **Создать**, а затем введите название и дату праздника или нерабочего дня.</span><span class="sxs-lookup"><span data-stu-id="f8678-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="f8678-127">Настройка нерабочего времени</span><span class="sxs-lookup"><span data-stu-id="f8678-127">Configure non-work time</span></span>

<span data-ttu-id="f8678-128">Нерабочее время можно добавлять или изменять отдельно от календаря рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="f8678-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="f8678-129">На странице **Администрирование организации** щелкните **Нерабочее время**.</span><span class="sxs-lookup"><span data-stu-id="f8678-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="f8678-130">Выберите **Создать** и введите имя и диапазон времени для нерабочего времени.</span><span class="sxs-lookup"><span data-stu-id="f8678-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="f8678-131">Если вы включили функцию предварительного просмотра корректировок для государственных праздников для отпуска и отсутствия, Human Resources даты праздников и нерабочих дней для определения количества дней для корректировки для сотрудников, зарегистрированных в календаре.</span><span class="sxs-lookup"><span data-stu-id="f8678-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8678-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f8678-132">See also</span></span>

- [<span data-ttu-id="f8678-133">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="f8678-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="f8678-134">Настройка типов отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="f8678-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]