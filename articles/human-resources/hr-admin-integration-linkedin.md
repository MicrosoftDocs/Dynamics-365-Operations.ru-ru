---
title: Интеграция с LinkedIn Talent Hub
description: В этом разделе объясняется, как настроить интеграцию между Microsoft Dynamics 365 Human Resources и LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f70e3a6ccf9770c75334d355db5e9df9ee912dd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527893"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="10739-103">Интеграция с LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="10739-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="10739-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) является платформой системы отслеживания кандидатов (АТС).</span><span class="sxs-lookup"><span data-stu-id="10739-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="10739-105">Оно позволяет искать, контролировать и нанимать сотрудников в одном месте.</span><span class="sxs-lookup"><span data-stu-id="10739-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="10739-106">Интегрировав Microsoft Dynamics 365 Human Resources с LinkedIn Talent Hub, можно легко создавать записи о сотрудниках в Human Resources для претендентов, которые были приняты на должность.</span><span class="sxs-lookup"><span data-stu-id="10739-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="10739-107">Настройка</span><span class="sxs-lookup"><span data-stu-id="10739-107">Setup</span></span>

<span data-ttu-id="10739-108">Системный администратор должен выполнить задачи настройки для включения интеграции с LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="10739-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="10739-109">Во-первых, в среде Power Apps необходимо настроить пользователя и роль безопасности, чтобы предоставить LinkedIn Talent Hub соответствующие разрешения на запись данных в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10739-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="10739-110">Связывание среды с LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="10739-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="10739-111">Откройте [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="10739-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="10739-112">В раскрывающемся меню пользователя выберите **Параметры продукта**.</span><span class="sxs-lookup"><span data-stu-id="10739-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="10739-113">В левой области переходов в разделе **Дополнительно** выберите **Интеграции**.</span><span class="sxs-lookup"><span data-stu-id="10739-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="10739-114">Выберите **Авторизовать** для интеграции Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10739-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="10739-115">На странице **Dynamics 365 Human Resources** выберите среду, с которой требуется связать LinkedIn Talent Hub, затем выберите пункт **Ссылка**.</span><span class="sxs-lookup"><span data-stu-id="10739-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![Подключение LinkedIn Talent Hub](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="10739-117">Можно привязывать только к средам, в которых ваша учетная запись пользователя имеет доступ администратора к среде Human Resources и к связанной среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="10739-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="10739-118">Если на странице ссылки Human Resources отсутствуют среды, убедитесь, что у вас есть лицензированная среда Human Resources на клиенте, а пользователь, с которым вы выполнили вход на страницу ссылки, обладает правами администратора как в среде Human Resources, так и в среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="10739-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="10739-119">Создание роли безопасности Power Apps</span><span class="sxs-lookup"><span data-stu-id="10739-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="10739-120">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="10739-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="10739-121">В списке **Среды** выберите среду, связанную со средой Human Resources, с которой необходимо связать экземпляр LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="10739-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="10739-122">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="10739-122">Select **Settings**.</span></span>

4. <span data-ttu-id="10739-123">Разверните узел **Пользователи + Разрешения** и выберите **Роли безопасности**.</span><span class="sxs-lookup"><span data-stu-id="10739-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="10739-124">На странице **Роли безопасности** на панели инструментов выберите **Создать роль**.</span><span class="sxs-lookup"><span data-stu-id="10739-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="10739-125">На вкладке **Сведения** введите имя роли, например, **Интеграция LinkedIn Talent Hub HRIS**.</span><span class="sxs-lookup"><span data-stu-id="10739-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="10739-126">На вкладке **Настройка** выберите разрешение **Чтение** на уровне организации для следующих сущностей:</span><span class="sxs-lookup"><span data-stu-id="10739-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="10739-127">Объект</span><span class="sxs-lookup"><span data-stu-id="10739-127">Entity</span></span>
    - <span data-ttu-id="10739-128">Поле</span><span class="sxs-lookup"><span data-stu-id="10739-128">Field</span></span>
    - <span data-ttu-id="10739-129">Родственные связи</span><span class="sxs-lookup"><span data-stu-id="10739-129">Relationship</span></span>

8. <span data-ttu-id="10739-130">Сохраните и закройте роль безопасности.</span><span class="sxs-lookup"><span data-stu-id="10739-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="10739-131">Создание пользователя приложения Power Apps</span><span class="sxs-lookup"><span data-stu-id="10739-131">Create a Power Apps application user</span></span>

<span data-ttu-id="10739-132">Пользователь приложения должен быть создан для адаптера LinkedIn Talent Hub, чтобы предоставить разрешения на адаптер для записи записей кандидатов в среду Power Apps.</span><span class="sxs-lookup"><span data-stu-id="10739-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="10739-133">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="10739-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="10739-134">В списке **Среды** выберите среду, связанную со средой Human Resources, с которой необходимо связать экземпляр LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="10739-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="10739-135">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="10739-135">Select **Settings**.</span></span>

4. <span data-ttu-id="10739-136">Разверните узел **Пользователи + Разрешения** и выберите **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="10739-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="10739-137">Выберите **Управление пользователями в Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="10739-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="10739-138">Используйте раскрывающееся меню над списком, чтобы изменить представление с представления по умолчанию **Включенные пользователи** на **Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="10739-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Представление пользователей приложений](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="10739-140">На панели инструментов выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="10739-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="10739-141">На странице **Создать пользователя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="10739-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="10739-142">Измените значение поля **Тип пользователя** на **Пользователь приложения**.</span><span class="sxs-lookup"><span data-stu-id="10739-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="10739-143">Задайте в поле **Имя пользователя** значение **Интеграция Dynamics365 HR LinkedIn HRIS**.</span><span class="sxs-lookup"><span data-stu-id="10739-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="10739-144">Задайте в поле **Код приложения** значение **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="10739-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="10739-145">Введите любое значение в поля **Имя**, **Фамилия** и **Основной адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="10739-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="10739-146">На панели инструментов выберите **Сохранить \& закрыть**.</span><span class="sxs-lookup"><span data-stu-id="10739-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="10739-147">Назначение роли безопасности новому пользователю</span><span class="sxs-lookup"><span data-stu-id="10739-147">Assign a security role to the new user</span></span>

<span data-ttu-id="10739-148">После сохранения и закрытия нового пользователя приложения в предыдущем разделе выполняется возврат на страницу **Список пользователя**.</span><span class="sxs-lookup"><span data-stu-id="10739-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="10739-149">На странице **Список пользователей** измените представление на **Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="10739-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="10739-150">Выберите пользователя приложения, которого вы создали в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="10739-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="10739-151">На панели инструментов выберите **Управление ролями**.</span><span class="sxs-lookup"><span data-stu-id="10739-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="10739-152">Выберите роль безопасности, которая была создана ранее для интеграции.</span><span class="sxs-lookup"><span data-stu-id="10739-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="10739-153">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="10739-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="10739-154">Добавление приложения Azure Active Directory в Human Resources</span><span class="sxs-lookup"><span data-stu-id="10739-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="10739-155">В Dynamics 365 Human Resources откройте страницу **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="10739-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="10739-156">Добавьте новую запись в список и задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="10739-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="10739-157">**Код клиента**: введите **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="10739-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="10739-158">**Имя**: введите имя созданной ранее роли безопасности Power Apps, например **Интеграция LinkedIn Talent Hub HRIS**.</span><span class="sxs-lookup"><span data-stu-id="10739-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="10739-159">**Код пользователя**: выберите пользователя, обладающего разрешениями на запись данных в управлении персоналом.</span><span class="sxs-lookup"><span data-stu-id="10739-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-entity-in-common-data-service"></a><span data-ttu-id="10739-160">Создание сущности в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="10739-160">Create the entity in Common Data Service</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10739-161">Интеграция с LinkedIn Talent Hub зависит от виртуальных сущностей в Common Data Service для Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10739-161">The integration with LinkedIn Talent Hub depends on virtual entities in Common Data Service for Human Resources.</span></span> <span data-ttu-id="10739-162">В качестве обязательного условия для этого шага настройки необходимо настроить виртуальные сущности.</span><span class="sxs-lookup"><span data-stu-id="10739-162">As a prerequisite for this step in the setup, you must configure virtual entities.</span></span> <span data-ttu-id="10739-163">Сведения о настройке виртуальных сущностей см. в разделе [Настройка виртуальных сущностей Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="10739-163">For information about how to configure virtual entities, see [Configure Common Data Service virtual entities](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="10739-164">В Human Resources откройте страницу **Интеграция Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="10739-164">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="10739-165">Выберите вкладку **Виртуальные сущности**.</span><span class="sxs-lookup"><span data-stu-id="10739-165">Select the **Virtual entities** tab.</span></span>

3. <span data-ttu-id="10739-166">Отфильтруйте список сущностей по метке сущности, чтобы найти **Экспортированный кандидат LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="10739-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="10739-167">Выберите сущность, затем выберите **Генерировать/обновить**.</span><span class="sxs-lookup"><span data-stu-id="10739-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="10739-168">Экспорт записей кандидатов</span><span class="sxs-lookup"><span data-stu-id="10739-168">Exporting candidate records</span></span>

<span data-ttu-id="10739-169">После завершения настройки сотрудники по найму персонала и специалисты отдела кадров (HR) могут использовать функцию **Экспорт в HRIS** в LinkedIn Talent Hub для экспорта записей о нанятых кандидатах из LinkedIn Talent Hub в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10739-169">After the setup is completed, recruiters and Human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="10739-170">Экспорт записей из LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="10739-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="10739-171">После того как кандидат перешел в процесс набора персонала и был принят на работу, можно экспортировать запись кандидата из LinkedIn Talent Hub в модуль Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10739-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="10739-172">В LinkedIn Talent Hub откройте проект, для которого вы нанимаете нового сотрудника.</span><span class="sxs-lookup"><span data-stu-id="10739-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="10739-173">Выберите запись кандидата.</span><span class="sxs-lookup"><span data-stu-id="10739-173">Select a candidate record.</span></span>

3. <span data-ttu-id="10739-174">Выберите **Изменить стадию**, затем выберите **Нанят**.</span><span class="sxs-lookup"><span data-stu-id="10739-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="10739-175">В меню с многоточием (**...**) для кандидата выберите **Экспорт в HRIS**.</span><span class="sxs-lookup"><span data-stu-id="10739-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="10739-176">В области **Экспорт в HRIS** введите информацию, которую необходимо экспортировать:</span><span class="sxs-lookup"><span data-stu-id="10739-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="10739-177">В поле **Поставщик HRIS** выберите **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="10739-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="10739-178">В поле **Дата начала** выберите значение для нового сотрудника.</span><span class="sxs-lookup"><span data-stu-id="10739-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="10739-179">В поле **Должность** введите название должности для нового сотрудника.</span><span class="sxs-lookup"><span data-stu-id="10739-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="10739-180">В поле **Местоположение** введите местоположение, в котором будет базироваться сотрудник.</span><span class="sxs-lookup"><span data-stu-id="10739-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="10739-181">Введите или проверьте адрес электронной почты сотрудника.</span><span class="sxs-lookup"><span data-stu-id="10739-181">Enter or verify the employee's email address.</span></span>

![Панель экспорта в HRIS в LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="10739-183">Завершение подключения в модуле Human Resources</span><span class="sxs-lookup"><span data-stu-id="10739-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="10739-184">Записи кандидатов, экспортированные из LinkedIn Talent Hub в модуль Human Resources, отображаются в разделе **Кандидаты на прием на работу** на странице **Управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="10739-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="10739-185">В Human Resources откройте страницу **Управление персоналом**.</span><span class="sxs-lookup"><span data-stu-id="10739-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="10739-186">В разделе **Кандидаты на прием на работу** выберите **Нанять** для выбранного кандидата.</span><span class="sxs-lookup"><span data-stu-id="10739-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="10739-187">В диалоговом окне **Нанять нового работника** проверьте запись и добавьте все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="10739-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="10739-188">Можно также выбрать номер должности, на которую кандидат был нанят.</span><span class="sxs-lookup"><span data-stu-id="10739-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="10739-189">После ввода требуемой информации можно продолжить работу со стандартными процессами для создания записей о сотрудниках и адаптации сотрудников.</span><span class="sxs-lookup"><span data-stu-id="10739-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="10739-190">Следующие сведения импортируются и включаются в новую запись сотрудника:</span><span class="sxs-lookup"><span data-stu-id="10739-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="10739-191">Имя</span><span class="sxs-lookup"><span data-stu-id="10739-191">First name</span></span>
- <span data-ttu-id="10739-192">Фамилия</span><span class="sxs-lookup"><span data-stu-id="10739-192">Last name</span></span>
- <span data-ttu-id="10739-193">Дата начала трудоустройства</span><span class="sxs-lookup"><span data-stu-id="10739-193">Employment start date</span></span>
- <span data-ttu-id="10739-194">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="10739-194">Email address</span></span>
- <span data-ttu-id="10739-195">Номер телефона</span><span class="sxs-lookup"><span data-stu-id="10739-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="10739-196">См. также</span><span class="sxs-lookup"><span data-stu-id="10739-196">See also</span></span>

[<span data-ttu-id="10739-197">Настройка виртуальных сущностей Common Data Service</span><span class="sxs-lookup"><span data-stu-id="10739-197">Configure Common Data Service virtual entities</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="10739-198">Что такое Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="10739-198">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
