---
title: Анализ результатов анкеты
description: Статистику анкетирования можно использовать для расчета среднего, итогов и процентов по набору демографических данных.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b49868b76dcc0a5df420e56fd1fc2477c475596
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115182"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="cfed1-103">Анализ результатов анкеты</span><span class="sxs-lookup"><span data-stu-id="cfed1-103">Analyzing questionnaire results</span></span>



<span data-ttu-id="cfed1-104">Статистику анкетирования можно использовать для расчета среднего, итогов и процентов по набору демографических данных.</span><span class="sxs-lookup"><span data-stu-id="cfed1-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="cfed1-105">Чтобы начать эту процедуру, перейдите в раздел "Анкета" > "Просмотр и анализ результатов" > "Статистика анкетирования".</span><span class="sxs-lookup"><span data-stu-id="cfed1-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="cfed1-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="cfed1-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="cfed1-107">Создание записи статистики анкетирования</span><span class="sxs-lookup"><span data-stu-id="cfed1-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="cfed1-108">Перейдите в раздел "Статистика анкетирования".</span><span class="sxs-lookup"><span data-stu-id="cfed1-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="cfed1-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cfed1-109">Click New.</span></span>
3. <span data-ttu-id="cfed1-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="cfed1-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cfed1-111">В поле "Статистика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cfed1-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="cfed1-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cfed1-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cfed1-113">В поле "Анкета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cfed1-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cfed1-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cfed1-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cfed1-115">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="cfed1-115">Click the General tab.</span></span>
    * <span data-ttu-id="cfed1-116">Укажите, следует ли включить анонимные результаты или результаты от работников, контактных лиц и кандидатов.</span><span class="sxs-lookup"><span data-stu-id="cfed1-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="cfed1-117">Установите или снимите флажок "Работник".</span><span class="sxs-lookup"><span data-stu-id="cfed1-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="cfed1-118">Если вы будете просматривать результаты по трудовом стажу или возрасту, укажите интервалы, которые вам хотелось бы использовать для группирования результатов.</span><span class="sxs-lookup"><span data-stu-id="cfed1-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="cfed1-119">Если ввести в качестве возрастного интервала 5, результаты будут сгруппированы по пятилетним интервалам.</span><span class="sxs-lookup"><span data-stu-id="cfed1-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="cfed1-120">В поле "Возраст" введите число.</span><span class="sxs-lookup"><span data-stu-id="cfed1-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="cfed1-121">Укажите, следует ли запустить расчет для всей анкеты, для каждой группы результатов, для каждого вопроса или для каждой строки вопроса.</span><span class="sxs-lookup"><span data-stu-id="cfed1-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="cfed1-122">Выберите, как требуется сгруппировать результаты.</span><span class="sxs-lookup"><span data-stu-id="cfed1-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="cfed1-123">Например, при расчете среднего количества баллов на вопрос имеет смысл просматривать вопросы сгруппированными по группе результатов.</span><span class="sxs-lookup"><span data-stu-id="cfed1-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="cfed1-124">Выберите данные, на которых будет основан расчет.</span><span class="sxs-lookup"><span data-stu-id="cfed1-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="cfed1-125">Например, если вы хотите просматривать средний полученный по анкете процент по своим работникам, а не среднее полученное количество баллов по работникам.</span><span class="sxs-lookup"><span data-stu-id="cfed1-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="cfed1-126">Перейдите на вкладку "Диапазон".</span><span class="sxs-lookup"><span data-stu-id="cfed1-126">Click the Range tab.</span></span>
    * <span data-ttu-id="cfed1-127">Диапазоны позволяют ограничить набор результатов только результатами, отвечающими критериям диапазона.</span><span class="sxs-lookup"><span data-stu-id="cfed1-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="cfed1-128">Перейдите на вкладку "Группировка по".</span><span class="sxs-lookup"><span data-stu-id="cfed1-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="cfed1-129">Группировки используются для определения того, как должны отображаться результаты.</span><span class="sxs-lookup"><span data-stu-id="cfed1-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="cfed1-130">Например, группируйте результаты сначала по полу, а затем по возрасту.</span><span class="sxs-lookup"><span data-stu-id="cfed1-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="cfed1-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="cfed1-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cfed1-132">Переместите группировки на строну "Выбранные" и расположите их в требуемом порядке.</span><span class="sxs-lookup"><span data-stu-id="cfed1-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="cfed1-133">Выполнение расчета статистики</span><span class="sxs-lookup"><span data-stu-id="cfed1-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="cfed1-134">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="cfed1-134">Click Execute.</span></span>
    * <span data-ttu-id="cfed1-135">Выберите функцию расчета, которую требуется выполнить над результатами.</span><span class="sxs-lookup"><span data-stu-id="cfed1-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="cfed1-136">Например, рассчитайте средние проценты по анкете для выбранных группировок или просуммируйте баллы по группам результатов для выбранных группировок.</span><span class="sxs-lookup"><span data-stu-id="cfed1-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="cfed1-137">Установите или снимите флажок "Удалить результаты предыдущих поисков".</span><span class="sxs-lookup"><span data-stu-id="cfed1-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="cfed1-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="cfed1-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="cfed1-139">Просмотрите результаты расчета статистики анкетирования.</span><span class="sxs-lookup"><span data-stu-id="cfed1-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="cfed1-140">Щелкните "Результат".</span><span class="sxs-lookup"><span data-stu-id="cfed1-140">Click Result.</span></span>
2. <span data-ttu-id="cfed1-141">Щелкните "Результат".</span><span class="sxs-lookup"><span data-stu-id="cfed1-141">Click Result.</span></span>
3. <span data-ttu-id="cfed1-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cfed1-142">Close the page.</span></span>

