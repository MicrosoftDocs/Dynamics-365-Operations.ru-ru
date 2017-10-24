---
title: "Контроль работы склада с шаблонами работы и директивами для мест хранения"
description: "Эта статья описывает, как использовать шаблоны работы и директивы расположения для того, чтобы определить, как и где выполняется работа на складе."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b32e2d178f9f0307fea4362e5ec99aa67c81ee8
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a><span data-ttu-id="7130e-103">Контроль работы склада с шаблонами работы и директивами для мест хранения</span><span class="sxs-lookup"><span data-stu-id="7130e-103">Control warehouse work by using work templates and location directives</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7130e-104">Эта статья описывает, как использовать шаблоны работы и директивы расположения для того, чтобы определить, как и где выполняется работа на складе.</span><span class="sxs-lookup"><span data-stu-id="7130e-104">This article describes how to use work templates and location directives to determine how and where work is carried out in the warehouse.</span></span>

<span data-ttu-id="7130e-105">Инструкции, которые работники склада получают на мобильное устройство, определяются рабочими шаблонами, которые вы настраиваете в Microsoft Dynamics 365 for Finance and Operations, чтобы определить разные процессы и задачи склад</span><span class="sxs-lookup"><span data-stu-id="7130e-105">The instructions that warehouse workers receive on a mobile device are determined by the work templates that you set up in Microsoft Dynamics 365 for Finance and Operations to define the various warehouse processes and tasks.</span></span> <span data-ttu-id="7130e-106">Шаблоны работы определяют, как работа выполнена для каждого процесса склада.</span><span class="sxs-lookup"><span data-stu-id="7130e-106">Work templates determine how the work is performed for each warehouse process.</span></span> <span data-ttu-id="7130e-107">Связывая директиву расположения с рабочими шаблонами, можно гарантировать, что работа выполняется в определенных физических областях склада.</span><span class="sxs-lookup"><span data-stu-id="7130e-107">By linking a location directive to work templates, you can help guarantee that work occurs in specific physical areas of the warehouses.</span></span>

## <a name="work-templates"></a><span data-ttu-id="7130e-108">Шаблоны работ</span><span class="sxs-lookup"><span data-stu-id="7130e-108">Work templates</span></span>
<span data-ttu-id="7130e-109">На странице **Рабочие шаблоны** можно определить рабочие операции, которые должны быть выполнены на складе.</span><span class="sxs-lookup"><span data-stu-id="7130e-109">The **Work templates** page lets you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="7130e-110">Как правило, рабочие операции склада состоят из пары действий: рабочий склада комплектует запасы в наличии в одном расположении и помещает скомплектованные запасы в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="7130e-110">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks up on-hand inventory in one location and then puts the picked inventory down in another location.</span></span> 

<span data-ttu-id="7130e-111">Рабочие шаблоны состоят из заголовка и связанных строк.</span><span class="sxs-lookup"><span data-stu-id="7130e-111">Work templates consists of a header and associated lines.</span></span> <span data-ttu-id="7130e-112">Каждый рабочий шаблон предназначен для определенного *типа заказа на работу*.</span><span class="sxs-lookup"><span data-stu-id="7130e-112">Each work template is for a specific *work order type*.</span></span> <span data-ttu-id="7130e-113">Многие типы заказов на работу связаны с исходными документами, например заказами на покупку или продажу.</span><span class="sxs-lookup"><span data-stu-id="7130e-113">Many work order types are associated with source documents, such as purchase or sales orders.</span></span> <span data-ttu-id="7130e-114">Тем не менее другие типы заказов на работу представляют отдельные складские процессы, например подсчет циклов.</span><span class="sxs-lookup"><span data-stu-id="7130e-114">However, other work order types represent separate warehouse processes, such as cycle counting.</span></span> <span data-ttu-id="7130e-115">*ИД пула работ* позволяет организовать работу по группам.</span><span class="sxs-lookup"><span data-stu-id="7130e-115">The *work pool ID* lets you organize work into groups.</span></span> 

<span data-ttu-id="7130e-116">Параметры в определении заголовка работы можно использовать, чтобы определить, когда создавать новый элемент работы.</span><span class="sxs-lookup"><span data-stu-id="7130e-116">The settings in the work header definition can be used to determine when a new piece of work should be created.</span></span> <span data-ttu-id="7130e-117">Например, можно задать максимальное число строк комплектования и максимальное ожидаемое время комплектования.</span><span class="sxs-lookup"><span data-stu-id="7130e-117">For example, you can set a maximum number of pick lines and a maximum expected pick time.</span></span> <span data-ttu-id="7130e-118">Затем, если работа по процессу комплектования заказа на продажу превышает какое-либо из этих значений, эта работа разделяется на два компонента.</span><span class="sxs-lookup"><span data-stu-id="7130e-118">Then, if the work for a sales order picking process exceeds either of those values, that work is split into two pieces of work.</span></span> 

<span data-ttu-id="7130e-119">Строки работы представляют физические задачи, которые необходимы для обработки работы.</span><span class="sxs-lookup"><span data-stu-id="7130e-119">The work lines represent the physical tasks that are required in order to process the work.</span></span> <span data-ttu-id="7130e-120">Например, для исходящего складского процесса может существовать строка работы для комплектования номенклатур на складе и другая строка для размещения этих номенклатур в зоне ожидания.</span><span class="sxs-lookup"><span data-stu-id="7130e-120">For example, for an outbound warehouse process, there might be a work line for picking up the items within the warehouse and another line for putting those items into a staging area.</span></span> <span data-ttu-id="7130e-121">Кроме того, может существовать дополнительная строка для комплектования номенклатур из зоны ожидания и еще одна строка для размещения номенклатур в грузовом автомобиле в процессе погрузки.</span><span class="sxs-lookup"><span data-stu-id="7130e-121">There can then be an additional line for picking the items from staging, and another line for putting the items into a truck as part of the loading process.</span></span> <span data-ttu-id="7130e-122">Можно задать *директивный код* в строках рабочего шаблона.</span><span class="sxs-lookup"><span data-stu-id="7130e-122">You can set a *directive code* on work template lines.</span></span> <span data-ttu-id="7130e-123">Директивный код связан с директивой расположения и помогает гарантировать, что складская работа обрабатывается в правильном расположении склада.</span><span class="sxs-lookup"><span data-stu-id="7130e-123">A directive code is linked to a location directive and therefore helps guarantee that the warehouse work is processed in the correct location in the warehouse.</span></span> 

<span data-ttu-id="7130e-124">Можно задать запрос, чтобы контролировать время использования определенного рабочего шаблона.</span><span class="sxs-lookup"><span data-stu-id="7130e-124">You can set up a query to control when a particular work template is used.</span></span> <span data-ttu-id="7130e-125">Например, можно задать ограничение, чтобы определенный шаблон можно было использовать только для работы на определенном складе.</span><span class="sxs-lookup"><span data-stu-id="7130e-125">For example, you can set a limitation so that a particular template can be used for work only in a specific warehouse.</span></span> <span data-ttu-id="7130e-126">Кроме того, можно использовать несколько шаблонов для создания работы для исходящей обработки заказов на продажу в зависимости от источника продаж.</span><span class="sxs-lookup"><span data-stu-id="7130e-126">Alternatively, you might have several templates that are used to create work for outbound sales order processing, depending on the sales origin.</span></span> <span data-ttu-id="7130e-127">Система использует поле **Порядковый номер**, чтобы определить порядок оценки доступных рабочих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7130e-127">The system uses the **Sequence number** field to determine the order that the available work templates are assessed in.</span></span> <span data-ttu-id="7130e-128">Следовательно, при наличии очень конкретного запроса для определенного рабочего шаблона нужно присвоить ему низкий порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="7130e-128">Therefore, if you have a very specific query for a particular work template, you should give it a low sequence number.</span></span> <span data-ttu-id="7130e-129">В этом случае запрос будет оцениваться раньше, чем другие, более общие запросы.</span><span class="sxs-lookup"><span data-stu-id="7130e-129">That query will then be evaluated before other, more general queries.</span></span> 

<span data-ttu-id="7130e-130">Чтобы остановить или приостановить рабочий процесс, можно воспользоваться параметром **Остановить работу** в строке работы.</span><span class="sxs-lookup"><span data-stu-id="7130e-130">To stop or pause a work process, you can use the **Stop work** setting on the work line.</span></span> <span data-ttu-id="7130e-131">В таком случае работник, выполняющий работу, не получит запрос на выполнение следующего этапа в строке работы.</span><span class="sxs-lookup"><span data-stu-id="7130e-131">In that case, the worker who is performing the work won't be asked to perform the next work line step.</span></span> <span data-ttu-id="7130e-132">Чтобы перейти к следующему шагу, этот или другой работник должен выбрать работу снова.</span><span class="sxs-lookup"><span data-stu-id="7130e-132">To move on to the next step, that worker or another worker must select the work again.</span></span> <span data-ttu-id="7130e-133">Можно разделить задачи в пределах элемента работы, воспользовавшись другим *ИД рабочего класса* в строках рабочего шаблона.</span><span class="sxs-lookup"><span data-stu-id="7130e-133">You can also separate the tasks within a piece of work by using a different *work class ID* on the work template lines.</span></span>

## <a name="location-directives"></a><span data-ttu-id="7130e-134">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="7130e-134">Location directives</span></span>
<span data-ttu-id="7130e-135">Директивы местонахождения — это правила, с помощью которых можно определить местонахождения комплектации и размещения для перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="7130e-135">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="7130e-136">Например, в проводке заказа на продажу директива местонахождения определяет места комплектации и размещения номенклатур.</span><span class="sxs-lookup"><span data-stu-id="7130e-136">For example, in a sales order transaction, a location directive determines where the items will be picked, and where the picked items will be put.</span></span> <span data-ttu-id="7130e-137">Директивы расположения состоят из заголовка и сопутствующих строк, и создаются на странице **Директивы расположения**.</span><span class="sxs-lookup"><span data-stu-id="7130e-137">Location directives consist of a header and associated lines, and you create them on the **Location directives** page.</span></span> 

<span data-ttu-id="7130e-138">В заголовке каждая директива расположения должна быть связана с *типом заказа на работу*, определяющим тип проводки по запасам, для которой будет использоваться директив, такой как заказы на продажу, пополнение или комплектация сырья.</span><span class="sxs-lookup"><span data-stu-id="7130e-138">On the header, each location directive must be associated with a *work order type* that specifies the type of inventory transaction that the directive will be used for, such as sales orders, replenishment, or raw material picking.</span></span> <span data-ttu-id="7130e-139">*Тип работы* определяет, будет ли директива расположения использоваться для комплектации или размещения работы, а также для других складских процессов, например расчета или изменения состояния запасов.</span><span class="sxs-lookup"><span data-stu-id="7130e-139">The *work type* specifies whether the location directive will be used for picking or putting work, or for some other warehouse process, such as counting or inventory status changes.</span></span> <span data-ttu-id="7130e-140">Необходимо также задать *объект* и *склад*.</span><span class="sxs-lookup"><span data-stu-id="7130e-140">You must also specify a *site* and a *warehouse*.</span></span> <span data-ttu-id="7130e-141">*Директивный код*, который вы определяете в заголовке, можно использовать, чтобы связать директиву расположения с одним или несколькими рабочими шаблонами.</span><span class="sxs-lookup"><span data-stu-id="7130e-141">A *directive code* that you specify on the header can be used to link the location directive to one or more work templates.</span></span> 

<span data-ttu-id="7130e-142">Что касается рабочих шаблонов, можно настроить запрос и определить, когда используется конкретная директива расположения.</span><span class="sxs-lookup"><span data-stu-id="7130e-142">As for work templates, you can set up a query to determine when a particular location directive is used.</span></span> <span data-ttu-id="7130e-143">Например, можно задать, что если электронная коммерция является источником заказа на продажу, запасы должны комплектоваться из специальной области склада.</span><span class="sxs-lookup"><span data-stu-id="7130e-143">For example, you can specify that when e-commerce is the origin of a sales order, the inventory must be picked up from a dedicated area in the warehouse.</span></span> <span data-ttu-id="7130e-144">Система использует поле **Порядковый номер** для идентификации заказа, в котором оцениваются директивы доступного местоположения.</span><span class="sxs-lookup"><span data-stu-id="7130e-144">The system uses the **Sequence number** field to determine the order that the available location directives are assessed in.</span></span> 

<span data-ttu-id="7130e-145">Строки директив местоположения задают дополнительные ограничения на применение правил поиска местоположения.</span><span class="sxs-lookup"><span data-stu-id="7130e-145">The location directive lines set additional restrictions on the application of the location finding rules.</span></span> <span data-ttu-id="7130e-146">Можно определить минимальное количество и максимальное количество, к которому должна применяться директива, и можно указать, что директива должна относиться к конкретной единице измерения складского учета.</span><span class="sxs-lookup"><span data-stu-id="7130e-146">You can specify a minimum quantity and a maximum quantity that the directive should apply to, and you can specify that the directive should be for a specific inventory unit.</span></span> <span data-ttu-id="7130e-147">Например, если единицей измерения является палета, в определенном местонахождении можно разместить номенклатуры в палетах.</span><span class="sxs-lookup"><span data-stu-id="7130e-147">For example, if the unit of measure is pallets, the items in pallets can be put in a specific location.</span></span> <span data-ttu-id="7130e-148">Можно также определить, может ли количество разделяться между несколькими расположениями.</span><span class="sxs-lookup"><span data-stu-id="7130e-148">You can also specify whether the quantity can be split across multiple locations.</span></span> <span data-ttu-id="7130e-149">В качестве заголовка директивы местоположения каждая строка директивы местоположения имеет порядковый номер, определяющий порядок, в котором оцениваются строки.</span><span class="sxs-lookup"><span data-stu-id="7130e-149">Like the location directive header, each location directive line has a sequence number that determines the order that the lines are assessed in.</span></span> 

<span data-ttu-id="7130e-150">Директивы местоположения имеют один дополнительный уровень детализации: *действия директивы местоположения*.</span><span class="sxs-lookup"><span data-stu-id="7130e-150">Location directives have one additional level of detail: *location directive actions*.</span></span> <span data-ttu-id="7130e-151">Можно определить несколько действий директивы расположения для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="7130e-151">You can define multiple location directive actions for each line.</span></span> <span data-ttu-id="7130e-152">Опять же, порядковый номер используется, чтобы определить порядок оценки действий.</span><span class="sxs-lookup"><span data-stu-id="7130e-152">Once again, a sequence number is used to determine the order that the actions are assessed in.</span></span> <span data-ttu-id="7130e-153">На этом уровне можно настроить запрос для определения способа поиска оптимального расположения на складе.</span><span class="sxs-lookup"><span data-stu-id="7130e-153">On this level, you can set up a query to define how to find the best location in the warehouse.</span></span> <span data-ttu-id="7130e-154">Для поиска оптимального расположения можно также использовать предопределенные параметры **Стратегия**.</span><span class="sxs-lookup"><span data-stu-id="7130e-154">You can also use predefined **Strategy** settings to find an optimal location.</span></span>

### <a name="example-of-the-use-of-location-directives"></a><span data-ttu-id="7130e-155">Пример использования директив расположения</span><span class="sxs-lookup"><span data-stu-id="7130e-155">Example of the use of location directives</span></span>

<span data-ttu-id="7130e-156">В этом примере мы рассмотрим процедуру, связанную с заказом на покупку, когда директива расположения должна найти свободное место на складе для единиц измерения складского учета, которые только что были зарегистрированы в доке приемке.</span><span class="sxs-lookup"><span data-stu-id="7130e-156">For this example, we will consider a purchase order process where the location directive must find free capacity within a warehouse for inventory items that have just been registered at the receiving dock.</span></span> <span data-ttu-id="7130e-157">Во-первых, нужно попытаться найти свободное место на складе, выполнив объединение с существующими запасами в наличии.</span><span class="sxs-lookup"><span data-stu-id="7130e-157">First, we want to try to find free capacity within the warehouse by consolidating with existing on-hand inventory.</span></span> <span data-ttu-id="7130e-158">Если это невозможно, нужно найти пустое расположение.</span><span class="sxs-lookup"><span data-stu-id="7130e-158">If consolidation isn't possible, we then want to find an empty location.</span></span> 

<span data-ttu-id="7130e-159">Для этого сценария необходимо определить два действия директивы расположения.</span><span class="sxs-lookup"><span data-stu-id="7130e-159">For this scenario, we must define two location directive actions.</span></span> <span data-ttu-id="7130e-160">Первое действие в последовательности должно использовать стратегию **Консолидировать**, а второе — **Пустое расположение без входящей работы**.</span><span class="sxs-lookup"><span data-stu-id="7130e-160">The first action in the sequence must use the **Consolidate** strategy, and the second should use the **Empty location with no incoming work** strategy.</span></span> <span data-ttu-id="7130e-161">Если не определено третье действие для обработки сценария переполнения, возможны два результата, если места на складе нет: работа будет создана, несмотря на отсутствие определенных расположений, либо процедура создания работы завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="7130e-161">Unless we define a third action to handle an overflow scenario, two outcomes are possible when there is no more capacity in the warehouse: work can be created even though no locations are defined, or the work creation process can fail.</span></span> <span data-ttu-id="7130e-162">Результат определяется настройкой страницы **Сбои директивы расположения**, где можно определить, нужно ли выбирать параметр **Останавливать работу в случае сбоя директивы расположения** для каждого типа заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="7130e-162">The outcome is determined by the setup on the **Location directive failures** page, where you can decide whether to select the **Stop work on location directive failure** option for each work order type.</span></span>



