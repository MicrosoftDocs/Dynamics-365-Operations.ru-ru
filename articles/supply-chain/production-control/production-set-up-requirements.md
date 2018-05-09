---
title: "Требования к настройке производства"
description: "Эта статья содержит информацию о требованиях по настройке перед началом работы с производственным контролем."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ade7e55e0568acd7eff3ceead29c3c6d0ca2da1e
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="production-setup-requirements"></a><span data-ttu-id="34fea-103">Требования к настройке производства</span><span class="sxs-lookup"><span data-stu-id="34fea-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34fea-104">Эта статья содержит информацию о требованиях по настройке перед началом работы с производственным контролем.</span><span class="sxs-lookup"><span data-stu-id="34fea-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="34fea-105">Управление производством интегрировано с функциями в других модулях.</span><span class="sxs-lookup"><span data-stu-id="34fea-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="34fea-106">Это взаимодействие позволяет менять производственные заказы и обеспечивать автоматическое их обновление во всех связанных процессах и расчетах в системе.</span><span class="sxs-lookup"><span data-stu-id="34fea-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="34fea-107">Следующие процессы указаны в том в порядке, в каком их следует выполнять.</span><span class="sxs-lookup"><span data-stu-id="34fea-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="34fea-108">Необходимая базовая настройка в других модулях</span><span class="sxs-lookup"><span data-stu-id="34fea-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="34fea-109">Перед началом работы с управлением производством необходимо настроить данные в других модулях.</span><span class="sxs-lookup"><span data-stu-id="34fea-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="34fea-110">Процедура настройки включает в себя следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="34fea-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="34fea-111">Задание общей информации о компании.</span><span class="sxs-lookup"><span data-stu-id="34fea-111">Set up general company information.</span></span>
-   <span data-ttu-id="34fea-112">Настройка Главной книги.</span><span class="sxs-lookup"><span data-stu-id="34fea-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="34fea-113">Определение групп номенклатур.</span><span class="sxs-lookup"><span data-stu-id="34fea-113">Define item groups.</span></span>
-   <span data-ttu-id="34fea-114">Настройка счетов ГК для групп номенклатур.</span><span class="sxs-lookup"><span data-stu-id="34fea-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="34fea-115">Настройка таблицы складируемых номенклатур в управлении запасами.</span><span class="sxs-lookup"><span data-stu-id="34fea-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="34fea-116">Создание спецификаций и их версий в управлении запасами.</span><span class="sxs-lookup"><span data-stu-id="34fea-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="34fea-117">Требуется настройка календаря и ресурсов</span><span class="sxs-lookup"><span data-stu-id="34fea-117">Required calendar and resource setup</span></span>
<span data-ttu-id="34fea-118">Перед началом использования управления производством откройте управление организацией, создайте и определите календарь и операционные ресурсы в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="34fea-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="34fea-119">**Шаблоны расписания** — настройка шаблонов рабочего времени для определения времени, доступного для производственного планирования.</span><span class="sxs-lookup"><span data-stu-id="34fea-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="34fea-120">**Календари** — настройка календарей рабочего времени для определения того, какие дни в году доступны для производственного планирования.</span><span class="sxs-lookup"><span data-stu-id="34fea-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="34fea-121">**Группы ресурсов** — настройка групп ресурсов для группировки операционных ресурсов и получения обзора свободой мощности при планировании.</span><span class="sxs-lookup"><span data-stu-id="34fea-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="34fea-122">Не требуется настраивать группы ресурсов перед настройкой операционных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34fea-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="34fea-123">Однако мы рекомендуем понять, как группировать ресурсы при настройке управления производством.</span><span class="sxs-lookup"><span data-stu-id="34fea-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="34fea-124">**Ресурсы** — настройка операционных ресурсов для определения различных ресурсов, используемых для выполнения производственного процесса и для планирования мощностей.</span><span class="sxs-lookup"><span data-stu-id="34fea-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="34fea-125">Требуется настройка параметров производства</span><span class="sxs-lookup"><span data-stu-id="34fea-125">Required production parameters setup</span></span>
<span data-ttu-id="34fea-126">**Параметры управления производством** — настройка базовых параметров производства для определения того, как система обрабатывает производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="34fea-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="34fea-127">Определите, как производственные заказы создаются, оцениваются, планируются и используются.</span><span class="sxs-lookup"><span data-stu-id="34fea-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="34fea-128">Вы также можете выбрать тип обратной связи и способ учета затрат.</span><span class="sxs-lookup"><span data-stu-id="34fea-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="34fea-129">Требуется идентификация имени журнала</span><span class="sxs-lookup"><span data-stu-id="34fea-129">Required journal name identification</span></span>
<span data-ttu-id="34fea-130">**Наименования производственных журналов** — определите наименования производственных журналов, которые используются для записи и разноски проводок.</span><span class="sxs-lookup"><span data-stu-id="34fea-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="34fea-131">Настройте, если используются операции</span><span class="sxs-lookup"><span data-stu-id="34fea-131">Setup if you use operations</span></span>
<span data-ttu-id="34fea-132">Операции представляют собой специальные действия, направленные на производство готового продукта.</span><span class="sxs-lookup"><span data-stu-id="34fea-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="34fea-133">**Примечание.** Вы должны знать типы операций, которые необходимы для производства номенклатуры, а также порядок и приоритеты таких операций.</span><span class="sxs-lookup"><span data-stu-id="34fea-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="34fea-134">Вы также должны знать, какие ресурсы используются, и сколько.</span><span class="sxs-lookup"><span data-stu-id="34fea-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="34fea-135">**Операции** — настройка операций для представления задач, которые необходимо завершить для производства готовой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="34fea-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="34fea-136">**Отношения** — настройка связей операции для определения подробных свойств.</span><span class="sxs-lookup"><span data-stu-id="34fea-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="34fea-137">Чтобы определить отношения операции, щелкните **Отношения** на странице **Операции**.</span><span class="sxs-lookup"><span data-stu-id="34fea-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="34fea-138">Настройте, если используются маршруты</span><span class="sxs-lookup"><span data-stu-id="34fea-138">Setup if you use routes</span></span>
<span data-ttu-id="34fea-139">Если вы работаете с маршрутами, операции следует определить для каждого производственного маршрута, которые вы настроили.</span><span class="sxs-lookup"><span data-stu-id="34fea-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="34fea-140">Маршрут представляет собой путь, по которому номенклатура проходит от операции к операции, начиная с запуска производственного процесса, и до его завершения.</span><span class="sxs-lookup"><span data-stu-id="34fea-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="34fea-141">**Категории затрат** — настройка категорий затрат для определения почасовых затрат для указанного процесса, и время настройки.</span><span class="sxs-lookup"><span data-stu-id="34fea-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="34fea-142">**Группы затрат** — настройка групп затрат для создания и ведения различных типов затрат.</span><span class="sxs-lookup"><span data-stu-id="34fea-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="34fea-143">**Маршрутные группы** — настройка маршрутных групп для определения параметров, относящихся к группе маршрутов.</span><span class="sxs-lookup"><span data-stu-id="34fea-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="34fea-144">Перед созданием производственных маршрутов можно создать производственные маршруты.</span><span class="sxs-lookup"><span data-stu-id="34fea-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="34fea-145">**Маршруты** — настройка производственных маршрутов и определение настроек по умолчанию для управления планированием, затратами и ценами операций маршрутов, а также создания отчетов о ходе выполнения для управления отчетностью.</span><span class="sxs-lookup"><span data-stu-id="34fea-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="34fea-146">**Маршруты** — настройка версий маршрутов, чтобы обеспечить вариации номенклатур в производстве.</span><span class="sxs-lookup"><span data-stu-id="34fea-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="34fea-147">Дополнительные расширенные настройки</span><span class="sxs-lookup"><span data-stu-id="34fea-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="34fea-148">**Производственные группы** — настройка производственных групп для установки отношений между заказами на производство и счетами ГК.</span><span class="sxs-lookup"><span data-stu-id="34fea-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="34fea-149">Счета учета используются для разноски или группировки заказов в отчетах.</span><span class="sxs-lookup"><span data-stu-id="34fea-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="34fea-150">**Производственные кластеры** — создание производственных кластеров для группирования производственных заказов для обработки срочных производственных заказов или для удаления и разноски групп заказов.</span><span class="sxs-lookup"><span data-stu-id="34fea-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="34fea-151">**Свойства** — определение свойств для создания особых атрибутов, которые можно назначить ресурсам для управления последовательностью производства.</span><span class="sxs-lookup"><span data-stu-id="34fea-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="34fea-152">Эти атрибуты подключаются к шаблону рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="34fea-152">These attributes are connected to the working time template.</span></span>





