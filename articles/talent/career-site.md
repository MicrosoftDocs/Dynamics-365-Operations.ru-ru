---
title: "Функция сайта карьеры в Attract"
description: "Эта статья содержит обзор возможности предназначенного для кандидатов сайта карьеры в Microsoft Dynamics 365 for Talent - Attract. Также описывается, как настроить эту функцию."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: ru-ru
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="11e68-104">Функция сайта карьеры в Attract</span><span class="sxs-lookup"><span data-stu-id="11e68-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="11e68-105">Эта статья содержит обзор возможности предназначенного для кандидатов сайта карьеры в Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="11e68-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="11e68-106">Также описывается, как настроить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="11e68-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="11e68-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="11e68-107">Overview</span></span>

<span data-ttu-id="11e68-108">Attract содержит один сайт карьеры для каждой среды в клиенте.</span><span class="sxs-lookup"><span data-stu-id="11e68-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="11e68-109">Например, если в организации есть среда разработки и тестовая среда, один сайт карьеры предоставляется для среды разработки, а другой сайт карьеры предоставляется для тестовой среды.</span><span class="sxs-lookup"><span data-stu-id="11e68-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="11e68-110">Каждый сайт карьеры **полностью изолирован**, и имеет свой собственный механизм проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="11e68-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="11e68-111">Должности и профили кандидатов не являются общими между сайтами карьеры.</span><span class="sxs-lookup"><span data-stu-id="11e68-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="11e68-112">По умолчанию сайт карьеры является открытым.</span><span class="sxs-lookup"><span data-stu-id="11e68-112">By default, the career site is public.</span></span> <span data-ttu-id="11e68-113">Таким образом, кандидаты могут просматривать все задания, помеченные как внешние, без необходимости входа в систему.</span><span class="sxs-lookup"><span data-stu-id="11e68-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="11e68-114">Однако все другие действия требуют, чтобы кандидаты вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="11e68-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="11e68-115">Управление сайтом вакансий</span><span class="sxs-lookup"><span data-stu-id="11e68-115">Career site management</span></span>

<span data-ttu-id="11e68-116">Следующие элементы на сайте карьеры управляются с помощью параметров:</span><span class="sxs-lookup"><span data-stu-id="11e68-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="11e68-117">**Название организации:** название организации отображается на панели переходов в верхней части сайта карьеры.</span><span class="sxs-lookup"><span data-stu-id="11e68-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="11e68-118">Выбрав название организации, кандидаты переходят на страницу со списком всех открытых вакансий.</span><span class="sxs-lookup"><span data-stu-id="11e68-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="11e68-119">**Эмблема организации:** изображение эмблемы организации отображается в верхнем левом углу сайта карьеры.</span><span class="sxs-lookup"><span data-stu-id="11e68-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="11e68-120">Выбрав эмблему организации, кандидаты переходят на страницу со списком всех открытых вакансий.</span><span class="sxs-lookup"><span data-stu-id="11e68-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="11e68-121">Чтобы задать значения для названия и логотипа организации, выполните вход в систему Attract с правами администратора, выберите **Центр администрирования** в меню **Параметры** (символ шестеренки), затем выберите вкладку **Сведения о компании**.</span><span class="sxs-lookup"><span data-stu-id="11e68-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="11e68-122">Изображение логотипа, отображаемое на сайте карьеры, имеет фиксированную высоту 20 пикселов (px).</span><span class="sxs-lookup"><span data-stu-id="11e68-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="11e68-123">Изображение, которое добавляется в центре администрирования, масштабируется по размерам.</span><span class="sxs-lookup"><span data-stu-id="11e68-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="11e68-124">Таким образом, в зависимости от изображения, ширина может измениться.</span><span class="sxs-lookup"><span data-stu-id="11e68-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="11e68-125">URL-адрес сайта вакансий</span><span class="sxs-lookup"><span data-stu-id="11e68-125">Career site URL</span></span>

<span data-ttu-id="11e68-126">При первой [публикации объявления о внешней должности](./Creating-jobs-Attract.md#postings) можно скопировать ссылку **Применить** из приложения Attract.</span><span class="sxs-lookup"><span data-stu-id="11e68-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="11e68-127">URL-адрес для этой ссылки будет иметь следующий формат: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="11e68-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="11e68-128">URL-адрес сайта карьеры является подстрокой URL-адреса **Применить** .</span><span class="sxs-lookup"><span data-stu-id="11e68-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="11e68-129">Он состоит из всего вверх от названия компании.</span><span class="sxs-lookup"><span data-stu-id="11e68-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="11e68-130">Таким образом, для предыдущего URL-адреса **Применить** URL-адрес сайта карьеры имеет вид `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="11e68-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="11e68-131">Параметры аутентификации</span><span class="sxs-lookup"><span data-stu-id="11e68-131">Authentication options</span></span>

<span data-ttu-id="11e68-132">Кандидаты имеют следующие варианты входа для сайта карьеры Attract:</span><span class="sxs-lookup"><span data-stu-id="11e68-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="11e68-133">Личная учетная запись:</span><span class="sxs-lookup"><span data-stu-id="11e68-133">Personal account:</span></span>

    - <span data-ttu-id="11e68-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="11e68-134">LinkedIn</span></span>
    - <span data-ttu-id="11e68-135">Майкрософт</span><span class="sxs-lookup"><span data-stu-id="11e68-135">Microsoft</span></span>
    - <span data-ttu-id="11e68-136">Google</span><span class="sxs-lookup"><span data-stu-id="11e68-136">Google</span></span>
    - <span data-ttu-id="11e68-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="11e68-137">Facebook</span></span>

- <span data-ttu-id="11e68-138">Рабочая или учебная учетная запись:</span><span class="sxs-lookup"><span data-stu-id="11e68-138">Work or school account:</span></span>

    - <span data-ttu-id="11e68-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="11e68-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="11e68-140">Вход Azure AD предназначен только для внутреннего кандидатов.</span><span class="sxs-lookup"><span data-stu-id="11e68-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="11e68-141">Таким образом, он работает только для внутренних кандидатов, которые используют свои учетные данные Azure AD компании.</span><span class="sxs-lookup"><span data-stu-id="11e68-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="11e68-142">Например, кандидат, который в настоящее время является сотрудником компании Contoso Ltd, хочет подать заявление на должность в несвязанной компании Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="11e68-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="11e68-143">В этом случае вход будет неудачным, когда сотрудник пытается использовать свои учетные данные Azure AD из Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="11e68-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="11e68-144">Создание и ведение профиля</span><span class="sxs-lookup"><span data-stu-id="11e68-144">Create and maintain a profile</span></span>

<span data-ttu-id="11e68-145">После входа кандидатов на сайт карьеры они могут выбрать **Мой профиль** на панели навигации в верхней части страницы для создания и ведения их профилей.</span><span class="sxs-lookup"><span data-stu-id="11e68-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="11e68-146">Профиль включает в себя личные данные, информацию об опыте работы, сведения об образовании, документы, ссылки и сведения о наборе навыков.</span><span class="sxs-lookup"><span data-stu-id="11e68-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="11e68-147">После создания профиля он может использоваться для применения для должностей, в которых кандидат заинтересован.</span><span class="sxs-lookup"><span data-stu-id="11e68-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="11e68-148">Профили также помогают Attract рекомендовать правильные должности для кандидатов.</span><span class="sxs-lookup"><span data-stu-id="11e68-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="11e68-149">Поиск правильной должности</span><span class="sxs-lookup"><span data-stu-id="11e68-149">Find the right job</span></span>

<span data-ttu-id="11e68-150">На странице списка должностей кандидаты могут искать конкретную должность, введя условия поиска.</span><span class="sxs-lookup"><span data-stu-id="11e68-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="11e68-151">Функция поиска выполняет поиск слов в названиях должностей и описаниях должностных обязанностей и отображает соответствующие должности в результатах.</span><span class="sxs-lookup"><span data-stu-id="11e68-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="11e68-152">Кандидаты могут фильтровать результаты в любое время на основе местоположения должности или функциональных обязанностей.</span><span class="sxs-lookup"><span data-stu-id="11e68-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="11e68-153">Кандидаты также могут просматривать набор рекомендованных должностей на сайте карьеры.</span><span class="sxs-lookup"><span data-stu-id="11e68-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="11e68-154">Должности, которые рекомендуются кандидату, основаны на прошлых заявлениях, профиле и резюме кандидата.</span><span class="sxs-lookup"><span data-stu-id="11e68-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="11e68-155">Рекомендации по должности отображаются только в том случае, если по крайней мере 10 объявлений о вакансиях на должности размещены на сайте карьеры и если кандидат заполнил свой профиль.</span><span class="sxs-lookup"><span data-stu-id="11e68-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="11e68-156">Подача заявления о приеме на работу</span><span class="sxs-lookup"><span data-stu-id="11e68-156">Apply for jobs</span></span>

<span data-ttu-id="11e68-157">После того как кандидаты нашли подходящую должность, они могут подать заявление на нее с помощью кнопки **Применить** на странице сведений о должности.</span><span class="sxs-lookup"><span data-stu-id="11e68-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="11e68-158">На этом этапе кандидаты могут либо создать совершенно новый профиль, либо просмотреть сведения в своем существующем профиле.</span><span class="sxs-lookup"><span data-stu-id="11e68-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="11e68-159">Кандидаты могут также отправить резюме, если это необходимо, и затем отправить заявление на должность.</span><span class="sxs-lookup"><span data-stu-id="11e68-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="11e68-160">Проверка статуса заявления</span><span class="sxs-lookup"><span data-stu-id="11e68-160">Check application status</span></span>

<span data-ttu-id="11e68-161">После того как кандидаты подали заявление на одну или несколько должностей, они могут выбрать пункт **Заявления** на панели навигации в верхней части страницы для просмотра своих открытых и закрытых заявлений.</span><span class="sxs-lookup"><span data-stu-id="11e68-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="11e68-162">Когда кандидаты открывают одно из своих заявлений, они видят текущий этап и все ожидающие действия, которые они должны выполнить.</span><span class="sxs-lookup"><span data-stu-id="11e68-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="11e68-163">Например, если кандидат должен предоставить потенциальные даты для личного собеседования, на странице отображаются возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="11e68-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="11e68-164">Внутренние должности</span><span class="sxs-lookup"><span data-stu-id="11e68-164">Internal jobs</span></span>

<span data-ttu-id="11e68-165">В настоящее время должности, которые помечены как внутренние и опубликованы на сайте карьеры Attract, не отображаются на сайте карьеры.</span><span class="sxs-lookup"><span data-stu-id="11e68-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="11e68-166">Они доступны только через прямой URL-адрес **Применить**, который можно скопировать из приложения Attract.</span><span class="sxs-lookup"><span data-stu-id="11e68-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

