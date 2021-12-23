---
title: Развертывание пограничных единиц масштабирования на пользовательском оборудовании с помощью LBD
description: В этой теме объясняется, как подготавливать локальные пограничные единицы масштабирования с помощью пользовательского оборудования и развертывания на основе локальных бизнес-данных (LBD).
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8913debd614827ef66ded88e0da61663ca9c6b3d
ms.sourcegitcommit: 29d34f2fd509e2bb27d8572cd57c397d014a8e38
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/07/2021
ms.locfileid: "7894726"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Развертывание пограничных единиц масштабирования на пользовательском оборудовании с помощью LBD

[!include [banner](../includes/banner.md)]

Пограничные единицы масштабирования играют важную роль в распределенной гибридной топологии для управления цепочкой поставок. В гибридной топологии можно распределить рабочие нагрузки между облачным центром Supply Chain Management и дополнительными единицами масштабирования в облаке или на пограничном уровне.

Пограничные единицы масштабирования могут быть развернуты путем создания локальных бизнес-данных (LBD) [в локальной среде](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md), а затем настроены для функционирования в качестве единицы масштабирования в распределенной гибридной топологии для управления цепочкой поставок. Это достигается путем связывания локальной среды LBD со средой Supply Chain Management в облаке, которая была настроена для работы в качестве концентратора.  

В этой теме описывается, как настроить локальную среду LBD в качестве пограничной единицы масштабирования и затем связать ее с концентратором.

## <a name="deployment-overview"></a>Обзор развертывания

Ниже приведены шаги развертывания.

1. **Включите слот LBD в проекте LBD в Microsoft Dynamics Lifecycle Services (LCS).**

1. **Установка и развертывание среды LBD с *пустой* базой данных.**

    LCS можно использовать для развертывания среды LBD с последней топологией и пустой базой данных. Дополнительные сведения см. в разделе [Настройка и развертывание среды LBD с пустой базой данных](#set-up-deploy) далее в этой теме. Следует использовать версию Supply Chain Management 10.0.21 или новее в средах концентратора и единицы масштабирования.

1. **Отправка целевых пакетов в активы проекта LBD в LCS.**

    Подготовка пакетов приложений, платформ и настроек, которые используются в концентраторе и в пограничных единицах масштабирования. Дополнительные сведения см. в разделе [Отправка целевых пакетов в активы проекта LBD в LCS](#upload-packages) далее в этой теме.

1. **Обслуживание среды LBD с целевыми пакетами.**

    Этот шаг гарантирует, что в концентраторе и луче развернуты те же сборка и настройки. Дополнительные сведения см. в разделе [Обслуживание среды LBD с целевыми пакетами](#service-target-packages) далее в этой теме.

1. **Выполните настройку единиц масштабирования и назначение рабочей нагрузки.**

    Дополнительные сведения см. в разделе [Назначение пограничной единицы масштабирования LBD концентратору](#assign-edge-to-hub) далее в этой теме.

В остальных разделах этой темы приведены дополнительные сведения о выполнении этих шагов.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Установка и развертывание среды LBD с пустой базой данных

На этом шаге создается функциональная среда LBD. Однако среда не обязательно должна иметь одинаковую версию приложения и платформы в качестве среды концентратора. Кроме того, еще не хватает настроек, и она не может работать в качестве единицы масштабирования.

1. Следуйте инструкциям по [установке и развертыванию локальных сред (обновление платформы 41 и новее)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Следует использовать версию Supply Chain Management 10.0.21 или новее в средах концентратора и единицы масштабирования. Кроме того, необходимо использовать сценарии инфраструктуры версии 2.12.0 или более поздней. 

    > [!IMPORTANT]
    > Ознакомьтесь с оставшейся частью данного раздела **перед** выполнением шагов, описанных в этом разделе.

1. Перед описанием конфигурации в файле infrastructure\\ConfigTemplate.xml выполните следующий сценарий:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Этот сценарий удалит все конфигурации, которые не требуются для развертывания пограничных единиц масштабирования.

1. Настройте базу данных, содержащую пустые данные, как описано в разделе [Настройка баз данных](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Для этого шага используйте пустой файл data.bak.
1. После выполнения шага [Настройка баз данных](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) выполните следующий сценарий для конфигурирования базы данных оркестратора ALM единицы масштабирования.

    > [!NOTE]
    > Не настраивайте базу данных Financial Reporting на шаге [Настройка баз данных](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Сценарий Initialize-Database.ps1 выполняет следующие действия:

    1. Создайте пустую базу данных с именем **ScaleUnitAlmDb**.
    2. Сопоставьте пользователей с ролями базы данных на основе следующей таблицы.

        | Пользователь            | Тип | Роль базы данных |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. Продолжайте следовать инструкциям по [установке и развертыванию локальных сред (обновление платформы 41 и новее)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. После завершения шага [Настройка службы AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) выполните следующие действия:

    1. Создайте новое приложение службы федерации Active Directory (AD FS), которое позволит службе оркестрации ALM обмениваться данными с сервером Application Object Server (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Создайте новое приложение Azure Active Directory (Azure AD), которое позволит службе оркестрации ALM обмениваться данными со службой управления единицей масштабирования.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Продолжайте следовать инструкциям по [установке и развертыванию локальных сред (обновление платформы 41 и новее)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Когда необходимо ввести конфигурацию для локального агента, убедитесь, что включены функции Edge Scale Unit и указаны все необходимые параметры.

    ![Включение функций Edge Scale Unit.](media/EnableEdgeScaleUnitFeatures.png "Включение функций Edge Scale Unit.")

1. Перед развертыванием среды из LCS настройте скрипт, выполняемый перед развертыванием. Дополнительные сведения см. в разделе [Сценарии, выполняемые перед развертыванием и после развертывания локального агента](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Скопируйте скрипт Configure-CloudAndEdge.ps1 из папки **ScaleUnit** в разделе **Сценарии инфраструктуры** в папку **Scripts** в общей папке хранилища файлов агента, которая была настроена в среде. Типичным путем является \\\\lbdiscsi01\\agent\\Scripts.
    2. Создайте сценарий **PreDeployment.ps1**, который будет вызывать сценарии с использованием обязательных параметров. Сценарий, выполняемый перед развертыванием, должен быть помещен в папку **Scripts** в общем ресурсе хранилища файлов агента. В противном случае он не может быть выполнен. Типичным путем является \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Содержимое сценария PreDeployment.ps1 будет аналогичным в следующем примере.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > Параметр InstanceId должен состоять из двух символов. Первый символ — @, второй — любая прописная буква английского алфавита.
        >
        > - Допустимые значения:
        >   - @D
        >   - @X
        > - Недопустимые значения:
        >   - @a
        >   - @4
        >   - @#

1. Разверните среду, используя последнюю доступную базовую топологию.
1. После того как ваша среда развернута, выполните следующие действия:

    1. Выполните следующие команды SQL в бизнес-базе данных (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Увеличьте значение одновременных максимальных пакетных сеансов до значения, которое больше 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Убедитесь, что в бизнес-базе данных включено отслеживание изменений (AXDB).

        1. Откройте SQL Server Management Studio (SSMS).
        1. Выберите и удерживайте (или щелкните правой кнопкой мыши) вашу базу бизнес-данных (AXDB), затем выберите **Свойства**.
        1. В появившемся окне выберите **Отслеживание изменений** и затем задайте следующие значения:

            - **Отслеживание изменений:** *Истина*
            - **Период хранения:** *7*
            - **Единицы удержания:** *дни*
            - **Автоматическая очистка:** *Истина*

    1. Добавьте код приложения AD FS, созданный ранее (с помощью сценария Create-ADFSServerApplicationForEdgeScaleUnits.ps1), в таблицу приложений Azure AD в вашей единице масштабирования. Этот шаг можно выполнить вручную с помощью пользовательского интерфейса (UI). Кроме того, можно выполнить его в базе данных, используя следующий сценарий.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Настройка Azure Key Vault и приложения Azure AD для обеспечения взаимодействия между единицами масштабирования

1. После развертывания среды создайте дополнительное приложение Azure AD для обеспечения доверенного обмена данными между концентратором и единицей масштабирования.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. После создания приложения необходимо создать секрет клиента и сохранить сведения в Azure Key Vault. Кроме того, необходимо предоставить доступ к созданному приложению Azure AD, чтобы оно могло извлечь секреты, хранящиеся в этом хранилище ключей. Для удобства следующий сценарий автоматически выполнит все необходимые действия.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Если не существует ни одного хранилища ключей с указанным значением **KeyVaultName**, оно автоматически создается сценарием.

1. Добавьте только что созданный код приложения Azure AD (при использовании сценария Create-SpokeToHubAADApplication.ps1) в таблицу приложений Azure AD в концентраторе. Этот шаг можно выполнить вручную с помощью пользовательского интерфейса.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Отправка целевых пакетов в активы проекта LBD в LCS

Этот шаг позволяет подготовить версию приложения, версию платформы и настройки, которые будут перенесены в среду единицы масштабирования LBD.

1. Отправьте одинаковый комбинированный пакет приложения/платформы, который был применен к среде концентратора, в библиотеку активов локального проекта LCS.
1. Получите копию настраиваемого развертываемого пакета, который был применен к среде концентратора, и отправьте в библиотеку активов локального проекта LCS.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Обслуживание среды LBD с целевыми пакетами

Этот шаг сопоставляет версию приложения, версию платформы и настройки в среде единицы масштабирования LBD с концентратором.

1. Обслуживание среды LBD с объединенным пакетом приложения/платформы, который был отправлен на предыдущем шаге.
1. Обслуживание среды LBD с настраиваемым развертываемым пакетом, который был отправлен на предыдущем шаге.

    ![Применение обновлений в LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Применение обновлений в LCS")

    ![Выбор вашего пакета настройки.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Выбор вашего пакета настройки")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Назначение пограничной единицы масштабирования LBD концентратору

Настройка и управление пограничной единицей масштабирования осуществляется с помощью портала управления единицами масштабирования. Дополнительные сведения см. в разделе [Управление единицами масштабирования и рабочими нагрузками с помощью портала диспетчера единиц масштабирования](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
