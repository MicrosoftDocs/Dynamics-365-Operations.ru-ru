---
title: Рекомендации по развертыванию образца интеграции финансового принтера для Польши (устаревшая версия)
description: В этой статье приводятся указания по развертыванию примера интеграции финансового принтера для Польши, относящегося к пакету разработки программного обеспечения Retail SDK Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: b19c8d7a80ac772ae238191d1285a1ad80e6f611
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473967"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Рекомендации по развертыванию образца интеграции финансового принтера для Польши (устаревшая версия)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Необходимо следовать указаниям, изложенным в этой статье, только если используется Microsoft Dynamics 365 Commerce версии 10.0.28 или более ранней. В Commerce версии 10.0.29 пример интеграции финансового принтера для Польши доступен в пакете Commerce SDK. Дополнительные сведения см. в разделе [Настройка компонентов каналов](./emea-pol-fpi-sample.md#configure-channel-components).

В этой статье приводятся рекомендации по развертыванию образца интеграции финансового принтера для Польши из пакета Retail SDK Dynamics 365 Commerce на виртуальной машине разработчика в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения об этом примере финансовой интеграции см. в разделе [Пример интеграции финансового принтера для Польши](emea-pol-fpi-sample.md). 

Пример финансовой интеграции для Польши является частью пакета Retail SDK. Сведения о том, как установить и использовать этот пакет SDK см. в разделе [Архитектура комплекта средств разработки программного обеспечения (SDK) для Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Этот пример состоит из расширений Commerce Runtime (CRT) и Hardware Station. Для работы с этим примером необходимо изменить и построить проекты CRT и Hardware Station. Для внесения изменений, описанных в этой статье, рекомендуется использовать немодифицированный пакет Retail SDK. Кроме того, рекомендуется использовать систему управления версиями, такую как Azure DevOps, в которой никакие файлы еще не были изменены.

## <a name="development-environment"></a>Среда разработки

Выполните эти шаги для настройки среды разработки, чтобы можно было проверить и расширить пример.

### <a name="commerce-runtime-extension-components"></a>Компоненты расширения Commerce Runtime

Компоненты расширения CRT включены в Retail SDK. Чтобы выполнить следующие процедуры, откройте решение **CommerceRuntimeSamples.sln** в папке **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Найдите проект **Runtime.Extensions.DocumentProvider.PosnetSample** и постройте его.
2. В папке **Runtime.Extensions.DocumentProvider.PosnetSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. Скопируйте этот файл сборки в папку расширения CRT:

    - **Commerce Scale Unit:** скопируйте файл в папку **\\bin\\ext** в местоположении сайта Internet Information Services (IIS) Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** скопируйте файл в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Перезапустите службу Commerce:

    - **Commerce Scale Unit:** перезапустите сайт службы Commerce из диспетчера IIS.
    - **Брокер клиента:** завершите процесс **dllhost.exe** в диспетчере задач, затем перезапустите Modern POS.

### <a name="hardware-station-extension-components"></a>Компоненты расширения Hardware Station

Компоненты расширения Hardware Station включены в Retail SDK. Чтобы выполнить следующие процедуры, откройте решение **HardwareStationSamples.sln** в папке **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Найдите проект **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** и выполните его сборку.
2. В папке **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. Скопируйте файл сборки на развернутый компьютер Hardware Station:

    - **Удаленная Hardware Station:** скопируйте файл в папку **bin** в местоположении сайта IIS Hardware Station. Скопируйте библиотеки драйверов принтера (**libposcmbth.dll**, **libcmbth\_serial.dll** и **cmbth\_pl.lng**).

4. Найдите файл конфигурации для расширений Hardware Station. Файл называется **HardwareStation.Extension.config**:

    - **Удаленная Hardware Station:** файл находится в местоположении сайта IIS Hardware Station.

5. Добавьте следующую строку в раздел **composition** файла конфигурации.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Перезапустите службу Hardware Station:

    - **Удаленная Hardware Station:** перезапустите сайт Hardware Station из диспетчера IIS.

## <a name="production-environment"></a>Рабочая среда

В предыдущей процедуре вы включили расширения, которые являются компонентами примера интеграции службы финансовой регистрации. Кроме того, вы должны выполнить следующие дополнительные шаги, чтобы создать развертываемые пакеты, содержащие компоненты Commerce, и применить эти пакеты в производственной среде.

1. Выполните следующие изменения в файлах конфигурации пакетов в папке **RetailSdk\\Assets**:

    - В файлах конфигурации **commerceruntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - В файле конфигурации **HardwareStation.Extension.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Внесите следующие изменения в файл конфигурации настройки пакета **Customization.settings** в папке **BuildTools**:

    - Добавьте следующую строку, чтобы включить расширение CRT в развертываемые пакеты.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Добавьте следующую строку, чтобы включить расширение Hardware Station в развертываемые пакеты.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Запустите утилиту командной строки MSBuild для Visual Studio и запустите **msbuild** в папке Retail SDK, чтобы создать развертываемые пакеты.
1. Примените пакеты через LCS или вручную. Дополнительные сведения см. в разделе [Создание развертываемых пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Разработка расширений

Образец интеграции финансового принтера для Польши базируется на [функции финансовой интеграции](fiscal-integration-for-retail-channel.md). Дополнительные сведения о разработке решения финансовой интеграции см. в разделе [Обзор разработки примера финансовой интеграции](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Разработка расширения Commerce Runtime

Целью расширения, которое является поставщиком финансовых документов, является создание документов для конкретного принтера и обработка откликов от финансового принтера.

Расширение CRT — это **Runtime.Extensions.DocumentProvider.PosnetSample**. Это расширение создает набор связанных с принтером команд в формате JavaScript Object Notation (JSON), который определяется спецификацией POSNET 19-3678.

Дополнительную информацию о разработке решения финансовой интеграции см. в разделе [Примеры процесса финансовой регистрации и финансовой интеграции для финансовых устройств и служб](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **DocumentProviderPosnetProtocol** является точкой входа для запроса на создание документов с финансового принтера.

Обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени поставщика документа соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **GetFiscalDocumentDocumentProviderRequest** — этот запрос содержит сведения о том, что должен создаваться документ. Он возвращает специфический для принтера документ, который должен быть зарегистрирован в финансовом принтере.
- **GetSupportedRegistrableEventsDocumentProviderRequest** — этот запрос возвращает список событий, на которые необходимо подписаться. В настоящее время поддерживаются следующие события: продажи, печать X-отчета и печать Z-отчета.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **Configuration** проекта расширения. Целью этого файла является разрешение настройки для параметров поставщика фискального документа из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- Сопоставление ставок НДС
- Сопоставление типов платежных средств
- Типа платежа депозита

### <a name="hardware-station-extension-design"></a>Разработка расширения Hardware Station

Целью расширения, которое является финансовым соединителем, является обмен данными с финансовым принтером.

Расширение Hardware Station — это **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Это расширение вызывает функции драйвера POSNET для отправки команд, которые расширение CRT создает на финансовом принтере. Оно также обрабатывает ошибки устройства.

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **FiscalPrinterHandler** является точкой входа для обработки запроса к финансовому периферийному устройству.

Обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени финансового соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **SubmitDocumentFiscalDeviceRequest** — этот запрос отправляет документы на принтеры и возвращает отклики из финансового принтера.
- **IsReadyFiscalDeviceRequest** — этот запрос используется для проверки работоспособности устройства.
- **InitializeFiscalDeviceRequest** — этот запрос используется для инициализации принтера.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **Configuration** проекта расширения. Целью файла является разрешение настройки для параметров соединителя из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- **Строка подключения** — строка, описывающая сведения о соединении с устройством в формате, поддерживаемом драйвером. Дополнительные сведения см. в документации по драйверу POSNET.
- **Синхронизация даты и времени** — значение, указывающее, должны ли дата и время принтера быть синхронизированы с подключенной аппаратной станцией Hardware Station.
- **Время ожидания устройства** — период времени в миллисекундах, в течение которого драйвер будет ожидать отклика от устройства. Дополнительные сведения см. в документации по драйверу POSNET.
