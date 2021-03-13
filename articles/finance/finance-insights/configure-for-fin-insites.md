---
title: Конфигурация для финансового анализа (предварительная версия)
description: В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в финансовом анализе.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: bb887bbff5eb5b92f588d3fa966ea204633575db
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115640"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="ae6a4-103">Конфигурация для финансового анализа (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="ae6a4-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ae6a4-104">Финансовый анализ сочетает в себе функции из Microsoft Dynamics 365 Finance с Microsoft Dataverse, Azure и AI Builder, чтобы предоставить мощные средства прогнозирования для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="ae6a4-105">В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="ae6a4-106">Разверните Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ae6a4-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="ae6a4-107">Разверните среды, выполнив следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="ae6a4-108">В Microsoft Dynamics Lifecycle Services (LCS) создайте или обновите среду Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="ae6a4-109">Среде требуется версия приложения 10.0.11/Platform Update 35 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="ae6a4-110">Среда должна быть средой с высокой доступностью (HA) в песочнице.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="ae6a4-111">(Этот тип среды также известен как среда уровня 2.) Дополнительные сведения см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="ae6a4-112">Если используются демонстрационные данные компании Contoso, для использования функций прогнозирования платежей клиентов, прогнозов движения денежных средств и прогнозов бюджета потребуется дополнительный образец данных.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="ae6a4-113">Настроить Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae6a4-113">Configure Dataverse</span></span>

<span data-ttu-id="ae6a4-114">Можно выполнить следующие действия по настройке вручную или можно ускорить процесс настройки, используя предлагаемый сценарий Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="ae6a4-115">После завершения выполнения сценария PowerShell вы получите значения, которые будут использоваться для настройки финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="ae6a4-116">Откройте PowerShell на своем компьютере, чтобы запустить сценарий.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="ae6a4-117">Возможно, вам понадобится PowerShell версии 5.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="ae6a4-118">Функция интерфейса командной строки Microsoft Azure "Попробовать" может не работать.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="ae6a4-119">Шаги конфигурации вручную</span><span class="sxs-lookup"><span data-stu-id="ae6a4-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="ae6a4-120">Откройте [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/) и выполните следующие действия, чтобы создать новую среду Dataverse в одном и том же клиенте Active Directory:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="ae6a4-121">Откройте страницу **Среды**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="ae6a4-122">[![Страница сред](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="ae6a4-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="ae6a4-123">Выберите **Создать среду**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="ae6a4-124">В поле **Тип** выберите **Песочница**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="ae6a4-125">Установите параметр **Создать базу данных** на значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="ae6a4-126">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-126">Select **Next**.</span></span>
    6. <span data-ttu-id="ae6a4-127">Выберите язык и валюту для организации.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="ae6a4-128">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="ae6a4-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-129">Select **Save**.</span></span>
    9. <span data-ttu-id="ae6a4-130">Обновите страницу **Среды**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="ae6a4-131">Дождитесь, когда значение поля **Состояние** будет обновлено на **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="ae6a4-132">Запишите код организации Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="ae6a4-133">Выберите среду, затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="ae6a4-134">Выберите **Ресурсы \> Все устаревшие параметры**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="ae6a4-135">На верхней панели навигации выберите **Параметры**, а затем выберите **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="ae6a4-136">Выберите **Ресурсы разработчика**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="ae6a4-137">Задайте в поле **Код ссылки экземпляра** значение идентификатора организации Dataverse, который вы записали ранее.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-137">Set the **Instance Reference Information ID** field to the Dataverse organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="ae6a4-138">В адресной строке браузера запишите URL-адрес для организации Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="ae6a4-139">Например, может быть указан URL-адрес `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="ae6a4-140">Если планируется использовать функцию прогнозов движения денежных средств или прогнозов бюджета, выполните следующие действия, чтобы обновить ограничение для аннотации организации как минимум до 50 мегабайт (МБ):</span><span class="sxs-lookup"><span data-stu-id="ae6a4-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="ae6a4-141">Откройте [портал Power Apps](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="ae6a4-142">Выберите только что созданную среду, а затем выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="ae6a4-143">Выберите **Параметры \> Конфигурация электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="ae6a4-144">Измените значение поля **Максимальный размер файла** на **51200**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="ae6a4-145">(Это значение задается в килобайтах \[КБ\].)</span><span class="sxs-lookup"><span data-stu-id="ae6a4-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="ae6a4-146">Выберите **ОК**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="ae6a4-147">Сценарий конфигурации Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae6a4-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="ae6a4-148">Задание настройки Azure</span><span class="sxs-lookup"><span data-stu-id="ae6a4-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="ae6a4-149">Введите код каталога Dataverse и код объекта пользователя Azure AD</span><span class="sxs-lookup"><span data-stu-id="ae6a4-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="ae6a4-150">Введите код каталога Dataverse:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="ae6a4-151">Откройте [портал Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="ae6a4-152">Выполните вход, используя код пользователя, который использовался при создании среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="ae6a4-153">Перейдите на страницу **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="ae6a4-154">Скопируйте значение **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="ae6a4-155">Введите код объекта Azure Active Directory (Azure AD) пользователя:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="ae6a4-156">На [портале Azure](https://portal.azure.com) перейдите в раздел **Пользователи** и выполните поиск пользователя по адресу электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="ae6a4-157">Выберите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-157">Select the user's name.</span></span>
    3. <span data-ttu-id="ae6a4-158">Скопируйте значение **Код объекта**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="ae6a4-159">Использование Azure Cloud Shell для настройки ресурсов Data Lake финансового анализа</span><span class="sxs-lookup"><span data-stu-id="ae6a4-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="ae6a4-160">Использование сценария Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae6a4-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="ae6a4-161">Был предоставлен сценарий Windows PowerShell, который позволяет легко настроить ресурсы Azure, описанные в разделе [Настройка экспорта в Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="ae6a4-162">Если вы предпочитаете выполнить настройку вручную, пропустите эту процедуру и продолжите процедуру, описанную в разделе [Настройка вручную](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="ae6a4-163">Выполните приведенные ниже шаги, чтобы выполнить сценарий PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="ae6a4-164">Параметр Azure CLI "Попробовать" или запуск сценария на компьютере может не работать.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="ae6a4-165">Выполните следующие действия, чтобы настроить Azure с помощью сценария Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="ae6a4-166">Необходимо иметь права на создание группы ресурсов Azure, ресурсов Azure и приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="ae6a4-167">Сведения о необходимых разрешениях см. в разделе [Проверка разрешений Azure AD](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="ae6a4-168">На [портале Azure](https://portal.azure.com) перейдите к целевой подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="ae6a4-169">Выберите кнопку **Cloud Shell** справа от поля **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="ae6a4-170">Выберите **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="ae6a4-171">В случае появлении соответствующего запроса создайте хранилище.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="ae6a4-172">Затем отправьте сценарий Windows PowerShell в сеанс.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="ae6a4-173">Выполните сценарий.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-173">Run the script.</span></span>
5. <span data-ttu-id="ae6a4-174">Следуйте инструкциям для выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="ae6a4-175">Используйте сведения из выходных данных сценария для установки надстройки **Экспорт в Data Lake** в LCS.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="ae6a4-176">Используйте сведения из выходных данных сценария для включения хранилища сущностей на странице **Подключения данных** в Finance (**Администрирование системы \> Параметры системы \> Подключения данных**).</span><span class="sxs-lookup"><span data-stu-id="ae6a4-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="ae6a4-177">Настройка вручную</span><span class="sxs-lookup"><span data-stu-id="ae6a4-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="ae6a4-178">Добавление приложений в клиент Azure AD</span><span class="sxs-lookup"><span data-stu-id="ae6a4-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="ae6a4-179">На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="ae6a4-180">Выберите **Управление \> Корпоративные приложения**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="ae6a4-181">Выполните поиск следующих приложений по коду приложения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="ae6a4-182">Заявление</span><span class="sxs-lookup"><span data-stu-id="ae6a4-182">Application</span></span>                              | <span data-ttu-id="ae6a4-183">Код приложения</span><span class="sxs-lookup"><span data-stu-id="ae6a4-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="ae6a4-184">Микрослужбы Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="ae6a4-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="ae6a4-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="ae6a4-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="ae6a4-186">Микрослужбы Microsoft Dynamics ERP CDS</span><span class="sxs-lookup"><span data-stu-id="ae6a4-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="ae6a4-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="ae6a4-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="ae6a4-188">Служба авторизации AI Builder</span><span class="sxs-lookup"><span data-stu-id="ae6a4-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="ae6a4-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="ae6a4-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="ae6a4-190">Если не удается найти какое-либо из вышеперечисленных приложений, попробуйте выполнить следующие действия</span><span class="sxs-lookup"><span data-stu-id="ae6a4-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="ae6a4-191">На локальном компьютере выберите меню **Пуск** и выполните поиск **powershell**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="ae6a4-192">Выберите и удерживайте (или щелкните правой кнопкой мыши) **Windows PowerShell**, затем выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="ae6a4-193">Выполните следующую команду для установки модуля **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="ae6a4-194">Если для продолжения требуется поставщик NuGet, выберите **Y**, чтобы установить его.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="ae6a4-195">В случае появления сообщения "Ненадежный репозиторий" выберите **Y** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="ae6a4-196">Для каждого приложения, которое необходимо добавить, выполните следующие команды, чтобы добавить приложение в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="ae6a4-197">При появлении запроса войдите в систему как администратор Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="ae6a4-198">Создание ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="ae6a4-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="ae6a4-199">Убедитесь, что следующие ресурсы созданы в том же экземпляре Azure AD, что и среда Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="ae6a4-200">Нельзя использовать ресурсы из других экземпляров Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="ae6a4-201">Создайте новую учетную запись хранения:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="ae6a4-202">На [портале Azure](https://portal.azure.com) создайте учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="ae6a4-203">В диалоговом окне **Создание учетной записи хранения** установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="ae6a4-204">**Местонахождение** — выберите центр обработки данных, в котором находится среда.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="ae6a4-205">**Производительность** — рекомендуется выбирать **Стандартная**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="ae6a4-206">**Вид учетной записи** — необходимо выбрать **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="ae6a4-207">В диалоговом окне **Дополнительные параметры** для параметра **Data Lake storage Gen2** выберите **Включить** в функции **Иерархические пространства имен**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="ae6a4-208">Если эта функция отключена, вы не сможете потреблять данные, которые приложения Finance and Operations записывают с помощью таких служб, как потоки данных Power BI.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="ae6a4-209">Выберите **Просмотр и создание**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-209">Select **Review and create**.</span></span> <span data-ttu-id="ae6a4-210">После завершения развертывания новый ресурс будет показан на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="ae6a4-211">Перейдите к созданной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="ae6a4-212">В левом меню выберите **Ключи доступа**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="ae6a4-213">Скопируйте и сохраните строку подключения для **Key1** или **Key2**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="ae6a4-214">Скопируйте и сохраните имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="ae6a4-215">Создайте новое хранилище ключей:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="ae6a4-216">На [портале Azure](https://portal.azure.com) создайте хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="ae6a4-217">В диалоговом окне **Создать хранилище ключей** в поле **Расположение** выберите центр обработки данных, в котором находится среда.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="ae6a4-218">После создания хранилища ключей выберите его в списке, а затем выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="ae6a4-219">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="ae6a4-220">В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="ae6a4-221">Введите имя для секрета.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-221">Enter a name for the secret.</span></span> <span data-ttu-id="ae6a4-222">Запишите имя, поскольку его потребуется указать позже.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="ae6a4-223">В поле **Значение** введите строку подключения, полученную из учетной записи хранения в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="ae6a4-224">Выберите **Включено**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="ae6a4-225">Секрет создается и добавляется в Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="ae6a4-226">Перейдите в раздел **Обзор Key Vault** и запишите DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="ae6a4-227">Создание и регистрация приложения Azure AD:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="ae6a4-228">На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**, затем выберите **Регистрации приложений**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="ae6a4-229">Выберите **Регистрация нового приложения** и задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="ae6a4-230">**Имя** — введите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="ae6a4-231">**Тип приложения** — выберите **Веб-API**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="ae6a4-232">**Настройка URI перенаправления** — введите URL-адрес для экземпляра Dynamics 365, например, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="ae6a4-233">Перейдите к только что созданному приложению и скопируйте его значение **Код приложения (клиента)**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="ae6a4-234">Это значение будет необходимо ввести позднее при настройке хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="ae6a4-235">Перейдите на страницу **Разрешения API** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="ae6a4-236">Выберите **Добавить разрешение**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="ae6a4-237">Выберите **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="ae6a4-238">После выбора делегированных разрешений выберите **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="ae6a4-239">Выберите **Добавить разрешения**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="ae6a4-240">В меню приложения выберите **Сертификаты \& секреты**, затем выполните следующие действия, чтобы создать секреты для Key Vault:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="ae6a4-241">Выберите **Создать секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="ae6a4-242">В поле **Описание ключа** введите имя.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="ae6a4-243">Выберите длительность, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="ae6a4-244">Секрет создается в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="ae6a4-245">Скопируйте и сохраните значение секрета.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="ae6a4-246">Создайте секреты Key Vault:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="ae6a4-247">Перейдите к созданному ранее хранилищу ключей и выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="ae6a4-248">Для каждого имени секрета в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ae6a4-249">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="ae6a4-250">В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="ae6a4-251">Создайте имя и значение секрета из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="ae6a4-252">Выберите **Включено**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="ae6a4-253">Секрет создается и добавляется в Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="ae6a4-254">Имя секрета</span><span class="sxs-lookup"><span data-stu-id="ae6a4-254">Secret name</span></span>                       | <span data-ttu-id="ae6a4-255">Значение секрета</span><span class="sxs-lookup"><span data-stu-id="ae6a4-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="ae6a4-256">app-id</span><span class="sxs-lookup"><span data-stu-id="ae6a4-256">app-id</span></span>                            | <span data-ttu-id="ae6a4-257">Код приложения, созданного ранее</span><span class="sxs-lookup"><span data-stu-id="ae6a4-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="ae6a4-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="ae6a4-258">app-secret</span></span>                        | <span data-ttu-id="ae6a4-259">Секрет клиента, который был сохранен ранее</span><span class="sxs-lookup"><span data-stu-id="ae6a4-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="ae6a4-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="ae6a4-260">storage-account-name</span></span>              | <span data-ttu-id="ae6a4-261">Имя созданной ранее учетной записи хранения, например **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="ae6a4-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="ae6a4-262">storage-account-connection-string</span></span> | <span data-ttu-id="ae6a4-263">Строка подключения, скопированная со страницы **Ключи доступа** для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ae6a4-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="ae6a4-264">Авторизуйте приложение для доступа к хранилищу ключей:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="ae6a4-265">На [портале Azure](https://portal.azure.com) откройте созданное ранее хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="ae6a4-266">Выберите политики доступа.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-266">Select the access policies.</span></span>
    3. <span data-ttu-id="ae6a4-267">Для каждого приложения в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ae6a4-268">Выберите **Добавить политику доступа**, чтобы создать политику доступа.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="ae6a4-269">В поле **Разрешения секрета** выберите разрешения из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="ae6a4-270">В поле **Выберите субъект** найдите отображаемое имя приложения из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="ae6a4-271">Выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-271">Select **Select**.</span></span>
        5. <span data-ttu-id="ae6a4-272">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-272">Select **Add**.</span></span>
        6. <span data-ttu-id="ae6a4-273">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-273">Select **Save**.</span></span>

        | <span data-ttu-id="ae6a4-274">Заявление</span><span class="sxs-lookup"><span data-stu-id="ae6a4-274">Application</span></span>                                              | <span data-ttu-id="ae6a4-275">Права доступа</span><span class="sxs-lookup"><span data-stu-id="ae6a4-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="ae6a4-276">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="ae6a4-276">The display name of the new application that you created</span></span> | <span data-ttu-id="ae6a4-277">Получить, Список</span><span class="sxs-lookup"><span data-stu-id="ae6a4-277">Get, List</span></span>   |
        | <span data-ttu-id="ae6a4-278">**Микрослужбы Microsoft Dynamics ERP**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="ae6a4-279">Получить, Список</span><span class="sxs-lookup"><span data-stu-id="ae6a4-279">Get, List</span></span>   |

6. <span data-ttu-id="ae6a4-280">Назначьте роли для доступа к учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="ae6a4-281">На [портале Azure](https://portal.azure.com) откройте созданную ранее учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="ae6a4-282">Выберите **Управление доступом (IAM)**, затем выберите **Назначения ролей**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="ae6a4-283">Выберите **Добавить, Добавить назначение ролей**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="ae6a4-284">Для каждого приложения в следующей таблице выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ae6a4-285">Выберите роль из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="ae6a4-286">В поле **Назначить доступ** оставьте значение **Пользователь, группа или субъект-служба Azure AD**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="ae6a4-287">В поле **Выбрать** введите приложение из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="ae6a4-288">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-288">Select **Save**.</span></span>

        | <span data-ttu-id="ae6a4-289">Заявление</span><span class="sxs-lookup"><span data-stu-id="ae6a4-289">Application</span></span>                                              | <span data-ttu-id="ae6a4-290">Роль</span><span class="sxs-lookup"><span data-stu-id="ae6a4-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="ae6a4-291">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="ae6a4-291">The display name of the new application that you created</span></span> | <span data-ttu-id="ae6a4-292">Ответственный</span><span class="sxs-lookup"><span data-stu-id="ae6a4-292">Owner</span></span>                       |
        | <span data-ttu-id="ae6a4-293">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="ae6a4-293">The display name of the new application that you created</span></span> | <span data-ttu-id="ae6a4-294">Участник</span><span class="sxs-lookup"><span data-stu-id="ae6a4-294">Contributor</span></span>                 |
        | <span data-ttu-id="ae6a4-295">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="ae6a4-295">The display name of the new application that you created</span></span> | <span data-ttu-id="ae6a4-296">Участник учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="ae6a4-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="ae6a4-297">Отображаемое имя нового приложения, созданного вами</span><span class="sxs-lookup"><span data-stu-id="ae6a4-297">The display name of the new application that you created</span></span> | <span data-ttu-id="ae6a4-298">Владелец данных BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="ae6a4-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="ae6a4-299">**Служба авторизации AI Builder**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="ae6a4-300">Модуль чтения данных BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="ae6a4-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="ae6a4-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="ae6a4-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-entity-store"></a><span data-ttu-id="ae6a4-302">Настройка хранилища сущностей</span><span class="sxs-lookup"><span data-stu-id="ae6a4-302">Configure the entity store</span></span>

<span data-ttu-id="ae6a4-303">Выполните следующие действия, чтобы настроить хранилище сущностей в среде Finance.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="ae6a4-304">Перейдите в раздел **Администрирование системы \> Настройка \> Параметры системы \> Подключения данных**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="ae6a4-305">Установите для параметра **Разрешить интеграцию с Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="ae6a4-306">Настройте следующие поля Key Vault:</span><span class="sxs-lookup"><span data-stu-id="ae6a4-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="ae6a4-307">**Код приложения (клиента)** — введите код клиента приложения, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="ae6a4-308">**Секрет приложения** — введите секрет, сохраненный для ранее созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="ae6a4-309">**DNS-имя** — имя службы доменных имен (DNS) можно найти на странице сведения о приложении для приложения, которое было создано вами ранее.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="ae6a4-310">**Имя секрета** — введите **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="ae6a4-311">Настройка Data Lake</span><span class="sxs-lookup"><span data-stu-id="ae6a4-311">Configure the data lake</span></span>

<span data-ttu-id="ae6a4-312">Выполните следующие действия, чтобы использовать LCS для добавления надстройки Azure Data Lake в среду.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="ae6a4-313">Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="ae6a4-314">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="ae6a4-315">Выберите надстройку **Экспорт в Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="ae6a4-316">Введите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-316">Enter the following values.</span></span>

    | <span data-ttu-id="ae6a4-317">значение</span><span class="sxs-lookup"><span data-stu-id="ae6a4-317">Value</span></span>                                                              | <span data-ttu-id="ae6a4-318">описание</span><span class="sxs-lookup"><span data-stu-id="ae6a4-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="ae6a4-319">Идентификатор клиента подписки Azure, в которой расположено хранилище Key Vault</span><span class="sxs-lookup"><span data-stu-id="ae6a4-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="ae6a4-320">Код клиента, в котором расположены учетная запись хранения, приложения и хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="ae6a4-321">Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="ae6a4-322">Укажите DNS-имя вашего Key Vault</span><span class="sxs-lookup"><span data-stu-id="ae6a4-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="ae6a4-323">DNS-имя хранилища ключа, например `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="ae6a4-324">(Это значение соответствует DNS-имени, которое используется в хранилище сущностей.)</span><span class="sxs-lookup"><span data-stu-id="ae6a4-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="ae6a4-325">Введите секрет, содержащий имя учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ae6a4-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="ae6a4-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="ae6a4-327">Имя секрета для кода приложения, которое будет использоваться для доступа к Data Lake</span><span class="sxs-lookup"><span data-stu-id="ae6a4-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="ae6a4-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-328">**app-id**</span></span> |
    | <span data-ttu-id="ae6a4-329">Имя секрета для использования с кодом приложения</span><span class="sxs-lookup"><span data-stu-id="ae6a4-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="ae6a4-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="ae6a4-330">**app-secret**</span></span> |

5. <span data-ttu-id="ae6a4-331">Примите условия и выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="ae6a4-332">Надстройка будет установлена в течение нескольких минут.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="ae6a4-333">Настройка AI Builder</span><span class="sxs-lookup"><span data-stu-id="ae6a4-333">Configure AI Builder</span></span>

1. <span data-ttu-id="ae6a4-334">Выполните вход в LCS и откройте страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="ae6a4-335">Перейдите в раздел **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="ae6a4-336">Вы должны увидеть надстройки, уже установленные в этой среде.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="ae6a4-337">Если надстройка **Экспорт в Data Lake** среди них отсутствует, настройте эту надстройку.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="ae6a4-338">Выберите надстройку **Получить анализ**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="ae6a4-339">На странице сведений о надстройке **Получить анализ** введите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="ae6a4-340">значение</span><span class="sxs-lookup"><span data-stu-id="ae6a4-340">Value</span></span>                                                    | <span data-ttu-id="ae6a4-341">описание</span><span class="sxs-lookup"><span data-stu-id="ae6a4-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="ae6a4-342">URL-адрес организации CDS</span><span class="sxs-lookup"><span data-stu-id="ae6a4-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="ae6a4-343">URL-адрес организации Dataverse экземпляра Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae6a4-343">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="ae6a4-344">Чтобы найти это значение, откройте [портал Power Apps](https://make.powerapps.com), нажмите кнопку **Параметры** (символ шестеренки) в верхнем правом верхнем углу, выберите **Дополнительные параметры** и скопируйте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="ae6a4-345">(URL-адрес заканчивается на "dynamics.com".)</span><span class="sxs-lookup"><span data-stu-id="ae6a4-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="ae6a4-346">Код организации CDS</span><span class="sxs-lookup"><span data-stu-id="ae6a4-346">CDS Org ID</span></span>                                               | <span data-ttu-id="ae6a4-347">Код среды экземпляра Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-347">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="ae6a4-348">Чтобы найти это значение, откройте [портал Power Apps](https://make.powerapps.com), нажмите кнопку **Параметры** (символ шестеренки) в верхнем правом верхнем углу, выберите **Настройки \> Ресурсы разработчика \> Справочная информация экземпляра** и скопируйте значение **Код**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="ae6a4-349">Код клиента CDS (код каталога из AAD)</span><span class="sxs-lookup"><span data-stu-id="ae6a4-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="ae6a4-350">Код клиента экземпляра Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-350">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="ae6a4-351">Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="ae6a4-352">Укажите код объекта пользователя, имеющего роль системного администратора</span><span class="sxs-lookup"><span data-stu-id="ae6a4-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="ae6a4-353">Код объекта пользователя Azure AD для пользователя в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-353">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="ae6a4-354">Этот пользователь должен быть системным администратором экземпляра Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-354">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="ae6a4-355">Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите к разделу **Azure Active Directory \> Пользователи**, выберите пользователя, затем в разделе **Удостоверение** скопируйте значение **Код объекта**.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="ae6a4-356">Является ли данная среда средой CDS по умолчанию для клиента?</span><span class="sxs-lookup"><span data-stu-id="ae6a4-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="ae6a4-357">Если экземпляр Dataverse был первым созданным производственным экземпляром, установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-357">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="ae6a4-358">Если экземпляр Dataverse создан вручную, снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-358">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="ae6a4-359">Отзывы и поддержка</span><span class="sxs-lookup"><span data-stu-id="ae6a4-359">Feedback and support</span></span>

<span data-ttu-id="ae6a4-360">Отправьте сообщение электронной почты по адресу [Аналитика платежей клиентов (предварительная версия)](mailto:fiap@microsoft.com), если вы хотите предоставить отзыв или вам нужна поддержка.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="ae6a4-361">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="ae6a4-361">Privacy notice</span></span>

<span data-ttu-id="ae6a4-362">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
