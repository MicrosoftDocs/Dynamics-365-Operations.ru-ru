---
title: Создание внутрихолдингового плана
description: Эта процедура демонстрирует порядок создания внутрихолдингового плана.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555985"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="38670-103">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="38670-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38670-104">Эта процедура демонстрирует порядок создания внутрихолдингового плана.</span><span class="sxs-lookup"><span data-stu-id="38670-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="38670-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="38670-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="38670-106">Настройка группы внутрихолдингового планирования</span><span class="sxs-lookup"><span data-stu-id="38670-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="38670-107">Перейдите к группам внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="38670-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="38670-108">"Сводное планирование" > "Настройка" > "Группы внутрихолдингового планирования"</span><span class="sxs-lookup"><span data-stu-id="38670-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="38670-109">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="38670-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="38670-110">Например, отфильтруйте поле "Имя" по значению "10".</span><span class="sxs-lookup"><span data-stu-id="38670-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="38670-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="38670-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="38670-112">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="38670-112">Click Delete.</span></span>
    * <span data-ttu-id="38670-113">Это действие необходимо, чтобы ускорить выполнение внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="38670-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="38670-114">Внутрихолдинговое планирование будет выполнять сводное планирование во всех компаниях в группе планирования, начиная с наименьшей запланированной последовательности.</span><span class="sxs-lookup"><span data-stu-id="38670-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="38670-115">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="38670-115">Click Yes.</span></span>
6. <span data-ttu-id="38670-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="38670-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="38670-117">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="38670-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="38670-118">Щелкните "Внутрихолдинговое сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="38670-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="38670-119">Это в рабочей области сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="38670-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="38670-120">В поле "Группа внутрихолдингового планирования" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="38670-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="38670-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="38670-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="38670-122">Выберите группу внутрихолдингового планирования 10.</span><span class="sxs-lookup"><span data-stu-id="38670-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="38670-123">В поле "Количество внутрихолдинговых итераций планирования" введите "2".</span><span class="sxs-lookup"><span data-stu-id="38670-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="38670-124">Группа внутрихолдингового планирования 10 содержит двух участников.</span><span class="sxs-lookup"><span data-stu-id="38670-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="38670-125">Чтобы распространить задержки из компании-источника (USMF) на компанию клиента (DEMF), потребуется выполнить внутрихолдинговое планирование в обеих компаниях два раза.</span><span class="sxs-lookup"><span data-stu-id="38670-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="38670-126">Первая итерация распространяет спрос и определяет задержки в компании-источнике (USMF).</span><span class="sxs-lookup"><span data-stu-id="38670-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="38670-127">Вторая итерация распространяет задержки из USMF на DEMF.</span><span class="sxs-lookup"><span data-stu-id="38670-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="38670-128">В поле "Первая итерация" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="38670-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="38670-129">В поле "Первая итерация" выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="38670-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="38670-130">В поле "Последующие итерации" выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="38670-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="38670-131">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="38670-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="38670-132">Представляет собой количество параллельных потоков, которые будут использоваться для планирования.</span><span class="sxs-lookup"><span data-stu-id="38670-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="38670-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="38670-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="38670-134">Просмотр результата плана</span><span class="sxs-lookup"><span data-stu-id="38670-134">View the result of the plan</span></span>
1. <span data-ttu-id="38670-135">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="38670-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="38670-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="38670-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="38670-137">Нажмите на ссылку для StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="38670-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="38670-138">Необходимо находиться в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="38670-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="38670-139">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="38670-139">Click Planned orders.</span></span>

