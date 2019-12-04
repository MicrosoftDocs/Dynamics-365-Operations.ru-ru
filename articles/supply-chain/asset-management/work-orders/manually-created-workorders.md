---
title: Созданные вручную заказы на работу
description: В этом разделе описывается, как вручную создавать заказы на работу в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2652458a5fea9e46b8b68d3b197d2ccb1385731d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811760"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="4ebbc-103">Созданные вручную заказы на работу</span><span class="sxs-lookup"><span data-stu-id="4ebbc-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="4ebbc-104">Можно создать заказ на работу вручную двумя способами:</span><span class="sxs-lookup"><span data-stu-id="4ebbc-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="4ebbc-105">На странице **Все заказы на работу** или **Активные заказы на работу**</span><span class="sxs-lookup"><span data-stu-id="4ebbc-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="4ebbc-106">На странице **Все запросы на обслуживание**, **Активные запросы на обслуживание** или **Запросы на обслуживание моего функционального местоположения**</span><span class="sxs-lookup"><span data-stu-id="4ebbc-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="4ebbc-107">Создать заказ на работу</span><span class="sxs-lookup"><span data-stu-id="4ebbc-107">Create work order</span></span>

1. <span data-ttu-id="4ebbc-108">Выберите **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4ebbc-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-109">Select **New**.</span></span>

3. <span data-ttu-id="4ebbc-110">В диалоговом окне **создать заказ на работу** выберите тип заказа на работу в поле **Тип заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="4ebbc-111">Если требуется, выберите **описание**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="4ebbc-112">В поле **Актив** выберите актив.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="4ebbc-113">При выборе актива в раскрывающемся списке **Актив** могут быть доступны три вкладки:</span><span class="sxs-lookup"><span data-stu-id="4ebbc-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="4ebbc-114">**Активные активы** — эта вкладка содержит список всех активов с состоянием жизненного цикла актива "Активный".</span><span class="sxs-lookup"><span data-stu-id="4ebbc-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="4ebbc-115">**Представление актива** — эта вкладка отображает представление дерева функциональных местоположений и активов, установленных в них.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="4ebbc-116">**Мои активы** — Эта вкладка содержит активы, которые относятся к функциональным местоположениям, на которые может быть распределен пользователь (сотрудник, вошедший в систему).</span><span class="sxs-lookup"><span data-stu-id="4ebbc-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="4ebbc-117">(Дополнительные сведения о настройке см. в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md).) Если ни одно функциональное местоположение не настроено для работника в [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md), вкладка **Мои активы** недоступна.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="4ebbc-118">Выберите тип заданий обслуживания для заказа на работу в поле **Тип заданий обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="4ebbc-119">При необходимости выберите **Вариант типа задания обслуживания** и **Специальность**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="4ebbc-120">Если необходимо, можно изменить уровень обслуживания для заказа на работу в поле **Уровень обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="4ebbc-121">Выберите **Ожидаемая дата начала** и **Ожидаемая дата завершения** в связанных полях.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="4ebbc-122">Щелкните **ОК**, чтобы создать заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="4ebbc-123">На странице списка **Все заказы на работу** можно редактировать заказ на работу по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="4ebbc-124">Обратите внимание на следующие аспекты:</span><span class="sxs-lookup"><span data-stu-id="4ebbc-124">Note the following points:</span></span>

- <span data-ttu-id="4ebbc-125">В представлении сведений на странице списка **Все заказы на работу** можно добавить несколько активов в заказ на работу, добавив строки на экспресс-вкладке **Задания обслуживания для заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="4ebbc-126">В активе можно выбрать только типы заданий обслуживания, которые определены в типе актива, который выбран к активе.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="4ebbc-127">Если вы измените уровень обслуживания активов или критичность актива после того, как вы уже использовали актив в заказе на работу, уровень обслуживания или критичность в заказе на работу не обновляется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="4ebbc-128">Для получения дополнительных сведений об уровнях обслуживания и критичностях см. разделы [Уровни обслуживания активов](../setup-for-objects/object-priorities.md) и [Типы критичности активов](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="4ebbc-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="4ebbc-129">Критичность в заказе на работу пересчитывается каждый раз при добавлении задания заказа на работу в заказ на работу или удалении задания заказа на работу из него.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="4ebbc-130">В представлении сведений **Все заказы на работу** > вкладка **Заголовок** > экспресс-вкладка **График**, в полях **Ответственная группа** или **Ответственный** можно выбрать группу ответственных специалистов по обслуживанию или ответственного специалиста по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="4ebbc-131">Эти параметры могут быть изменены, если заказ на работу активен.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="4ebbc-132">Например, они могут быть изменены при изменении состояния жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="4ebbc-133">Автоматический выбор, сделанный при создании заказа на работу, основан на настройке на странице **Ответственные специалисты по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="4ebbc-134">Если добавить или удалить задания заказа на работу после создания заказа на работу, и если поля **Ответственная группа** и **Ответственный** пусты при обновлении заказа на работу, управление активами пытается найти группы ответственных сотрудников по обслуживанию или ответственного сотрудника по обслуживанию на предмет возможных соответствий на странице настройки.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="4ebbc-135">Если поле **Ответственная группа** или **Ответственный** уже задано при обновлении заказа на работу, изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="4ebbc-136">Для получения дополнительных сведений об ответственных специалистах по обслуживанию и группах специалистов, см. раздел [Ответственные специалисты по обслуживанию](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="4ebbc-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="4ebbc-137">На странице [Состояние обслуживания](../controlling-and-reporting/maintenance-status.md) можно выполнить расчет для получения обзора рабочей нагрузки для входящих и завершенных заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="4ebbc-138">В представлении сведения на странице **все заказы на работу** на экспресс-вкладке **сведения о строке** можно использовать поля **Широта** и **долгота** для добавления географических координат для актива, выбранного в задании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="4ebbc-139">Создать связанный заказ на работу</span><span class="sxs-lookup"><span data-stu-id="4ebbc-139">Create related work order</span></span>

<span data-ttu-id="4ebbc-140">Можно создать заказ на работу, связанный с существующим заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="4ebbc-141">Эта возможность полезна, если, например, вы хотите работать с первичными и вторичными заказами на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="4ebbc-142">Новый заказ на работу базируется на задании заказа на работу из существующего заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="4ebbc-143">Выберите **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4ebbc-144">Выберите заказ на работу, ля которого необходимо создать связанный заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="4ebbc-145">В области действий на вкладке **заказ на работу** в группе **Создать** выберите **Связанный заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="4ebbc-146">В диалоговом окне **Создать связанный заказ на работу** в поле **Задание заказа на работу** выберите задание заказа на работу, для которого требуется создать связанный заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="4ebbc-147">В поле **Тип заданий обслуживания** выберите тип задания обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="4ebbc-148">Выберите вариант и специальность, связанные с типом задания обслуживания в полях **Вариант типа задания обслуживания** и **Специальность** по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="4ebbc-149">Если этот заказ на работу является первым связанным заказом на работу, созданным для выбранного заказа на работу, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4ebbc-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="4ebbc-150">Выберите параметр **создать заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="4ebbc-151">В поле **Тип заказа на работу** выберите тип заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="4ebbc-152">В **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="4ebbc-153">Если необходимо, в поле **Уровень обслуживания** измените уровень обслуживания для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="4ebbc-154">В полях **Ожидаемая дата начала** и **Ожидаемая дата завершения** выберите ожидаемые начальную и конечную даты.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="4ebbc-155">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-155">Select **OK**.</span></span> <span data-ttu-id="4ebbc-156">Новый связанный заказ на работу отображается на странице списка **Все заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="4ebbc-157">Если заказ на работу, для которого создается этот связанный заказ на работу, уже имеет связанные заказы на работу, выполните следующие действия, чтобы добавить новое задание заказа на работу в существующий связанный заказ на работу:</span><span class="sxs-lookup"><span data-stu-id="4ebbc-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="4ebbc-158">Выберите параметр **добавить в связанный заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="4ebbc-159">В поле **заказ на работу** выберите связанный заказ на работу, чтобы добавить новое задание заказа на работу в него.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="4ebbc-160">Если необходимо, в поле **Уровень обслуживания** измените уровень обслуживания для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="4ebbc-161">В полях **Ожидаемая дата начала** и **Ожидаемая дата завершения** измените ожидаемые начальную и конечную даты по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="4ebbc-162">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-162">Select **OK**.</span></span> <span data-ttu-id="4ebbc-163">Задание заказа на работу добавляется к существующему связанному заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="4ebbc-164">На приведенном ниже рисунке показан пример диалогового окна **Создать связанный заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Рисунок 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="4ebbc-166">Если была настроена маска связанного заказа на работу в **Параметры управления активами** >  вкладка **Заказы на работу** > поле **Маска связанных заказов на работу**, коды заказов на работу будут созданы в соответствии с настройкой маски.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="4ebbc-167">Если не была настроена никакая маска связанного заказа на работу, то для связанных заказов на работу используется следующий доступный код заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="4ebbc-168">Копировать заказ на работу</span><span class="sxs-lookup"><span data-stu-id="4ebbc-168">Copy a work order</span></span>

<span data-ttu-id="4ebbc-169">Можно быстро создать новый заказ на работу из существующего заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="4ebbc-170">Этот способ работы с заказами на работу отличается от создания заказов на работу на основе [планов обслуживания](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="4ebbc-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="4ebbc-171">Это полезно, если, например, заказ на работу содержит множество заданий заказа на работу, и различные задания должны выполняться с различными активами с регулярными интервалами.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="4ebbc-172">Выберите **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4ebbc-173">Выберите заказ на работу, из которого скопировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="4ebbc-174">В области действий на вкладке > **заказ на работу** > в группе **Создать** выберите **Копировать заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="4ebbc-175">Отображается настройка заказа на работу из выбранного заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="4ebbc-176">Если необходимо, можно изменить некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="4ebbc-177">Выберите **ОК**, чтобы создать новый заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="4ebbc-178">На странице списка **Все заказы на работу** можно редактировать заказ на работу по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="4ebbc-179">Когда создается новый заказ на работу, часть информации копируется непосредственно из существующего заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="4ebbc-180">Сведения о прогнозах, инструментах, контрольных списках обслуживания, функциональном местоположении, адресах и планировании не копируются.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="4ebbc-181">Вместо этого оно инициализируется из текущей настройки в управлении активами.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="4ebbc-182">Таким образом, если эта информация была изменена с момента создания первого заказа на работу и времени, когда была сделана копия заказа на работу, эти изменения включаются в новый заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="4ebbc-183">Примеры включают изменения в прогнозах и обновления в контрольные списки обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="4ebbc-184">На приведенном ниже рисунке показан пример диалогового окна **Копировать заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Рисунок 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="4ebbc-186">Создание заказа на работу на основе запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="4ebbc-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="4ebbc-187">Выберите **Управление активами** > **Общее** > **Запросы на обслуживание** > **Все запросы на обслуживание** или **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="4ebbc-188">Выберите запрос на обслуживание, для которого необходимо создать заказ на работу, и щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="4ebbc-189">В области действий на вкладке > **Запрос на обслуживание** > в группе **Создать** выберите **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="4ebbc-190">В диалоговом окне **заказ на работу** задайте поля.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="4ebbc-191">Если в запросе на обслуживание выбран тип задания обслуживания, можно выбрать другой тип задания обслуживания, при создании заказа на работу, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="4ebbc-192">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-192">Select **OK**.</span></span> <span data-ttu-id="4ebbc-193">Сообщение указывает, что заказ на работу создан.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="4ebbc-194">Чтобы просмотреть заказы на работу, которые связаны с запросом на обслуживание, выберите запрос на обслуживание на странице списка **Все запросы на обслуживание** или **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="4ebbc-195">Затем, в области действий на вкладке **Запрос на обслуживание**, в группе **Просмотр** выберите **Заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="4ebbc-196">На приведенном ниже рисунке показан пример диалогового окна **Создание заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Рисунок 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="4ebbc-198">Если вы хотите, чтобы заказы на работу создавались автоматически, вы можете запланировать задания плана обслуживания или настроить "Автосоздание" [планы обслуживания](../preventive-and-reactive-maintenance/maintenance-plans.md) или [циклы обслуживания](../preventive-and-reactive-maintenance/maintenance-rounds.md) по активу.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="4ebbc-199">Заказы на работу, созданные на основе запросов на обслуживание на странице списка **Весь график обслуживания**, имеют типы заданий обслуживания, выбранные в запросах на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

