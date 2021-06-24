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
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a>Конфигурация для общедоступной предварительной версии Finance Insights — версия 10.0.20 и более поздняя

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Финансовый анализ сочетает в себе функции из Microsoft Dynamics 365 Finance с Dataverse, Azure и AI Builder, чтобы предоставить мощные средства прогнозирования для вашей организации. В этой теме объясняется, как настроить Dynamics 365 Finance версии 10.0.20, чтобы система могла использовать возможности, доступные в общедоступной предварительной версии Finance Insights.

> [!NOTE]
> Шаги конфигурации, описанные в данной теме, применимы только к Finance версии 10.0.20 и более поздним версиям. Чтобы настроить Finance Insights в версии 10.0.19 и более ранних, см. раздел [Настройка для Finance Insights — версии до 10.0.18](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Развертывание Finance

Выполните следующие шаги, чтобы развернуть среды.

1. В Microsoft Dynamics Lifecycle Services (LCS) создайте или обновите среду Finance. Среде требуется версия 10.0.20 или более поздней версии приложений Finance and Operations.
2. Среда должна быть средой с высокой доступностью (HA) в песочнице. (Этот тип среды также известен как среда уровня 2.) Дополнительные сведения см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. При настройке Finance Insights в среде песочницы, возможно, потребуется скопировать в эту среду производственные данные, чтобы прогнозы работали. Модель прогнозирования использует несколько лет данных для создания прогнозов. Демонстрационные данные Contoso не содержат достаточно исторических данных для адекватной тренировки прогнозной модели. 

## <a name="configure-dataverse"></a>Настроить Dataverse

Выполните следующие шаги, чтобы настроить Dataverse для Finance Insights.

1. В LCS откройте страницу среды и убедитесь, что раздел **Интеграция Power Platform** уже настроен.

    - Если уже настроен, должно быть указано имя среды Dataverse, связанной со средой Finance.
    - Если не настроен, выполните следующие действия:

        1. В разделе **Интеграция Power Platform** выберите **Настройка**. Настройка среды может занять около часа.
        2. Если среда Dataverse успешно настроена, должно быть указано имя среды Dataverse, связанной со средой Finance.

        > [!NOTE]
        > После завершения настройки среды **не** выбирайте ссылку **Ссылка на CDS для приложений**. Эта кнопка не требуется для Finance Insights. Если вы ее выберите, вы не сможете настроить необходимые надстройки среды в LCS.

## <a name="configure-azure"></a>Настройка Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Использование Azure Cloud Shell для настройки ресурсов Data Lake финансового анализа

# <a name="use-a-windows-powershell-script"></a>[Использование сценария Windows PowerShell](#tab/use-a-powershell-script)

Был предоставлен сценарий Windows PowerShell, который позволяет легко настроить ресурсы Azure, описанные в разделе [Настройка экспорта в Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Если вы предпочитаете выполнить настройку вручную, пропустите эту процедуру и выполните процедуру, описанную в разделе [Настройка вручную](#manual-setup).

> [!NOTE]
> Для выполнения сценария Windows PowerShell используется следующая процедура. Настройка может не работать, если используется вариант **Попробовать** в Azure CLI или если на компьютере выполняется сценарий.

Выполните следующие действия, используя Windows PowerShell, чтобы настроить Azure. Необходимо иметь права на создание группы ресурсов Azure, ресурсов Azure и приложения Azure AD. Сведения о необходимых разрешениях см. в разделе [Проверка разрешений Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. На [портале Azure](https://portal.azure.com) перейдите к целевой подписке Azure.
2. Выберите **Cloud Shell** справа от поля **Поиск**.
3. Выберите **PowerShell**.
4. Создайте хранилище, если будет предложено его создать.
5. На вкладке **Azure CLI** выберите **Копировать**.
6. Откройте новый файл в блокноте и вставьте в его сценарий Windows PowerShell.
7. Сохраните файл под именем **ConfigureDataLake.ps1**.
8. Отправьте сценарий Windows PowerShell в сеанс, используя команду меню для отправки в Cloud Shell.
9. Выполните сценарий **.\ConfigureDataLake.ps1**.
10. Следуйте инструкциям для выполнения сценария.
11. Используйте сведения из выходных данных сценария для установки надстройки Экспорт в Data Lake в LCS.

### <a name="manual-setup"></a>Настройка вручную

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Добавление приложений в клиент Azure AD

1. На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**.
2. Выберите **Управление \> Корпоративные приложения**.
3. Выполните поиск следующих приложений по коду приложения.

    | Заявление                              | Код приложения                               |
    |------------------------------------------|--------------------------------------|
    | Микрослужбы Microsoft Dynamics ERP     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Микрослужбы Microsoft Dynamics ERP CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | Служба авторизации AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Если не удается найти какое-либо из вышеперечисленных приложений, попробуйте выполнить следующие действия

1. На локальном компьютере в меню **Пуск** найдите **powershell**.
2. Выберите и удерживайте (или щелкните правой кнопкой мыши) **Windows PowerShell**, затем выберите команду **Запуск от имени администратора**.
3. Выполните следующую команду для установки модуля **AzureAD**.

    `Install-Module -Name AzureAD`

4. Если для продолжения требуется поставщик NuGet, выберите **Y**, чтобы установить его.
5. В случае получения сообщения "Ненадежный репозиторий" выберите **Y** для продолжения.
6. Для каждого приложения, которое необходимо добавить, выполните следующие команды, чтобы добавить приложение в Azure AD. При появлении запроса войдите в систему как администратор Azure AD.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Создание ресурсов Azure

> [!NOTE]
> Убедитесь, что следующие ресурсы созданы в том же экземпляре Azure AD, в котором находится среда Dataverse. Нельзя использовать ресурсы из других экземпляров Azure AD.

1. Создайте учетную запись хранения:

    1. На [портале Azure](https://portal.azure.com) создайте учетную запись хранения.
    2. В диалоговом окне **Создание учетной записи хранения** установите следующие поля:

        - **Местонахождение** — выберите центр обработки данных, в котором находится среда.
        - **Производительность** — рекомендуется выбирать **Стандартная**.
        - **Вид учетной записи** — необходимо выбрать **StorageV2**.

    3. В диалоговом окне **Дополнительные параметры** для параметра **Data Lake storage Gen2** выберите **Включить** в функции **Иерархические пространства имен**. Если эта функция не включена, вы не сможете потреблять данные, которые приложения Finance and Operations записывают с помощью таких служб, как потоки данных Power BI.
    4. Выберите **Просмотр и создание**. После завершения развертывания новый ресурс будет показан на портале Azure.
    5. Перейдите к созданной учетной записи хранения.
    6. В левом меню выберите **Ключи доступа**.
    7. Скопируйте и сохраните имя учетной записи хранения. Это значение будет необходимо ввести позднее при настройке секретов хранилища ключей.

2. Создайте хранилище ключей:

    1. На [портале Azure](https://portal.azure.com) создайте хранилище ключей.
    2. В диалоговом окне **Создать хранилище ключей** в поле **Расположение** выберите центр обработки данных, в котором находится среда.
    3. После создания хранилища ключей перейдите к пункту **Обзор Key Vault** и скопируйте и сохраните DNS-имя. Это значение будет необходимо ввести позднее при настройке надстройки Data Lake.

3. Создание и регистрация приложения Azure AD:

    1. На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**, затем выберите **Регистрации приложений**.
    2. Выберите **Регистрация нового приложения** и задайте следующие поля:

        - **Имя** — введите имя приложения.
        - **Тип приложения** — выберите **Веб-API**.
        - **Настройка URI перенаправления** — введите URL-адрес для экземпляра Dynamics 365, например, `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Перейдите к только что созданному приложению и скопируйте его значение **Код приложения (клиента)**. Это значение будет необходимо ввести позднее при настройке секретов хранилища ключей.
    4. Перейдите на страницу **Разрешения API** и выполните следующие действия:

        1. Выберите **Добавить разрешение**.
        2. Выберите **Azure Key Vault**.
        3. После выбора делегированных разрешений выберите **user\_impersonation**.
        4. Выберите **Добавить разрешения**.

    5. В меню приложения выберите **Сертификаты \& секреты**, затем выполните следующие действия, чтобы создать секреты для Key Vault:

        1. Выберите **Создать секрет клиента**.
        2. В поле **Описание ключа** введите имя.
        3. Выберите длительность, затем выберите **Добавить**. Секрет создается в поле **Значение**.
        4. Скопируйте и сохраните значение секрета клиента. Это значение будет необходимо ввести позднее при настройке секретов хранилища ключей.

4. Создайте секреты Key Vault:

    1. Перейдите к созданному ранее хранилищу ключей и выберите **Секреты**.
    2. Для каждого имени секрета в следующей таблице выполните следующие действия:

        1. Выберите **Создать/Импортировать**.
        2. В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.
        3. Создайте имя и значение секрета из таблицы.
        4. Выберите **Включено**, затем выберите **Создать**. Секрет создается и добавляется в Key Vault.

        | Имя секрета                       | Значение секрета                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | Код приложения, созданного ранее.                                      |
        | app-secret                        | Секрет клиента, который был сохранен ранее.                                                    |
        | storage-account-name              | Имя созданной ранее учетной записи хранения, например **storageaccount1**.       |

5. Авторизуйте приложение для доступа к хранилищу ключей:

    1. На [портале Azure](https://portal.azure.com) откройте созданное ранее хранилище ключей.
    2. Выберите политики доступа.
    3. Для каждого приложения в следующей таблице выполните следующие действия:

        1. Выберите **Добавить политику доступа**, чтобы создать политику доступа.
        2. В поле **Разрешения секрета** выберите разрешения из таблицы.
        3. В поле **Выберите субъект** найдите отображаемое имя приложения из таблицы.
        4. Выберите **Выбрать**.
        5. Выберите **Добавить**.
        6. Нажмите **Сохранить**.

        | Заявление                                              | Права доступа |
        |----------------------------------------------------------|-------------|
        | Отображаемое имя нового приложения, созданного вами | Получить, Список   |
        | **Микрослужбы Microsoft Dynamics ERP**                 | Получить, Список   |

6. Назначьте роли для доступа к учетной записи хранения:

    1. На [портале Azure](https://portal.azure.com) откройте созданную ранее учетную запись хранения.
    2. Выберите **Управление доступом (IAM)**, затем выберите **Назначения ролей**.
    3. Выберите **Добавить, Добавить назначение ролей**.
    4. Для каждого приложения в следующей таблице выполните следующие действия:

        1. Выбор роли из таблицы.
        2. В поле **Назначить доступ** оставьте значение **Пользователь, группа или субъект-служба Azure AD**
        3. В поле **Выбрать** введите приложение из таблицы.
        4. Нажмите **Сохранить**.

        | Заявление                                              | Роль                        |
        |----------------------------------------------------------|-----------------------------|
        | Отображаемое имя нового приложения, созданного вами | Ответственный                       |
        | Отображаемое имя нового приложения, созданного вами | Участник                 |
        | Отображаемое имя нового приложения, созданного вами | Участник учетных записей хранения |
        | Отображаемое имя нового приложения, созданного вами | Владелец данных BLOB-объектов хранилища     |
        | **Служба авторизации AI Builder**                     | Модуль чтения данных BLOB-объектов хранилища    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a>Настройка надстройки экспорта в Data Lake

Выполните следующие действия, чтобы использовать LCS для добавления надстройки экспорта в Data Lake в среду.

1. Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.
2. В разделе **Надстройки сред** выберите **Установить новую надстройку**.
3. Выберите надстройку **Экспорт в Data Lake**.
4. Введите следующие значения.

    | значение                                                              | описание |
    |--------------------------------------------------------------------|-------------|
    | Идентификатор клиента подписки Azure, в которой расположено хранилище Key Vault | Код клиента, в котором расположены учетная запись хранения, приложения и хранилища ключей. Чтобы получить это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**. |
    | Укажите DNS-имя вашего Key Vault                             | DNS-имя хранилища ключа, например `https://customkeyvault.vault.azure.net/`. |
    | Введите секрет, содержащий имя учетной записи хранения   | **storage-account-name** |
    | Имя секрета для кода приложения, которое будет использоваться для доступа к Data Lake          | **app-id** |
    | Имя секрета для секрета клиента приложения                                  | **app-secret** |

5. Примите условия, затем выберите **Установить**.

Надстройка будет установлена в течение нескольких минут.

## <a name="configure-the-finance-insights-add-in"></a>Настройка надстройки Finance Insights

> [!NOTE]
> Если ранее была установлена надстройка "Получить анализ", удалите ее перед выполнением следующей процедуры.

Выполните следующие шаги, чтобы установить надстройку Finance Insights.

1. Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.
2. В разделе **Надстройки сред** выберите **Установить новую надстройку**.
3. Выберите надстройку **Finance Insights**.
4. Примите условия, затем выберите **Установить**.

## <a name="feedback-and-support"></a>Отзывы и поддержка

Если вы хотите предоставить отзыв или вам нужна поддержка, отправьте сообщение электронной почты по адресу [Finance Insights (предварительная версия)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
