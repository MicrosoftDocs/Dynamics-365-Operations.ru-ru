---
title: Создание внутрихолдингового плана
description: Эта процедура демонстрирует порядок создания внутрихолдингового плана.
author: ShylaThompson
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fb787955a67776b24b626eb23b7c1a9df87a0c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841703"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="5ffd2-103">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="5ffd2-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ffd2-104">Эта процедура демонстрирует порядок создания внутрихолдингового плана.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="5ffd2-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="5ffd2-106">Настройка группы внутрихолдингового планирования</span><span class="sxs-lookup"><span data-stu-id="5ffd2-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="5ffd2-107">В **области переходов** выберите **Модули > Сводное планирование > Настройка > Группы внутрихолдингового планирования**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="5ffd2-108">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5ffd2-109">Например, отфильтруйте поле "Имя" по значению "10".</span><span class="sxs-lookup"><span data-stu-id="5ffd2-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="5ffd2-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5ffd2-111">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-111">Click **Delete**.</span></span> <span data-ttu-id="5ffd2-112">Это действие необходимо, чтобы ускорить выполнение внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="5ffd2-113">Внутрихолдинговое планирование будет выполнять сводное планирование во всех компаниях в группе планирования, начиная с наименьшей запланированной последовательности.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="5ffd2-114">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-114">Click **Yes**.</span></span>
6. <span data-ttu-id="5ffd2-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="5ffd2-116">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="5ffd2-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="5ffd2-117">В **области переходов** выберите **Модули > Сводное планирование > Рабочие области > Сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="5ffd2-118">Щелкните **Внутрихолдинговое сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="5ffd2-119">В поле **Группа внутрихолдингового планирования** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5ffd2-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="5ffd2-121">Выберите группу внутрихолдингового планирования 10.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="5ffd2-122">В поле **Количество внутрихолдинговых итераций планирования** введите "2".</span><span class="sxs-lookup"><span data-stu-id="5ffd2-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="5ffd2-123">Группа внутрихолдингового планирования 10 содержит двух участников.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="5ffd2-124">Чтобы распространить задержки из компании-источника (USMF) на компанию клиента (DEMF), потребуется выполнить внутрихолдинговое планирование в обеих компаниях два раза.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="5ffd2-125">Первая итерация распространяет спрос и определяет задержки в компании-источнике (USMF).</span><span class="sxs-lookup"><span data-stu-id="5ffd2-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="5ffd2-126">Вторая итерация распространяет задержки из USMF на DEMF.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="5ffd2-127">В поле **Первая итерация** выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="5ffd2-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="5ffd2-128">В поле **Последующие итерации** выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="5ffd2-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="5ffd2-129">В поле **Количество потоков** введите число.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="5ffd2-130">Представляет собой количество параллельных потоков, которые будут использоваться для планирования.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="5ffd2-131">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="5ffd2-132">Просмотр результата плана</span><span class="sxs-lookup"><span data-stu-id="5ffd2-132">View the result of the plan</span></span>
1. <span data-ttu-id="5ffd2-133">В поле **План** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="5ffd2-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="5ffd2-135">Нажмите на ссылку для StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="5ffd2-136">Необходимо находиться в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="5ffd2-137">Щелкните **Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="5ffd2-137">Click **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]