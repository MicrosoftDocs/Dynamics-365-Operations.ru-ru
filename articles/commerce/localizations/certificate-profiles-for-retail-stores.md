---
title: Определенные пользователем профили сертификатов для розничных магазинов
description: В этой статье представлен обзор профилей сертификатов, доступных в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558446"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Определенные пользователем профили сертификатов для розничных магазинов

[!include [banner](../includes/banner.md)]

В этой статье представлен обзор профилей сертификатов, доступных в Microsoft Dynamics 365 Commerce. Эта функция расширяет функцию [Управление секретами для розничных каналов](../dev-itpro/manage-secrets.md) путем добавления поддержки локальных сертификатов.

Когда POS-терминал работает в автономном режиме, он не может получить доступ к сертификатам, хранящимся в этом хранилище Microsoft Azure Key Vault. Вместо этого следует использовать локальный сертификат. Поддерживаются следующие возможности:

- Использование локальных сертификатов в сценариях резервного хранилища Key Vault
- Использование локальных сертификатов без хранилища Key Vault (например, в локальной установке)
- Постепенное обновление сертификатов, где некоторые магазины и терминалы используют новую версию сертификата, но другие магазины и терминалы продолжают использовать предыдущую версию

Функция профилей сертификатов позволяет указать сертификат по умолчанию и задать порядок поиска сертификатов в одном и том же профиле сертификатов. Эта функция также обеспечивает аналогичный подход к настройке для локальных сертификатов и сертификатов из хранилища ключей. Для сертификатов можно добавлять параметры, специфические для компании, но уникальный межфирменный идентификатор для каждого сертификата можно использовать в каналах Commerce.

### <a name="scenarios"></a>Сценарии

Функциональность профилей сертификатов поддерживает следующие сценарии в каналах Commerce:

- Использование локального сертификата в сценариях резервного хранилища Key Vault. Ниже приведены несколько примеров таких резервных сценариев:

    - Хранилище ключей недоступно.
    - Сертификат не найден в хранилище ключей.
    - POS-терминал работает в автономном режиме.

- Использование локальных сертификатов, но без хранения их в хранилище Key Vault (например, в локальной установке).
- Выполнение постепенного обновления сертификатов, когда новая версия сертификата используется только в магазинах или на терминалах, в которых уже доступна новая версия.
- Использование одного и того же сертификата в нескольких компаниях.

## <a name="set-up-certificate-profiles"></a>Настройка профилей сертификатов

В следующей процедуре описан порядок настройки профилей сертификатов.

### <a name="set-up-key-vault"></a>Настройка Key Vault

Необходимо выполнить следующие действия, прежде чем можно будет использовать цифровой сертификат, хранящийся в хранилище ключей Key Vault.

1. Создайте учетную запись хранения Key Vault. Рекомендуется разворачивать учетную запись хранилища в той же географической области, что и Commerce Scale Unit.
1. Отправьте цифровой сертификат в учетную запись хранения Key Vault.
1. Авторизуйте приложение Application Object Server (AOS) для чтения секретов из учетной записи хранилища ключей Key Vault.

Дополнительные сведения о работе с хранилищем ключей Key Vault см. в разделе [Приступая к работе с Azure Key Vault](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Настройка системных параметров

Перед настройкой профилей сертификатов в каналах Commerce необходимо разрешить Commerce использовать оба сертификата, которые хранятся в профилях хранилища ключей Key Vault и профилях сертификатов.

Для настройки параметров системы в Commerce headquarters выполните следующие действия.

1. На странице **Системные параметры** установите в параметре **Использовать расширенное хранилище сертификатов** значение **Да**.
1. В рабочей области **Управление функциями** включите функцию **Определяемые пользователем профили сертификатов для розничных магазинов**.

### <a name="set-up-key-vault-parameters"></a>Настройка параметров Key Vault

На странице **Параметры Key Vault** необходимо указать следующие параметры для доступа к хранилищу ключей Key Vault:

- **Имя** и **Описание** — имя и описание учетной записи хранилища ключей Key Vault.
- **URL-адрес Key Vault** — URL-адрес учетной записи хранилища ключей Key Vault.
- **Клиент Key Vault** — код интерактивного клиента приложения Azure Active Directory (Azure AD), связанного с учетной записью хранилища ключей Key Vault для целей проверки подлинности. Этот клиент должен иметь доступ для чтения секретов из учетной записи хранилища.
- **Секретный ключ хранилища ключей** — секретный ключ, который связан с приложением Azure AD, используемым для проверки подлинности в учетной записи хранилища ключей Key Vault.
- **Имя**, **Описание** и **Секретная ссылка** — имя, описание и секретная ссылка сертификата.

Дополнительные сведения см. в разделе [Настройка клиента Azure Key Vault](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Настройка профиля сертификата

Чтобы настроить профиль сертификата в Commerce Headquarters, выполните следующие шаги.

1. Перейдите в раздел **Администрирование системы \> Настройка \> Профили сертификатов**.
1. На панели операций выберите **Создать** для создания записи.
1. Введите значения в поля **Профиль сертификата**, **Имя** и **Описание**.

    > [!NOTE]
    > Профиль сертификата является уникальным идентификатором сертификата во всех компаниях и компонентах Commerce.

1. На экспресс-вкладке **Юридические лица** выберите **Добавить**, чтобы добавить строку.
1. В разделе **Юридические лица** выберите юридическое лицо (компанию), для которого должен использоваться текущий профиль сертификатов.

    Если профиль сертификатов должен использоваться для нескольких юридических лиц, повторите шаги 4 и 5, чтобы добавить строку для каждого дополнительного юридического лица.

1. Выберите **Параметры**, чтобы открыть страницу **Параметры профиля сертификатов**, на которой можно ввести параметры профиля сертификатов для конкретного компании. Укажите, какие сертификаты могут использоваться при вызове текущего профиля сертификатов в каналах Commerce. Добавьте столько сертификатов, сколько требуется, и задайте для них приоритеты. Если сертификат с более высоким приоритетом недоступен, будет использован следующий сертификат на основе приоритета. Дополнительные сведения см. в разделе [Рабочий процесс: поиск сертификатов в Commerce Runtime](#workflow-searching-certificates-in-the-commerce-runtime).

    > [!NOTE]
    > Поле **Приоритет** устанавливается автоматически. Значение **1** соответствует наивысшему приоритету. При добавлении новой строки на странице **Параметры профиля сертификата** для ее приоритета устанавливается число, которое на единицу больше приоритета предыдущей строки. Чтобы изменить приоритет определенной строки, выберите строку, затем выберите либо **Переместить вверх**, чтобы увеличить приоритет, либо **Переместить вниз**, чтобы уменьшить приоритет.

1. При добавлении новой строки на страницу **Параметры профиля сертификатов** задайте следующие поля:

    - **Тип местоположения** — выберите местоположение, в котором хранится сертификат. У этого поля есть два возможных значения: **Локальный сертификат** и **Хранилище ключей**.
    - **Сертификат хранилища ключей** — это поле является обязательным, если в поле **Тип местоположения** указано значение **Хранилище ключей**. Используйте его для указания секрета сертификата хранилища ключей.
    - **Имя хранилища** — это поле является необязательным и доступно только в том случае, если в поле **Тип местоположения** задано значение **Локальный сертификат**. Используйте его для указания имени хранилища по умолчанию, которое должно использоваться для поиска локальных сертификатов.
    - **Местоположение хранилища** — это поле является необязательным и доступно только в том случае, если в поле **Тип местоположения** задано значение **Локальный сертификат**. Используйте его для указания местоположения хранилища по умолчанию, которое должно использоваться для поиска локальных сертификатов.

        > [!NOTE]
        > Для упрощения процесса поиска локальных сертификатов в Commerce Runtime добавлены имя хранилища и местоположение хранилища по умолчанию. X509StoreProvider содержит список папок, в которых хранятся сертификаты. Если не указано имя хранилища по умолчанию и местоположение хранилища по умолчанию, X509StoreProvider пытается найти сертификат в других папках в своем списке. Дополнительные сведения о доступных значениях для имени магазина и местоположения магазина см. в разделах [Перечисление StoreName](/dotnet/api/system.security.cryptography.x509certificates.storename) и [Перечисление StoreLocation](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Отпечаток** — это поле является обязательным и доступно только в том случае, если в поле **Тип местоположения** задано значение **Локальный сертификат**. Используйте его для указания отпечатка сертификата.

        > [!IMPORTANT]
        > Необходимо убедиться, что пользователь, выполняющий приложение, которое должно использовать локальный сертификат (например, Modern POS в автономном режиме), имеет по крайней мере доступ только для чтения к закрытому ключу сертификата.

    - **Комментарии** — это поле является необязательным и позволяет пользователям вводить примечания.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Рабочий процесс: поиск сертификатов в Commerce Runtime

Ниже приводится основной рабочий процесс, используемый для поиска сертификата при вызове профиля сертификата в среде Commerce Runtime.

1. Система определяет, имеет ли профиль сертификата специфические для компании параметры для текущего юридического лица.
1. Система пытается найти сертификат, используя значения на странице **Параметры профиля сертификатов** для строки, в поле **Приоритет** которого указано значение **1**.

    - Если для поля **Тип местоположения** задано значение **Key Vault**, значение в поле **Секрет сертификата хранилища ключей** используется для поиска сертификата на странице **Параметры хранилища ключей**. Затем выполняется поиск сертификата в хранилище ключей.
    - Если в поле **Тип местоположения** задано значение **Локальный сертификат**, X509StoreProvider сначала выполняет поиск сертификата, используя имя хранилища и местоположение хранилища по умолчанию, если эти параметры указаны. Затем он выполняет поиск во всех других папках в своем списке папок.

1. Если сертификат не найден, процесс повторяется для строки, в поле **Приоритет** которого установлено значение **2**, и т. д.

> [!NOTE]
> Если профиль сертификата не имеет параметров для текущего юридического лица или если поиск сертификата завершился неудачно для всех строк на странице **Параметры профиля сертификатов**, сертификат не найден.

### <a name="caching-the-results-of-certificate-searches"></a>Кэширование результатов поиска сертификатов

Результаты поиска сертификатов кэшируются. По умолчанию для кэша используется срок действия один час. Однако это время можно настроить и задать максимальное значение в 24 часа.

## <a name="gradual-update"></a>Постепенное обновление

Если новая версия сертификата введена, но ее невозможно одновременно обновить во всех магазинах, функция профилей сертификатов позволяет постепенно обновлять сертификат.

1. Найдите профиль сертификатов и строку, которую необходимо обновить, затем выберите **Параметры**.
1. Добавьте строку и укажите параметры, которые относятся к последней версии сертификата.
1. Увеличьте значение **Приоритет** для новой строки. Используйте кнопку **Переместить вверх**, чтобы переместить строку так, чтобы она была над строкой предыдущей версии того же сертификата.
> [!NOTE]
> В среде Commerce Runtime новая версия сертификата будет называться первой. Если сертификат еще не был обновлен в конкретном магазине или на конкретном терминале, будет вызвана предыдущая версия.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
