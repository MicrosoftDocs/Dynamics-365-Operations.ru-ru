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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959583"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="3e1ae-104">Настройка виртуальных сущностей Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3e1ae-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3e1ae-105">Dynamics 365 Human Resources — это виртуальный источник данных в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="3e1ae-106">Он предоставляет полные операции создания, чтения, обновления и удаления (CRUD) в Common Data Service и Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="3e1ae-107">Данные для виртуальных сущностей хранятся не в Common Data Service, а в базе данных приложения.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="3e1ae-108">Чтобы включить операции CRUD для сущностей Human Resources в Common Data Service, необходимо сделать эти сущности доступными в качестве виртуальных сущностей в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="3e1ae-109">Это позволяет выполнять операции CRUD из Common Data Service и Microsoft Power Platform с данными, находящимися в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="3e1ae-110">Операции также поддерживают полные проверки бизнес-логики Human Resources для обеспечения целостности данных при записи данных в сущности.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="3e1ae-111">Доступные виртуальные сущности для Human Resources</span><span class="sxs-lookup"><span data-stu-id="3e1ae-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="3e1ae-112">Все сущности Open Data Protocol (OData) в приложении Human Resources доступны как виртуальные сущности в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="3e1ae-113">Они также доступны в Power Platform.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-113">They're also available in Power Platform.</span></span> <span data-ttu-id="3e1ae-114">Теперь можно создавать приложения и взаимодействие с данными непосредственно из модуля Human Resources, используя полные возможности CRUD, без копирования или синхронизации данных с Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="3e1ae-115">Порталы Power Apps можно использовать для создания веб-сайтов с внешним интерфейсом, которые позволяют выполнять сценарии совместной работы в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="3e1ae-116">Можно просмотреть список виртуальных сущностей, включенных в среде, и начать работу с сущностями в [Power Apps](https://make.powerapps.com), в решении **Виртуальные сущности Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Виртуальные сущности Dynamics 365 HR в Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="3e1ae-118">Сравнение виртуальных и естественных сущностей</span><span class="sxs-lookup"><span data-stu-id="3e1ae-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="3e1ae-119">Виртуальные сущности для приложения Human Resources не совпадают с естественными сущностями Common Data Service, созданными для приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="3e1ae-120">Естественные сущности для приложения Human Resources создаются отдельно и поддерживаются в общем решении HCM в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="3e1ae-121">В случае естественных сущностей данные хранятся в Common Data Service и требуют синхронизации с базой данных приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="3e1ae-122">Список естественных сущностей Common Data Service для решения Human Resources см. в разделе [Сущности Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="3e1ae-123">Настройка</span><span class="sxs-lookup"><span data-stu-id="3e1ae-123">Setup</span></span>

<span data-ttu-id="3e1ae-124">Для включения виртуальных сущностей в среде выполните следующие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="3e1ae-125">Регистрация приложения в Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="3e1ae-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="3e1ae-126">Прежде всего необходимо зарегистрировать приложение на портале Azure, чтобы платформа идентификации Microsoft могла предоставлять службы проверки подлинности и авторизации для приложения и пользователей.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="3e1ae-127">Дополнительные сведения о регистрации приложений в Azure см. в разделе [Краткое руководство: регистрация приложения на платформе идентификации Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="3e1ae-128">Откройте [портал Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="3e1ae-129">В списке служб Azure выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="3e1ae-130">Выберите **Создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-130">Select **New registration**.</span></span>

4. <span data-ttu-id="3e1ae-131">В поле **Имя** введите описательное имя для приложения.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="3e1ae-132">Например, **Виртуальные сущности Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="3e1ae-133">В поле **URI перенаправления** введите URL-адрес пространства имен вашего экземпляра Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="3e1ae-134">Выберите **Регистр**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-134">Select **Register**.</span></span>

7. <span data-ttu-id="3e1ae-135">После завершения регистрации портал Azure отображает область **Обзор** регистрации приложения, которая содержит **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="3e1ae-136">На этом этапе запишите **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="3e1ae-137">Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="3e1ae-138">В левой области навигации выберите **Сертификаты и секреты**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="3e1ae-139">В разделе **Секреты клиентов** этой страницы выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="3e1ae-140">Введите описание, выберите продолжительность и выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="3e1ae-141">Запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-141">Record the secret's value.</span></span> <span data-ttu-id="3e1ae-142">Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3e1ae-143">На этом этапе обязательно запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="3e1ae-144">Секрет никогда не отображается снова после выхода с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="3e1ae-145">Установка приложения Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="3e1ae-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="3e1ae-146">Установите приложение Dynamics 365 HR Virtual Entity в своей среде Power Apps, чтобы развернуть пакет решения виртуальных сущностей в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="3e1ae-147">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3e1ae-148">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="3e1ae-149">В разделе **Ресурсы** этой страницы выберите **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="3e1ae-150">Выберите действие **Установить приложение**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="3e1ae-151">Выберите **Dynamics 365 HR Virtual Entity**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="3e1ae-152">Просмотрите и отметьте, чтобы принять условия обслуживания.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="3e1ae-153">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-153">Select **Install**.</span></span>

<span data-ttu-id="3e1ae-154">Установка занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-154">The install takes a few minutes.</span></span> <span data-ttu-id="3e1ae-155">После завершения переходите к следующим шагам.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-155">When it completes, continue to the next steps.</span></span>

![Установка приложения Dynamics 365 HR Virtual Entity с помощью центра администрирования Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="3e1ae-157">Настройка источника данных виртуальной сущности</span><span class="sxs-lookup"><span data-stu-id="3e1ae-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="3e1ae-158">Следующим шагом является настройка источника данных виртуальных сущностей в среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="3e1ae-159">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3e1ae-160">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="3e1ae-161">Выберите **URL-адрес среды** в разделе **Сведения** на странице.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="3e1ae-162">В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="3e1ae-163">На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Конфигурации виртуальных источников данных Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="3e1ae-164">Выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-164">Select **Results**.</span></span>

7. <span data-ttu-id="3e1ae-165">Выберите запись **Источник данных Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="3e1ae-166">Введите требуемые сведения для конфигурации источника данных.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="3e1ae-167">**Целевой URL-адрес**: URL-адрес вашего пространства имен Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="3e1ae-168">**Код клиента**: код клиента Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="3e1ae-169">**Код приложения AAD**: код приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="3e1ae-170">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="3e1ae-171">**Секрет приложения AAD**: секрет приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="3e1ae-172">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="3e1ae-173">Нажмите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-173">Select **Save & Close**.</span></span>

   ![Источник данных Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="3e1ae-175">Предоставление разрешений приложения в Human Resources</span><span class="sxs-lookup"><span data-stu-id="3e1ae-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="3e1ae-176">Предоставьте разрешения двум приложениям Azure AD в Human Resources:</span><span class="sxs-lookup"><span data-stu-id="3e1ae-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="3e1ae-177">Приложение, созданное для вашего клиента на портале Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="3e1ae-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="3e1ae-178">Приложение Dynamics 365 HR Virtual Entity, установленное в среде Power Apps</span><span class="sxs-lookup"><span data-stu-id="3e1ae-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="3e1ae-179">В Human Resources откройте страницу **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="3e1ae-180">Выберите **Создать** для создания новой записи приложения:</span><span class="sxs-lookup"><span data-stu-id="3e1ae-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="3e1ae-181">В поле **Код клиента** введите код клиента приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="3e1ae-182">В поле **Имя** введите имя приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="3e1ae-183">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="3e1ae-184">Выберите **Создать** для создания записи второго приложения:</span><span class="sxs-lookup"><span data-stu-id="3e1ae-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="3e1ae-185">**Код клиента**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="3e1ae-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="3e1ae-186">**Имя**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="3e1ae-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="3e1ae-187">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="3e1ae-188">Создание виртуальных сущностей</span><span class="sxs-lookup"><span data-stu-id="3e1ae-188">Generate virtual entities</span></span>

<span data-ttu-id="3e1ae-189">По завершении настройки можно выбрать виртуальные сущности, которые требуется создать и включить в данном экземпляре Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="3e1ae-190">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3e1ae-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3e1ae-191">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="3e1ae-192">Выберите **URL-адрес среды** в разделе **Сведения** на странице.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="3e1ae-193">В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="3e1ae-194">На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Доступные сущности HR**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="3e1ae-195">Воспользуйтесь параметрами фильтра, чтобы найти сущности или сущности, которые требуется включить.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="3e1ae-196">Выберите сущность в списке.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="3e1ae-197">На странице сущности измените значение свойства **Создана** на **Да** для сущности.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="3e1ae-198">Сохраните и закройте страницу сущности.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="3e1ae-199">Можно создать сразу несколько виртуальных сущностей, используя страницу **Изменение нескольких записей**.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="3e1ae-200">Выберите несколько записей на странице и нажмите кнопку **Изменить** на ленте.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="3e1ae-201">Затем можно изменить свойство **Создана** для всех выбранных записей.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Доступные сущности HR](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="3e1ae-203">Для упрощения процесса создания виртуальных сущностей в будущих выпусках процесс будет выполняться на странице в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3e1ae-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e1ae-204">См. также</span><span class="sxs-lookup"><span data-stu-id="3e1ae-204">See also</span></span>

[<span data-ttu-id="3e1ae-205">Что такое Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="3e1ae-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="3e1ae-206">Обзора сущностей</span><span class="sxs-lookup"><span data-stu-id="3e1ae-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="3e1ae-207">Обзор отношений сущностей</span><span class="sxs-lookup"><span data-stu-id="3e1ae-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="3e1ae-208">Создание и редактирование виртуальных сущностей, содержащих данные из внешнего источника данных</span><span class="sxs-lookup"><span data-stu-id="3e1ae-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="3e1ae-209">Что такое порталы Power Apps?</span><span class="sxs-lookup"><span data-stu-id="3e1ae-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="3e1ae-210">Обзор создания приложений в Power Apps</span><span class="sxs-lookup"><span data-stu-id="3e1ae-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
