---
title: Пример интеграции службы финансовой регистрации для Австрии
description: В этой теме представлен обзор примера финансовой интеграции для Австрии в Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f03eab49f0abfc8a279ea43f69fa2ac0100bd34a
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2021
ms.locfileid: "7945047"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Пример интеграции службы финансовой регистрации для Австрии

[!include[banner](../includes/banner.md)]

В этой теме представлен обзор примера финансовой интеграции для Австрии в Microsoft Dynamics 365 Commerce.

Для соблюдения локальных финансовых требований для кассовых ККМ в Австрии функции Dynamics 365 Retail для Австрии включают образец интеграции POS-терминалов с внешней службой финансовой регистрации. Образец расширяет [функциональность финансовой интеграции](fiscal-integration-for-retail-channel.md). Он основан на решении [EFR (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) от [EFSTA](https://www.efsta.eu/at/) и обеспечивает связь с службой EFR через протокол HTTPS. Служба EFR должна располагаться на станции Retail Hardware Station или на отдельном компьютере, к которому можно подключиться с помощью Hardware Station. Пример представлен в форме исходного кода и является частью пакета SDK Retail.

Корпорация Майкрософт не выпускает никакое оборудование, программное обеспечение или документацию из EFSTA. Для получения сведений о получении решения EFR и работе с ним обратитесь в [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Сценарии

Пример интеграции службы финансовой интеграции для Австрии покрывает следующие сценарии.

- Регистрация кассовых проводок в службе финансовой регистрации:

    - Отправка подробной информации о проводках в службу финансовой регистрации. Эти данные включают сведения о строке продаж и сведения о скидках, платежах и налогах.
    - Сбор отклика от службы финансовой регистрации. Этот ответ содержит цифровую подпись и ссылку на зарегистрированную транзакцию.
    - Регистрация налогов и сопоставление их с налоговыми кодами службы финансовой регистрации.
    - Печать QR-кода для зарегистрированной проводки на чеке.

- Регистрация операций с подарочными сертификатами и депозитами клиентов в виде проводок, не связанных с наличными, в службе финансовой регистрации:

    - Расход или добавление средств на счету подарочного сертификата.
    - Регистрация депозита на счету клиента.
    - Регистрация депозита по заказу клиента.

- Регистрация проводок и событий, не связанных с продажами, в виде проводок, не связанных с наличными, в службе финансовой регистрации:

    - Открытие смены и закрытие смены
    - Начальная сумма, внесение денежных средств и удаление платежного средства
    - Переопределение цены
    - Переопределение налога
    - Печать копии чека
    - Открыть кассовый лоток
    - Печать X-отчета
    - Печать Z-отчета

- Печать выписок на конец дня (X/Z-отчетов), имеющих поля, связанные с Австрией:

    - Общее количество продуктов или услуг, которые были доставлены клиентам
    - Разбивка продаж по налоговой ставке
    - Разбивка платежей по кассиру/оператору контрольно-кассовой машины
    - Ценовые скидки и возвраты, уменьшающие ежедневные продажи
    - Нулевые продажи (раздачи)

- Обработка ошибок, например, следующие параметры:

    - Повторите попытку выполнения финансовой регистрации, если возможна повторная попытка, например в том случае, если служба финансовой регистрации недоступна, не готова или не отвечает.
    - Откладывание финансовой регистрации.
    - Пропустите финансовую регистрацию или пометьте проводку как зарегистрированную и включите коды сведений для фиксации причины сбоя и дополнительной информации.
    - Проверка доступности службы финансовой регистрации до открытия новой проводки по продажам или завершения проводки по продажам.

### <a name="gift-cards"></a>Подарочные сертификаты

В образце интеграции со службой финансовой регистрации реализованы следующие правила, которые относятся к подарочным сертификатам:

- Исключаются строки продаж, которые относятся к *выпуску подарочного сертификата* и *пополнения подарочного сертификата* из кассовой проводки. Вместо того, чтобы регистрировать эти строки как часть кассовой проводки, необходимо зарегистрировать их как отдельную проводку без наличных средств в службе финансовой регистрации.
- Не печатайте разбивку налоговых групп и QR-код в чеке, если чек состоит только из строк подарочного сертификата.
- Печатать общую сумму подарочных сертификатов, которые были выпущены или пополнены в проводке отдельно от суммы проводок с наличными средствами, на чеке.
- Сохранение рассчитанных корректировок строк платежа в базе данных канала со ссылкой на соответствующую финансовую проводку.
- Платеж по подарочным сертификатам считается обычным платежом.

### <a name="customer-deposits-and-customer-order-deposits"></a>Депозиты клиента и депозиты по заказу клиента

В образце интеграции со службой финансовой регистрации реализованы следующие правила, которые относятся к депозитам клиентов и депозитам заказов клиентов:

- Регистрация неденежной проводки, если проводка является депозитом клиента.
- Регистрация неденежной проводки, если проводка содержит только депозит по заказу клиента или возврат депозита по заказу клиента.
- Вычесть сумму депозита по заказу клиента из строк платежа, когда создается гибридный заказ клиента.
- Сохранение рассчитанных корректировок строк платежа в базе данных канала со ссылкой на финансовую проводку для гибридного заказа клиента.

### <a name="limitations-of-the-sample"></a>Ограничения примера

Служба финансовой регистрации поддерживает только ситуации, в которых налог включается в цену. Поэтому параметр **Цена включает налог** должен быть установлен в значение **Да** как для магазинов, так и для клиентов.

## <a name="set-up-commerce-for-austria"></a>Настройка Commerce для Австрии

В этом разделе описываются параметры Commerce, которые относятся к Австрии и рекомендованы для нее. Дополнительные сведения о настройке см. в разделе [Домашняя страница Commerce](../index.md).

Чтобы использовать функциональность, относящуюся к Австрии, вы должны указать следующие параметры:

- В основном адресе юридического лица задайте для поля **Страна/регион** значение **AUT** (Австрия).
- В профиле функциональности POS каждого магазина, расположенного в Австрии, установите для поля **Код ISO** значение **DE** (Австрия).

Также необходимо указать следующие параметры для Австрии. Обратите внимание, что после завершения настройки необходимо выполнить соответствующие задания распределения.

### <a name="set-up-vat-per-austrian-requirements"></a>Настройка НДС по требованиям Австрии

Необходимо создать коды налога, налоговые группы и налоговые группы номенклатур. Необходимо также настроить сведения о налогах для продуктов и услуг. Дополнительные сведения о настройке кодов и использовании функций налогов см. в разделе [Обзор налогов](../../finance/general-ledger/indirect-taxes-overview.md).

В чеке на продажу можно напечатать сокращенный код для налогового кода (например, "A" или "B"). Чтобы сделать эту функциональность доступной, установите поле **Печать кода** на странице **Налоговые коды**.

### <a name="set-up-stores"></a>Настройка магазинов

На странице **Все магазины** обновите сведения о магазинах. Конкретно, задайте следующие параметры:

- В поле **Налоговая группа** укажите налоговую группу, которая должна использоваться для продажи клиенту по умолчанию.
- Установите для параметра **Цены включают налог** значение **Да**.
- Задайте в поле **Имя** название компании. Это изменение помогает гарантировать, что название компании появится в чеке по продажам. Кроме того, можно добавить название компании в макет чека по продажам в качестве текста произвольной формы.
- В поле **Идентификационный номер налогоплательщика (ИНН)** укажите идентификационный номер компании. Это изменение помогает гарантировать, что идентификационный номер компании появится в чеке по продажам. Кроме того, можно добавить идентификационный номер компании в макет чека по продажам в качестве текста произвольной формы.

### <a name="set-up-functionality-profiles"></a>Настройка профилей функциональности

Настройте профили функциональности POS:

- На экспресс-вкладке **Нумерация чеков** настройте нумерацию чеков путем создания или обновления записей для типов проводок **Продажа**, **Заказ на продажу** и **Возврат**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Настройка настраиваемых полей таким образом, чтобы их можно было использовать в форматах чеков для чеков на продажу

Можно настроить текст языка и настраиваемые поля, используемые в форматах чеков POS-терминала. Компанией по умолчанию для пользователя, который создает настройку чека, должна быть то же юридическое лицо, в котором создана текстовая настройка языка. В качестве альтернативы необходимо создать те же тексты на языке компании пользователя по умолчанию и на языке юридического лица магазина, для которого создается настройка.

На странице **Текст языка** добавьте следующие записи для меток настраиваемых полей для макетов чеков. Обратите внимание на то, что значения **Код языка**, **Код текста** и **Текст**, показанные в таблице, являются просто примерами. Их можно изменить в зависимости от требований. Однако используемые вами значения **Код текста** должны быть уникальными и должны быть больше или равны 900001.

Добавьте следующие ярлыки POS в раздел **POS** поля **Текст языка** из таблицы:

| Код языка | Код текста | Текст                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR-код                   |
| en-US       | 900002  | Непрерывный номер         |
| en-US       | 900003  | Код печати налога на розницу     |
| en-US       | 900004  | Всего (продажи)             |
| en-US       | 900005  | Итого налог (продажи)         |
| en-US       | 900006  | Итого с налогом (продажи) |
| en-US       | 900007  | Сумма налога (продажи)        |
| en-US       | 900008  | Налоговая база (продажи)         |

На странице **Настраиваемые поля** добавьте следующие записи для настраиваемых полей для макетов чеков. Обратите внимание, что значения **Код текста подписи** должны соответствовать значениям **Код текста**, указанным на странице **Текст языка**:

| Имя                 | Тип    | ИД текста заголовка |
|----------------------|---------|-----------------|
| QRCODE               | Чек | 900001          |
| CONTINUOUSNUMBER     | Чек | 900002          |
| RETAILPRINTCODE      | Чек | 900003          |
| SALESTOTAL           | Чек | 900004          |
| SALESTOTALTAX        | Чек | 900005          |
| SALESTOTALINCLUDETAX | Чек | 900006          |
| SALESTAXAMOUNT       | Чек | 900007          |
| SALESTAXBASIS        | Чек | 900008          |

> [!NOTE]
> Важно указать правильные имена настраиваемых полей, как перечислено в предыдущей таблице. Неправильное имя настраиваемого поля приведет к пропущенным данным в чеках.

### <a name="configure-receipt-formats"></a>Настройка форматов чеков

Для каждого требуемого формата чека измените значение в поле **Поведение печати** на **Всегда печатать**.

В конструкторе формата чеков добавьте следующие настраиваемые поля в соответствующие разделы чека. Обратите внимание, что имена полей соответствуют текстам языка, определенным в предыдущем разделе.

- **Заголовок:** добавьте следующие поля:

    - Поля **Название магазина** и **Идентификационный номер налогоплательщика**, которые используются для печати названия компании и идентификационного номера на чеках. Кроме того, можно добавить название компании и идентификационный номер в макет чека по продажам в качестве текста произвольной формы.
    - Поля **Адрес магазина**, **Дата**, **Время в формате 24H**, **Номер чека** и **Номер ККМ**.
    - Поле **Непрерывный номер**, чтобы идентифицировать номер кассовой проводки в службе финансовой регистрации.

- **Строки:** добавьте следующие поля:

    - **Наименование номенклатуры**.
    - **Кол-во**.
    - **Общая цена с учетом налога**.
    - **Код печати налога на розницу**, которое используется для печати сокращенного кода, соответствующего налоговому коду, который применяется к номенклатуре.

- **Нижний колонтитул:** добавьте следующие поля:

    - Поля оплаты, чтобы печатались суммы платежа для каждого метода платежа. Например, добавьте поля **Название платежного средства** и **Сумма платежного средства** в одну строку макета.
    - Группа полей **Итого по продажам**:

        - Поле **Всего (продажи)**, которое используется для печати общей суммы кассовых продаж по чеку. Сумма не включает налог. Операции с предоплатой и подарочными картами исключаются.
        - Поле **Всего с налогами (продажи)**, которое используется для печати общей суммы кассовых продаж по чеку. Сумма включает налог. Операции с предоплатой и подарочными картами исключаются.
        - Поле **Итого налоги (продажи)**, которое используется для печати общей суммы налогов по чеку для кассовых продаж. Операции с предоплатой и подарочными картами исключаются.

    - Группа полей **Разбиение налогов**. Все поля в этой группе полей должны печататься на одной отдельной строке.

        - Поле **Налоговый код**, представляющее собой стандартное поле, позволяющее печатать сводку налогов для каждого налогового кода. Это поле должно быть добавлено на новую строку.
        - Поле **Процент налога** — это стандартное поле, используемое для печати эффективной налоговой ставки для налогового кода.
        - Поле **Налоговая база (продажи)**, используемое для печати общей суммы чека продажи за денежные средства для налогового кода. Операции с предоплатой и подарочными картами исключаются.
        - Поле **Сумма налога (продажи)**, используемое для печати суммы налога по чеку для продаж за денежные средства для налогового кода.
        - Поле **Код печати налога на розницу**, которое используется для печати сокращенного кода, соответствующего налоговому коду.

    - Поле **QR-код**, которое используется для печати ссылки на зарегистрированную кассовую проводку в форме QR-кода.

        > [!NOTE]
        > Значение **QR-код** извлекается из ответа финансового регистра. EFR возвращает QR-код в своем ответе, только если значение поля **Атрибуты** в конфигурации EFR описано в документации EFSTA. Формат QR-кода в поле **Атрибуты** конфигурации EFR должен быть установлено на значение **BMP**.

Дополнительные сведения о работе с форматами чеков см. в разделе [Настройка и конструирование форматов чеков](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Настройка финансовой интеграции для Австрия

Образец интеграции службы финансовой регистрации для Австрии базируется на [функции финансовой интеграции](fiscal-integration-for-retail-channel.md) и входит в состав пакета Retail SDK. Пример находится в папке **src\\FiscalIntegration\\Efr** репозитория [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (например, [пример в выпуске release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Пример [состоит](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) из поставщика финансового документа, который является расширением среды выполнения Commerce Runtime (CRT), и финансового соединителя, который является расширением Commerce Hardware Station. Для получения дополнительных сведений о способах использования пакета Retail SDK см. разделы [Архитектура пакета Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) и [Настройка конвейера сборки для пакета SDK независимой упаковки](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Вследствие ограничений [новой модели независимой упаковки и расширения](../dev-itpro/build-pipeline.md), она не может использоваться для этого образца финансовой интеграции. Необходимо использовать предыдущую версию пакета Retail SDK на виртуальной машине (ВМ) разработчика в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения см. в разделе [рекомендации по развертыванию образца интеграции финансового принтера для Австрии (устаревшая версия)](emea-aut-fi-sample-sdk.md). Поддержка новой независимой модели упаковки и расширения для образцов финансовой интеграции запланирована для последующих версий.

Выполните шаги настройки финансовой интеграции, как описано в разделе [Настройка финансовой интеграции для каналов Commerce](setting-up-fiscal-integration-for-retail-channel.md):

1. [Настройте процесс финансовой регистрации](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Кроме того, запишите настройки для процесса финансовой регистрации, которые [относятся к данному образцу интеграции со службой финансовой регистрации](#set-up-the-registration-process).
1. [Задайте параметры обработки ошибок](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Включите выполнение вручную отложенной финансовой регистрации](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Настройте компоненты каналов](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Настройка процесса регистрации

Чтобы включить процесс регистрации, выполните следующие действия для настройки Commerce Headquarters. Дополнительные сведения см. в разделе [Настройка финансовой интеграции для каналов Commerce](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Загрузите файлы конфигурации для поставщика фискальных документов и финансового соединителя:

    1. Откройте репозиторий [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Выберите правильную версию ветви выпуска в соответствии с версией пакета SDK/приложения (например, **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Откройте **src \> FiscalIntegration \> Efr**.
    1. Откройте **Конфигурации \> DocumentProviders** и загрузите файлы конфигурации поставщика финансовых документов: **DocumentProviderFiscalEFRSampleAustria.xml** и **DocumentProviderNonFiscalEFRSampleAustria.xml** (например, [местоположение файлов для выпуска release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Загрузите файл конфигурации финансового соединителя по пути **Конфигурации \> Соединители \> ConnectorEFRSample.xml** (например, [файл для release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Вследствие ограничений [новой модели независимой упаковки и расширения](../dev-itpro/build-pipeline.md), она не может использоваться для этого образца финансовой интеграции. Необходимо использовать предыдущую версию пакета Retail SDK на виртуальной машине разработчика в LCS. Файлы конфигурации для данного образца финансовой интеграции находятся в следующих папках пакета Retail SDK на виртуальной машине для разработчиков в LCS:
    >
    > - **Файлы конфигурации поставщика финансовых документов:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Файл конфигурации финансового соединителя:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > Поддержка новой независимой модели упаковки и расширения для образцов финансовой интеграции запланирована для последующих версий.

1. Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры \> Общие параметры Commerce**. На вкладке **Общие** задайте для параметра **Включить финансовую интеграцию** значение **Да**.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Поставщики финансовых документов** и загрузите ранее скаченные файлы конфигурации поставщика финансовых документов.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Финансовые соединители** и загрузите ранее скаченный файл конфигурации финансового соединителя.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Функциональные профили соединителей**. Создайте два новых функциональных профиля соединителей, по одному для каждого поставщика финансовых документов, которые были загружены ранее, и выберите ранее загруженный финансовый соединитель. При необходимости обновите [параметры сопоставления данных](#default-data-mapping).
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Технические профили соединителей**. Создайте новый технический профиль соединителя и выберите финансовый соединитель, который был загружен ранее. При необходимости обновите [параметры соединителя](#fiscal-connector-settings).
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Группы финансовых соединителей**. Создайте две новые группы финансовых соединителей, по одному для каждого функционального профиля соединителя, созданного ранее.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Процессы финансовой регистрации**. Создайте новый процесс финансовой регистрации и два шага процесса финансовой регистрации и выберите созданные ранее группы фискальных соединителей.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка POS \> Профили POS \> Профили функциональности**. Выберите профиль функциональности, связанный с магазином, в котором должен быть активирован процесс регистрации. На экспресс-вкладке **Процесс финансовой регистрации** выберите ранее созданный процесс финансовой регистрации. Чтобы включить регистрацию нефинансовых событий в POS, на экспресс-вкладке **Функции** в группе **POS** установите для параметра **Аудит** значение **Да**.
1. Перейдите **Retail и Commerce \> Настройка канала \> Настройка POS \> Профили POS \> Профили оборудования**. Выберите профиль оборудования, который связан с Hardware Station, с которой будет связан фискальный принтер. На экспресс-вкладке **Фискальная периферия** выберите ранее созданный технический профиль соединителя.
1. Откройте график распределения (**Retail и Commerce \> ИТ Retail и Commerce \> График распределения**) и выберите задания **1070** и **1090** для передачи данных в базу данных канала.

#### <a name="default-data-mapping"></a>Сопоставление данных по умолчанию

Следующее сопоставление данных по умолчанию включено в конфигурацию поставщика фискальных документов, которая предоставляется в составе образца финансовой интеграции:

- **Сопоставление ставок налога на добавленную стоимость (НДС)** — сопоставление значений процента налога, которые настроены для налоговых кодов для значений атрибута **TaxG** (налоговая группа) в запросах, отправляемых в финансовую службу. Вот сопоставление по умолчанию:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Первый компонент в каждой паре представляет налоговую группу НДС, которая поддерживается службой финансовой регистрации EFR. Второй компонент представляет соответствующую ставку НДС. Дополнительные сведения о налоговых группах НДС, поддерживаемых EFR для Австрии, см. в разделе [Справочник по EFR](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Параметры финансового соединителя

Следующие параметры включены в конфигурацию финансового соединителя, которая предоставляется в составе образца финансовой интеграции:

- **Адрес конечной точки** — URL-адрес службы финансовой регистрации.
- **Время ожидания устройства** — период времени в миллисекундах, в течение которого финансовый соединитель будет ожидать отклика от службы финансовой регистрации.
- **Показывать уведомления о финансовой регистрации** — этот флаг определяет, должны ли отображаться оператору уведомления, возвращаемые службой финансовой регистрации.

### <a name="configure-channel-components"></a>Настройка компонентов канала

> [!WARNING]
> Вследствие ограничений [новой модели независимой упаковки и расширения](../dev-itpro/build-pipeline.md), она не может использоваться для этого образца финансовой интеграции. Необходимо использовать предыдущую версию пакета Retail SDK на виртуальной машине разработчика в LCS. Дополнительные сведения см. в разделе [рекомендации по развертыванию образца интеграции финансового принтера для Австрии (устаревшая версия)](emea-aut-fi-sample-sdk.md).
>
> Поддержка новой независимой модели упаковки и расширения для образцов финансовой интеграции запланирована для последующих версий.

#### <a name="set-up-the-development-environment"></a>Настройка среды разработки

Чтобы настроить среду разработки для проверки и расширения образца, выполните следующие действия.

1. Создайте точную копию или загрузите репозиторий [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Выберите правильную версию ветви выпуска в соответствии с версией пакета SDK/приложения. Дополнительные сведения см. в разделе [Загрузка примеров Retail SDK и справочных пакетов из GitHub и NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Откройте решение EFR в **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** и создайте его.
1. Установите расширения CRT:

    1. Найдите установщик расширений CRT:

        - **Commerce Scale Unit:** в папке **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** найдите программу установки **ScaleUnit.EFR.Installer**.
        - **Локальный CRT на Modern POS:** в папке **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** найдите программу установки **ModernPOS.EFR.Installer**.

    1. Запустите установщик расширений CRT из командной строки:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Локальный CRT на Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Установите расширения Hardware Station:

    1. В папке **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** найдите программу установки **HardwareStation.EFR.Installer**.
    1. Запустите установщик расширений из командной строки.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Рабочая среда

Выполните шаги, описанные в разделе [Настройка конвейера построения для образца финансовой интеграции](fiscal-integration-sample-build-pipeline.md), чтобы создать и выпустить облачную единицу масштабирования и развертываемые пакеты самообслуживания для образца финансовой интеграции. Файл шаблона YAML **EFR build-pipeline.yml** можно найти в папке **Pipeline\\YAML_Files** репозитория [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Разработка расширений

Образец интеграции службы финансовой регистрации для Австрии базируется на [функции финансовой интеграции](fiscal-integration-for-retail-channel.md) и входит в состав пакета Retail SDK. Пример находится в папке **src\\FiscalIntegration\\Efr** репозитория [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (например, [пример в выпуске release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Пример [состоит](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) из поставщика финансового документа, который является расширением CRT, и финансового соединителя, который является расширением Commerce Hardware Station. Для получения дополнительных сведений о способах использования пакета Retail SDK см. разделы [Архитектура пакета Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) и [Настройка конвейера сборки для пакета SDK независимой упаковки](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Вследствие ограничений [новой модели независимой упаковки и расширения](../dev-itpro/build-pipeline.md), она не может использоваться для этого образца финансовой интеграции. Необходимо использовать предыдущую версию пакета Retail SDK на виртуальной машине разработчика в LCS. Дополнительные сведения см. в разделе [рекомендации по развертыванию образца интеграции финансового принтера для Австрии (устаревшая версия)](emea-aut-fi-sample-sdk.md). Поддержка новой независимой модели упаковки и расширения для образцов финансовой интеграции запланирована для последующих версий.

### <a name="commerce-runtime-extension-design"></a>Разработка расширения Commerce Runtime

Целью расширения, которое является поставщиком финансовых документов, является создание документов для конкретной службы и обработка откликов от службы финансовой регистрации.

#### <a name="request-handler"></a>Обработчик запросов

Для поставщиков документов имеется два обработчика запросов:

- **DocumentProviderEFRFiscalAUT** — этот обработчик используется для создания финансовых документов для службы финансовой регистрации.
- **DocumentProviderEFRNonFiscalAUT** — этот обработчик используется для создания нефинансовых документов для службы финансовой регистрации.

Эти обработчики наследуются из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени поставщика документа соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **GetFiscalDocumentDocumentProviderRequest** — этот запрос содержит сведения о том, что должен создаваться документ. Он возвращает специфический для службы документ, который должен быть зарегистрирован в службе финансовой регистрации.
- **GetNonFiscalDocumentDocumentProviderRequest** — этот запрос содержит сведения о том, что должен создаваться нефинансовый документ. Он возвращает специфический для службы документ, который должен быть зарегистрирован в службе финансовой регистрации.
- **GetSupportedRegistrableEventsDocumentProviderRequest** — этот запрос возвращает список событий, на которые необходимо подписаться. В настоящее время поддерживаются следующие события: продажи, печать X-отчета, печать Z-отчета, депозиты счетов клиентов, депозиты заказов клиентов, события аудита и проводки, не связанные с продажами.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** — этот запрос возвращает ответ от службы финансовой регистрации. Этот ответ сериализуется для формирования строки, чтобы ее можно было сохранить.

#### <a name="configuration"></a>Конфигурация

Файлы конфигурации для поставщика фискального документа расположены в папке **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** в репозитории [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/):

- **DocumentProviderFiscalEFRSampleAustria** — файл конфигурации для поставщика финансовых документов для финансовых документов.
- **DocumentProviderNonFiscalEFRSampleAustria** — файл конфигурации для поставщика финансовых документов для нефинансовых документов.

Целью этих файлов является разрешение настройки параметров поставщика фискального документа из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции.

### <a name="hardware-station-extension-design"></a>Разработка расширения Hardware Station

Целью расширения, которое является финансовым соединителем, является обмен данными со службой финансовой регистрации. Расширение аппаратной станции использует протокол HTTP для отправки документов, создаваемых расширением CRT в службе финансовой регистрации. Оно также обрабатывает отклики, полученные от службы финансовой регистрации.

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **EFRHandler** является точкой входа для обработки запросов к службе финансовой регистрации.

Обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени финансового соединителя, указанного в Commerce Headquarters.

Финансовый соединитель поддерживает следующие запросы:

- **SubmitDocumentFiscalDeviceRequest** — этот запрос отправляет документы в службу финансовой регистрации и возвращает из него отклики.
- **IsReadyFiscalDeviceRequest** — этот запрос используется для проверки работоспособности службы финансовой регистрации.
- **InitializeFiscalDeviceRequest** — этот запрос используется для инициализации службы финансовой регистрации.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации для фискального соединителя расположен по пути **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** в репозитории [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Целью файла является разрешение настройки параметров финансового соединителя из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]