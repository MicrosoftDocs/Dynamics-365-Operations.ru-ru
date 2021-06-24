---
title: Конфигурация для общедоступной предварительной версии Finance Insights — версия 10.0.20 и более поздняя
description: В этой теме объясняется, как настроить систему для использования возможностей, доступных в общедоступной предварительной версии Finance Insights в версии 10.0.20 или более поздней.
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222620"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="256a5-103">Конфигурация для общедоступной предварительной версии Finance Insights — версия 10.0.20 и более поздняя</span><span class="sxs-lookup"><span data-stu-id="256a5-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="256a5-104">Финансовый анализ сочетает в себе функции из Microsoft Dynamics 365 Finance с Dataverse, Azure и AI Builder, чтобы предоставить мощные средства прогнозирования для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="256a5-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="256a5-105">В этой теме объясняется, как настроить Dynamics 365 Finance версии 10.0.20, чтобы система могла использовать возможности, доступные в общедоступной предварительной версии Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="256a5-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="256a5-106">Шаги конфигурации, описанные в данной теме, применимы только к Finance версии 10.0.20 и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="256a5-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="256a5-107">Чтобы настроить Finance Insights в версии 10.0.19 и более ранних, см. раздел [Настройка для Finance Insights — версии до 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="256a5-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="256a5-108">Развертывание Finance</span><span class="sxs-lookup"><span data-stu-id="256a5-108">Deploy Finance</span></span>

<span data-ttu-id="256a5-109">Выполните следующие шаги, чтобы развернуть среды.</span><span class="sxs-lookup"><span data-stu-id="256a5-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="256a5-110">В Microsoft Dynamics Lifecycle Services (LCS) создайте или обновите среду Finance.</span><span class="sxs-lookup"><span data-stu-id="256a5-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="256a5-111">Среде требуется версия 10.0.20 или более поздней версии приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="256a5-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="256a5-112">Среда должна быть средой с высокой доступностью (HA) в песочнице.</span><span class="sxs-lookup"><span data-stu-id="256a5-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="256a5-113">(Этот тип среды также известен как среда уровня 2.) Дополнительные сведения см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="256a5-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="256a5-114">При настройке Finance Insights в среде песочницы, возможно, потребуется скопировать в эту среду производственные данные, чтобы прогнозы работали.</span><span class="sxs-lookup"><span data-stu-id="256a5-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="256a5-115">Модель прогнозирования использует несколько лет данных для создания прогнозов.</span><span class="sxs-lookup"><span data-stu-id="256a5-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="256a5-116">Демонстрационные данные Contoso не содержат достаточно исторических данных для адекватной тренировки прогнозной модели.</span><span class="sxs-lookup"><span data-stu-id="256a5-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="256a5-117">Настроить Dataverse</span><span class="sxs-lookup"><span data-stu-id="256a5-117">Configure Dataverse</span></span>

<span data-ttu-id="256a5-118">Выполните следующие шаги, чтобы настроить Dataverse для Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="256a5-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="256a5-119">В LCS откройте страницу среды и убедитесь, что раздел **Интеграция Power Platform** уже настроен.</span><span class="sxs-lookup"><span data-stu-id="256a5-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="256a5-120">Если уже настроен, должно быть указано имя среды Dataverse, связанной со средой Finance.</span><span class="sxs-lookup"><span data-stu-id="256a5-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="256a5-121">Если не настроен, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="256a5-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="256a5-122">В разделе **Интеграция Power Platform** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="256a5-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="256a5-123">Настройка среды может занять около часа.</span><span class="sxs-lookup"><span data-stu-id="256a5-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="256a5-124">Если среда Dataverse успешно настроена, должно быть указано имя среды Dataverse, связанной со средой Finance.</span><span class="sxs-lookup"><span data-stu-id="256a5-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="256a5-125">После завершения настройки среды **не** выбирайте ссылку **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="256a5-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="256a5-126">Эта кнопка не требуется для Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="256a5-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="256a5-127">Если вы ее выберите, вы не сможете настроить необходимые надстройки среды в LCS.</span><span class="sxs-lookup"><span data-stu-id="256a5-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="256a5-128">Настройка Azure</span><span class="sxs-lookup"><span data-stu-id="256a5-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="256a5-129">Использование Azure Cloud Shell для настройки ресурсов Data Lake финансового анализа</span><span class="sxs-lookup"><span data-stu-id="256a5-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="256a5-130">Использование сценария Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="256a5-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="256a5-131">Был предоставлен сценарий Windows PowerShell, который позволяет легко настроить ресурсы Azure, описанные в разделе [Настройка экспорта в Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="256a5-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="256a5-132">Если вы предпочитаете выполнить настройку вручную, пропустите эту процедуру и выполните процедуру, описанную в разделе [Настройка вручную](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="256a5-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="256a5-133">Для выполнения сценария Windows PowerShell используется следующая процедура.</span><span class="sxs-lookup"><span data-stu-id="256a5-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="256a5-134">Настройка может не работать, если используется вариант **Попробовать** в Azure CLI или если на компьютере выполняется сценарий.</span><span class="sxs-lookup"><span data-stu-id="256a5-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="256a5-135">Выполните следующие действия, используя Windows PowerShell, чтобы настроить Azure.</span><span class="sxs-lookup"><span data-stu-id="256a5-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="256a5-136">Необходимо иметь права на создание группы ресурсов Azure, ресурсов Azure и приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="256a5-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="256a5-137">Сведения о необходимых разрешениях см. в разделе [Проверка разрешений Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="256a5-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="256a5-138">На [портале Azure](https://portal.azure.com) перейдите к целевой подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="256a5-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="256a5-139">Выберите **Cloud Shell** справа от поля **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="256a5-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="256a5-140">Выберите **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="256a5-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="256a5-141">Создайте хранилище, если будет предложено его создать.</span><span class="sxs-lookup"><span data-stu-id="256a5-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="256a5-142">На вкладке **Azure CLI** выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="256a5-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="256a5-143">Откройте новый файл в блокноте и вставьте в его сценарий Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="256a5-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="256a5-144">Сохраните файл под именем **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="256a5-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="256a5-145">Отправьте сценарий Windows PowerShell в сеанс, используя команду меню для отправки в Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="256a5-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="256a5-146">Выполните сценарий **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="256a5-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="256a5-147">Следуйте инструкциям для выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="256a5-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="256a5-148">Используйте сведения из выходных данных сценария для установки надстройки Экспорт в Data Lake в LCS.</span><span class="sxs-lookup"><span data-stu-id="256a5-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="256a5-149">Настройка вручную</span><span class="sxs-lookup"><span data-stu-id="256a5-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="256a5-150">Добавление приложений в клиент Azure AD</span><span class="sxs-lookup"><span data-stu-id="256a5-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="256a5-151">На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="256a5-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="256a5-152">Выберите **Управление \> Корпоративные приложения**.</span><span class="sxs-lookup"><span data-stu-id="256a5-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="256a5-153">Выполните поиск следующих приложений по коду приложения.</span><span class="sxs-lookup"><span data-stu-id="256a5-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="256a5-154">Заявление</span><span class="sxs-lookup"><span data-stu-id="256a5-154">Application</span></span>                              | <span data-ttu-id="256a5-155">Код приложения</span><span class="sxs-lookup"><span data-stu-id="256a5-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="256a5-156">Микрослужбы Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="256a5-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="256a5-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="256a5-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="256a5-158">Микрослужбы Microsoft Dynamics ERP CDS</span><span class="sxs-lookup"><span data-stu-id="256a5-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="256a5-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="256a5-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="256a5-160">Служба авторизации AI Builder</span><span class="sxs-lookup"><span data-stu-id="256a5-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="256a5-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="256a5-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="256a5-162">Если не удается найти какое-либо из вышеперечисленных приложений, попробуйте выполнить следующие действия</span><span class="sxs-lookup"><span data-stu-id="256a5-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="256a5-163">На локальном компьютере в меню **Пуск** найдите **powershell**.</span><span class="sxs-lookup"><span data-stu-id="256a5-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="256a5-164">Выберите и удерживайте (или щелкните правой кнопкой мыши) **Windows PowerShell**, затем выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="256a5-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="256a5-165">Выполните следующую команду для установки модуля **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="256a5-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="256a5-166">Если для продолжения требуется поставщик NuGet, выберите **Y**, чтобы установить его.</span><span class="sxs-lookup"><span data-stu-id="256a5-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="256a5-167">В случае получения сообщения "Ненадежный репозиторий" выберите **Y** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="256a5-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="256a5-168">Для каждого приложения, которое необходимо добавить, выполните следующие команды, чтобы добавить приложение в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="256a5-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="256a5-169">При появлении запроса войдите в систему как администратор Azure AD.</span><span class="sxs-lookup"><span data-stu-id="256a5-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="256a5-170">Создание ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="256a5-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="256a5-171">Убедитесь, что следующие ресурсы созданы в том же экземпляре Azure AD, в котором находится среда Dataverse.</span><span class="sxs-lookup"><span data-stu-id="256a5-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="256a5-172">Нельзя использовать ресурсы из других экземпляров Azure AD.</span><span class="sxs-lookup"><span data-stu-id="256a5-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="256a5-173">Создайте учетную запись хранения:</span><span class="sxs-lookup"><span data-stu-id="256a5-173">Create a storage account:</span></span>

    1. <span data-ttu-id="256a5-174">На [портале Azure](https://portal.azure.com) создайте учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="256a5-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="256a5-175">В диалоговом окне **Создание учетной записи хранения** установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="256a5-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="256a5-176">**Местонахождение** — выберите центр обработки данных, в котором находится среда.</span><span class="sxs-lookup"><span data-stu-id="256a5-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="256a5-177">**Производительность** — рекомендуется выбирать **Стандартная**.</span><span class="sxs-lookup"><span data-stu-id="256a5-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="256a5-178">**Вид учетной записи** — необходимо выбрать **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="256a5-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="256a5-179">В диалоговом окне **Дополнительные параметры** для параметра **Data Lake storage Gen2** выберите **Включить** в функции **Иерархические пространства имен**.</span><span class="sxs-lookup"><span data-stu-id="256a5-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="256a5-180">Если эта функция не включена, вы не сможете потреблять данные, которые приложения Finance and Operations записывают с помощью таких служб, как потоки данных Power BI.</span><span class="sxs-lookup"><span data-stu-id="256a5-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="256a5-181">Выберите **Просмотр и создание**.</span><span class="sxs-lookup"><span data-stu-id="256a5-181">Select **Review and create**.</span></span> <span data-ttu-id="256a5-182">После завершения развертывания новый ресурс будет показан на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="256a5-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="256a5-183">Перейдите к созданной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="256a5-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="256a5-184">В левом меню выберите **Ключи доступа**.</span><span class="sxs-lookup"><span data-stu-id="256a5-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="256a5-185">Скопируйте и сохраните имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="256a5-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="256a5-186">Это значение будет необходимо ввести позднее при настройке секретов хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="256a5-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="256a5-187">Создайте хранилище ключей:</span><span class="sxs-lookup"><span data-stu-id="256a5-187">Create a key vault:</span></span>

    1. <span data-ttu-id="256a5-188">На [портале Azure](https://portal.azure.com) создайте хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="256a5-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="256a5-189">В диалоговом окне **Создать хранилище ключей** в поле **Расположение** выберите центр обработки данных, в котором находится среда.</span><span class="sxs-lookup"><span data-stu-id="256a5-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="256a5-190">После создания хранилища ключей перейдите к пункту **Обзор Key Vault** и скопируйте и сохраните DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="256a5-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="256a5-191">Это значение будет необходимо ввести позднее при настройке надстройки Data Lake.</span><span class="sxs-lookup"><span data-stu-id="256a5-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="256a5-192">Создание и регистрация приложения Azure AD:</span><span class="sxs-lookup"><span data-stu-id="256a5-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="256a5-193">На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**, затем выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="256a5-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="256a5-194">Выберите **Регистрация нового приложения** и задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="256a5-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="256a5-195">**Имя** — введите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="256a5-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="256a5-196">**Тип приложения** — выберите **Веб-API**.</span><span class="sxs-lookup"><span data-stu-id="256a5-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="256a5-197">**Настройка URI перенаправления** — введите URL-адрес для экземпляра Dynamics 365, например, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="256a5-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="256a5-198">Перейдите к только что созданному приложению и скопируйте его значение **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="256a5-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="256a5-199">Это значение будет необходимо ввести позднее при настройке секретов хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="256a5-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="256a5-200">Перейдите на страницу **Разрешения API** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="256a5-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="256a5-201">Выберите **Добавить разрешение**.</span><span class="sxs-lookup"><span data-stu-id="256a5-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="256a5-202">Выберите **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="256a5-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="256a5-203">После выбора делегированных разрешений выберите **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="256a5-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="256a5-204">Выберите **Добавить разрешения**.</span><span class="sxs-lookup"><span data-stu-id="256a5-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="256a5-205">В меню приложения выберите **Сертификаты \& секреты**, затем выполните следующие действия, чтобы создать секреты для Key Vault:</span><span class="sxs-lookup"><span data-stu-id="256a5-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="256a5-206">Выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="256a5-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="256a5-207">В поле **Описание ключа** введите имя.</span><span class="sxs-lookup"><span data-stu-id="256a5-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="256a5-208">Выберите длительность, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="256a5-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="256a5-209">Секрет создается в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="256a5-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="256a5-210">Скопируйте и сохраните значение секрета клиента.</span><span class="sxs-lookup"><span data-stu-id="256a5-210">Copy and save the client secret value.</span></span> <span data-ttu-id="256a5-211">Это значение будет необходимо ввести позднее при настройке секретов хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="256a5-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="256a5-212">Создайте секреты Key Vault:</span><span class="sxs-lookup"><span data-stu-id="256a5-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="256a5-213">Перейдите к созданному ранее хранилищу ключей и выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="256a5-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="256a5-214">Для каждого имени секрета в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="256a5-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="256a5-215">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="256a5-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="256a5-216">В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="256a5-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="256a5-217">Создайте имя и значение секрета из таблицы.</span><span class="sxs-lookup"><span data-stu-id="256a5-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="256a5-218">Выберите **Включено**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="256a5-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="256a5-219">Секрет создается и добавляется в Key Vault.</span><span class="sxs-lookup"><span data-stu-id="256a5-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="256a5-220">Имя секрета</span><span class="sxs-lookup"><span data-stu-id="256a5-220">Secret name</span></span>                       | <span data-ttu-id="256a5-221">Значение секрета</span><span class="sxs-lookup"><span data-stu-id="256a5-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="256a5-222">app-id</span><span class="sxs-lookup"><span data-stu-id="256a5-222">app-id</span></span>                            | <span data-ttu-id="256a5-223">Код приложения, созданного ранее.</span><span class="sxs-lookup"><span data-stu-id="256a5-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="256a5-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="256a5-224">app-secret</span></span>                        | <span data-ttu-id="256a5-225">Секрет клиента, который был сохранен ранее.</span><span class="sxs-lookup"><span data-stu-id="256a5-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="256a5-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="256a5-226">storage-account-name</span></span>              | <span data-ttu-id="256a5-227">Имя созданной ранее учетной записи хранения, например **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="256a5-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="256a5-228">Авторизуйте приложение для доступа к хранилищу ключей:</span><span class="sxs-lookup"><span data-stu-id="256a5-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="256a5-229">На [портале Azure](https://portal.azure.com) откройте созданное ранее хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="256a5-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="256a5-230">Выберите политики доступа.</span><span class="sxs-lookup"><span data-stu-id="256a5-230">Select the access policies.</span></span>
    3. <span data-ttu-id="256a5-231">Для каждого приложения в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="256a5-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="256a5-232">Выберите **Добавить политику доступа**, чтобы создать политику доступа.</span><span class="sxs-lookup"><span data-stu-id="256a5-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="256a5-233">В поле **Разрешения секрета** выберите разрешения из таблицы.</span><span class="sxs-lookup"><span data-stu-id="256a5-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="256a5-234">В поле **Выберите субъект** найдите отображаемое имя приложения из таблицы.</span><span class="sxs-lookup"><span data-stu-id="256a5-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="256a5-235">Выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="256a5-235">Select **Select**.</span></span>
        5. <span data-ttu-id="256a5-236">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="256a5-236">Select **Add**.</span></span>
        6. <span data-ttu-id="256a5-237">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="256a5-237">Select **Save**.</span></span>

        | <span data-ttu-id="256a5-238">Заявление</span><span class="sxs-lookup"><span data-stu-id="256a5-238">Application</span></span>                                              | <span data-ttu-id="256a5-239">Права доступа</span><span class="sxs-lookup"><span data-stu-id="256a5-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="256a5-240">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="256a5-240">The display name of the new application that you created</span></span> | <span data-ttu-id="256a5-241">Получить, Список</span><span class="sxs-lookup"><span data-stu-id="256a5-241">Get, List</span></span>   |
        | <span data-ttu-id="256a5-242">**Микрослужбы Microsoft Dynamics ERP**</span><span class="sxs-lookup"><span data-stu-id="256a5-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="256a5-243">Получить, Список</span><span class="sxs-lookup"><span data-stu-id="256a5-243">Get, List</span></span>   |

6. <span data-ttu-id="256a5-244">Назначьте роли для доступа к учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="256a5-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="256a5-245">На [портале Azure](https://portal.azure.com) откройте созданную ранее учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="256a5-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="256a5-246">Выберите **Управление доступом (IAM)**, затем выберите **Назначения ролей**.</span><span class="sxs-lookup"><span data-stu-id="256a5-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="256a5-247">Выберите **Добавить, Добавить назначение ролей**.</span><span class="sxs-lookup"><span data-stu-id="256a5-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="256a5-248">Для каждого приложения в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="256a5-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="256a5-249">Выбор роли из таблицы.</span><span class="sxs-lookup"><span data-stu-id="256a5-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="256a5-250">В поле **Назначить доступ** оставьте значение **Пользователь, группа или субъект-служба Azure AD**</span><span class="sxs-lookup"><span data-stu-id="256a5-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="256a5-251">В поле **Выбрать** введите приложение из таблицы.</span><span class="sxs-lookup"><span data-stu-id="256a5-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="256a5-252">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="256a5-252">Select **Save**.</span></span>

        | <span data-ttu-id="256a5-253">Заявление</span><span class="sxs-lookup"><span data-stu-id="256a5-253">Application</span></span>                                              | <span data-ttu-id="256a5-254">Роль</span><span class="sxs-lookup"><span data-stu-id="256a5-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="256a5-255">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="256a5-255">The display name of the new application that you created</span></span> | <span data-ttu-id="256a5-256">Ответственный</span><span class="sxs-lookup"><span data-stu-id="256a5-256">Owner</span></span>                       |
        | <span data-ttu-id="256a5-257">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="256a5-257">The display name of the new application that you created</span></span> | <span data-ttu-id="256a5-258">Участник</span><span class="sxs-lookup"><span data-stu-id="256a5-258">Contributor</span></span>                 |
        | <span data-ttu-id="256a5-259">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="256a5-259">The display name of the new application that you created</span></span> | <span data-ttu-id="256a5-260">Участник учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="256a5-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="256a5-261">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="256a5-261">The display name of the new application that you created</span></span> | <span data-ttu-id="256a5-262">Владелец данных BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="256a5-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="256a5-263">**Служба авторизации AI Builder**</span><span class="sxs-lookup"><span data-stu-id="256a5-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="256a5-264">Модуль чтения данных BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="256a5-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="256a5-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="256a5-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="256a5-266">Настройка надстройки экспорта в Data Lake</span><span class="sxs-lookup"><span data-stu-id="256a5-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="256a5-267">Выполните следующие действия, чтобы использовать LCS для добавления надстройки экспорта в Data Lake в среду.</span><span class="sxs-lookup"><span data-stu-id="256a5-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="256a5-268">Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="256a5-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="256a5-269">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="256a5-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="256a5-270">Выберите надстройку **Экспорт в Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="256a5-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="256a5-271">Введите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="256a5-271">Enter the following values.</span></span>

    | <span data-ttu-id="256a5-272">значение</span><span class="sxs-lookup"><span data-stu-id="256a5-272">Value</span></span>                                                              | <span data-ttu-id="256a5-273">описание</span><span class="sxs-lookup"><span data-stu-id="256a5-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="256a5-274">Идентификатор клиента подписки Azure, в которой расположено хранилище Key Vault</span><span class="sxs-lookup"><span data-stu-id="256a5-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="256a5-275">Код клиента, в котором расположены учетная запись хранения, приложения и хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="256a5-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="256a5-276">Чтобы получить это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="256a5-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="256a5-277">Укажите DNS-имя вашего Key Vault</span><span class="sxs-lookup"><span data-stu-id="256a5-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="256a5-278">DNS-имя хранилища ключа, например `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="256a5-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="256a5-279">Введите секрет, содержащий имя учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="256a5-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="256a5-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="256a5-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="256a5-281">Имя секрета для кода приложения, которое будет использоваться для доступа к Data Lake</span><span class="sxs-lookup"><span data-stu-id="256a5-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="256a5-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="256a5-282">**app-id**</span></span> |
    | <span data-ttu-id="256a5-283">Имя секрета для секрета клиента приложения</span><span class="sxs-lookup"><span data-stu-id="256a5-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="256a5-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="256a5-284">**app-secret**</span></span> |

5. <span data-ttu-id="256a5-285">Примите условия, затем выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="256a5-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="256a5-286">Надстройка будет установлена в течение нескольких минут.</span><span class="sxs-lookup"><span data-stu-id="256a5-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="256a5-287">Настройка надстройки Finance Insights</span><span class="sxs-lookup"><span data-stu-id="256a5-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="256a5-288">Если ранее была установлена надстройка "Получить анализ", удалите ее перед выполнением следующей процедуры.</span><span class="sxs-lookup"><span data-stu-id="256a5-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="256a5-289">Выполните следующие шаги, чтобы установить надстройку Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="256a5-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="256a5-290">Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="256a5-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="256a5-291">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="256a5-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="256a5-292">Выберите надстройку **Finance Insights**.</span><span class="sxs-lookup"><span data-stu-id="256a5-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="256a5-293">Примите условия, затем выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="256a5-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="256a5-294">Отзывы и поддержка</span><span class="sxs-lookup"><span data-stu-id="256a5-294">Feedback and support</span></span>

<span data-ttu-id="256a5-295">Если вы хотите предоставить отзыв или вам нужна поддержка, отправьте сообщение электронной почты по адресу [Finance Insights (предварительная версия)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="256a5-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
