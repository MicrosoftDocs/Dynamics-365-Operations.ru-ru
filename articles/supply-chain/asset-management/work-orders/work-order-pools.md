---
title: Пулы заказа на работу
description: В этом разделе описывается, как работать с пулами заказов на работу в управлении активами.
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875862"
---
# <a name="work-order-pools"></a><span data-ttu-id="4fef9-103">Пулы заказа на работу</span><span class="sxs-lookup"><span data-stu-id="4fef9-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="4fef9-104">Пулы заказов на работу можно использовать для группировки заказов на работу, для которых имеется что-либо общее.</span><span class="sxs-lookup"><span data-stu-id="4fef9-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="4fef9-105">Например, можно создать пулы заказов на работу для следующего</span><span class="sxs-lookup"><span data-stu-id="4fef9-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="4fef9-106">рабочие экипажи, например экипаж по обслуживанию A, экипаж по обслуживанию B</span><span class="sxs-lookup"><span data-stu-id="4fef9-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="4fef9-107">профессиональные навыки, например электрики или водопроводчики</span><span class="sxs-lookup"><span data-stu-id="4fef9-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="4fef9-108">физические местоположения</span><span class="sxs-lookup"><span data-stu-id="4fef9-108">physical locations</span></span>  

- <span data-ttu-id="4fef9-109">графики времени, например недели или другие периоды</span><span class="sxs-lookup"><span data-stu-id="4fef9-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="4fef9-110">Если необходимо, один заказ на работу можно разместить в нескольких пулах заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="4fef9-111">Создание пула заказов на работу</span><span class="sxs-lookup"><span data-stu-id="4fef9-111">Create work order pool</span></span>

<span data-ttu-id="4fef9-112">В разделе **Все пулы заказов на работу** или **Активные пулы заказов на работу** можно получить обзор пулов заказов на работу и создать новые пулы.</span><span class="sxs-lookup"><span data-stu-id="4fef9-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="4fef9-113">Щелкните **Управление активами** > **Общее** > **Пулы заказов на работу** > **Все пулы заказов на работу** или **Активные пулы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="4fef9-114">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-114">Click **New**.</span></span>

3. <span data-ttu-id="4fef9-115">Вставьте идентификатор пула заказов на работу в поле **Пул** и имя в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="4fef9-116">Выберите "Да" на переключателе **Активный**, чтобы указать, что пул заказов на работу активен.</span><span class="sxs-lookup"><span data-stu-id="4fef9-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="4fef9-117">Выберите "Да" для переключателя **Удалить связи заказов на работу**, если необходимо автоматически удалять заказы на работу из пула заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="4fef9-118">В поле **Удалить состояние жизненного цикла** выберите состояние жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="4fef9-119">Например, состояние жизненного цикла заказа на работу для завершения заказа на работу может быть настроено таким образом, чтобы автоматически удалять отношения с пулами заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="4fef9-120">Можно сразу начать добавлять заказы на работу в пул заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="4fef9-121">На экспресс-вкладке **Заказы на работу** щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="4fef9-122">Выберите заказ на работу в поле **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="4fef9-123">Связанные поля обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="4fef9-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="4fef9-124">Повторите шаги 7–8, если требуется добавить дополнительные заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="4fef9-125">В поле **Порядок сортировки** можно указать, должны ли заказы на работу быть выполнены в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="4fef9-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="4fef9-126">Вставьте цифры 1, 2, 3 и так далее, чтобы указать конкретную последовательность для выбранных заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="4fef9-127">Нажмите кнопку **Заказы на работу**, чтобы просмотреть список всех заказов на работу, включенных в пул заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="4fef9-128">Нажмите кнопку **Максимальная мощность**, чтобы открыть окно **Максимальная мощность** для расчета и просмотра максимальной мощности для графика обслуживания, незапланированных заказов на работу и запланированных заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="4fef9-129">Нажмите кнопку **Прогноз по номенклатурам**, чтобы открыть окно **Прогноз по номенклатурам**, чтобы рассчитать и просмотреть прогнозы для номенклатур (запчасти и другие необходимые номенклатуры), соответствующих графику обслуживания, незапланированным заказам на работу и запланированным заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="4fef9-130">Нажмите кнопку **Заявка на покупку по заказу на работу**, чтобы открыть окно **Заявка на покупку по заказу на работу** для просмотра списка заявок на покупку, связанных с заказами на работу в пуле заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="4fef9-131">Нажмите кнопку **Покупка по заказу на работу**, чтобы открыть список **Покупка по заказу на работу** для просмотра списка заказов на покупку, связанных с заказами на работу в пуле заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="4fef9-132">Если пул заказов на работу больше не имеет отношения к планированию работ, установите для флажка **Активен** для этого пула значение "Нет" в представлении списка **Пул заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="4fef9-133">Установите флажок **Удалить связи заказов на работу**, если необходимо удалить все строки заказа на работу, например, чтобы создать пустой пул, который впоследствии можно будет использовать для других заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="4fef9-134">Не забудьте снять флажок **Удалить связи заказов на работу**, если необходимо использовать пул заказов на работу для создания новых отношений заказов на работу позднее.</span><span class="sxs-lookup"><span data-stu-id="4fef9-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Рисунок 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="4fef9-136">Добавление заказа на работу в пул заказов на работу</span><span class="sxs-lookup"><span data-stu-id="4fef9-136">Add work order to a work order pool</span></span>

<span data-ttu-id="4fef9-137">Как описано в разделе выше, при создании пула можно добавлять заказы на работу в пул заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="4fef9-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="4fef9-138">Кроме того, заказ на работу можно добавить в пул заказов на работу из одного из списков **Все заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="4fef9-139">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4fef9-140">Выберите заказ на работу в списке и щелкните **Пул заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="4fef9-141">Выберите "Добавить" в поле **Добавить/удалить**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="4fef9-142">Выберите пул заказов на работу в поле **Пул**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="4fef9-143">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-143">Click **OK**.</span></span>

6. <span data-ttu-id="4fef9-144">После добавления заказа на работу в пул заказов на работу, если необходимо поместить заказ на работу в определенную последовательность в пуле: откройте одну из страниц списка пулов заказов на работу, выберите пул и щелкните **Правка**, затем скорректируйте порядок сортировки заказов на работу в пуле в форме **Пул заказов на работу** > экспресс-вкладка **Заказы на работу** > поле **Порядок сортировки**.</span><span class="sxs-lookup"><span data-stu-id="4fef9-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="4fef9-145">Если необходимо удалить выбранный заказ на работу из пула заказов на работу, выберите "Удалить" на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="4fef9-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

