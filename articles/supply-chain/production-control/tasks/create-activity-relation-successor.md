---
title: 'Создание связи мероприятия: последующий элемент'
description: Поток мероприятий в бережливом производственном потоке документируется через связи мероприятия.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5e5844939e1eb40e31530c434c096c5b3be7abe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "325465"
---
# <a name="create-activity-relation-successor"></a><span data-ttu-id="77363-103">Создание связи мероприятия: последующий элемент</span><span class="sxs-lookup"><span data-stu-id="77363-103">Create activity relation: Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77363-104">Поток мероприятий в бережливом производственном потоке документируется через связи мероприятия.</span><span class="sxs-lookup"><span data-stu-id="77363-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="77363-105">Эта запись показывает, как создать связь мероприятия.</span><span class="sxs-lookup"><span data-stu-id="77363-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="77363-106">Обязательные компоненты:</span><span class="sxs-lookup"><span data-stu-id="77363-106">Prerequisites:</span></span>

- <span data-ttu-id="77363-107">Производственный поток и версия в черновом режиме.</span><span class="sxs-lookup"><span data-stu-id="77363-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="77363-108">Два мероприятия, следующих друг за другом в производственном потоке, создаются, но не связываются.</span><span class="sxs-lookup"><span data-stu-id="77363-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="77363-109">Поиск версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="77363-109">Find the production flow version</span></span> 
1. <span data-ttu-id="77363-110">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="77363-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="77363-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="77363-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="77363-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="77363-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="77363-113">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="77363-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="77363-114">В списке выберите черновую версию.</span><span class="sxs-lookup"><span data-stu-id="77363-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="77363-115">Связи мероприятий можно добавить как в черновые, так и в активные версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="77363-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="77363-116">Открыть обзор мероприятия</span><span class="sxs-lookup"><span data-stu-id="77363-116">Open the activity overview</span></span>
1. <span data-ttu-id="77363-117">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="77363-117">Click Activities.</span></span>
    * <span data-ttu-id="77363-118">Обратите внимание, что в форме отображаются все мероприятия производственного потока, которые назначены для версии производственного потока, в которой вы работаете.</span><span class="sxs-lookup"><span data-stu-id="77363-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="77363-119">Добавить последующий элемент</span><span class="sxs-lookup"><span data-stu-id="77363-119">Add a Successor</span></span>
1. <span data-ttu-id="77363-120">Щелкните "Добавить последующий элемент".</span><span class="sxs-lookup"><span data-stu-id="77363-120">Click Add successor.</span></span>
2. <span data-ttu-id="77363-121">В поле "Мероприятие" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="77363-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="77363-122">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="77363-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="77363-123">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="77363-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="77363-124">Установите флажок "Ограничение".</span><span class="sxs-lookup"><span data-stu-id="77363-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="77363-125">В поле "Значение ограничения" введите число.</span><span class="sxs-lookup"><span data-stu-id="77363-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="77363-126">Время ограничения — это время для планирования между плановым завершением предшествующего элемента (срок выполнения и время) и плановым началом последующего действия.</span><span class="sxs-lookup"><span data-stu-id="77363-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="77363-127">В поле "Единица" введите значение.</span><span class="sxs-lookup"><span data-stu-id="77363-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="77363-128">В поле "Коэффициент времени цикла" введите число.</span><span class="sxs-lookup"><span data-stu-id="77363-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="77363-129">Если оба мероприятия выполняются в одном и том же такте, то коэффициент времени цикла должен быть равен 1.</span><span class="sxs-lookup"><span data-stu-id="77363-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="77363-130">Если предшествующий элемент выполняется с удвоенной скоростью относительного последующего элемента, коэффициент должен быть равен 2.</span><span class="sxs-lookup"><span data-stu-id="77363-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="77363-131">Коэффициенты времени цикла используются для расчета отдельных времен циклов мероприятий производственного потока.</span><span class="sxs-lookup"><span data-stu-id="77363-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="77363-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="77363-132">Click OK.</span></span>
10. <span data-ttu-id="77363-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="77363-133">Close the page.</span></span>
11. <span data-ttu-id="77363-134">Перейдите на вкладку "Панель сетки".</span><span class="sxs-lookup"><span data-stu-id="77363-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="77363-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="77363-135">Close the page.</span></span>
13. <span data-ttu-id="77363-136">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="77363-136">Refresh the page.</span></span>

