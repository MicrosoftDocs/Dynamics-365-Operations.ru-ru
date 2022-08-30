---
title: Рекомендации по развертыванию образца интеграции службы финансовой регистрации для Германии (устаревшая версия)
description: В этой статье приводятся указания по развертыванию примера финансовой интеграции для Германии, относящегося к пакету разработки программного обеспечения Retail SDK Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7315b6bb145ccdc5631a558af88de55660ebf877
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313864"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Рекомендации по развертыванию образца интеграции службы финансовой регистрации для Германии (устаревшая версия)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Необходимо следовать указаниям, изложенным в этой статье, только если используется Microsoft Dynamics 365 Commerce версии 10.0.28 или более ранней. В Commerce версии 10.0.29 пример интеграции службы финансовой регистрации для Германии доступен в пакете Commerce SDK. Дополнительные сведения см. в разделе [Настройка компонентов каналов](./emea-deu-fi-sample.md#configure-channel-components).

В этой статье приводятся рекомендации по развертыванию примера интеграции службы финансовой регистрации для Германии из пакета Retail SDK Dynamics 365 Commerce на виртуальной машине разработчика в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения об этом примере финансовой интеграции см. в разделе [Пример интеграции службы финансовой регистрации для Германии](emea-deu-fi-sample.md). 

Пример финансовой интеграции для Германии является частью пакета Retail SDK. Сведения о том, как установить и использовать этот пакет SDK см. в разделе [Архитектура комплекта средств разработки программного обеспечения (SDK) для Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Этот пример состоит из расширений Commerce Runtime (CRT) и Hardware Station. Для работы с этим примером необходимо изменить и построить проекты CRT и Hardware Station. Для внесения изменений, описанных в этой статье, рекомендуется использовать немодифицированный пакет Retail SDK. Кроме того, рекомендуется использовать систему управления версиями, такую как Azure DevOps, в которой никакие файлы еще не были изменены.

## <a name="development-environment"></a>Среда разработки

Выполните эти шаги для настройки среды разработки, чтобы можно было проверить и расширить пример.

### <a name="enable-commerce-runtime-extensions"></a>Включение расширений Commerce Runtime

Компоненты расширения CRT включены в образцы CRT. Чтобы выполнить следующие процедуры, откройте решение **CommerceRuntimeSamples.sln** в папке **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>Компонент DocumentProvider.EFRSample

1. Найдите проект **Runtime.Extensions.DocumentProvider.EFRSample** и постройте его.
2. В папке **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Commerce Scale Unit:** скопируйте файл в папку **\\bin\\ext** в местоположении сайта Internet Information Services (IIS) Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** скопируйте файл в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>Компонент DocumentProvider.DataModelEFR

1. Найдите проект **Runtime.Extensions.DocumentProvider.DataModelEFR** и постройте его.
2. В папке **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Commerce Scale Unit:** скопируйте файл в папку **\\bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** скопируйте файл в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Файл конфигурации расширения

1. Найдите файл конфигурации расширения для CRT:

    - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

2. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Включение расширений финансового соединителя

Можно включить расширения финансовых соединителей на [станции оборудования](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) или [POS-терминале](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Включение расширения Hardware Station

Компоненты расширения Hardware Station включены в образцы Hardware Station. Чтобы выполнить следующие процедуры, откройте решение **HardwareStationSamples.sln** в папке **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>Компонент EFRSample

1. Найдите проект **HardwareStation.Extension.EFRSample** и выполните его сборку.
2. В папке **Extension.EFRSample\\bin\\Debug** найдите следующие файлы сборок:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Скопируйте файлы сборки в папку расширений Hardware Station.

    - **Общая Hardware Station:** скопируйте файлы в папку **bin** в местоположении сайта IIS Hardware Station.
    - **Выделенная Hardware Station в Modern POS:** скопируйте файлы в местоположение брокера клиента Modern POS.

4. Найдите файл конфигурации расширения для расширений Hardware Station. Файл называется **HardwareStation.Extension.config**.

    - **Общая Hardware Station:** файл находится в местоположении сайта IIS Hardware Station.
    - **Выделенная Hardware Station в Modern POS:** файл находится в местоположении брокера клиента Modern POS.

5. Добавьте следующую строку в раздел **composition** файла конфигурации.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Включение расширений POS-терминала

Образец расширения POS-терминала находится в папке **src\\FiscalIntegration\\PosFiscalConnectorSample** репозитория [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

Чтобы использовать образец расширения POS-терминала в устаревшем пакете SDK, выполните следующие действия.

1. Скопируйте папку **Pos.Extension** в папку POS **Расширения** старого пакета SDK (например, `C:\RetailSDK\src\POS\Extensions`).
1. Переименуйте копию папки **Pos.Extension** в **PosFiscalConnector**.
1. Удалите следующие папки и файлы из папки **PosFiscalConnector**:

    - bin
    - DataService
    - devDependencies
    - Библиотеки
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Откройте решение **CloudPos.sln** или **ModernPos.sln**.
1. В проекте **Pos.Extensions** включите папку **PosFiscalConnector**.
1. Откройте файл **extensions.json** и добавьте расширение **PosFiscalConnector**.
1. Создайте SDK.

### <a name="production-environment"></a>Рабочая среда

В предыдущей процедуре вы включили расширения, которые являются компонентами примера интеграции службы финансовой регистрации. Кроме того, вы должны выполнить следующие дополнительные шаги, чтобы создать развертываемые пакеты, содержащие компоненты Commerce, и применить эти пакеты в производственной среде.

1. Выполните следующие изменения в файлах конфигурации пакетов в папке **RetailSdk\\Assets**:

    - В файлах конфигурации **commerceruntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** добавьте следующие строки в раздел **composition**.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - В файле конфигурации **HardwareStation.Extension.config** добавьте следующие строки в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Внесите следующие изменения в файл конфигурации настройки пакета **Customization.settings** в папке **BuildTools**:

    - Добавьте следующие строки, чтобы включить расширения CRT в развертываемые пакеты.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Добавьте следующие строки, чтобы включить расширения Hardware Station в развертываемые пакеты.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Запустите утилиту командной строки MSBuild для Visual Studio и запустите **msbuild** в папке Retail SDK, чтобы создать развертываемые пакеты.
4. Примените пакеты через LCS или вручную. Дополнительные сведения см. в разделе [Создание развертываемых пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Выполните все необходимые задачи настройки, описанные в разделе [Настройка Commerce для Германии](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Разработка расширений

Образец интеграции службы финансовой регистрации для Германии базируется на [функции финансовой интеграции](fiscal-integration-for-retail-channel.md). Дополнительные сведения о разработке решения финансовой интеграции см. в разделе [Обзор разработки примера финансовой интеграции](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Разработка расширения Commerce Runtime

Целью расширения, которое является поставщиком финансовых документов, является создание документов для конкретной службы и обработка откликов от службы финансовой регистрации.

Расширение CRT — это **Runtime.Extensions.DocumentProvider.EFRSample**. Дополнительные сведения о разработке решения финансовой интеграции см. в разделе [Обзор финансовой интеграции для каналов Commerce](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Обработчик запросов

Имеется один обработчик запросов для поставщика документов, **DocumentProviderEFRFiscalDEU**. Этот обработчик используется для создания финансовых документов для службы финансовой регистрации. Он наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени поставщика документа соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **GetFiscalDocumentDocumentProviderRequest** — этот запрос содержит сведения о том, что должен создаваться документ. Он возвращает специфический для службы документ, который должен быть зарегистрирован в службе финансовой регистрации.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** — этот запрос возвращает ответ вместе с расширенными данными.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации **DocumentProviderFiscalEFRSampleGermany** находится в папке **Configuration** проекта расширения. Целью этого файла является разрешение настройки для параметров поставщика фискального документа из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции.

Добавлены следующие параметры:

- **Сопоставление ставок НДС** — сопоставление значений процента налога, которые настроены для налоговых кодов для значений атрибута **TaxG** (налоговая группа) в запросах, отправляемых в финансовую службу.
- **Налоговая группа для подарочных сертификатов и депозитов** — значение атрибута **TaxG** в запросах, отправляемых в финансовую службу, на основе операций, включающих подарочные сертификаты или депозиты.
- **Сопоставление типов платежных средств** — сопоставление методов оплаты со значениями атрибута **PayG** (платежная группа) в запросах, отправляемых в финансовую службу.
- **Налоговая группа для освобождения от НДС** — значение атрибута **TaxG** в запросах, отправляемых в финансовую службу на основе операций, освобожденных от налоговых обязательств.
- **Включить данные клиента** — если этот параметр включен, запросы к финансовой службе будут содержать сведения о клиенте, такие как имена и адреса, в случаях, когда клиент добавляется в проводку.

### <a name="hardware-station-extension-design"></a>Разработка расширения Hardware Station

Целью расширения, которое является финансовым соединителем, является обмен данными со службой финансовой регистрации.

Расширение Hardware Station — это **HardwareStation.Extension.EFRSample**. Оно использует протокол HTTP для отправки документов, создаваемых расширением CRT в службе финансовой регистрации. Оно также обрабатывает отклики, полученные от службы финансовой регистрации.

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **EFRHandler** является точкой входа для обработки запросов к службе финансовой регистрации. Этот обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени финансового соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **SubmitDocumentFiscalDeviceRequest** — этот запрос отправляет документы в службу финансовой регистрации и возвращает из него отклики.
- **IsReadyFiscalDeviceRequest** — этот запрос используется для проверки работоспособности службы финансовой регистрации.
- **InitializeFiscalDeviceRequest** — этот запрос используется для инициализации службы финансовой регистрации.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **Configuration** проекта расширения. Целью файла является разрешение настройки для параметров финансового соединителя из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции.

Добавлены следующие параметры:

- **Адрес конечной точки** — URL-адрес службы финансовой регистрации.
- **Время ожидания** — период времени в миллисекундах (мс), в течение которого драйвер будет ожидать отклика от службы финансовой регистрации.
- **Показывать уведомления о финансовой регистрации** — если этот параметр включен, уведомления от финансовой службы будут отображаться как сообщения пользователя на POS-терминале.

### <a name="pos-fiscal-connector-extension-design"></a>Дизайн расширения финансового соединителя POS-терминала

Целью расширения финансового соединителя POS-терминала является обмен данными со службой финансовой регистрации из POS-терминала. Он использует протокол HTTPS для связи.

#### <a name="fiscal-connector-factory"></a>Фабрика финансовых соединителей

Фабрика финансовых соединителей сопоставляет имя соединителя с реализацией финансового соединителя и находится в файле **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Имя соединителя должно соответствовать имени финансового соединителя, указанного в Commerce Headquarters.

#### <a name="efr-fiscal-connector"></a>Финансовый соединитель EFR

Финансовый соединитель EFR находится в файле **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Он реализует интерфейс **IFiscalConnector**, который поддерживает следующие запросы:

- **FiscalRegisterSubmitDocumentClientRequest** — этот запрос отправляет документы в службу финансовой регистрации и возвращает из него отклики.
- **FiscalRegisterIsReadyClientRequest** — этот запрос используется для проверки работоспособности службы финансовой регистрации.
- **FiscalRegisterInitializeClientRequest** — этот запрос используется для инициализации службы финансовой регистрации.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** репозитория [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Целью файла является разрешение настройки для параметров финансового соединителя из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- **Адрес конечной точки** — URL-адрес службы финансовой регистрации.
- **Время ожидания** — период времени в миллисекундах, в течение которого соединитель будет ожидать отклика от службы финансовой регистрации.
