---
title: Найм кандидатов на работу
description: В этом разделе показано, как нанимать кандидатов в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 529f419a4e3e4e8807c6938fd2425ae01ce282f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051817"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="623bb-103">Найм кандидатов на работу</span><span class="sxs-lookup"><span data-stu-id="623bb-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="623bb-104">Dynamics 365 Human Resources помогает управлять запросами набора персонала.</span><span class="sxs-lookup"><span data-stu-id="623bb-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="623bb-105">Кроме того, он позволяет легко переводить кандидатов в сотрудников.</span><span class="sxs-lookup"><span data-stu-id="623bb-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="623bb-106">Если ваша организация использует отдельное заявление о приеме на работу, процесс найма может включать следующие этапы:</span><span class="sxs-lookup"><span data-stu-id="623bb-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="623bb-107">Введите запрос по набору сотрудников в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="623bb-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="623bb-108">Получите рекомендации кандидатов в Human Resources из заявления о приеме на работу.</span><span class="sxs-lookup"><span data-stu-id="623bb-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="623bb-109">Выполните процедуру утверждения кандидатов в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="623bb-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="623bb-110">Если не используется отдельное заявление о приеме на работу, можно также вручную управлять кандидатами в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="623bb-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="623bb-111">Если вы являетесь администратором или разработчиком и хотите интегрировать Human Resources со сторонним приложением, см. раздел [Настройка интеграции Dataverse](hr-admin-integration-common-data-service.md) и [Настройка виртуальных таблиц Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="623bb-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="623bb-112">Вы также можете найти приложения интеграции набора персонала на [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="623bb-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="623bb-113">Чтобы испытать нашу предварительную версию функции для интеграции с LinkedIn Talent Hub, см. раздел [Интеграция с LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="623bb-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="623bb-114">Включить запросы на набор сотрудников</span><span class="sxs-lookup"><span data-stu-id="623bb-114">Enable recruiting requests</span></span>

<span data-ttu-id="623bb-115">Если необходимо отправить запросы на набор сотрудников в Human Resources, необходимо сначала включить функцию в разделе **Общие параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="623bb-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="623bb-116">В рабочей области **Управление персоналом** выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="623bb-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="623bb-117">В разделе **Настройка** выберите **Совместно используемые параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="623bb-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="623bb-118">На вкладке **Набор сотрудников** в области **НАБОР СОТРУДНИКОВ** установите для параметра **Включить запросы набора персонала** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="623bb-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="623bb-119">Добавление местоположения запроса по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="623bb-119">Add a recruiting request location</span></span>

<span data-ttu-id="623bb-120">Если организация имеет несколько местоположений, можно добавить их, чтобы инициаторы запросов могли выбрать местоположение, в котором будет работать новый сотрудник.</span><span class="sxs-lookup"><span data-stu-id="623bb-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="623bb-121">Местоположение будет включено в разноску задания.</span><span class="sxs-lookup"><span data-stu-id="623bb-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="623bb-122">В строке поиска введите **местоположение запроса набора персонала**.</span><span class="sxs-lookup"><span data-stu-id="623bb-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="623bb-123">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="623bb-123">Select **New**.</span></span>

3. <span data-ttu-id="623bb-124">В поле **Местоположение запроса набора персонала** введите название местоположения.</span><span class="sxs-lookup"><span data-stu-id="623bb-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Добавление местоположения запроса по набору сотрудников](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="623bb-126">В поле **Описание** введите описание для местоположения.</span><span class="sxs-lookup"><span data-stu-id="623bb-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="623bb-127">В поле **Местоположение** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="623bb-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="623bb-128">Если появится всплывающее окно **Новый адрес**, введите адрес местоположения.</span><span class="sxs-lookup"><span data-stu-id="623bb-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Введите адрес](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="623bb-130">В разделе **Контактная информация** введите информацию для контакта местоположения.</span><span class="sxs-lookup"><span data-stu-id="623bb-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="623bb-131">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="623bb-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="623bb-132">Добавление запроса по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="623bb-132">Add a recruiting request</span></span>

<span data-ttu-id="623bb-133">Менеджеры могут отправлять запросы на набор сотрудников в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="623bb-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="623bb-134">Если используется отдельное заявление о найме на работу, выполнение этих шагов приведет к отправке запроса на набор персонала и запуску процесса найма в этом приложении.</span><span class="sxs-lookup"><span data-stu-id="623bb-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="623bb-135">В противном случае выполните эту процедуру, чтобы начать рабочий-процесс для внутреннего процесса набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="623bb-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="623bb-136">Выберите **Самообслуживание сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="623bb-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="623bb-137">Выберите вкладку **Моя рабочая группа**.</span><span class="sxs-lookup"><span data-stu-id="623bb-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="623bb-138">Выберите **Запрос на набор сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="623bb-138">Select  **Request to recruit**.</span></span>

   ![Запуск запроса по набору сотрудников](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="623bb-140">Заполните поля **Описание**, **Должность** и **Ожидаемая дата начала**.</span><span class="sxs-lookup"><span data-stu-id="623bb-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Завершение запроса по набору сотрудников](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="623bb-142">Выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="623bb-142">Select **Continue**.</span></span> <span data-ttu-id="623bb-143">Появится запрос по набору сотрудников для данной должности.</span><span class="sxs-lookup"><span data-stu-id="623bb-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="623bb-144">В разделе **Общие** выберите агентство по найму из раскрывающегося списка **Агентство по найму**, затем выберите местоположение в раскрывающемся списке **Местоположение запроса по набору сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="623bb-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="623bb-145">В области **Должность** измените любую необходимую информацию, затем выберите **Создать сведения из должности**.</span><span class="sxs-lookup"><span data-stu-id="623bb-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Создать сведения из должности](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="623bb-147">Оставшаяся часть запроса набора сотрудников будет заполняться сведениями по умолчанию для введенной вами должности.</span><span class="sxs-lookup"><span data-stu-id="623bb-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="623bb-148">В поле **Внешнее описание** введите внешнее описание должности.</span><span class="sxs-lookup"><span data-stu-id="623bb-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="623bb-149">В области **Позиции** выберите **Добавить**, затем выберите позицию для этого запроса набора персонала.</span><span class="sxs-lookup"><span data-stu-id="623bb-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Добавление должности](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="623bb-151">В области **Навыки** выберите **Добавить**, а затем выберите навык.</span><span class="sxs-lookup"><span data-stu-id="623bb-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="623bb-152">В области **Требования к образованию** выберите **Добавить**, затем выберите значения в раскрывающихся списках **Образование** и **Уровень образования**.</span><span class="sxs-lookup"><span data-stu-id="623bb-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Добавление требований к образованию](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="623bb-154">В области **Комментарий** добавьте комментарии, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="623bb-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="623bb-155">В области **Компенсация** выберите уровень в раскрывающемся списке **Уровень**, затем скорректируйте **Нижний порог**, **Контрольная точка** и **Верхний порог**, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="623bb-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="623bb-156">Когда запрос набора персонала завершен и вы готовы начать процесс найма, выберите **Активировать** в строке меню.</span><span class="sxs-lookup"><span data-stu-id="623bb-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Активация запроса на набор сотрудников](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="623bb-158">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="623bb-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="623bb-159">Просмотр и редактирование запросов на набор сотрудников</span><span class="sxs-lookup"><span data-stu-id="623bb-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="623bb-160">Если вы являетесь руководителем и хотите просмотреть собственные запросы:</span><span class="sxs-lookup"><span data-stu-id="623bb-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="623bb-161">Выберите **Самообслуживание сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="623bb-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="623bb-162">Выберите вкладку **Моя рабочая группа**.</span><span class="sxs-lookup"><span data-stu-id="623bb-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="623bb-163">В **Сведения о моей группе** выберите вкладку **Запросы на набор сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="623bb-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Выберите вкладку запросов на набор сотрудников](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="623bb-165">Для просмотра или изменения запроса на набор сотрудников выберите его в сетке.</span><span class="sxs-lookup"><span data-stu-id="623bb-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="623bb-166">Если вы являетесь специалистом отдела кадров и хотите просмотреть все запросы на набор сотрудников:</span><span class="sxs-lookup"><span data-stu-id="623bb-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="623bb-167">Выберите **Управление персоналом**.</span><span class="sxs-lookup"><span data-stu-id="623bb-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="623bb-168">Выберите **Запросы на набор сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="623bb-168">Select **Recruiting requests**.</span></span>

   ![Просмотр запросов на набор сотрудников в модуле управления персоналом](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="623bb-170">Для просмотра или изменения запроса на набор сотрудников выберите его в сетке.</span><span class="sxs-lookup"><span data-stu-id="623bb-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="623bb-171">Добавление или изменение профиля кандидата</span><span class="sxs-lookup"><span data-stu-id="623bb-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="623bb-172">Если ваша организация интегрирована с другим приложением для управления запросами набора персонала, запросы на набор персонала направляются этому приложению.</span><span class="sxs-lookup"><span data-stu-id="623bb-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="623bb-173">Затем приложение по набору персонала отправляет сведения о кандидате обратно в модуль Human Resources.</span><span class="sxs-lookup"><span data-stu-id="623bb-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="623bb-174">В противном случае можно выполнить собственные внутренние процессы набора сотрудников и ввести сведения о кандидате вручную.</span><span class="sxs-lookup"><span data-stu-id="623bb-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="623bb-175">Выберите **Управление персоналом**.</span><span class="sxs-lookup"><span data-stu-id="623bb-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="623bb-176">Выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="623bb-176">Select **Links**.</span></span>

3. <span data-ttu-id="623bb-177">В области **Набор сотрудников** выберите **Кандидаты**.</span><span class="sxs-lookup"><span data-stu-id="623bb-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Просмотр кандидатов](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="623bb-179">Чтобы добавить кандидата, выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="623bb-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="623bb-180">Чтобы изменить существующего кандидата, выберите кандидата из списка, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="623bb-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="623bb-181">Появляется профиль кандидата.</span><span class="sxs-lookup"><span data-stu-id="623bb-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="623bb-182">В области **Сводка кандидата** введите или отредактируйте сведения о кандидате, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="623bb-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="623bb-183">В области **Запрос набора персонала** выберите запрос набора персонала, с которым требуется связать кандидата.</span><span class="sxs-lookup"><span data-stu-id="623bb-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="623bb-184">Затем заполните поля **Ожидаемая дата начала**, **Менеджер по найму**, **Должность** и **Описание**, как требуется.</span><span class="sxs-lookup"><span data-stu-id="623bb-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Связывание с запросом по набору сотрудников](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="623bb-186">Заполните все сведения в следующих областях, которые требуется включить в запись кандидата:</span><span class="sxs-lookup"><span data-stu-id="623bb-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="623bb-187">**Комментарии**</span><span class="sxs-lookup"><span data-stu-id="623bb-187">**Comments**</span></span>
   - <span data-ttu-id="623bb-188">**Опыт работы**</span><span class="sxs-lookup"><span data-stu-id="623bb-188">**Professional experience**</span></span>
   - <span data-ttu-id="623bb-189">**Контактная информация**</span><span class="sxs-lookup"><span data-stu-id="623bb-189">**Contact information**</span></span>
   - <span data-ttu-id="623bb-190">**Образование**</span><span class="sxs-lookup"><span data-stu-id="623bb-190">**Education**</span></span>
   - <span data-ttu-id="623bb-191">**Навыки**</span><span class="sxs-lookup"><span data-stu-id="623bb-191">**Skills**</span></span>
   - <span data-ttu-id="623bb-192">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="623bb-192">**Certificates**</span></span>
   - <span data-ttu-id="623bb-193">**Отборы**</span><span class="sxs-lookup"><span data-stu-id="623bb-193">**Screenings**</span></span>

8. <span data-ttu-id="623bb-194">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="623bb-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="623bb-195">Прием кандидата на работу</span><span class="sxs-lookup"><span data-stu-id="623bb-195">Hire a candidate</span></span>

<span data-ttu-id="623bb-196">Когда все готово для приема кандидата на работу, выполните следующую процедуру, чтобы перевести кандидата в сотрудника.</span><span class="sxs-lookup"><span data-stu-id="623bb-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="623bb-197">В форме кандидат выберите **Прием на работу**.</span><span class="sxs-lookup"><span data-stu-id="623bb-197">On the candidate form, select **Hire**.</span></span>

   ![Прием кандидата на работу](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="623bb-199">В форме **Нанять нового работника** в области **Сведения** заполните все поля.</span><span class="sxs-lookup"><span data-stu-id="623bb-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Ввод сведений о новом нанимаемом сотруднике](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="623bb-201">В области **Сведения о должности** проверьте и измените сведения, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="623bb-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="623bb-202">В разделе **Контрольные списки адаптации** выберите соответствующие контрольные списки адаптации для этого сотрудника.</span><span class="sxs-lookup"><span data-stu-id="623bb-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="623bb-203">Выберите **Продолжить**, чтобы создать запись сотрудника.</span><span class="sxs-lookup"><span data-stu-id="623bb-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="623bb-204">В зависимости от рабочего процесса в вашей организации, запись кандидата могла пройти через дополнительные этапы утверждения, прежде чем стать записью сотрудника.</span><span class="sxs-lookup"><span data-stu-id="623bb-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="623bb-205">Принятие решения не принимать кандидата на работу</span><span class="sxs-lookup"><span data-stu-id="623bb-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="623bb-206">Если вы решили не принимать кандидата на работу, выполните следующую процедуру, чтобы удалить его из процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="623bb-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="623bb-207">В форме кандидата выберите **Не принимать на работу**.</span><span class="sxs-lookup"><span data-stu-id="623bb-207">On the candidate form, select **Do not hire**.</span></span>

   ![Не принимать кандидата на работу](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="623bb-209">Выберите **Код причины** и добавьте комментарии.</span><span class="sxs-lookup"><span data-stu-id="623bb-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="623bb-210">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="623bb-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="623bb-211">Отклонение кандидата</span><span class="sxs-lookup"><span data-stu-id="623bb-211">Dismiss a candidate</span></span>

<span data-ttu-id="623bb-212">При необходимости можно отклонить кандидата после найма.</span><span class="sxs-lookup"><span data-stu-id="623bb-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="623bb-213">Например, кандидат может отклонить ваше предложение или не прийти на работу в первый день.</span><span class="sxs-lookup"><span data-stu-id="623bb-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="623bb-214">В форме кандидата выберите **Отклонить кандидата**.</span><span class="sxs-lookup"><span data-stu-id="623bb-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Удалить кандидата](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="623bb-216">См. также</span><span class="sxs-lookup"><span data-stu-id="623bb-216">See also</span></span>

[<span data-ttu-id="623bb-217">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="623bb-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="623bb-218">Организация трудовых ресурсов</span><span class="sxs-lookup"><span data-stu-id="623bb-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="623bb-219">Настройка компонентов должности</span><span class="sxs-lookup"><span data-stu-id="623bb-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
