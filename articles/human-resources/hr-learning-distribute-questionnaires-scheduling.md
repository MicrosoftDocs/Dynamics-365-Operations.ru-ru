---
title: Распределение анкет с помощью планирования
description: Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d233938fe553dbd7da7fcc5477097fd885665102
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420304"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="00e77-103">Распределение анкет с помощью планирования</span><span class="sxs-lookup"><span data-stu-id="00e77-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="00e77-104">Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам.</span><span class="sxs-lookup"><span data-stu-id="00e77-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="00e77-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="00e77-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="00e77-106">Создание графика анкетирования</span><span class="sxs-lookup"><span data-stu-id="00e77-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="00e77-107">Перейдите в раздел "Анкета" > "Распределение" > "Графики анкетирования".</span><span class="sxs-lookup"><span data-stu-id="00e77-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="00e77-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="00e77-108">Click New.</span></span>

3. <span data-ttu-id="00e77-109">В поле "Планирование" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00e77-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="00e77-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00e77-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="00e77-111">Настройте планирование как "анонимное", если ответы должны записываться без имен, связанных с ответом.</span><span class="sxs-lookup"><span data-stu-id="00e77-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="00e77-112">Сначала необходимо настроить разрешение анонимных результатов в параметрах управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="00e77-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="00e77-113">В поле "Тип" выберите тип планирования.</span><span class="sxs-lookup"><span data-stu-id="00e77-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="00e77-114">В этом примере будет использоваться тип "Удовлетворенность".</span><span class="sxs-lookup"><span data-stu-id="00e77-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="00e77-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="00e77-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="00e77-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="00e77-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="00e77-117">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="00e77-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="00e77-118">Разверните раздел "Электронная почта для портала самообслуживания сотрудников".</span><span class="sxs-lookup"><span data-stu-id="00e77-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="00e77-119">В поле "Тема" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00e77-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="00e77-120">Пример. Анкета доступная</span><span class="sxs-lookup"><span data-stu-id="00e77-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="00e77-121">В поле "Текст" введите текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="00e77-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="00e77-122">Обратите внимание, что эту переменную можно использовать для подстановки значений в системе.</span><span class="sxs-lookup"><span data-stu-id="00e77-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="00e77-123">Пример. Уважаемый %P%! Выполните вход на портал самообслуживания сотрудников для заполнения анкеты "Здоровье трудовых ресурсов".</span><span class="sxs-lookup"><span data-stu-id="00e77-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="00e77-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="00e77-124">Contoso</span></span>  

12. <span data-ttu-id="00e77-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="00e77-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="00e77-126">Используйте "Сведения о настройке" для выбора анкеты (анкет) для ответов, а также запросы, используемые для выбора респондентов.</span><span class="sxs-lookup"><span data-stu-id="00e77-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="00e77-127">Щелкните "Сведения о настройке".</span><span class="sxs-lookup"><span data-stu-id="00e77-127">Click Setup details.</span></span>

2. <span data-ttu-id="00e77-128">В списке выберите запрос для поиска в системе респондентов для анкеты.</span><span class="sxs-lookup"><span data-stu-id="00e77-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="00e77-129">Пример. Работники</span><span class="sxs-lookup"><span data-stu-id="00e77-129">Example: Workers</span></span>  

3. <span data-ttu-id="00e77-130">Нажмите "Просмотр или изменение запроса" для выбора конкретных людей или изменения запроса для поиска людей, соответствующих конкретным критериям.</span><span class="sxs-lookup"><span data-stu-id="00e77-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="00e77-131">Обратите внимание, что все респонденты должны быть пользователями в системе.</span><span class="sxs-lookup"><span data-stu-id="00e77-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="00e77-132">В списке пометьте строку для "Респондент".</span><span class="sxs-lookup"><span data-stu-id="00e77-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="00e77-133">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="00e77-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="00e77-134">Выберите Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="00e77-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="00e77-135">В списке выберите Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="00e77-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="00e77-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="00e77-136">Click OK.</span></span>

8. <span data-ttu-id="00e77-137">Перейдите на вкладку "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="00e77-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="00e77-138">В дереве разверните узел для типа анкеты "Исследование уровня удовлетворенности".</span><span class="sxs-lookup"><span data-stu-id="00e77-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="00e77-139">В дереве установите флажок "Оценка здоровья трудовых ресурсов".</span><span class="sxs-lookup"><span data-stu-id="00e77-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="00e77-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="00e77-140">Click OK.</span></span>

12. <span data-ttu-id="00e77-141">Щелкните "Запланированный опрос".</span><span class="sxs-lookup"><span data-stu-id="00e77-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="00e77-142">Обратите внимание, что запланированные опросы были созданы для каждого выбранного/опрошенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="00e77-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="00e77-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00e77-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="00e77-144">Запустите расписание анкеты, чтобы сделать анкету доступной для респондентов.</span><span class="sxs-lookup"><span data-stu-id="00e77-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="00e77-145">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="00e77-145">Click Functions.</span></span>

2. <span data-ttu-id="00e77-146">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="00e77-146">Click Start.</span></span>

3. <span data-ttu-id="00e77-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="00e77-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="00e77-148">Отправьте электронное письмо, чтобы проинформировать респондентов о наличии анкеты.</span><span class="sxs-lookup"><span data-stu-id="00e77-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="00e77-149">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="00e77-149">Click Functions.</span></span>

2. <span data-ttu-id="00e77-150">Щелкните "Отправить сообщение электронной почты".</span><span class="sxs-lookup"><span data-stu-id="00e77-150">Click Send email.</span></span>

3. <span data-ttu-id="00e77-151">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="00e77-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="00e77-152">Используйте запланированные опросы для отслеживания, кто должен заполнить анкету.</span><span class="sxs-lookup"><span data-stu-id="00e77-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="00e77-153">Щелкните "Запланированный опрос".</span><span class="sxs-lookup"><span data-stu-id="00e77-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="00e77-154">Удалите оставшийся запланированный опрос, когда вы готовы завершить запланированный опрос.</span><span class="sxs-lookup"><span data-stu-id="00e77-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="00e77-155">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="00e77-155">Click Delete.</span></span>

3. <span data-ttu-id="00e77-156">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="00e77-156">Click Yes.</span></span>

4. <span data-ttu-id="00e77-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00e77-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="00e77-158">Завершите график, когда все респонденты заполнили анкету и (или) все оставшиеся запланированные опросы были удалены.</span><span class="sxs-lookup"><span data-stu-id="00e77-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="00e77-159">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="00e77-159">Click Functions.</span></span>
2. <span data-ttu-id="00e77-160">Щелкните "Готово".</span><span class="sxs-lookup"><span data-stu-id="00e77-160">Click End.</span></span>
3. <span data-ttu-id="00e77-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="00e77-161">Click OK.</span></span>

