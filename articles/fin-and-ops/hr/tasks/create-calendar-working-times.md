--- 
title: "Создание календаря и создание рабочего времени"
description: "Календари описывают производительность и рабочее время операционных ресурсов."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 97751310cee3441d80d57860bc90490cf5708de2
ms.contentlocale: ru-ru
ms.lasthandoff: 02/02/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="4d10f-103">Создание календаря и создание рабочего времени</span><span class="sxs-lookup"><span data-stu-id="4d10f-103">Create a calendar and generate working times</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d10f-104">Календари описывают производительность и рабочее время операционных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d10f-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="4d10f-105">Эта процедура поможет определить рабочий календарь на основе шаблона рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="4d10f-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="4d10f-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="4d10f-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="4d10f-107">Перейдите в раздел "Все рабочие области" > "Управление жизненным циклом ресурса".</span><span class="sxs-lookup"><span data-stu-id="4d10f-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="4d10f-108">Щелкните "Календари".</span><span class="sxs-lookup"><span data-stu-id="4d10f-108">Click Calendars.</span></span>
3. <span data-ttu-id="4d10f-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4d10f-109">Click New.</span></span>
4. <span data-ttu-id="4d10f-110">В поле "Календарь" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4d10f-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="4d10f-111">Это код календаря, используемый в качестве ссылки при назначении календарей, таких как операционные ресурсы или группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d10f-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="4d10f-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4d10f-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="4d10f-113">В поле "Стандартный рабочий день в часах" введите число.</span><span class="sxs-lookup"><span data-stu-id="4d10f-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="4d10f-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4d10f-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4d10f-115">Щелкните "Рабочее время".</span><span class="sxs-lookup"><span data-stu-id="4d10f-115">Click Working times.</span></span>
9. <span data-ttu-id="4d10f-116">Щелкните "Формирование операционных времен".</span><span class="sxs-lookup"><span data-stu-id="4d10f-116">Click Compose working times.</span></span>
    * <span data-ttu-id="4d10f-117">Создание рабочих часов для каждого дня периода, где можно будет планировать работу.</span><span class="sxs-lookup"><span data-stu-id="4d10f-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="4d10f-118">С течением времени можно создать рабочее время для дополнительных периодов.</span><span class="sxs-lookup"><span data-stu-id="4d10f-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="4d10f-119">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="4d10f-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4d10f-120">Это первый день, в который должен начинаться этот календарь.</span><span class="sxs-lookup"><span data-stu-id="4d10f-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="4d10f-121">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="4d10f-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="4d10f-122">Это последний день, в который календарь открыт.</span><span class="sxs-lookup"><span data-stu-id="4d10f-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="4d10f-123">В поле "Шаблон расписания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4d10f-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="4d10f-124">Шаблон рабочего времени определяет рабочие часы для каждого дня недели.</span><span class="sxs-lookup"><span data-stu-id="4d10f-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="4d10f-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4d10f-125">Click OK.</span></span>
14. <span data-ttu-id="4d10f-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4d10f-126">Close the page.</span></span>


