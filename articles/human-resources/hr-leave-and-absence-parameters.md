---
title: Настройка параметров отпусков и отсутствий
description: Определение параметров управления персоналом для отпусков и отсутствия в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 45f5ebfe7bd11a529e871f5fd3244577954534f5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794645"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="33363-103">Настройка параметров отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="33363-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="33363-104">Прежде чем настраивать планы отпусков и отсутствия в Dynamics 365 Human Resources, рекомендуется проверить настройки для всех соответствующих параметров модуля управления персоналом, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="33363-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="33363-105">Номерная серия для запросов отпусков</span><span class="sxs-lookup"><span data-stu-id="33363-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="33363-106">Параметры Family Medical and Leave Act (FMLA)</span><span class="sxs-lookup"><span data-stu-id="33363-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="33363-107">Настройки самообслуживания сотрудников для запросов отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="33363-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="33363-108">Параметры отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="33363-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="33363-109">Просмотр и изменение параметров управления персоналом</span><span class="sxs-lookup"><span data-stu-id="33363-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="33363-110">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="33363-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="33363-111">В **Настройка** выберите **Параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="33363-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="33363-112">На вкладке **Номерные серии** проверьте **Код номерной серии** для **Код запроса отпуска** и измените его, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="33363-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="33363-113">Этот параметр определяет последовательность, используемую для автоматического назначения кодов для запросов отпуска.</span><span class="sxs-lookup"><span data-stu-id="33363-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="33363-114">На вкладке **FMLA** проверьте настройки FMLA и, если необходимо, измените их.</span><span class="sxs-lookup"><span data-stu-id="33363-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="33363-115">На вкладке **Самообслуживание сотрудников** укажите, могут ли менеджеры вводить запросы на отпуск и отсутствие от имени своих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="33363-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="33363-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="33363-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="33363-117">Просмотр отпусков и отсутствия в нескольких компаниях в настоящее время является предварительной версией.</span><span class="sxs-lookup"><span data-stu-id="33363-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="33363-118">Необходимо включить ее в среде **Песочница**, чтобы отображался параметр для отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="33363-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="33363-119">Дополнительные сведения о включении функций предварительной версии см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="33363-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="33363-120">Просмотр и изменение общих параметров управления персоналом</span><span class="sxs-lookup"><span data-stu-id="33363-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="33363-121">На странице **Управление персоналом** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="33363-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="33363-122">В разделе **Настройка** выберите **Совместно используемые параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="33363-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="33363-123">На вкладке **Расширенный доступ** выберите **Да** для параметра **Включить просмотр отпусков в разных компаниях**, чтобы разрешить просмотр отпусков в нескольких компаниях.</span><span class="sxs-lookup"><span data-stu-id="33363-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="33363-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="33363-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="33363-125">Просмотр и изменение параметров отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="33363-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="33363-126">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="33363-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="33363-127">В **Настройка** выберите **Параметры отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="33363-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="33363-128">На вкладке **Общие** установите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="33363-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="33363-129">Задайте для параметра **Единица измерения отпусков и отсутствия** часы или дни.</span><span class="sxs-lookup"><span data-stu-id="33363-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="33363-130">Если заданы дни, можно выбрать **Включить определение половины дня**, чтобы сотрудники могли выбирать в своих запросах отгулов первую или вторую половину дня.</span><span class="sxs-lookup"><span data-stu-id="33363-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="33363-131">Выберите **Дата начала учета месяцев службы**, чтобы задать, когда вступят в силу коэффициенты начисления для планов отпусков с использованием месяцев службы.</span><span class="sxs-lookup"><span data-stu-id="33363-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="33363-132">Выберите **Расчет сальдо** для отображения сальдо по состоянию на сегодня или по состоянию на период начисления.</span><span class="sxs-lookup"><span data-stu-id="33363-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="33363-133">Если выбрано значение **Сальдо на текущий день**, сальдо отображает общую сумму всех начислений, корректировок и запросов по состоянию на сегодня.</span><span class="sxs-lookup"><span data-stu-id="33363-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="33363-134">Если выбрано значение **Сальдо на период начисления**, сальдо отображает общую сумму всех начислений, корректировок и запросов за период начисления, определенный частотой в плане отпусков.</span><span class="sxs-lookup"><span data-stu-id="33363-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="33363-135">Задайте время начала для пакетного задания переноса истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="33363-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="33363-136">Выберите **Да** для параметров **Разрешить сотрудникам покупать отпуск** и **Разрешить сотрудникам продавать отпуск**.</span><span class="sxs-lookup"><span data-stu-id="33363-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="33363-137">Если для этих параметров выбрано значение **Да**, можно создать политики покупки и продажи, позволяющие сотрудникам отправлять запросы на покупку и продажу отпуска.</span><span class="sxs-lookup"><span data-stu-id="33363-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="33363-138">Настройка параметров календаря</span><span class="sxs-lookup"><span data-stu-id="33363-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="33363-139">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="33363-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="33363-140">В **Настройка** выберите **Параметры отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="33363-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="33363-141">На вкладке **Календарь** измените настройки, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="33363-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="33363-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="33363-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="33363-143">См. также</span><span class="sxs-lookup"><span data-stu-id="33363-143">See also</span></span>

- [<span data-ttu-id="33363-144">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="33363-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]