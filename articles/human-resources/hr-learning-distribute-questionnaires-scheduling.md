---
title: Распределение анкет с помощью планирования
description: Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 952048ce0a2ac94be70d7bde0dc52610f19151ed
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056308"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="660a2-103">Распределение анкет с помощью планирования</span><span class="sxs-lookup"><span data-stu-id="660a2-103">Distribute questionnaires using scheduling</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="660a2-104">Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам.</span><span class="sxs-lookup"><span data-stu-id="660a2-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="660a2-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="660a2-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="660a2-106">Создание графика анкетирования</span><span class="sxs-lookup"><span data-stu-id="660a2-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="660a2-107">Перейдите в раздел "Анкета" > "Распределение" > "Графики анкетирования".</span><span class="sxs-lookup"><span data-stu-id="660a2-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="660a2-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="660a2-108">Click New.</span></span>

3. <span data-ttu-id="660a2-109">В поле "Планирование" введите значение.</span><span class="sxs-lookup"><span data-stu-id="660a2-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="660a2-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="660a2-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="660a2-111">Настройте планирование как "анонимное", если ответы должны записываться без имен, связанных с ответом.</span><span class="sxs-lookup"><span data-stu-id="660a2-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="660a2-112">Сначала необходимо настроить разрешение анонимных результатов в параметрах управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="660a2-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="660a2-113">В поле "Тип" выберите тип планирования.</span><span class="sxs-lookup"><span data-stu-id="660a2-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="660a2-114">В этом примере будет использоваться тип "Удовлетворенность".</span><span class="sxs-lookup"><span data-stu-id="660a2-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="660a2-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="660a2-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="660a2-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="660a2-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="660a2-117">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="660a2-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="660a2-118">Разверните раздел "Электронная почта для портала самообслуживания сотрудников".</span><span class="sxs-lookup"><span data-stu-id="660a2-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="660a2-119">В поле "Тема" введите значение.</span><span class="sxs-lookup"><span data-stu-id="660a2-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="660a2-120">Пример. Анкета доступная</span><span class="sxs-lookup"><span data-stu-id="660a2-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="660a2-121">В поле "Текст" введите текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="660a2-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="660a2-122">Обратите внимание, что эту переменную можно использовать для подстановки значений в системе.</span><span class="sxs-lookup"><span data-stu-id="660a2-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="660a2-123">Пример. Уважаемый %P%! Выполните вход на портал самообслуживания сотрудников для заполнения анкеты "Здоровье трудовых ресурсов".</span><span class="sxs-lookup"><span data-stu-id="660a2-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="660a2-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="660a2-124">Contoso</span></span>  

12. <span data-ttu-id="660a2-125">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="660a2-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="660a2-126">Используйте "Сведения о настройке" для выбора анкеты (анкет) для ответов, а также запросы, используемые для выбора респондентов.</span><span class="sxs-lookup"><span data-stu-id="660a2-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="660a2-127">Щелкните "Сведения о настройке".</span><span class="sxs-lookup"><span data-stu-id="660a2-127">Click Setup details.</span></span>

2. <span data-ttu-id="660a2-128">В списке выберите запрос для поиска в системе респондентов для анкеты.</span><span class="sxs-lookup"><span data-stu-id="660a2-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="660a2-129">Пример. Работники</span><span class="sxs-lookup"><span data-stu-id="660a2-129">Example: Workers</span></span>  

3. <span data-ttu-id="660a2-130">Нажмите "Просмотр или изменение запроса" для выбора конкретных людей или изменения запроса для поиска людей, соответствующих конкретным критериям.</span><span class="sxs-lookup"><span data-stu-id="660a2-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="660a2-131">Обратите внимание, что все респонденты должны быть пользователями в системе.</span><span class="sxs-lookup"><span data-stu-id="660a2-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="660a2-132">В списке пометьте строку для "Респондент".</span><span class="sxs-lookup"><span data-stu-id="660a2-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="660a2-133">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="660a2-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="660a2-134">Выберите Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="660a2-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="660a2-135">В списке выберите Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="660a2-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="660a2-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="660a2-136">Click OK.</span></span>

8. <span data-ttu-id="660a2-137">Перейдите на вкладку "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="660a2-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="660a2-138">В дереве разверните узел для типа анкеты "Исследование уровня удовлетворенности".</span><span class="sxs-lookup"><span data-stu-id="660a2-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="660a2-139">В дереве установите флажок "Оценка здоровья трудовых ресурсов".</span><span class="sxs-lookup"><span data-stu-id="660a2-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="660a2-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="660a2-140">Click OK.</span></span>

12. <span data-ttu-id="660a2-141">Щелкните "Запланированный опрос".</span><span class="sxs-lookup"><span data-stu-id="660a2-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="660a2-142">Обратите внимание, что запланированные опросы были созданы для каждого выбранного/опрошенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="660a2-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="660a2-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="660a2-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="660a2-144">Запустите расписание анкеты, чтобы сделать анкету доступной для респондентов.</span><span class="sxs-lookup"><span data-stu-id="660a2-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="660a2-145">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="660a2-145">Click Functions.</span></span>

2. <span data-ttu-id="660a2-146">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="660a2-146">Click Start.</span></span>

3. <span data-ttu-id="660a2-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="660a2-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="660a2-148">Отправьте электронное письмо, чтобы проинформировать респондентов о наличии анкеты.</span><span class="sxs-lookup"><span data-stu-id="660a2-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="660a2-149">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="660a2-149">Click Functions.</span></span>

2. <span data-ttu-id="660a2-150">Щелкните "Отправить сообщение электронной почты".</span><span class="sxs-lookup"><span data-stu-id="660a2-150">Click Send email.</span></span>

3. <span data-ttu-id="660a2-151">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="660a2-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="660a2-152">Используйте запланированные опросы для отслеживания, кто должен заполнить анкету.</span><span class="sxs-lookup"><span data-stu-id="660a2-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="660a2-153">Щелкните "Запланированный опрос".</span><span class="sxs-lookup"><span data-stu-id="660a2-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="660a2-154">Удалите оставшийся запланированный опрос, когда вы готовы завершить запланированный опрос.</span><span class="sxs-lookup"><span data-stu-id="660a2-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="660a2-155">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="660a2-155">Click Delete.</span></span>

3. <span data-ttu-id="660a2-156">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="660a2-156">Click Yes.</span></span>

4. <span data-ttu-id="660a2-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="660a2-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="660a2-158">Завершите график, когда все респонденты заполнили анкету и (или) все оставшиеся запланированные опросы были удалены.</span><span class="sxs-lookup"><span data-stu-id="660a2-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="660a2-159">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="660a2-159">Click Functions.</span></span>
2. <span data-ttu-id="660a2-160">Щелкните "Готово".</span><span class="sxs-lookup"><span data-stu-id="660a2-160">Click End.</span></span>
3. <span data-ttu-id="660a2-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="660a2-161">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]