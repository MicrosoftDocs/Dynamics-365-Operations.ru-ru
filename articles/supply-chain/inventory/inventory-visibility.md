---
title: Надстройка видимости запасов
description: В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8faae53f66c069c53609dee72fa30ca18a22c9eb8a86b4669c745c00976af34d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742712"
---
# <a name="inventory-visibility-add-in"></a>Надстройка видимости запасов

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Надстройка для отображения запасов — это независимая и масштабируемая микрослужба, позволяющая осуществлять отслеживание запасов в наличии в реальном времени, обеспечивая таким образом глобальное представление отображения запасов.

Вся информация, относящаяся к запасам в наличии, экспортируется в службу практически в реальном времени с помощью SQL-интеграции низкого уровня. Внешние системы обращаются к службе через API RESTful для запроса информации о наличии по заданным наборам аналитик, тем самым получая список доступных позиций в наличии.

Видимость запасов — это микрослужба, основанная на Microsoft Dataverse, что означает, что ее можно расширить путем создания приложений Power Apps и применения Power BI для предоставления настраиваемых функций в соответствии с потребностями бизнеса. Возможно также обновление индекса для выполнения складских запросов.

Видимость запасов предоставляет параметры конфигурации, которые позволяют ей интегрироваться с несколькими системами сторонних производителей. Она поддерживает стандартизированную складскую аналитику, настраиваемую расширяемость и стандартизованные настраиваемые подсчитанные количества.

В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management и как использовать ее интерфейс программирования приложений (API).

## <a name="install-the-inventory-visibility-add-in"></a>Установка надстройки видимости запасов

Необходимо установить надстройку отображения запасов, используя Microsoft Dynamics Lifecycle Services (LCS). LCS — это портал совместной работы, который предоставляет среду и набор регулярно обновленных служб, которые помогут управлять жизненным циклом приложений Dynamics 365 Finance and Operations.

Дополнительные сведения см. в разделе [Ресурсы Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>Необходимые условия для надстройки контроля запасов

Перед установкой надстройки видимости запасов необходимо сделать следующее:

- Получите проект внедрения LCS с по крайней мере одной развернутой средой.
- Убедитесь, что необходимые условия для настройки надстроек в [Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), обеспечены. Для контроля запасов не требуется связывание с двойной записью.
- Для получения следующих трех необходимых файлов обратитесь к специалистам по контролю запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (если версия Supply Chain Management, которую вы используете, более ранняя, чем версия 10.0.18)
- Или же для получения пакетов Package Deployer обратитесь к специалистам по контролю запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Эти пакеты могут использоваться официальным средством Package Deployer.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip` (этот пакет содержит все изменения, внесенные в пакет `InventoryServiceBase` плюс дополнительные компоненты пользовательского интерфейса)
- Следуйте инструкциям, приведенным в [Быстрое начало: регистрация приложения на платформе Microsoft Identity](/azure/active-directory/develop/quickstart-register-app) для регистрации приложения и добавления секрета клиента в AAD в рамках подписки Azure.
  - [Регистрация приложения](/azure/active-directory/develop/quickstart-register-app)
  - [Добавить секрет клиента](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - **Код приложения (клиент)**, **Секрет клиента** и **Код клиента** будут использоваться в следующих шагах.

> [!NOTE]
> Поддерживаемые в настоящее время страны и регионы включают Канаду, США и Европейский союз (ЕС).

При возникновении каких-либо вопросов о необходимых условиях свяжитесь с группой разработчиков продукта для отображения запасов.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Настройка Dataverse

Чтобы настроить Dataverse для использования с контролем запасов, необходимо сначала подготовить необходимые компоненты, а затем решить, нужно ли настраивать Dataverse, используя либо инструмент Package Deployer, либо вручную импортировать решения (не нужно делать и то, и другое). Затем установите надстройку контроля запасов. Следующие подразделы описывают выполнение каждой задачи.

#### <a name="prepare-dataverse-prerequisites"></a>Подготовка необходимых компонентов Dataverse

Прежде чем приступить к настройке Dataverse, добавьте в клиент субъект-службу, выполнив следующие действия:

1. Установите модуль Azure AD PowerShell v2, как описано в подразделе [Установка Azure Active Directory PowerShell для Graph](/powershell/azure/active-directory/install-adv2).

1. Выполните следующую команду PowerShell:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>Настройка Dataverse с помощью средства Package Deployer

После установки необходимых компонентов используйте следующую процедуру, если предпочитаете настроить Dataverse с помощью средства Package Deployer. Сведения о том, как импортировать решения вручную, см. в следующем разделе (не нужно выполнять оба процесса).

1. Установите средства для разработчиков, как описано в разделе [Загрузить средства из NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).

1. На основе своих бизнес-требований выберите пакет `InventoryServiceBase` или `InventoryServiceApplication`.

1. Импорт решений:
    1. Для пакета `InventoryServiceBase`:
        - Разархивируйте `InventoryServiceBase.PackageDeployer.zip`
        - Найдите папку `InventoryServiceBase` и файлы `[Content_Types].xml`, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` и `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`. 
        - Скопируйте каждую из этих папок и файлов в каталог `.\Tools\PackageDeployment`, созданный при установке средств разработчика.
    1. Для пакета `InventoryServiceApplication`:
        - Разархивируйте `InventoryServiceApplication.PackageDeployer.zip`
        - Найдите папку `InventoryServiceApplication` и файлы `[Content_Types].xml`, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` и `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.
        - Скопируйте каждую из этих папок и файлов в каталог `.\Tools\PackageDeployment`, созданный при установке средств разработчика.
    1. Выполните `.\Tools\PackageDeployment\PackageDeployer.exe`. Следуйте инструкциям на экране, чтобы импортировать решения.

1. Назначение ролей безопасности новому пользователю.
    1. Откройте URL-адрес своей среды Dataverse.
    1. Перейдите **Дополнительные параметры \> Система \> Безопасность \> Пользователи** и найдите пользователя с именем **# InventoryVisibility**.
    1. Выберите **Назначить роль**, а затем выберите **Системный администратор**. Если имеется роль с именем **Пользователь Common Data Service**, выберите также и ее.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>Настройка вручную Dataverse путем импортирования решений

После установки необходимых компонентов используйте следующую процедуру, если предпочитаете настроить Dataverse, вручную импортировав решения. Более подробную информацию об использовании средства Package Deployer (не нужно выполнять обе процедуры) см. в предыдущем разделе.

1. Создайте пользователя приложения для контроля запасов в Dataverse:

    1. Откройте URL-адрес своей среды Dataverse.
    1. Перейдите **Дополнительные параметры \> Система \> Безопасность \> Пользователи** и создайте пользователя приложения. Используйте меню вида для изменения вида страницы на **Пользователи приложения**.
    1. Выберите **Создать**. Задайте код приложения как *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (Код объекта будет автоматически загружен после сохранения изменений.) Можно настроить имя. Например, можно изменить его на *Контроль запасов*. Закончив, выберите **Сохранить**.
    1. Выберите **Назначить роль**, а затем выберите **Системный администратор**. Если имеется роль с именем **Пользователь Common Data Service**, выберите ее.

    Дополнительные сведения см. в разделе [Создание пользователя приложения](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Если языком по умолчанию в Dataverse является не **Английский**, выполните следующие действия:

    1. Переход к **Дополнительные параметры \> Администрирование \> Языки**,
    1. Выберите **Английский (LanguageCode=1033)** и нажмите кнопку **применить**.

1. Импортируйте файл `Inventory Visibility Dataverse Solution.zip`, который включает в себя соответствующие записи конфигурации Dataverse и Power Apps:

    1. Перейдите на страницу **Решения**.
    1. Выберите **Импорт**.

1. Импортируйте поток триггеров обновления конфигурации:

    1. Перейдите на страницу Microsoft Flow.
    1. Убедитесь, что подключение с именем *Dataverse (устар.)* существует. (Если оно не существует, создайте его.)
    1. Импортируйте файл формата `Inventory Visibility Configuration Trigger.zip`. После импорта триггер появится в разделе **Мои потоки**.
    1. Инициализируйте четыре следующие переменные на основе информации о среде:

        - Идентификатор клиента Azure
        - Идентификатор клиента приложения Azure
        - Секрет клиента приложения Azure
        - Конечная точка контроля запасов

            Дополнительные сведения об этой переменной см. в разделе [Настройка интеграции контроля запасов](#setup-inventory-visibility-integration) далее в этой теме.

        ![Триггер конфигурации.](media/configuration-trigger.png "Триггер конфигурации")

    1. Выберите **Включить**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Установка надстройки

Чтобы установить надстройку видимости запасов, необходимо сделать следующее:

1. Выполните вход на портал [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. На домашней странице выберите проект, в котором развернута среда.
1. На странице проекта выберите среду, в которой требуется установить надстройку.
1. На странице среды прокрутите вниз до появления раздела **Надстройки среды** в разделе **Интеграция Power Platform**, где можно найти имя среды Dataverse.
1. В разделе **Надстройки сред** выберите **Установить новую надстройку**.

    ![Страница среды в LCS.](media/inventory-visibility-environment.png "Страница среды в LCS")

1. Выберите ссылку **Установить новую надстройку**. Откроется список доступных надстроек.
1. Выберите **Контроль запасов** в списке.
1. Введите значения для следующих полей для вашей среды:

    - **Код приложения AAD (клиента)**
    - **Код арендатора AAD**

    ![Страница настройки надстройки.](media/inventory-visibility-setup.png "Страница настройки надстройки")

1. Примите условия, установив флажок **Условия**.
1. Выберите **Установить**. Статус надстройки будет отображаться как **Установка**. После завершения обновите страницу, чтобы увидеть статус, измененный на **Установлено**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Удаление надстройки

Чтобы удалить надстройку, выберите **Удалить**. При обновлении LCS надстройка для контроля запасов будет удалена. Процесс удаления приведет к удалению регистрации надстройки, а также запуску задания для очистки всех бизнес-данных, хранящихся в службе.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Потребление данных запасов в наличии из Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Развертывание пакета интеграции контроля запасов

Если используется Supply Chain Management версии 10.0.17 или более ранней, обратитесь в службу поддержки контроля запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) для получения пакетного файла. Затем разверните пакет в LCS.

> [!NOTE]
> Если во время развертывания возникает ошибка несоответствия версий, необходимо вручную импортировать проект X++ в среду разработки. Затем создайте развертываемый пакет в среде разработки и разверните его в рабочей среде.
> 
> Этот код включен в Supply Chain Management 10.0.18. Если вы используете эту версию или более позднюю, развертывание не требуется.

Убедитесь, что в среде Supply Chain Management включены следующие функции. (По умолчанию они включены.)

| Описание функции | Версия кода | Переключить класс |
|---|---|---|
| Включение и отключение использования складских аналитик в таблице InventSum | 10.0.11 | InventUseDimOfInventSumToggle |
| Включение и отключение использования складских аналитик в таблице InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Настройка интеграции Видимости запасов

1. В Supply Chain Management откройте рабочую область **[Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** и включите функцию **Интеграция контроля запасов**.
1. Перейдите **Управление запасами \> Настройка \> Параметры интеграции контроля запасов** и введите URL-адрес среды, в которой выполняется контроль запасов.

    Найдите свой регион Azure среды, а затем введите URL-адрес. URL-адрес имеет следующую форму:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Например, если вы находитесь в Европе, у вашей среды будет один из следующих URL-адресов:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    В настоящее время доступны следующие регионы.

    | Регион Azure | Краткое название региона |
    |---|---|
    | Восточная Австралия | eau |
    | Юго-восточная Австралия | seau |
    | Центральная Канада | cca |
    | Восточная Канада | eca |
    | Северная Европа | neu |
    | Западная Европа | weu |
    | Восточная часть США | eus |
    | Западная часть США | wus |

1. Перейдите **Управление запасами \> Периодические операции \> Интеграция контроля запасов** и включите задание. Все события изменения запасов из модуля Supply Chain Management будут разнесены в контроль запасов.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Открытый API-интерфейс надстройки контроля запасов

Открытый интерфейс REST API надстройки контроля запасов представляет несколько определенных конечных точек интеграции. Он поддерживает три основных типа взаимодействий:

- Разноска изменений запасов в наличии в надстройку из внешней системы
- Запрос текущих количеств в наличии из внешней системы
- Автоматическая синхронизация с запасами в наличии в Supply Chain Management

Автоматическая синхронизация не является частью общедоступного API. Вместо этого она обрабатывается в фоновом режиме для сред, в которых включена надстройка контроля запасов.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Аутентификация

Маркер безопасности платформы используется для вызова надстройки контроля запасов. Таким образом, необходимо создать *Маркер Azure Active Directory (Azure AD)* с помощью приложения Azure AD. Затем необходимо использовать маркер Azure AD, чтобы получить *маркер доступа* из службы безопасности.

Получите маркер службы безопасности, выполнив следующие действия:

1. Выполните вход на портал Azure и используйте его, чтобы найти `clientId` и `clientSecret` для вашего приложения Supply Chain Management.
1. Получите токен Azure Active Directory (`aadToken`), отправив HTTP-запрос со следующими свойствами:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Метод** - `GET`
    - **Содержимое основной части (данные формы)**:

        | ключ | значение |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | ресурс | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Вы должны получить токен `aadToken` в ответе, который напоминает следующий пример:

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Сформулируйте запрос JSON, похожий на следующий:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Где:
    - Значение `client_assertion` должно быть токеном `aadToken`, полученным на предыдущем шаге.
    - Значение `context` должно быть идентификатором среды, в которой требуется развернуть надстройку.
    - Установите все остальные значения, как показано в примере.

1. Отправьте запрос HTTP со следующими свойствами:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **Метод** - `POST`
    - **Заголовок HTTP** — включает версию API (ключ равен `Api-Version`, значение равно `1.0`)
    - **Основное содержимое** — включает запрос JSON, созданный на предыдущем шаге.

1. В ответе вы получите `access_token`. Это то, что требуется в качестве маркера носителя для вызова API отображения запасов. Рассмотрим пример:

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Образец запроса

Для справки, вот образец http-запроса, для отправки этого запроса можно использовать любые инструменты или язык кодирования, например ``Postman``.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Настройка интерфейса API для отображения запасов

Перед использованием службы необходимо выполнить конфигурации, описанные в следующих подразделах. Конфигурация может различаться в зависимости от сведений о среде. В основном она включает четыре части:

- [Секционирование](#partitioning)
- [Конфигурации аналитик](#dimension-configurations)
- [Индексация](#indexing)
- [Пользовательское измерение](#custom-measurement)

#### <a name="partitioning"></a>Секционирование

Секционирование может значительно повлиять на производительность API отображения запасов. Рекомендуется определить схему, позволяющую выполнять небольшие группирования данных, сохраняя при этом возможность осмысленных запросов данных.

`organizationId` (`dataAreaId` в Supply Chain Management) всегда будет частью секционирования, и по умолчанию для отображения запасов устанавливается секционирование по аналитикам, таким как *Сайт + Местоположение*. Это означает, что служба должна всегда запрашиваться с этими аналитиками, определенными в фильтрах.

> [!NOTE]
> *Сайт* и *Местоположение* — это две общих аналитики по умолчанию в видимости запасов. В Supply Chain Management эти аналитики называются *Сайт* (`InventSiteId`) и *Склад* (`InventLocationId`)

### <a name="dimension-configurations"></a>Конфигурации аналитик

Видимость запасов представляет список основных аналитик по умолчанию для включения интеграции нескольких источников в систему.

В следующей таблице перечислены складские аналитики, которые будут именами аналитик по умолчанию в видимости запасов.

| Тип аналитики | Имя аналитики |
|---|---|
| Продукт | `ColorId` |
| Продукт | `SizeId` |
| Продукт | `StyleId` |
| Продукт | `ConfigId` |
| Отслеживание | `BatchId` |
| Отслеживание | `SerialId` |
| Расположение | `LocationId` |
| Расположение | `SiteId` |
| Статус запасов | `StatusId` |
| Зависит от склада | `WMSLocationId` |
| Зависит от склада | `WMSPalletId` |
| Зависит от склада | `LicensePlateId` |

> [!NOTE]
> Тип аналитики, приведенный в предыдущей таблице, используется только для справки. Нет необходимости определять тип аналитики в видимости запасов.

Если имеется настраиваемая аналитика, которая должна перетекать в значение по умолчанию при потреблении видимостью запасов, можно настроить имя **настраиваемой аналитики** в видимости запасов.

Внешние системы получают доступ к видимости запасов через интерфейсы API RESTful, которые позволяют запрашивать информацию о наличии по данным наборам аналитик. Для интеграции видимость запасов позволяет настроить *источник данных внешнего канала* и исходную аналитику на *целевые аналитики* в видимости запасов.

Целевые аналитики должны быть одной из следующих:

- Аналитики по умолчанию в видимости запасов
- Настраиваемые аналитики

Целью настройки аналитики является стандартизация интеграции нескольких систем для запроса по аналитикам и события разноски с аналитиками.

#### <a name="indexing"></a>Индексация

В большинстве случаев запрос запасов в наличии будет не только на самом высоком уровне "итога", но может потребоваться просмотреть результаты агрегирования на основе складских аналитик.

Видимость запасов обеспечивает гибкость, позволяя настраивать индексы, которые основаны на аналитике или комбинации аналитик.

> [!NOTE]
> В настоящее время для индексов можно настроить не более пяти. Необходимо тщательно продумать, какая аналитика или комбинация аналитик будет использоваться, перед реализацией, чтобы обеспечить, что она будут удовлетворять вашим деловым потребностям. Например, если требуется запросить продукты следующим образом:

- Запрос агрегированного наличия продуктов по аналитикам *Цвет* и *Размер*.
- В некоторых случаях требуется только выполнить запрос по продукту в целом.

Можно определить два индекса следующим образом:

- `["ColorId", "SizeId"]`
- `[]`

Пустая скобка будет агрегирована на основе идентификатора продукта в секции.

Индексация определяет способ группировки результатов в зависимости от настройки запроса `groupBy`. В этом случае, если никакие значения `groupBy` не определены, будут выведены итоги по `productid`. В противном случае, если определить `groupBy` как `groupBy=ColorId&groupBy=SizeId`, будет возвращено несколько строк, в зависимости от различных комбинаций цвета и размера в системе.

Критерии запроса можно разместить в теле запроса.

Вот пример запроса для комбинации цвета и размера продукта.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

Для поля `filters` в настоящее время только `ProductId` поддерживает несколько значений. Если `ProductId` является пустым массивом, будут запрашиваться все продукты.

#### <a name="custom-measurement"></a>Пользовательское измерение

Количества измерений по умолчанию связаны с Supply Chain Management. Однако, возможно, потребуется количество, состоящее из комбинации измерений по умолчанию. Чтобы сделать это, можно задать конфигурацию настраиваемых количеств, которая будет добавлена к выходным данным запросов запасов в наличии.

Функциональность просто позволяют определить набор мер, которые будут добавлены, и/или набор мер, которые будут вычтены, чтобы сформировать настраиваемое измерение.

Например, со следующим условием запроса вы настроите пользовательское количество измерения как `MyCustomAvailableforReservation` для потребления системой потребления.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Система потребления | Рассчитанные меры | Иcточник данных | Модификатор | Тип расчета модификатора |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Сложение |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Сложение |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Вычитание |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Сложение |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Вычитание |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Сложение |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Сложение |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Вычитание |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Вычитание |

При этом запрос настраиваемого количества измерения возвратит следующий результат.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Выходные данные `MyCustomAvailableforReservation` основаны на параметрах расчета в настраиваемых измерениях следующим образом:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Разноска изменений запасов в наличии

Точный URL-адрес, на который будет разнесено событие, будет зависеть от географического региона. Он будет иметь вид:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

После аутентификации этот URL-адрес может использоваться вместе с методом HTTP `POST` для отправки в службу событий изменения запасов в наличии.

Специальный заголовок используется для связи с службами Dynamics 365 с помощью запросов HTTP, в которых указывается идентификатор среды экземпляра Supply Chain Management, с которым связаны данные. Пример:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Пример 1 разноски запроса изменений запасов в наличии

В этом примере показан сценарий, в котором будет настроена конфигурация аналитики в Power Apps.

Следующий запрос используется для настройки сопоставления измерений в Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах. Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Пример 2 разноски запроса изменений запасов в наличии

В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики. Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` имеет значение NULL, является пустым или пробелом.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>Свойства полей документов JSON

Поля из примеров запросов JSON, приведенных выше, имеют свойства, перечисленные в следующей таблице.

| FieldID | описание |
|---|---|
| `id` | Уникальный код для конкретного события изменения. Этот код используется, чтобы гарантировать, что при возникновении ошибки при обмене данными с службой во время разноски повторная отправка события не приведет к тому, что в системе дважды будет учитываться одно и то же событие. |
| `organizationId` | Идентификатор организации, связанной с событием. Это сопоставляется с организациями Supply Chain Management или идентификаторами областей данных. |
| `productId` | Идентификатор рассматриваемого продукта. |
| `quantity` | Количество, для которого должны быть изменены запасы в наличии. Если, например, 10 новых бубликов были добавлены на полку, это значение было бы равно 10. Если 3 бублика были удалены с полки или проданы, это значение было бы равно -3. |
| `dimensionDataSource` | Источник данных для аналитик, используемых в разноске события изменения и запроса. Если указан источник данных, можно использовать настраиваемые аналитики из указанного источника данных. С помощью конфигурации аналитик видимость запасов может сопоставлять пользовательские аналитики с общими аналитиками по умолчанию. Если параметр `dimensionDataSource` не указан, в запросах могут использоваться только общие аналитики по умолчанию.   |
| `dimensions` | Динамический набор пар "ключ-значение". Это будет сопоставляться с некоторыми аналитиками в Supply Chain Management, но можно также добавить настраиваемые аналитики(например, *Источник*), которые могут обозначать, когда событие поступает из Supply Chain Management или из внешней системы. |

### <a name="querying-current-on-hand"></a>Запрос текущих запасов в наличии

Конечная точка для запроса текущих запасов в наличии будет иметь похожий URL-адрес:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Запрос будет выполняться с использованием метода HTTP `POST`.

#### <a name="current-on-hand-query-example-1"></a>Пример 1 запроса текущих запасов в наличии

В этом примере показан сценарий, в котором вы уже выполнили настройку конфигурации аналитики в Power Apps.

Следующий запрос используется для настройки сопоставления измерений в Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах. Система будет автоматически преобразовывать пользовательские измерения в базовые измерения. Можно указать `DimensionDataSource` в поле `filters` и указать настраиваемые аналитики в обоих полях `filters` и `groupByValues`. Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Пример 2 запроса текущих запасов в наличии

В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики. Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` в разделе `filters` имеет значение NULL, является пустым или пробелом.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Пример возвращаемого результата

Запросы, показанные в предыдущих примерах, могут вернуть результат, подобный этому.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Обратите внимание, что поля количества структурированы как словарь мер и связанные с ними значений.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
