---
title: График обслуживания
description: В этом разделе описываются графики обслуживания в управлении активами.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 351e088ece0512fee1bb5f9dad020f32f7728fe4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436069"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="8a58b-103">График обслуживания</span><span class="sxs-lookup"><span data-stu-id="8a58b-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8a58b-104">График обслуживания содержит список всех ожидаемых планов профилактического обслуживания, запросов на обслуживание и циклов обслуживания. Некоторые строки графика могли быть преобразованы в заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="8a58b-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="8a58b-105">Четыре представления графика обслуживания слегка различаются в зависимости от того, какие строки графика обслуживания нужно просмотреть.</span><span class="sxs-lookup"><span data-stu-id="8a58b-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="8a58b-106">Пункт меню</span><span class="sxs-lookup"><span data-stu-id="8a58b-106">Menu item</span></span>                  | <span data-ttu-id="8a58b-107">Описание содержимого</span><span class="sxs-lookup"><span data-stu-id="8a58b-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a58b-108">Весь график обслуживания</span><span class="sxs-lookup"><span data-stu-id="8a58b-108">All maintenance schedule</span></span>       | <span data-ttu-id="8a58b-109">Отображаются все строки графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8a58b-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="8a58b-110">Мой план активов</span><span class="sxs-lookup"><span data-stu-id="8a58b-110">My asset schedule</span></span>        | <span data-ttu-id="8a58b-111">Все строки графика обслуживания, содержащие активы, установленные в функциональных местоположениях, с которыми вы связаны в качестве работника (настраивается в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md)), отображаются в этом списке.</span><span class="sxs-lookup"><span data-stu-id="8a58b-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="8a58b-112">Открытие строки графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="8a58b-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="8a58b-113">В этом списке отображаются строки графика обслуживания со статусом "Создано" — означает, что они еще не преобразованы в заказ на работу или они не были удалены.</span><span class="sxs-lookup"><span data-stu-id="8a58b-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="8a58b-114">Открытие пулов графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="8a58b-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="8a58b-115">В этом списке отображаются строки графика обслуживания, имеющие отношение к пулу заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="8a58b-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="8a58b-116">Если строка графика обслуживания включена в несколько пулов заказов на работу (см. раздел [Пулы заказов на работу](../work-orders/work-order-pools.md)), то для каждого пула в разделе **Открыть пулы графика обслуживания** отображается одна запись.</span><span class="sxs-lookup"><span data-stu-id="8a58b-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="8a58b-117">Это сделано для оптимизации параметров фильтрации в пулах заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="8a58b-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="8a58b-118">Чтобы открыть график обслуживания:</span><span class="sxs-lookup"><span data-stu-id="8a58b-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="8a58b-119">Щелкните **Управление активами** > **Общее** > **График обслуживания** > **Весь график обслуживания**, **Открыть строки графика обслуживания** или **Открыть пулы графиков обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="8a58b-120">Для обновления графика обслуживания щелкните **План обслуживания** или **Циклы обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="8a58b-121">Можно изменить строку графика обслуживания, выбрав ее и нажав **Правка**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="8a58b-122">Например, можно легко обновить уровень обслуживания или сотрудника, ответственного за задание.</span><span class="sxs-lookup"><span data-stu-id="8a58b-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="8a58b-123">Можно редактировать только те строки графика обслуживания, которые еще не были связаны с заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="8a58b-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="8a58b-124">Можно удалить строку графика обслуживания, выбрав ее на странице списка и нажав **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="8a58b-125">Можно отменить строку графика обслуживания, выбрав ее на странице списка и нажав **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="8a58b-126">Эта функция полезна, если, например, актив имеет план обслуживания 2 000 км и план обслуживания 10 000 км.</span><span class="sxs-lookup"><span data-stu-id="8a58b-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="8a58b-127">В этом случае может возникнуть необходимость отменить строку, созданную из плана обслуживания при пробеге 2 000 км, если она совпадает с обслуживанием при пробеге 10 000 км, 20 000 км, 30 000 км и так далее.</span><span class="sxs-lookup"><span data-stu-id="8a58b-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="8a58b-128">При отмене строки графика обслуживания, имеющей отношение к плану обслуживания, эта строка никогда не будет больше отображаться при планировании этого плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8a58b-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="8a58b-129">Можно выбрать несколько строк графика обслуживания в разделе **Все графики обслуживания** и щелкнуть **Пул заказов на работу**, если необходимо включить все выбранные строки в один и тот же пул заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="8a58b-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="8a58b-130">Можно выбрать несколько строк графика обслуживания в разделе **Весь график обслуживания** или **Открыть строки графика обслуживания** или **Открыть пулы графиков обслуживания** и щелкнуть **Настроить расписание**, если необходимо выполнить одинаковые коррекции в нескольких строках.</span><span class="sxs-lookup"><span data-stu-id="8a58b-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="8a58b-131">Можно изменить ожидаемые даты начала и завершения, уровень обслуживания и группу ответственных специалистов по обслуживанию или ответственного специалиста по обслуживанию для выбранных строк графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8a58b-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="8a58b-132">Когда строка графика обслуживания связана с заказом на работу, код заказа на работу будет отображен в поле **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="8a58b-133">В представлении сведений **Все активы** > на экспресс-вкладке **Планы обслуживания актива** можно выбрать план обслуживания для актива.</span><span class="sxs-lookup"><span data-stu-id="8a58b-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="8a58b-134">Если затем вы удалите строку плана обслуживания, связанную с активом в пункте **Все активы**, вы также автоматически удалите все строки графика обслуживания со статусом "Создано", которые были созданы на основе этого плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8a58b-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="8a58b-135">См. также [Создание актива](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="8a58b-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="8a58b-136">На следующей иллюстрации показана страница списка **Весь график обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="8a58b-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Рисунок 1](media/16-preventive-maintenance.png)

