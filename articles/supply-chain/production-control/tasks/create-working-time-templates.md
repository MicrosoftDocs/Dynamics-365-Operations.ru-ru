--- 
title: "Создание шаблонов рабочего времени"
description: "Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="2b108-103">Создание шаблонов рабочего времени</span><span class="sxs-lookup"><span data-stu-id="2b108-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b108-104">Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени.</span><span class="sxs-lookup"><span data-stu-id="2b108-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="2b108-105">Эта процедура описывает определение шаблона рабочего времени с помощью свойств планирования рабочего времени для классификации интервалов рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="2b108-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="2b108-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="2b108-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="2b108-107">Перейдите в раздел "Все рабочие области" > "Управление жизненным циклом ресурса".</span><span class="sxs-lookup"><span data-stu-id="2b108-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="2b108-108">Щелкните "Шаблоны расписания".</span><span class="sxs-lookup"><span data-stu-id="2b108-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="2b108-109">Создание шаблона рабочего времени</span><span class="sxs-lookup"><span data-stu-id="2b108-109">Create working time template</span></span>
1. <span data-ttu-id="2b108-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2b108-110">Click New.</span></span>
2. <span data-ttu-id="2b108-111">В поле "Шаблон рабочего времени" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2b108-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="2b108-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2b108-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2b108-113">Разверните раздел "Понедельник".</span><span class="sxs-lookup"><span data-stu-id="2b108-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="2b108-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="2b108-114">Click Add.</span></span>
6. <span data-ttu-id="2b108-115">В поле "С" введите время.</span><span class="sxs-lookup"><span data-stu-id="2b108-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="2b108-116">Укажите время, когда работа начинается утром.</span><span class="sxs-lookup"><span data-stu-id="2b108-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="2b108-117">В поле "По" введите время.</span><span class="sxs-lookup"><span data-stu-id="2b108-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="2b108-118">Укажите время, когда работники уходят на обед.</span><span class="sxs-lookup"><span data-stu-id="2b108-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="2b108-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="2b108-119">Click Add.</span></span>
9. <span data-ttu-id="2b108-120">В поле "С" введите время.</span><span class="sxs-lookup"><span data-stu-id="2b108-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="2b108-121">Укажите время, когда работа возобновляется после обеда.</span><span class="sxs-lookup"><span data-stu-id="2b108-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="2b108-122">В поле "По" введите время.</span><span class="sxs-lookup"><span data-stu-id="2b108-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="2b108-123">Укажите конец работы за день.</span><span class="sxs-lookup"><span data-stu-id="2b108-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="2b108-124">Дублирование рабочего времени на все дни недели</span><span class="sxs-lookup"><span data-stu-id="2b108-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="2b108-125">Щелкните "Копировать день".</span><span class="sxs-lookup"><span data-stu-id="2b108-125">Click Copy day.</span></span>
    * <span data-ttu-id="2b108-126">Скопируйте определения рабочего времени с понедельника по вторник.</span><span class="sxs-lookup"><span data-stu-id="2b108-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="2b108-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2b108-127">Click OK.</span></span>
3. <span data-ttu-id="2b108-128">Щелкните "Копировать день".</span><span class="sxs-lookup"><span data-stu-id="2b108-128">Click Copy day.</span></span>
    * <span data-ttu-id="2b108-129">Скопируйте определения рабочего времени с понедельника по среду.</span><span class="sxs-lookup"><span data-stu-id="2b108-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="2b108-130">В поле "В день недели" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="2b108-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="2b108-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2b108-131">Click OK.</span></span>
6. <span data-ttu-id="2b108-132">Щелкните "Копировать день".</span><span class="sxs-lookup"><span data-stu-id="2b108-132">Click Copy day.</span></span>
    * <span data-ttu-id="2b108-133">Скопируйте определения рабочего времени с понедельника по четверг.</span><span class="sxs-lookup"><span data-stu-id="2b108-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="2b108-134">В поле "В день недели" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="2b108-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="2b108-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2b108-135">Click OK.</span></span>
9. <span data-ttu-id="2b108-136">Щелкните "Копировать день".</span><span class="sxs-lookup"><span data-stu-id="2b108-136">Click Copy day.</span></span>
    * <span data-ttu-id="2b108-137">Скопируйте определения рабочего времени с понедельника по пятницу.</span><span class="sxs-lookup"><span data-stu-id="2b108-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="2b108-138">В поле "В день недели" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="2b108-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="2b108-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2b108-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="2b108-140">Определение временных интервалов для специальных операций</span><span class="sxs-lookup"><span data-stu-id="2b108-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="2b108-141">Разверните раздел "Пятница".</span><span class="sxs-lookup"><span data-stu-id="2b108-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="2b108-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2b108-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2b108-143">В поле "Свойство" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2b108-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="2b108-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2b108-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2b108-145">В поле "Свойство" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2b108-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="2b108-146">Отметка выходных дней как закрытых для отправки</span><span class="sxs-lookup"><span data-stu-id="2b108-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="2b108-147">Разверните раздел "Суббота".</span><span class="sxs-lookup"><span data-stu-id="2b108-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="2b108-148">Выберите "Да" в поле "Закрыто для отправки".</span><span class="sxs-lookup"><span data-stu-id="2b108-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="2b108-149">Разверните раздел "Воскресенье".</span><span class="sxs-lookup"><span data-stu-id="2b108-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="2b108-150">Выберите "Да" в поле "Закрыто для отправки".</span><span class="sxs-lookup"><span data-stu-id="2b108-150">Select Yes in the Closed for pickup field.</span></span>


