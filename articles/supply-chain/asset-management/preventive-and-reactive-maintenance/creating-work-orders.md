---
title: Создание заказов на работу
description: В этом разделе описывается, как создавать заказы на работу в модуле "Управление активами".
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131801"
---
# <a name="creating-work-orders"></a><span data-ttu-id="32558-103">Создание заказов на работу</span><span class="sxs-lookup"><span data-stu-id="32558-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32558-104">После планирования заданий профилактического обслуживания следующим шагом будет создание заказов на работу для них.</span><span class="sxs-lookup"><span data-stu-id="32558-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="32558-105">Можно выполнить этот шаг, используя одно из графиков обслуживания.</span><span class="sxs-lookup"><span data-stu-id="32558-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="32558-106">Запланированные задания в графике обслуживания могут иметь различные типы ссылок, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="32558-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="32558-107">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="32558-107">Reference type</span></span> | <span data-ttu-id="32558-108">описание</span><span class="sxs-lookup"><span data-stu-id="32558-108">Description</span></span> |
|---|---|
| <span data-ttu-id="32558-109">Планы обслуживания</span><span class="sxs-lookup"><span data-stu-id="32558-109">Maintenance plans</span></span> | <span data-ttu-id="32558-110">Задания профилактического обслуживания, основанные на типах планов обслуживания *Время* или *Счетчик*.</span><span class="sxs-lookup"><span data-stu-id="32558-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="32558-111">Циклы обслуживания</span><span class="sxs-lookup"><span data-stu-id="32558-111">Maintenance rounds</span></span> | <span data-ttu-id="32558-112">Задания профилактического обслуживания, содержащие несколько активов, требующих подобного типа обслуживания.</span><span class="sxs-lookup"><span data-stu-id="32558-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="32558-113">Запрос на обслуживание</span><span class="sxs-lookup"><span data-stu-id="32558-113">Maintenance request</span></span> | <span data-ttu-id="32558-114">Запрос, созданный вручную для обслуживания или ремонта актива.</span><span class="sxs-lookup"><span data-stu-id="32558-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="32558-115">Этот запрос может быть преобразован в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="32558-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="32558-116">Создание заказов на работу на основе графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="32558-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="32558-117">Для создания заказов на работу, которые основаны на расписании обслуживания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="32558-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="32558-118">Откройте одну из следующих страниц, в зависимости от того, как вы хотите выбирать элементы планирования для заказов на работу:</span><span class="sxs-lookup"><span data-stu-id="32558-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="32558-119">Все расписание обслуживания ( **Управление активами \> Расписание обслуживания \> Все расписание обслуживания**)</span><span class="sxs-lookup"><span data-stu-id="32558-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="32558-120">Откройте строки расписания обслуживания (**Управление активами \> Расписание обслуживания \> Открыть строки расписания обслуживания**)</span><span class="sxs-lookup"><span data-stu-id="32558-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="32558-121">Откройте пулы расписаний обслуживания (**Управление активами \> Расписание обслуживания \> Открыть пулы расписаний обслуживания**)</span><span class="sxs-lookup"><span data-stu-id="32558-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="32558-122">В сетке установите флажок для каждого задания планового обслуживания, для которого необходимо создать заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="32558-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="32558-123">Затем на панели операций выберите **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="32558-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="32558-124">Откроется диалоговое окно **Создание заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="32558-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="32558-125">В поле **Прогноз часов обслуживания** отображается общее количество часов прогноза для выбранных строк.</span><span class="sxs-lookup"><span data-stu-id="32558-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Диалоговое окно создания заказов на работу](media/18-preventive-maintenance.png)

1. <span data-ttu-id="32558-127">В разделе **Параметры** укажите количество заказов на работу, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="32558-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="32558-128">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="32558-128">Select one of the following options:</span></span>

    - <span data-ttu-id="32558-129">**Один заказ на работу на строку** — создание одного заказа на работу на каждую строку графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="32558-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="32558-130">**Один заказ на работу на** — создание заказов на работу, сгруппированных в соответствии с настройками других параметров, которые становятся доступными при выборе данного параметра.</span><span class="sxs-lookup"><span data-stu-id="32558-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="32558-131">В поле **Тип заказа на работу** выберите тип заказа на работу, который будет использоваться для всех создаваемых заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="32558-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="32558-132">Выберите **ОК**, чтобы создать заказы на работу в соответствии с вашими настройками.</span><span class="sxs-lookup"><span data-stu-id="32558-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="32558-133">Группировка строк заказов на работу, которые создаются автоматически при выполнении плана обслуживания</span><span class="sxs-lookup"><span data-stu-id="32558-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32558-134">Функциональность, описанная в этом разделе, доступна в рамках предварительного выпуска.</span><span class="sxs-lookup"><span data-stu-id="32558-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="32558-135">Содержимое и функциональность могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="32558-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="32558-136">Дополнительные сведения о предварительных выпусках см. в разделе [Вопросы и ответы по обновлениям службы с одной версией](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="32558-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="32558-137">Эта функция позволяет определить правила для группировки строк заказа на работу в одном заказе на работу, когда система настроена на автоматическое создание заказов на работу на основе плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="32558-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="32558-138">Ранее автоматически созданные заказы на работу могли содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="32558-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="32558-139">Однако теперь можно группировать заказы на работу по, например, активу, типу актива или функциональному местоположению.</span><span class="sxs-lookup"><span data-stu-id="32558-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="32558-140">(Созданные вручную заказы на работу уже могут быть сгруппированы таким образом, как это описано в предыдущем разделе этой темы.)</span><span class="sxs-lookup"><span data-stu-id="32558-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="32558-141">Включение группировки для автоматически создаваемых заказов на работу</span><span class="sxs-lookup"><span data-stu-id="32558-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="32558-142">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="32558-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="32558-143">Администраторы могут использовать параметры [управления компонентами](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="32558-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="32558-144">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="32558-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="32558-145">**Модуль:** *Управление активами*</span><span class="sxs-lookup"><span data-stu-id="32558-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="32558-146">**Имя компонента:** *(Предварительная версия) Применение правил группировки заказов на работу во время выполнения плана обслуживания*</span><span class="sxs-lookup"><span data-stu-id="32558-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="32558-147">Настройка группирования для автоматически создаваемых заказов на работу</span><span class="sxs-lookup"><span data-stu-id="32558-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="32558-148">Чтобы настроить группирование для автоматически создаваемых заказов на работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="32558-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="32558-149">Перейдите в раздел **Управление активами \> Настройка \> Профилактическое обслуживание \> Планы обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="32558-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="32558-150">Для каждого плана, в котором необходимо создать сгруппированные заказы на работу, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="32558-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="32558-151">Выберите план в области списка.</span><span class="sxs-lookup"><span data-stu-id="32558-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="32558-152">На экспресс-вкладке **Строки** убедитесь, что флажок **Автоматически создать** установлен на каждой строке.</span><span class="sxs-lookup"><span data-stu-id="32558-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="32558-153">Перейдите в раздел **Управление активами \> Периодические \> Профилактическое обслуживание \> Составление графика планов обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="32558-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="32558-154">В диалоговом окне **Составление графика планов обслуживания** в разделе **Период** укажите временной горизонт для плана (насколько далеко вперед искать запланированных задания обслуживания для создания для них работы).</span><span class="sxs-lookup"><span data-stu-id="32558-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="32558-155">Установите для параметра **Автоматически создавать заказ на работу по графику** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="32558-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="32558-156">В разделе **Заказ на работу** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="32558-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="32558-157">**Один заказ на работу на строку** — создание одного заказа на работу на каждую строку графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="32558-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="32558-158">(Этот параметр предоставляет те же функциональные возможности, которые доступны, если функция *Применение правил группировки заказов на работу во время выполнения плана обслуживания* отключена.)</span><span class="sxs-lookup"><span data-stu-id="32558-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="32558-159">**Один заказ на работу на** — создание заказов на работу, сгруппированных в соответствии с настройками других параметров, которые становятся доступными при выборе данного параметра.</span><span class="sxs-lookup"><span data-stu-id="32558-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="32558-160">Если требуется применить параметры при выполнении только некоторых планов обслуживания, на экспресс-вкладке **Включаемые записи** добавьте фильтры так же, как это возможно для других пакетных заданий в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="32558-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="32558-161">На экспресс-вкладке **Выполнять в фоновом режиме** настройте параметры пакетной обработки и планирования так, как вы бы это делали для других пакетных заданий в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="32558-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="32558-162">Выберите **ОК**, чтобы выполнить и/или спланировать выбранные планы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="32558-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
