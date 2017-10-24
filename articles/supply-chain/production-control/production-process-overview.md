---
title: "Обзор производственного процесса"
description: "Эта статья содержит обзор производственных процессов. В ней описываются различные этапы производственных заказов, заказов партии и канбанов, начиная с создания заказа до закрытия финансового периода."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdStatusListPage, JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e50e64057d19d0e1fbf5645c2abc31fbd19ea43a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="production-process-overview"></a><span data-ttu-id="b2251-104">Обзор производственного процесса</span><span class="sxs-lookup"><span data-stu-id="b2251-104">Production process overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b2251-105">Эта статья содержит обзор производственных процессов.</span><span class="sxs-lookup"><span data-stu-id="b2251-105">This article gives an overview of the production processes.</span></span> <span data-ttu-id="b2251-106">В ней описываются различные этапы производственных заказов, заказов партии и канбанов, начиная с создания заказа до закрытия финансового периода.</span><span class="sxs-lookup"><span data-stu-id="b2251-106">It describes the various stages of production orders, batch orders, and kanbans, from order creation to closing of the financial period.</span></span> 

<span data-ttu-id="b2251-107">Производство продуктов — это процесс, который также называют жизненным циклом производства, включает в себя определенные шаги, которые требуются для изготовления номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b2251-107">The production of products, a process that is also known as the production life cycle, follows specific steps that are required to complete the manufacture of an item.</span></span> <span data-ttu-id="b2251-108">Жизненный цикл начинается с создания производственного заказа, заказа партии или канбана.</span><span class="sxs-lookup"><span data-stu-id="b2251-108">The life cycle begins with the creation of the production order, batch order, or kanban.</span></span> <span data-ttu-id="b2251-109">Он заканчивается принятой произведенной продукцией, готовой для поставки клиенту или для передачи на другой этап производства.</span><span class="sxs-lookup"><span data-stu-id="b2251-109">It ends with a finished, manufactured item that is ready for either a customer or another phase of production.</span></span> <span data-ttu-id="b2251-110">На каждом шаге жизненного цикла для выполнения процесса требуется информация различного типа.</span><span class="sxs-lookup"><span data-stu-id="b2251-110">Each step in the life cycle requires different kinds of information to complete the process.</span></span> <span data-ttu-id="b2251-111">Завершение каждого шага отражается в производственном заказе, заказе партии или канбане путем изменения его статуса производства.</span><span class="sxs-lookup"><span data-stu-id="b2251-111">As each step is completed, the production order, batch order, or kanban shows a change in the production status.</span></span> <span data-ttu-id="b2251-112">Разные виды продуктов требуют различных процессов производства.</span><span class="sxs-lookup"><span data-stu-id="b2251-112">Different types of products require different manufacturing processes.</span></span>  

<span data-ttu-id="b2251-113">Модуль **Управление производством** связан с другими модулями, такими как **Управление сведениями о продукте**, **Управление запасами**, **Главная книга**, **Управление складом**, **Отчетность проектов** и **Управление организацией**.</span><span class="sxs-lookup"><span data-stu-id="b2251-113">The **Production control** module is linked to other modules, such as **Product information management**, **Inventory management**, **General ledger**, **Warehouse management**, **Project accounting**, and **Organization administration**.</span></span> <span data-ttu-id="b2251-114">Такая интеграция требуется для создания информационного потока, необходимого для производства готовой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b2251-114">This integration supports the information flow that is required to complete the manufacturing of a finished item.</span></span>  

<span data-ttu-id="b2251-115">На производственный процесс обычно влияют методы учета затрат и оценки запасов, которые выбраны для конкретного производственного процесса.</span><span class="sxs-lookup"><span data-stu-id="b2251-115">The production process is typically influenced by the cost accounting and inventory valuation methods that are chosen for a specific production process.</span></span> <span data-ttu-id="b2251-116">Finance and Operations поддерживает как методы фактических затрат (раньше пришел, раньше ушел \[FIFO\]; последний пришел, первый вышел \[LIFO\]; скользящее среднее; и периодический средневзвешенный показатель), так и методы нормативных затрат.</span><span class="sxs-lookup"><span data-stu-id="b2251-116">Finance and Operations supports both actual cost (first in, first out \[FIFO\]; last in, first out \[LIFO\]; moving average; and periodic weighted average) and standard cost methods.</span></span> <span data-ttu-id="b2251-117">Бережливое производство реализуется на основе принципа backflush-расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="b2251-117">Lean manufacturing is implemented based on the backflush costing principle.</span></span>  

<span data-ttu-id="b2251-118">Выбор методов измерения затрат также определяет требования для отчетности о потреблении материалов и ресурсов во время производственного процесса.</span><span class="sxs-lookup"><span data-stu-id="b2251-118">The choice of the cost measurement methods also defines the requirements for reporting about material and resource consumption during the production process.</span></span> <span data-ttu-id="b2251-119">Обычно методы фактических затрат требуют точной отчетности на уровне заданий, тогда как периодические методы оценки допускают менее подробную отчетность о потреблении материалов и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2251-119">Typically, actual cost methods require accurate reporting on the job level, whereas periodic costing methods allow for less granular reporting of material and resource consumption.</span></span>

## <a name="mixed-mode-manufacturing"></a><span data-ttu-id="b2251-120">Смешанный режим производства</span><span class="sxs-lookup"><span data-stu-id="b2251-120">Mixed mode manufacturing</span></span>
<span data-ttu-id="b2251-121">Различные продукты и топологии производства требуют применения различных типов заказа.</span><span class="sxs-lookup"><span data-stu-id="b2251-121">Different products and production topologies require the application of different order types.</span></span> <span data-ttu-id="b2251-122">Finance and Operations может применять различные типы заказа в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="b2251-122">Finance and Operations can apply the various order types in a mixed mode.</span></span> <span data-ttu-id="b2251-123">Другими словами, все типы заказов могут использоваться во время сквозного процесса производства одного готового продукта.</span><span class="sxs-lookup"><span data-stu-id="b2251-123">In other words, all order types can occur during the end-to-end process of producing one finished product.</span></span>

-   <span data-ttu-id="b2251-124">**Производственный заказ** — это классический тип заказа для производства определенного продукта или варианта продукта в определенном количестве к конкретной дате.</span><span class="sxs-lookup"><span data-stu-id="b2251-124">**Production order** – This is the classic order type to produce a specific product or product variant in a given quantity on a specific date.</span></span> <span data-ttu-id="b2251-125">Производственные заказы основаны на спецификациях и маршрутах.</span><span class="sxs-lookup"><span data-stu-id="b2251-125">Production orders are based on bills of materials (BOMs) and routes.</span></span>
-   <span data-ttu-id="b2251-126">**Заказ партии** — этот тип заказа используется в перерабатывающих отраслях и дискретных процессах, где преобразование производства основано на формуле, или где сопутствующие и побочные продукты могут быть конечными продуктами, как в дополнение, так и вместо главного продукта.</span><span class="sxs-lookup"><span data-stu-id="b2251-126">**Batch order** – This order type is used for process industries and discrete processes where the manufacturing conversion is based on a formula, or where co-products and by-products can be end products, either in addition to or instead of the main product.</span></span> <span data-ttu-id="b2251-127">В заказах партии используются спецификации и маршруты типа **Формула**.</span><span class="sxs-lookup"><span data-stu-id="b2251-127">Batch orders use **Formula** type BOMs and routes.</span></span>
-   <span data-ttu-id="b2251-128">**Канбан** — канбаны используются для сигнализации повторяющихся бережливых процессов производства, которые основаны на производственных потоках, правилах канбан и спецификациях.</span><span class="sxs-lookup"><span data-stu-id="b2251-128">**Kanban** – Kanbans are used to signal repetitive lean manufacturing processes that are based on production flows, kanban rules, and BOMs.</span></span>
-   <span data-ttu-id="b2251-129">**Проект** — проект производства совмещает продукты и услуги с определенным графиком и бюджетом.</span><span class="sxs-lookup"><span data-stu-id="b2251-129">**Project** – A manufacturing project combines products and services with a given schedule and budget.</span></span> <span data-ttu-id="b2251-130">Производственная часть проекта можно осуществляться через любое другие типы заказа.</span><span class="sxs-lookup"><span data-stu-id="b2251-130">The manufacturing part of a project can be delivered through any of the other order types.</span></span>

## <a name="manufacturing-principles"></a><span data-ttu-id="b2251-131">Принципы производства</span><span class="sxs-lookup"><span data-stu-id="b2251-131">Manufacturing principles</span></span>
<span data-ttu-id="b2251-132">Для того, чтобы выбрать принцип производства, который лучше всего подходит к определенному продукту и связанному рынку, вы должны рассматривать требования производства и снабжения, а также ожидания клиента о времени выполнения поставки.</span><span class="sxs-lookup"><span data-stu-id="b2251-132">To select the manufacturing principle that best applies to a particular product and related market, you must consider the requirements of production and logistics, and also customer expectations about delivery lead times.</span></span>

-   <span data-ttu-id="b2251-133">**Изготовление на склад** — это классический принцип производства, где продукты производятся для склада на основе прогноза или пополнения минимального запаса (последний обычно рассчитывается на основе прогноза или исторического потребления).</span><span class="sxs-lookup"><span data-stu-id="b2251-133">**Make to stock** – This is the classic manufacturing principle, where products are produced for stock, based on forecast or minimum stock refill (the latter is typically calculated based on forecast or historic consumption).</span></span>
-   <span data-ttu-id="b2251-134">**Изготовление на заказ** — стандартные продукты изготавливаются на заказ или их изготовление завершается на заказ.</span><span class="sxs-lookup"><span data-stu-id="b2251-134">**Make to order** – Standard products are made to order or finished to order.</span></span> <span data-ttu-id="b2251-135">Хотя возможно подготовительное производство с использованием принципа "Изготовление на склад", затратные этапы создания стоимости или этапы, создающие варианты, запускаются заказом на продажу или заказом на перемещение.</span><span class="sxs-lookup"><span data-stu-id="b2251-135">Although pre-production might be done by using the Make to stock principle, expensive steps of the value chain, or steps that create variants, are triggered by a sales order or transfer order.</span></span>
-   <span data-ttu-id="b2251-136">**Конфигурирование на заказ** — как и в случае принципа "Изготовление на заказ", конечные операции цепочки создания стоимости выполняются на заказ.</span><span class="sxs-lookup"><span data-stu-id="b2251-136">**Configure to order** – As for the Make to order principle, the final operations of the value chain are made to order.</span></span> <span data-ttu-id="b2251-137">Фактический вариант произведенного продукта не определен заранее, а создается во время ввода заказа на основе модели конфигурации продаваемого продукта.</span><span class="sxs-lookup"><span data-stu-id="b2251-137">The actual product variant that is produced isn't predefined but is created at the time of order entry, based on the configuration model of the sales product.</span></span> <span data-ttu-id="b2251-138">Принцип "Конфигурирование на заказ" требует некоторого уровня унификации процесса для определенной линейки продуктов.</span><span class="sxs-lookup"><span data-stu-id="b2251-138">The Configure to order principle requires a certain level of process unification for a given product line.</span></span>
-   <span data-ttu-id="b2251-139">**Разработка на заказ** — процессы разработки на заказ обычно реализуются в рамках проекта и начинаются с этапа инженерной разработки.</span><span class="sxs-lookup"><span data-stu-id="b2251-139">**Engineer to order** – Engineer to order processes are typically adressed by a project and usually start with the engineering phase.</span></span> <span data-ttu-id="b2251-140">Во время этапа инженерной разработки конструируются и описываются фактические продукты, которые необходимы для выполнения заказа.</span><span class="sxs-lookup"><span data-stu-id="b2251-140">During the engineering phase, the actual products that are required fulfill the order are designed and described.</span></span> <span data-ttu-id="b2251-141">Производственные заказы, заказы партии или канбаны после этого могут создаваться для того, чтобы произвести продукты.</span><span class="sxs-lookup"><span data-stu-id="b2251-141">Production orders, batch orders, or kanbans can then be created to produce the products.</span></span>

## <a name="overview-of-the-production-life-cycle"></a><span data-ttu-id="b2251-142">Обзор жизненного цикла производства</span><span class="sxs-lookup"><span data-stu-id="b2251-142">Overview of the production life cycle</span></span>
<span data-ttu-id="b2251-143">Следующие шаги в жизненный цикл производства могут возникать для всех типов заказа смешанного режима производства.</span><span class="sxs-lookup"><span data-stu-id="b2251-143">The following steps in the production life cycle can occur for all order types of mixed mode manufacturing.</span></span> <span data-ttu-id="b2251-144">Однако не все из них представлены как явный статус заказа.</span><span class="sxs-lookup"><span data-stu-id="b2251-144">However, not all of them are represented as an explicit order status.</span></span>

1.  <span data-ttu-id="b2251-145">**Создано** — вы можете создать производственный заказ, заказ партии или канбан вручную, или вы можете настроить систему для их создания на основе различных сигналов о спросе.</span><span class="sxs-lookup"><span data-stu-id="b2251-145">**Created** – You can create a production order, batch order, or kanban manually, or you can configure the system to generate them based on various demand signals.</span></span> <span data-ttu-id="b2251-146">Сводное планирование создает производственные заказы, заказы партии или канбаны путем утверждения спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="b2251-146">Master planning creates production orders, batch orders, or kanbans by firming planned orders.</span></span> <span data-ttu-id="b2251-147">К другим сигналам о спросе относятся заказы на продажу или фиксированные сигналы о поставках от других производственных заказов или канбанов.</span><span class="sxs-lookup"><span data-stu-id="b2251-147">Other demand signals are sales orders or pegged supply signals from other production orders or kanbans.</span></span> <span data-ttu-id="b2251-148">Для канбанов с фиксированным количеством сигналы спроса создаются, когда канбаны зарегистрированы как пустые.</span><span class="sxs-lookup"><span data-stu-id="b2251-148">For fixed-quantity kanbans, demand signals are generated when kanbans are registered as empty.</span></span>
2.  <span data-ttu-id="b2251-149">**Оценено** — вы можете рассчитывать оценки потребления материала и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2251-149">**Estimated** – You can calculate estimates for material and resource consumption.</span></span> <span data-ttu-id="b2251-150">Оценка создает проводки запасов с сырьем, которые имеют статус **Заказано**.</span><span class="sxs-lookup"><span data-stu-id="b2251-150">The estimation generates inventory transactions for raw materials that have a status of **On order**.</span></span> <span data-ttu-id="b2251-151">Поступления для главных продуктов, сопутствующих продуктов и побочных продуктов создаются при оценке производственных заказов или заказов партий.</span><span class="sxs-lookup"><span data-stu-id="b2251-151">The receipts for main products, co-products, and by-products are generate when production orders or batch orders are estimated.</span></span> <span data-ttu-id="b2251-152">Если спецификация содержит строки типа **Фиксированное снабжение**, создаются заказы на покупку материалов или создаются субподрядные операционные услуги, которые прикрепляются к производственному заказу или заказу партии.</span><span class="sxs-lookup"><span data-stu-id="b2251-152">If the BOM contains lines of the **Pegged supply** type, purchase orders for materials or subcontracted operation services are generated and pegged to the production order or batch order.</span></span> <span data-ttu-id="b2251-153">Номенклатуры или заказы, зарезервированные согласно стратегии резервирования производственного заказа, и цена готовых изделий вычисляются на основе настроек параметров.</span><span class="sxs-lookup"><span data-stu-id="b2251-153">Items or orders are reserved according to the reservation strategy of the production order, and the price of the finished goods is calculated based on parameter settings.</span></span>
3.  <span data-ttu-id="b2251-154">**Запланировано** — можно планировать производство на основе операций, отдельных заданий или на основе обоих этих параметров.</span><span class="sxs-lookup"><span data-stu-id="b2251-154">**Scheduled** – You can schedule production based on operations, individual jobs, or both.</span></span>
    -   <span data-ttu-id="b2251-155">**Планирование операций** — этот метод планирования позволяет получить приблизительный долгосрочный план.</span><span class="sxs-lookup"><span data-stu-id="b2251-155">**Operations scheduling** – This scheduling method provides a rough, long-term plan.</span></span> <span data-ttu-id="b2251-156">С помощью этого метода вы можете назначать даты начала и окончания производственным заказам.</span><span class="sxs-lookup"><span data-stu-id="b2251-156">By using this method, you can assign start and end dates to production orders.</span></span> <span data-ttu-id="b2251-157">Если производственные заказы назначены операциям маршрута, вы можете назначать их группам центров затрат.</span><span class="sxs-lookup"><span data-stu-id="b2251-157">If the production orders are attached to route operations, you can assign them to cost center groups.</span></span>
    -   <span data-ttu-id="b2251-158">**Планирование заданий** — этот метод планирования позволяет получить детальный план.</span><span class="sxs-lookup"><span data-stu-id="b2251-158">**Job scheduling** – This scheduling method provides a detailed plan.</span></span> <span data-ttu-id="b2251-159">Каждая операция разбивается на отдельные задания с определенными датами, временем и назначенными операционными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="b2251-159">Each operation is broken down into individual jobs that have specific dates, times, and assigned operations resources.</span></span> <span data-ttu-id="b2251-160">Если используется конечная мощность, задания назначаются операционным ресурсам с учетом их доступности.</span><span class="sxs-lookup"><span data-stu-id="b2251-160">If finite capacity is used, jobs are assigned to operations resources based on availability.</span></span> <span data-ttu-id="b2251-161">Вы можете просматривать и изменять план на диаграмме Ганта.</span><span class="sxs-lookup"><span data-stu-id="b2251-161">You can view and change the schedule in a Gantt chart.</span></span>
    -   <span data-ttu-id="b2251-162">**График канбана** — задания канбана планируются на доске графика канбана или автоматически на основе автоматической конфигурации планирования правил канбан.</span><span class="sxs-lookup"><span data-stu-id="b2251-162">**Kanban schedule** – Kanban jobs are scheduled on the kanban schedule board or automatically scheduled based on the automatic planning configuration of the kanban rules.</span></span>

4.  <span data-ttu-id="b2251-163">**Выпущено** — вы можете выпустить производственный заказ или заказ партии, когда график закончен и материалы доступны для подборки или подготовки.</span><span class="sxs-lookup"><span data-stu-id="b2251-163">**Released** – You can release the production order or batch order when the schedule is finished and the material is available to be picked or prepared.</span></span> <span data-ttu-id="b2251-164">Проверка наличия материалов помогает заведующему цехом определить наличие материалов для производственных заказов или заказов партий.</span><span class="sxs-lookup"><span data-stu-id="b2251-164">The material availability check helps the shop floor supervisor assess the availabilty of material for the production orders or batch orders.</span></span> <span data-ttu-id="b2251-165">Вы также можете печатать документы производственного заказа, такие как листы комплектации, карта задания, карта маршрута и маршрутное задание.</span><span class="sxs-lookup"><span data-stu-id="b2251-165">You can also print the production order documents, such as the pick lists, job card, route card, and route job.</span></span> <span data-ttu-id="b2251-166">Когда производственный заказ выпускается, статус заказа изменяется для указания того, что можно начинать производство.</span><span class="sxs-lookup"><span data-stu-id="b2251-166">When the production order is released, the status of the order changes to indicate that the production can begin.</span></span> <span data-ttu-id="b2251-167">Когда используется управление складом, выпуск производственного заказа или заказа партии выпускает строки производственной спецификации для модуля управления складом.</span><span class="sxs-lookup"><span data-stu-id="b2251-167">When warehouse management is used, release of the production order or batch order releases the production BOM lines to warehouse management.</span></span> <span data-ttu-id="b2251-168">Волны склада и работа склада после этого создаются согласно настройке склада.</span><span class="sxs-lookup"><span data-stu-id="b2251-168">Warehouse waves and warehouse work are then generated according to the setup of the warehouse.</span></span>
5.  <span data-ttu-id="b2251-169">**Подготовлено**/**Скомплектовано** — когда все материалы и ресурсы перемещены в производственное местонахождение, строки производственной спецификации или строки канбан обновляются до статуса **Скомплектовано**.</span><span class="sxs-lookup"><span data-stu-id="b2251-169">**Prepared**/**Picked** – When all materials and resources have been staged at the production location, the production BOM lines or kanban lines are updated to a status of **Picked**.</span></span> <span data-ttu-id="b2251-170">Фиксированные заказы поставки и связанная работа склада обычно выполняются на данном этапе.</span><span class="sxs-lookup"><span data-stu-id="b2251-170">Pegged supply orders and related warehouse work are typically completed at this stage.</span></span> <span data-ttu-id="b2251-171">Карточки канбан или карточки задания, которые необходимы для сообщения о ходе производства, должны быть назначены и напечатаны.</span><span class="sxs-lookup"><span data-stu-id="b2251-171">The kanban cards or job cards that are required to report production progress should be assigned and printed.</span></span>
6.  <span data-ttu-id="b2251-172">**Начато** — когда производственный заказ, заказ партии или канбан запущен, вы можете сообщить о потреблении материалов и ресурсов по заказу.</span><span class="sxs-lookup"><span data-stu-id="b2251-172">**Started** – When a production order, batch order, or kanban is started, you can report material and resource consumption against the order.</span></span> <span data-ttu-id="b2251-173">Систему можно настроить для автоматической разности потребления материалов и ресурсов, выделенных заказу при его запуске.</span><span class="sxs-lookup"><span data-stu-id="b2251-173">The system can be configured to automatically post the material and resource consumption that are allocated to the order when the order is started.</span></span> <span data-ttu-id="b2251-174">Такое выделение называется "упреждающее списание", "опережающее списание" или "автопотребление".</span><span class="sxs-lookup"><span data-stu-id="b2251-174">This allocation is known as preflushing, forward flushing, or autoconsumption.</span></span> <span data-ttu-id="b2251-175">Вы можете вручную выделять материалы для производственных заказов или заказов партии, создавая дополнительные журналы списка комплектации.</span><span class="sxs-lookup"><span data-stu-id="b2251-175">You can manually allocate materials to production orders or batch orders by creating additional picking list journals.</span></span> <span data-ttu-id="b2251-176">Также вы можете вручную распределить затраты на оплату труда и другие затраты маршрута для заказа.</span><span class="sxs-lookup"><span data-stu-id="b2251-176">You can also manually allocate labor and other route costs to the order.</span></span> <span data-ttu-id="b2251-177">Если вы используете планирование операций, вы можете распределить эти затраты, создав журнал карт маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b2251-177">If you're using operations scheduling, you can allocate these costs by creating a route card journal.</span></span> <span data-ttu-id="b2251-178">Если вы используете планирование заданий, вы можете распределить эти затраты, создав журнал карт заданий.</span><span class="sxs-lookup"><span data-stu-id="b2251-178">If you're using job scheduling, you can allocate the costs by creating a job card journal.</span></span> <span data-ttu-id="b2251-179">Производственные заказы или заказы партий можно запускать партиями запрошенного окончательного количества.</span><span class="sxs-lookup"><span data-stu-id="b2251-179">Production orders or batch orders can be started in batches of the requested final quantity.</span></span> <span data-ttu-id="b2251-180">В производственном заказе, заказе партии или канбане созданные задания можно начинать и подавать отчеты о них отдельно через журналы, терминал исполнения производства (терминал MES) или доски канбан.</span><span class="sxs-lookup"><span data-stu-id="b2251-180">Within a production order, batch order, or kanban, the jobs that are created can be started and reported separately through journals, the manufacturing execution terminal (MES Terminal), or the kanban boards.</span></span>
7.  <span data-ttu-id="b2251-181">Сообщение о ходе выполнения/**выполненные** задания — используйте терминал MES, журналы производства, доски канбан или мобильные сканеры для того, чтобы сообщать о ходе производства по заданиям или ресурсам.</span><span class="sxs-lookup"><span data-stu-id="b2251-181">Report progress/**Complete** jobs – Use the MES Terminal, production journals, kanban boards, or mobile scanning capabilities to report the production progress by job or resource.</span></span> <span data-ttu-id="b2251-182">Потребление материалов и ресурсов будет разнесено, а состояние связанных канбанов, производственных заказов и заказов партий может быть обновлено на **Получено** или **Принято**.</span><span class="sxs-lookup"><span data-stu-id="b2251-182">Material and resource consumption will be posted, and the status of the related kanbans, production orders, and batch orders might be updated to **Received** or **Reported as finished**.</span></span> <span data-ttu-id="b2251-183">Может быть создана работа "отложить" для склада, в зависимости от конфигурации склада.</span><span class="sxs-lookup"><span data-stu-id="b2251-183">Put-away work for the warehouse might be created, depending on the warehouse configuration.</span></span>
8.  <span data-ttu-id="b2251-184">**Принято** (поступление продуктов) — когда производственный заказ или заказ партии принят, количество готовых товаров, которые были завершены, обновляется в запасах.</span><span class="sxs-lookup"><span data-stu-id="b2251-184">**Reported as finished** (the product receipt) – When a production order or batch order is reported as finished, the quantity of the finished goods that were completed is updated in inventory.</span></span> <span data-ttu-id="b2251-185">Это количество включает количество соответствующих сопутствующих и побочных продуктов.</span><span class="sxs-lookup"><span data-stu-id="b2251-185">This quantity includes the quantity of relevant co-products and by-products.</span></span> <span data-ttu-id="b2251-186">Если вы используете учет незавершенного производства (НЗП), в журнале ГК уменьшается количество на счетах НЗП и увеличиваются запасы готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="b2251-186">If you're using work-in-process (WIP) accounting, a ledger journal is generated to reduce the WIP accounts and increase the inventory of the finished goods.</span></span> <span data-ttu-id="b2251-187">При расчете стоимости производственного заказа разносятся фактические затраты на производство.</span><span class="sxs-lookup"><span data-stu-id="b2251-187">When the cost of a production order is calculated, the actual cost of the production is posted.</span></span> <span data-ttu-id="b2251-188">Затраты на материал и оплату труда, связанные с производством, еще не выделены в журнале или путем упреждающего списания. Их можно автоматически выделить методом backflush.</span><span class="sxs-lookup"><span data-stu-id="b2251-188">If the material and labor costs that are associated with a production aren't already allocated in a journal or by preflushing, they can be automatically allocated through back-flushing.</span></span> <span data-ttu-id="b2251-189">Выделение через обратный учет требует обратного удержания для процессов складских проводок.</span><span class="sxs-lookup"><span data-stu-id="b2251-189">Allocation through back-flushing involves the post-deducting of inventory transaction processes.</span></span> <span data-ttu-id="b2251-190">Если производственный заказ выполнен, установите флажок **Заключительное задание**, чтобы изменить статус недопоставленного на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="b2251-190">If the production order is completed, select the **End job** check box to change the remaining status to **Ended**.</span></span> <span data-ttu-id="b2251-191">В противном случае оставьте поле пустым, чтобы сделать возможным информирование о дополнительных произведенных количествах.</span><span class="sxs-lookup"><span data-stu-id="b2251-191">Otherwise, leave the field empty to enable reporting of additional quantities that are produced.</span></span>
9.  <span data-ttu-id="b2251-192">**Оценка качества** — получение продукта может запускать создание заказов для контроля качества, в зависимости от конфигурации процессов испытания и правил качества, которые установлены для специфических продуктов.</span><span class="sxs-lookup"><span data-stu-id="b2251-192">**Quality assessment** – A product receipt can trigger the creation of quality orders, depending on the configuration of test processes and the quality rules that are established for specific products.</span></span> <span data-ttu-id="b2251-193">Так как заказ для контроля качества может обновить статус запасов или атрибуты партии испытанных продуктов, оценка качества являются необходимым процессом во много отраслях.</span><span class="sxs-lookup"><span data-stu-id="b2251-193">Because a quality order can update the inventory status or the batch attributes of the tested products, quality assessment is a mandatory process in many industries.</span></span>
10. <span data-ttu-id="b2251-194">**Разместить** и **Отгрузить по заказу** — после получения продукта и оценки качества необязательная работа "разместить" направляет полученные продукты к следующему пункту потребления, на склад готовых товаров или в зону отгрузки, если имеются требования отгрузки по заказу.</span><span class="sxs-lookup"><span data-stu-id="b2251-194">**Put away** and **Ship to order** – After product receipt and quality assessment, optional put-away work directs the received products to the next point of consumption, to a finished goods warehouse, or to a shipment zone if there are ship-to-order requirements.</span></span>
11. <span data-ttu-id="b2251-195">**Завершено** — до завершения производства для произведенного количества рассчитываются фактические затраты.</span><span class="sxs-lookup"><span data-stu-id="b2251-195">**Ended** – Before production is ended, actual costs are calculated for the quantity that was produced.</span></span> <span data-ttu-id="b2251-196">Все ожидаемые затраты на материал, оплату труда и накладные расходы реверсируются и заменяются фактическими затратами.</span><span class="sxs-lookup"><span data-stu-id="b2251-196">All estimated costs of material, labor, and overhead are reversed and replaced with actual costs.</span></span> <span data-ttu-id="b2251-197">Если вы установили флажок **Заключительное задание** при выполнении расчета стоимости, статус производственного заказа изменяется на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="b2251-197">If you select the **End job** check box when you run the cost calculation, the production order status changes to **Ended**.</span></span> <span data-ttu-id="b2251-198">Этот статус предотвращает любую разноску дополнительных затрат в завершенном производственном заказе.</span><span class="sxs-lookup"><span data-stu-id="b2251-198">This status prevents any additional costs from being posted to a completed production order.</span></span>
12. <span data-ttu-id="b2251-199">**Закрытие периода** — некоторые принципы калькуляции себестоимости, такие как периодическое среднее, backflush-расчет себестоимости, FIFO или LIFO, требуют периодических действий для закрытия инвентарного или финансового периода.</span><span class="sxs-lookup"><span data-stu-id="b2251-199">**Period closure** – Some cost accounting principles, such as periodic average, back-flush costing, FIFO, or LIFO, require periodic activities to close the inventory or financial period.</span></span> <span data-ttu-id="b2251-200">Обычно система пытается сообщить о всем потреблении материалов и ресурсов, и также коррекциях запасов и утиля перед тем, как периоды будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="b2251-200">Typically, the system tries to report all material and resource consumption, and also corrections of inventory and scrap, before the periods are closed.</span></span> <span data-ttu-id="b2251-201">Эта отчетность обычно выполняется с помощью журналов движения запасов или журналов корректировки.</span><span class="sxs-lookup"><span data-stu-id="b2251-201">This reporting is typically done by using inventory movement journals or adjustment journals.</span></span> <span data-ttu-id="b2251-202">Цель — оценка экономических показателей операционных единиц за период.</span><span class="sxs-lookup"><span data-stu-id="b2251-202">The goal is to assess the economic performance of operating units per period.</span></span> <span data-ttu-id="b2251-203">В некоторых случаях, когда используются длительные производственные заказы, охватывающие несколько периодов финансовой отчетности, используются журналы производства для информирования о ходе производства и потреблении ресурса в конце периода.</span><span class="sxs-lookup"><span data-stu-id="b2251-203">In some cases, when long-running production orders are used that span the financial reporting periods, production journals are used to report the production progress and resource consumption by the end of the period.</span></span>


<a name="see-also"></a><span data-ttu-id="b2251-204">См. также</span><span class="sxs-lookup"><span data-stu-id="b2251-204">See also</span></span>
--------

[<span data-ttu-id="b2251-205">Обратная связь производства</span><span class="sxs-lookup"><span data-stu-id="b2251-205">Production feedback</span></span>](production-feedback.md)

[<span data-ttu-id="b2251-206">Модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="b2251-206">Product configuration models</span></span>](../pim/product-configuration-models.md)

[<span data-ttu-id="b2251-207">Бережливое производство</span><span class="sxs-lookup"><span data-stu-id="b2251-207">Lean manufacturing</span></span>](lean-manufacturing-overview.md)



