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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664098"
---
# <a name="configuration-for-finance-insights-preview"></a>Конфигурация для финансового анализа (предварительная версия)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Финансовый анализ сочетает в себе функции из Microsoft Dynamics 365 Finance с Common Data Service, Azure и AI Builder, чтобы предоставить мощные средства прогнозирования для вашей организации. В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в финансовом анализе.

## <a name="deploy-dynamics-365-finance"></a>Разверните Dynamics 365 Finance

Разверните среды, выполнив следующие шаги.

1. В Microsoft Dynamics Lifecycle Services (LCS) создайте или обновите среду Dynamics 365 Finance. Среде требуется версия приложения 10.0.11/Platform Update 35 или более поздней версии.
2. Среда должна быть средой с высокой доступностью (HA) в песочнице. (Этот тип среды также известен как среда уровня 2.) Дополнительные сведения см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Если используются демонстрационные данные компании Contoso, для использования функций прогнозирования платежей клиентов, прогнозов движения денежных средств и прогнозов бюджета потребуется дополнительный образец данных. 

## <a name="configure-common-data-service"></a>Настроить Common Data Service

Можно выполнить следующие действия по настройке вручную или можно ускорить процесс настройки, используя предлагаемый сценарий Windows PowerShell. После завершения выполнения сценария PowerShell вы получите значения, которые будут использоваться для настройки финансовой аналитики. 

> [!NOTE]
> Откройте PowerShell на своем компьютере, чтобы запустить сценарий. Возможно, вам понадобится PowerShell версии 5. Функция интерфейса командной строки Microsoft Azure "Попробовать" может не работать.

# <a name="manual-configuration-steps"></a>[Шаги конфигурации вручную](#tab/configuration-steps)

1. Откройте [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/) и выполните следующие действия, чтобы создать новую среду Common Data Service в одном и том же клиенте Active Directory:

    1. Откройте страницу **Среды**.

        [![Страница сред](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Выберите **Создать среду**.
    3. В поле **Тип** выберите **Песочница**.
    4. Установите параметр **Создать базу данных** на значение **Да**.
    5. Выберите **Далее**.
    6. Выберите язык и валюту для организации.
    7. Примите для остальных полей значения по умолчанию.
    8. Нажмите **Сохранить**.
    9. Обновите страницу **Среды**.
    10. Дождитесь, когда значение поля **Состояние** будет обновлено на **Готово**.
    11. Запишите код организации Common Data Service.
    12. Выберите среду, затем выберите **Параметры**.
    13. Выберите **Ресурсы \> Все устаревшие параметры**.
    14. На верхней панели навигации выберите **Параметры**, а затем выберите **Настройки**.
    15. Выберите **Ресурсы разработчика**.
    16. Задайте в поле **Код ссылки экземпляра** значение идентификатора организации Common Data Service, который вы записали ранее.
    17. В адресной строке браузера запишите URL-адрес для организации Common Data Service. Например, может быть указан URL-адрес `https://org42b2b3d3.crm.dynamics.com`.

2. Если планируется использовать функцию прогнозов движения денежных средств или прогнозов бюджета, выполните следующие действия, чтобы обновить ограничение для аннотации организации как минимум до 50 мегабайт (МБ):

    1. Откройте [портал Power Apps](https://make.powerapps.com).
    2. Выберите только что созданную среду, а затем выберите **Дополнительные параметры**.
    3. Выберите **Параметры \> Конфигурация электронной почты**.
    4. Измените значение поля **Максимальный размер файла** на **51200**. (Это значение задается в килобайтах \[КБ\].)
    5. Выберите **ОК**, чтобы сохранить изменения.

# <a name="windows-powershell-configuration-script"></a>[Сценарий конфигурации Windows PowerShell](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>Задание настройки Azure

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a>Введите код каталога Common Data Service и код объекта пользователя Azure AD

1. Введите код каталога Common Data Service:

    1. Откройте [портал Azure](https://portal.azure.com).
    2. Выполните вход, используя код пользователя, который использовался при создании среды Common Data Service.
    3. Перейдите на страницу **Azure Active Directory**.
    4. Скопируйте значение **Код клиента**.

2. Введите код объекта Azure Active Directory (Azure AD) пользователя:

    1. На [портале Azure](https://portal.azure.com) перейдите в раздел **Пользователи** и выполните поиск пользователя по адресу электронной почты.
    2. Выберите имя пользователя.
    3. Скопируйте значение **Код объекта**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Использование Azure Cloud Shell для настройки ресурсов Data Lake финансового анализа

# <a name="use-a-windows-powershell-script"></a>[Использование сценария Windows PowerShell](#tab/use-a-powershell-script)

Был предоставлен сценарий Windows PowerShell, который позволяет легко настроить ресурсы Azure, описанные в разделе [Настройка экспорта в Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake). Если вы предпочитаете выполнить настройку вручную, пропустите эту процедуру и продолжите процедуру, описанную в разделе [Настройка вручную](#manual-setup).

> [!NOTE]
> Выполните приведенные ниже шаги, чтобы выполнить сценарий PowerShell. Параметр Azure CLI "Попробовать" или запуск сценария на компьютере может не работать.

Выполните следующие действия, чтобы настроить Azure с помощью сценария Windows PowerShell. Необходимо иметь права на создание группы ресурсов Azure, ресурсов Azure и приложения Azure AD. Сведения о необходимых разрешениях см. в разделе [Проверка разрешений Azure AD](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. На [портале Azure](https://portal.azure.com) перейдите к целевой подписке Azure. Выберите кнопку **Cloud Shell** справа от поля **Поиск**.
2. Выберите **PowerShell**.
3. В случае появлении соответствующего запроса создайте хранилище. Затем отправьте сценарий Windows PowerShell в сеанс.
4. Выполните сценарий.
5. Следуйте инструкциям для выполнения сценария.
6. Используйте сведения из выходных данных сценария для установки надстройки **Экспорт в Data Lake** в LCS.
7. Используйте сведения из выходных данных сценария для включения хранилища сущностей на странице **Подключения данных** в Finance (**Администрирование системы \> Параметры системы \> Подключения данных**).

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

1. На локальном компьютере выберите меню **Пуск** и выполните поиск **powershell**.
2. Выберите и удерживайте (или щелкните правой кнопкой мыши) **Windows PowerShell**, затем выберите команду **Запуск от имени администратора**.
3. Выполните следующую команду для установки модуля **AzureAD**.

    `Install-Module -Name AzureAD`

4. Если для продолжения требуется поставщик NuGet, выберите **Y**, чтобы установить его.
5. В случае появления сообщения "Ненадежный репозиторий" выберите **Y** для продолжения.
6. Для каждого приложения, которое необходимо добавить, выполните следующие команды, чтобы добавить приложение в Azure AD. При появлении запроса войдите в систему как администратор Azure AD.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Создание ресурсов Azure

> [!NOTE]
> Убедитесь, что следующие ресурсы созданы в том же экземпляре Azure AD, что и среда Common Data Service. Нельзя использовать ресурсы из других экземпляров Azure AD.

1. Создайте новую учетную запись хранения:

    1. На [портале Azure](https://portal.azure.com) создайте учетную запись хранения.
    2. В диалоговом окне **Создание учетной записи хранения** установите следующие поля:

        - **Местонахождение** — выберите центр обработки данных, в котором находится среда.
        - **Производительность** — рекомендуется выбирать **Стандартная**.
        - **Вид учетной записи** — необходимо выбрать **StorageV2**.

    3. В диалоговом окне **Дополнительные параметры** для параметра **Data Lake storage Gen2** выберите **Включить** в функции **Иерархические пространства имен**. Если эта функция отключена, вы не сможете потреблять данные, которые приложения Finance and Operations записывают с помощью таких служб, как потоки данных Power BI.
    4. Выберите **Просмотр и создание**. После завершения развертывания новый ресурс будет показан на портале Azure.
    5. Перейдите к созданной учетной записи хранения.
    6. В левом меню выберите **Ключи доступа**.
    7. Скопируйте и сохраните строку подключения для **Key1** или **Key2**.
    8. Скопируйте и сохраните имя учетной записи хранения.

2. Создайте новое хранилище ключей:

    1. На [портале Azure](https://portal.azure.com) создайте хранилище ключей.
    2. В диалоговом окне **Создать хранилище ключей** в поле **Расположение** выберите центр обработки данных, в котором находится среда.
    3. После создания хранилища ключей выберите его в списке, а затем выберите **Секреты**.
    4. Выберите **Создать/Импортировать**.
    5. В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.
    6. Введите имя для секрета. Запишите имя, поскольку его потребуется указать позже.
    7. В поле **Значение** введите строку подключения, полученную из учетной записи хранения в предыдущей процедуре.
    8. Выберите **Включено**, затем выберите **Создать**. Секрет создается и добавляется в Key Vault.
    9. Перейдите в раздел **Обзор Key Vault** и запишите DNS-имя.

3. Создание и регистрация приложения Azure AD:

    1. На [портале Azure](https://portal.azure.com) перейдите в раздел **Azure Active Directory**, затем выберите **Регистрации приложений**.
    2. Выберите **Регистрация нового приложения** и задайте следующие поля:

        - **Имя** — введите имя приложения.
        - **Тип приложения** — выберите **Веб-API**.
        - **Настройка URI перенаправления** — введите URL-адрес для экземпляра Dynamics 365, например, `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Перейдите к только что созданному приложению и скопируйте его значение **Код приложения (клиента)**. Это значение будет необходимо ввести позднее при настройке хранилища ключей.
    4. Перейдите на страницу **Разрешения API** и выполните следующие действия:

        1. Выберите **Добавить разрешение**.
        2. Выберите **Azure Key Vault**.
        3. После выбора делегированных разрешений выберите **user\_impersonation**.
        4. Выберите **Добавить разрешения**.

    5. В меню приложения выберите **Сертификаты \& секреты**, затем выполните следующие действия, чтобы создать секреты для Key Vault:

        1. Выберите **Создать секрет клиента**.
        2. В поле **Описание ключа** введите имя.
        3. Выберите длительность, затем выберите **Добавить**. Секрет создается в поле **Значение**.
        4. Скопируйте и сохраните значение секрета.

4. Создайте секреты Key Vault:

    1. Перейдите к созданному ранее хранилищу ключей и выберите **Секреты**.
    2. Для каждого имени секрета в следующей таблице выполните следующие действия:

        1. Выберите **Создать/Импортировать**.
        2. В диалоговом окне **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.
        3. Создайте имя и значение секрета из следующей таблицы.
        4. Выберите **Включено**, затем выберите **Создать**. Секрет создается и добавляется в Key Vault.

        | Имя секрета                       | Значение секрета                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | Код приложения, созданного ранее                                      |
        | app-secret                        | Секрет клиента, который был сохранен ранее                                                    |
        | storage-account-name              | Имя созданной ранее учетной записи хранения, например **storageaccount1**       |
        | storage-account-connection-string | Строка подключения, скопированная со страницы **Ключи доступа** для учетной записи хранения |

5. Авторизуйте приложение для доступа к хранилищу ключей:

    1. На [портале Azure](https://portal.azure.com) откройте созданное ранее хранилище ключей.
    2. Выберите политики доступа.
    3. Для каждого приложения в следующей таблице выполните следующие действия:

        1. Выберите **Добавить политику доступа**, чтобы создать политику доступа.
        2. В поле **Разрешения секрета** выберите разрешения из следующей таблицы.
        3. В поле **Выберите субъект** найдите отображаемое имя приложения из следующей таблицы.
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

        1. Выберите роль из следующей таблицы.
        2. В поле **Назначить доступ** оставьте значение **Пользователь, группа или субъект-служба Azure AD**
        3. В поле **Выбрать** введите приложение из следующей таблицы.
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
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
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

## <a name="configure-the-entity-store"></a>Настройка хранилища сущностей

Выполните следующие действия, чтобы настроить хранилище сущностей в среде Finance.

1. Перейдите в раздел **Администрирование системы \> Настройка \> Параметры системы \> Подключения данных**.
2. Установите для параметра **Разрешить интеграцию с Data Lake** значение **Да**.
3. Настройте следующие поля Key Vault:

    - **Код приложения (клиента)** — введите код клиента приложения, который был создан ранее.
    - **Секрет приложения** — введите секрет, сохраненный для ранее созданного приложения.
    - **DNS-имя** — имя службы доменных имен (DNS) можно найти на странице сведения о приложении для приложения, которое было создано вами ранее.
    - **Имя секрета** — введите **storage-account-connection-string**.

## <a name="configure-the-data-lake"></a>Настройка Data Lake

Выполните следующие действия, чтобы использовать LCS для добавления надстройки Azure Data Lake в среду.

1. Выполните вход в LCS, а затем под именем среды в правой части страницы выберите **Полные сведения**.
2. В разделе **Надстройки сред** выберите **Установить новую надстройку**.
3. Выберите надстройку **Экспорт в Data Lake**.
4. Введите следующие значения.

    | значение                                                              | описание |
    |--------------------------------------------------------------------|-------------|
    | Идентификатор клиента подписки Azure, в которой расположено хранилище Key Vault | Код клиента, в котором расположены учетная запись хранения, приложения и хранилища ключей. Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**. |
    | Укажите DNS-имя вашего Key Vault                             | DNS-имя хранилища ключа, например `https://customkeyvault.vault.azure.net/`. (Это значение соответствует DNS-имени, которое используется в хранилище сущностей.) |
    | Введите секрет, содержащий имя учетной записи хранения   | **storage-account-name** |
    | Имя секрета для кода приложения, которое будет использоваться для доступа к Data Lake          | **app-id** |
    | Имя секрета для использования с кодом приложения                                 | **app-secret** |

5. Примите условия и выберите **Установить**.

Надстройка будет установлена в течение нескольких минут.

## <a name="configure-ai-builder"></a>Настройка AI Builder

1. Выполните вход в LCS и откройте страницу **Сведения о среде**.
2. Перейдите в раздел **Надстройки среды**. Вы должны увидеть надстройки, уже установленные в этой среде. Если надстройка **Экспорт в Data Lake** среди них отсутствует, настройте эту надстройку.
3. Выберите надстройку **Получить анализ**.
4. На странице сведений о надстройке **Получить анализ** введите следующие значения.

    | значение                                                    | описание |
    |----------------------------------------------------------|-------------|
    | URL-адрес организации CDS                                     | URL-адрес организации Common Data Service экземпляра Common Data Service Чтобы найти это значение, откройте [портал Power Apps](https://make.powerapps.com), нажмите кнопку **Параметры** (символ шестеренки) в верхнем правом верхнем углу, выберите **Дополнительные параметры** и скопируйте URL-адрес. (URL-адрес заканчивается на "dynamics.com".) |
    | Код организации CDS                                               | Код среды экземпляра Common Data Service. Чтобы найти это значение, откройте [портал Power Apps](https://make.powerapps.com), нажмите кнопку **Параметры** (символ шестеренки) в верхнем правом верхнем углу, выберите **Настройки \> Ресурсы разработчика \> Справочная информация экземпляра** и скопируйте значение **Код**. |
    | Код клиента CDS (код каталога из AAD)               | Код клиента экземпляра Common Data Service. Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите в раздел **Azure Active Directory** и скопируйте значение **Код клиента**. |
    | Укажите код объекта пользователя, имеющего роль системного администратора | Код объекта пользователя Azure AD для пользователя в Common Data Service. Этот пользователь должен быть системным администратором экземпляра Common Data Service. Чтобы найти это значение, откройте [портал Azure](https://portal.azure.com), перейдите к разделу **Azure Active Directory \> Пользователи**, выберите пользователя, затем в разделе **Удостоверение** скопируйте значение **Код объекта**. |
    | Является ли данная среда средой CDS по умолчанию для клиента?      | Если экземпляр Common Data Service был первым созданным производственным экземпляром, установите этот флажок. Если экземпляр Common Data Service создан вручную, снимите этот флажок. |

## <a name="feedback-and-support"></a>Отзывы и поддержка

Отправьте сообщение электронной почты по адресу [Аналитика платежей клиентов (предварительная версия)](mailto:fiap@microsoft.com), если вы хотите предоставить отзыв или вам нужна поддержка.

## <a name="privacy-notice"></a>Уведомление о конфиденциальности

Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.
