---
title: Пулы заказа на работу
description: В этом разделе описывается, как работать с пулами заказов на работу в управлении активами.
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
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626370"
---
# <a name="work-order-pools"></a><span data-ttu-id="a7d9b-103">Пулы заказа на работу</span><span class="sxs-lookup"><span data-stu-id="a7d9b-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="a7d9b-104">Пулы заказов на работу можно использовать для группировки заказов на работу, для которых имеется что-либо общее.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="a7d9b-105">Ниже приводятся примеры того, что можно создать пулы заказов на работу для:</span><span class="sxs-lookup"><span data-stu-id="a7d9b-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="a7d9b-106">Рабочие экипажи, например, экипаж по обслуживанию A, экипаж по обслуживанию B</span><span class="sxs-lookup"><span data-stu-id="a7d9b-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="a7d9b-107">Профессиональные навыки, например электрики или водопроводчики</span><span class="sxs-lookup"><span data-stu-id="a7d9b-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="a7d9b-108">Физические местоположения</span><span class="sxs-lookup"><span data-stu-id="a7d9b-108">Physical locations</span></span>  

- <span data-ttu-id="a7d9b-109">Графики времени, например, недели или другие периоды</span><span class="sxs-lookup"><span data-stu-id="a7d9b-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="a7d9b-110">При необходимости можно создать один заказ на работу в нескольких пулах заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="a7d9b-111">Создание пула заказов на работу</span><span class="sxs-lookup"><span data-stu-id="a7d9b-111">Create a work order pool</span></span>

<span data-ttu-id="a7d9b-112">На странице списка **Все пулы заказов на работу** или **Активные пулы заказов на работу** можно получить обзор пулов заказов на работу и создать новые пулы.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="a7d9b-113">Выберите **Управление активами** > **Общее** > **Пулы заказов на работу** > **Все пулы заказов на работу** или **Активные пулы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="a7d9b-114">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-114">Select **New**.</span></span>

3. <span data-ttu-id="a7d9b-115">В поле **Пул** введите код для пула заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="a7d9b-116">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="a7d9b-117">Установите параметр **Активный** на **Да**, чтобы указать, что пул заказов на работу активен.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="a7d9b-118">Установите параметр **Удалить связи заказов на работу** на **Да**, если необходимо автоматически удалять заказы на работу из пула заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="a7d9b-119">В поле **Удалить состояние жизненного цикла** выберите состояние жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="a7d9b-120">Например, состояние жизненного цикла заказа на работу для завершения заказа на работу может быть настроено таким образом, чтобы автоматически удалять отношения с пулами заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="a7d9b-121">Можно сразу начать добавлять заказы на работу в пул заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="a7d9b-122">На экспресс-вкладке **Заказы на работу** выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="a7d9b-123">Выберите заказ на работу в поле **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="a7d9b-124">Связанные поля обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="a7d9b-125">Повторите шаги 8–9, чтобы добавить другие заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="a7d9b-126">Если добавленные заказы на работу должны выполняться в конкретном порядке, в поле **Порядок сортировки** можно ввести номера **1**, **2**, **3** и так далее, чтобы указать этот заказ.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="a7d9b-127">Чтобы просмотреть список всех заказов на работу, включенных в пул заказов на работу, в области действий на вкладке **Пул заказов на работу** в группе **просмотр связанного пула заказов на работу** выберите **заказы на работу**, чтобы открыть страницу списка **Все заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="a7d9b-128">Чтобы рассчитать и просмотреть максимальную мощность для графика обслуживания, незапланированных заказов на работу и спланированных заказов на работу, в области действий на вкладке **Пул заказов на работу** в группе **просмотр связанного пула заказов на работу** выберите **максимальная мощность** для открытия диалогового окна **Расчет максимальной мощности**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="a7d9b-129">Чтобы рассчитать и просмотреть для номенклатур (запчасти и другие необходимые номенклатуры), соответствующих графику обслуживания, незапланированным заказам на работу и запланированным заказам на работу, в области действий на вкладке **Пул заказов на работу** в группе **просмотр связанного пула заказов на работу** выберите **Прогноз по номенклатурам** для открытия диалогового окна **Рассчитать прогноз по номенклатурам**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="a7d9b-130">Чтобы просмотреть список заявок на покупку, связанных с заказами на работу в пуле заказов на работу, в области действий на вкладке **Пул заказов на работу** в группе **Закупки** выберите **Заявка на покупку заказа на работу**, чтобы открыть страницу списка **Заявка на покупку заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="a7d9b-131">Чтобы просмотреть список заказов на покупку, связанных с заказами на работу в пуле заказов на работу, в области действий на вкладке **Пул заказов на работу** в группе **Закупки** выберите **Покупка по заказу на работу**, чтобы открыть страницу списка **Покупка по заказу на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="a7d9b-132">Если пул заказов на работу больше не имеет отношения к планированию работ, установите для параметра **Активен** значение **Нет** в представлении списка страницы **Пул заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="a7d9b-133">Чтобы удалить все строки заказа на работу, установите для параметра **Удалить связи заказов на работу** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="a7d9b-134">Этот параметр полезен, если, например, необходимо создать пустой пул, который впоследствии можно будет использовать для других заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="a7d9b-135">Когда вы будете готовы использовать пул заказов на работу для создания новых связей заказов на работу позднее, не забудьте установить для параметра **Удалить связи заказов на работу** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="a7d9b-136">На приведенном ниже рисунке показан пример страницы списка **Пул заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Рисунок 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="a7d9b-138">Добавление заказа на работу в пул заказов на работу</span><span class="sxs-lookup"><span data-stu-id="a7d9b-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="a7d9b-139">Как описано в предыдущем разделе, при создании пула можно добавлять заказы на работу в пул заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="a7d9b-140">Заказы на обслуживание можно также добавить в пул заказов на работу на странице списка **все заказы на работу** или **активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="a7d9b-141">Выберите заказ на работу, а затем в области действий на вкладке **Заказ на работу** в группе **Поддержка** выберите **Пул заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="a7d9b-142">Выберите заказ на работу в списке и щелкните **Пул заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="a7d9b-143">В диалоговом окне **Поддержка пула заказов на работу** в поле **добавить/удалить** выберите **добавить**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="a7d9b-144">Выберите пул заказов на работу в поле **Пул**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="a7d9b-145">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-145">Select **OK**.</span></span>

6. <span data-ttu-id="a7d9b-146">Чтобы поместить заказ на работу, добавленный в конкретном заказе, в пул заказов на работу, на странице списка **Все пулы заказов на работу** или **Активные пулы заказов на работу** выберите пул, а затем выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="a7d9b-147">Затем на странице **Пул заказов на работу** на экспресс-вкладке **заказы на работу** с помощью поля **Порядок сортировки** настройте порядок сортировки заказов на работу, включенных в пул.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="a7d9b-148">Чтобы удалить выбранный заказ на работу из пула заказов на работу, повторите эти шаги, но выберите **Удалить** на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="a7d9b-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

