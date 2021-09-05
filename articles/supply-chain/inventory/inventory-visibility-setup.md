---
title: Настройка видимости запасов
description: В этой теме описывается, как установить надстройку отображения запасов для Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343592"
---
# <a name="set-up-inventory-visibility"></a>Настройка видимости запасов

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

В этой теме описывается, как установить надстройку отображения запасов для Microsoft Dynamics 365 Supply Chain Management.

Необходимо использовать Microsoft Dynamics Lifecycle Services (LCS), чтобы установить надстройку отображения запасов. LCS — это портал совместной работы, который предоставляет среду и набор регулярно обновленных служб, которые помогут управлять жизненным циклом приложений Finance and Operations.

Дополнительные сведения см. в разделе [Ресурсы Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Необходимые условия для видимости запасов

Перед установкой надстройки видимости запасов необходимо сделать следующее:

- Получите проект внедрения LCS с по крайней мере одной развернутой средой.
- Убедитесь, что необходимые условия для настройки надстроек завершены. Сведения об этих предварительных требованиях см. в разделе [Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Для контроля запасов не требуется связывание с двойной записью.
- Для получения следующих необходимых файлов обратитесь к специалистам по контролю запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (если версия Supply Chain Management, которую вы используете, более ранняя, чем версия 10.0.18)

> [!NOTE]
> Страны и регионы, которые в настоящее время поддерживаются: Канада (CCA, ECA), США (WUS, EUS), Европейский Союз (NEU, WEU), Соединенное Королевство (SUK, WUK) и Австралия (EAU, SEAU).

При возникновении каких-либо вопросов о необходимых условиях свяжитесь с группой разработчиков продукта для отображения запасов.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Настройка Dataverse

Чтобы настроить Dataverse, чтобы его можно было использовать с видимостью запасов, воспользуйтесь Package Deployer для развертывания пакета отображения запасов. Следующие подразделы описывают выполнение каждой задачи.

> [!NOTE]
> В настоящее время поддерживаются только среды Dataverse, созданные с использованием LCS. Если среда Dataverse была создана каким-либо другим способом (например, с помощью центра администрирования Power Apps) и если она связана с вашей средой Supply Chain Management, необходимо сначала связаться с группой разработчиков продуктов видимости запасов, чтобы устранить проблему с сопоставлением. Затем можно установить видимость запасов.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Миграция из старой версии решения Dataverse

Если вы установили старую версию решения видимости запасов Dataverse, воспользуйтесь приведенными ниже инструкциями, чтобы обновить версию. Имеется две возможности:

- **Случай 1:** Если вы вручную настраиваете Dataverse при импорте решения `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip`, выполните следующие действия:

    1. Загрузите следующие три файла:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Импортируйте вручную `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` и `InventoryServiceBase_managed.cab` в Dataverse, выполнив следующие действия:

        1. Откройте URL-адрес своей среды Dataverse.
        1. Откройте на страницу **Решения**.
        1. Выберите **Импорт**.

    1. Используйте Package Deployer для развертывания пакета `InventoryServiceApplication.PackageDeployer.zip`. Инструкции см. в разделе [Использование Package Deployer для развертывания пакета](#deploy-package) далее в этой теме.

- **Случай 2:** При настройке Dataverse с помощью Package Deployer перед установкой более раннего пакета `.*PackageDeployer.zip`, загрузите `InventoryServiceApplication.PackageDeployer.zip` и выполните обновление. Инструкции см. в разделе [Использование Package Deployer для развертывания пакета](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Используйте Package Deployer для развертывания пакета

1. Установите средства для разработчиков, как описано в разделе [Загрузить средства из NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Чтобы разблокировать файл `InventoryServiceApplication.PackageDeployer.zip`, загруженный из группы Teams, необходимо выполнить следующие действия:

    1. Выберите и удерживайте (или щелкните правой кнопкой мыши) файл, затем выберите **Свойства**.
    1. В диалоговом окне **Свойства** на вкладке **Общие** найдите раздел **Безопасность**, выберите **Разблокировать** и примените изменение. Если раздел **Безопасность** отсутствует на вкладке **Общие**, файл не заблокирован. В этом случае перейдите к следующему шагу.

    ![Разблокирование загруженного файла](media/unblock-file.png "Разблокирование загруженного файла")

1. Разархивируйте `InventoryServiceApplication.PackageDeployer.zip` для получения следующих элементов:

    - Папка `InventoryServiceApplication`
    - Файл `[Content_Types].xml`
    - Файл `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`

1. Скопируйте все эти элементы в каталог `.\Tools\PackageDeployment`. (Эта папка была создана при установке средств разработчика.)
1. Выполните `.\Tools\PackageDeployment\PackageDeployer.exe`, следуйте инструкциям на экране, чтобы импортировать решения.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Установка надстройки видимости запасов

Перед установкой надстройки зарегистрируйте приложение и добавьте секрет клиента в Azure Active Directory (Azure AD) в своей подписке Azure. Инструкции см. в разделе [Регистрация приложения](/azure/active-directory/develop/quickstart-register-app) и [Добавление секрета клиента](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Обязательно запишите значения **Идентификатор приложения (клиента)**, **Секрет клиента** и **Идентификатора арендатора**, так как они понадобятся позже.

После регистрации приложения и добавления к нему секрета клиента в Azure AD выполните следующие действия, чтобы установить надстройку "Отображение запасов".

1. Войдите в [LCS](https://lcs.dynamics.com/Logon/Index).
1. На домашней странице выберите проект, в котором развернута среда.
1. На странице проекта выберите среду, в которой требуется установить надстройку.
1. На странице среды прокрутите вниз, чтобы увидеть раздел **Надстройки среды** в разделе **Интеграция Power Platform**. Там можно найти имя среды Dataverse.
1. В разделе **Надстройки сред** выберите **Установить новую надстройку**.

    ![Страница среды в LCS](media/inventory-visibility-environment.png "Страница среды в LCS")

1. Выберите ссылку **Установить новую надстройку**. Откроется список доступных надстроек.
1. Выберите **Контроль запасов** в списке.
1. Задайте следующие поля для своей среды:

    - **Идентификатор приложения (клиента) AAD** — введите идентификатор приложения Azure AD, который был создан ранее и который вы записали.
    - **Идентификатор арендатора AAD** — введите идентификатор арендатора, который вы записали ранее.

    ![Страница настройки надстройки](media/inventory-visibility-setup.png "Страница настройки надстройки")

1. Примите условия, установив флажок **Условия**.
1. Выберите **Установить**. Статус надстройки будет отображаться как **Установка**. После завершения установки обновите страницу. Статус должен изменяться на **Установлено**.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Удаление надстройки видимости запасов

Чтобы удалить надстройку "Отображение запасов", выберите **Удалить** на странице LCS. Процесс удаления отключает надстройку "Отображение запасов", отменяет регистрацию надстройки в LCS и удаляет все временные данные, которые хранятся в кэше данных надстройки "Отображение запасов". Однако основные данные запасов, которые хранятся в подписке Dataverse, не удаляются.

Чтобы удалить данные инвентаризации, которые хранятся в подписке Dataverse, откройте [Power Apps](https://make.powerapps.com), выберите **Среда** на панели переходов и выберите среду Dataverse, связанную с вашей средой LCS. Затем перейдите к **Решения** и удалите следующие пять решений:

- Привязка решения для приложения отображения запасов в решениях Dynamics 365
- Решение приложений видимости запасов Dynamics 365 FNO SCM
- Конфигурация службы запасов
- Изолированная версия "Видимость запасов"
- Базовое решение видимости запасов Dynamics 365 FNO SCM

После удаления этих решений данные, хранящиеся в таблицах, также будут удалены.

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Настройка Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Развертывание пакета интеграции контроля запасов

Если используется Supply Chain Management версии 10.0.17 или более ранней, обратитесь в службу поддержки контроля запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) для получения пакетного файла. Затем разверните пакет в LCS.

> [!NOTE]
> Если во время развертывания возникает ошибка несоответствия версий, необходимо вручную импортировать проект X++ в среду разработки. Затем создайте развертываемый пакет в среде разработки и разверните его в рабочей среде.
>
> Этот код включен в Supply Chain Management 10.0.18. Если вы используете эту версию или более позднюю, развертывание не требуется.

Убедитесь, что в среде Supply Chain Management включены следующие функции. (По умолчанию они включены.)

| Описание функции | Версия кода | Переключить класс |
|---|---|---|
| Включение и отключение использования складских аналитик в таблице InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Включение и отключение использования складских аналитик в таблице InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Настройка интеграции Видимости запасов

1. В Supply Chain Management откройте рабочую область **[Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** и включите функцию *Интеграция контроля запасов*.
1. Перейдите **Управление запасами \> Настройка \> Параметры интеграции контроля запасов** и введите URL-адрес среды, в которой выполняется контроль запасов. Дополнительные сведения см. в [Поиск конечной точки службы](inventory-visibility-power-platform.md#get-service-endpoint).
1. Перейдите **Управление запасами \> Периодические операции \> Интеграция контроля запасов** и включите задание. Все события изменения запасов из модуля Supply Chain Management будут разнесены в контроль запасов.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
