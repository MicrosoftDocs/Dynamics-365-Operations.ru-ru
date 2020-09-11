---
title: Настройка параметров отпусков и отсутствий
description: Определение параметров управления персоналом для отпусков и отсутствия в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712384"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="2f811-103">Настройка параметров отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="2f811-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="2f811-104">Прежде чем настраивать планы отпусков и отсутствия в Dynamics 365 Human Resources, рекомендуется проверить настройки для всех соответствующих параметров модуля управления персоналом, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="2f811-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="2f811-105">Номерная серия для запросов отпусков</span><span class="sxs-lookup"><span data-stu-id="2f811-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="2f811-106">Параметры Family Medical and Leave Act (FMLA)</span><span class="sxs-lookup"><span data-stu-id="2f811-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="2f811-107">Настройки самообслуживания сотрудников для запросов отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="2f811-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="2f811-108">Параметры отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="2f811-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="2f811-109">Просмотр и изменение параметров управления персоналом</span><span class="sxs-lookup"><span data-stu-id="2f811-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="2f811-110">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2f811-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2f811-111">В **Настройка** выберите **Параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="2f811-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="2f811-112">На вкладке **Номерные серии** проверьте **Код номерной серии** для **Код запроса отпуска** и измените его, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="2f811-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="2f811-113">Этот параметр определяет последовательность, используемую для автоматического назначения кодов для запросов отпуска.</span><span class="sxs-lookup"><span data-stu-id="2f811-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="2f811-114">На вкладке **FMLA** проверьте настройки FMLA и, если необходимо, измените их.</span><span class="sxs-lookup"><span data-stu-id="2f811-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="2f811-115">На вкладке **Самообслуживание сотрудников** укажите, могут ли менеджеры вводить запросы на отпуск и отсутствие от имени своих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="2f811-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="2f811-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2f811-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="2f811-117">Просмотр и изменение параметров отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="2f811-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="2f811-118">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2f811-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2f811-119">В **Настройка** выберите **Параметры отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="2f811-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="2f811-120">На вкладке **Общие** установите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="2f811-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="2f811-121">Задайте для параметра **Единица измерения отпусков и отсутствия** часы или дни.</span><span class="sxs-lookup"><span data-stu-id="2f811-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="2f811-122">Если заданы дни, можно выбрать **Включить определение половины дня**, чтобы сотрудники могли выбирать в своих запросах отгулов первую или вторую половину дня.</span><span class="sxs-lookup"><span data-stu-id="2f811-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="2f811-123">Выберите **Дата начала учета месяцев службы**, чтобы задать, когда вступят в силу коэффициенты начисления для планов отпусков с использованием месяцев службы.</span><span class="sxs-lookup"><span data-stu-id="2f811-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="2f811-124">Выберите **Расчет сальдо** для отображения сальдо по состоянию на сегодня или по состоянию на период начисления.</span><span class="sxs-lookup"><span data-stu-id="2f811-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="2f811-125">Если выбрано значение **Сальдо на текущий день**, сальдо отображает общую сумму всех начислений, корректировок и запросов по состоянию на сегодня.</span><span class="sxs-lookup"><span data-stu-id="2f811-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="2f811-126">Если выбрано значение **Сальдо на период начисления**, сальдо отображает общую сумму всех начислений, корректировок и запросов за период начисления, определенный частотой в плане отпусков.</span><span class="sxs-lookup"><span data-stu-id="2f811-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="2f811-127">Задайте время начала для пакетного задания переноса истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="2f811-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="2f811-128">Выберите **Да** для параметров **Разрешить сотрудникам покупать отпуск** и **Разрешить сотрудникам продавать отпуск**.</span><span class="sxs-lookup"><span data-stu-id="2f811-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="2f811-129">Если для этих параметров выбрано значение **Да**, можно создать политики покупки и продажи, позволяющие сотрудникам отправлять запросы на покупку и продажу отпуска.</span><span class="sxs-lookup"><span data-stu-id="2f811-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="2f811-130">Настройка параметров календаря</span><span class="sxs-lookup"><span data-stu-id="2f811-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="2f811-131">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2f811-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2f811-132">В **Настройка** выберите **Параметры отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="2f811-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="2f811-133">На вкладке **Календарь** измените настройки, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="2f811-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="2f811-134">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2f811-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f811-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2f811-135">See also</span></span>

- [<span data-ttu-id="2f811-136">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="2f811-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
