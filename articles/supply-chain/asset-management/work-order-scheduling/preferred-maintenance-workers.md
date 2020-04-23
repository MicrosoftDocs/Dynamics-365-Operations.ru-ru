---
title: Настройка предпочитаемых специалистов по обслуживанию
description: В этом разделе описан порядок настройки предпочтительных специалистов по обслуживанию в модуле "Управлении активами".
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 327cda12a05ad54b310e472a652f1c822ad97142
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215340"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="b3a2e-103">Настройка предпочитаемых специалистов по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="b3a2e-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b3a2e-104">Во время планирования заказа на работу можно задать предпочтения в отношении того, какие специалисты или группы специалистов по обслуживанию назначаются для выполнения заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="b3a2e-105">Использование этой функции не является обязательным, но может помочь в выборе наиболее квалифицированного специалиста по обслуживанию для выполнения задания на основе навыков и компетенций специалиста.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="b3a2e-106">Планируются только специалисты по обслуживанию, доступные во время планирования.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="b3a2e-107">Если при планировании настройка предпочтительного специалиста по обслуживанию соответствует заказу на работу, но специалист по обслуживанию назначен на другое задание, заказ на работу будет запланирован другому доступному специалисту по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="b3a2e-108">Прежде чем можно будет настроить предпочтительных специалистов по обслуживанию, необходимо сначала настроить специалистов и группы специалистов по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="b3a2e-109">Описание того, как настроить специалистов и группы специалистов по обслуживанию, см. в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="b3a2e-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="b3a2e-110">Настройка предпочтительных специалистов</span><span class="sxs-lookup"><span data-stu-id="b3a2e-110">Set up preferred workers</span></span>

<span data-ttu-id="b3a2e-111">Предпочтительный специалист или группа специалистов по обслуживанию могут быть связаны с одним или несколькими из следующих:</span><span class="sxs-lookup"><span data-stu-id="b3a2e-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="b3a2e-112">торговля</span><span class="sxs-lookup"><span data-stu-id="b3a2e-112">trade</span></span>  
- <span data-ttu-id="b3a2e-113">вариант тип задания обслуживания</span><span class="sxs-lookup"><span data-stu-id="b3a2e-113">maintenance job type variant</span></span>  
- <span data-ttu-id="b3a2e-114">тип задания обслуживания</span><span class="sxs-lookup"><span data-stu-id="b3a2e-114">maintenance job type</span></span>  
- <span data-ttu-id="b3a2e-115">категория типа задания обслуживания</span><span class="sxs-lookup"><span data-stu-id="b3a2e-115">maintenance job type category</span></span>  
- <span data-ttu-id="b3a2e-116">ОС</span><span class="sxs-lookup"><span data-stu-id="b3a2e-116">asset</span></span>  
- <span data-ttu-id="b3a2e-117">тип актива</span><span class="sxs-lookup"><span data-stu-id="b3a2e-117">asset type</span></span>  

<span data-ttu-id="b3a2e-118">Чем больше параметров выбрано для одной и той же записи, тем более конкретной будет настройка.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="b3a2e-119">Щелкните **Управление активами** > **Настройка** > **Работники** > **Предпочтительные специалисты по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="b3a2e-120">Для создания новой записи щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="b3a2e-121">Начнем с создания специалиста или группы специалистов по обслуживанию "по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="b3a2e-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="b3a2e-122">Это означает , что выбор осуществляется только в поле **Предпочтительная группа специалистов по обслуживанию** или в поле **Предпочтительный специалист по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="b3a2e-123">На приведенном ниже снимке экрана показан пример первой записи, в которой "Запросы" выбраны как **Предпочтительная группа специалистов по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="b3a2e-124">Эта настройка по умолчанию будет использоваться при планировании заказа на работу, если никакая другая, более конкретная комбинация не соответствует содержимому заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="b3a2e-125">Для создания новой записи повторите шаг 2.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="b3a2e-126">Выберите требуемые параметры, в зависимости от уровня детализации для предпочтительного специалиста или группы специалистов.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="b3a2e-127">*Пример:* на следующем снимке экрана в шестой записи специалист по обслуживанию Шон Ричардсон (Shawn Richardson) выбран как предпочитаемый работник.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="b3a2e-128">Он будет автоматически выбран при планировании заказа на работу, который включает актив "CH-BP1-03-02" и тип задания обслуживания "Оценка помещения", если он доступен в запланированное время.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="b3a2e-129">Обычно при выборе предпочтительного специалиста по обслуживанию во время планирования заказов на работу управление активами просматривает все записи **Предпочтительные специалисты по обслуживанию** для проверки возможных совпадений, всегда сначала проверяя наиболее конкретные комбинации.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="b3a2e-130">Если совпадений не найдено, используется запись "по умолчанию" с выбором в поле **Предпочтительная группа специалистов по обслуживанию** или в поле **Предпочтительный специалист по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Рисунок 1](media/02-work-order-scheduling.png)

<span data-ttu-id="b3a2e-132">Можно также настроить *ответственных* специалистов по обслуживанию, которые могут быть выбраны при создании запроса на обслуживание или заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="b3a2e-133">Можно изменить выбор в разделе **Все заказы на работу** и **Все запросы на обслуживание**, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="b3a2e-134">Дополнительную информацию см. в разделе [Ответственные специалисты по обслуживанию](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="b3a2e-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="b3a2e-135">При планировании заказов на работу рассчитываются различные показатели, чтобы определить, какие работники должны выполнять задания, связанные с заказом на работу ( эти показатели настраиваются в ссылке **Параметры управления активами** > **Планирование заказа на работу**).</span><span class="sxs-lookup"><span data-stu-id="b3a2e-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="b3a2e-136">Если два или более предпочтительных или ответственных специалистов по обслуживанию получат одинаковый балл во время планирования заказов на работу, один из специалистов выбирается случайным образом.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="b3a2e-137">В противном случае всегда назначается специалист с наивысшим рейтингом для выполнения заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="b3a2e-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

