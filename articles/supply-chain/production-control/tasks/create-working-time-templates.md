---
title: Создание шаблонов рабочего времени
description: Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920937"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="d8ef8-103">Создание шаблонов рабочего времени</span><span class="sxs-lookup"><span data-stu-id="d8ef8-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8ef8-104">Шаблоны рабочего времени определяют рабочие часы в течение недели и используются для создания рабочего времени для периода времени.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="d8ef8-105">Эта процедура описывает определение шаблона рабочего времени с помощью свойств планирования рабочего времени для классификации интервалов рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="d8ef8-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d8ef8-107">Перейдите в раздел **Рабочие области > Управление жизненным циклом ресурса**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="d8ef8-108">Выберите **Шаблоны рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="d8ef8-109">Создание шаблона рабочего времени</span><span class="sxs-lookup"><span data-stu-id="d8ef8-109">Create working time template</span></span>

1. <span data-ttu-id="d8ef8-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-110">Select **New**.</span></span>
1. <span data-ttu-id="d8ef8-111">В поле **Шаблон рабочего времени** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="d8ef8-112">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="d8ef8-113">Разверните раздел **Понедельник**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="d8ef8-114">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-114">Select **Add**.</span></span>
1. <span data-ttu-id="d8ef8-115">В поле **С** введите время.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="d8ef8-116">Укажите время, когда работа начинается утром.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="d8ef8-117">В поле **По** введите время.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="d8ef8-118">Укажите время, когда работники уходят на обед.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="d8ef8-119">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-119">Select **Add**.</span></span>
1. <span data-ttu-id="d8ef8-120">В поле **С** введите время.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="d8ef8-121">Укажите время, когда работа возобновляется после обеда.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="d8ef8-122">В поле **По** введите время.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="d8ef8-123">Укажите конец работы за день.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="d8ef8-124">Дублирование рабочего времени на все дни недели</span><span class="sxs-lookup"><span data-stu-id="d8ef8-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="d8ef8-125">Выберите **Копировать день**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="d8ef8-126">Скопируйте определения рабочего времени с понедельника по вторник.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="d8ef8-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-127">Select **OK**.</span></span>
1. <span data-ttu-id="d8ef8-128">Выберите **Копировать день**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="d8ef8-129">Скопируйте определения рабочего времени с понедельника по среду.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="d8ef8-130">В поле **В день недели** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="d8ef8-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-131">Select **OK**.</span></span>
1. <span data-ttu-id="d8ef8-132">Выберите **Копировать день**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="d8ef8-133">Скопируйте определения рабочего времени с понедельника по четверг.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="d8ef8-134">В поле **В день недели** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="d8ef8-135">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-135">Select **OK**.</span></span>
1. <span data-ttu-id="d8ef8-136">Выберите **Копировать день**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="d8ef8-137">Скопируйте определения рабочего времени с понедельника по пятницу.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="d8ef8-138">В поле **В день недели** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="d8ef8-139">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="d8ef8-140">Определение временных интервалов для специальных операций</span><span class="sxs-lookup"><span data-stu-id="d8ef8-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="d8ef8-141">Разверните раздел **Пятница**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="d8ef8-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d8ef8-143">В поле **Свойство** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="d8ef8-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d8ef8-145">В поле **Свойство** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="d8ef8-146">Отметка выходных дней как закрытых для отправки</span><span class="sxs-lookup"><span data-stu-id="d8ef8-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="d8ef8-147">Разверните раздел **Суббота**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="d8ef8-148">Выберите *Да* в поле **Закрыто для отправки**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="d8ef8-149">Разверните раздел **Воскресенье**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="d8ef8-150">Выберите *Да* в поле **Закрыто для отправки**.</span><span class="sxs-lookup"><span data-stu-id="d8ef8-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]