---
title: "Управление работниками склада"
description: "В этой статье рассматривается использование Dynamics 365 for Finance and Operations для контроля и мониторинга работы, выполняемой сотрудниками на складах."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b91c139987473be65fddf8b05759a5ad6f6c223
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="manage-warehouse-workers"></a><span data-ttu-id="62eea-103">Управление работниками склада</span><span class="sxs-lookup"><span data-stu-id="62eea-103">Manage warehouse workers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="62eea-104">В этой статье рассматривается использование Microsoft Dynamics 365 for Finance and Operations, Enterprise edition для контроля и мониторинга работы, выполняемой сотрудниками на складах.</span><span class="sxs-lookup"><span data-stu-id="62eea-104">This article describes how you can use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to help control and monitor the work that's carried out by employees in your warehouses.</span></span>

<span data-ttu-id="62eea-105">Если вы используете функциональность в модуле "Управление складом", все операции, выполняемые работниками склада, называются *работой*.</span><span class="sxs-lookup"><span data-stu-id="62eea-105">If you're using the functionality in Warehouse management, all warehouse worker operations are referred to as *work*.</span></span> <span data-ttu-id="62eea-106">Работа, такая как комплектация, перемещение и подсчет запасов в наличии регистрируется путем использования мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="62eea-106">Work such as picking, moving, and counting on-hand inventory is recorded by using mobile devices.</span></span> <span data-ttu-id="62eea-107">Прежде чем работник склада сможет выполнять работу, его необходимо связать с работником в модуле "Управление персоналом".</span><span class="sxs-lookup"><span data-stu-id="62eea-107">Before a warehouse worker can perform work, he or she must be associated with a worker in Human resources.</span></span> <span data-ttu-id="62eea-108">С каждой учетной записью **работника** может быть связано несколько пользователей работы склада.</span><span class="sxs-lookup"><span data-stu-id="62eea-108">Each **Worker** account can have multiple warehouse work users associated with it.</span></span> <span data-ttu-id="62eea-109">Эти пользователи работы могут работать на разных складах и иметь разные уровни доступа к различным меню на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="62eea-109">Those work users can work in different warehouses and can have different levels of access to the various mobile device menus.</span></span> <span data-ttu-id="62eea-110">Пользователей работы склада можно рассматривать как несколько разных учетных записей для входа для одного работника.</span><span class="sxs-lookup"><span data-stu-id="62eea-110">You can think of the warehouse work users as multiple logons for the selected worker.</span></span> <span data-ttu-id="62eea-111">У каждого пользователя работы есть склад по умолчанию и конкретные workflow-процессы, представленные пунктами меню, доступными этому пользователю работы.</span><span class="sxs-lookup"><span data-stu-id="62eea-111">Each work user has a default warehouse, and specific workflows are exposed by the menus items that are available to that work user.</span></span> 

<span data-ttu-id="62eea-112">Чтобы создать нового пользователя работы, на странице **Работники** на вкладке **Общее** в разделе **Склады** щелкните **Работник**.</span><span class="sxs-lookup"><span data-stu-id="62eea-112">To create a new work user, on the **Workers** page, on the **General** tab, in the **Warehouses** section, click **Worker**.</span></span> <span data-ttu-id="62eea-113">Вы должны указать код пользователя, имя пользователя, склад по умолчанию и имя меню.</span><span class="sxs-lookup"><span data-stu-id="62eea-113">You must specify a user ID, a user name, a default warehouse, and a menu name.</span></span> <span data-ttu-id="62eea-114">Это меню загружается, когда пользователь входит на портал мобильных устройств склада, и позволяет вам определить, к каким пунктам меню имеет доступ пользователь.</span><span class="sxs-lookup"><span data-stu-id="62eea-114">This menu is loaded when the user signs in to the Warehouse Mobile Device Portal, and lets you define which menu items the user has access to.</span></span> 

<span data-ttu-id="62eea-115">В рамках настройки каждого пользователя работы можно также определить конкретные worklow-процессы.</span><span class="sxs-lookup"><span data-stu-id="62eea-115">As part of the setup for each work user, you can also define specific process workflows.</span></span> <span data-ttu-id="62eea-116">Например, можно использовать поле **Является супервизор по подсчету циклов**, чтобы указать, может пользователь обрабатывать корректировки расхождений подсчета циклов во время операции подсчета или эти корректировки должны сначала быть рассмотрены другим лицом.</span><span class="sxs-lookup"><span data-stu-id="62eea-116">For example, you can use the **Is a cycle count supervisor** field to specify whether the user can process adjustments to cycle counting discrepancies during a counting operation, or whether these adjustments must first be reviewed by another person.</span></span>

## <a name="defining-labor-standards"></a><span data-ttu-id="62eea-117">Определение трудовых стандартов</span><span class="sxs-lookup"><span data-stu-id="62eea-117">Defining labor standards</span></span>
<span data-ttu-id="62eea-118">Страница **Трудовые стандарты** позволяет определить методы расчета, которые система использует для расчета предполагаемого времени, которое должно уходить на выполнение работы того или иного типа.</span><span class="sxs-lookup"><span data-stu-id="62eea-118">The **Labor standards** page lets you define the calculation methods that the system uses to calculate the estimated time that a particular type of work should require.</span></span> <span data-ttu-id="62eea-119">Это определение может быть установлено на общем уровне или на конкретном уровне.</span><span class="sxs-lookup"><span data-stu-id="62eea-119">This definition can be set on a generic level or on a specific level.</span></span> <span data-ttu-id="62eea-120">Например, вы можете определить время, необходимое для обработки комплектации заказа на продажу по весу для конкретного определения единицы измерения при использовании конкретного процесса комплектации.</span><span class="sxs-lookup"><span data-stu-id="62eea-120">For example, you can define the time that should be required in order to process a sales order pick per weight for a specific unit definition when a specific picking process is used.</span></span> <span data-ttu-id="62eea-121">В то же время вы можете записать время, основанное на другом методе расчета, для операции складирования скомплектованных запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="62eea-121">At the same time, you can record the time, based on another calculation method, for the put operation of the on-hand inventory that is picked.</span></span> 

<span data-ttu-id="62eea-122">Чтобы включить определенные вами трудовые стандарты, необходимо выбрать параметр **Разрешить трудовые стандарты** для каждого склада, где будут использовать стандарты труда.</span><span class="sxs-lookup"><span data-stu-id="62eea-122">To enable the labor standards that you've defined, you must select the **Allow labor standards** option for each warehouse where labor standards will be used.</span></span>

## <a name="monitoring-and-controlling-warehouse-work"></a><span data-ttu-id="62eea-123">Мониторинг и контроль работы склада</span><span class="sxs-lookup"><span data-stu-id="62eea-123">Monitoring and controlling warehouse work</span></span>
<span data-ttu-id="62eea-124">Страница **Вся работа** позволяет осуществлять мониторинг и корректировку всей запланированной, выполняющейся и завершенной работы.</span><span class="sxs-lookup"><span data-stu-id="62eea-124">The **All work** page lets you monitor and maintain all work that is planned, in progress, and completed.</span></span> <span data-ttu-id="62eea-125">С этой страницы вы можете обновлять различные процессы, такие как назначение складской работы пользователям и приоритет работы.</span><span class="sxs-lookup"><span data-stu-id="62eea-125">From this page, you can update various processes, such as warehouse work user assignments and work priority.</span></span> <span data-ttu-id="62eea-126">Также можно детализировать сведения, связанные с заголовком работы и строками работы, чтобы получить представление об ожидаемых или завершенных процессах работы.</span><span class="sxs-lookup"><span data-stu-id="62eea-126">You can also drill down into the details that are related to the work header and work lines to gain an understanding of the expected or completed work processes.</span></span> 

<span data-ttu-id="62eea-127">Если вы включили параметр **Стандарты труда**, вы можете видеть рассчитанное предполагаемое время выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="62eea-127">If you enable the **Labor standards** option, you can see the calculated estimated time for the work.</span></span> <span data-ttu-id="62eea-128">После этого, когда работа будет выполнена, для каждой операции работы также будет отображаться фактическое время.</span><span class="sxs-lookup"><span data-stu-id="62eea-128">Then, when the work is processed, the actual time will also be shown for each work operation.</span></span> <span data-ttu-id="62eea-129">Таким образом, вы можете сравнить расчетное (предполагаемое) время с фактическим.</span><span class="sxs-lookup"><span data-stu-id="62eea-129">In this way, you can compare the estimated time calculations to the actual time.</span></span> 

<span data-ttu-id="62eea-130">Кроме того, вы можете использовать расчетное время в правилах для автоматического разбиения работы во время создания работы.</span><span class="sxs-lookup"><span data-stu-id="62eea-130">Additionally, you can use the estimated time in the rules for automatically splitting work during work creation.</span></span> <span data-ttu-id="62eea-131">Так вы можете балансировать нагрузку между работниками, исходя из предполагаемого времени выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="62eea-131">In this way, you can load balance work, based on the expected time to complete the tasks.</span></span> 

<span data-ttu-id="62eea-132">Анализ времени, затраченного на обработку элементов работы, может помочь повысить эффективность работы работников склада.</span><span class="sxs-lookup"><span data-stu-id="62eea-132">Analysis of the time that is used to process work items can help drive improvements in the warehouse workers’ efficiency.</span></span> <span data-ttu-id="62eea-133">Для такого анализа предусмотрены следующие отчеты:</span><span class="sxs-lookup"><span data-stu-id="62eea-133">The following reports are available to help with this analysis:</span></span>

-   <span data-ttu-id="62eea-134">**Труд по пользователям** — этот отчет показывает производительность работника, исходя из сравнения фактического времени с предполагаемым.</span><span class="sxs-lookup"><span data-stu-id="62eea-134">**Labor by user** – This report shows worker productivity, based on actual times against expected times.</span></span>
-   <span data-ttu-id="62eea-135">**Труд по типу проводки работы** — вы можете использовать этот отчет для изучения неэффективных моментов в в конкретных складских процессах.</span><span class="sxs-lookup"><span data-stu-id="62eea-135">**Labor by work transaction type** – You can use this report to investigate inefficiencies in specific warehouse processes.</span></span> <span data-ttu-id="62eea-136">Предположим, вы заметили, что комплектация для заказов на перемещение на этой неделе занимает больше времени, чем на предыдущих неделях.</span><span class="sxs-lookup"><span data-stu-id="62eea-136">For example, you notice that picks for transfer orders are taking longer this week than in previous weeks.</span></span> <span data-ttu-id="62eea-137">Эту информацию можно использовать для дальнейшего изучения проблемы.</span><span class="sxs-lookup"><span data-stu-id="62eea-137">You can then use this information for further investigation.</span></span>




