---
title: Настройка виртуальных сущностей Common Data Service
description: В этом разделе показано, как настроить виртуальные сущности для Dynamics 365 Human Resources. Создание и обновление существующих виртуальных сущностей и анализ созданных и доступных сущностей.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645609"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="27e18-104">Настройка виртуальных сущностей Common Data Service</span><span class="sxs-lookup"><span data-stu-id="27e18-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="27e18-105">Dynamics 365 Human Resources — это виртуальный источник данных в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="27e18-106">Он предоставляет полные операции создания, чтения, обновления и удаления (CRUD) в Common Data Service и Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="27e18-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="27e18-107">Данные для виртуальных сущностей хранятся не в Common Data Service, а в базе данных приложения.</span><span class="sxs-lookup"><span data-stu-id="27e18-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="27e18-108">Чтобы включить операции CRUD для сущностей Human Resources в Common Data Service, необходимо сделать эти сущности доступными в качестве виртуальных сущностей в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="27e18-109">Это позволяет выполнять операции CRUD из Common Data Service и Microsoft Power Platform с данными, находящимися в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="27e18-110">Операции также поддерживают полные проверки бизнес-логики Human Resources для обеспечения целостности данных при записи данных в сущности.</span><span class="sxs-lookup"><span data-stu-id="27e18-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="27e18-111">Доступные виртуальные сущности для Human Resources</span><span class="sxs-lookup"><span data-stu-id="27e18-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="27e18-112">Все сущности Open Data Protocol (OData) в приложении Human Resources доступны как виртуальные сущности в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="27e18-113">Они также доступны в Power Platform.</span><span class="sxs-lookup"><span data-stu-id="27e18-113">They're also available in Power Platform.</span></span> <span data-ttu-id="27e18-114">Теперь можно создавать приложения и взаимодействие с данными непосредственно из модуля Human Resources, используя полные возможности CRUD, без копирования или синхронизации данных с Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="27e18-115">Порталы Power Apps можно использовать для создания веб-сайтов с внешним интерфейсом, которые позволяют выполнять сценарии совместной работы в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="27e18-116">Можно просмотреть список виртуальных сущностей, включенных в среде, и начать работу с сущностями в [Power Apps](https://make.powerapps.com), в решении **Виртуальные сущности Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="27e18-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Виртуальные сущности Dynamics 365 HR в Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="27e18-118">Сравнение виртуальных и естественных сущностей</span><span class="sxs-lookup"><span data-stu-id="27e18-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="27e18-119">Виртуальные сущности для приложения Human Resources не совпадают с естественными сущностями Common Data Service, созданными для приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="27e18-120">Естественные сущности для приложения Human Resources создаются отдельно и поддерживаются в общем решении HCM в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="27e18-121">В случае естественных сущностей данные хранятся в Common Data Service и требуют синхронизации с базой данных приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="27e18-122">Список естественных сущностей Common Data Service для решения Human Resources см. в разделе [Сущности Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="27e18-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="27e18-123">Настройка</span><span class="sxs-lookup"><span data-stu-id="27e18-123">Setup</span></span>

<span data-ttu-id="27e18-124">Для включения виртуальных сущностей в среде выполните следующие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="27e18-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="27e18-125">Включение виртуальных сущностей в Human Resources</span><span class="sxs-lookup"><span data-stu-id="27e18-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="27e18-126">Сначала необходимо включить виртуальные объекты в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="27e18-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="27e18-127">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="27e18-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="27e18-128">Выберите плитку **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="27e18-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="27e18-129">Выберите **Поддержка виртуальных сущностей в HR/CDS**, а затем выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="27e18-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="27e18-130">Дополнительные сведения о включении и отключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="27e18-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="27e18-131">Регистрация приложения в Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="27e18-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="27e18-132">Необходимо зарегистрировать ваш экземпляр Human Resources на портале Azure, чтобы платформа идентификации Microsoft могла предоставлять службы проверки подлинности и авторизации для приложения и пользователей.</span><span class="sxs-lookup"><span data-stu-id="27e18-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="27e18-133">Дополнительные сведения о регистрации приложений в Azure см. в разделе [Краткое руководство: регистрация приложения на платформе идентификации Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="27e18-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="27e18-134">Откройте [портал Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="27e18-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="27e18-135">В списке служб Azure выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="27e18-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="27e18-136">Выберите **Создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="27e18-136">Select **New registration**.</span></span>

4. <span data-ttu-id="27e18-137">В поле **Имя** введите описательное имя для приложения.</span><span class="sxs-lookup"><span data-stu-id="27e18-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="27e18-138">Например, **Виртуальные сущности Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="27e18-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="27e18-139">В поле **URI перенаправления** введите URL-адрес пространства имен вашего экземпляра Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="27e18-140">Выберите **Регистр**.</span><span class="sxs-lookup"><span data-stu-id="27e18-140">Select **Register**.</span></span>

7. <span data-ttu-id="27e18-141">После завершения регистрации портал Azure отображает область **Обзор** регистрации приложения, которая содержит **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="27e18-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="27e18-142">На этом этапе запишите **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="27e18-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="27e18-143">Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="27e18-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="27e18-144">В левой области навигации выберите **Сертификаты и секреты**.</span><span class="sxs-lookup"><span data-stu-id="27e18-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="27e18-145">В разделе **Секреты клиентов** этой страницы выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="27e18-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="27e18-146">Введите описание, выберите продолжительность и выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="27e18-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="27e18-147">Запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="27e18-147">Record the secret's value.</span></span> <span data-ttu-id="27e18-148">Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="27e18-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="27e18-149">На этом этапе обязательно запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="27e18-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="27e18-150">Секрет никогда не отображается снова после выхода с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="27e18-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="27e18-151">Установка приложения Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="27e18-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="27e18-152">Установите приложение Dynamics 365 HR Virtual Entity в своей среде Power Apps, чтобы развернуть пакет решения виртуальных сущностей в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="27e18-153">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="27e18-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="27e18-154">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="27e18-155">В разделе **Ресурсы** этой страницы выберите **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="27e18-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="27e18-156">Выберите действие **Установить приложение**.</span><span class="sxs-lookup"><span data-stu-id="27e18-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="27e18-157">Выберите **Dynamics 365 HR Virtual Entity**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="27e18-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="27e18-158">Просмотрите и отметьте, чтобы принять условия обслуживания.</span><span class="sxs-lookup"><span data-stu-id="27e18-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="27e18-159">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="27e18-159">Select **Install**.</span></span>

<span data-ttu-id="27e18-160">Установка занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="27e18-160">The install takes a few minutes.</span></span> <span data-ttu-id="27e18-161">После завершения переходите к следующим шагам.</span><span class="sxs-lookup"><span data-stu-id="27e18-161">When it completes, continue to the next steps.</span></span>

![Установка приложения Dynamics 365 HR Virtual Entity с помощью центра администрирования Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="27e18-163">Настройка источника данных виртуальной сущности</span><span class="sxs-lookup"><span data-stu-id="27e18-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="27e18-164">Следующим шагом является настройка источника данных виртуальных сущностей в среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="27e18-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="27e18-165">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="27e18-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="27e18-166">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="27e18-167">Выберите **URL-адрес среды** в разделе **Сведения** на странице.</span><span class="sxs-lookup"><span data-stu-id="27e18-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="27e18-168">В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="27e18-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="27e18-169">На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Конфигурации виртуальных источников данных Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="27e18-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="27e18-170">Выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="27e18-170">Select **Results**.</span></span>

7. <span data-ttu-id="27e18-171">Выберите запись **Источник данных Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="27e18-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="27e18-172">Введите требуемые сведения для конфигурации источника данных:</span><span class="sxs-lookup"><span data-stu-id="27e18-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="27e18-173">**Целевой URL-адрес**: URL-адрес вашего пространства имен Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27e18-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="27e18-174">Формат целевого URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="27e18-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="27e18-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="27e18-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="27e18-176">Пример:</span><span class="sxs-lookup"><span data-stu-id="27e18-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="27e18-177">Не забудьте включить символ "**/**" в конце URL-адреса, чтобы избежать возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="27e18-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="27e18-178">**Код клиента**: код клиента Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="27e18-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="27e18-179">**Код приложения AAD**: код приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27e18-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="27e18-180">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="27e18-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="27e18-181">**Секрет приложения AAD**: секрет приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27e18-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="27e18-182">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="27e18-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Источник данных Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="27e18-184">Нажмите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="27e18-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="27e18-185">Предоставление разрешений приложения в Human Resources</span><span class="sxs-lookup"><span data-stu-id="27e18-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="27e18-186">Предоставьте разрешения двум приложениям Azure AD в Human Resources:</span><span class="sxs-lookup"><span data-stu-id="27e18-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="27e18-187">Приложение, созданное для вашего клиента на портале Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="27e18-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="27e18-188">Приложение Dynamics 365 HR Virtual Entity, установленное в среде Power Apps</span><span class="sxs-lookup"><span data-stu-id="27e18-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="27e18-189">В Human Resources откройте страницу **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="27e18-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="27e18-190">Выберите **Создать** для создания новой записи приложения:</span><span class="sxs-lookup"><span data-stu-id="27e18-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="27e18-191">В поле **Код клиента** введите код клиента приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27e18-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="27e18-192">В поле **Имя** введите имя приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27e18-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="27e18-193">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="27e18-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="27e18-194">Выберите **Создать** для создания записи второго приложения:</span><span class="sxs-lookup"><span data-stu-id="27e18-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="27e18-195">**Код клиента**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="27e18-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="27e18-196">**Имя**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="27e18-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="27e18-197">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="27e18-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="27e18-198">Создание виртуальных сущностей</span><span class="sxs-lookup"><span data-stu-id="27e18-198">Generate virtual entities</span></span>

<span data-ttu-id="27e18-199">По завершении настройки можно выбрать виртуальные сущности, которые требуется создать и включить в данном экземпляре Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="27e18-200">В Human Resources откройте страницу **Интеграция Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="27e18-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="27e18-201">Выберите вкладку **Виртуальные сущности**.</span><span class="sxs-lookup"><span data-stu-id="27e18-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="27e18-202">Переключатель **Включить виртуальную сущность** будет установлен в значение **Да** автоматически, если все необходимые настройки завершены.</span><span class="sxs-lookup"><span data-stu-id="27e18-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="27e18-203">Если переключатель имеет значение **Нет**, просмотрите шаги в предыдущих разделах данного документа, чтобы выполнить настройку всех необходимых компонентов.</span><span class="sxs-lookup"><span data-stu-id="27e18-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="27e18-204">Выберите сущность или сущности, которые требуется создать в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="27e18-205">Выберите **Создать/обновить**.</span><span class="sxs-lookup"><span data-stu-id="27e18-205">Select **Generate/refresh**.</span></span>

![Интеграция Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="27e18-207">Проверка статуса создания сущности</span><span class="sxs-lookup"><span data-stu-id="27e18-207">Check entity generation status</span></span>

<span data-ttu-id="27e18-208">Виртуальные сущности создаются в Common Data Service через асинхронный фоновый процесс.</span><span class="sxs-lookup"><span data-stu-id="27e18-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="27e18-209">Обновления на экране процесса в центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="27e18-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="27e18-210">Подробные сведения о процессе, включая журналы ошибок, отображаются на странице **Автоматизация процесса**.</span><span class="sxs-lookup"><span data-stu-id="27e18-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="27e18-211">В Human Resources откройте страницу **Автоматизация процесса**.</span><span class="sxs-lookup"><span data-stu-id="27e18-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="27e18-212">Выберите вкладку **Фоновые процессы**.</span><span class="sxs-lookup"><span data-stu-id="27e18-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="27e18-213">Выберите **Фоновый процесс асинхронной операции опроса виртуальных сущностей**.</span><span class="sxs-lookup"><span data-stu-id="27e18-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="27e18-214">Выберите **Просмотреть самые последние результаты**.</span><span class="sxs-lookup"><span data-stu-id="27e18-214">Select **View most recent results**.</span></span>

<span data-ttu-id="27e18-215">В области слайд-шоу отображаются самые последние результаты выполнения для процесса.</span><span class="sxs-lookup"><span data-stu-id="27e18-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="27e18-216">Можно просмотреть журнал для процесса, включая все ошибки, возвращенные из Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27e18-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="27e18-217">См. также</span><span class="sxs-lookup"><span data-stu-id="27e18-217">See also</span></span>

[<span data-ttu-id="27e18-218">Что такое Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="27e18-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="27e18-219">Обзора сущностей</span><span class="sxs-lookup"><span data-stu-id="27e18-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="27e18-220">Обзор отношений сущностей</span><span class="sxs-lookup"><span data-stu-id="27e18-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="27e18-221">Создание и редактирование виртуальных сущностей, содержащих данные из внешнего источника данных</span><span class="sxs-lookup"><span data-stu-id="27e18-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="27e18-222">Что такое порталы Power Apps?</span><span class="sxs-lookup"><span data-stu-id="27e18-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="27e18-223">Обзор создания приложений в Power Apps</span><span class="sxs-lookup"><span data-stu-id="27e18-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
