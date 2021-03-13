---
title: Настройка виртуальных таблиц Dataverse
description: В этом разделе показано, как настроить виртуальные таблицы для Dynamics 365 Human Resources. Создание и обновление существующих виртуальных таблиц и анализ созданных и доступных таблиц.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: cd299b51e38cc30c3e18f3ef9de1f43fa817b840
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114047"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="9c09a-104">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="9c09a-104">Configure Dataverse virtual tables</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9c09a-105">Dynamics 365 Human Resources — это виртуальный источник данных в Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="9c09a-106">Он предоставляет полные операции создания, чтения, обновления и удаления (CRUD) в Dataverse и Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="9c09a-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="9c09a-107">Данные для виртуальных таблиц хранятся не в Dataverse, а в базе данных приложения.</span><span class="sxs-lookup"><span data-stu-id="9c09a-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="9c09a-108">Чтобы включить операции CRUD для сущностей Human Resources в Dataverse, необходимо сделать эти сущности доступными в качестве виртуальных таблиц в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="9c09a-109">Это позволяет выполнять операции CRUD из Dataverse и Microsoft Power Platform с данными, находящимися в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="9c09a-110">Операции также поддерживают полные проверки бизнес-логики Human Resources для обеспечения целостности данных при записи данных в сущности.</span><span class="sxs-lookup"><span data-stu-id="9c09a-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="9c09a-111">Сущности Human Resources соответствуют таблицам Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="9c09a-112">Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="9c09a-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="9c09a-113">Доступные виртуальные таблицы для Human Resources</span><span class="sxs-lookup"><span data-stu-id="9c09a-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="9c09a-114">Все сущности Open Data Protocol (OData) в приложении Human Resources доступны как виртуальные таблицы в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="9c09a-115">Они также доступны в Power Platform.</span><span class="sxs-lookup"><span data-stu-id="9c09a-115">They're also available in Power Platform.</span></span> <span data-ttu-id="9c09a-116">Теперь можно создавать приложения и взаимодействие с данными непосредственно из модуля Human Resources, используя полные возможности CRUD, без копирования или синхронизации данных с Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="9c09a-117">Порталы Power Apps можно использовать для создания веб-сайтов с внешним интерфейсом, которые позволяют выполнять сценарии совместной работы в приложении Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="9c09a-118">Можно просмотреть список виртуальных таблиц, включенных в среде, и начать работу с таблицами в [Power Apps](https://make.powerapps.com), в решении **Виртуальные таблицы Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Виртуальные таблицы Dynamics 365 HR в Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="9c09a-120">Виртуальные таблицы и собственные таблицы</span><span class="sxs-lookup"><span data-stu-id="9c09a-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="9c09a-121">Виртуальные таблицы для приложения Human Resources не совпадают с собственными таблицами Dataverse, созданными для приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="9c09a-122">Собственные таблицы для приложения Human Resources создаются отдельно и поддерживаются в общем решении HCM в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="9c09a-123">В случае собстивенных таблиц данные хранятся в Dataverse и требуют синхронизации с базой данных приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="9c09a-124">Список собственный таблиц Dataverse для решения Human Resources см. в разделе [Таблицы Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="9c09a-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="9c09a-125">Настройка</span><span class="sxs-lookup"><span data-stu-id="9c09a-125">Setup</span></span>

<span data-ttu-id="9c09a-126">Для включения виртуальных таблиц в среде выполните следующие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="9c09a-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="9c09a-127">Включение виртуальных таблиц в Human Resources</span><span class="sxs-lookup"><span data-stu-id="9c09a-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="9c09a-128">Сначала необходимо включить виртуальные таблицы в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="9c09a-129">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="9c09a-130">Выберите плитку **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="9c09a-131">Выберите **Поддержка виртуальных таблиц в Dataverse**, а затем выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="9c09a-132">Дополнительные сведения о включении и отключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="9c09a-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="9c09a-133">Регистрация приложения в Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9c09a-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="9c09a-134">Необходимо зарегистрировать ваш экземпляр Human Resources на портале Azure, чтобы платформа идентификации Microsoft могла предоставлять службы проверки подлинности и авторизации для приложения и пользователей.</span><span class="sxs-lookup"><span data-stu-id="9c09a-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="9c09a-135">Дополнительные сведения о регистрации приложений в Azure см. в разделе [Краткое руководство: регистрация приложения на платформе идентификации Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="9c09a-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="9c09a-136">Откройте [портал Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9c09a-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="9c09a-137">В списке служб Azure выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="9c09a-138">Выберите **Создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-138">Select **New registration**.</span></span>

4. <span data-ttu-id="9c09a-139">В поле **Имя** введите описательное имя для приложения.</span><span class="sxs-lookup"><span data-stu-id="9c09a-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="9c09a-140">Например, **Виртуальные таблицы Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="9c09a-141">В поле **URI перенаправления** введите URL-адрес пространства имен вашего экземпляра Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="9c09a-142">Выберите **Регистр**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-142">Select **Register**.</span></span>

7. <span data-ttu-id="9c09a-143">После завершения регистрации портал Azure отображает область **Обзор** регистрации приложения, которая содержит **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="9c09a-144">На этом этапе запишите **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="9c09a-145">Эти сведения будут введены при [настройке источника данных виртуальной таблицы](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="9c09a-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="9c09a-146">В левой области навигации выберите **Сертификаты и секреты**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="9c09a-147">В разделе **Секреты клиентов** этой страницы выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="9c09a-148">Введите описание, выберите продолжительность и выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="9c09a-149">Запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="9c09a-149">Record the secret's value.</span></span> <span data-ttu-id="9c09a-150">Эти сведения будут введены при [настройке источника данных виртуальной таблицы](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="9c09a-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9c09a-151">На этом этапе обязательно запишите значение секрета.</span><span class="sxs-lookup"><span data-stu-id="9c09a-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="9c09a-152">Секрет никогда не отображается снова после выхода с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="9c09a-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="9c09a-153">Установка приложения Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="9c09a-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="9c09a-154">Установите приложение Dynamics 365 HR Virtual Table в своей среде Power Apps, чтобы развернуть пакет решения виртуальных таблиц в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="9c09a-155">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9c09a-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="9c09a-156">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="9c09a-157">В разделе **Ресурсы** этой страницы выберите **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="9c09a-158">Выберите действие **Установить приложение**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="9c09a-159">Выберите **Dynamics 365 HR Virtual Table**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="9c09a-160">Просмотрите и отметьте, чтобы принять условия обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9c09a-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="9c09a-161">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-161">Select **Install**.</span></span>

<span data-ttu-id="9c09a-162">Установка занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="9c09a-162">The install takes a few minutes.</span></span> <span data-ttu-id="9c09a-163">После завершения переходите к следующим шагам.</span><span class="sxs-lookup"><span data-stu-id="9c09a-163">When it completes, continue to the next steps.</span></span>

![Установка приложения Dynamics 365 HR Virtual Table с помощью центра администрирования Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="9c09a-165">Настройка источника данных виртуальной таблицы</span><span class="sxs-lookup"><span data-stu-id="9c09a-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="9c09a-166">Следующим шагом является настройка источника данных виртуальных таблиц в среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9c09a-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="9c09a-167">Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9c09a-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="9c09a-168">В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="9c09a-169">Выберите **URL-адрес среды** в разделе **Сведения** на странице.</span><span class="sxs-lookup"><span data-stu-id="9c09a-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="9c09a-170">В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="9c09a-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="9c09a-171">На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Конфигурации виртуальных источников данных Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="9c09a-172">Выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-172">Select **Results**.</span></span>

7. <span data-ttu-id="9c09a-173">Выберите запись **Источник данных Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="9c09a-174">Введите требуемые сведения для конфигурации источника данных:</span><span class="sxs-lookup"><span data-stu-id="9c09a-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="9c09a-175">**Целевой URL-адрес**: URL-адрес вашего пространства имен Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9c09a-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="9c09a-176">Формат целевого URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="9c09a-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="9c09a-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="9c09a-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="9c09a-178">Пример:</span><span class="sxs-lookup"><span data-stu-id="9c09a-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="9c09a-179">Не забудьте включить символ "**/**" в конце URL-адреса, чтобы избежать возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c09a-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="9c09a-180">**Код клиента**: код клиента Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="9c09a-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="9c09a-181">**Код приложения AAD**: код приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c09a-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="9c09a-182">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="9c09a-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="9c09a-183">**Секрет приложения AAD**: секрет приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c09a-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="9c09a-184">Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="9c09a-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Источник данных Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="9c09a-186">Нажмите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="9c09a-187">Предоставление разрешений приложения в Human Resources</span><span class="sxs-lookup"><span data-stu-id="9c09a-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="9c09a-188">Предоставьте разрешения двум приложениям Azure AD в Human Resources:</span><span class="sxs-lookup"><span data-stu-id="9c09a-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="9c09a-189">Приложение, созданное для вашего клиента на портале Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9c09a-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="9c09a-190">Приложение Dynamics 365 HR Virtual Table, установленное в среде Power Apps</span><span class="sxs-lookup"><span data-stu-id="9c09a-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="9c09a-191">В Human Resources откройте страницу **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="9c09a-192">Выберите **Создать** для создания новой записи приложения:</span><span class="sxs-lookup"><span data-stu-id="9c09a-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="9c09a-193">В поле **Код клиента** введите код клиента приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c09a-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="9c09a-194">В поле **Имя** введите имя приложения, зарегистрированного на портале Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c09a-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="9c09a-195">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9c09a-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="9c09a-196">Выберите **Создать** для создания записи второго приложения:</span><span class="sxs-lookup"><span data-stu-id="9c09a-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="9c09a-197">**Код клиента**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="9c09a-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="9c09a-198">**Имя**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="9c09a-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="9c09a-199">В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9c09a-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="9c09a-200">Создание виртуальных таблиц</span><span class="sxs-lookup"><span data-stu-id="9c09a-200">Generate virtual tables</span></span>

<span data-ttu-id="9c09a-201">По завершении настройки можно выбрать виртуальные таблицы, которые требуется создать и включить в данном экземпляре Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="9c09a-202">В Human Resources откройте страницу **Интеграция Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="9c09a-203">Выберите вкладку **Виртуальные таблицы**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="9c09a-204">Переключатель **Включить виртуальные таблицы** будет установлен в значение **Да** автоматически, если все необходимые настройки завершены.</span><span class="sxs-lookup"><span data-stu-id="9c09a-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="9c09a-205">Если переключатель имеет значение **Нет**, просмотрите шаги в предыдущих разделах данного документа, чтобы выполнить настройку всех необходимых компонентов.</span><span class="sxs-lookup"><span data-stu-id="9c09a-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="9c09a-206">Выберите таблицу или таблицы, которые требуется создать в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="9c09a-207">Выберите **Создать/обновить**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-207">Select **Generate/refresh**.</span></span>

![Интеграция Dataverse](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="9c09a-209">Проверка статуса создания таблицы</span><span class="sxs-lookup"><span data-stu-id="9c09a-209">Check table generation status</span></span>

<span data-ttu-id="9c09a-210">Виртуальные таблицы создаются в Dataverse через асинхронный фоновый процесс.</span><span class="sxs-lookup"><span data-stu-id="9c09a-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="9c09a-211">Обновления на экране процесса в центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9c09a-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="9c09a-212">Подробные сведения о процессе, включая журналы ошибок, отображаются на странице **Автоматизация процесса**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="9c09a-213">В Human Resources откройте страницу **Автоматизация процесса**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="9c09a-214">Выберите вкладку **Фоновые процессы**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="9c09a-215">Выберите **Фоновый процесс асинхронной операции опроса виртуальных таблиц**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="9c09a-216">Выберите **Просмотреть самые последние результаты**.</span><span class="sxs-lookup"><span data-stu-id="9c09a-216">Select **View most recent results**.</span></span>

<span data-ttu-id="9c09a-217">В области слайд-шоу отображаются самые последние результаты выполнения для процесса.</span><span class="sxs-lookup"><span data-stu-id="9c09a-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="9c09a-218">Можно просмотреть журнал для процесса, включая все ошибки, возвращенные из Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c09a-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c09a-219">См. также</span><span class="sxs-lookup"><span data-stu-id="9c09a-219">See also</span></span>

[<span data-ttu-id="9c09a-220">Что такое Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9c09a-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="9c09a-221">Таблицы в Dataverse</span><span class="sxs-lookup"><span data-stu-id="9c09a-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="9c09a-222">Обзор отношений таблиц</span><span class="sxs-lookup"><span data-stu-id="9c09a-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="9c09a-223">Создание и редактирование виртуальных таблиц, содержащих данные из внешнего источника данных</span><span class="sxs-lookup"><span data-stu-id="9c09a-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="9c09a-224">Что такое порталы Power Apps?</span><span class="sxs-lookup"><span data-stu-id="9c09a-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="9c09a-225">Обзор создания приложений в Power Apps</span><span class="sxs-lookup"><span data-stu-id="9c09a-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
