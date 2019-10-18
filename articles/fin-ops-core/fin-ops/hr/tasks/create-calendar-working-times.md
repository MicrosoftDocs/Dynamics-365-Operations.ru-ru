---
title: Создание календарей и создание рабочего времени
description: Календари описывают производительность и рабочее время операционных ресурсов. В этой теме объясняется, как определить рабочий календарь на основе шаблона рабочего времени.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50b81ae228d9aee4111ce8d161508d5ed1af4f27
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190680"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="8bfe6-104">Создание календаря и создание рабочих времен</span><span class="sxs-lookup"><span data-stu-id="8bfe6-104">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8bfe6-105">Календари описывают производительность и рабочее время операционных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="8bfe6-106">В этой теме объясняется, как определить рабочий календарь на основе шаблона рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-106">This topic explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="8bfe6-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="8bfe6-108">На главной странице выберите **Управление жизненным циклом ресурса**.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="8bfe6-109">Выберите **Календари**.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="8bfe6-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-110">Select **New**.</span></span>
4. <span data-ttu-id="8bfe6-111">В поле **Календарь** классифицируйте календарь.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="8bfe6-112">Это код календаря, используемый в качестве ссылки при назначении календарей, таких как операционные ресурсы или группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="8bfe6-113">В поле **Имя** задайте имя календаря.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="8bfe6-114">В поле **Стандартный рабочий день в часах** введите число.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="8bfe6-115">Убедитесь, что строка выбрана, затем выберите **Рабочее время** из панели операций.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="8bfe6-116">Выберите **Формирование опер. времен**.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-116">Select **Compose working times**.</span></span> <span data-ttu-id="8bfe6-117">Создание рабочих часов для каждого дня периода, где можно будет планировать работу.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="8bfe6-118">С течением времени можно создать рабочее время для дополнительных периодов.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="8bfe6-119">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="8bfe6-120">Это первый день, в который должен начинаться этот календарь.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="8bfe6-121">В поле **Дата окончания** введите дату.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="8bfe6-122">Это последний день, в который календарь открыт.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="8bfe6-123">В поле **Шаблон расписания** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="8bfe6-124">Шаблон рабочего времени определяет рабочие часы для каждого дня недели.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="8bfe6-125">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-125">Select **OK**.</span></span>
13. <span data-ttu-id="8bfe6-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bfe6-126">Close the page.</span></span>

