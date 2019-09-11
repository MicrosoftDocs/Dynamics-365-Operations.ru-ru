---
title: Созданные вручную заказы на работу
description: В этом разделе описывается, как вручную создавать заказы на работу в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875860"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="ed4c1-103">Созданные вручную заказы на работу</span><span class="sxs-lookup"><span data-stu-id="ed4c1-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="ed4c1-104">Можно создать заказ на работу вручную двумя способами:</span><span class="sxs-lookup"><span data-stu-id="ed4c1-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="ed4c1-105">в разделе **Все заказы на работу** или **Активные заказы на работу**</span><span class="sxs-lookup"><span data-stu-id="ed4c1-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="ed4c1-106">в разделе **Все запросы на обслуживание**, **Активные запросы на обслуживание** или **Запросы на обслуживание моего функционального местоположения**</span><span class="sxs-lookup"><span data-stu-id="ed4c1-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="ed4c1-107">Создать заказ на работу</span><span class="sxs-lookup"><span data-stu-id="ed4c1-107">Create work order</span></span>

1. <span data-ttu-id="ed4c1-108">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ed4c1-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-109">Click the **New** button.</span></span>

3. <span data-ttu-id="ed4c1-110">В раскрывающемся списке **Создать заказ на работу** выберите тип заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="ed4c1-111">Если требуется, выберите описание.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-111">If required, select a description.</span></span>

5. <span data-ttu-id="ed4c1-112">Выберите актив для заказа на работу, а также тип задания обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="ed4c1-113">При выборе актива могут быть доступны три вкладки: вкладка **Мои активы** содержит активы, связанные с функциональными местоположениями, в которые вы (как работник, выполнивший вход в систему) можете быть назначены (настраивается в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="ed4c1-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="ed4c1-114">Если функциональные местоположения настроены для работника в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md), вкладка **Мои активы** не будет видна.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="ed4c1-115">Вкладка **Активные активы** содержит список всех активов с состоянием жизненного цикла актива "Активный".</span><span class="sxs-lookup"><span data-stu-id="ed4c1-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="ed4c1-116">Вкладка **Представление актива** отображает представление дерева функциональных местоположений и ресурсов, установленных в этих местоположениях.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="ed4c1-117">При необходимости выберите **Вариант типа задания обслуживания** и **Специальность**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="ed4c1-118">Если необходимо, можно изменить уровень обслуживания для заказа на работу в поле **Уровень обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="ed4c1-119">Выберите ожидаемые начальную и конечную даты в связанных полях.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="ed4c1-120">Щелкните **ОК**, чтобы создать новый заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="ed4c1-121">Отредактируйте заказ на работу в разделе **Все заказы на работу**, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="ed4c1-122">В разделе **Все заказы на работу** можно добавить несколько активов в заказ на работу в представлении "Сведения", добавив строки на экспресс-вкладке **Задания обслуживания для заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="ed4c1-123">В активе можно выбрать только типы заданий обслуживания, которые определены в типе актива, выбранном для актива.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="ed4c1-124">При изменении уровня обслуживания активов или критичности актива после того как они использовались в заказе на работу (см. [Уровни обслуживания активов](../setup-for-objects/object-priorities.md) и [Критичность активов](../setup-for-objects/object-criticalities.md)), уровень обслуживания или критичность в заказе на работу не будут соответственно обновлены.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="ed4c1-125">Критичность в заказе на работу пересчитывается каждый раз при добавлении или удалении строки заказа на работу в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="ed4c1-126">В представлении сведений **Все заказы на работу** > представление **Заголовок** > экспресс-вкладка **График** можно выбрать группу ответственных за обслуживание специалистов или ответственного специалиста по обслуживанию в полях **Ответственная группа** или **Ответственный**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="ed4c1-127">Эти параметры могут быть изменены, если заказ на работу активен, например, при изменении состояния жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="ed4c1-128">Автоматический выбор, сделанный при создании заказа на работу, основан на настройке в параметре **Ответственные специалисты по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="ed4c1-129">Если добавить или удалить задания заказа на работу после создания заказа на работу, а поля **Ответственная группа** и **Ответственный** пусты при обновлении заказа на работу, управление активами выполняет поиск возможных соответствий в форме настройки для группы ответственных сотрудников по обслуживанию или ответственного сотрудника по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="ed4c1-130">Если поле **Ответственная группа** или **Ответственный** уже заполнены при обновлении заказа на работу, изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="ed4c1-131">В поле **Состояние обслуживания** можно выполнить расчет для получения обзора рабочей нагрузки относительно входящих и завершенных заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="ed4c1-132">На экспресс-вкладке **Сведения по строке** используйте поля **Широта** и **Долгота** для добавления географических координат для актива, выбранного в задании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="ed4c1-133">Создать связанный заказ на работу</span><span class="sxs-lookup"><span data-stu-id="ed4c1-133">Create related work order</span></span>

<span data-ttu-id="ed4c1-134">Можно создать связанный заказ на работу с существующим заказом на работу, если, например, необходимо работать с первичным и вторичным заказами на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="ed4c1-135">Новый заказ на работу базируется на задании заказа на работу из существующего заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="ed4c1-136">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ed4c1-137">Выберите заказ на работу, для которого требуется создать связанный заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="ed4c1-138">Щелкните **Связанный заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="ed4c1-139">В раскрывающемся диалоговом окне **Создать связанный заказ на работу** выберите задание заказа на работу, для которого требуется создать связанный заказ на работу, в поле **Задание заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="ed4c1-140">Выберите тип задания обслуживания в поле **Тип задания обслуживания** и, если это необходимо, связанные вариант и специальность типа задания обслуживания в полях **Вариант типа задания обслуживания** и **Специальность**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="ed4c1-141">Если это первый создаваемый вами связанный заказ на работу, щелкните переключатель **Новый заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="ed4c1-142">Выберите **Тип заказа на работу** и **Описание** в соответствующих полях.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="ed4c1-143">Если необходимо, измените уровень обслуживания для заказа на работу в поле **Уровень обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="ed4c1-144">Вставьте ожидаемые начальную и конечную даты в связанных полях.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="ed4c1-145">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-145">Click **OK**.</span></span> <span data-ttu-id="ed4c1-146">Новый связанный заказ на работу отображается в списке **Все заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="ed4c1-147">Если создать связанный заказ на работу в заказе на работу, который уже имеет связанные заказы на работу, можно добавить задание заказа на работу в уже связанный заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="ed4c1-148">Это можно сделать, щелкнув переключатель **Добавить в связанный заказ на работу** на шаге 6.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="ed4c1-149">Затем выберите связанный заказ на работу, к которому необходимо добавить новое задание заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="ed4c1-150">При необходимости измените значения в полях **Уровень обслуживания**, **Ожидаемое начало** и **Ожидаемое окончание**, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="ed4c1-151">Задание заказа на работу добавляется к существующему связанному заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-151">The work order job is added to the existing related work order.</span></span>


![Рисунок 1](media/03-work-orders.png)

<span data-ttu-id="ed4c1-153">**Примечание.** Если была настроена маска связанного заказа на работу в поле **Параметры управления активами** > ссылка **Заказы на работу** > **Маска связанных заказов на работу**, коды заказов на работу будут созданы в соответствии с настройкой маски.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="ed4c1-154">Если не была настроена никакая маска связанного заказа на работу, то для связанных заказов на работу будет использован следующий доступный код заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="ed4c1-155">Копировать заказ на работу</span><span class="sxs-lookup"><span data-stu-id="ed4c1-155">Copy work order</span></span>

<span data-ttu-id="ed4c1-156">Можно быстро создать новый заказ на работу из существующего заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="ed4c1-157">Этот способ работы с заказами на работу отличается от создания заказов на работу на основе планов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="ed4c1-158">Это полезно, если, например, имеется заказ на работу, содержащий множество заданий заказа на работу с различными активами, которые должны выполняться с регулярными интервалами.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="ed4c1-159">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ed4c1-160">Выберите заказ на работу, из которого необходимо скопировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="ed4c1-161">Щелкните **Копировать заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-161">Click **Copy work order**.</span></span> <span data-ttu-id="ed4c1-162">Отображается настройка заказа на работу из выбранного заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="ed4c1-163">Если необходимо, можно изменить некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="ed4c1-164">Щелкните **ОК**, чтобы создать новый заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="ed4c1-165">Отредактируйте заказ на работу в разделе **Все заказы на работу**, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="ed4c1-166">Когда создается новый заказ на работу, часть информации копируется непосредственно из существующего заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="ed4c1-167">Сведения о прогнозах, инструментах, контрольных списках обслуживания, функциональном местоположении, адресах и планировании не копируется, но инициализируется из текущей настройки в управлении активами.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="ed4c1-168">Это означает, что если в эти данные были внесены изменения с момента создания первого заказа на работу до момента создания копии заказа на работу, эти изменения включаются в новый созданный заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="ed4c1-169">Примерами являются изменения в прогнозах или обновленные контрольные списки обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Рисунок 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="ed4c1-171">Создание заказа на работу на основе запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="ed4c1-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="ed4c1-172">Щелкните **Управление активами** > **Общее** > **Запросы на обслуживание** > **Все запросы на обслуживание** или **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="ed4c1-173">Выберите запрос на обслуживание, для которого необходимо создать заказ на работу, и щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="ed4c1-174">В разделе **Все запросы** щелкните **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="ed4c1-175">Заполните раскрывающийся список **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="ed4c1-176">Если в запросе на обслуживание выбран тип задания обслуживания, можно выбрать другой тип задания обслуживания, если это необходимо, при создании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="ed4c1-177">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-177">Click **OK**.</span></span> <span data-ttu-id="ed4c1-178">Будет выведено сообщение о том, что заказ на работу был создан.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="ed4c1-179">Если требуется просмотреть, какие заказы на обслуживание связаны с запросом на обслуживание, выберите запрос на обслуживание в списках **Все запросы на обслуживание** или **Активные запросы на обслуживание** и щелкните кнопку **Заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Рисунок 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="ed4c1-181">Заказы на работу можно также создать автоматически, планируя задания плана обслуживания, или путем настройки автоматического создания планов обслуживания или циклов обслуживания для актива.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="ed4c1-182">Заказы на работу, созданные на основе запросов на обслуживание в пункте **График обслуживания**, создаются с типами заданий обслуживания, выбранными в запросах на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

