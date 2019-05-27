---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (11 января 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518902"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="4e447-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (11 января 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="4e447-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e447-104">**Сборка 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="4e447-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="4e447-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="4e447-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="4e447-106">Изменения</span><span class="sxs-lookup"><span data-stu-id="4e447-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="4e447-107">Проверка запросов на отпуск путем прогнозирования доступного сальдо</span><span class="sxs-lookup"><span data-stu-id="4e447-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="4e447-108">Изменения, внесенные в данном выпуске, позволяют сотрудникам запрашивать отпуск в будущем времени без вычитания из их текущего сальдо.</span><span class="sxs-lookup"><span data-stu-id="4e447-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="4e447-109">Стандартные workflow-процессы будут использоваться для любых будущих запросов.</span><span class="sxs-lookup"><span data-stu-id="4e447-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="4e447-110">Дополнительные сведения см. в разделе [Начисление времени отпуска на основе отработанных часов](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="4e447-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="4e447-111">Просмотр прогнозируемого сальдо отпуска в системе дистанционной регистрации рабочего времени и области "Люди"</span><span class="sxs-lookup"><span data-stu-id="4e447-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="4e447-112">Эта функция позволяет просматривать сальдо для отпуска будущих периодов сотрудниками отдела кадров, руководителями и сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="4e447-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="4e447-113">Сотрудники могли посмотреть будущие сальдо в рабочей области **Дистанционная регистрация рабочего времени**, а отделу кадров эта же информация доступна в рабочей области **Люди**.</span><span class="sxs-lookup"><span data-stu-id="4e447-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="4e447-114">Уведомления об изменении сальдо отпуска</span><span class="sxs-lookup"><span data-stu-id="4e447-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="4e447-115">Сальдо отпуска будут отображать текущее сальдо сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4e447-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="4e447-116">Будущие сальдо можно найти в рабочих областях **Дистанционная регистрация рабочего времени** и **Люди**, введя "на дату" для расчета прогнозируемого сальдо.</span><span class="sxs-lookup"><span data-stu-id="4e447-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="4e447-117">Навигация была добавлена для просмотра прогнозируемых сальдо в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="4e447-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="4e447-118">Карточка **Отгул** в рабочей области **Дистанционная регистрация рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="4e447-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="4e447-119">Карточка **Отпуск и отсутствие** в рабочей области **Портал самообслуживания менеджеров**.</span><span class="sxs-lookup"><span data-stu-id="4e447-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="4e447-120">Страница **Отпуск и отсутствие** в рабочей области **Люди**.</span><span class="sxs-lookup"><span data-stu-id="4e447-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="4e447-121">Разрешить десятичные знаки для планов переменной компенсации (планы денежных средств)</span><span class="sxs-lookup"><span data-stu-id="4e447-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="4e447-122">Переменное денежное вознаграждение и планы теперь содержат дополнительную гибкость для сумм и переопределения значений с десятичными суммами.</span><span class="sxs-lookup"><span data-stu-id="4e447-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="4e447-123">Не удается изменить даты регистраций переменной компенсации после сохранения плана</span><span class="sxs-lookup"><span data-stu-id="4e447-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="4e447-124">Это изменение позволяет обновить дату окончания плана (продленный или с истекшим сроком действия) после сохранения плана.</span><span class="sxs-lookup"><span data-stu-id="4e447-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="4e447-125">Вы может по-прежнему активировать или отключить планы независимо от даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="4e447-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="4e447-126">Информации о заработной плате доступна при назначении роли безопасности администратора заработной платы</span><span class="sxs-lookup"><span data-stu-id="4e447-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="4e447-127">Роль администратора заработной платы была обновлена для доступа к информации о заработной плате во время процесса запроса.</span><span class="sxs-lookup"><span data-stu-id="4e447-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="4e447-128">Детализация иерархии портала самообслуживания сотрудников | штатных единиц из плитки не получает родительский узел</span><span class="sxs-lookup"><span data-stu-id="4e447-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="4e447-129">Чтобы устранить ошибки, возникшие при добавлении иерархии должностей в новые рабочие области и навигации в организационной структуре организации, были внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="4e447-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="4e447-130">Новое сообщение проверки, когда номерная серия персонала уже используется</span><span class="sxs-lookup"><span data-stu-id="4e447-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="4e447-131">Изменение было сделано для уточнения того, что проблема возникает, когда при приеме сотрудника на работу и следующий номер персонала используется.</span><span class="sxs-lookup"><span data-stu-id="4e447-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="4e447-132">Рабочая область дистанционного обслуживания сотрудников выбрана в качестве исходной начальной страницы</span><span class="sxs-lookup"><span data-stu-id="4e447-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="4e447-133">Когда рабочая область **Самообслуживание сотрудников** выбрана как страница начальной загрузки для пользователя, и пользователю не назначена роль сотрудника, система будет перенаправлять на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e447-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="4e447-134">Код причины увольнения обновляет запись назначения для должность</span><span class="sxs-lookup"><span data-stu-id="4e447-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="4e447-135">Код причины увольнения теперь обновляет назначение на должность при увольнении сотрудника и прекращении должности.</span><span class="sxs-lookup"><span data-stu-id="4e447-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
