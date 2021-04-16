---
title: Создание заказов на работу
description: В этом разделе описывается, как создавать заказы на работу в модуле "Управление активами".
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836742"
---
# <a name="creating-work-orders"></a><span data-ttu-id="35aa0-103">Создание заказов на работу</span><span class="sxs-lookup"><span data-stu-id="35aa0-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35aa0-104">После планирования заданий профилактического обслуживания следующим шагом будет создание заказов на работу для них.</span><span class="sxs-lookup"><span data-stu-id="35aa0-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="35aa0-105">Можно выполнить этот шаг, используя одно из графиков обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35aa0-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="35aa0-106">Запланированные задания в графике обслуживания могут иметь различные типы ссылок, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="35aa0-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="35aa0-107">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="35aa0-107">Reference type</span></span> | <span data-ttu-id="35aa0-108">описание</span><span class="sxs-lookup"><span data-stu-id="35aa0-108">Description</span></span> |
|---|---|
| <span data-ttu-id="35aa0-109">Планы обслуживания</span><span class="sxs-lookup"><span data-stu-id="35aa0-109">Maintenance plans</span></span> | <span data-ttu-id="35aa0-110">Задания профилактического обслуживания, основанные на типах планов обслуживания *Время* или *Счетчик*.</span><span class="sxs-lookup"><span data-stu-id="35aa0-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="35aa0-111">Циклы обслуживания</span><span class="sxs-lookup"><span data-stu-id="35aa0-111">Maintenance rounds</span></span> | <span data-ttu-id="35aa0-112">Задания профилактического обслуживания, содержащие несколько активов, требующих подобного типа обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35aa0-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="35aa0-113">Запрос на обслуживание</span><span class="sxs-lookup"><span data-stu-id="35aa0-113">Maintenance request</span></span> | <span data-ttu-id="35aa0-114">Запрос, созданный вручную для обслуживания или ремонта актива.</span><span class="sxs-lookup"><span data-stu-id="35aa0-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="35aa0-115">Этот запрос может быть преобразован в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="35aa0-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="35aa0-116">Создание заказов на работу на основе графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="35aa0-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="35aa0-117">Для создания заказов на работу, которые основаны на расписании обслуживания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="35aa0-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="35aa0-118">Откройте одну из следующих страниц, в зависимости от того, как вы хотите выбирать элементы планирования для заказов на работу:</span><span class="sxs-lookup"><span data-stu-id="35aa0-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="35aa0-119">Все расписание обслуживания ( **Управление активами \> Расписание обслуживания \> Все расписание обслуживания**)</span><span class="sxs-lookup"><span data-stu-id="35aa0-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="35aa0-120">Откройте строки расписания обслуживания (**Управление активами \> Расписание обслуживания \> Открыть строки расписания обслуживания**)</span><span class="sxs-lookup"><span data-stu-id="35aa0-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="35aa0-121">Откройте пулы расписаний обслуживания (**Управление активами \> Расписание обслуживания \> Открыть пулы расписаний обслуживания**)</span><span class="sxs-lookup"><span data-stu-id="35aa0-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="35aa0-122">В сетке установите флажок для каждого задания планового обслуживания, для которого необходимо создать заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="35aa0-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="35aa0-123">Затем на панели операций выберите **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="35aa0-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="35aa0-124">Откроется диалоговое окно **Создание заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="35aa0-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="35aa0-125">В поле **Прогноз часов обслуживания** отображается общее количество часов прогноза для выбранных строк.</span><span class="sxs-lookup"><span data-stu-id="35aa0-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Диалоговое окно создания заказов на работу](media/18-preventive-maintenance.png)

1. <span data-ttu-id="35aa0-127">В разделе **Параметры** укажите количество заказов на работу, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="35aa0-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="35aa0-128">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="35aa0-128">Select one of the following options:</span></span>

    - <span data-ttu-id="35aa0-129">**Один заказ на работу на строку** — создание одного заказа на работу на каждую строку графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35aa0-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="35aa0-130">**Один заказ на работу на** — создание заказов на работу, сгруппированных в соответствии с настройками других параметров, которые становятся доступными при выборе данного параметра.</span><span class="sxs-lookup"><span data-stu-id="35aa0-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="35aa0-131">В поле **Тип заказа на работу** выберите тип заказа на работу, который будет использоваться для всех создаваемых заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="35aa0-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="35aa0-132">Выберите **ОК**, чтобы создать заказы на работу в соответствии с вашими настройками.</span><span class="sxs-lookup"><span data-stu-id="35aa0-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="35aa0-133">Группировка строк заказов на работу, которые создаются автоматически при выполнении плана обслуживания</span><span class="sxs-lookup"><span data-stu-id="35aa0-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

<span data-ttu-id="35aa0-134">Эта функция позволяет определить правила для группировки строк заказа на работу в одном заказе на работу, когда система настроена на автоматическое создание заказов на работу на основе плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35aa0-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="35aa0-135">Ранее автоматически созданные заказы на работу могли содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="35aa0-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="35aa0-136">Однако теперь можно группировать заказы на работу по, например, активу, типу актива или функциональному местоположению.</span><span class="sxs-lookup"><span data-stu-id="35aa0-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="35aa0-137">(Созданные вручную заказы на работу уже могут быть сгруппированы таким образом, как это описано в предыдущем разделе этой темы.)</span><span class="sxs-lookup"><span data-stu-id="35aa0-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="35aa0-138">Включение группировки для автоматически создаваемых заказов на работу</span><span class="sxs-lookup"><span data-stu-id="35aa0-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="35aa0-139">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="35aa0-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="35aa0-140">Администраторы могут использовать параметры [управления компонентами](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="35aa0-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="35aa0-141">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="35aa0-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="35aa0-142">**Модуль:** *Управление активами*</span><span class="sxs-lookup"><span data-stu-id="35aa0-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="35aa0-143">**Имя компонента:** *Применение правил группировки заказов на работу во время выполнения плана обслуживания*</span><span class="sxs-lookup"><span data-stu-id="35aa0-143">**Feature name:** *Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="35aa0-144">Настройка группирования для автоматически создаваемых заказов на работу</span><span class="sxs-lookup"><span data-stu-id="35aa0-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="35aa0-145">Чтобы настроить группирование для автоматически создаваемых заказов на работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="35aa0-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="35aa0-146">Перейдите в раздел **Управление активами \> Настройка \> Профилактическое обслуживание \> Планы обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="35aa0-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="35aa0-147">Для каждого плана, в котором необходимо создать сгруппированные заказы на работу, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="35aa0-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="35aa0-148">Выберите план в области списка.</span><span class="sxs-lookup"><span data-stu-id="35aa0-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="35aa0-149">На экспресс-вкладке **Строки** убедитесь, что флажок **Автоматически создать** установлен на каждой строке.</span><span class="sxs-lookup"><span data-stu-id="35aa0-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="35aa0-150">Перейдите в раздел **Управление активами \> Периодические \> Профилактическое обслуживание \> Составление графика планов обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="35aa0-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="35aa0-151">В диалоговом окне **Составление графика планов обслуживания** в разделе **Период** укажите временной горизонт для плана (насколько далеко вперед искать запланированных задания обслуживания для создания для них работы).</span><span class="sxs-lookup"><span data-stu-id="35aa0-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="35aa0-152">Установите для параметра **Автоматически создавать заказ на работу по графику** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="35aa0-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="35aa0-153">В разделе **Заказ на работу** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="35aa0-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="35aa0-154">**Один заказ на работу на строку** — создание одного заказа на работу на каждую строку графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35aa0-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="35aa0-155">(Этот параметр предоставляет те же функциональные возможности, которые доступны, если функция *Применение правил группировки заказов на работу во время выполнения плана обслуживания* отключена.)</span><span class="sxs-lookup"><span data-stu-id="35aa0-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="35aa0-156">**Один заказ на работу на** — создание заказов на работу, сгруппированных в соответствии с настройками других параметров, которые становятся доступными при выборе данного параметра.</span><span class="sxs-lookup"><span data-stu-id="35aa0-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="35aa0-157">Если требуется применить параметры при выполнении только некоторых планов обслуживания, на экспресс-вкладке **Включаемые записи** добавьте фильтры так же, как это возможно для других пакетных заданий в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="35aa0-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="35aa0-158">На экспресс-вкладке **Выполнять в фоновом режиме** настройте параметры пакетной обработки и планирования так, как вы бы это делали для других пакетных заданий в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="35aa0-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="35aa0-159">Выберите **ОК**, чтобы выполнить и/или спланировать выбранные планы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35aa0-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]