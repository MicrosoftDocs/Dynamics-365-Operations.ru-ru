---
title: Настройка типов отпусков и отсутствий
description: Настройка типов отпусков, которые могут взять сотрудники в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420215"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="30b56-103">Настройка типов отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="30b56-103">Configure leave and absence types</span></span>

<span data-ttu-id="30b56-104">Типы отпусков в Dynamics 365 Human Resources определяют типы отсутствий, о которых могут сообщать сотрудники.</span><span class="sxs-lookup"><span data-stu-id="30b56-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="30b56-105">Типы отпусков можно настроить в соответствии с потребностями организации.</span><span class="sxs-lookup"><span data-stu-id="30b56-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="30b56-106">Примеры типов отпуска:</span><span class="sxs-lookup"><span data-stu-id="30b56-106">Examples of leave types include:</span></span>

- <span data-ttu-id="30b56-107">Оплачиваемое отсутствие (PTO)</span><span class="sxs-lookup"><span data-stu-id="30b56-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="30b56-108">Неоплачиваемый отпуск</span><span class="sxs-lookup"><span data-stu-id="30b56-108">Unpaid leave</span></span>
- <span data-ttu-id="30b56-109">Оплачиваемый отпуск</span><span class="sxs-lookup"><span data-stu-id="30b56-109">Paid vacation</span></span>
- <span data-ttu-id="30b56-110">Больничный</span><span class="sxs-lookup"><span data-stu-id="30b56-110">Sick leave</span></span>
- <span data-ttu-id="30b56-111">Отпуск по медицинским причинам</span><span class="sxs-lookup"><span data-stu-id="30b56-111">Medical leave</span></span>
- <span data-ttu-id="30b56-112">Отпуск по семейным обстоятельствам</span><span class="sxs-lookup"><span data-stu-id="30b56-112">Family leave</span></span>
- <span data-ttu-id="30b56-113">Кратковременная нетрудоспособность</span><span class="sxs-lookup"><span data-stu-id="30b56-113">Short-term disability</span></span>
- <span data-ttu-id="30b56-114">Отпуск в связи со смертью</span><span class="sxs-lookup"><span data-stu-id="30b56-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="30b56-115">Добавление типа отпуска</span><span class="sxs-lookup"><span data-stu-id="30b56-115">Add a leave type</span></span>

1. <span data-ttu-id="30b56-116">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="30b56-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="30b56-117">В **Настройка** выберите **Типы отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="30b56-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="30b56-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="30b56-118">Select **New**.</span></span>

4. <span data-ttu-id="30b56-119">Введите имя для типа отпуска в **Тип**, выберите workflow-процесс в **Код workflow-процесса** и введите описание в **Описание**.</span><span class="sxs-lookup"><span data-stu-id="30b56-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="30b56-120">В **Общее** выберите **Нет**, **Запланировано** или **Незапланированно** в раскрывающемся списке **Категория**.</span><span class="sxs-lookup"><span data-stu-id="30b56-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="30b56-121">Выбор кода дохода из раскрывающегося списка **Код дохода**.</span><span class="sxs-lookup"><span data-stu-id="30b56-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="30b56-122">В **Требуется код основания** необходимо указать, нужно ли требовать код причины.</span><span class="sxs-lookup"><span data-stu-id="30b56-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="30b56-123">Если требуется указать коды причины, возможно, потребуется их добавить.</span><span class="sxs-lookup"><span data-stu-id="30b56-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="30b56-124">В **Коды причин** выберите **Добавить**, выберите код причины, а затем установите флажок **Включено** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="30b56-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="30b56-125">В **Ограничить доступ выбранными ролями** выберите, следует ли ограничить доступ.</span><span class="sxs-lookup"><span data-stu-id="30b56-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="30b56-126">Затем выберите роли безопасности в **Роли безопасности для данного типа отпуска**.</span><span class="sxs-lookup"><span data-stu-id="30b56-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="30b56-127">Роли безопасности определяются в workflow-процессе, выбранном в **Код workflow-процесса** ранее в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="30b56-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="30b56-128">В разделе **Цвет календаря** выберите цвет для показа в календарях отпусков и отсутствия для данного типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="30b56-129">В области **Отношения приостановки** выберите, если хотите, чтобы этот тип отпуска был приостановлен, либо приостановлен другим типом отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="30b56-130">При отправке запроса об отсутствии для приостанавливаемого типа отпуска, приостановка отпуска будет автоматически создана для типа приостановленного отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="30b56-131">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="30b56-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="30b56-132">Настройка правил типов отпусков</span><span class="sxs-lookup"><span data-stu-id="30b56-132">Configure leave type rules</span></span>

1. <span data-ttu-id="30b56-133">Настройка параметров округления для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="30b56-134">Возможны следующие варианты: **Нет**, **Вверх**, **Вниз** и **Ближайшее**.</span><span class="sxs-lookup"><span data-stu-id="30b56-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="30b56-135">Можно также задать точность округления для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="30b56-136">Настройте **Корректировка праздников** для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="30b56-137">При выборе этого параметра Human Resources использует число праздников, которые выпадают на рабочий день, чтобы определить, как начислять время отсутствия для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="30b56-138">Например, если Рождество приходится на понедельник, при обработке начислений модуль Human Resources вычтет один день из типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="30b56-139">Можно установить праздники в календаре рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="30b56-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="30b56-140">Дополнительные сведения см. в [Создание календаря рабочего времени](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="30b56-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="30b56-141">Задайте **Перенести тип отпуска** для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="30b56-142">При выборе этого параметра все перенесенные балансы будут перенесены в указанный тип отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="30b56-143">Тип переноса также должен быть включен в план отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="30b56-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="30b56-144">Задайте **Правила истечения срока действия** для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="30b56-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="30b56-145">При настройке этого параметра можно выбрать единицу измерения дней или месяцев и установить срок действия.</span><span class="sxs-lookup"><span data-stu-id="30b56-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="30b56-146">Можно также задать дату окончания срока действия правила истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="30b56-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="30b56-147">Любые балансы отпусков, существующие на момент окончания срока, будут вычитаться из типа отпуска и будут отражены в балансе отпусков.</span><span class="sxs-lookup"><span data-stu-id="30b56-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="30b56-148">См. также</span><span class="sxs-lookup"><span data-stu-id="30b56-148">See also</span></span>

- [<span data-ttu-id="30b56-149">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="30b56-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="30b56-150">Создание плана отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="30b56-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="30b56-151">Создание календаря рабочего времени</span><span class="sxs-lookup"><span data-stu-id="30b56-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="30b56-152">Приостановка отпуска</span><span class="sxs-lookup"><span data-stu-id="30b56-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

