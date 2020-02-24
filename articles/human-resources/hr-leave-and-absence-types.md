---
title: Настройка типов отпусков и отсутствий
description: Настройка типов отпусков, которые могут взять сотрудники в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010374"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="39933-103">Настройка типов отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="39933-103">Configure leave and absence types</span></span>

<span data-ttu-id="39933-104">Типы отпусков в Dynamics 365 Human Resources определяют типы отсутствий, о которых могут сообщать сотрудники.</span><span class="sxs-lookup"><span data-stu-id="39933-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="39933-105">Типы отпусков можно настроить в соответствии с потребностями организации.</span><span class="sxs-lookup"><span data-stu-id="39933-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="39933-106">Примеры типов отпуска:</span><span class="sxs-lookup"><span data-stu-id="39933-106">Examples of leave types include:</span></span>

- <span data-ttu-id="39933-107">Оплачиваемое отсутствие (PTO)</span><span class="sxs-lookup"><span data-stu-id="39933-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="39933-108">Неоплачиваемый отпуск</span><span class="sxs-lookup"><span data-stu-id="39933-108">Unpaid leave</span></span>
- <span data-ttu-id="39933-109">Оплачиваемый отпуск</span><span class="sxs-lookup"><span data-stu-id="39933-109">Paid vacation</span></span>
- <span data-ttu-id="39933-110">Больничный</span><span class="sxs-lookup"><span data-stu-id="39933-110">Sick leave</span></span>
- <span data-ttu-id="39933-111">Отпуск по медицинским причинам</span><span class="sxs-lookup"><span data-stu-id="39933-111">Medical leave</span></span>
- <span data-ttu-id="39933-112">Отпуск по семейным обстоятельствам</span><span class="sxs-lookup"><span data-stu-id="39933-112">Family leave</span></span>
- <span data-ttu-id="39933-113">Кратковременная нетрудоспособность</span><span class="sxs-lookup"><span data-stu-id="39933-113">Short-term disability</span></span>
- <span data-ttu-id="39933-114">Отпуск в связи со смертью</span><span class="sxs-lookup"><span data-stu-id="39933-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="39933-115">Добавление типа отпуска</span><span class="sxs-lookup"><span data-stu-id="39933-115">Add a leave type</span></span>

1. <span data-ttu-id="39933-116">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="39933-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="39933-117">В **Настройка** выберите **Типы отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="39933-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="39933-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="39933-118">Select **New**.</span></span>

4. <span data-ttu-id="39933-119">Введите имя для типа отпуска в **Тип**, выберите workflow-процесс в **Код workflow-процесса** и введите описание в **Описание**.</span><span class="sxs-lookup"><span data-stu-id="39933-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="39933-120">В **Общее** выберите **Нет**, **Запланировано** или **Незапланированно** в раскрывающемся списке **Категория**.</span><span class="sxs-lookup"><span data-stu-id="39933-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="39933-121">Выбор кода дохода из раскрывающегося списка **Код дохода**.</span><span class="sxs-lookup"><span data-stu-id="39933-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="39933-122">В **Требуется код основания** необходимо указать, нужно ли требовать код причины.</span><span class="sxs-lookup"><span data-stu-id="39933-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="39933-123">Если требуется указать коды причины, возможно, потребуется их добавить.</span><span class="sxs-lookup"><span data-stu-id="39933-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="39933-124">В **Коды причин** выберите **Добавить**, выберите код причины, а затем установите флажок **Включено** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="39933-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="39933-125">В **Ограничить доступ выбранными ролями** выберите, следует ли ограничить доступ.</span><span class="sxs-lookup"><span data-stu-id="39933-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="39933-126">Затем выберите роли безопасности в **Роли безопасности для данного типа отпуска**.</span><span class="sxs-lookup"><span data-stu-id="39933-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="39933-127">Роли безопасности определяются в workflow-процессе, выбранном в **Код workflow-процесса** ранее в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="39933-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="39933-128">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="39933-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="39933-129">Настройка предварительных функций</span><span class="sxs-lookup"><span data-stu-id="39933-129">Configure preview features</span></span>

<span data-ttu-id="39933-130">Если включены функции предварительного просмотра для отпусков и отсутствия, необходимо также настроить для них параметры.</span><span class="sxs-lookup"><span data-stu-id="39933-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="39933-131">Настройка параметров округления для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="39933-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="39933-132">Возможны следующие варианты: **Нет**, **Вверх**, **Вниз** и **Ближайшее**.</span><span class="sxs-lookup"><span data-stu-id="39933-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="39933-133">Можно также задать точность округления для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="39933-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="39933-134">Настройте **Корректировка праздников** для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="39933-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="39933-135">При выборе этого параметра Human Resources использует число праздников, которые выпадают на рабочий день, чтобы определить, как начислять время отсутствия для типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="39933-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="39933-136">Например, если Рождество приходится на понедельник, при обработке начислений модуль Human Resources вычтет один день из типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="39933-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="39933-137">Можно установить праздники в календаре рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="39933-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="39933-138">Дополнительные сведения см. в [Создание календаря рабочего времени](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="39933-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="39933-139">См. также</span><span class="sxs-lookup"><span data-stu-id="39933-139">See also</span></span>

- [<span data-ttu-id="39933-140">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="39933-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="39933-141">Создание плана отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="39933-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="39933-142">Создание календаря рабочего времени</span><span class="sxs-lookup"><span data-stu-id="39933-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)