---
title: Создание внутрихолдингового плана
description: Эта процедура демонстрирует порядок создания внутрихолдингового плана.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867358"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="b0bd8-103">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="b0bd8-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0bd8-104">Эта процедура демонстрирует порядок создания внутрихолдингового плана.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="b0bd8-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="b0bd8-106">Настройка группы внутрихолдингового планирования</span><span class="sxs-lookup"><span data-stu-id="b0bd8-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="b0bd8-107">В **области переходов** выберите **Модули > Сводное планирование > Настройка > Группы внутрихолдингового планирования**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="b0bd8-108">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b0bd8-109">Например, отфильтруйте поле "Имя" по значению "10".</span><span class="sxs-lookup"><span data-stu-id="b0bd8-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="b0bd8-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b0bd8-111">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-111">Select **Delete**.</span></span> <span data-ttu-id="b0bd8-112">Это действие необходимо, чтобы ускорить выполнение внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="b0bd8-113">Внутрихолдинговое планирование будет выполнять сводное планирование во всех компаниях в группе планирования, начиная с наименьшей запланированной последовательности.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="b0bd8-114">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-114">Select **Yes**.</span></span>
6. <span data-ttu-id="b0bd8-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="b0bd8-116">Создание внутрихолдингового сводного плана</span><span class="sxs-lookup"><span data-stu-id="b0bd8-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="b0bd8-117">В **области переходов** выберите **Модули > Сводное планирование > Рабочие области > Сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="b0bd8-118">Выберите **Внутрихолдинговое сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="b0bd8-119">В поле **Группа внутрихолдингового планирования** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b0bd8-120">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="b0bd8-121">Выберите группу внутрихолдингового планирования 10.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="b0bd8-122">В поле **Количество внутрихолдинговых итераций планирования** введите "2".</span><span class="sxs-lookup"><span data-stu-id="b0bd8-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="b0bd8-123">Группа внутрихолдингового планирования 10 содержит двух участников.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="b0bd8-124">Чтобы распространить задержки из компании-источника (USMF) на компанию клиента (DEMF), потребуется выполнить внутрихолдинговое планирование в обеих компаниях два раза.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="b0bd8-125">Первая итерация распространяет спрос и определяет задержки в компании-источнике (USMF).</span><span class="sxs-lookup"><span data-stu-id="b0bd8-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="b0bd8-126">Вторая итерация распространяет задержки из USMF на DEMF.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="b0bd8-127">В поле **Первая итерация** выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="b0bd8-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="b0bd8-128">В поле **Последующие итерации** выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="b0bd8-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="b0bd8-129">В поле **Количество потоков** введите число.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="b0bd8-130">Представляет собой количество параллельных потоков, которые будут использоваться для планирования.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="b0bd8-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="b0bd8-132">Просмотр результата плана</span><span class="sxs-lookup"><span data-stu-id="b0bd8-132">View the result of the plan</span></span>

1. <span data-ttu-id="b0bd8-133">В поле **План** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="b0bd8-134">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="b0bd8-135">Выберите ссылку для StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="b0bd8-136">Необходимо находиться в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="b0bd8-137">Выберите **Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="b0bd8-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]