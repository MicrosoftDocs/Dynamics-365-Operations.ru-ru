---
title: Начало работы с администрированием службы электронного выставления накладных
description: В этой теме объясняется, как начать работать с модулем электронного выставления накладных.
author: gionoder
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7c4d69edd4a8f7c7acc2ac1bc22c1ba6eaba25ae
ms.sourcegitcommit: 90a289962598394ad98209026013689322854b7b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "6092414"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Начало работы с администрированием службы электронного выставления накладных

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Необходимые условия

Перед выполнением процедур из данной темы необходимо выполнить следующие предварительные требования:

- Необходимо иметь доступ к учетной записи Microsoft Dynamics Lifecycle Services (LCS).
- Необходим проект LCS, включающий версию 10.0.17 или более позднюю версию Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management. Кроме того, эти приложения должны быть развернуты в одном из следующих географических регионов Azure:

    - США
    - Европа
    - Великобритания
    - Азия

- Необходимо иметь доступ к учетной записи службы Dynamics 365 Regulatory Configuration Services (RCS).
- Необходимо активировать функцию глобализации для вашей учетной записи RCS в управлении функциями. Дополнительные сведения см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md).
- Необходимо создать Key Vault и учетную запись хранилища в Azure. Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Установка надстройки для микрослужб в Lifecycle Services

1. Войдите в свою учетную запись LCS и на панели мониторинга проектов LCS выберите проект LCS.
2. В этом проекте на панели мониторинга среды выберите проект развертывания LCS. Выбранный проект должен быть запущен.
3. На вкладке **Интеграция Power Platform** в группе полей **Надстройки среды** выберите **Установить новую надстройку**.
4. Выберите **Электронное выставление накладных**.
5. В поле **Код приложения AAD** введите **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Это фиксированное значение.
6. В поле **Код клиента AAD** введите код клиента вашей учетной записи подписки Azure.
7. Ознакомьтесь с условиями и установите флажок.
8. Выберите **Установить**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Настройка параметров для интеграции RCS с модулем электронного выставления накладных

1. Войдите в учетную запись RCS.
2. В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Параметры электронной отчетности**.
3. На вкладке **Служба электронного выставления накладных** в поле **URI конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.

    | География центра обработки данных Azure | Универсальный код ресурса (URI) конечной точки службы                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | США              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Европа                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Великобритания             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Азия                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Убедитесь, что в поле **Код приложения** установлено значение **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Это значение является фиксированным значением.
5. В поле **Код среды LCS** введите идентификатор вашей среды LCS.
6. Выберите **Сохранить** и закройте страницу.

## <a name="create-key-vault-references"></a>Создание ссылок Key Vault

1. Войдите в учетную запись RCS.
2. В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Электронное выставление накладных**.
3. На странице **Настройки среды** на панели действий выберите **Среда службы**, затем выберите **Параметры Key Vault**.
4. Выберите **Создать**, чтобы создать ссылку Key Vault.
5. В поле **Имя** введите имя ссылки Key Vault. В поле **Описание** введите описание.
6. В поле **URI Key Vault** вставьте секрет хранилища ключей из Azure Key Vault. Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
7. Нажмите **Сохранить**.

## <a name="create-storage-account-secret"></a>Создание секрета учетной записи хранения

1. На странице **Настройки среды** на панели действий выберите **Среда службы** > **Параметры Key Vault**.
2. Выберите пункт **Ссылка Key Vault** и в разделе **Сертификаты** выберите **Добавить**.
3. В поле **Имя** введите имя секрета учетной записи хранения. Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
4. В поле **Описание** введите описание.
5. В поле **Тип** выберите **Секрет**.
6. Выберите **Сохранить** и закройте страницу.

## <a name="create-a-digital-certificate-secret"></a>Создайте секрет для цифрового сертификата

1. На странице **Настройки среды** на панели действий выберите **Среда службы**, затем выберите **Параметры Key Vault**.
2. Выберите пункт **Ссылка Key Vault**, затем в разделе **Сертификаты** выберите **Добавить**.
3. В поле **Имя** введите имя секрета цифрового сертификата. Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
4. В поле **Описание** введите описание.
5. В поле **Тип** выберите **Сертификат**.
6. Выберите **Сохранить** и закройте страницу.

## <a name="create-a-service-environment"></a>Создание среды службы

1. Войдите в учетную запись RCS.
2. В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Электронное выставление накладных**.
3. На странице **Настройки среды** на панели действий выберите **Среда службы**.
4. Выберите **Создать** для создания новой среды службы.
5. В поле **Имя** введите имя среды электронного выставления накладных. В поле **Описание** введите описание.
6. В поле **Секрет маркера SAS хранилища** выберите имя секрета учетной записи хранения, который должен использоваться для проверки подлинности доступа к учетной записи хранения.
7. В разделе **Пользователи** выберите **Добавить**, чтобы добавить пользователя, которому разрешено отправлять электронные накладные через среду, а также подключиться к учетной записи хранения.
8. В поле **Код пользователя** введите псевдоним пользователя. В поле **Электронная почта** введите адрес электронной почты пользователя.
9. Нажмите **Сохранить**.
10. Если в накладных для конкретной страны/региона требуется цепочка сертификатов для применения цифровых подписей, на панели действий выберите **Параметры Key Vault**, затем выберите **Цепочка сертификатов** и выполните следующие действия:
    1. Для создания цепочки сертификатов выберите **Создать**.
    2. В поле **Имя** введите имя цепочки сертификатов. В поле **Описание** введите описание.
    3. В разделе **Сертификаты** выберите **Добавить**, чтобы добавить сертификат в цепочку.
    4. Используйте кнопки **Вверх** или **Вниз**, чтобы изменить положение сертификата в цепочке.
    5. Выберите **Сохранить** и закройте страницу.
    6. Закройте страницу.
11. На странице **Среда службы** в области действий выберите **Опубликовать** для публикации среды в облаке. Значение в поле **Статус** изменяется на **Опубликовано**.

## <a name="create-a-connected-application"></a>Создание подключенного приложения

1. На странице **Настройки среды** на панели действий выберите **Подключенные приложения**.
2. Выберите **Создать** для создания подключенного приложения.
3. В поле **Имя** введите имя подключаемого приложения.
4. В поле **Приложение** введите URL-адрес среды Finance и Supply Chain Management для подключения.
4. В поле **Клиент** укажите клиент среды Finance и Supply Chain Management.
5. Нажмите **Сохранить**.
6. В области действий выберите **Проверить подключение** для проверки подключения к среде. Затем закройте страницу.

## <a name="link-connected-applications-to-environments"></a>Связывание подключенных приложений со средами

1. На странице **Настройки среды** выберите **Создать**, чтобы назначить подключенное приложение среде.
2. В поле **Подключенное приложение** выберите подключенное приложение.
3. В поле **Среда службы** выберите среду службы.
4. Выберите **Сохранить** и закройте страницу.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Настройка интеграции электронного выставления накладных в Finance и Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Включение функции интеграции электронного выставления накладных

1. Войдите в свой экземпляр Finance или Supply Chain Management.
2. В рабочей области **Управление функциями** выполните поиск функции **Интеграция электронного выставления накладных**. Если эта функция не отображается на странице, выберите **Проверить наличие обновлений**.
3. Выберите эту функцию, затем выберите **Включить сейчас**.

### <a name="set-up-the-service-endpoint-url"></a>Настройка URL-адреса конечной точки службы

1. Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.
2. На вкладке **Служба отправки** в поле **URL конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.

    | География центра обработки данных Azure | Универсальный код ресурса (URI) конечной точки службы                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | США              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Европа                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Великобритания             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Азия                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. В поле **Среда** введите имя среды службы, опубликованной в модуле электронного выставления накладных.
4. Выберите **Сохранить** и закройте страницу.

### <a name="enable-flighting-keys"></a>Включение ключей фокус-тестирования

Включите ключи фокус-тестирования для Microsoft Dynamics 365 Finance или Microsoft Dynamics 365 Supply Chain Management версии 10.0.17 или более ранней версии. 
1. Выполните следующую команду SQL:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Выполните команду IISreset для всех серверов AOS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
