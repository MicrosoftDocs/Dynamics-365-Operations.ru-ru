---
title: "Распределение и заполнение анкеты"
description: "В этом разделе объясняется, как распределить составленные анкеты, чтобы они были доступны отдельному пользователю или группе пользователей, которые должны ее заполнить."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a523ff097eedf9a4a2cb0341b3be9d05abfa09fa
ms.openlocfilehash: ea95ab7c68cc8e80d88f0542d9bc14ddaa32f36e
ms.contentlocale: ru-ru
ms.lasthandoff: 01/23/2018

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="d2a23-103">Распределение и заполнение анкеты</span><span class="sxs-lookup"><span data-stu-id="d2a23-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d2a23-104">В этом разделе объясняется, как распределить составленные анкеты, чтобы они были доступны отдельному пользователю или группе пользователей, которые должны ее заполнить.</span><span class="sxs-lookup"><span data-stu-id="d2a23-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="d2a23-105">Существует несколько способов распределить анкету:</span><span class="sxs-lookup"><span data-stu-id="d2a23-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="d2a23-106">Пометить анкету как активную.</span><span class="sxs-lookup"><span data-stu-id="d2a23-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="d2a23-107">Анкета будет доступна всем сотрудникам до тех пор, пока группа анкет не будет настроена для ограничения доступа к анкете.</span><span class="sxs-lookup"><span data-stu-id="d2a23-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="d2a23-108">Присвоить права на группу анкет.</span><span class="sxs-lookup"><span data-stu-id="d2a23-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="d2a23-109">После этого анкета станет доступна всем членам выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="d2a23-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="d2a23-110">Создать запланированные опросы.</span><span class="sxs-lookup"><span data-stu-id="d2a23-110">Create planned answer sessions.</span></span> <span data-ttu-id="d2a23-111">Анкета будет доступна только определенному сотруднику.</span><span class="sxs-lookup"><span data-stu-id="d2a23-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="d2a23-112">Создать график.</span><span class="sxs-lookup"><span data-stu-id="d2a23-112">Create a schedule.</span></span> <span data-ttu-id="d2a23-113">Анкета станет доступна нескольким людям.</span><span class="sxs-lookup"><span data-stu-id="d2a23-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="d2a23-114">Пометка анкеты как активной</span><span class="sxs-lookup"><span data-stu-id="d2a23-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="d2a23-115">Задав в поле **Активно** значение **Да** на странице **Анкеты**, вы предоставляете доступ для заполнения анкеты всем сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="d2a23-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="d2a23-116">Респонденты могут заполнить анкету несколько раз.</span><span class="sxs-lookup"><span data-stu-id="d2a23-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="d2a23-117">Эта возможность полезна, если вы хотите получать отзывы на протяжении всего года.</span><span class="sxs-lookup"><span data-stu-id="d2a23-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="d2a23-118">Например, вы можете создать анкету, в которой сотрудники смогут оставлять отзывы о качестве обедов в кафетерии.</span><span class="sxs-lookup"><span data-stu-id="d2a23-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="d2a23-119">Группы анкет</span><span class="sxs-lookup"><span data-stu-id="d2a23-119">Questionnaire groups</span></span>
<span data-ttu-id="d2a23-120">Можно настроить группы анкет, а затем включить респондентов, для которых предназначена анкета.</span><span class="sxs-lookup"><span data-stu-id="d2a23-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="d2a23-121">Группы анкет можно создавать на следующих страницах.</span><span class="sxs-lookup"><span data-stu-id="d2a23-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="d2a23-122">**Группы анкет** — только отдельные люди в группе анкет могут заполнять выбранную анкету.</span><span class="sxs-lookup"><span data-stu-id="d2a23-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="d2a23-123">Например, если вашей аудиторией являются подрядчики, можно создать группу анкет, относящуюся к этим респондентам.</span><span class="sxs-lookup"><span data-stu-id="d2a23-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="d2a23-124">**Члены группы анкет** — можно добавлять людей в группы анкет.</span><span class="sxs-lookup"><span data-stu-id="d2a23-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="d2a23-125">Чтобы назначить группу анкет анкете, на странице **Анкеты** щелкните **Права доступа**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="d2a23-126">После сохранения анкеты как активной члены группы анкет смогут заполнить анкету.</span><span class="sxs-lookup"><span data-stu-id="d2a23-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="d2a23-127">Эта возможность полезна, если вы хотите протестировать анкету на определенной группе людей, прежде чем предлагать ее более широкой группе, или если вы хотите нацелить анкету на очень специфическую аудиторию.</span><span class="sxs-lookup"><span data-stu-id="d2a23-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="d2a23-128">Запланированные опросы в анкете</span><span class="sxs-lookup"><span data-stu-id="d2a23-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="d2a23-129">Запланированные опросы — это составленные анкеты, для которых выбраны респонденты.</span><span class="sxs-lookup"><span data-stu-id="d2a23-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="d2a23-130">**Примечание.** Чтобы настроить запланированный опрос, сначала следует составить анкету.</span><span class="sxs-lookup"><span data-stu-id="d2a23-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="d2a23-131">На странице **Запланированный опрос** можно создать запланированный опрос для отдельного сотрудника.</span><span class="sxs-lookup"><span data-stu-id="d2a23-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="d2a23-132">В списке на странице отображаются все запланированные анкеты.</span><span class="sxs-lookup"><span data-stu-id="d2a23-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="d2a23-133">Запланированные опросы применяются также на странице **Графики анкетирования**, где можно планировать анкеты для многих людей.</span><span class="sxs-lookup"><span data-stu-id="d2a23-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="d2a23-134">Сотрудники</span><span class="sxs-lookup"><span data-stu-id="d2a23-134">Employees</span></span>
-   <span data-ttu-id="d2a23-135">Слушатели курса</span><span class="sxs-lookup"><span data-stu-id="d2a23-135">Course participants</span></span>
-   <span data-ttu-id="d2a23-136">Подразделения</span><span class="sxs-lookup"><span data-stu-id="d2a23-136">Organizational units</span></span>

<span data-ttu-id="d2a23-137">Каждый человек может заполнить анкету только один раз.</span><span class="sxs-lookup"><span data-stu-id="d2a23-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="d2a23-138">Планирование анкетирования</span><span class="sxs-lookup"><span data-stu-id="d2a23-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="d2a23-139">Дополнительно можно запланировать анкетирование нескольких респондентов.</span><span class="sxs-lookup"><span data-stu-id="d2a23-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="d2a23-140">Типы планирования</span><span class="sxs-lookup"><span data-stu-id="d2a23-140">Planning types</span></span>

<span data-ttu-id="d2a23-141">Типы планирования необходимы для формирования расписания запланированных опросов для нескольких респондентов.</span><span class="sxs-lookup"><span data-stu-id="d2a23-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="d2a23-142">Типы планирования используются для классификации расписаний анкетирования.</span><span class="sxs-lookup"><span data-stu-id="d2a23-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="d2a23-143">Например, можно планировать анкеты для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="d2a23-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="d2a23-144">Оценка</span><span class="sxs-lookup"><span data-stu-id="d2a23-144">Evaluation</span></span>
-   <span data-ttu-id="d2a23-145">Исследование</span><span class="sxs-lookup"><span data-stu-id="d2a23-145">Survey</span></span>
-   <span data-ttu-id="d2a23-146">Тестирование</span><span class="sxs-lookup"><span data-stu-id="d2a23-146">Testing</span></span>

<span data-ttu-id="d2a23-147">Типы планирования для расписания анкетирования можно задать на странице **Графики анкетирования**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="d2a23-148">Типы ссылок для анкеты</span><span class="sxs-lookup"><span data-stu-id="d2a23-148">Reference types for questionnaire</span></span>

<span data-ttu-id="d2a23-149">Вы можете использовать типы ссылок, чтобы вводить критерии для респондентов, которых вы можете выбрать для планирования анкеты.</span><span class="sxs-lookup"><span data-stu-id="d2a23-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="d2a23-150">Используйте страницу **Типы ссылок**, чтобы настроить типы ссылок для анкеты.</span><span class="sxs-lookup"><span data-stu-id="d2a23-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="d2a23-151">Каждый тип ссылки соответствует таблице в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d2a23-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d2a23-152">При создании планов анкет можно указывать отдельные записи в таблице или диапазоне таблиц, с которыми будет связана анкета.</span><span class="sxs-lookup"><span data-stu-id="d2a23-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="d2a23-153">Например, если вы выберете таблицу "Курсы", вы можете указать, для какого конкретно курса будет предназначена анкета.</span><span class="sxs-lookup"><span data-stu-id="d2a23-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="d2a23-154">Когда вы настроите ссылки для таблицы "Курсы", некоторые поля и кнопки на странице **Курсы** станут доступными.</span><span class="sxs-lookup"><span data-stu-id="d2a23-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="d2a23-155">Графики анкетирования</span><span class="sxs-lookup"><span data-stu-id="d2a23-155">Questionnaire schedules</span></span>

<span data-ttu-id="d2a23-156">Графики анкетирования можно использовать для создания нескольких запланированных опросов для группы пользователей на основании типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="d2a23-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="d2a23-157">Создайте график на странице **Графики анкетирования**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="d2a23-158">Выберите тип планирования для классификации графика и выберите тип ссылки, который следует использовать для запроса системы относительно определенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d2a23-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="d2a23-159">Например, если задать тип ссылки как таблицу "Курсы", можно выбрать определенный курс в поле **Ссылка**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="d2a23-160">Щелкните **Сведения о настройке**, чтобы выбрать анкету и другие критерии.</span><span class="sxs-lookup"><span data-stu-id="d2a23-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="d2a23-161">Например, укажите имя инструктора как критерий, если анкета является оценкой инструктора.</span><span class="sxs-lookup"><span data-stu-id="d2a23-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="d2a23-162">По завершении ввода сведений настройки система создаст запланированные сеансы опроса для пользователей, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="d2a23-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="d2a23-163">Щелкните **Запланированные опросы**, чтобы осмотреть сеансы ответов для графика.</span><span class="sxs-lookup"><span data-stu-id="d2a23-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="d2a23-164">Можно вручную создать дополнительные запланированные опросы или удалить запланированные опросы, на которые получены ответы.</span><span class="sxs-lookup"><span data-stu-id="d2a23-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="d2a23-165">Щелкните **Функции** &gt; **Начать**, чтобы сделать анкету доступной для пользователей в связанных запланированных опросах.</span><span class="sxs-lookup"><span data-stu-id="d2a23-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="d2a23-166">Щелкните **Ответы**, чтобы просмотреть заполненные ответы на анкету.</span><span class="sxs-lookup"><span data-stu-id="d2a23-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="d2a23-167">Также можно скопировать параметры графика анкеты, запланированные опросы и ответы в новый график анкеты.</span><span class="sxs-lookup"><span data-stu-id="d2a23-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="d2a23-168">Уведомление респондентов о доступных для них анкетах</span><span class="sxs-lookup"><span data-stu-id="d2a23-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="d2a23-169">При распространении анкет необходимо уведомить респондентов о том, что им доступны анкеты.</span><span class="sxs-lookup"><span data-stu-id="d2a23-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="d2a23-170">Уведомление респондентов о запланированном опросе</span><span class="sxs-lookup"><span data-stu-id="d2a23-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="d2a23-171">Если вы используете запланированный опрос, необходимо уведомить респондента напрямую, например по телефону или электронной почте.</span><span class="sxs-lookup"><span data-stu-id="d2a23-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="d2a23-172">Уведомление респондентов о планировании</span><span class="sxs-lookup"><span data-stu-id="d2a23-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="d2a23-173">Страница **Графики анкетирования** позволяет подготовить и отправить электронные письма всем респондентам, назначенным для опроса.</span><span class="sxs-lookup"><span data-stu-id="d2a23-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="d2a23-174">Введите текст сообщения электронной почты на вкладке **Электронная почта для портала самообслуживания сотрудников**. После запуска графика щелкните **Функции** &gt; **Отправить сообщение электронной почты**, чтобы создать и отправить сообщение электронной почты респондентам.</span><span class="sxs-lookup"><span data-stu-id="d2a23-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="d2a23-175">После этого респонденты смогут войти на веб-сайт и заполнить анкету.</span><span class="sxs-lookup"><span data-stu-id="d2a23-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="d2a23-176">**Примечание.** Прежде чем вы можете использовать функциональность электронной почты, администратор ИТ должен ввести параметры электронной почты на странице **Параметры электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="d2a23-177">Завершение запланированного анкетирования</span><span class="sxs-lookup"><span data-stu-id="d2a23-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="d2a23-178">Можно завершить запланированную анкету, после того как все респонденты завершили заданные сеансы опроса.</span><span class="sxs-lookup"><span data-stu-id="d2a23-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="d2a23-179">После завершения запланированного анкетирования, его настройки не могут копироваться в новый график.</span><span class="sxs-lookup"><span data-stu-id="d2a23-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="d2a23-180">**Примечание.** Если один или несколько респондентов не заполнили анкету, а требуется закончить планирование, удалите сначала соответствующих респондентов из списка, который находится на странице **Запланированный опрос**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="d2a23-181">Затем можно завершить планирование.</span><span class="sxs-lookup"><span data-stu-id="d2a23-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="d2a23-182">Заполнение анкет</span><span class="sxs-lookup"><span data-stu-id="d2a23-182">Completing questionnaires</span></span>
<span data-ttu-id="d2a23-183">После составления и распространения анкеты выбранные респонденты могут ее заполнить.</span><span class="sxs-lookup"><span data-stu-id="d2a23-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="d2a23-184">Заполните анкеты, доступные в двух местах:</span><span class="sxs-lookup"><span data-stu-id="d2a23-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="d2a23-185">В области перехода щелкните **Анкеты** &gt; **Распределить** &gt; **Заполнение анкеты**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="d2a23-186">На портале самообслуживания сотрудников щелкните **Анкеты для заполнения**.</span><span class="sxs-lookup"><span data-stu-id="d2a23-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="d2a23-187">Анкеты могут быть сделаны доступными для всех пользователей сети, либо для всех пользователей в сети.</span><span class="sxs-lookup"><span data-stu-id="d2a23-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="d2a23-188">См. также</span><span class="sxs-lookup"><span data-stu-id="d2a23-188">See also</span></span>
--------

[<span data-ttu-id="d2a23-189">Создание анкет</span><span class="sxs-lookup"><span data-stu-id="d2a23-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="d2a23-190">Использование анкет</span><span class="sxs-lookup"><span data-stu-id="d2a23-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="d2a23-191">Просмотр и оценка результатов анкет</span><span class="sxs-lookup"><span data-stu-id="d2a23-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



