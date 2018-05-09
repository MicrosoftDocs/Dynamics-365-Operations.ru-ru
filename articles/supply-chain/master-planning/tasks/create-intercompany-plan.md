--- 
title: "Создание внутрихолдингового плана"
description: "Эта процедура демонстрирует порядок создания внутрихолдингового плана."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 287741ce871f7f7cff7c2e2159b28ec509058240
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="a7717-103">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="a7717-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7717-104">Эта процедура демонстрирует порядок создания внутрихолдингового плана.</span><span class="sxs-lookup"><span data-stu-id="a7717-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="a7717-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a7717-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="a7717-106">Настройка группы внутрихолдингового планирования</span><span class="sxs-lookup"><span data-stu-id="a7717-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="a7717-107">Перейдите к группам внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="a7717-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="a7717-108">"Сводное планирование" > "Настройка" > "Группы внутрихолдингового планирования"</span><span class="sxs-lookup"><span data-stu-id="a7717-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="a7717-109">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="a7717-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a7717-110">Например, отфильтруйте поле "Имя" по значению "10".</span><span class="sxs-lookup"><span data-stu-id="a7717-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="a7717-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a7717-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a7717-112">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="a7717-112">Click Delete.</span></span>
    * <span data-ttu-id="a7717-113">Это действие необходимо, чтобы ускорить выполнение внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="a7717-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="a7717-114">Внутрихолдинговое планирование будет выполнять сводное планирование во всех компаниях в группе планирования, начиная с наименьшей запланированной последовательности.</span><span class="sxs-lookup"><span data-stu-id="a7717-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="a7717-115">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="a7717-115">Click Yes.</span></span>
6. <span data-ttu-id="a7717-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a7717-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="a7717-117">Создание внутрихолдингового плана</span><span class="sxs-lookup"><span data-stu-id="a7717-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="a7717-118">Щелкните "Внутрихолдинговое сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="a7717-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="a7717-119">Это в рабочей области сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="a7717-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="a7717-120">В поле "Группа внутрихолдингового планирования" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a7717-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a7717-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a7717-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7717-122">Выберите группу внутрихолдингового планирования 10.</span><span class="sxs-lookup"><span data-stu-id="a7717-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="a7717-123">В поле "Количество внутрихолдинговых итераций планирования" введите "2".</span><span class="sxs-lookup"><span data-stu-id="a7717-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="a7717-124">Группа внутрихолдингового планирования 10 содержит двух участников.</span><span class="sxs-lookup"><span data-stu-id="a7717-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="a7717-125">Чтобы распространить задержки из компании-источника (USMF) на компанию клиента (DEMF), потребуется выполнить внутрихолдинговое планирование в обеих компаниях два раза.</span><span class="sxs-lookup"><span data-stu-id="a7717-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="a7717-126">Первая итерация распространяет спрос и определяет задержки в компании-источнике (USMF).</span><span class="sxs-lookup"><span data-stu-id="a7717-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="a7717-127">Вторая итерация распространяет задержки из USMF на DEMF.</span><span class="sxs-lookup"><span data-stu-id="a7717-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="a7717-128">В поле "Первая итерация" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="a7717-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="a7717-129">В поле "Первая итерация" выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="a7717-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="a7717-130">В поле "Последующие итерации" выберите "Пересоздание".</span><span class="sxs-lookup"><span data-stu-id="a7717-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="a7717-131">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="a7717-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="a7717-132">Представляет собой количество параллельных потоков, которые будут использоваться для планирования.</span><span class="sxs-lookup"><span data-stu-id="a7717-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="a7717-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a7717-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="a7717-134">Просмотр результата плана</span><span class="sxs-lookup"><span data-stu-id="a7717-134">View the result of the plan</span></span>
1. <span data-ttu-id="a7717-135">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a7717-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a7717-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a7717-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7717-137">Нажмите на ссылку для StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="a7717-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="a7717-138">Необходимо находиться в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="a7717-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="a7717-139">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="a7717-139">Click Planned orders.</span></span>


