---
title: Конфигурация для Finance Insights — версии до 10.0.19
description: В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в Finance Insights для версий до 10.0.19.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186428"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="603d8-103">Конфигурация для финансового анализа (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="603d8-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="603d8-104">Следующие процедуры настройки Finance Insights действительны для версий Microsoft Dynamics 365 Finance до 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="603d8-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="603d8-105">Чтобы настроить Finance Insights в версии 10.0.20 и позже, см. раздел [Настройка для Finance Insights (предварительная версия) — версии 10.0.20 и старше](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="603d8-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="603d8-106">Финансовый анализ сочетает в себе функции из Microsoft Dynamics 365 Finance с Microsoft Dataverse, Azure и AI Builder, чтобы предоставить мощные средства прогнозирования для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="603d8-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="603d8-107">В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="603d8-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="603d8-108">Разверните Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="603d8-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="603d8-109">Разверните среды, выполнив следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="603d8-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="603d8-110">В Microsoft Dynamics Lifecycle Services (LCS) создайте или обновите среду Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="603d8-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="603d8-111">Среде требуется версия приложения 10.0.11/Platform Update 35 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="603d8-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="603d8-112">Среда должна быть средой с высокой доступностью (HA) в песочнице.</span><span class="sxs-lookup"><span data-stu-id="603d8-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="603d8-113">(Этот тип среды также известен как среда уровня 2.) Дополнительные сведения см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="603d8-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="603d8-114">При настройке Finance Insights в среде песочницы, возможно, потребуется скопировать в эту среду производственные данные, чтобы прогнозы работали.</span><span class="sxs-lookup"><span data-stu-id="603d8-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="603d8-115">Модель прогнозирования использует несколько лет данных для создания прогнозов.</span><span class="sxs-lookup"><span data-stu-id="603d8-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="603d8-116">Демонстрационные данные Contoso не содержат достаточно исторических данных для адекватной тренировки прогнозной модели.</span><span class="sxs-lookup"><span data-stu-id="603d8-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="603d8-117">Настроить Dataverse</span><span class="sxs-lookup"><span data-stu-id="603d8-117">Configure Dataverse</span></span>

<span data-ttu-id="603d8-118">Выполните следующие действия, чтобы настроить Dataverse для Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="603d8-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="603d8-119">Откройте страницу среды в LCS и убедитесь, что раздел **Интеграция Power Platform** уже настроен.</span><span class="sxs-lookup"><span data-stu-id="603d8-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="603d8-120">Если уже настроено, должно быть указано имя среды Dataverse, связанное со средой Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="603d8-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="603d8-121">Скопируйте имя среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="603d8-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="603d8-122">Если не настроено, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="603d8-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="603d8-123">Нажмите кнопку **Настройка** в разделе интеграции Power Platform.</span><span class="sxs-lookup"><span data-stu-id="603d8-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="603d8-124">Настройка среды может занять до часа.</span><span class="sxs-lookup"><span data-stu-id="603d8-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="603d8-125">Если среда Dataverse успешно настроена, должно быть указано имя среды Dataverse, связанной со средой Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="603d8-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="603d8-126">Скопируйте имя среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="603d8-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="603d8-127">После завершения настройки среды **НЕ ВЫБИРАЙТЕ** кнопку **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="603d8-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="603d8-128">Это не требуется для Finance Insights и отключит возможность завершения необходимых надстроек среды в LCS.</span><span class="sxs-lookup"><span data-stu-id="603d8-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="603d8-129">Откройте [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/) и выполните следующие действия, чтобы создать новую среду Dataverse в одном и том же клиенте Active Directory:</span><span class="sxs-lookup"><span data-stu-id="603d8-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="603d8-130">Откройте страницу **Среды**.</span><span class="sxs-lookup"><span data-stu-id="603d8-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="603d8-131">[![Страница сред](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="603d8-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="603d8-132">Выберите созданную выше среду Dataverse, затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="603d8-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="603d8-133">Выберите **Ресурсы \> Все устаревшие параметры**.</span><span class="sxs-lookup"><span data-stu-id="603d8-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="603d8-134">На верхней панели навигации выберите **Параметры**, а затем выберите **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="603d8-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="603d8-135">Выберите **Ресурсы разработчика**.</span><span class="sxs-lookup"><span data-stu-id="603d8-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="603d8-136">Скопируйте значение **Код организации Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="603d8-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="603d8-137">В адресной строке браузера запишите URL-адрес для организации Dataverse.</span><span class="sxs-lookup"><span data-stu-id="603d8-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="603d8-138">Например, может быть указан URL-адрес `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="603d8-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="603d8-139">Если планируется использовать функцию прогнозов движения денежных средств или прогнозов бюджета, выполните следующие действия, чтобы обновить ограничение для аннотации организации как минимум до 50 мегабайт (МБ):</span><span class="sxs-lookup"><span data-stu-id="603d8-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="603d8-140">Откройте [портал Power Apps](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="603d8-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="603d8-141">Выберите только что созданную среду, а затем выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="603d8-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="603d8-142">Выберите **Параметры \> Конфигурация электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="603d8-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="603d8-143">Измените значение поля **Максимальный размер файла** на **51200**.</span><span class="sxs-lookup"><span data-stu-id="603d8-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="603d8-144">(Это значение задается в килобайтах \[КБ\].)</span><span class="sxs-lookup"><span data-stu-id="603d8-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="603d8-145">Выберите **ОК**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="603d8-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="603d8-146">Задание настройки Azure</span><span class="sxs-lookup"><span data-stu-id="603d8-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="603d8-147">Введите код каталога Dataverse и код объекта пользователя Azure AD</span><span class="sxs-lookup"><span data-stu-id="603d8-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="603d8-148">Введите код каталога Dataverse:</span><span class="sxs-lookup"><span data-stu-id="603d8-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="603d8-149">Откройте [портал Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="603d8-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="603d8-150">Выполните вход, используя код пользователя, который использовался при создании среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="603d8-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="603d8-151">Перейдите на страницу **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="603d8-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="603d8-152">Скопируйте значение **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="603d8-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="603d8-153">Введите код объекта Azure Active Directory (Azure AD) пользователя:</span><span class="sxs-lookup"><span data-stu-id="603d8-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="603d8-154">На [портале Azure](https://portal.azure.com) перейдите в раздел **Пользователи** и выполните поиск пользователя по адресу электронной почты.</span><span class="sxs-lookup"><span data-stu-id="603d8-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="603d8-155">Выберите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="603d8-155">Select the user's name.</span></span>
    3. <span data-ttu-id="603d8-156">Скопируйте значение **Код объекта**.</span><span class="sxs-lookup"><span data-stu-id="603d8-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="603d8-157">Использование Azure Cloud Shell для настройки ресурсов Data Lake финансового анализа</span><span class="sxs-lookup"><span data-stu-id="603d8-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="603d8-158">Использование сценария Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="603d8-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="603d8-159">Был предоставлен сценарий Windows PowerShell, который позволяет легко настроить ресурсы Azure, описанные в разделе [Настройка экспорта в Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="603d8-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="603d8-160">Если вы предпочитаете выполнить настройку вручную, пропустите эту процедуру и продолжите процедуру, описанную в разделе [Настройка вручную](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="603d8-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="603d8-161">Выполните приведенные ниже шаги, чтобы выполнить сценарий PowerShell.</span><span class="sxs-lookup"><span data-stu-id="603d8-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="603d8-162">Параметр Azure CLI "Попробовать" или запуск сценария на компьютере может не работать.</span><span class="sxs-lookup"><span data-stu-id="603d8-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="603d8-163">Выполните следующие действия, чтобы настроить Azure с помощью сценария Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="603d8-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="603d8-164">Необходимо иметь права на создание группы ресурсов Azure, ресурсов Azure и приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="603d8-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="603d8-165">Сведения о необходимых разрешениях см. в разделе [Проверка разрешений Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="603d8-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="603d8-166">На [портале Azure](https://portal.azure.com) перейдите к целевой подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="603d8-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="603d8-167">Выберите кнопку **Cloud Shell** справа от поля **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="603d8-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="603d8-168">Выберите **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="603d8-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="603d8-169">В случае появлении соответствующего запроса создайте хранилище.</span><span class="sxs-lookup"><span data-stu-id="603d8-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="603d8-170">Перейдите на вкладку **Azure CLI** и выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="603d8-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="603d8-171">Откройте Блокнот и вставьте сценарий PowerShell.</span><span class="sxs-lookup"><span data-stu-id="603d8-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="603d8-172">Сохраните файл под именем ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="603d8-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="603d8-173">Отправьте сценарий Windows PowerShell в сеанс, используя команду меню для отправки в Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="603d8-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="603d8-174">Выполните сценарий .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="603d8-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="603d8-175">Следуйте инструкциям для выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="603d8-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="603d8-176">Используйте сведения из выходных данных сценария для установки надстройки **Экспорт в Data Lake** в LCS.</span><span class="sxs-lookup"><span data-stu-id="603d8-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="603d8-177">Используйте сведения из выходных данных сценария для включения хранилища сущностей на странице **Подключения данных** в Finance (**Администрирование системы \> Параметры системы \> Подключения данных**).</span><span class="sxs-lookup"><span data-stu-id="603d8-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="603d8-178">Настройка вручную</span><span class="sxs-lookup"><span data-stu-id="603d8-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="603d8-179">Добавление приложений в клиент Azure AD</span><span class="sxs-lookup"><span data-stu-id="603d8-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="603d8-180">На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="603d8-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="603d8-181">Выберите **Управление \> Корпоративные приложения**.</span><span class="sxs-lookup"><span data-stu-id="603d8-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="603d8-182">Выполните поиск следующих приложений по коду приложения.</span><span class="sxs-lookup"><span data-stu-id="603d8-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="603d8-183">Заявление</span><span class="sxs-lookup"><span data-stu-id="603d8-183">Application</span></span>                              | <span data-ttu-id="603d8-184">Код приложения</span><span class="sxs-lookup"><span data-stu-id="603d8-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="603d8-185">Микрослужбы Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="603d8-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="603d8-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="603d8-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="603d8-187">Микрослужбы Microsoft Dynamics ERP CDS</span><span class="sxs-lookup"><span data-stu-id="603d8-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="603d8-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="603d8-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="603d8-189">Служба авторизации AI Builder</span><span class="sxs-lookup"><span data-stu-id="603d8-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="603d8-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="603d8-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="603d8-191">Если не удается найти какое-либо из вышеперечисленных приложений, попробуйте выполнить следующие действия</span><span class="sxs-lookup"><span data-stu-id="603d8-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="603d8-192">На локальном компьютере выберите меню **Пуск** и выполните поиск **powershell**.</span><span class="sxs-lookup"><span data-stu-id="603d8-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="603d8-193">Выберите и удерживайте (или щелкните правой кнопкой мыши) **Windows PowerShell**, затем выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="603d8-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="603d8-194">Выполните следующую команду для установки модуля **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="603d8-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="603d8-195">Если для продолжения требуется поставщик NuGet, выберите **Y**, чтобы установить его.</span><span class="sxs-lookup"><span data-stu-id="603d8-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="603d8-196">В случае появления сообщения "Ненадежный репозиторий" выберите **Y** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="603d8-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="603d8-197">Для каждого приложения, которое необходимо добавить, выполните следующие команды, чтобы добавить приложение в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="603d8-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="603d8-198">При появлении запроса войдите в систему как администратор Azure AD.</span><span class="sxs-lookup"><span data-stu-id="603d8-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="603d8-199">Создание ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="603d8-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="603d8-200">Убедитесь, что следующие ресурсы созданы в том же экземпляре Azure AD, что и среда Dataverse.</span><span class="sxs-lookup"><span data-stu-id="603d8-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="603d8-201">Нельзя использовать ресурсы из других экземпляров Azure AD.</span><span class="sxs-lookup"><span data-stu-id="603d8-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="603d8-202">Создайте новую учетную запись хранения:</span><span class="sxs-lookup"><span data-stu-id="603d8-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="603d8-203">На [портале Azure](https://portal.azure.com) создайте учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="603d8-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="603d8-204">В диалоговом окне **Создание учетной записи хранения** установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="603d8-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="603d8-205">**Местонахождение** — выберите центр обработки данных, в котором находится среда.</span><span class="sxs-lookup"><span data-stu-id="603d8-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="603d8-206">**Производительность** — рекомендуется выбирать **Стандартная**.</span><span class="sxs-lookup"><span data-stu-id="603d8-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="603d8-207">**Вид учетной записи** — необходимо выбрать **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="603d8-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="603d8-208">В диалоговом окне **Дополнительные параметры** для параметра **Data Lake storage Gen2** выберите **Включить** в функции **Иерархические пространства имен**.</span><span class="sxs-lookup"><span data-stu-id="603d8-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="603d8-209">Если эта функция отключена, вы не сможете потреблять данные, которые приложения Finance and Operations записывают с помощью таких служб, как потоки данных Power BI.</span><span class="sxs-lookup"><span data-stu-id="603d8-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="603d8-210">Выберите **Просмотр и создание**.</span><span class="sxs-lookup"><span data-stu-id="603d8-210">Select **Review and create**.</span></span> <span data-ttu-id="603d8-211">После завершения развертывания новый ресурс будет показан на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="603d8-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="603d8-212">Перейдите к созданной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="603d8-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="603d8-213">В левом меню выберите **Ключи доступа**.</span><span class="sxs-lookup"><span data-stu-id="603d8-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="603d8-214">Скопируйте и сохраните строку подключения для **Key1** или **Key2**.</span><span class="sxs-lookup"><span data-stu-id="603d8-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="603d8-215">Скопируйте и сохраните имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="603d8-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="603d8-216">Создайте новое хранилище ключей:</span><span class="sxs-lookup"><span data-stu-id="603d8-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="603d8-217">На [портале Azure](https://portal.azure.com) создайте хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="603d8-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="603d8-218">В диалоговом окне **Создать хранилище ключей** в поле **Расположение** выберите центр обработки данных, в котором находится среда.</span><span class="sxs-lookup"><span data-stu-id="603d8-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="603d8-219">После создания хранилища ключей выберите его в списке, а затем выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="603d8-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="603d8-220">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="603d8-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="603d8-221">В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="603d8-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="603d8-222">Введите имя для секрета.</span><span class="sxs-lookup"><span data-stu-id="603d8-222">Enter a name for the secret.</span></span> <span data-ttu-id="603d8-223">Запишите имя, поскольку его потребуется указать позже.</span><span class="sxs-lookup"><span data-stu-id="603d8-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="603d8-224">В поле **Значение** введите строку подключения, полученную из учетной записи хранения в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="603d8-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="603d8-225">Выберите **Включено**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="603d8-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="603d8-226">Секрет создается и добавляется в Key Vault.</span><span class="sxs-lookup"><span data-stu-id="603d8-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="603d8-227">Перейдите в раздел **Обзор Key Vault** и запишите DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="603d8-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="603d8-228">Создание и регистрация приложения Azure AD:</span><span class="sxs-lookup"><span data-stu-id="603d8-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="603d8-229">На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**, затем выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="603d8-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="603d8-230">Выберите **Регистрация нового приложения** и задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="603d8-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="603d8-231">**Имя** — введите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="603d8-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="603d8-232">**Тип приложения** — выберите **Веб-API**.</span><span class="sxs-lookup"><span data-stu-id="603d8-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="603d8-233">**Настройка URI перенаправления** — введите URL-адрес для экземпляра Dynamics 365, например, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="603d8-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="603d8-234">Перейдите к только что созданному приложению и скопируйте его значение **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="603d8-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="603d8-235">Это значение будет необходимо ввести позднее при настройке хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="603d8-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="603d8-236">Перейдите на страницу **Разрешения API** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="603d8-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="603d8-237">Выберите **Добавить разрешение**.</span><span class="sxs-lookup"><span data-stu-id="603d8-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="603d8-238">Выберите **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="603d8-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="603d8-239">После выбора делегированных разрешений выберите **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="603d8-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="603d8-240">Выберите **Добавить разрешения**.</span><span class="sxs-lookup"><span data-stu-id="603d8-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="603d8-241">В меню приложения выберите **Сертификаты \& секреты**, затем выполните следующие действия, чтобы создать секреты для Key Vault:</span><span class="sxs-lookup"><span data-stu-id="603d8-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="603d8-242">Выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="603d8-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="603d8-243">В поле **Описание ключа** введите имя.</span><span class="sxs-lookup"><span data-stu-id="603d8-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="603d8-244">Выберите длительность, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="603d8-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="603d8-245">Секрет создается в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="603d8-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="603d8-246">Скопируйте и сохраните значение секрета.</span><span class="sxs-lookup"><span data-stu-id="603d8-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="603d8-247">Создайте секреты Key Vault:</span><span class="sxs-lookup"><span data-stu-id="603d8-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="603d8-248">Перейдите к созданному ранее хранилищу ключей и выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="603d8-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="603d8-249">Для каждого имени секрета в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="603d8-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="603d8-250">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="603d8-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="603d8-251">В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="603d8-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="603d8-252">Создайте имя и значение секрета из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="603d8-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="603d8-253">Выберите **Включено**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="603d8-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="603d8-254">Секрет создается и добавляется в Key Vault.</span><span class="sxs-lookup"><span data-stu-id="603d8-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="603d8-255">Имя секрета</span><span class="sxs-lookup"><span data-stu-id="603d8-255">Secret name</span></span>                       | <span data-ttu-id="603d8-256">Значение секрета</span><span class="sxs-lookup"><span data-stu-id="603d8-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="603d8-257">app-id</span><span class="sxs-lookup"><span data-stu-id="603d8-257">app-id</span></span>                            | <span data-ttu-id="603d8-258">Код приложения, созданного ранее</span><span class="sxs-lookup"><span data-stu-id="603d8-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="603d8-259">app-secret</span><span class="sxs-lookup"><span data-stu-id="603d8-259">app-secret</span></span>                        | <span data-ttu-id="603d8-260">Секрет клиента, который был сохранен ранее</span><span class="sxs-lookup"><span data-stu-id="603d8-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="603d8-261">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="603d8-261">storage-account-name</span></span>              | <span data-ttu-id="603d8-262">Имя созданной ранее учетной записи хранения, например **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="603d8-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="603d8-263">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="603d8-263">storage-account-connection-string</span></span> | <span data-ttu-id="603d8-264">Строка подключения, скопированная со страницы **Ключи доступа** для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="603d8-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="603d8-265">Авторизуйте приложение для доступа к хранилищу ключей:</span><span class="sxs-lookup"><span data-stu-id="603d8-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="603d8-266">На [портале Azure](https://portal.azure.com) откройте созданное ранее хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="603d8-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="603d8-267">Выберите политики доступа.</span><span class="sxs-lookup"><span data-stu-id="603d8-267">Select the access policies.</span></span>
    3. <span data-ttu-id="603d8-268">Для каждого приложения в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="603d8-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="603d8-269">Выберите **Добавить политику доступа**, чтобы создать политику доступа.</span><span class="sxs-lookup"><span data-stu-id="603d8-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="603d8-270">В поле **Разрешения секрета** выберите разрешения из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="603d8-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="603d8-271">В поле **Выберите субъект** найдите отображаемое имя приложения из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="603d8-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="603d8-272">Выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="603d8-272">Select **Select**.</span></span>
        5. <span data-ttu-id="603d8-273">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="603d8-273">Select **Add**.</span></span>
        6. <span data-ttu-id="603d8-274">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="603d8-274">Select **Save**.</span></span>

        | <span data-ttu-id="603d8-275">Заявление</span><span class="sxs-lookup"><span data-stu-id="603d8-275">Application</span></span>                                              | <span data-ttu-id="603d8-276">Права доступа</span><span class="sxs-lookup"><span data-stu-id="603d8-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="603d8-277">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="603d8-277">The display name of the new application that you created</span></span> | <span data-ttu-id="603d8-278">Получить, Список</span><span class="sxs-lookup"><span data-stu-id="603d8-278">Get, List</span></span>   |
        | <span data-ttu-id="603d8-279">**Микрослужбы Microsoft Dynamics ERP**</span><span class="sxs-lookup"><span data-stu-id="603d8-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="603d8-280">Получить, Список</span><span class="sxs-lookup"><span data-stu-id="603d8-280">Get, List</span></span>   |

6. <span data-ttu-id="603d8-281">Назначьте роли для доступа к учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="603d8-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="603d8-282">На [портале Azure](https://portal.azure.com) откройте созданную ранее учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="603d8-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="603d8-283">Выберите **Управление доступом (IAM)**, затем выберите **Назначения ролей**.</span><span class="sxs-lookup"><span data-stu-id="603d8-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="603d8-284">Выберите **Добавить, Добавить назначение ролей**.</span><span class="sxs-lookup"><span data-stu-id="603d8-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="603d8-285">Для каждого приложения в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="603d8-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="603d8-286">Выберите роль из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="603d8-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="603d8-287">В поле **Назначить доступ** оставьте значение **Пользователь, группа или субъект-служба Azure AD**</span><span class="sxs-lookup"><span data-stu-id="603d8-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="603d8-288">В поле **Выбрать** введите приложение из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="603d8-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="603d8-289">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="603d8-289">Select **Save**.</span></span>

        | <span data-ttu-id="603d8-290">Заявление</span><span class="sxs-lookup"><span data-stu-id="603d8-290">Application</span></span>                                              | <span data-ttu-id="603d8-291">Роль</span><span class="sxs-lookup"><span data-stu-id="603d8-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="603d8-292">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="603d8-292">The display name of the new application that you created</span></span> | <span data-ttu-id="603d8-293">Ответственный</span><span class="sxs-lookup"><span data-stu-id="603d8-293">Owner</span></span>                       |
        | <span data-ttu-id="603d8-294">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="603d8-294">The display name of the new application that you created</span></span> | <span data-ttu-id="603d8-295">Участник</span><span class="sxs-lookup"><span data-stu-id="603d8-295">Contributor</span></span>                 |
        | <span data-ttu-id="603d8-296">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="603d8-296">The display name of the new application that you created</span></span> | <span data-ttu-id="603d8-297">Участник учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="603d8-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="603d8-298">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="603d8-298">The display name of the new application that you created</span></span> | <span data-ttu-id="603d8-299">Владелец данных BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="603d8-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="603d8-300">**Служба авторизации AI Builder**</span><span class="sxs-lookup"><span data-stu-id="603d8-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="603d8-301">Модуль чтения данных BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="603d8-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="603d8-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="603d8-302">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="603d8-303">Настройка Data Lake</span><span class="sxs-lookup"><span data-stu-id="603d8-303">Configure the data lake</span></span>

<span data-ttu-id="603d8-304">Выполните следующие действия, чтобы использовать LCS для добавления надстройки Azure Data Lake в среду.</span><span class="sxs-lookup"><span data-stu-id="603d8-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="603d8-305">Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="603d8-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="603d8-306">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="603d8-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="603d8-307">Выберите надстройку **Экспорт в Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="603d8-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="603d8-308">Введите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="603d8-308">Enter the following values.</span></span>

    | <span data-ttu-id="603d8-309">значение</span><span class="sxs-lookup"><span data-stu-id="603d8-309">Value</span></span>                                                              | <span data-ttu-id="603d8-310">описание</span><span class="sxs-lookup"><span data-stu-id="603d8-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="603d8-311">Идентификатор клиента подписки Azure, в которой расположено хранилище Key Vault</span><span class="sxs-lookup"><span data-stu-id="603d8-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="603d8-312">Код клиента, в котором расположены учетная запись хранения, приложения и хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="603d8-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="603d8-313">Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="603d8-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="603d8-314">Укажите DNS-имя вашего Key Vault</span><span class="sxs-lookup"><span data-stu-id="603d8-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="603d8-315">DNS-имя хранилища ключа, например `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="603d8-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="603d8-316">(Это значение соответствует DNS-имени, которое используется в хранилище сущностей.)</span><span class="sxs-lookup"><span data-stu-id="603d8-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="603d8-317">Введите секрет, содержащий имя учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="603d8-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="603d8-318">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="603d8-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="603d8-319">Имя секрета для кода приложения, которое будет использоваться для доступа к Data Lake</span><span class="sxs-lookup"><span data-stu-id="603d8-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="603d8-320">**app-id**</span><span class="sxs-lookup"><span data-stu-id="603d8-320">**app-id**</span></span> |
    | <span data-ttu-id="603d8-321">Имя секрета для использования с кодом приложения</span><span class="sxs-lookup"><span data-stu-id="603d8-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="603d8-322">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="603d8-322">**app-secret**</span></span> |

5. <span data-ttu-id="603d8-323">Примите условия и выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="603d8-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="603d8-324">Надстройка будет установлена в течение нескольких минут.</span><span class="sxs-lookup"><span data-stu-id="603d8-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="603d8-325">Настройка AI Builder</span><span class="sxs-lookup"><span data-stu-id="603d8-325">Configure AI Builder</span></span>

1. <span data-ttu-id="603d8-326">Выполните вход в LCS и откройте страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="603d8-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="603d8-327">Перейдите в раздел **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="603d8-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="603d8-328">Вы должны увидеть надстройки, уже установленные в этой среде.</span><span class="sxs-lookup"><span data-stu-id="603d8-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="603d8-329">Если надстройка **Экспорт в Data Lake** среди них отсутствует, настройте эту надстройку.</span><span class="sxs-lookup"><span data-stu-id="603d8-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="603d8-330">Выберите надстройку **Получить анализ**.</span><span class="sxs-lookup"><span data-stu-id="603d8-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="603d8-331">На странице сведений о надстройке **Получить анализ** введите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="603d8-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="603d8-332">значение</span><span class="sxs-lookup"><span data-stu-id="603d8-332">Value</span></span>                                                    | <span data-ttu-id="603d8-333">описание</span><span class="sxs-lookup"><span data-stu-id="603d8-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="603d8-334">URL-адрес организации CDS</span><span class="sxs-lookup"><span data-stu-id="603d8-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="603d8-335">URL-адрес организации Dataverse, скопированный ранее.</span><span class="sxs-lookup"><span data-stu-id="603d8-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="603d8-336">Код организации CDS</span><span class="sxs-lookup"><span data-stu-id="603d8-336">CDS Org ID</span></span>                                               | <span data-ttu-id="603d8-337">Код организации Dataverse, скопированный ранее.</span><span class="sxs-lookup"><span data-stu-id="603d8-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="603d8-338">Включите **Является ли данная среда средой по умолчанию для клиента**.</span><span class="sxs-lookup"><span data-stu-id="603d8-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="603d8-339">Настройка хранилища сущностей</span><span class="sxs-lookup"><span data-stu-id="603d8-339">Configure the entity store</span></span>

<span data-ttu-id="603d8-340">Выполните следующие действия, чтобы настроить хранилище сущностей в среде Finance.</span><span class="sxs-lookup"><span data-stu-id="603d8-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="603d8-341">Перейдите в раздел **Администрирование системы \> Настройка \> Параметры системы \> Подключения данных**.</span><span class="sxs-lookup"><span data-stu-id="603d8-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="603d8-342">Настройте следующие поля хранилища ключей:</span><span class="sxs-lookup"><span data-stu-id="603d8-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="603d8-343">**Код приложения (клиента)** — введите код клиента приложения, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="603d8-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="603d8-344">**Секрет приложения** — введите секрет, сохраненный для ранее созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="603d8-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="603d8-345">**DNS-имя** — имя службы доменных имен (DNS) можно найти на странице сведения о приложении для приложения, которое было создано вами ранее.</span><span class="sxs-lookup"><span data-stu-id="603d8-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="603d8-346">**Имя секрета** — введите **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="603d8-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="603d8-347">Включите **Разрешить интеграцию с Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="603d8-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="603d8-348">Выберите **Проверка Azure Key Vault** и убедитесь в отсутствии ошибок.</span><span class="sxs-lookup"><span data-stu-id="603d8-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="603d8-349">Выберите **Проверка хранилища Azure** и убедитесь в отсутствии ошибок.</span><span class="sxs-lookup"><span data-stu-id="603d8-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="603d8-350">Отзывы и поддержка</span><span class="sxs-lookup"><span data-stu-id="603d8-350">Feedback and support</span></span>

<span data-ttu-id="603d8-351">Отправьте сообщение электронной почты по адресу [Аналитика платежей клиентов (предварительная версия)](mailto:fiap@microsoft.com), если вы хотите предоставить отзыв или вам нужна поддержка.</span><span class="sxs-lookup"><span data-stu-id="603d8-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="603d8-352">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="603d8-352">Privacy notice</span></span>

<span data-ttu-id="603d8-353">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="603d8-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
