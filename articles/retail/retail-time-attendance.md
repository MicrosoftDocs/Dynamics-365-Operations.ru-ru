---
title: Планирование управления временем и присутствием в Retail
description: В этой теме описываются сценарии, поддерживаемые для управления временем и посещаемостью в Microsoft Dynamics 365 for Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "321279"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="92d00-103">Планирование управления временем и присутствием в Retail</span><span class="sxs-lookup"><span data-stu-id="92d00-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92d00-104">В этой теме описываются сценарии, поддерживаемые для управления временем и посещаемостью в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="92d00-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="92d00-105">Настройка и планирование управления работниками</span><span class="sxs-lookup"><span data-stu-id="92d00-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="92d00-106">Начальная конфигурация</span><span class="sxs-lookup"><span data-stu-id="92d00-106">Initial configuration</span></span>

- <span data-ttu-id="92d00-107">Запустите мастер конфигурации.</span><span class="sxs-lookup"><span data-stu-id="92d00-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="92d00-108">Зарегистрируйте работников как работников с регистрацией времени.</span><span class="sxs-lookup"><span data-stu-id="92d00-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="92d00-109">Планирование расписаний работника</span><span class="sxs-lookup"><span data-stu-id="92d00-109">Plan worker schedules</span></span>

- <span data-ttu-id="92d00-110">Примените профили, воспользовавшись планировщиком работы.</span><span class="sxs-lookup"><span data-stu-id="92d00-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="92d00-111">Дополнительные сведения см. в разделе [Применение профиля с помощью планировщика работы](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="92d00-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="92d00-112">Сведения об этапах настройки см. в разделе [Настройка времени и посещаемости](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="92d00-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="92d00-113">Конфигурация для розничной торговли</span><span class="sxs-lookup"><span data-stu-id="92d00-113">Retail-specific configuration</span></span>

- <span data-ttu-id="92d00-114">Включите профиль функциональности "Таймер" для работников, для который нужно включить регистрацию времени.</span><span class="sxs-lookup"><span data-stu-id="92d00-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="92d00-115">Щелкните **Профили функциональности POS** &gt; **Функции** &gt; **Регистрации времени POS** &gt; **Включить регистрации времени**.</span><span class="sxs-lookup"><span data-stu-id="92d00-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="92d00-116">Настройте группы разрешений POS, чтобы включить разрешение "Просмотр записей таймера".</span><span class="sxs-lookup"><span data-stu-id="92d00-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="92d00-117">Это разрешение позволяет пользователю просматривать регистрации времени других работников магазина (и из любого другого магазина, с которым связан пользователь, через адресную книгу).</span><span class="sxs-lookup"><span data-stu-id="92d00-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="92d00-118">Это разрешение имеет смысл включить для менеджера, например, но не для кассира.</span><span class="sxs-lookup"><span data-stu-id="92d00-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="92d00-119">Щелкните **Группы разрешений POS** &gt; **Просмотр записей таймера**.</span><span class="sxs-lookup"><span data-stu-id="92d00-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="92d00-120">Зарегистрировать время</span><span class="sxs-lookup"><span data-stu-id="92d00-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="92d00-121">Регистрация времени кассира и других сотрудников</span><span class="sxs-lookup"><span data-stu-id="92d00-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="92d00-122">В POS:</span><span class="sxs-lookup"><span data-stu-id="92d00-122">On POS:</span></span>

    - <span data-ttu-id="92d00-123">Операции прихода:</span><span class="sxs-lookup"><span data-stu-id="92d00-123">Clock-in operations:</span></span>

        - <span data-ttu-id="92d00-124">выполните вход с помощью операции, не связанной с денежным ящиком, или начните новую смену.</span><span class="sxs-lookup"><span data-stu-id="92d00-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="92d00-125">Выберите операцию "Таймер".</span><span class="sxs-lookup"><span data-stu-id="92d00-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="92d00-126">Выберите нужную операцию:</span><span class="sxs-lookup"><span data-stu-id="92d00-126">Select a desired operation:</span></span>

            - <span data-ttu-id="92d00-127">Время прихода</span><span class="sxs-lookup"><span data-stu-id="92d00-127">Clock-in</span></span>
            - <span data-ttu-id="92d00-128">Перерыв в работе</span><span class="sxs-lookup"><span data-stu-id="92d00-128">Break for Work</span></span>
            - <span data-ttu-id="92d00-129">Перерыв на обед</span><span class="sxs-lookup"><span data-stu-id="92d00-129">Break for Lunch</span></span>
            - <span data-ttu-id="92d00-130">Время ухода</span><span class="sxs-lookup"><span data-stu-id="92d00-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="92d00-131">Текущий статус</span><span class="sxs-lookup"><span data-stu-id="92d00-131">Current state</span></span></th>
        <th><span data-ttu-id="92d00-132">Доступные операции</span><span class="sxs-lookup"><span data-stu-id="92d00-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="92d00-133">Время прихода</span><span class="sxs-lookup"><span data-stu-id="92d00-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="92d00-134">Перерыв в работе</span><span class="sxs-lookup"><span data-stu-id="92d00-134">Break for Work</span></span></li>
        <li><span data-ttu-id="92d00-135">Перерыв на обед</span><span class="sxs-lookup"><span data-stu-id="92d00-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="92d00-136">Время ухода</span><span class="sxs-lookup"><span data-stu-id="92d00-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="92d00-137">Перерыв в работе</span><span class="sxs-lookup"><span data-stu-id="92d00-137">Break for Work</span></span></td>
        <td><span data-ttu-id="92d00-138">Время прихода</span><span class="sxs-lookup"><span data-stu-id="92d00-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="92d00-139">Перерыв на обед</span><span class="sxs-lookup"><span data-stu-id="92d00-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="92d00-140">Время прихода</span><span class="sxs-lookup"><span data-stu-id="92d00-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="92d00-141">Время ухода</span><span class="sxs-lookup"><span data-stu-id="92d00-141">Clock-out</span></span></td>
        <td><span data-ttu-id="92d00-142">Время прихода</span><span class="sxs-lookup"><span data-stu-id="92d00-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="92d00-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="92d00-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="92d00-144">Просмотрите сообщение конфигурации и убедитесь, что время текущего действия указано верно.</span><span class="sxs-lookup"><span data-stu-id="92d00-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="92d00-145">Регистрационный журнал:</span><span class="sxs-lookup"><span data-stu-id="92d00-145">Logbook:</span></span>

    - <span data-ttu-id="92d00-146">Щелкните **Регистрационный журнал**, чтобы просмотреть деятельность таймера.</span><span class="sxs-lookup"><span data-stu-id="92d00-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="92d00-147">Используйте временные фильтры, чтобы выбрать другие периоды.</span><span class="sxs-lookup"><span data-stu-id="92d00-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="92d00-148">Если вы работаете в нескольких магазинах, вы увидите свои регистрации времени изо всех магазинов, где вы фиксировали время.</span><span class="sxs-lookup"><span data-stu-id="92d00-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="92d00-149">Можно использовать фильтр магазина для просмотра регистраций времени в выбранном магазине.</span><span class="sxs-lookup"><span data-stu-id="92d00-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="92d00-150">Другие часовые пояса:</span><span class="sxs-lookup"><span data-stu-id="92d00-150">Different time zones:</span></span>

    - <span data-ttu-id="92d00-151">если вы просматриваете время из другого расположения (для регистрационного журнала кассира или с помощью команды **Просмотр записей таймера** в случае менеджера) и это расположение находится в другом часовом поясе, отображаемые записи времени переводятся в ваш локальный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="92d00-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="92d00-152">Например, вы менеджер в двух магазинах: один — в Аризоне, а другой — в Неваде.</span><span class="sxs-lookup"><span data-stu-id="92d00-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="92d00-153">Кассир регистрирует приход в 09:00</span><span class="sxs-lookup"><span data-stu-id="92d00-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="92d00-154">в Аризоне.</span><span class="sxs-lookup"><span data-stu-id="92d00-154">in Arizona.</span></span> <span data-ttu-id="92d00-155">В Неваде в это время 08:00.</span><span class="sxs-lookup"><span data-stu-id="92d00-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="92d00-156">Поэтому если вы в магазине в Неваде смотрите записи регистрации времени, время регистрации отмечено как 08:00.</span><span class="sxs-lookup"><span data-stu-id="92d00-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="92d00-157">Просмотр регистраций времени работников</span><span class="sxs-lookup"><span data-stu-id="92d00-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="92d00-158">Просмотрите регистрации времени работников и отфильтруйте их по магазину или типу деятельности</span><span class="sxs-lookup"><span data-stu-id="92d00-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="92d00-159">В POS:</span><span class="sxs-lookup"><span data-stu-id="92d00-159">On POS:</span></span>

- <span data-ttu-id="92d00-160">Выберите **Просмотр записей таймера**.</span><span class="sxs-lookup"><span data-stu-id="92d00-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="92d00-161">Вы увидите действия по регистрации таймера для всех работников, назначенных тем же магазинам, что и вы.</span><span class="sxs-lookup"><span data-stu-id="92d00-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="92d00-162">Можно использовать фильтры по типу деятельности и магазину, чтобы отфильтровать регистрации времени.</span><span class="sxs-lookup"><span data-stu-id="92d00-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="92d00-163">Обработка регистраций времени и управление ими</span><span class="sxs-lookup"><span data-stu-id="92d00-163">Process and manage time registrations</span></span>

<span data-ttu-id="92d00-164">Пользователь Dynamics 365 for Retail выполняет workflow-процесс, чтобы вычислить, утвердить и перенеси регистрации времени в зарплату.</span><span class="sxs-lookup"><span data-stu-id="92d00-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="92d00-165">Основные операции</span><span class="sxs-lookup"><span data-stu-id="92d00-165">Primary operations</span></span>

- <span data-ttu-id="92d00-166">Рассчитать</span><span class="sxs-lookup"><span data-stu-id="92d00-166">Calculate</span></span>
- <span data-ttu-id="92d00-167">Утвердить</span><span class="sxs-lookup"><span data-stu-id="92d00-167">Approve</span></span>
- <span data-ttu-id="92d00-168">Отправить на зарплату</span><span class="sxs-lookup"><span data-stu-id="92d00-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="92d00-169">Прочие распространенные операции</span><span class="sxs-lookup"><span data-stu-id="92d00-169">Other common operations</span></span>

- <span data-ttu-id="92d00-170">Массовый уход</span><span class="sxs-lookup"><span data-stu-id="92d00-170">Bulk Clock-out</span></span>
- <span data-ttu-id="92d00-171">Регистрация отсутствия</span><span class="sxs-lookup"><span data-stu-id="92d00-171">Register Absence</span></span>

<span data-ttu-id="92d00-172">Дополнительные сведения о том, как обрабатывать регистрацию времени и посещаемости, см. в разделе [Обработка регистраций времени и посещаемости](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="92d00-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
