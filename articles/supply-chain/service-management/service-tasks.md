---
title: Обзор задач сервисного обслуживания
description: Задачи обслуживания используются для описания задачи, которая должна быть выполнена в ходе заказа на обслуживание. Эта информация будет видна и специалистам, и клиентам.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dfeddcf754ccaf1f5fb5d3f20ca771145c5f2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223322"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="90a87-104">Обзор задач сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="90a87-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90a87-105">Задачи обслуживания используются для описания задачи, которая должна быть выполнена в ходе заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="90a87-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="90a87-106">Эта информация будет видна и специалистам, и клиентам.</span><span class="sxs-lookup"><span data-stu-id="90a87-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="90a87-107">Задачи обслуживания создаются на странице **Задачи обслуживания**; чтобы связать их с конкретным соглашением на обслуживание или заказом на обслуживание, создаются связи задачи обслуживания.</span><span class="sxs-lookup"><span data-stu-id="90a87-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="90a87-108">Каждый раз при создании связи задачи сервисного обслуживания можно создать следующее.</span><span class="sxs-lookup"><span data-stu-id="90a87-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="90a87-109">внутренние примечания для задачи, например подробные технические требования для задачи, которые важно знать специалисту;</span><span class="sxs-lookup"><span data-stu-id="90a87-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="90a87-110">Внешние примечания, которые будут видны клиенту.</span><span class="sxs-lookup"><span data-stu-id="90a87-110">External notes that the customer can see.</span></span> <span data-ttu-id="90a87-111">Они могут содержать более общее описание задачи, выполняемой в соответствии с соглашением о сервисном обслуживании между клиентом и обслуживающей компанией.</span><span class="sxs-lookup"><span data-stu-id="90a87-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="90a87-112">После того как связь задачи сервисного обслуживания между задачей сервисного обслуживания и заказом на сервисное обслуживание или соглашением о сервисном обслуживании будет настроена, эту задачу сервисного обслуживания можно указывать при создании строк текущего заказа на сервисное обслуживание или строк текущего соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="90a87-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="90a87-113">При создании заказов на сервисное обслуживание из соглашения о сервисном обслуживании можно использовать задачи сервисного обслуживания, назначенные каждой строке соглашения о сервисном обслуживании, чтобы группировать строки заказа на сервисное обслуживание в заказы на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="90a87-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="90a87-114">Создание задачи обслуживания</span><span class="sxs-lookup"><span data-stu-id="90a87-114">Create a service task</span></span>

1. <span data-ttu-id="90a87-115">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Задачи обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="90a87-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="90a87-116">Создайте новую строку.</span><span class="sxs-lookup"><span data-stu-id="90a87-116">Create a new line.</span></span>
3. <span data-ttu-id="90a87-117">Введите код и описание сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="90a87-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="90a87-118">Пример</span><span class="sxs-lookup"><span data-stu-id="90a87-118">Example</span></span>

<span data-ttu-id="90a87-119">Специалист должен выполнить два задания по коробке передач (объект обслуживания GB-1234) на предприятии клиента.</span><span class="sxs-lookup"><span data-stu-id="90a87-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="90a87-120">Для клиента было создано соглашение о сервисном обслуживании, и с заданиями были связаны несколько проводок.</span><span class="sxs-lookup"><span data-stu-id="90a87-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="90a87-121">Соглашение о сервисном обслуживании и его строки для этих двух заданий представлены ниже.</span><span class="sxs-lookup"><span data-stu-id="90a87-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="90a87-122">Соглашение о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="90a87-122">Service agreement</span></span>

| <span data-ttu-id="90a87-123">Project</span><span class="sxs-lookup"><span data-stu-id="90a87-123">Project</span></span> | <span data-ttu-id="90a87-124">Соглашение о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="90a87-124">Service agreement</span></span> | <span data-ttu-id="90a87-125">описание</span><span class="sxs-lookup"><span data-stu-id="90a87-125">Description</span></span>                                  | <span data-ttu-id="90a87-126">Групповое</span><span class="sxs-lookup"><span data-stu-id="90a87-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="90a87-127">9012</span><span class="sxs-lookup"><span data-stu-id="90a87-127">9012</span></span>    | <span data-ttu-id="90a87-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="90a87-128">000008\_001</span></span>       | <span data-ttu-id="90a87-129">Осмотр и плановая замена — GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="90a87-130">Вознаграждение</span><span class="sxs-lookup"><span data-stu-id="90a87-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="90a87-131">Строки соглашения на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="90a87-131">Service agreement lines</span></span>

| <span data-ttu-id="90a87-132">описание</span><span class="sxs-lookup"><span data-stu-id="90a87-132">Description</span></span>             | <span data-ttu-id="90a87-133">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="90a87-133">Transaction type</span></span> | <span data-ttu-id="90a87-134">Объект сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="90a87-134">Service object</span></span> | <span data-ttu-id="90a87-135">Задача сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="90a87-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="90a87-136">Осмотр и очистка</span><span class="sxs-lookup"><span data-stu-id="90a87-136">Inspection and cleaning</span></span> | <span data-ttu-id="90a87-137">Часы</span><span class="sxs-lookup"><span data-stu-id="90a87-137">Hour</span></span>             | <span data-ttu-id="90a87-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-138">GB-1234</span></span>        | <span data-ttu-id="90a87-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-139">I/C - GB1234</span></span> |
| <span data-ttu-id="90a87-140">Командировочные расходы</span><span class="sxs-lookup"><span data-stu-id="90a87-140">Travel</span></span>                  | <span data-ttu-id="90a87-141">Expense</span><span class="sxs-lookup"><span data-stu-id="90a87-141">Expense</span></span>          | <span data-ttu-id="90a87-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-142">GB-1234</span></span>        | <span data-ttu-id="90a87-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-143">I/C - GB1234</span></span> |
| <span data-ttu-id="90a87-144">Материалы</span><span class="sxs-lookup"><span data-stu-id="90a87-144">Materials</span></span>               | <span data-ttu-id="90a87-145">Элемент</span><span class="sxs-lookup"><span data-stu-id="90a87-145">Item</span></span>             | <span data-ttu-id="90a87-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-146">GB-1234</span></span>        | <span data-ttu-id="90a87-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-147">I/C - GB1234</span></span> |
| <span data-ttu-id="90a87-148">Плановая замена</span><span class="sxs-lookup"><span data-stu-id="90a87-148">Routine replacement</span></span>     | <span data-ttu-id="90a87-149">Часы</span><span class="sxs-lookup"><span data-stu-id="90a87-149">Hour</span></span>             | <span data-ttu-id="90a87-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-150">GB-1234</span></span>        | <span data-ttu-id="90a87-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-151">RR - GB1234</span></span>  |
| <span data-ttu-id="90a87-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="90a87-152">GR-1</span></span>                    | <span data-ttu-id="90a87-153">Элемент</span><span class="sxs-lookup"><span data-stu-id="90a87-153">Item</span></span>             | <span data-ttu-id="90a87-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-154">GB-1234</span></span>        | <span data-ttu-id="90a87-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-155">RR - GB1234</span></span>  |
| <span data-ttu-id="90a87-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="90a87-156">GR-5</span></span>                    | <span data-ttu-id="90a87-157">Элемент</span><span class="sxs-lookup"><span data-stu-id="90a87-157">Item</span></span>             | <span data-ttu-id="90a87-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-158">GB-1234</span></span>        | <span data-ttu-id="90a87-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-159">RR - GB1234</span></span>  |

<span data-ttu-id="90a87-160">К строкам соглашения на обслуживание для двух заданий присоединены две задачи обслуживания.</span><span class="sxs-lookup"><span data-stu-id="90a87-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="90a87-161">Задачи обслуживания определяют проводки, принадлежащие каждому заданию.</span><span class="sxs-lookup"><span data-stu-id="90a87-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="90a87-162">В первом случае задача сервисного обслуживания I/C - GB1234 определяет все строки соглашения о сервисном обслуживании, относящиеся к осмотру и очистке объекта GB-1234.</span><span class="sxs-lookup"><span data-stu-id="90a87-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="90a87-163">Во втором случае задача сервисного обслуживания RR - GB1234 определяет все строки соглашения о сервисном обслуживании, относящиеся к выполнению задания плановой замены.</span><span class="sxs-lookup"><span data-stu-id="90a87-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="90a87-164">Связи задачи обслуживания, которые соединяют задачи обслуживания с конкретным соглашением, будут следующими.</span><span class="sxs-lookup"><span data-stu-id="90a87-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="90a87-165">Задачи обслуживания</span><span class="sxs-lookup"><span data-stu-id="90a87-165">Service tasks</span></span>

| <span data-ttu-id="90a87-166">Задача обслуживания</span><span class="sxs-lookup"><span data-stu-id="90a87-166">Service task</span></span> | <span data-ttu-id="90a87-167">Описание</span><span class="sxs-lookup"><span data-stu-id="90a87-167">Description</span></span>                             | <span data-ttu-id="90a87-168">Внутреннее примечание</span><span class="sxs-lookup"><span data-stu-id="90a87-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="90a87-169">Внешнее примечание</span><span class="sxs-lookup"><span data-stu-id="90a87-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="90a87-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-170">I/C - GB1234</span></span> | <span data-ttu-id="90a87-171">Осмотр коробки передач GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="90a87-172">Визуальный и инструментальный осмотр и очистка коробки передач GB-1234.</span><span class="sxs-lookup"><span data-stu-id="90a87-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="90a87-173">Плановый осмотр коробки передач</span><span class="sxs-lookup"><span data-stu-id="90a87-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="90a87-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="90a87-174">RR - GB1234</span></span>  | <span data-ttu-id="90a87-175">Плановая замена частей в GB-1234</span><span class="sxs-lookup"><span data-stu-id="90a87-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="90a87-176">Плановая замена при обслуживании компонентов GR-1 и GR-5 (в коробках передач, произведенных до 2002 г. также заменяется компонент GR-2)</span><span class="sxs-lookup"><span data-stu-id="90a87-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="90a87-177">Плановая замена деталей</span><span class="sxs-lookup"><span data-stu-id="90a87-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="90a87-178">Группирование заказов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="90a87-178">Group service orders</span></span>

<span data-ttu-id="90a87-179">При автоматическом создании заказов на сервисное обслуживание задачи сервисного обслуживания можно использовать в качестве критерия группировки.</span><span class="sxs-lookup"><span data-stu-id="90a87-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="90a87-180">Чтобы сгруппировать заказы на сервисное обслуживание по задачам сервисного обслуживания, определите в соглашении о сервисном обслуживании, что заказы на сервисное обслуживание, основанные на соглашении о сервисном обслуживании, должны быть сгруппированы по идентификатору задачи сервисного обслуживания в качестве начального критерия группировки.</span><span class="sxs-lookup"><span data-stu-id="90a87-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="90a87-181">**Группировка по задаче обслуживания**</span><span class="sxs-lookup"><span data-stu-id="90a87-181">**Group by service task**</span></span>

1. <span data-ttu-id="90a87-182">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="90a87-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="90a87-183">На вкладке **Настройка** выберите **По задачам сервисного обслуживания** в поле **Объединение заказов на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="90a87-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]