---
title: Инициализация Commerce Scale Unit (облако)
description: В этой статье объясняется, как инициализировать Commerce Scale Unit (облако) в Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 6b42252a37f01a2b387c2393760998a6b2e4761d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271526"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Инициализация Commerce Scale Unit (облако)

[!include[banner](../includes/banner.md)]

В этой статье объясняется, как инициализировать Commerce Scale Unit (облако) в Microsoft Dynamics 365 Commerce.

Если используется песочница уровня 2 или рабочая среда с версией приложения 8.1.2. x или более поздней, необходимо инициализировать Commerce Scale Unit (облако), прежде чем можно будет использовать функцию канала розничной торговли для операций POS или операций электронной коммерции, использующих розничный сервер в облаке. При инициализации будет выполнено развертывание Commerce Scale Unit (облако).

> [!IMPORTANT]
> Для существующих клиентов, использующих функции канала розничной торговли в облаке, чтобы обеспечить непрерывную и бесперебойную поддержку бизнеса, необходимо обновить каналы розничной торговли для использования Commerce Scale Unit. Новые среды, развернутые без Commerce Scale Unit, не будут получать обновления качества и обслуживания для компонентов канала розничной торговли, размещаемых в облаке. Нет необходимости предпринимать никаких действий для клиентов, которые используют исключительно Commerce Scale Unit (самостоятельная версия). Если вам требуется расширение, обратитесь к своему Microsoft FastTrack Solution Architect.

## <a name="prerequisites"></a>Необходимые условия

1. Разверните песочницу уровня 2 или рабочую среду с версией 8.1.2. x или более поздней.
2. Можно самостоятельно развернуть до 2 Commerce Scale Unit на каждую среду. Если требуется более 2 Commerce Scale Unit на каждую среду, в Microsoft Dynamics Lifecycle Services (LCS) создайте запрос на техническую поддержку и введите **Запрос на дополнительные Commerce Scale Unit** и укажите код среды, количество Commerce Scale Unit и требуемые регионы центров обработки данных. Запрос будет завершен в течение пяти рабочих дней. Если не требуется более 2 Commerce Scale Unit на каждую среду, нет необходимости создавать запрос поддержки. 
3. Прежде чем можно будет инициализировать Commerce Scale Unit, необходимо получить разрешения владельца проекта в Lifecycle Services.
4. Убедитесь, что ключи конфигурации розничной лицензии включены в вашей среде. Дополнительные сведения см. в разделе [Отчет о лицензионных кодах и ключах конфигурации](../sysadmin/license-codes-configuration-keys-report.md). Для использования Commerce Scale Unit необходимо включить следующие ключи.

    - RetailBasic
    - RetaileCommerce — если планируется использовать электронную коммерцию для Dynamics 365 Commerce.
    - RetailGiftCard — если планируется использовать подарочные сертификаты.
    - RetailInvent — если планируется использовать запасы.
    - RetailModernPos — если планируется использовать POS.
    - RetailReplenishment — если планируется использовать пополнения.
    - RetailScheduler
    - RetailStores — если планируется использовать POS.


## <a name="region-availability"></a>Региональная доступность
Commerce Scale Unit доступно для развертывания в следующих регионах:

| Глобальное местоположение | Регион              | Доступность        | Комментарии                  |
|-----------------|---------------------|---------------------|---------------------------|
| АМЕРИКА        | Восточная часть США             | Общедоступно |  Комментариев нет.                         |
| АМЕРИКА        | Восточная часть США 2           | Общедоступно |  Комментариев нет.                          |
| АМЕРИКА        | Северо-центральный регион США    | Ограничение по емкости    |  Комментариев нет.                            |
| АМЕРИКА        | Юго-центральный регион США    | Ограничение по емкости    |  Комментариев нет.                            |
| АМЕРИКА        | Центральная часть США          | Общедоступно |  Комментариев нет.                            |
| АМЕРИКА        | Западная часть США             | Общедоступно |  Комментариев нет.                            |
| АМЕРИКА        | Западная часть США 2           | Общедоступно |  Комментариев нет.                            |
| АМЕРИКА        | Центральная Канада      | Ограничение по емкости    |  Комментариев нет.                            |
| АМЕРИКА        | Восточная Канада         | Ограничение по емкости    |   Комментариев нет.                           |
| АМЕРИКА        | Центрально-западная часть США     | Ограничение по емкости    |   Комментариев нет.                           |
| Азиатско-Тихоокеанский регион            | Восточная Австралия      | Общедоступно |   Комментариев нет.                           |
| Азиатско-Тихоокеанский регион            | Юго-Восточная Азия      | Емкость ограничена | Развертывание запрещено.    |
| Азиатско-Тихоокеанский регион            | Восточная Япония          | Общедоступно |  Комментариев нет.                            |
| Азиатско-Тихоокеанский регион            | Западная Япония          | Общедоступно |   Комментариев нет.                           |
| Азиатско-Тихоокеанский регион            | Юго-восточная Австралия | Общедоступно |   Комментариев нет.                           |
| Азиатско-Тихоокеанский регион            | Восточная Азия           | Ограничение по емкости    |   Комментариев нет.                           |
| Азиатско-Тихоокеанский регион            | Южная Индия         | Емкость ограничена | Развертывание запрещено.    |
| Азиатско-Тихоокеанский регион            | Центральная Индия       | Ограничение по емкости    | Требуется процесс утверждения. |
| Европа, Ближний Восток и Африка            | Западная Европа         | Ограничение по емкости    | В настоящее время недоступно в LCS. |
| Европа, Ближний Восток и Африка            | Северная Европа        | Ограничение по емкости    | В настоящее время недоступно в LCS. |
| Европа, Ближний Восток и Африка            | Южная часть Соединенного Королевства            | Общедоступно |    Комментариев нет.                          |
| Европа, Ближний Восток и Африка            | Западная часть Соединенного Королевства             | Общедоступно |    Комментариев нет.                          |
| Швейцария     | Северная Швейцария   | Ограничение по емкости    | Требуется процесс утверждения. |
| ОАЭ             | Северная часть ОАЭ           | Ограничение по емкости    | Требуется процесс утверждения. |

Емкость развертывания в регионах с ограниченной емкостью чрезвычайно ограничена. Запросы на развертывание оцениваются в зависимости от обстоятельств. Если у вас есть важные бизнес-потребности для развертывания в регионах с ограничением по емкости, вы можете подать запрос на поддержку для добавления в список ожидания. В настоящее время развертывание Commerce Scale Unit в областях с ограниченной емкостью не разрешено. 

![Карта, показывающая доступность региона](media/Commerce-Scale-Unit-Region-Availability.png "Карта, показывающая доступность региона")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Инициализация Commerce Scale Unit в рамках развертывания новой среды

Убедитесь, что центральный офис доступен. Это необходимо для регистрации единицы масштабирования в центральном офисе в процессе инициализации. Не рекомендуется инициализировать единицу масштабирования в случае, когда центральный офис находится на обслуживании, поскольку он может стать недоступным во время процесса обслуживания.

1. Убедитесь, что среда центрального офиса доступна и не находится в [режиме обслуживания](../sysadmin/maintenance-mode.md).
2. В LCS на странице сведений о среде выберите **Функции среды \> Commerce**.
3. На странице развертывания настройки Commerce выберите **Инициализировать**.
4. Выберите версию Commerce Scale Unit, которую необходимо инициализировать.
5. Выберите регион для инициализации Commerce Scale Unit.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Настройка каналов для использования Commerce Scale Unit

После развертывания Commerce Scale Unit необходимо убедиться, что каналы настроены на использование для них базы данных. 

Чтобы настроить каналы для использования базы данных Commerce Scale Unit, выполните следующие действия.

1. В Commerce Headquarters перейдите в раздел **Розничная торговля и коммерция \> Настройка центрального офиса \> Планировщик коммерции \> База данных канала**.
1. В левой области выберите базу данных канала.
1. На экспресс-вкладке **Канал розничной торговли** выберите **Добавить**, а затем выберите розничный канал в раскрывающемся списке.
1. Выберите **Добавить**, а затем выберите интерактивный канал в раскрывающемся списке. 

По готовности перейдите **Розничная торговля и коммерция \> ИТ розничной торговли и коммерции \> График распределения** и выполните задание 9999.

> [!NOTE] 
> Задание 9999 синхронизирует все новые продукты и клиенты в Commerce Scale Unit. Этот процесс может занять продолжительное время. Если канал должен быть доступен только для конфигурации конструктора сайта электронной коммерции, можно выполнить задание 1070 вместо задания 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Обновления базы данных и Commerce Scale Unit

Прежде чем начать, убедитесь, что вы знакомы с [шагами, которые необходимо выполнить после обновления базы данных для сред, использующих функции Commerce](../database/database-refresh.md).

Записи базы данных канала масштабирования (в форме базы данных канала) не могут быть перемещены между средами в ходе обновления базы данных. Это обусловлено тем, что записи представляют собой конфигурацию, зависящую от среды.

После обновления базы данных можно повторно создать запись базы данных канала единицы масштабирования, выполнив повторное развертывание единицы масштабирования в LCS. Любая операция развертывания или обслуживания в единице масштабирования попытается зарегистрировать единицу масштабирования в центральном офисе, если регистрация найдена как отсутствующая.

Можно выполнить повторное развертывание единицы масштабирования, не меняя каких-либо компонентов, выбрав развертывание той же версии единицы масштабирования, которая уже используется. Это можно сделать с помощью LCS, выполнив следующие действия:

1. В LCS на странице сведений о среде выберите **Функции среды \> Розничная торговля**.
2. На странице развертывания установки выберите единицу масштабирования, которую необходимо развернуть повторно.
3. В меню единицы масштабирования выберите **Обновить**.
4. На ползунке в раскрывающемся списке **Выберите версию**, выберите параметр **Указать версию**.
5. В текстовом поле в разделе **Указать версию** введите версию, отображаемую для единицы масштабирования, которая отображается помимо метки **текущей версии**.
6. Нажмите кнопку **Обновить**.

Вам не нужно выбирать **Обновить расширения**, даже если ранее были применены расширения, так как последний пакет расширения, примененный к единице масштабирования, автоматически устанавливается при обновлении единицы масштабирования.

При наличии нескольких единиц масштабирования необходимо выполнить операцию, указанную выше, для каждой единицы масштабирования. При необходимости эти операции можно выполнить параллельно.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Развертывание дополнительных Commerce Scale Unit (необязательно)

После инициализации Commerce Scale Unit можно выполнить автоматическое развертывание второй единицы масштабирования, если лицензия дает право на это. Чтобы развернуть более двух единиц масштабирования, необходимо создать запрос в поддержку. В запросе в поддержку укажите количество требуемых Commerce Scale Unit, название среды и нужные регионы. Дополнительные сведения об лицензировании см. в разделе [Руководство по лицензированию Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Для каждого дополнительного Commerce Scale Unit, который будет развернуто, рекомендуется создать отдельную группу базы данных каналов, выполнив следующие действия.

1. В центральном офисе Commerce перейдите в раздел **Розничная торговля и коммерция > Retail Headquarters > Настройка Розничная сеть - Планировщик > Группа базы данных канала**.
2. Создание новой группы баз данных канала.
3. Перейдите в **Розничная торговля и коммерция > Retail Headquarters > Настройка Розничная сеть - Планировщик > База данных канала** и выберите базу данных канала, соответствующую вновь созданному Commerce Scale Unit.
4. Выберите **Редактировать** и выберите новую группу базы данных канала.
5. Нажмите **Сохранить**.
6. Выберите **Выполнение полной синхронизации данных** для выбранной базы данных канала.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Дополнительные сведения о том, как инициализировать компоненты канала Commerce в облаке в существующей среде

Если в среде уже используются компоненты канала Commerce, размещенные в облаке, инициализация Commerce Scale Unit поможет сократить время простоя при обновлении этих компонентов. Перед инициализацией Commerce Scale Unit необходимо выполнить дополнительное планирование.

При инициализации первого Commerce Scale Unit в среде, использующей компоненты канала Commerce, размещенные на облаке, процесс инициализации перенесет каналы, связанные с компонентами канала в облаке, в первую единицу масштабирования. Каналы, связанные с единицами масштабирования магазина, не изменяются.

Процесс миграции прозрачен для каналов. После начала инициализации единицы масштабирования автоматически выполняются следующие операции:

1. Будет создана новая Commerce Scale Unit и связана со средой.
2. Commerce Scale Unit будет зарегистрирована как доступная база данных канала в центральном офисе.
3. Все каналы, сопоставленные с базой данных канала **По умолчанию** в центральном офисе, будут обновлены для сопоставления с новой Commerce Scale Unit.
4. Полная синхронизация данных Commerce Data Exchange (CDX) будет выполнена, чтобы вернуть данные канала в новую единицу масштабирования.

**Планирование и тестирование для инициализации Commerce Scale Unit** Как правило, при инициализации Commerce Scale Unit необходимо запланировать период бездействия в пять часов для операций магазина, а также все операции каналов электронной коммерции, использующие розничный сервер или облачный POS.

1. Выполните обновление базы данных из рабочей среды в среду-песочницу UAT. 
2. Инициализируйте Commerce Scale Unit в среде-песочнице UAT. 
3. Обратите внимание на время инициализации, которое должно пройти для Commerce Scale Unit. Это будет сравнимо с временем, которое эта операция занимает в рабочей среде, в течение которого операции магазина и операции электронной коммерции будут недоступны.

Перед инициализацией Commerce Scale Unit необходимо выполнить следующие дополнительные шаги.

- **Закрыть все смены POS** — после миграции пользователи POS не смогут закрыть смены, которые были активны в процессе миграции.
- **Убедитесь, что все P-задания были успешно выполнены** — рекомендуется, чтобы P-задания синхронизировали ожидающие обработки проводки до инициализации CSU.
- **Выйти со всех устройств POS** — во время миграции операции POS не поддерживаются.
- **Отозвать и аннулировать все приостановленные проводки в POS** — приостановленные проводки не сохраняются в процессе инициализации.

> [!IMPORTANT]
> В процессе инициализации Commerce Scale Unit предыдущие приостановленные проводки будут утрачены и не могут быть отозваны. 

В течение периода инициализации происходит следующее:

- Каналы Commerce, размещаемые в облаке, не будут работать, если не будет включена функция работы POS в автономном режиме.
- POS-устройства, в которых включены возможности автономной работы, будут иметь ограниченную функциональность.
- Все клиенты электронной коммерции, зависящие от розничного сервера, будут нарушены.
- Это не повлияет на каналы, размещенные в Commerce Scale Unit (автономно).
- Функциональность центрального офиса не затрагивается.

После завершения инициализации происходит следующее:

- Состояние активации устройства всех активированных POS-устройств сохраняется, что означает, что устройства не должны быть повторно активированы.
- Автономные экземпляры аппаратных станций будут продолжать работать.
- Отчеты по каналам POS будут сброшены и не будут показывать данные перед инициализацией.
- Операция отображения журнала также будет сброшена и не будет показывать данные перед инициализацией.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]