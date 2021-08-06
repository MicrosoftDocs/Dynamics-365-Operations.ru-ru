---
title: Конфигурация для Finance Insights — до версии 10.0.19
description: В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в Finance Insights для версий до 10.0.19.
author: ShivamPandey-msft
ms.date: 07/21/2021
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
ms.openlocfilehash: 9f46fd95b516eeff4b716a0ecc093f94fac722af
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638736"
---
# <a name="configuration-for-finance-insights-for-private-preview-preview---before-version-10019"></a>Конфигурация для закрытой предварительной версии Finance Insights — до версии 10.0.19

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Следующие процедуры настройки Finance Insights действительны для Microsoft Dynamics 365 Finance до версии 10.0.19. Чтобы настроить Finance Insights в версии 10.0.20 и позже, см. раздел [Настройка для Finance Insights (предварительная версия) — версии 10.0.20 и старше](configure-for-fin-insites-PubPrvw.md).

Финансовый анализ сочетает в себе функции из Microsoft Dynamics 365 Finance с Microsoft Dataverse, Azure и AI Builder, чтобы предоставить мощные средства прогнозирования для вашей организации. В этой теме описываются этапы настройки, которые позволят системе использовать возможности, доступные в финансовом анализе.

## <a name="deploy-dynamics-365-finance"></a>Разверните Dynamics 365 Finance

Разверните среды, выполнив следующие шаги.

1. В Microsoft Dynamics Lifecycle Services (LCS) создайте или обновите среду Dynamics 365 Finance. Среде требуется версия приложения 10.0.11/Platform Update 35 или более поздней версии.
2. Среда должна быть средой с высокой доступностью (HA) в песочнице. (Этот тип среды также известен как среда уровня 2.) Дополнительные сведения см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. При настройке Finance Insights в среде песочницы, возможно, потребуется скопировать в эту среду производственные данные, чтобы прогнозы работали. Модель прогнозирования использует несколько лет данных для создания прогнозов. Демонстрационные данные Contoso не содержат достаточно исторических данных для адекватной тренировки прогнозной модели. 

## <a name="configure-dataverse"></a>Настроить Dataverse

Выполните следующие действия, чтобы настроить Dataverse для Finance Insights.

1. Откройте страницу среды в LCS и убедитесь, что раздел **Интеграция Power Platform** уже настроен.
    1. Если уже настроено, должно быть указано имя среды Dataverse, связанное со средой Dynamics 365 Finance. Скопируйте имя среды Dataverse.
    2. Если не настроено, выполните следующие действия:
        1. Нажмите кнопку **Настройка** в разделе интеграции Power Platform. Настройка среды может занять до часа.
        2. Если среда Dataverse успешно настроена, должно быть указано имя среды Dataverse, связанной со средой Dynamics 365 Finance. Скопируйте имя среды Dataverse.
> [!NOTE]
> После завершения настройки среды **НЕ ВЫБИРАЙТЕ** кнопку **Ссылка на CDS для приложений**. Это не требуется для Finance Insights и отключит возможность завершения необходимых надстроек среды в LCS.

2. Откройте [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/) и выполните следующие действия, чтобы создать новую среду Dataverse в одном и том же клиенте Active Directory:

    1. Откройте страницу **Среды**.

        [![Страница сред.](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Выберите созданную выше среду Dataverse, затем выберите **Параметры**.
    3. Выберите **Ресурсы \> Все устаревшие параметры**.
    4. На верхней панели навигации выберите **Параметры**, а затем выберите **Настройки**.
    5. Выберите **Ресурсы разработчика**.
    6. Скопируйте значение **Код организации Dataverse**.
    7. В адресной строке браузера запишите URL-адрес для организации Dataverse. Например, может быть указан URL-адрес `https://org42b2b3d3.crm.dynamics.com`.

3. Если планируется использовать функцию прогнозов движения денежных средств или прогнозов бюджета, выполните следующие действия, чтобы обновить ограничение для аннотации организации как минимум до 50 мегабайт (МБ):

    1. Откройте [портал Power Apps](https://make.powerapps.com).
    2. Выберите только что созданную среду, а затем выберите **Дополнительные параметры**.
    3. Выберите **Параметры \> Конфигурация электронной почты**.
    4. Измените значение поля **Максимальный размер файла** на **51200**. (Это значение задается в килобайтах \[КБ\].)
    5. Выберите **ОК**, чтобы сохранить изменения.

## <a name="configure-the-azure-setup"></a>Задание настройки Azure

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Введите код каталога Dataverse и код объекта пользователя Azure AD

1. Введите код каталога Dataverse:

    1. Откройте [портал Azure](https://portal.azure.com).
    2. Выполните вход, используя код пользователя, который использовался при создании среды Dataverse.
    3. Перейдите на страницу **Azure Active Directory**.
    4. Скопируйте значение **Код клиента**.

2. Введите код объекта Azure Active Directory (Azure AD) пользователя:

    1. На [портале Azure](https://portal.azure.com) перейдите в раздел **Пользователи** и выполните поиск пользователя по адресу электронной почты.
    2. Выберите имя пользователя.
    3. Скопируйте значение **Код объекта**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Использование Azure Cloud Shell для настройки ресурсов Data Lake финансового анализа

# <a name="use-a-windows-powershell-script"></a>[Использование сценария Windows PowerShell](#tab/use-a-powershell-script)

Был предоставлен сценарий Windows PowerShell, который позволяет легко настроить ресурсы Azure, описанные в разделе [Настройка экспорта в Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Если вы предпочитаете выполнить настройку вручную, пропустите эту процедуру и продолжите процедуру, описанную в разделе [Настройка вручную](#manual-setup).

> [!NOTE]
> Выполните приведенные ниже шаги, чтобы выполнить сценарий PowerShell. Параметр Azure CLI "Попробовать" или запуск сценария на компьютере может не работать.

Выполните следующие действия, чтобы настроить Azure с помощью сценария Windows PowerShell. Необходимо иметь права на создание группы ресурсов Azure, ресурсов Azure и приложения Azure AD. Сведения о необходимых разрешениях см. в разделе [Проверка разрешений Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. На [портале Azure](https://portal.azure.com) перейдите к целевой подписке Azure. Выберите кнопку **Cloud Shell** справа от поля **Поиск**.
2. Выберите **PowerShell**.
3. В случае появлении соответствующего запроса создайте хранилище.
4. Перейдите на вкладку **Azure CLI** и выберите **Копировать**.  
5. Откройте Блокнот и вставьте сценарий PowerShell. Сохраните файл под именем ConfigureDataLake.ps1.
6. Отправьте сценарий Windows PowerShell в сеанс, используя команду меню для отправки в Cloud Shell.
7. Выполните сценарий .\ConfigureDataLake.ps1.
8. Следуйте инструкциям для выполнения сценария.
9. Используйте сведения из выходных данных сценария для установки надстройки **Экспорт в Data Lake** в LCS.
10. Используйте сведения из выходных данных сценария для включения хранилища сущностей на странице **Подключения данных** в Finance (**Администрирование системы \> Параметры системы \> Подключения данных**).

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
> Убедитесь, что следующие ресурсы созданы в том же экземпляре Azure AD, что и среда Dataverse. Нельзя использовать ресурсы из других экземпляров Azure AD.

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
    | URL-адрес организации CDS                                     | URL-адрес организации Dataverse, скопированный ранее. |
    | Код организации CDS                                               | Код организации Dataverse, скопированный ранее. |
5. Включите **Является ли данная среда средой по умолчанию для клиента**.

Установка надстройки может занять несколько минут.
    
## <a name="configure-the-entity-store"></a>Настройка хранилища сущностей

Выполните следующие действия, чтобы настроить хранилище сущностей в среде Finance.

1. Перейдите в раздел **Администрирование системы \> Настройка \> Параметры системы \> Подключения данных**.
2. Настройте следующие поля хранилища ключей:

    - **Код приложения (клиента)** — введите код клиента приложения, который был создан ранее.
    - **Секрет приложения** — введите секрет, сохраненный для ранее созданного приложения.
    - **DNS-имя** — имя службы доменных имен (DNS) можно найти на странице сведения о приложении для приложения, которое было создано вами ранее.
    - **Имя секрета** — введите **storage-account-connection-string**.
3. Включите **Разрешить интеграцию с Data Lake**.
4. Выберите **Проверка Azure Key Vault** и убедитесь в отсутствии ошибок.
5. Выберите **Проверка хранилища Azure** и убедитесь в отсутствии ошибок.

## <a name="feedback-and-support"></a>Отзывы и поддержка

Отправьте сообщение электронной почты по адресу [Аналитика платежей клиентов (предварительная версия)](mailto:fiap@microsoft.com), если вы хотите предоставить отзыв или вам нужна поддержка.

## <a name="privacy-notice"></a>Уведомление о конфиденциальности

Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
