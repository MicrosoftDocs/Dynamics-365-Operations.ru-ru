---
title: Циклы обслуживания
description: В этом разделе описываются циклы обслуживания в модуле управления активами.
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
ms.openlocfilehash: a0ac4820d2efa37387382c2890e3ddc7dbc0878b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875858"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="c54a2-103">Циклы обслуживания</span><span class="sxs-lookup"><span data-stu-id="c54a2-103">Maintenance rounds</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c54a2-104">В модуле **Управление активами** можно создавать циклы обслуживания для различных активов, на которых необходимо выполнять аналогичную задачу через регулярные промежутки времени.</span><span class="sxs-lookup"><span data-stu-id="c54a2-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="c54a2-105">Например, задания смазки или проверки на безопасность, которые должны быть выполнены на нескольких станках в пределах одного и того же интервала.</span><span class="sxs-lookup"><span data-stu-id="c54a2-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="c54a2-106">Первым шагом является создание цикла обслуживания, включая активы, для которых требуется одна и та же форма задания обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="c54a2-107">Затем запланируйте циклы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="c54a2-108">По завершении планирования циклов обслуживания можно просмотреть все записи заданий, относящиеся к циклу, в пунктах **Весь график обслуживания** и **Открытые строки графика обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="c54a2-109">Циклы обслуживания могут быть также настроены в функциональных местоположениях для выполнения по активам, установленным в функциональном местоположении во время создания заказа на работу на основе цикла.</span><span class="sxs-lookup"><span data-stu-id="c54a2-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="c54a2-110">См. раздел [Создание функциональных местоположений](../functional-locations/create-functional-locations.md) для получения дополнительных сведений о настройке циклов обслуживания в функциональных местоположениях.</span><span class="sxs-lookup"><span data-stu-id="c54a2-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="c54a2-111">Настройка цикла обслуживания</span><span class="sxs-lookup"><span data-stu-id="c54a2-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="c54a2-112">Щелкните **Управление активами** > **Настройка** > **Профилактическое обслуживание** > **Циклы обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="c54a2-113">Щелкните **Создать**, чтобы создать новый цикл обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="c54a2-114">Вставьте идентификатор в поле **Цикл обслуживания** и имя для цикла обслуживания в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="c54a2-115">Выберите дату начала для цикла в поле **Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="c54a2-116">В полях **Время завершения, дней** и **Время завершения, часы** можно вставить ожидаемую конечную дату в днях или часах.</span><span class="sxs-lookup"><span data-stu-id="c54a2-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="c54a2-117">Ожидаемая дата окончания рассчитывается относительно даты начала, которая рассчитывается при создании строк графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="c54a2-118">Например, можно вставить "7" в поле **Время завершения, дней**, чтобы указать, что связанное задание должно быть завершено в течение недели с даты начала.</span><span class="sxs-lookup"><span data-stu-id="c54a2-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="c54a2-119">Выберите "Да" на переключателе **Автосоздание**, если заказы на работу должны автоматически создаваться из строк графика обслуживания, созданных из этого цикла обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="c54a2-120">В поле **Тип заказа на работу** выберите тип заказа на работу, который будет использоваться в заказах на работу, созданных из этого цикла обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="c54a2-121">В поле **Уровень обслуживания** выберите уровень обслуживания заказа на работу, который будет использоваться в заказах на работу, созданных из этого цикла обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="c54a2-122">На экспресс-вкладке **Строки активов** выберите **Добавить**, чтобы добавить актив в цикл обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="c54a2-123">Номер строки автоматически вставляется в поле **Номер строки**, чтобы указать последовательность активов в цикле обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="c54a2-124">Выберите актив в поле **Актив**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="c54a2-125">Выберите тип заданий обслуживания для актива в поле **Тип заданий обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="c54a2-126">При необходимости выберите **Вариант типа задания обслуживания** и **Специальность**, связанные с типом задания обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="c54a2-127">Выберите повторение (день, неделя и т. д.) в поле **Тип периода**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="c54a2-128">В поле **Частота периода** введите число повторений для цикла обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="c54a2-129">Пример. Если в поле **Тип периода** было выбрано значение "День", и в это поле введено число "7", новые строки цикла обслуживания создаются в ходе планирования профилактического обслуживания раз в неделю.</span><span class="sxs-lookup"><span data-stu-id="c54a2-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="c54a2-130">Выберите дату начала для включения актива в цикл обслуживания в поле **Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="c54a2-131">Эта дата может отличаться от даты начала, установленной в цикле обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="c54a2-132">Повторите шаги 9–16, чтобы добавить дополнительные активы в цикл обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="c54a2-133">На экспресс-вкладке **Строки функциональных местоположений** выберите **Добавить**, чтобы добавить функциональное местоположение в цикл обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="c54a2-134">См. описание соответствующих полей выше.</span><span class="sxs-lookup"><span data-stu-id="c54a2-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="c54a2-135">Доступны те же поля, что и для создания строки актива, но при необходимости можно также выбрать значения **Производитель** и **Модель** для функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c54a2-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="c54a2-136">Если в строке выбрано только функциональное местоположение, но не выбраны значения **Тип актива**, **Изготовитель**, **Модель**, **Тип задания обслуживания**, **Вариант типа задания обслуживания** и **Специальность**, все активы, которые связаны с этим функциональным местоположением, во время планирования обслуживания будут включены в цикл обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="c54a2-137">На экспресс-вкладке **Пулы** щелкните **Добавить** для выбора пула заказов на работу, который должен быть включен в цикл обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="c54a2-138">Несколько пулов заказов на работу можно подключить к одному циклу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="c54a2-139">Сохраните настройку.</span><span class="sxs-lookup"><span data-stu-id="c54a2-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="c54a2-140">Поля **Ресурсы** и **Строки**, расположенные в группе **Сведения** на экспресс- вкладке **Заголовок**, показывают общее число активов и строк, которые связаны с выбранным циклом обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

![Рисунок 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="c54a2-142">Запланировать циклы обслуживания</span><span class="sxs-lookup"><span data-stu-id="c54a2-142">Schedule maintenance rounds</span></span>

<span data-ttu-id="c54a2-143">После настройки цикла обслуживания можно выполнить задание планирования, чтобы запланировать все задания, имеющие отношение к циклу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-143">When you have set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="c54a2-144">Щелкните **Управление активами** > **Периодические операции** > **Профилактическое обслуживание** > **Запланировать циклы обслуживания** или **Управление активами** > **Общее** > **График обслуживания** > **Весь график обслуживания** или **Открыть строки графика обслуживания** или **Открыть пулы графика обслуживания** > выберите строку графика обслуживания в списке > кнопка **Циклы обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-144">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="c54a2-145">В поле **Период** выберите тип периода, который будет использоваться для задания планирования.</span><span class="sxs-lookup"><span data-stu-id="c54a2-145">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="c54a2-146">В поле **Частота периода** введите количество периодов, которые должны быть включены в задание планирования.</span><span class="sxs-lookup"><span data-stu-id="c54a2-146">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="c54a2-147">Начало планирования является текущей датой.</span><span class="sxs-lookup"><span data-stu-id="c54a2-147">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="c54a2-148">Выберите "Да" для переключателя **Автосоздание**, если заказ на работу должен быть автоматически создан на основе цикла обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-148">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="c54a2-149">Если этот переключатель установлен в значение "Да", а кнопка переключателя **Автосоздание** также установлена в значение "Да" в форме **Циклы обслуживания**, заказы на работу создаются на основе строк цикла обслуживания, а строки графика обслуживания со статусом "Заказ на работу создан" также создаются.</span><span class="sxs-lookup"><span data-stu-id="c54a2-149">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="c54a2-150">Если только один из переключателей **Автосоздание** имеет значение "Да", в этом раскрывающемся списке или в **Циклы обслуживания**, создаются только строки графика обслуживания со статусом "Создано".</span><span class="sxs-lookup"><span data-stu-id="c54a2-150">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="c54a2-151">В этом случае заказы на работу не создаются.</span><span class="sxs-lookup"><span data-stu-id="c54a2-151">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="c54a2-152">Если необходимо, можно выбрать отдельные циклы или другую дату начала для запланированного задания.</span><span class="sxs-lookup"><span data-stu-id="c54a2-152">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="c54a2-153">Щелкните **Фильтр** и добавьте циклы, которые требуется включить.</span><span class="sxs-lookup"><span data-stu-id="c54a2-153">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="c54a2-154">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-154">Click **OK**.</span></span>

7. <span data-ttu-id="c54a2-155">Теперь можно увидеть задания циклов обслуживания в модуле **Управление активами** > **Общее** > **График обслуживания** > **Весь график обслуживания** или **Открыть строки графика обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-155">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="c54a2-156">Если запланированные циклы связаны с пулом заказов на работу, можно также просмотреть строки графика обслуживания в пункте **Открыть пулы графиков обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="c54a2-156">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c54a2-157">Строки графика обслуживания, созданные на основе цикла, имеют тип ссылки "Циклы обслуживания".</span><span class="sxs-lookup"><span data-stu-id="c54a2-157">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

![Рисунок 2](media/14-preventive-maintenance.png)

![Рисунок 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="c54a2-160">Когда заказы на работу создаются вручную по активам, которые покрываются гарантией поставщика, отображается диалоговое окно, чтобы пользователь знал о гарантии.</span><span class="sxs-lookup"><span data-stu-id="c54a2-160">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="c54a2-161">После этого создание заказа на работу может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="c54a2-161">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="c54a2-162">Проверка гарантийных отношений пропускается для автоматически создаваемых заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="c54a2-162">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="c54a2-163">Можно настроить пакетное задание на экспресс-вкладке **Выполнять в фоновом режиме**, чтобы запланировать циклы с регулярными интервалами.</span><span class="sxs-lookup"><span data-stu-id="c54a2-163">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="c54a2-164">Если цикл включен в несколько пулов заказов на работу (см. раздел [Пулы заказов на работу](../work-orders/work-order-pools.md)), то для каждого пула в разделе **Открыть пулы графика обслуживания** отображается одна запись.</span><span class="sxs-lookup"><span data-stu-id="c54a2-164">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c54a2-165">Это сделано для оптимизации параметров фильтрации для пулов заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="c54a2-165">This is done to optimize the filtering options for work order pools.</span></span>
