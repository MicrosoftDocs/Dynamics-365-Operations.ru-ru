---
title: "Поиск с помощью LinkedIn Recruiter"
description: "В этом разделе представлена информация об использовании машинного обучения для получения должности и рекомендаций кандидата на должность."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: ru-ru
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="770a5-103">Поиск с помощью LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="770a5-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="770a5-104">LinkedIn является крупнейшей в мире кадровой базой данных и часто основной системой, которую агенты по найму могут использовать для поиска, взаимодействия и привлечения кандидатов для должностей, которые агентам по найму требуется заполнить.</span><span class="sxs-lookup"><span data-stu-id="770a5-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="770a5-105">Интеграция LinkedIn Recruiter с Dynamics 365 for Talent: Attract упрощает для пользователей прием на работу и поддержание синхронизации данных между двумя системами.</span><span class="sxs-lookup"><span data-stu-id="770a5-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="770a5-106">Требуются рабочие места надстройки Comprehensive hiring и LinkedIn Recruiter, чтобы можно было использовать интеграцию LinkedIn Recruiter с Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="770a5-107">Настройка LinkedIn Recruiter с Attract</span><span class="sxs-lookup"><span data-stu-id="770a5-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="770a5-108">Перед использованием возможностей LinkedIn Recruiter необходимо настроить доступ уровня контракта или уровня компании с экземпляром Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="770a5-109">Чтобы завершить процесс настройки, необходимо работать с пользователем, который является администратором вашего контракта LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="770a5-110">Выполните следующие действия, чтобы настроить LinkedIn Recruiter с Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="770a5-111">Выполните вход в Attract как администратор и перейдите к пункту **Параметры администратора**.</span><span class="sxs-lookup"><span data-stu-id="770a5-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="770a5-112">В левой области щелкните вкладку **Интеграция с LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="770a5-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="770a5-113">[![Представление администратора Attract для запуска интеграции LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="770a5-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="770a5-114">Щелкните **Подключить** для запуска настройки и выполнения процесса входа в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="770a5-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="770a5-115">При наличии мест в нескольких контрактах LinkedIn выберите контракт, который вы хотите подключить к системе Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="770a5-116">Если имеется место в единственном контракте LinkedIn, этот шаг не требуется.</span><span class="sxs-lookup"><span data-stu-id="770a5-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="770a5-117">Теперь мини-приложение LinkedIn загрузится в ваши параметры администратора с показанным список интеграций.</span><span class="sxs-lookup"><span data-stu-id="770a5-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="770a5-118">В разделе **Recruiter System Connect** щелкните **Запросить**.</span><span class="sxs-lookup"><span data-stu-id="770a5-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="770a5-119">[![Представление администратора Attract для запроса интеграции LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="770a5-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="770a5-120">После запроса интеграции из Attract он будет показываться как **Партнер готов**, и его можно включить из пункта **Параметры администратора Recruiter**.</span><span class="sxs-lookup"><span data-stu-id="770a5-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="770a5-121">Если на этой странице отображается сообщение **Уведомить партнера**, подождите несколько секунд, щелкните **Уведомить партнера**, затем обновите эту страницу.</span><span class="sxs-lookup"><span data-stu-id="770a5-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="770a5-122">Теперь должно отображаться значение **Партнер готов**.</span><span class="sxs-lookup"><span data-stu-id="770a5-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="770a5-123">[![Представление администратора Attract для индикации, что запросы со стороны Attract выполнены](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="770a5-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="770a5-124">Для выполнения следующего шага необходимо иметь права администратора контракта LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="770a5-125">Выполните вход в LinkedIn с помощью учетной записи администратора и перейдите в LinkedIn Recruiter в правом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="770a5-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="770a5-126">В меню **Дополнительно** в верхней части экрана щелкните **Параметры администратора**, затем выберите вкладку **ATS**.</span><span class="sxs-lookup"><span data-stu-id="770a5-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="770a5-127">Система Attract отображаются с парой параметров, которые можно включить.</span><span class="sxs-lookup"><span data-stu-id="770a5-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="770a5-128">Если необходимо включить только экспорт одним щелчком для **Индикатор в ATS** и **Мини-приложение профиля в ATS**, выберите **Доступ на уровне компании**.</span><span class="sxs-lookup"><span data-stu-id="770a5-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="770a5-129">Если необходимо включить все возможности доступа на уровне компании, а также историю InMail, историю Notes и доступ к профилю заглушки InMail, выберите **Доступ на уровне контракта**.</span><span class="sxs-lookup"><span data-stu-id="770a5-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="770a5-130">Включите требуемый уровень доступа из параметров **Администратор-ATS** в LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="770a5-131">[![Включение интеграции Attract из представления администратора LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="770a5-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="770a5-132">Вернитесь в параметры администратора Attract в качестве AttractAdmin и выберите вкладку **Интеграция LinkedIn**. Теперь должна быть видна загрузка мини-приложения LinkedIn со значением **Включено** с включенным выбранным уровнем доступа.</span><span class="sxs-lookup"><span data-stu-id="770a5-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="770a5-133">[![Интеграция LinkedIn Recruiter завершена](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="770a5-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="770a5-134">Использование возможностей LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="770a5-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="770a5-135">После того как возможности LinkedIn Recruiter были включены администратором Attract, он становится доступным для менеджеров и агентов по найму.</span><span class="sxs-lookup"><span data-stu-id="770a5-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="770a5-136">Чтобы использовать эти возможности, подключите свою учетную запись LinkedIn в разделе **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="770a5-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="770a5-137">Несколько возможностей будут доступны после подключения как параметров администратора, так и параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="770a5-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="770a5-138">Мини-приложение профиля в ATS</span><span class="sxs-lookup"><span data-stu-id="770a5-138">In-ATS profile widget</span></span>

<span data-ttu-id="770a5-139">Можно просмотреть профиль LinkedIn кандидата в Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="770a5-140">Мини-приложение LinkedIn отображает профиль кандидата, когда сведения ATS соответствуют сведениям LinkedIn его пользователей.</span><span class="sxs-lookup"><span data-stu-id="770a5-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="770a5-141">Чтобы просмотреть профиль, перейдите в профиль кандидата из должности или кадрового пула.</span><span class="sxs-lookup"><span data-stu-id="770a5-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="770a5-142">В профиле кандидата выберите вкладку **LinkedIn**, и мини-приложение профиля будет загружено.</span><span class="sxs-lookup"><span data-stu-id="770a5-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="770a5-143">С помощью мини-приложения профиля укажите, является ли это правильным соответствием.</span><span class="sxs-lookup"><span data-stu-id="770a5-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="770a5-144">Если это не так, найдите правильного человека.</span><span class="sxs-lookup"><span data-stu-id="770a5-144">If it is not, find the correct person.</span></span> <span data-ttu-id="770a5-145">С этой страницы можно также сохранять кандидата в ваши проекты LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="770a5-146">Экспорт одним щелчком</span><span class="sxs-lookup"><span data-stu-id="770a5-146">1-click export</span></span> 

<span data-ttu-id="770a5-147">Во время поиска кандидатов в LinkedIn имеется возможность экспорта одним щелчком мыши кандидата для должностей, на которых в данный момент имеются вакансии.</span><span class="sxs-lookup"><span data-stu-id="770a5-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="770a5-148">Выполните следующие действия для экспорта одним щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="770a5-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="770a5-149">Прежде чем завершить следующие действия, убедитесь, что вам назначена роль менеджера или агента по найму персонала для должности, а также что эта должность имеет стадию **Соискатель**.</span><span class="sxs-lookup"><span data-stu-id="770a5-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="770a5-150">Создайте должность, назначьте соответствующие роли и активируйте должность.</span><span class="sxs-lookup"><span data-stu-id="770a5-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="770a5-151">Когда должность будет активирована, перейдите в LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="770a5-152">Найдите требуемого кандидата и перейдите в его профиль.</span><span class="sxs-lookup"><span data-stu-id="770a5-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="770a5-153">С помощью поля поиска должности в карточке контакта найдите должность по названию или коду должность, которая была активирована в Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="770a5-154">Если должность не найдена, нажмите **Изменить ATS** для поиска соответствующего экземпляра Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="770a5-155">После выбора должности нажмите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="770a5-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="770a5-156">Кандидат теперь получается системой Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="770a5-157">Перейдите в Attract и откройте соответствующую должность.</span><span class="sxs-lookup"><span data-stu-id="770a5-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="770a5-158">Вы найдете только что экспортированного кандидата в стадии **Соискатель**.</span><span class="sxs-lookup"><span data-stu-id="770a5-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="770a5-159">Индикатор в ATS</span><span class="sxs-lookup"><span data-stu-id="770a5-159">In-ATS indicator</span></span> 

<span data-ttu-id="770a5-160">С помощью LinkedIn Recruiter можно отслеживать, подавал ли кандидат заявления на другие должности в вашей организации,посмотреть, где они находятся на других стадиях подачи заявления на должность, а также просмотреть отзывы и комментарии из Attract в LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="770a5-161">Откройте LinkedIn Recruiter и найдите профиль кандидата, которого вы ищете.</span><span class="sxs-lookup"><span data-stu-id="770a5-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="770a5-162">Прокрутите вниз для просмотра раздела **в ATS** в профиле кандидата.</span><span class="sxs-lookup"><span data-stu-id="770a5-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="770a5-163">Это мини-приложение можно использовать для просмотра всех сведений о кандидате, которые присутствуют в Attract, из представления LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="770a5-164">Выберите вкладку **Должности и статусы**, чтобы увидеть должности, к которым они относятся, последний статус и как они перемещались для каждой должности.</span><span class="sxs-lookup"><span data-stu-id="770a5-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="770a5-165">Выберите вкладку **Отзыв о собеседовании** для просмотра отзыва, который проводившие собеседование сотрудники представили в Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="770a5-166">Выберите вкладку **Примечания**, чтобы увидеть примечания, которые были записаны для этого кандидата в Attract.</span><span class="sxs-lookup"><span data-stu-id="770a5-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="770a5-167">Журнал InMail</span><span class="sxs-lookup"><span data-stu-id="770a5-167">InMail history</span></span>

<span data-ttu-id="770a5-168">История LinkedIn InMail доступна с доступом на уровне контракта с LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="770a5-169">Когда она включена, можно просматривать всю историю InMail с кандидатом.</span><span class="sxs-lookup"><span data-stu-id="770a5-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="770a5-170">Можно также просмотреть, кто еще из вашей организации обменивался сообщениями InMail с кандидатом, однако вы не можете просматривать сообщения между ними.</span><span class="sxs-lookup"><span data-stu-id="770a5-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="770a5-171">Для просмотра истории InMail перейдите к профилю кандидата, перейдите на вкладку **LinkedIn** и перейдите в нижнюю часть страницы, чтобы просмотреть историю.</span><span class="sxs-lookup"><span data-stu-id="770a5-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="770a5-172">Можно просмотреть историю InMail только в том случае, если кандидат ответил на ваш запрос и разрешил вам доступ к своему профилю в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="770a5-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="770a5-173">Сообщения из InMail синхронизируются с Attract каждую пару часов.</span><span class="sxs-lookup"><span data-stu-id="770a5-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="770a5-174">Журнал заметок</span><span class="sxs-lookup"><span data-stu-id="770a5-174">Notes history</span></span> 

<span data-ttu-id="770a5-175">История заметок LinkedIn доступна с доступом на уровне контракта с LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="770a5-176">Когда она включена, можно просмотреть заметки, записанные о кандидате разными агентами из вашей организации.</span><span class="sxs-lookup"><span data-stu-id="770a5-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="770a5-177">Для просмотра истории заметок перейдите к профилю кандидата, перейдите на вкладку **LinkedIn** и перейдите в нижнюю часть страницы, чтобы просмотреть историю.</span><span class="sxs-lookup"><span data-stu-id="770a5-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="770a5-178">Можно просмотреть все заметки о кандидате из LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="770a5-179">Профиль заглушки InMail</span><span class="sxs-lookup"><span data-stu-id="770a5-179">InMail stub profile</span></span>

<span data-ttu-id="770a5-180">Профиль заглушки InMail LinkedIn доступен с доступом на уровне контракта с LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="770a5-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="770a5-181">Если кандидаты согласились поделиться своими профилями LinkedIn с любым пользователем в вашей организации, можно отслеживать кандидатов в Attract, и создается новая запись кандидата для каждого кандидата.</span><span class="sxs-lookup"><span data-stu-id="770a5-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="770a5-182">Чтобы просмотреть список кандидатов, перейдите к пункту **Кадровые пулы** для просмотра созданного системой кадрового пула LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="770a5-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="770a5-183">Этот кадровый пул содержит список кандидатов и заглушки их профилей, как полученные от LinkedIn, показывая имя и фамилию кандидата.</span><span class="sxs-lookup"><span data-stu-id="770a5-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="770a5-184">Код электронной почты кандидата будет отображаться, если кандидат разрешил доступ к своему адресу электронной почты.</span><span class="sxs-lookup"><span data-stu-id="770a5-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

