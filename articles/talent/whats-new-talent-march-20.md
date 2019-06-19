---
title: Что нового и что изменилось в Dynamics 365 for Talent (20 марта 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d69294b64c841c5486d694b129cf6c0f26fd93fd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518944"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-20-2019"></a><span data-ttu-id="c03da-103">Что нового и что изменилось в Dynamics 365 for Talent (20 марта 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="c03da-103">What's new or changed in Dynamics 365 for Talent (March 20, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c03da-104">В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="c03da-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c03da-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="c03da-105">Changes in Attract</span></span>

### <a name="setting-the-audience-on-activities"></a><span data-ttu-id="c03da-106">Настройка аудитории для мероприятий</span><span class="sxs-lookup"><span data-stu-id="c03da-106">Setting the audience on activities</span></span>
<span data-ttu-id="c03da-107">Действия в системе теперь могут иметь определенную аудиторию.</span><span class="sxs-lookup"><span data-stu-id="c03da-107">Activities in the system can now have the audience defined.</span></span> <span data-ttu-id="c03da-108">Действий, связанные с процессом (например, собеседование, расписание, обратная связь и EEO), можно настроить для всех кандидатов, кандидатов внутренних и внешних кандидатов.</span><span class="sxs-lookup"><span data-stu-id="c03da-108">Process-related activities (such as Interview, Schedule, Feedback, and EEO) can be set to All candidates, Internal candidates, and External candidates.</span></span> <span data-ttu-id="c03da-109">Пользовательские действия, например, такие как Microsoft Forms, видео YouTube или веб-содержимое, могут доставляться всем кандидатам, внутренним кандидатам, внешним кандидатам или группе по найму на работу.</span><span class="sxs-lookup"><span data-stu-id="c03da-109">Custom activities, such as Microsoft Forms, YouTube videos, and web content can be delivered to All candidates, Internal candidates, External candidates, or the hiring team.</span></span>  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a><span data-ttu-id="c03da-110">Улучшение возможности обнаружения вакансий на сайте карьеры: оптимизация для поисковых систем</span><span class="sxs-lookup"><span data-stu-id="c03da-110">Improve career site job discoverability: Search Engine Optimization</span></span>
<span data-ttu-id="c03da-111">Эта функция позволяет поисковым модулям находить и индексировать объявления о вакансиях на сайте карьеры Attract.</span><span class="sxs-lookup"><span data-stu-id="c03da-111">This feature enables search engine crawlers to reach and index job postings on the Attract career site.</span></span> <span data-ttu-id="c03da-112">Это помогает кандидатам находить вакансии, размещенные на сайте карьеры Attract, с помощью популярных поисковых модулей.</span><span class="sxs-lookup"><span data-stu-id="c03da-112">This helps candidates find jobs posted to the Attract career site using popular search engines.</span></span>

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a><span data-ttu-id="c03da-113">Отображение подсказки по учетным данным для кандидатов, которые забыли свои учетные данные</span><span class="sxs-lookup"><span data-stu-id="c03da-113">Show login hint to candidates who forgot their credentials</span></span>
<span data-ttu-id="c03da-114">Если кандидат забыл учетные данные социальной сети, которые они использовали для подачи заявления на вакансию при открытии ссылки, которая была сохранена или отправлена им по электронной почте, теперь они увидят подсказку с именем поставщика и именем пользователя (запутанным).</span><span class="sxs-lookup"><span data-stu-id="c03da-114">If a candidate forgot the social credentials they used to apply to a job while opening a link that was saved or emailed to them, they will now see a hint with the provider name and user name (obfuscated).</span></span> <span data-ttu-id="c03da-115">Это помогает им использовать правильные учетные данные для доступа к своим заявлениям о приеме на работу.</span><span class="sxs-lookup"><span data-stu-id="c03da-115">This helps them use the correct credentials to access their job application.</span></span>

### <a name="help-internal-candidates-explore-internal-jobs"></a><span data-ttu-id="c03da-116">Помощь внутренним кандидатам исследовать внутренние должности</span><span class="sxs-lookup"><span data-stu-id="c03da-116">Help internal candidates explore internal jobs</span></span>
<span data-ttu-id="c03da-117">Проблема устранена, где внешние кандидаты могут видеть имя агента по найму или менеджера по найму для должности.</span><span class="sxs-lookup"><span data-stu-id="c03da-117">An issue has been fixed where external candidates could see the name of the recruiter or the hiring manager of a job.</span></span> <span data-ttu-id="c03da-118">Теперь только внутренние кандидатов могут увидеть членов группы найма на работу для должности.</span><span class="sxs-lookup"><span data-stu-id="c03da-118">Now only internal candidates can see the hiring team members for a job.</span></span> <span data-ttu-id="c03da-119">Также легче для внутренних кандидатов просматривать только внутренние должности и подавать заявления на них.</span><span class="sxs-lookup"><span data-stu-id="c03da-119">It’s also easier for internal candidates to view and apply to internal only jobs.</span></span> <span data-ttu-id="c03da-120">Когда кандидат пытается получить доступ по ссылке для просмотра или подачи заявления только на внутреннюю должность, им придется выполнить проверку подлинности с учетными данными Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c03da-120">When a candidate tries to access the link to view or apply to an internal-only job, they are forced to authenticate with Azure Active Directory credentials.</span></span> <span data-ttu-id="c03da-121">Внутренние кандидаты также должны иметь возможность обращаться к участникам команды найма на работу, чтобы выразить заинтересованность или получить дополнительные сведения о должности.</span><span class="sxs-lookup"><span data-stu-id="c03da-121">Internal candidates also have the ability to contact the hiring team member to express interest in or to know more about the job.</span></span> <span data-ttu-id="c03da-122">Эта возможность доступна для всех должностей только для внутренние кандидатов.</span><span class="sxs-lookup"><span data-stu-id="c03da-122">This capability is available for all jobs for only internal candidates.</span></span> <span data-ttu-id="c03da-123">Дополнительные сведения см. в разделе [Функция сайта карьеры в Attract](./career-site.md).</span><span class="sxs-lookup"><span data-stu-id="c03da-123">For more information, see [Career site functionality in Attract](./career-site.md).</span></span>

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a><span data-ttu-id="c03da-124">Обозначьте серебряных призеров для назначения качественных кандидатов для будущих должностей</span><span class="sxs-lookup"><span data-stu-id="c03da-124">Designate silver medalists to assign high value applicants for future positions</span></span>
<span data-ttu-id="c03da-125">Агенты по найму и менеджеры по найму часто ведут текущий список кандидатов, которые хорошо подходили для должности, но не могли быть приняты по предложению, так как должность уже заполнена.</span><span class="sxs-lookup"><span data-stu-id="c03da-125">Recruiters and hiring managers often keep a running list of applicants who were a good fit for the position but could not be extended an offer as the position was already filled.</span></span> <span data-ttu-id="c03da-126">Такие кандидаты, называемые серебряными медалистами, полезны, поскольку они позволяют сократить время приема на работу в следующий раз, когда открывается аналогичная вакансия.</span><span class="sxs-lookup"><span data-stu-id="c03da-126">Such applicants, termed silver medalists, are valuable as they can help reduce the time to hire the next time a similar position opens up.</span></span> <span data-ttu-id="c03da-127">Attract теперь позволяет агентам по найму и менеджерам по найму отмечать серебряных медалистов в списке кандидатов, если кандидат перешел на стадию предложения.</span><span class="sxs-lookup"><span data-stu-id="c03da-127">Attract now allows recruiters and hiring managers to designate silver medalists on the applicants list if the applicant is advanced to the Offer stage.</span></span> <span data-ttu-id="c03da-128">Обозначение серебряного медалиста будет появляться в списке кандидатов для должности, но также и в представлении кадрового пула, когда эти кандидаты являются членами какого-либо из пулов для агента по найму или менеджера по найму.</span><span class="sxs-lookup"><span data-stu-id="c03da-128">The silver medalist designation will appear on the applicants list for the job, but also in the talent pool view when these applicants are members of any of the recruiter's or hiring manager's pools.</span></span> <span data-ttu-id="c03da-129">Кроме того, это обозначение будут отображаться в журнале должности как часть профиля кадрового пула для кандидата.</span><span class="sxs-lookup"><span data-stu-id="c03da-129">Additionally, the designation will appear in the job history as part of the talent pool profile of a candidate.</span></span> <span data-ttu-id="c03da-130">Можно ознакомиться с предварительной версией этой функции, попросив администратора включить ее с помощью [управления функциями в центре администрирования](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="c03da-130">You can preview this feature by having an administrator turn it on using [Feature Management in the Admin Center](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="add-applicants-to-talent-pools"></a><span data-ttu-id="c03da-131">Добавление кандидатов в кадровые пулы</span><span class="sxs-lookup"><span data-stu-id="c03da-131">Add applicants to talent pools</span></span>
<span data-ttu-id="c03da-132">Теперь проще добавлять кандидатов в кадровые пулы за счет появления нового действия в списке кандидатов.</span><span class="sxs-lookup"><span data-stu-id="c03da-132">It is now easier to add applicants to talent pools by surfacing a new action on the Applicants list.</span></span> <span data-ttu-id="c03da-133">Выбрав значок **Добавить в кадровый пул**, агент по найму или менеджер по найму может выбрать из списка своих кадровых пулов и легко добавить кандидатов в кадровые пулы прямо из списка кандидатов на должность.</span><span class="sxs-lookup"><span data-stu-id="c03da-133">By selecting the **Add to talent pool** icon, the recruiter or hiring manager can choose from their list of talent pools and easily add applicants to talent pools right from the Applicants list on a job.</span></span>

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a><span data-ttu-id="c03da-134">Настройка необходимости резюме для подачи заявления для конкретной должности</span><span class="sxs-lookup"><span data-stu-id="c03da-134">Configure whether a resume is required to apply for a particular job</span></span>
<span data-ttu-id="c03da-135">Основываясь на отзывах клиентов, агенты по найму теперь могут настроить, требуется ли резюме, в виде загруженного файла, при подаче заявления для конкретной должности.</span><span class="sxs-lookup"><span data-stu-id="c03da-135">Based on customer feedback, recruiters can now configure whether a resume, in the form of an uploaded file, is required when applying for a particular job.</span></span> <span data-ttu-id="c03da-136">Эта конфигурация является частью действия заявления, доступного в процессе найма.</span><span class="sxs-lookup"><span data-stu-id="c03da-136">This configuration is part of the Application activity, accessible in the hiring process.</span></span> <span data-ttu-id="c03da-137">При включении каждому потенциальному кандидату будет предложено отправить резюме при подаче заявления на эту должность.</span><span class="sxs-lookup"><span data-stu-id="c03da-137">When enabled, every potential applicant will be prompted to upload a resume as they apply for this position.</span></span> <span data-ttu-id="c03da-138">Заявление не будет считаться полным, если не загружено резюме.</span><span class="sxs-lookup"><span data-stu-id="c03da-138">The application will not be considered complete unless a resume is uploaded.</span></span> <span data-ttu-id="c03da-139">Это помогает уменьшить шум в кадровом пуле, гарантируя, что каждый кандидат предоставляет достаточно сведений, чтобы агент по найму мог их рассмотреть.</span><span class="sxs-lookup"><span data-stu-id="c03da-139">This helps reduce the noise in the applicant pool by ensuring that every applicant provides enough information to allow the recruiter to triage them.</span></span>

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a><span data-ttu-id="c03da-140">Кандидаты могут подавать заявление о приеме на должность с помощью своего профиля LinkedIn</span><span class="sxs-lookup"><span data-stu-id="c03da-140">Candidates can apply to a job using their LinkedIn profile</span></span>
<span data-ttu-id="c03da-141">Кандидаты, которые уже имеют текущий обновленный профиль LinkedIn, могут подавать заявления на должность только одним щелчком с использованием этого профиля.</span><span class="sxs-lookup"><span data-stu-id="c03da-141">Candidates who already have their current updated profile on LinkedIn can apply to jobs with just a single click using that profile.</span></span>

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a><span data-ttu-id="c03da-142">Отслеживание, как профиль кандидата появился в системе и где ваши кандидаты обнаружили должность, на которую они подают заявление</span><span class="sxs-lookup"><span data-stu-id="c03da-142">Track how a candidate profile originated in the system and where your applicants discover the jobs they applied for</span></span>
<span data-ttu-id="c03da-143">Теперь можно выяснить, как профиль кандидата был создан в Attract, просмотрев источник профиля в разделе сведений о кандидате на странице **Профиль** заявления или профиль кадрового пула.</span><span class="sxs-lookup"><span data-stu-id="c03da-143">You can now find out how a particular candidate's profile originated in Attract by looking at the profile source under candidate details on the **Profile** page of an application or talent pool profile.</span></span> <span data-ttu-id="c03da-144">Аналогичным образом, можно выяснить, как кандидат обнаружил должность, посмотрев источник заявления, указанный в разделе **Действие заявления** в канале активности заявления.</span><span class="sxs-lookup"><span data-stu-id="c03da-144">Similarly, you can find out how any applicant discovered the job by looking at the application source provided in the **Application activity** in the application activity feed.</span></span> <span data-ttu-id="c03da-145">Эта информация также доступна в журнале должностей в профиле кадрового пула.</span><span class="sxs-lookup"><span data-stu-id="c03da-145">This information is also available in the job history in the talent pool profile.</span></span> <span data-ttu-id="c03da-146">Когда агенты по найму или менеджеры по найму добавляют вручную кандидатов, им также предлагается задать источник заявления или профиля кандидата.</span><span class="sxs-lookup"><span data-stu-id="c03da-146">When recruiters or hiring managers add candidates manually, they will also be prompted to designate the source of the application or candidate profile.</span></span> <span data-ttu-id="c03da-147">Когда кандидат подает заявление в первый раз, его источник профиля будет таким же, как источник заявления.</span><span class="sxs-lookup"><span data-stu-id="c03da-147">When a candidate applies for the first time, their profile source will be the same as the origin of their application.</span></span> <span data-ttu-id="c03da-148">Можно ознакомиться с предварительной версией этой функции, попросив администратора включить ее с помощью [управления функциями в центре администрирования](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="c03da-148">You can preview this feature by having an administrator turn it on using [Feature Management in the Admin Center](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span></span> <span data-ttu-id="c03da-149">Обратите внимание, что имеющиеся кандидаты и заявители не будут иметь сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="c03da-149">Note that existing candidates and applicants won't have any source information.</span></span> <span data-ttu-id="c03da-150">Тем не менее агенты по найму могут добавить эту информацию вручную.</span><span class="sxs-lookup"><span data-stu-id="c03da-150">However, recruiters can add this information manually.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="c03da-151">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="c03da-151">Changes in Onboard</span></span>

<span data-ttu-id="c03da-152">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="c03da-152">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="c03da-153">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="c03da-153">Changes in Core HR</span></span>

<span data-ttu-id="c03da-154">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2195</span><span class="sxs-lookup"><span data-stu-id="c03da-154">Changes described in this section apply to build number 8.1.2195</span></span>

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a><span data-ttu-id="c03da-155">Интеграция Attract создает ошибку повторяющейся записи для заявлений</span><span class="sxs-lookup"><span data-stu-id="c03da-155">Attract integration throws duplicate record error for Applications</span></span>
<span data-ttu-id="c03da-156">В данном обновлении проблема с повторяющимися записями была исправлена.</span><span class="sxs-lookup"><span data-stu-id="c03da-156">In this update, an issue with duplicate records has been fixed.</span></span> <span data-ttu-id="c03da-157">Эта проблема появляется при открытии рабочей области **Управление персоналом**.</span><span class="sxs-lookup"><span data-stu-id="c03da-157">This issue is surfaced when opening the **Personnel management** workspace.</span></span>

### <a name="unable-to-close-form-when-editing-name-sequence"></a><span data-ttu-id="c03da-158">Не удается закрыть форму при изменении последовательности имен</span><span class="sxs-lookup"><span data-stu-id="c03da-158">Unable to close form when editing name sequence</span></span>
<span data-ttu-id="c03da-159">Внесены изменения для устранения проблемы при изменении последовательности имен в форме работника.</span><span class="sxs-lookup"><span data-stu-id="c03da-159">Changes have been made to correct an issue when editing the name sequence on the worker form.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c03da-160">Скоро</span><span class="sxs-lookup"><span data-stu-id="c03da-160">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="c03da-161">Расширенная безопасность компенсации (фиксированной и переменной)</span><span class="sxs-lookup"><span data-stu-id="c03da-161">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="c03da-162">Во многих организациях менеджеры по компенсации и льготам могут иметь доступ только к определенным записям компенсаций.</span><span class="sxs-lookup"><span data-stu-id="c03da-162">In many organizations, the compensation and benefits managers might only have access to certain compensation records.</span></span> <span data-ttu-id="c03da-163">Они могут быть для руководителей или региональных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="c03da-163">These could be for executives or regional employees.</span></span> <span data-ttu-id="c03da-164">С этим изменением отдел кадров можете управлять и обслуживать планы компенсации для различных групп сотрудников в организации.</span><span class="sxs-lookup"><span data-stu-id="c03da-164">With this change, HR can manage and maintain the compensation plans for different employee groups in the organization.</span></span> <span data-ttu-id="c03da-165">Можно назначить роли безопасности фиксированным и переменным планам, которые будут определять доступ к этим планам и данным о сотрудниках, относящихся к планам, таким как записи сведений о зарплате и премиях.</span><span class="sxs-lookup"><span data-stu-id="c03da-165">You can assign security roles to fixed and variable plans that determine access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="c03da-166">Только роли, которым предоставлен доступ, могут обработать компенсацию для этих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="c03da-166">Only the roles with the access granted can process compensation for those employees.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="c03da-167">Поддержка по электронной почте для оповещений</span><span class="sxs-lookup"><span data-stu-id="c03da-167">Email support for alerts</span></span>
<span data-ttu-id="c03da-168">С обновлением платформы Platform update 24 пользователи могут создавать правила оповещений, которые автоматически отправляют уведомления по электронной почте контактам при наступлении события.</span><span class="sxs-lookup"><span data-stu-id="c03da-168">With Platform update 24, users can create alert rules that automatically dispatch email notifications to contacts when triggered by an event.</span></span>

### <a name="duplicate-employee-check-interface-changes"></a><span data-ttu-id="c03da-169">Проверка дублирования сотрудника: изменения интерфейса</span><span class="sxs-lookup"><span data-stu-id="c03da-169">Duplicate employee check: Interface changes</span></span>
<span data-ttu-id="c03da-170">После этого изменения дубликаты определяются по мере ввода полей имени, и статус отображает число обнаруженных дубликатов.</span><span class="sxs-lookup"><span data-stu-id="c03da-170">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="c03da-171">Можно выбрать предоставленную ссылку, чтобы открыть новую страницу для оценки, следует ли использовать обнаруженное соответствие.</span><span class="sxs-lookup"><span data-stu-id="c03da-171">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="c03da-172">Форма дубликатов не открывается автоматически во избежание прерывания ввода данных.</span><span class="sxs-lookup"><span data-stu-id="c03da-172">The duplicates form doesn't automatically open, to avoid interrupting data entry.</span></span>

