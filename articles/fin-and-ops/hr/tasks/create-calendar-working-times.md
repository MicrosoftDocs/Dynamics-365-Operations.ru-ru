---
title: Создание календаря и создание рабочих времен
description: Календари описывают производительность и рабочее время операционных ресурсов.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: ba4bd51d2102b3036307f34ab46f94f83df4f461
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "856999"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="1c846-103">Создание календаря и создание рабочих времен</span><span class="sxs-lookup"><span data-stu-id="1c846-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c846-104">Календари описывают производительность и рабочее время операционных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c846-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="1c846-105">Эта процедура поможет определить рабочий календарь на основе шаблона рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="1c846-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="1c846-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="1c846-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="1c846-107">Перейдите в раздел "Все рабочие области" > "Управление жизненным циклом ресурса".</span><span class="sxs-lookup"><span data-stu-id="1c846-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="1c846-108">Щелкните "Календари".</span><span class="sxs-lookup"><span data-stu-id="1c846-108">Click Calendars.</span></span>
3. <span data-ttu-id="1c846-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1c846-109">Click New.</span></span>
4. <span data-ttu-id="1c846-110">В поле "Календарь" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1c846-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="1c846-111">Это код календаря, используемый в качестве ссылки при назначении календарей, таких как операционные ресурсы или группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c846-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="1c846-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1c846-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="1c846-113">В поле "Стандартный рабочий день в часах" введите число.</span><span class="sxs-lookup"><span data-stu-id="1c846-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="1c846-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1c846-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1c846-115">Щелкните "Рабочее время".</span><span class="sxs-lookup"><span data-stu-id="1c846-115">Click Working times.</span></span>
9. <span data-ttu-id="1c846-116">Щелкните "Формирование операционных времен".</span><span class="sxs-lookup"><span data-stu-id="1c846-116">Click Compose working times.</span></span>
    * <span data-ttu-id="1c846-117">Создание рабочих часов для каждого дня периода, где можно будет планировать работу.</span><span class="sxs-lookup"><span data-stu-id="1c846-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="1c846-118">С течением времени можно создать рабочее время для дополнительных периодов.</span><span class="sxs-lookup"><span data-stu-id="1c846-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="1c846-119">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1c846-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="1c846-120">Это первый день, в который должен начинаться этот календарь.</span><span class="sxs-lookup"><span data-stu-id="1c846-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="1c846-121">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1c846-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="1c846-122">Это последний день, в который календарь открыт.</span><span class="sxs-lookup"><span data-stu-id="1c846-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="1c846-123">В поле "Шаблон расписания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1c846-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="1c846-124">Шаблон рабочего времени определяет рабочие часы для каждого дня недели.</span><span class="sxs-lookup"><span data-stu-id="1c846-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="1c846-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1c846-125">Click OK.</span></span>
14. <span data-ttu-id="1c846-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1c846-126">Close the page.</span></span>

