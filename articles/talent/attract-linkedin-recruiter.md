---
title: Поиск кандидатов с помощью LinkedIn Recruiter в Attract
description: Используйте интеграцию LinkedIn, предоставляемую Microsoft Dynamics 365 Talent - Attract, для поиска кандидатов на вакансии с помощью LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528277"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a><span data-ttu-id="a7d6d-103">Поиск кандидатов с помощью LinkedIn Recruiter в Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-103">Source candidates with LinkedIn Recruiter in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7d6d-104">LinkedIn — это крупнейшая в мире профессиональная сеть в Интернете, предоставляющая вам доступ к лучшим специалистам в мире.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-104">LinkedIn is the world's largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="a7d6d-105">Microsoft Dynamics 365 Talent: Attract позволяет искать кандидатов непосредственно из LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-105">Microsoft Dynamics 365 Talent: Attract lets you source candidates directly from LinkedIn.</span></span> <span data-ttu-id="a7d6d-106">Таким образом, легче будет найти кандидата, необходимого для заполнения открытых вакансий.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-106">Therefore, it's easier than ever to find the talent that you need to fill your open positions.</span></span> <span data-ttu-id="a7d6d-107">После настройки подключения с LinkedIn через Attract можно просматривать потенциальных кандидатов из LinkedIn для должностей и экспортировать их в Attract всего одним щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-107">After you set up your connection with LinkedIn through Attract, you can view potential LinkedIn candidates for your positions and export them into Attract with just one click.</span></span>

<span data-ttu-id="a7d6d-108">Если у вас нет такой возможности, обратитесь к администратору. Прежде чем вы сможете воспользоваться преимуществами LinkedIn Recruiter из Attract, администратор должен [настроить интеграцию с LinkedIn](./attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="a7d6d-108">If you don't seem to have this capability, contact your admin. Before you can take advantage of LinkedIn Recruiter from Attract, your admin must [set up integration with LinkedIn](./attract-admin-linkedin.md).</span></span> <span data-ttu-id="a7d6d-109">Затем можно настроить подключение к LinkedIn Recruiter и начать поиск кандидатов.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-109">You can then set up your connection with LinkedIn Recruiter and start finding candidates.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a7d6d-110">По состоянию на 1 июля 2020 г. LinkedIn больше не поддерживает Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-110">As of July 1, 2020, LinkedIn no longer supports Internet Explorer 11.</span></span> <span data-ttu-id="a7d6d-111">Пользователи все еще могут получить доступ к LinkedIn из Internet Explorer 11, но им будет предложено обновиться или использовать другой браузер.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-111">Users can still access LinkedIn with Internet Explorer 11, but will be prompted to upgrade or use a different browser.</span></span> <span data-ttu-id="a7d6d-112">Дополнительные сведения см. в разделе [Поддерживаемые интернет-браузеры для LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span><span class="sxs-lookup"><span data-stu-id="a7d6d-112">For more information, see [Supported Internet Browsers for LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span></span>

## <a name="set-up-your-connection-with-linkedin-recruiter"></a><span data-ttu-id="a7d6d-113">Настройка подключения к LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="a7d6d-113">Set up your connection with LinkedIn Recruiter</span></span>

<span data-ttu-id="a7d6d-114">Прежде чем начать работать с LinkedIn Recruiter через Attract, необходимо настроить подключение к LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-114">Before you can start working with LinkedIn Recruiter through Attract, you must set up your connection with LinkedIn Recruiter.</span></span> <span data-ttu-id="a7d6d-115">Для этого шага требуются учетные данные пользователя LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-115">For this step, you need your LinkedIn Recruiter credentials.</span></span>

1. <span data-ttu-id="a7d6d-116">Выберите кнопку **Настройки** (значок шестеренки) в верхнем правом углу страницы.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-116">Select the **Settings** button (gear icon) in the upper-right corner of the page.</span></span>
2. <span data-ttu-id="a7d6d-117">Выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-117">Select **User settings**.</span></span>
3. <span data-ttu-id="a7d6d-118">На вкладке **Подключения** выберите **Подключить** рядом с **LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-118">On the **Connections** tab, select **Connect** next to **LinkedIn**.</span></span> <span data-ttu-id="a7d6d-119">Следуйте указаниям, предоставленным LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-119">Follow the instructions that are provided by LinkedIn.</span></span>

    ![[<span data-ttu-id="a7d6d-120">Настройка подключения к LinkedIn Recruiter из Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-120">Set up connection to LinkedIn Recruiter from Attract</span></span>](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a><span data-ttu-id="a7d6d-121">Просмотр кандидатов LinkedIn в Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-121">View LinkedIn candidates in Attract</span></span>

<span data-ttu-id="a7d6d-122">После подключения к LinkedIn Recruiter можно просматривать профили LinkedIn в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-122">After you're connected to LinkedIn Recruiter, you can view candidates' LinkedIn profiles in Attract.</span></span>

>[!NOTE]
><span data-ttu-id="a7d6d-123">Если вам назначено рабочее место Recruiter, вы можете видеть полную информацию о кандидатах.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-123">If you have a Recruiter seat assigned to you, you can see the candidates' full information.</span></span><br><br>
><span data-ttu-id="a7d6d-124">Если у вас есть рабочее место менеджера по найму персонала или вам не назначено рабочее место, обязательно выйдите из LinkedIn или LinkedIn Recruiter перед переходом на вкладку LinkedIn для кандидата в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-124">If you have a Hiring Manager seat or no seat assigned to you, be sure to sign out of LinkedIn or LinkedIn Recruiter before navigating to the LinkedIn tab for a candidate in Attract.</span></span> <span data-ttu-id="a7d6d-125">Вы сможете просмотреть основные данные открытого профиля кандидата, например, его имя и фамилию.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-125">You'll be able to see the candidate's basic public profile data, such as their first and last name.</span></span>

1. <span data-ttu-id="a7d6d-126">В Attract выберите **Должности** или **Кадровые пулы** слева, затем выберите соискателя.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-126">In Attract, select **Jobs** or **Talent pools** on the left, and then select an applicant.</span></span>

    ![[<span data-ttu-id="a7d6d-127">Просмотр кандидатов LinkedIn в Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-127">View LinkedIn candidates in Attract</span></span>](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. <span data-ttu-id="a7d6d-128">В профиле кандидата выберите вкладку **LinkedIn**. Можно просмотреть профиль кандидата и историю InMail.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-128">In the candidate's profile, select the **LinkedIn** tab. You can view the candidate's profile and InMail history.</span></span>

   ![Просмотр данных LinkedIn для кандидата](./media/attract-candidate-linkedin-tab.png)

<span data-ttu-id="a7d6d-130">Отсюда можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a7d6d-130">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="a7d6d-131">Выберите вкладку **Действия по набору персонала** для просмотра:</span><span class="sxs-lookup"><span data-stu-id="a7d6d-131">Select the **Recruiting activities** tab to view:</span></span>
   
   - <span data-ttu-id="a7d6d-132">Заметки специалиста по найму (открытые и частные).</span><span class="sxs-lookup"><span data-stu-id="a7d6d-132">Recruiter notes (both public and private).</span></span> <span data-ttu-id="a7d6d-133">По умолчанию заметки являются частными и видны только владельцу заметок.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-133">By default, notes are private and only visible to the owner of the notes.</span></span>
   - <span data-ttu-id="a7d6d-134">Действие InMail (но не содержимое InMail).</span><span class="sxs-lookup"><span data-stu-id="a7d6d-134">InMail activity (but not the InMail content).</span></span> <span data-ttu-id="a7d6d-135">Прокрутите вниз до конца страницы, чтобы просмотреть обмен сообщениями InMail с кандидатом и просмотреть других пользователей в вашей организации, которые взаимодействуют с вашим кандидатом.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-135">Scroll to the bottom of the page to view the InMail exchange with your prospect and view other users in your organization who are interacting with your prospect.</span></span>
   - <span data-ttu-id="a7d6d-136">Действие по отклонению кандидата</span><span class="sxs-lookup"><span data-stu-id="a7d6d-136">Candidate rejection activity</span></span>

- <span data-ttu-id="a7d6d-137">Выберите **Отправить InMail**, чтобы отправить InMail, не покидая Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-137">Select **Send InMail** to send InMail without having to leave Attract.</span></span>

- <span data-ttu-id="a7d6d-138">Выберите **Сохранить в задании**, чтобы сохранить задание, не покидая Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-138">Select **Save to a job** to save the job without leaving Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="a7d6d-139">Профиль LinkedIn для кандидата будет отображаться в Attract, когда информация в Attract о кандидате соответствует информации в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-139">A candidate's LinkedIn profile will display in Attract when the candidate's Attract information matches the LinkedIn information.</span></span> <span data-ttu-id="a7d6d-140">Используются следующие правила сопоставления:</span><span class="sxs-lookup"><span data-stu-id="a7d6d-140">Here are the matching rules that are used:</span></span>
> 
> 1. <span data-ttu-id="a7d6d-141">Если адрес электронной почты и кода участника LinkedIn совпадают в Attract и LinkedIn, будет показан профиль кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-141">If the email address and LinkedIn member ID match in Attract and LinkedIn, the candidate's profile is shown.</span></span> <span data-ttu-id="a7d6d-142">Кандидаты по-прежнему имеют возможность установить или удалить связь профиля LinkedIn из Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-142">Candidates still have the option to link or unlink their LinkedIn profile from Attract.</span></span>
> 2. <span data-ttu-id="a7d6d-143">Если адрес электронной почты или код участника LinkedIn не совпадает, отображается список возможных кандидатов.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-143">If the email address or LinkedIn member ID doesn't match, you see a list of possible candidates.</span></span> <span data-ttu-id="a7d6d-144">Затем можно выбрать кандидата в списке и связать профиль.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-144">You can then select a candidate in the list and link the profile.</span></span>
> 3. <span data-ttu-id="a7d6d-145">Если нет удачных совпадений, появится сообщение о том, что совпадений не найдено.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-145">If there are no good matches, you're notified that no match was found.</span></span>

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a><span data-ttu-id="a7d6d-146">Экспорт кандидатов LinkedIn в Attract одним щелчком</span><span class="sxs-lookup"><span data-stu-id="a7d6d-146">Export LinkedIn candidates to Attract with one click</span></span>

<span data-ttu-id="a7d6d-147">При просмотре кандидатов в LinkedIn Recruiter можно экспортировать их в должности, которые в данный момент открыты в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-147">While you're reviewing candidates in LinkedIn Recruiter, you can export them to jobs that you currently have open in Attract.</span></span> <span data-ttu-id="a7d6d-148">Для этого шага вам необходимо иметь в Attract разрешения нанимателя или специалиста по комплектации штата.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-148">For this step, you need Recruiter or Hiring Manager permissions in Attract.</span></span> <span data-ttu-id="a7d6d-149">Дополнительные сведения о ролях в Attract см. в разделе [Безопасность и управление ролями в Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span><span class="sxs-lookup"><span data-stu-id="a7d6d-149">For more information about roles in Attract, see [Security and role management in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span></span>

<span data-ttu-id="a7d6d-150">Кроме того, необходимо убедиться, что должность находится на этапе соискателя.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-150">You must also make sure that the job has a Prospect stage.</span></span> <span data-ttu-id="a7d6d-151">Подробнее см. в разделе [Действие подбора соискателей](./activities-attract.md#prospect-activity).</span><span class="sxs-lookup"><span data-stu-id="a7d6d-151">For more information, see [Prospect activity](./activities-attract.md#prospect-activity).</span></span>

1. <span data-ttu-id="a7d6d-152">В Attract создайте должность, назначьте соответствующие роли и активируйте должность.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-152">In Attract, create a job, assign the appropriate roles, and activate the job.</span></span>
2. <span data-ttu-id="a7d6d-153">В LinkedIn Recruiter найдите подходящего кандидата на должность и перейдите к профилю кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-153">In LinkedIn Recruiter, find a good candidate for the job, and go to the candidate's profile.</span></span>
3. <span data-ttu-id="a7d6d-154">В поле поиска должности в карточке контакта найдите должность по названию или коду должности, которая была активирована в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-154">In the job search box in the contact card, find the job by using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="a7d6d-155">Если не удается найти должность, выберите **Изменить ATS** для поиска соответствующего экземпляра Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-155">If you can't find the job, select **Change ATS** to find the correct Attract instance.</span></span>
4. <span data-ttu-id="a7d6d-156">Выберите должность, затем выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-156">Select the job, and then select **Export**.</span></span>
5. <span data-ttu-id="a7d6d-157">В Attract откройте должность.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-157">In Attract, open the job.</span></span> <span data-ttu-id="a7d6d-158">Экспортированный кандидат появится на вкладке **Соискатель** должности.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-158">The exported candidate will appear on the **Prospect** tab of the job.</span></span>

## <a name="view-attract-information-in-linkedin-recruiter"></a><span data-ttu-id="a7d6d-159">Просмотр информации Attract в LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="a7d6d-159">View Attract information in LinkedIn Recruiter</span></span>

<span data-ttu-id="a7d6d-160">В LinkedIn Recruiter можно отслеживать, подавал ли кандидат заявления на другие должности в вашей организации,посмотреть кандидатов на различных стадиях подачи заявления на должность, а также просмотреть отзывы и комментарии из Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-160">In LinkedIn Recruiter, you can track whether a candidate applied to other jobs in your organization, see where the candidate is in the various stages for job applications, and view feedback and comments from Attract.</span></span>

1. <span data-ttu-id="a7d6d-161">Откройте LinkedIn Recruiter и выберите профиль кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-161">Open LinkedIn Recruiter, and select a candidate profile.</span></span>
2. <span data-ttu-id="a7d6d-162">Наведите курсор на **В ATS**.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-162">Hover over **In ATS**.</span></span>
3. <span data-ttu-id="a7d6d-163">Выберите один из следующих параметров для просмотра сведений о кандидате, которые хранятся в Attract:</span><span class="sxs-lookup"><span data-stu-id="a7d6d-163">Select any of the following options to view the candidate information that is stored in Attract:</span></span>

    - <span data-ttu-id="a7d6d-164">**Должности и статусы** — просмотр должностей, к которым относится кандидат, самый последний статус и прогресс кандидата по каждой должности.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-164">**Jobs & Statuses** – See jobs that the candidate is part of, the latest status, and how the candidate is progressing for each job.</span></span>
    - <span data-ttu-id="a7d6d-165">**Отзыв о собеседовании** — просмотр отзыва, который проводившие собеседование сотрудники представили в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-165">**Interview Feedback** – See feedback that interviewers have submitted in Attract.</span></span>
    - <span data-ttu-id="a7d6d-166">**Примечания** — просмотр всех примечаний, которые были введены для этого кандидата в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-166">**Notes** – See any notes that have been entered for this candidate in Attract.</span></span>

    ![[<span data-ttu-id="a7d6d-167">Просмотр информации Attract из LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="a7d6d-167">View Attract information from LinkedIn Recruiter</span></span>](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> <span data-ttu-id="a7d6d-168">Данные о кандидате и заявлении о приеме на работу не будут синхронизированы с LinkedIn Recruiter, если кандидат не прошел далее стадии перспективного кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-168">Candidate and application data won't be synced with LinkedIn Recruiter if the candidate hasn't moved past the Prospect stage.</span></span>

## <a name="view-linkedin-talent-pools"></a><span data-ttu-id="a7d6d-169">Просмотр кадровых пулов LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a7d6d-169">View LinkedIn talent pools</span></span>

<span data-ttu-id="a7d6d-170">Если кандидаты соглашаются предоставить общий доступ к своим профилям LinkedIn любым пользователям вашей организации, новая запись создается в Attract.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-170">If candidates agree to share their LinkedIn profiles with any user in your organization, a new candidate record is created in Attract.</span></span> <span data-ttu-id="a7d6d-171">Эти кандидаты затем появятся в созданном системой кадровом пуле LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-171">These candidates then appear in a system-created LinkedIn talent pool.</span></span>

1. <span data-ttu-id="a7d6d-172">В Attract выберите **Кадровые пулы** в левой части.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-172">In Attract, select **Talent pools** on the left.</span></span>
2. <span data-ttu-id="a7d6d-173">Выберите кадровый пул LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-173">Select the LinkedIn talent pool.</span></span> <span data-ttu-id="a7d6d-174">Будет отображен список кандидатов и их профили-заготовки из LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-174">You will see a list of candidates and their stub profiles from LinkedIn.</span></span> <span data-ttu-id="a7d6d-175">Профили-заготовки содержат имя и фамилию кандидата и адрес электронной почты, если кандидат решил поделиться ими.</span><span class="sxs-lookup"><span data-stu-id="a7d6d-175">Stub profiles contain the candidate's first and last names and email address, if the candidate chose to share it.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7d6d-176">См. также</span><span class="sxs-lookup"><span data-stu-id="a7d6d-176">See also</span></span>

[<span data-ttu-id="a7d6d-177">Вопросы и ответы по интеграции Attract с LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a7d6d-177">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="a7d6d-178">Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-178">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="a7d6d-179">Создание, утверждение и публикация вакансий в Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-179">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="a7d6d-180">Публикация вакансий в LinkedIn из Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-180">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="a7d6d-181">Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="a7d6d-181">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
