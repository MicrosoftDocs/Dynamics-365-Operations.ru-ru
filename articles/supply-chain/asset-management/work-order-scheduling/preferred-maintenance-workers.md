---
title: Настройка предпочитаемых специалистов по обслуживанию
description: В этом разделе описан порядок настройки предпочтительных специалистов по обслуживанию в модуле "Управлении активами".
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887419"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="c3d87-103">Предпочтительные специалисты по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="c3d87-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c3d87-104">Можно задать предпочтения в отношении того, какие специалисты по обслуживанию назначаются для выполнения заказов на работу во время планирования заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="c3d87-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="c3d87-105">Использование этой функции не является обязательным, но может помочь в выборе наиболее квалифицированного специалиста по обслуживанию для выполнения задания на основе навыков и компетенций специалиста.</span><span class="sxs-lookup"><span data-stu-id="c3d87-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="c3d87-106">Таким образом, при планировании заказов на работу настройка в поле **Предпочтительные специалисты по обслуживанию** обслуживания используется, чтобы определить, следует ли планировать конкретного сотрудника или группу сотрудников для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="c3d87-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="c3d87-107">Планируются только специалисты по обслуживанию, доступные во время планирования.</span><span class="sxs-lookup"><span data-stu-id="c3d87-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="c3d87-108">Если при планировании настройка предпочтительного специалиста по обслуживанию соответствует заказу на работу, но специалист по обслуживанию назначен на другое задание, заказ на работу будет запланирован другому доступному специалисту по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="c3d87-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="c3d87-109">Прежде чем вы сможете настроить предпочтительных специалистов по обслуживанию, сначала нужно настроить специалистов и группы специалистов по обслуживанию, которые должны быть доступны для выбора.</span><span class="sxs-lookup"><span data-stu-id="c3d87-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="c3d87-110">Описание того, как настроить специалистов и группы специалистов по обслуживанию, см. в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c3d87-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="c3d87-111">Настройка предпочтительных специалистов</span><span class="sxs-lookup"><span data-stu-id="c3d87-111">Set up preferred workers</span></span>

<span data-ttu-id="c3d87-112">Предпочтительный специалист по обслуживанию или группа специалистов могут быть связаны с конкретными значениями полей</span><span class="sxs-lookup"><span data-stu-id="c3d87-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="c3d87-113">торговля</span><span class="sxs-lookup"><span data-stu-id="c3d87-113">trade</span></span>  
- <span data-ttu-id="c3d87-114">вариант тип задания обслуживания</span><span class="sxs-lookup"><span data-stu-id="c3d87-114">maintenance job type variant</span></span>  
- <span data-ttu-id="c3d87-115">тип задания обслуживания</span><span class="sxs-lookup"><span data-stu-id="c3d87-115">maintenance job type</span></span>  
- <span data-ttu-id="c3d87-116">категория типа задания обслуживания</span><span class="sxs-lookup"><span data-stu-id="c3d87-116">maintenance job type category</span></span>  
- <span data-ttu-id="c3d87-117">ОС</span><span class="sxs-lookup"><span data-stu-id="c3d87-117">asset</span></span>  
- <span data-ttu-id="c3d87-118">тип актива</span><span class="sxs-lookup"><span data-stu-id="c3d87-118">asset type</span></span>  

<span data-ttu-id="c3d87-119">или комбинацией этих параметров.</span><span class="sxs-lookup"><span data-stu-id="c3d87-119">or a combination of those selections.</span></span> <span data-ttu-id="c3d87-120">Чем больше параметров выбрано для одной и той же записи, тем более конкретной будет настройка.</span><span class="sxs-lookup"><span data-stu-id="c3d87-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="c3d87-121">Щелкните **Управление активами** > **Настройка** > **Работники** > **Предпочтительные специалисты по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="c3d87-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="c3d87-122">Для создания новой записи щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c3d87-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="c3d87-123">Начните с создания настройки специалиста или группы специалистов по обслуживанию "по умолчанию", у которых не выбраны никакие поля из приведенного выше маркированного списка.</span><span class="sxs-lookup"><span data-stu-id="c3d87-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="c3d87-124">Это означает , что выбор осуществляется только в поле **Предпочтительная группа специалистов по обслуживанию** или в поле **Предпочтительный специалист по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="c3d87-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="c3d87-125">На приведенном ниже рисунке показан пример первой записи, в которой "Запросы" выбраны в качестве предпочтительной группы специалистов по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="c3d87-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="c3d87-126">Настройка по умолчанию будет использоваться при планировании заказа на работу, если никакая другая, более конкретная комбинация не соответствует содержимому заказа на работу во время планирования заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="c3d87-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="c3d87-127">Для создания новой записи повторите шаг 2.</span><span class="sxs-lookup"><span data-stu-id="c3d87-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="c3d87-128">Выберите требуемые параметры, в зависимости от уровня детализации для предпочтительного специалиста или группы специалистов.</span><span class="sxs-lookup"><span data-stu-id="c3d87-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="c3d87-129">*Пример:* на следующем рисунке в шестой записи специалист по обслуживанию Шон Ричардсон (Shawn Richardson) выбран как предпочитаемый работник.</span><span class="sxs-lookup"><span data-stu-id="c3d87-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="c3d87-130">Он будет автоматически выбран при планировании заказа на работу, который включает актив "CH-BP1-03-02" и тип задания обслуживания "Оценка помещения", если он доступен в запланированное время.</span><span class="sxs-lookup"><span data-stu-id="c3d87-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="c3d87-131">Обычно при выборе предпочтительного специалиста по обслуживанию во время планирования заказов на работу управление активами просматривает все записи **Предпочтительные специалисты по обслуживанию** для проверки возможных совпадений, всегда сначала проверяя наиболее конкретные комбинации.</span><span class="sxs-lookup"><span data-stu-id="c3d87-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="c3d87-132">Если совпадений не найдено, используется запись "по умолчанию" с выбором в поле **Предпочтительная группа специалистов по обслуживанию** или в поле **Предпочтительный специалист по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="c3d87-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Рисунок 1](media/02-work-order-scheduling.png)

<span data-ttu-id="c3d87-134">Можно также настроить ответственных специалистов по обслуживанию, которые могут быть выбраны при создании запроса на обслуживание или заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="c3d87-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="c3d87-135">В разделе **Все заказы на работу** и **Все запросы на обслуживание** можно изменить выбор, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="c3d87-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="c3d87-136">Дополнительную информацию см. в разделе [Ответственные специалисты по обслуживанию](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="c3d87-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="c3d87-137">При планировании заказов на работу рассчитываются различные показатели, чтобы определить, какие работники должны выполнять задания, связанные с заказом на работу ( эти показатели настраиваются в ссылке **Параметры управления активами** > **Планирование заказа на работу**).</span><span class="sxs-lookup"><span data-stu-id="c3d87-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="c3d87-138">Если два или более предпочтительных или ответственных специалистов по обслуживанию получат одинаковый балл во время планирования заказов на работу, один из специалистов выбирается случайным образом.</span><span class="sxs-lookup"><span data-stu-id="c3d87-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="c3d87-139">В противном случае всегда назначается специалист с наивысшим рейтингом для выполнения заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="c3d87-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

