---
title: Обновление модели субъекта и глобальной адресной книги
description: В этом разделе описывается обновление данных с двойной записью для стороны и модели глобальной адресной книги.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 673c3a68e2eccdabdfc2df281389537297ec3524bee5e744e910c50d38b8d298
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720696"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Обновление модели субъекта и глобальной адресной книги

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Шаблон фабрики данных Microsoft Azure](https://aka.ms/dual-write-gab-adf) помогает обновлять существующие данные таблиц **Учетная запись**, **Контактное лицо** и **Поставщик** с двойной записью для стороны и модели глобальной адресной книги. Шаблон сопоставляет данные обоих приложений Finance and Operations и приложений взаимодействия с клиентами. В конце процесса, поля **Сторона** и **Контактное лицо** для записей **Сторона** будут созданы и связаны с записями **Учетная запись**, **Контактное лицо** и **Поставщик** в приложениях взаимодействия с клиентами. Файл CSV (`FONewParty.csv`) создается для создания новых записей **Сторона** в приложении Finance and Operations. В этом разделе представлены инструкции о том, как использовать шаблон фабрики данных и обновлять данные.

При отсутствии каких-либо настроек можно использовать шаблон как есть. Если имеются настройки для **Учетная запись**, **Контактное лицо** и **Поставщик**, необходимо изменить шаблон с помощью следующих инструкций.

> [!NOTE]
> Шаблон обновляет только данные **Сторона**. В будущих выпусках будут включены почтовый и электронный адрес.

## <a name="prerequisites"></a>Необходимые условия

Для обновления стороны и модели глобальной адресной книги необходимо выполнить следующие условия:

+ [Подписка Azure](https://portal.azure.com/)
+ [Доступ к шаблону](https://aka.ms/dual-write-gab-adf)
+ Вы должны быть существующим клиентом с двойной записью.

## <a name="prepare-for-the-upgrade"></a>Подготовка к обновлению
Для подготовки к обновлению необходимо выполнить следующие действия:

+ **Полностью синхронизировано**: обе среды полностью синхронизированы для параметров **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик**.
+ **Ключи интеграции**: таблицы **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик** в приложениях взаимодействия с клиентами используют ключи интеграции, которые поставлялись в комплекте. При настройке ключей интеграции необходимо настроить шаблон.
+ **Номер стороны**: все записи **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик**, для которых будет выполнено обновление, имеют номер **Стороны**. Записи без номера **стороны** будут пропущены. Если необходимо обновить эти записи, добавьте к ним номер **Стороны** перед началом процесса обновления.
+ **Отключение системы**: в ходе процесса обновления вам придется в автономном режиме использовать как среду Finance and Operations, так и среду взаимодействия с клиентами.
+ **Моментальный снимок**: создание моментальных снимков приложений Finance and Operations и приложений взаимодействия с клиентами. При необходимости восстановите предыдущее состояние при помощи моментальных снимков.

## <a name="deployment"></a>Развертывание

1. Загрузите шаблон из [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Войдите в [Microsoft Azure](https://portal.azure.com/).

3. Создайте [группу ресурсов](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Создайте [учетную запись хранения](/azure/storage/common/storage-account-create?tabs=azure-portal) в созданной группе ресурсов.

5. Создайте [фабрика данных](/azure/data-factory/quickstart-create-data-factory-portal) в созданной ранее группе ресурсов.

6. Откройте фабрику данных и выберите плитку **Автор и Монитор**.

7. На вкладке **Управление** выберите **шаблон ARM**.

8. Выберите **Импортировать шаблон ARM**, чтобы импортировать шаблон **Стороны**.

9. Импортируйте шаблон в фабрику данных. Введите следующие значения для **сведений о проекте** и **сведения об экземпляре**.

    Поле | значение
    ---|---
    Подписка | Подписка Azure
    Группа ресурсов | Укажите ресурс, под которым создается учетная запись хранения.
    Область | Укажите регион.
    Название фабрики | Укажите название фабрики.
    FO Linked Service_service Principal Key | Указывается ключ приложения.
    Azure Blob Storage_connection String | Строка подключения хранилища BLOB-объектов Azure.
    Dynamics Crm Linked Service_password | Пароль для учетной записи пользователя, указанной в качестве имени пользователя.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Укажите сведения о клиенте (доменное имя или код клиента), под которым приложение будет расположено.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Указывается идентификатор клиента приложения.
    Dynamics Crm Linked Service_properties_type Properties_username | Имя пользователя для подключения к Dynamics 365.

    Дополнительные сведения см. в следующих темах: 
    
    - [Ручное распространение шаблона Resource Manager для каждой среды](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Свойства связанной службы](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Копировать данные с помощью Фабрики данных Azure](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. После развертывания проверьте наборы данных, поток данных и связанную службу фабрики данных.

   ![Наборы данных, поток данных и связанная служба.](media/data-factory-validate.png)

11. Перейдите к **Управление**. В **Подключения** выберите **связанная служба**. Выберите **DynamicsCrmLinkedService**. В форме **Изменение связанной службы (Dynamics CRM)** введите следующие значения.

    Поле | значение
    ---|---
    ФИО | DynamicsCrmLinkedService
    описание | Связанные службы для подключения к экземпляру CRM для получения данных сущностей
    Подключение через среду выполнения интеграции | AutoResolvelntegrationRuntime
    Тип развертывания | Интерактивный режим
    URI службы | `https://<organization-name>.crm[x].dynamics.com`
    Тип проверки подлинности | Office365
    Имя пользователя |
    Пароль или Azure Key Vault | Пароль
    Пароль |

## <a name="run-the-template"></a>Выполните шаблон

1. Остановите сопоставления двойной записи **Учетная запись**, **Контактное лицо** и **Поставщик** с помощью приложения Finance and Operations.

    + Клиенты V3 (accounts)
    + Клиенты V3 (контакты)
    + CDS Контакты V2 (контакты)
    + CDS Контакты V2 (контакты)
    + Поставщик V2 (msdyn_vendor)

2. Убедитесь, что сопоставления удалены из таблицы `msdy_dualwriteruntimeconfig` в Dataverse.

3. Установка [решений стороны с двойной записью и глобальной адресной книги](https://aka.ms/dual-write-gab) из AppSource.

4. В приложении Finance and Operations, если следующие таблицы содержат данные, выполните действие **Начальная синхронизация** для них.

    + Приветствия
    + Типы характеров людей
    + Заключение
    + Обращения к контактному лицу
    + Роли принятия решений
    + Уровни лояльности

5. В приложении взаимодействия с клиентами отключите следующие шаги подключаемого модуля.

    + Обновление учетной записи
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Обновление учетной записи
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Обновление учетной записи
    + Обновление контактного лица
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Обновление контактного лица
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Обновление контактного лица
    + Обновление msdyn_party
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Обновление msdyn_party
    + Обновление msdyn_vendor
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Обновление msdyn_vendor

6. В приложении взаимодействия с клиентами отключите следующие workflow-процессы:

    + Создание поставщиков в таблице "Организации"
    + Создание поставщиков в таблице "Организации"
    + Создание поставщиков типа "респондент" в таблице "Контакты"
    + Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"
    + Обновление поставщиков в таблице "Организации"
    + Обновление поставщиков в таблице "Поставщики"
    + Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"
    + Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"

7. В фабрике данных выполните шаблон, выбрав **Активировать сейчас**, как показано на следующем изображении. Этот процесс может занять несколько часов в зависимости от объема данных.

    ![Активировать выполнение.](media/data-factory-trigger.png)

    > [!NOTE]
    > Если имеются настройки для **Учетная запись**, **Контактное лицо** и **Поставщик**, требуется изменить шаблон.

8. Импортируйте новые записи **Стороны** в приложение Finance and Operations.

    + Загрузите файл `FONewParty.csv` из хранилища BLOB-объектов Azure. Путь `partybootstrapping/output/FONewParty.csv`.
    + Преобразуйте файл `FONewParty.csv` в файл Excel и импортируйте файл Excel в приложение Finance and Operations. Если вам подходит импорт csv, можно напрямую импортировать файл CSV. Для выполнения импорта может потребоваться несколько часов, в зависимости от объема данных. Дополнительные сведения см. в разделе [Обзор заданий импорта и экспорта данных](../data-import-export-job.md).

    ![Импорт записей стороны Datavers.](media/data-factory-import-party.png)

9. В приложениях взаимодействия с клиентами включите следующие шаги подключаемого модуля:

    + Обновление учетной записи
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Обновление учетной записи
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Обновление учетной записи
    + Обновление контактного лица
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Обновление контактного лица
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Обновление контактного лица
    + Обновление msdyn_party
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Обновление msdyn_party
    + Обновление msdyn_vendor
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Обновление msdyn_vendor

10. В приложениях взаимодействия с клиентами активируйте следующие workflow-процессы, если они были деактивированы в предыдущих шагах:

    + Создание поставщиков в таблице "Организации"
    + Создание поставщиков в таблице "Организации"
    + Создание поставщиков типа "респондент" в таблице "Контакты"
    + Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"
    + Обновление поставщиков в таблице "Организации"
    + Обновление поставщиков в таблице "Поставщики"
    + Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"
    + Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"

11. Выполните сопоставления, связанные с **Стороной**, в соответствии с указаниями в [Сторона и глобальная адресная книга](party-gab.md).

## <a name="troubleshooting"></a>Устранение неполадок

1. В случае сбоя процесса перезапустите фабрику данных, начиная с невыполненного действия.
2. Некоторые файлы создаются фабрикой данных, которую можно использовать для целей проверки данных.
3. Фабрика данных выполняется на основе файлов CSV, разделенных запятыми. Если имеется значение поля с запятой, оно может повлиять на результаты. Необходимо удалить запятые.
4. Вкладка **Мониторинг** содержит сведения обо всех шагах и обработанных данных. Выбор конкретного шага для его отладки.

    ![Вкладка "Мониторинг".](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Дополнительные сведения о шаблоне

Дополнительные сведения о шаблоне можно найти в [комментариях к файлу сведений для шаблона фабрики данных Azure](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
