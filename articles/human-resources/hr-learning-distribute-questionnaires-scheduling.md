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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ddad70792c4ebc1785698812fe12406142f07a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790628"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="600f8-103">Распределение анкет с помощью планирования</span><span class="sxs-lookup"><span data-stu-id="600f8-103">Distribute questionnaires using scheduling</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="600f8-104">Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам.</span><span class="sxs-lookup"><span data-stu-id="600f8-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="600f8-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="600f8-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="600f8-106">Создание графика анкетирования</span><span class="sxs-lookup"><span data-stu-id="600f8-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="600f8-107">Перейдите в раздел "Анкета" > "Распределение" > "Графики анкетирования".</span><span class="sxs-lookup"><span data-stu-id="600f8-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="600f8-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="600f8-108">Click New.</span></span>

3. <span data-ttu-id="600f8-109">В поле "Планирование" введите значение.</span><span class="sxs-lookup"><span data-stu-id="600f8-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="600f8-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="600f8-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="600f8-111">Настройте планирование как "анонимное", если ответы должны записываться без имен, связанных с ответом.</span><span class="sxs-lookup"><span data-stu-id="600f8-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="600f8-112">Сначала необходимо настроить разрешение анонимных результатов в параметрах управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="600f8-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="600f8-113">В поле "Тип" выберите тип планирования.</span><span class="sxs-lookup"><span data-stu-id="600f8-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="600f8-114">В этом примере будет использоваться тип "Удовлетворенность".</span><span class="sxs-lookup"><span data-stu-id="600f8-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="600f8-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="600f8-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="600f8-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="600f8-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="600f8-117">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="600f8-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="600f8-118">Разверните раздел "Электронная почта для портала самообслуживания сотрудников".</span><span class="sxs-lookup"><span data-stu-id="600f8-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="600f8-119">В поле "Тема" введите значение.</span><span class="sxs-lookup"><span data-stu-id="600f8-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="600f8-120">Пример. Анкета доступная</span><span class="sxs-lookup"><span data-stu-id="600f8-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="600f8-121">В поле "Текст" введите текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="600f8-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="600f8-122">Обратите внимание, что эту переменную можно использовать для подстановки значений в системе.</span><span class="sxs-lookup"><span data-stu-id="600f8-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="600f8-123">Пример. Уважаемый %P%! Выполните вход на портал самообслуживания сотрудников для заполнения анкеты "Здоровье трудовых ресурсов".</span><span class="sxs-lookup"><span data-stu-id="600f8-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="600f8-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="600f8-124">Contoso</span></span>  

12. <span data-ttu-id="600f8-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="600f8-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="600f8-126">Используйте "Сведения о настройке" для выбора анкеты (анкет) для ответов, а также запросы, используемые для выбора респондентов.</span><span class="sxs-lookup"><span data-stu-id="600f8-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="600f8-127">Щелкните "Сведения о настройке".</span><span class="sxs-lookup"><span data-stu-id="600f8-127">Click Setup details.</span></span>

2. <span data-ttu-id="600f8-128">В списке выберите запрос для поиска в системе респондентов для анкеты.</span><span class="sxs-lookup"><span data-stu-id="600f8-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="600f8-129">Пример. Работники</span><span class="sxs-lookup"><span data-stu-id="600f8-129">Example: Workers</span></span>  

3. <span data-ttu-id="600f8-130">Нажмите "Просмотр или изменение запроса" для выбора конкретных людей или изменения запроса для поиска людей, соответствующих конкретным критериям.</span><span class="sxs-lookup"><span data-stu-id="600f8-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="600f8-131">Обратите внимание, что все респонденты должны быть пользователями в системе.</span><span class="sxs-lookup"><span data-stu-id="600f8-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="600f8-132">В списке пометьте строку для "Респондент".</span><span class="sxs-lookup"><span data-stu-id="600f8-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="600f8-133">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="600f8-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="600f8-134">Выберите Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="600f8-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="600f8-135">В списке выберите Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="600f8-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="600f8-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="600f8-136">Click OK.</span></span>

8. <span data-ttu-id="600f8-137">Перейдите на вкладку "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="600f8-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="600f8-138">В дереве разверните узел для типа анкеты "Исследование уровня удовлетворенности".</span><span class="sxs-lookup"><span data-stu-id="600f8-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="600f8-139">В дереве установите флажок "Оценка здоровья трудовых ресурсов".</span><span class="sxs-lookup"><span data-stu-id="600f8-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="600f8-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="600f8-140">Click OK.</span></span>

12. <span data-ttu-id="600f8-141">Щелкните "Запланированный опрос".</span><span class="sxs-lookup"><span data-stu-id="600f8-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="600f8-142">Обратите внимание, что запланированные опросы были созданы для каждого выбранного/опрошенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="600f8-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="600f8-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="600f8-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="600f8-144">Запустите расписание анкеты, чтобы сделать анкету доступной для респондентов.</span><span class="sxs-lookup"><span data-stu-id="600f8-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="600f8-145">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="600f8-145">Click Functions.</span></span>

2. <span data-ttu-id="600f8-146">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="600f8-146">Click Start.</span></span>

3. <span data-ttu-id="600f8-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="600f8-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="600f8-148">Отправьте электронное письмо, чтобы проинформировать респондентов о наличии анкеты.</span><span class="sxs-lookup"><span data-stu-id="600f8-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="600f8-149">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="600f8-149">Click Functions.</span></span>

2. <span data-ttu-id="600f8-150">Щелкните "Отправить сообщение электронной почты".</span><span class="sxs-lookup"><span data-stu-id="600f8-150">Click Send email.</span></span>

3. <span data-ttu-id="600f8-151">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="600f8-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="600f8-152">Используйте запланированные опросы для отслеживания, кто должен заполнить анкету.</span><span class="sxs-lookup"><span data-stu-id="600f8-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="600f8-153">Щелкните "Запланированный опрос".</span><span class="sxs-lookup"><span data-stu-id="600f8-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="600f8-154">Удалите оставшийся запланированный опрос, когда вы готовы завершить запланированный опрос.</span><span class="sxs-lookup"><span data-stu-id="600f8-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="600f8-155">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="600f8-155">Click Delete.</span></span>

3. <span data-ttu-id="600f8-156">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="600f8-156">Click Yes.</span></span>

4. <span data-ttu-id="600f8-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="600f8-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="600f8-158">Завершите график, когда все респонденты заполнили анкету и (или) все оставшиеся запланированные опросы были удалены.</span><span class="sxs-lookup"><span data-stu-id="600f8-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="600f8-159">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="600f8-159">Click Functions.</span></span>
2. <span data-ttu-id="600f8-160">Щелкните "Готово".</span><span class="sxs-lookup"><span data-stu-id="600f8-160">Click End.</span></span>
3. <span data-ttu-id="600f8-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="600f8-161">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]