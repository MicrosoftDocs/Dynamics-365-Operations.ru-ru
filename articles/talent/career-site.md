---
title: Функция сайта карьеры в Attract
description: В этом разделе представлен обзор функций сайта карьеры для кандидатов в Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2019
ms.locfileid: "389982"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="2b104-103">Функция сайта карьеры в Attract</span><span class="sxs-lookup"><span data-stu-id="2b104-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b104-104">В этом разделе представлен обзор функций сайта карьеры для кандидатов в Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="2b104-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="2b104-105">Также описывается, как настроить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2b104-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="2b104-106">Attract содержит один сайт карьеры для каждой среды в клиенте.</span><span class="sxs-lookup"><span data-stu-id="2b104-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="2b104-107">Например, если в организации есть среда разработки и тестовая среда, один сайт карьеры предоставляется для среды разработки, а другой сайт карьеры предоставляется для тестовой среды.</span><span class="sxs-lookup"><span data-stu-id="2b104-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="2b104-108">Каждый сайт карьеры полностью изолирован и имеет свой собственный механизм проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2b104-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="2b104-109">Должности и профили кандидатов не являются общими между сайтами карьеры.</span><span class="sxs-lookup"><span data-stu-id="2b104-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="2b104-110">По умолчанию сайт карьеры является открытым.</span><span class="sxs-lookup"><span data-stu-id="2b104-110">By default, the career site is public.</span></span> <span data-ttu-id="2b104-111">Таким образом, кандидаты могут просматривать все задания, помеченные как внешние, без необходимости входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2b104-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="2b104-112">Однако все другие действия требуют, чтобы кандидаты вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="2b104-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="2b104-113">Управление сайтом вакансий</span><span class="sxs-lookup"><span data-stu-id="2b104-113">Career site management</span></span>

<span data-ttu-id="2b104-114">Чтобы задать значения для следующих элементов, выполните вход в Attract с правами администратора, выберите **Центр администрирования** в меню **Параметры** (символ шестеренки), затем выберите вкладку **Сведения о компании**.</span><span class="sxs-lookup"><span data-stu-id="2b104-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="2b104-115">**Название организации** — название организации отображается на панели переходов в верхней части сайта карьеры.</span><span class="sxs-lookup"><span data-stu-id="2b104-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="2b104-116">Выбрав название организации, кандидаты переходят на страницу со списком всех открытых вакансий.</span><span class="sxs-lookup"><span data-stu-id="2b104-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="2b104-117">**Эмблема организации** — изображение эмблемы организации отображается в верхнем левом углу сайта карьеры.</span><span class="sxs-lookup"><span data-stu-id="2b104-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="2b104-118">Выбрав эмблему организации, кандидаты переходят на страницу со списком всех открытых вакансий.</span><span class="sxs-lookup"><span data-stu-id="2b104-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="2b104-119">Изображение логотипа, отображаемое на сайте карьеры, имеет фиксированную высоту 20 пикселов (px).</span><span class="sxs-lookup"><span data-stu-id="2b104-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="2b104-120">Изображение, которое добавляется в центре администрирования, масштабируется по размерам.</span><span class="sxs-lookup"><span data-stu-id="2b104-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="2b104-121">Таким образом, в зависимости от изображения, ширина может измениться.</span><span class="sxs-lookup"><span data-stu-id="2b104-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="2b104-122">Чтобы задать значения для следующих элементов, выполните вход в Attract с правами администратора, выберите **Центр администрирования** в меню **Параметры**, затем выберите вкладку **Управление сайтом вакансий**.</span><span class="sxs-lookup"><span data-stu-id="2b104-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="2b104-123">**Оптимизация для поисковых систем** — когда включена, все открытые вакансии, размещенные на сайте вакансий Attract, будут доступны для поиска с помощью механизмов поиска, таких как Bing или Google.</span><span class="sxs-lookup"><span data-stu-id="2b104-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="2b104-124">Возможна задержка между включением этого параметра и появлением в результатах поиска, в зависимости от используемого механизма поиска.</span><span class="sxs-lookup"><span data-stu-id="2b104-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="2b104-125">URL-адреса сайта вакансий</span><span class="sxs-lookup"><span data-stu-id="2b104-125">Career site URLs</span></span>

<span data-ttu-id="2b104-126">В следующем списке перечислены часто используемые URL-адреса сайта вакансий и способы доступа к ним.</span><span class="sxs-lookup"><span data-stu-id="2b104-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="2b104-127">**URL-адрес домашней страницы сайта вакансий** — чтобы просмотреть URL-адрес домашней страницы сайта вакансий выполните вход в Attract с правами администратора, выберите **Центр администрирования** в меню **Параметры**, затем выберите вкладку **Управление сайтом вакансий**.</span><span class="sxs-lookup"><span data-stu-id="2b104-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="2b104-128">**URL-адрес подачи заявления на индивидуальное объявление о вакансии** — при первой [публикации объявления о внешней должности](Creating-jobs-Attract.md#postings) можно скопировать ссылку **Управление сайтом вакансий** из приложения Attract.</span><span class="sxs-lookup"><span data-stu-id="2b104-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="2b104-129">URL-адрес для этой ссылки будет иметь следующий формат: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="2b104-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="2b104-130">**URL-адреса публикации индивидуального объявления о вакансии** — URL-адрес объявления о вакансии является подстрокой URL-адреса подачи заявления.</span><span class="sxs-lookup"><span data-stu-id="2b104-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="2b104-131">Он состоит из всего вверх от названия номера вакансии.</span><span class="sxs-lookup"><span data-stu-id="2b104-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="2b104-132">Таким образом, для предыдущего URL-адреса подачи заявления URL-адрес объявления о вакансии имеет вид [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="2b104-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="2b104-133">Параметры аутентификации</span><span class="sxs-lookup"><span data-stu-id="2b104-133">Authentication options</span></span>

<span data-ttu-id="2b104-134">Кандидаты имеют следующие варианты входа для сайта карьеры Attract:</span><span class="sxs-lookup"><span data-stu-id="2b104-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="2b104-135">Личная учетная запись:</span><span class="sxs-lookup"><span data-stu-id="2b104-135">Personal account:</span></span>

    -   <span data-ttu-id="2b104-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2b104-136">LinkedIn</span></span>

    -   <span data-ttu-id="2b104-137">Майкрософт</span><span class="sxs-lookup"><span data-stu-id="2b104-137">Microsoft</span></span>

    -   <span data-ttu-id="2b104-138">Google</span><span class="sxs-lookup"><span data-stu-id="2b104-138">Google</span></span>

    -   <span data-ttu-id="2b104-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="2b104-139">Facebook</span></span>

-   <span data-ttu-id="2b104-140">Рабочая или учебная учетная запись:</span><span class="sxs-lookup"><span data-stu-id="2b104-140">Work or school account:</span></span>

    -   <span data-ttu-id="2b104-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="2b104-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="2b104-142">Вход Azure AD предназначен только для внутренних кандидатов.</span><span class="sxs-lookup"><span data-stu-id="2b104-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="2b104-143">Таким образом, он работает только для внутренних кандидатов, которые используют свои учетные данные Azure AD компании.</span><span class="sxs-lookup"><span data-stu-id="2b104-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="2b104-144">Например, кандидат, который в настоящее время является сотрудником компании Contoso Ltd, хочет подать заявление на должность в несвязанной компании Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="2b104-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="2b104-145">В этом случае вход будет неудачным, когда сотрудник пытается использовать свои учетные данные Azure AD из Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="2b104-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="2b104-146">Создание и ведение профиля</span><span class="sxs-lookup"><span data-stu-id="2b104-146">Create and maintain a profile</span></span>

<span data-ttu-id="2b104-147">После входа кандидатов на сайт карьеры они могут выбрать **Мой профиль** на панели навигации в верхней части страницы для создания и ведения их профилей.</span><span class="sxs-lookup"><span data-stu-id="2b104-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="2b104-148">Профиль включает в себя личные данные, информацию об опыте работы, сведения об образовании, документы, ссылки и сведения о наборе навыков.</span><span class="sxs-lookup"><span data-stu-id="2b104-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="2b104-149">После создания профиля он может использоваться для применения для должностей, в которых кандидат заинтересован.</span><span class="sxs-lookup"><span data-stu-id="2b104-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="2b104-150">Профили также помогают Attract рекомендовать правильные должности для кандидатов.</span><span class="sxs-lookup"><span data-stu-id="2b104-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="2b104-151">Если кандидат использует идентификатор электронной почты для входа с помощью одного из перечисленных выше поставщиков проверки подлинности, этот идентификатор электронной почты будет по умолчанию принимать значение идентификатора электронной почты контакта, связанного с данным профилем.</span><span class="sxs-lookup"><span data-stu-id="2b104-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="2b104-152">Однако последний можно изменить в любое время и совершенно независимо от первого.</span><span class="sxs-lookup"><span data-stu-id="2b104-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="2b104-153">Attract будет всегда будет использоваться идентификатор электронной почты контакта для связи с вашим профилем для всех сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2b104-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="2b104-154">Поиск правильной должности</span><span class="sxs-lookup"><span data-stu-id="2b104-154">Find the right job</span></span>

<span data-ttu-id="2b104-155">На странице списка должностей кандидаты могут искать конкретную должность, введя условия поиска.</span><span class="sxs-lookup"><span data-stu-id="2b104-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="2b104-156">Функция поиска выполняет поиск слов в названиях должностей и описаниях должностных обязанностей и отображает соответствующие должности в результатах.</span><span class="sxs-lookup"><span data-stu-id="2b104-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="2b104-157">Кандидаты могут фильтровать результаты в любое время на основе местоположения должности или функциональных обязанностей.</span><span class="sxs-lookup"><span data-stu-id="2b104-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="2b104-158">Кандидаты также могут просматривать набор рекомендованных должностей на сайте карьеры.</span><span class="sxs-lookup"><span data-stu-id="2b104-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="2b104-159">Должности, которые рекомендуются кандидату, основаны на прошлых заявлениях, профиле и резюме кандидата.</span><span class="sxs-lookup"><span data-stu-id="2b104-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="2b104-160">Рекомендации по должности отображаются только в том случае, если по крайней мере 10 объявлений о вакансиях на должности размещены на сайте карьеры и если кандидат заполнил свой профиль.</span><span class="sxs-lookup"><span data-stu-id="2b104-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="2b104-161">Подача заявления о приеме на работу</span><span class="sxs-lookup"><span data-stu-id="2b104-161">Apply for jobs</span></span>

<span data-ttu-id="2b104-162">После того как кандидаты нашли подходящую должность, они могут подать заявление на нее с помощью кнопки **Подать заявление** на странице **Сведения о должности**.</span><span class="sxs-lookup"><span data-stu-id="2b104-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="2b104-163">На этом этапе кандидаты могут либо создать новый профиль, либо просмотреть сведения в своем существующем профиле.</span><span class="sxs-lookup"><span data-stu-id="2b104-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="2b104-164">Кандидаты могут также отправить резюме, если это необходимо, и затем отправить заявление на должность.</span><span class="sxs-lookup"><span data-stu-id="2b104-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="2b104-165">Проверка статуса заявления</span><span class="sxs-lookup"><span data-stu-id="2b104-165">Check application status</span></span>

<span data-ttu-id="2b104-166">После того как кандидаты подали заявление на одну или несколько должностей, они могут выбрать пункт **Заявления** на панели навигации в верхней части страницы для просмотра своих открытых и закрытых заявлений.</span><span class="sxs-lookup"><span data-stu-id="2b104-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="2b104-167">Когда кандидаты открывают одно из своих заявлений, они видят текущий этап и все ожидающие действия, которые они должны выполнить.</span><span class="sxs-lookup"><span data-stu-id="2b104-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="2b104-168">Например, если кандидат должен предоставить потенциальные даты для личного собеседования, на странице отображаются доступные варианты.</span><span class="sxs-lookup"><span data-stu-id="2b104-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="2b104-169">Внутренние должности</span><span class="sxs-lookup"><span data-stu-id="2b104-169">Internal jobs</span></span>

<span data-ttu-id="2b104-170">В настоящее время должности, которые помечены как внутренние и опубликованы на сайте карьеры Attract, не отображаются на сайте вакансий.</span><span class="sxs-lookup"><span data-stu-id="2b104-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="2b104-171">Они доступны только с помощью прямого URL-адреса **Подать заявление**, который можно скопировать из приложения Attract.</span><span class="sxs-lookup"><span data-stu-id="2b104-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
