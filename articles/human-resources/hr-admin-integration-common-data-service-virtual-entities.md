---
title: Настройка виртуальных сущностей Common Data Service
description: В этом разделе показано, как настроить виртуальные сущности для Dynamics 365 Human Resources. Создание и обновление существующих виртуальных сущностей и анализ созданных и доступных сущностей.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058162"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="0c2be-104">Настройка виртуальных сущностей Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0c2be-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="0c2be-105">Dynamics 365 Human Resources — это виртуальный источник данных в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="0c2be-106">Он предоставляет полные операции создания, чтения, обновления и удаления (CRUD) в Common Data Service и Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="0c2be-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="0c2be-107">Данные для виртуальных сущностей хранятся не в Common Data Service, а в базе данных приложения.</span><span class="sxs-lookup"><span data-stu-id="0c2be-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="0c2be-108">Чтобы включить операции CRUD для сущностей Human Resources в Common Data Service, необходимо сделать эти сущности доступными в качестве виртуальных сущностей в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="0c2be-109">Это позволяет выполнять операции CRUD из Common Data Service и Microsoft Power Platform с данными, находящимися в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="0c2be-110">Операции также поддерживают полные проверки бизнес-логики Human Resources для обеспечения целостности данных при записи данных в сущности.</span><span class="sxs-lookup"><span data-stu-id="0c2be-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="0c2be-111">Доступные виртуальные сущности для Human Resources</span><span class="sxs-lookup"><span data-stu-id="0c2be-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="0c2be-112">Все сущности Open Data Protocol (OData) в приложении Human Resources доступны как виртуальные сущности в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="0c2be-113">Они также доступны в Power Platform.</span><span class="sxs-lookup"><span data-stu-id="0c2be-113">They're also available in Power Platform.</span></span> <span data-ttu-id="0c2be-114">Теперь можно создавать приложения и взаимодействие с данными непосредственно из модуля Human Resources, используя полные возможности CRUD, без копирования или синхронизации данных с Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="0c2be-115">Порталы Power Apps можно использовать для создания веб-сайтов с внешним интерфейсом, которые позволяют выполнять сценарии совместной работы в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="0c2be-116">Можно просмотреть список виртуальных сущностей, включенных в среде, и начать работу с сущностями в [Power Apps](https://make.powerapps.com), в решении **Виртуальные сущности Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Виртуальные сущности Dynamics 365 HR в Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="0c2be-118">Сравнение виртуальных и естественных сущностей</span><span class="sxs-lookup"><span data-stu-id="0c2be-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="0c2be-119">Виртуальные сущности для приложения Human Resources не совпадают с естественными сущностями Common Data Service, созданными для приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="0c2be-120">Естественные сущности для приложения Human Resources создаются отдельно и поддерживаются в общем решении HCM в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="0c2be-121">В случае естественных сущностей данные хранятся в Common Data Service и требуют синхронизации с базой данных приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="0c2be-122">Список естественных сущностей Common Data Service для решения Human Resources см. в разделе [Сущности Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="0c2be-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="0c2be-123">Настройка</span><span class="sxs-lookup"><span data-stu-id="0c2be-123">Setup</span></span>

<span data-ttu-id="0c2be-124">Для включения виртуальных сущностей в среде выполните следующие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="0c2be-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="0c2be-125">Регистрация приложения в Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="0c2be-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="0c2be-126">Прежде всего необходимо зарегистрировать приложение на портале Azure, чтобы платформа идентификации Microsoft могла предоставлять службы проверки подлинности и авторизации для приложения и пользователей.</span><span class="sxs-lookup"><span data-stu-id="0c2be-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="0c2be-127">Дополнительные сведения о регистрации приложений в Azure см. в разделе [Краткое руководство: регистрация приложения на платформе идентификации Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="0c2be-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="0c2be-128">Откройте [портал Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c2be-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="0c2be-129">В списке служб Azure выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="0c2be-130">Выберите **Создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-130">Select **New registration**.</span></span>

4. <span data-ttu-id="0c2be-131">В поле **Имя** введите описательное имя для приложения.</span><span class="sxs-lookup"><span data-stu-id="0c2be-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="0c2be-132">Например, **Виртуальные сущности Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="0c2be-133">В поле **URI перенаправления** введите URL-адрес пространства имен вашего экземпляра Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="0c2be-134">Выберите **Регистр**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-134">Select **Register**.</span></span>

7. <span data-ttu-id="0c2be-135">После завершения регистрации портал Azure отображает область **Обзор** регистрации приложения, которая содержит **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="0c2be-136">На этом этапе запишите **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="0c2be-137">Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="0c2be-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="0c2be-138">В левой области навигации выберите **Сертификаты и секреты**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="0c2be-139">В разделе **Секреты клиентов** этой страницы выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="0c2be-140">Введите описание, выберите продолжительность и выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="0c2be-141">Запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="0c2be-141">Record the secret's value.</span></span> <span data-ttu-id="0c2be-142">Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="0c2be-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0c2be-143">На этом этапе обязательно запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="0c2be-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="0c2be-144">Секрет никогда не отображается снова после выхода с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="0c2be-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="0c2be-145">Установка приложения Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="0c2be-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="0c2be-146">Установите приложение Dynamics 365 HR Virtual Entity в своей среде Power Apps, чтобы развернуть пакет решения виртуальных сущностей в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="0c2be-147">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0c2be-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="0c2be-148">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="0c2be-149">В разделе **Ресурсы** этой страницы выберите **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="0c2be-150">Выберите действие **Установить приложение**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="0c2be-151">Выберите **Dynamics 365 HR Virtual Entity** , затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="0c2be-152">Просмотрите и отметьте, чтобы принять условия обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0c2be-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="0c2be-153">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-153">Select **Install**.</span></span>

<span data-ttu-id="0c2be-154">Установка занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="0c2be-154">The install takes a few minutes.</span></span> <span data-ttu-id="0c2be-155">После завершения переходите к следующим шагам.</span><span class="sxs-lookup"><span data-stu-id="0c2be-155">When it completes, continue to the next steps.</span></span>

![Установка приложения Dynamics 365 HR Virtual Entity с помощью центра администрирования Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="0c2be-157">Настройка источника данных виртуальной сущности</span><span class="sxs-lookup"><span data-stu-id="0c2be-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="0c2be-158">Следующим шагом является настройка источника данных виртуальных сущностей в среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0c2be-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="0c2be-159">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0c2be-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="0c2be-160">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="0c2be-161">Выберите **URL-адрес среды** в разделе **Сведения** на странице.</span><span class="sxs-lookup"><span data-stu-id="0c2be-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="0c2be-162">В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="0c2be-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="0c2be-163">На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Конфигурации виртуальных источников данных Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="0c2be-164">Выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-164">Select **Results**.</span></span>

7. <span data-ttu-id="0c2be-165">Выберите запись **Источник данных Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="0c2be-166">Введите требуемые сведения для конфигурации источника данных.</span><span class="sxs-lookup"><span data-stu-id="0c2be-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="0c2be-167">**Целевой URL-адрес** : URL-адрес вашего пространства имен Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c2be-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="0c2be-168">**Код клиента** : код клиента Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="0c2be-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="0c2be-169">**Код приложения AAD** : код приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2be-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="0c2be-170">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="0c2be-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="0c2be-171">**Секрет приложения AAD** : секрет приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2be-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="0c2be-172">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="0c2be-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="0c2be-173">Нажмите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-173">Select **Save & Close**.</span></span>

   ![Источник данных Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="0c2be-175">Предоставление разрешений приложения в Human Resources</span><span class="sxs-lookup"><span data-stu-id="0c2be-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="0c2be-176">Предоставьте разрешения двум приложениям Azure AD в Human Resources:</span><span class="sxs-lookup"><span data-stu-id="0c2be-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="0c2be-177">Приложение, созданное для вашего клиента на портале Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="0c2be-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="0c2be-178">Приложение Dynamics 365 HR Virtual Entity, установленное в среде Power Apps</span><span class="sxs-lookup"><span data-stu-id="0c2be-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="0c2be-179">В Human Resources откройте страницу **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="0c2be-180">Выберите **Создать** для создания новой записи приложения:</span><span class="sxs-lookup"><span data-stu-id="0c2be-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="0c2be-181">В поле **Код клиента** введите код клиента приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2be-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="0c2be-182">В поле **Имя** введите имя приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2be-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="0c2be-183">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0c2be-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="0c2be-184">Выберите **Создать** для создания записи второго приложения:</span><span class="sxs-lookup"><span data-stu-id="0c2be-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="0c2be-185">**Код клиента** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="0c2be-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="0c2be-186">**Имя** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="0c2be-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="0c2be-187">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0c2be-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="0c2be-188">Создание виртуальных сущностей</span><span class="sxs-lookup"><span data-stu-id="0c2be-188">Generate virtual entities</span></span>

<span data-ttu-id="0c2be-189">По завершении настройки можно выбрать виртуальные сущности, которые требуется создать и включить в данном экземпляре Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="0c2be-190">В Human Resources откройте страницу **Интеграция Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="0c2be-191">Выберите вкладку **Виртуальные сущности**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="0c2be-192">Переключатель **Включить виртуальную сущность** будет установлен в значение **Да** автоматически, если все необходимые настройки завершены.</span><span class="sxs-lookup"><span data-stu-id="0c2be-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="0c2be-193">Если переключатель имеет значение **Нет** , просмотрите шаги в предыдущих разделах данного документа, чтобы выполнить настройку всех необходимых компонентов.</span><span class="sxs-lookup"><span data-stu-id="0c2be-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="0c2be-194">Выберите сущность или сущности, которые требуется создать в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="0c2be-195">Выберите **Создать/обновить**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-195">Select **Generate/refresh**.</span></span>

![Интеграция Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="0c2be-197">Проверка статуса создания сущности</span><span class="sxs-lookup"><span data-stu-id="0c2be-197">Check entity generation status</span></span>

<span data-ttu-id="0c2be-198">Виртуальные сущности создаются в Common Data Service через асинхронный фоновый процесс.</span><span class="sxs-lookup"><span data-stu-id="0c2be-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="0c2be-199">Обновления на экране процесса в центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c2be-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="0c2be-200">Подробные сведения о процессе, включая журналы ошибок, отображаются на странице **Автоматизация процесса**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="0c2be-201">В Human Resources откройте страницу **Автоматизация процесса**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="0c2be-202">Выберите вкладку **Фоновые процессы**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="0c2be-203">Выберите **Фоновый процесс асинхронной операции опроса виртуальных сущностей**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="0c2be-204">Выберите **Просмотреть самые последние результаты**.</span><span class="sxs-lookup"><span data-stu-id="0c2be-204">Select **View most recent results**.</span></span>

<span data-ttu-id="0c2be-205">В области слайд-шоу отображаются самые последние результаты выполнения для процесса.</span><span class="sxs-lookup"><span data-stu-id="0c2be-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="0c2be-206">Можно просмотреть журнал для процесса, включая все ошибки, возвращенные из Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c2be-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c2be-207">См. также</span><span class="sxs-lookup"><span data-stu-id="0c2be-207">See also</span></span>

[<span data-ttu-id="0c2be-208">Что такое Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="0c2be-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="0c2be-209">Обзора сущностей</span><span class="sxs-lookup"><span data-stu-id="0c2be-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="0c2be-210">Обзор отношений сущностей</span><span class="sxs-lookup"><span data-stu-id="0c2be-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="0c2be-211">Создание и редактирование виртуальных сущностей, содержащих данные из внешнего источника данных</span><span class="sxs-lookup"><span data-stu-id="0c2be-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="0c2be-212">Что такое порталы Power Apps?</span><span class="sxs-lookup"><span data-stu-id="0c2be-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="0c2be-213">Обзор создания приложений в Power Apps</span><span class="sxs-lookup"><span data-stu-id="0c2be-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
