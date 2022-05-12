---
title: Рекомендации по развертыванию образца интеграции финансового принтера для Италии (устаревшая версия)
description: В этой теме приводятся указания по развертыванию примера интеграции финансового принтера для Италии, относящегося к пакету разработки программного обеспечения Retail SDK Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 617e97272fb4bd7cea0958958ae99648bb847b56
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614077"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Рекомендации по развертыванию образца интеграции финансового принтера для Италии (устаревшая версия)

[!include[banner](../includes/banner.md)]

В этой теме приводятся рекомендации по развертыванию образца интеграции финансового принтера для Италии из пакета Retail SDK Microsoft Dynamics 365 Commerce на виртуальной машине разработчика в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения об этом примере финансовой интеграции см. в разделе [Пример интеграции финансового принтера для Италии](emea-ita-fpi-sample.md). 

Пример финансовой интеграции для Италии является частью пакета Retail SDK. Сведения о том, как установить и использовать этот пакет SDK см. в разделе [Архитектура комплекта средств разработки программного обеспечения (SDK) для Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Этот пример состоит из расширений Commerce Runtime (CRT) и Hardware Station. Для работы с этим примером необходимо изменить и построить проекты CRT и Hardware Station. Для внесения изменений, описанных в этой теме, рекомендуется использовать немодифицированный пакет Retail SDK. Кроме того, рекомендуется использовать систему управления версиями, такую как Azure DevOps, в которой никакие файлы еще не были изменены.

## <a name="development-environment"></a>Среда разработки

Выполните эти шаги для настройки среды разработки, чтобы можно было проверить и расширить пример.

### <a name="commerce-runtime-extension-components"></a>Компоненты расширения Commerce Runtime

Компоненты расширения CRT включены в Retail SDK. Чтобы выполнить следующие процедуры, откройте решение **CommerceRuntimeSamples.sln** в папке **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Найдите проект **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** и постройте его.
2. В папке **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Commerce Scale Unit:** скопируйте файл в папку **\\bin\\ext** в местоположении сайта Internet Information Services (IIS) Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** скопируйте файл в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Перезапустите Commerce Scale Unit:

    - **Commerce Scale Unit:** перезапустите сайт Commerce Scale Unit из диспетчера IIS.
    - **Брокер клиента:** завершите процесс **dllhost.exe** в диспетчере задач, затем перезапустите Modern POS.

### <a name="hardware-station-extension-components"></a>Компоненты расширения Hardware Station

Компоненты расширения Hardware Station включены в Retail SDK. Чтобы выполнить следующие процедуры, откройте решение **HardwareStationSamples.sln** в папке **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Найдите проект **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** и постройте его.
2. В папке **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. Скопируйте файл сборки на развернутый компьютер Hardware Station:

    - **Удаленная Hardware Station:** скопируйте файл в папку **bin** в местоположении сайта IIS Hardware Station.
    - **Локальная Hardware Station:** скопируйте файл в местоположение брокера клиента Modern POS.

4. Найдите файл конфигурации для расширений Hardware Station. Файл называется **HardwareStation.Extension.config**:

    - **Удаленная Hardware Station:** файл находится в местоположении сайта IIS Hardware Station.
    - **Локальная Hardware Station:** файл находится в местоположении брокера клиента Modern POS.

5. Добавьте следующий раздел в раздел **composition** файла конфигурации.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Перезапустите службу Hardware Station:

    - **Удаленная Hardware Station:** перезапустите сайт Hardware Station из диспетчера IIS.
    - **Локальная Hardware Station:** завершите процесс **dllhost.exe** в диспетчере задач, затем перезапустите Modern POS.

## <a name="production-environment"></a>Рабочая среда

Чтобы создать развертываемые пакеты, содержащие компоненты Commerce, и применить эти пакеты в производственной среде, выполните следующие действия.

1. Выполните шаги, описанные в разделе [Среда разработки](#development-environment) ранее в этой теме.
2. Выполните следующие изменения в файлах конфигурации пакетов в папке **RetailSdk\\Assets**:

    1. В файлах конфигурации **commerceruntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. В файле конфигурации **HardwareStation.Extension.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Внесите следующие изменения в файл конфигурации настройки пакета **Customization.settings** в папке **BuildTools**:

    1. Добавьте следующую строку, чтобы включить расширение CRT в развертываемые пакеты.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Добавьте следующую строку, чтобы включить расширение Hardware Station в развертываемые пакеты.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Выполните следующие изменения в файле **Sdk.ModernPos.Shared.csproj** в папке **Packages\_SharedPackagingProjectComponents**, чтобы включить файлы ресурсов для Италии в развертываемые пакеты:

    1. Добавьте раздел **ItemGroup**, содержащий узлы, указывающие на файлы ресурсов для нужных переводов. Убедитесь, что указаны правильные пространства имен и образцы имен. В следующем примере добавляются узлы ресурсов для языков **it** и **it-CH**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. В разделе **Target Name="CopyPackageFiles"** добавьте по одной строке для каждого языкового стандарта, как показано в следующем примере.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Выполните следующие изменения в файле **Sdk.RetailServerSetup.proj** в папке **Packages\_SharedPackagingProjectComponents**, чтобы включить файлы ресурсов для Италии в развертываемые пакеты:

    1. Добавьте раздел **ItemGroup**, содержащий узлы, указывающие на файлы ресурсов для нужных переводов. Убедитесь, что указаны правильные пространства имен и образцы имен. В следующем примере добавляются узлы ресурсов для языков **it** и **it-CH**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. В разделе **Target Name="CopyPackageFiles"** добавьте по одной строке для каждого языкового стандарта, как показано в следующем примере.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Запустите утилиту командной строки MSBuild для Visual Studio и затем запустите **msbuild** в папке Retail SDK, чтобы создать развертываемые пакеты.
7. Примените пакеты через LCS или вручную. Дополнительные сведения см. в разделе [Создание развертываемых пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Разработка расширений

### <a name="commerce-runtime-extension-design"></a>Разработка расширения Commerce Runtime

Целью расширения, которое является поставщиком финансовых документов, является создание документов для конкретного принтера и обработка откликов от финансового принтера.

Расширение CRT — это **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Дополнительную информацию о разработке решения финансовой интеграции см. в разделе [Примеры процесса финансовой регистрации и финансовой интеграции для финансовых устройств и служб](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **DocumentProviderEpsonFP90III** является точкой входа для запроса на создание документов с финансового принтера.

Обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени поставщика документа соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **GetFiscalDocumentDocumentProviderRequest** — этот запрос содержит сведения о том, что должен создаваться документ. Он возвращает специфический для принтера документ, который должен быть зарегистрирован в финансовом принтере.
- **GetSupportedRegistrableEventsDocumentProviderRequest** — этот запрос возвращает список событий, на которые необходимо подписаться. В настоящее время поддерживаются следующие события: продажи, печать X-отчета и печать Z-отчета.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **Configuration** проекта расширения. Целью этого файла является разрешение настройки для параметров поставщика фискального документа из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- Сопоставление кодов НДС
- Сопоставление ставок НДС
- Сопоставление типов платежных средств
- Тип штрих-кода для номера чека
- Типа платежа депозита

### <a name="hardware-station-extension-design"></a>Разработка расширения Hardware Station

Целью расширения, которое является финансовым соединителем, является обмен данными с финансовым принтером.

Расширение Hardware Station — это **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Это расширение использует протокол HTTP для отправки документов, создаваемых расширением CRT, на финансовый принтер. Оно также обрабатывает отклики, полученные от финансового принтера.

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **EpsonFP90IIISample** является точкой входа для обработки запросов к финансовому периферийному устройству.

Обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени финансового соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **SubmitDocumentFiscalDeviceRequest** — этот запрос отправляет документы на принтеры и возвращает отклики из финансового принтера.
- **IsReadyFiscalDeviceRequest** — этот запрос используется для проверки работоспособности устройства.
- **InitializeFiscalDeviceRequest** — этот запрос используется для инициализации принтера.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **Configuration** проекта расширения. Целью файла является разрешение настройки для параметров соединителя из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- **Адрес конечной точки** — URL-адрес принтера.
- **Синхронизация даты и времени** — значение, указывающее, должны ли дата и время принтера быть синхронизированы с подключенной аппаратной станцией Hardware Station.
