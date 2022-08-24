---
ms.openlocfilehash: a20971ac9a44c409363bbce6cd8b8343f16d800f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274214"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Инструкции по развертыванию для примера интеграции блока управления для Швеции (устарело)
---

title: Инструкции по развертыванию для примера интеграции блока управления для Швеции (устарело) [!include [banner](../includes/banner.md)]
description: В этой статье приводятся рекомендации по развертыванию образца интеграции блока управления для Швеции из пакета SDK Retail

автор: EvgenyPopovMBS В этой статье приводятся рекомендации по развертыванию образца интеграции блока управления для Швеции из пакета Retail SDK на виртуальной машине разработчика в Microsoft Dynamics Lifecycle Services (LCS). Дополнительные сведения об этом примере финансовой интеграции см. в разделе [Пример интеграции блока управления для Швеции](emea-swe-fi-sample.md). ms.date: 20/12/2021

ms.topic: article Пример финансовой интеграции для Швеции является частью пакета SDK Retail. Сведения о том, как установить и использовать этот пакет SDK см. в разделе [Архитектура комплекта средств разработки программного обеспечения (SDK) для Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Этот пример состоит из расширений Commerce Runtime (CRT), Hardware Station и POS-терминала. Для работы с этим примером необходимо изменить и построить проекты CRT, Hardware Station и POS. Для внесения изменений, описанных в этой статье, рекомендуется использовать немодифицированный пакет Retail SDK. Кроме того, рекомендуется использовать систему управления версиями, такую как Azure DevOps, в которой никакие файлы еще не были изменены.
audience: пользователь приложения, разработчик, ИТ-профессионал

ms.reviewer: v-chgriffin
## <a name="development-environment"></a>Среда разработки
ms.search.region: Глобальный

ms.author: josaw Выполните эти действия для настройки среды разработки, чтобы можно было проверить и расширить образец.
ms.search.validFrom: 2019-03-01

### <a name="enable-crt-extensions"></a>Включение расширений CRT
---


Компоненты расширения CRT включены в образцы CRT. Чтобы выполнить следующие процедуры, откройте решение **CommerceRuntimeSamples.sln** в папке **RetailSdk\\SampleExtensions\\CommerceRuntime**.
2. Включите текущий пример расширения Hardware Station, добавив следующую строку в раздел **composition** в файле конфигурации **HardwareStation.Extension.config**.


#### <a name="documentprovidercleancashsample-component"></a>Компонент DocumentProvider.CleanCashSample
    ``` xml

    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
1. Найдите проект **Runtime.Extensions.DocumentProvider.CleanCashSample** и постройте его.
    ```
2. In the **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** assembly file.

3. Copy the assembly file to the CRT extensions folder:
3. Make the following changes in the **Customization.settings** package customization configuration file under the **BuildTools** folder:


    - **Commerce Scale Unit:** Copy the file to the **\\bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.
    - Remove the following line to exclude the earlier Hardware station extension from deployable packages.
    - **Local CRT on Modern POS:** Copy the file to the **\\ext** folder under the local CRT client broker location.


        ``` xml
4. Find the extension configuration file for CRT:
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />

        ```
    - **Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.

    - **Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.
    - Add the following lines to include the current sample Hardware station extension in deployable packages.


5. Register the CRT change in the extension configuration file.
        ``` xml

        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
    ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        ```
    ```


#### <a name="update-modern-pos"></a>Обновление Modern POS
#### <a name="extension-configuration-file"></a>Файл конфигурации расширения


1. Откройте решение **CloudPOS.sln** в **RetailSdk\\POS**.
1. Найдите файл конфигурации расширения для CRT:
2. Отключите предыдущее расширение POS-терминала:


    - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - В файле **tsconfig.json** добавьте папку **FiscalRegisterSample** в список исключений.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.
    - Удалите следующие строки из файла **extensions.json** в папке **RetailSDK\\POS\\Extensions**.


2. Зарегистрируйте изменение CRT в файле конфигурации расширения.
        ``` json

        {
    ``` xml
            "baseUrl": "FiscalRegisterSample"
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        }
    ```
        ```


### <a name="enable-hardware-station-extensions"></a>Включение расширения Hardware Station
3. Включите текущий пример расширения POS, добавив следующие строки в файл **extensions.json** в папке **RetailSDK\\POS\\Extensions**.


Компоненты расширения Hardware Station включены в образцы Hardware Station. Чтобы выполнить следующие процедуры, откройте решение **HardwareStationSamples.sln** в папке **RetailSdk\\SampleExtensions\\HardwareStation**.
    ``` json

    {
#### <a name="cleancash-component"></a>Компонент CleanCash
        "extensionPackages": [

            {
1. Найдите проект **HardwareStation.Extension.CleanCashSample** и выполните его сборку.
                "baseUrl": "Microsoft/AuditEvent.SE"
2. В папке **Extension.CleanCashSample\\bin\\Debug** найдите файлы сборки **Contoso.Commerce.HardwareStation.CleanCashSample.dll** и **Interop.CleanCash\_1\_1.dll**.
            }
3. Скопируйте файлы сборки в папку расширений Hardware Station:      ]

    }
    - **Общая Hardware Station:** скопируйте файлы в папку **bin** в местоположении сайта IIS Hardware Station.
    ```
    - **Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.


#### Update Cloud POS
4. Find the extension configuration file for the Hardware station's extensions. The file is named **HardwareStation.Extension.config**.


1. Open the **ModernPOS.sln** solution under **RetailSdk\\POS**.
    - **Shared hardware station:** The file is under the IIS Hardware station site location.
2. Disable the earlier POS extension:
    - **Dedicated hardware station on Modern POS:** The file is under the Modern POS client broker location.


    - In the **tsconfig.json** file, add the **FiscalRegisterSample** folder to the exclude list.
5. Add the following line to the **composition** section of the configuration file.
    - Remove the following lines from the **extensions.json** file under the **RetailSDK\\POS\\Extensions** folder.


    ``` xml
        ``` json
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        {
    ```
            "baseUrl": "FiscalRegisterSample"

        }
### <a name="enable-modern-pos-extension-components"></a>Включение компонентов расширения Modern POS
        ```


1. Откройте решение **ModernPOS.sln** в **RetailSdk\\POS** и убедитесь, что оно может быть скомпилировано без ошибок. Кроме того, убедитесь, что вы можете запустить Modern POS из Visual Studio, используя команду **Выполнить**.
3. Включите текущий пример расширения POS, добавив следующие строки в файл **extensions.json** в папке **RetailSDK\\POS\\Extensions**.


    > [!NOTE]
    ``` json
    > Modern POS must not be customized. You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.
    {

        "extensionPackages": [
2. Enable the extensions that must be loaded by adding the following lines in the **extensions.json** file.
            {

                "baseUrl": "Microsoft/AuditEvent.SE"
    ``` json
            }
    {
        ]
        "extensionPackages": [
    }
            {
    ```
                "baseUrl": "Microsoft/AuditEvent.SE"

            }
#### <a name="create-deployable-packages"></a>Создание готовых к развертыванию пакетов
        ]

    }
Выполните **msbuild** для всего пакета Retail SDK для создания развертываемых пакетов. Примените пакеты через LCS или вручную. Дополнительные сведения см. в разделе [Упаковка пакета Retail SDK](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
    ```

    > [!NOTE]
    > For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.

3. Заново постройте решение.
4. Выполните Modern POS в отладчике и проверьте работу функций.

### <a name="enable-cloud-pos-extension-components"></a>Включение компонентов расширения Cloud POS

1. Откройте решение **CloudPOS.sln** в **RetailSdk\\POS** и убедитесь, что оно может быть скомпилировано без ошибок.
2. Разрешите расширения, которые должны быть загружены, добавив следующие строки в файл **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Дополнительные сведения, а также примеры, демонстрирующие включение папок исходного кода и разрешение загрузки расширений, см. в инструкциях в файле readme.md в проекте **Pos.Extensions**.

3. Заново постройте решение.
4. Выполните решение с помощью команды **Выполнить** и выполните шаги в руководству пакета Retail SDK.

## <a name="production-environment"></a>Рабочая среда

Предыдущая процедура включает расширения, которые являются компонентами образца интеграции блока управления. Кроме того, вы должны выполнить следующие дополнительные шаги, чтобы создать развертываемые пакеты, содержащие компоненты Commerce, и применить эти пакеты в производственной среде.

1. Выполните следующие изменения в файлах конфигурации пакетов в папке **RetailSdk\\Assets**:

    - В файлах конфигурации **commerceruntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** добавьте следующие строки в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - В файле конфигурации **HardwareStation.Extension.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Внесите следующие изменения в файл конфигурации настройки пакета **Customization.settings** в папке **BuildTools**:

    - Добавьте следующую строку, чтобы включить расширения CRT в развертываемые пакеты.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Добавьте следующие строки, чтобы включить расширение Hardware Station в развертываемые пакеты.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Включите расширение POS, добавив следующие строки в файл **extensions.json** в папке **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Запустите утилиту командной строки MSBuild для Visual Studio и запустите **msbuild** в папке Retail SDK, чтобы создать развертываемые пакеты.
5. Примените пакеты через LCS или вручную. Дополнительные сведения см. в разделе [Создание развертываемых пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Выполните все необходимые задачи настройки, описанные в разделе [Настройка интеграции с блоками управления](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Разработка расширений

### <a name="crt-extension-design"></a>Разработка расширения CRT

Целью расширения, которое является поставщиком финансовых документов, является создание документов для конкретной службы и обработка откликов от блока управления.

Расширение CRT — это **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Дополнительную информацию о разработке решения финансовой интеграции см. в разделе [Примеры процесса финансовой регистрации и финансовой интеграции для финансовых устройств и служб](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Обработчик запросов

Имеется один обработчик запросов **DocumentProviderCleanCash** для поставщика документов. Этот обработчик используется для создания финансовых документов для блока управления.

Этот обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени поставщика документа соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **GetFiscalDocumentDocumentProviderRequest** — этот запрос содержит сведения о том, что должен создаваться документ. Он возвращает специфический для службы документ, который должен быть зарегистрирован в блоке управления.
- **GetSupportedRegistrableEventsDocumentProviderRequest** — этот запрос возвращает список событий, на которые необходимо подписаться. В настоящее время поддерживаются события продаж и аудита.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации **DocumentProviderFiscalCleanCashSample** находится в папке **Configuration** проекта расширения. Целью этого файла является разрешение настройки для параметров поставщика фискального документа из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- Сопоставление кодов НДС

### <a name="hardware-station-extension-design"></a>Разработка расширения Hardware Station

Целью расширения, которое является финансовым соединителем, является обмен данными с блоком управления.

Расширение Hardware Station — это **HardwareStation.Extension.CleanCashSample**. Оно использует протокол HTTP для отправки документов, создаваемых расширением CRT в блоке управления. Оно также обрабатывает отклики, полученные от блока управления.

#### <a name="request-handler"></a>Обработчик запросов

Обработчик запросов **CleanCashHandler** является точкой входа для обработки запросов к блоку управления.

Обработчик наследуется из интерфейса **INamedRequestHandler**. Метод **HandlerName** отвечает за возврат имени обработчика. Имя обработчика должно соответствовать имени финансового соединителя, указанного в Commerce Headquarters.

Соединитель поддерживает следующие запросы:

- **SubmitDocumentFiscalDeviceRequest** — этот запрос отправляет документы в блок управления и возвращает из него отклики.
- **IsReadyFiscalDeviceRequest** — этот запрос используется для проверки работоспособности блока управления.
- **InitializeFiscalDeviceRequest** — этот запрос используется для инициализации блока управления.

#### <a name="configuration"></a>Конфигурация

Файл конфигурации находится в папке **Configuration** проекта расширения. Целью файла является разрешение настройки для параметров финансового соединителя из Commerce Headquarters. Формат файла сопоставляется с требованиями к настройке финансовой интеграции. Добавлены следующие параметры:

- **Строка подключений** — параметры подключения блока управления.
- **Время ожидания** — период времени в миллисекундах, в течение которого драйвер будет ожидать отклика от блока управления.

## <a name="migrating-from-the-earlier-integration-sample"></a>Переход с более раннего примера интеграции

Если вы используете более раннюю версию [примера для интеграции POS с блоками управления для Швеции](retail-sdk-control-unit-sample.md), возможно, придется выполнить миграцию из этого примера в текущий пример интеграции. Для переоценки изменения и получения своевременных обновлений для функций для Швеции в будущем, возможно, придется выполнить обновление, внести незначительные изменения в код и настройки конфигурации в создаваемом расширении и перестроить решения. В созданной логике расширения не требуются значительные изменения. Образец более ранней интеграции и настройки будут продолжать работать, если со стороны пользователя изменения не выполняются. Таким образом, можно планировать, подготавливать и выполнять обновление для вашей среды.

### <a name="migration-process"></a>Процесс миграции

Миграция из предыдущего примера интеграции в текущий образец интеграции блока управления должна основываться на концепции постепенного обновления. Другими словами, все компоненты Commerce Headquarters и Commerce Scale Unit должны быть уже обновлены до начала обновления компонентов POS-терминала и Hardware Station.

Чтобы предотвратить ситуацию, когда событие или транзакция подписаны дважды (то есть они подписаны как предыдущим расширением, так и текущим расширением), или когда событие или транзакция не могут быть подписаны из-за отсутствия конфигурации, рекомендуется отключить все устройства POS и Hardware Station, использующие предыдущий образец, а затем обновить их одновременно. Такое одновременное обновление можно выполнить, например, по очереди для магазинов, обновив профиль функциональности магазина и профиль оборудования Hardware Station.

Процесс миграции должен состоять из следующих шагов.

1. Обновите компоненты Commerce Headquarters.
1. Обновите компоненты Commerce Scale Unit и включите расширения текущего образца.
1. Убедитесь, что все автономные транзакции синхронизированы с устройствами MPOS, поддерживающими работу в автономном режиме.
1. Отключите все устройства, которые используют компоненты предыдущего образца.
1. Выполните все необходимые задачи настройки, описанные в разделе [Настройка интеграции с блоками управления](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Обновите компоненты POS-терминала и Hardware Station, отключите расширения, которые являются частями более раннего образца, и включите расширения текущего образца.

    > [!NOTE]
    > В зависимости от типа среды более подробную техническую информацию о процессе миграции можно найти в разделе [Миграция в среде разработки](#migration-in-a-development-environment) или [Миграция в производственной среде](#migration-in-a-production-environment) данной статьи.

### <a name="migration-in-a-development-environment"></a>Миграция в среде разработки

#### <a name="update-crt"></a>Обновить CRT

1. Найдите проект **Runtime.Extensions.DocumentProvider.CleanCashSample** и постройте его.
2. В папке **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Commerce Scale Unit:** скопируйте файл в папку **\\bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** скопируйте файл в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Commerce Scale Unit:** файл называется **CommerceRuntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Commerce Scale Unit.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в папке **bin\\ext** в местоположении локального брокера клиента CRT.

    > [!WARNING]
    > **Не** изменяйте файлы CommerceRuntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

5. Найдите и удалите предыдущее расширение CRT из файла конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Не выполняйте этот шаг до тех пор, пока не будут обновлены все POS-устройства, которые работают с этим экземпляром CRT.

6. Зарегистрируйте текущие примеры расширения CRT в файле конфигурации расширения, добавив следующие строки:

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Обновление станции оборудования Hardware Station

1. Найдите проект **HardwareStation.Extension.CleanCashSample** и выполните его сборку.
2. В папке **Extension.CleanCashSample\\bin\\Debug** найдите файлы сборки **Contoso.Commerce.HardwareStation.CleanCashSample.dll** и **Interop.CleanCash\_1\_1.dll**.
3. Скопируйте файлы сборки в папку расширений Hardware Station.

    - **Общая Hardware Station:** скопируйте файлы в папку **bin** в местоположении сайта IIS Hardware Station.
    - **Выделенная Hardware Station в Modern POS:** скопируйте файлы в местоположение брокера клиента Modern POS.

4. Найдите файл конфигурации расширения **HardwareStation.Extension.config**:

    - **Удаленная Hardware Station:** файл находится в местоположении сайта IIS Hardware Station.
    - **Локальная Hardware Station в Modern POS:** файл находится в местоположении брокера клиента Modern POS.

    > [!WARNING]
    > **Не** изменяйте файлы CommerceRuntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

5. Найдите и удалите предыдущее расширение Hardware Station из файла конфигурации расширения.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 и более ранней версии](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 или более новая версия](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 или более новая версия](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Добавьте следующую строку в раздел **composition** файла конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Обновление Modern POS

1. Откройте решение **CloudPOS.sln** в разделе **RetailSdk\\POS**.
2. Отключите более раннее расширение POS-терминала, удалив следующие строки из файла **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Разрешите текущий пример расширения POS, добавив следующие строки в файл **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Обновление Cloud POS

1. Откройте решение **ModernPOS.sln** в разделе **RetailSdk\\POS**.
2. Отключите более раннее расширение POS-терминала, удалив следующие строки из файла **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Разрешите текущий пример расширения POS, добавив следующие строки в файл **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Миграция в производственной среде

#### <a name="update-crt"></a>Обновить CRT

1. Удалите предыдущее расширение CRT из файлов конфигурации **CommerceRuntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** в папке **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Не выполняйте этот шаг до тех пор, пока не будут обновлены все POS-устройства, которые работают с этим экземпляром CRT.

2. Включите текущий пример расширений CRT, внеся следующие изменения в файлы конфигурации **CommerceRuntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** в папке **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. В файле конфигурации настройки пакета **Customization.settings** в папке **BuildTools** добавьте следующую строку, чтобы включить текущий пример расширения CRT в развертываемые пакеты.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Обновление станции оборудования Hardware Station

1. Удалите предыдущее расширение Hardware Station, изменив файл конфигурации **HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 и более ранней версии](#tab/retail-7-3)

    Удалите следующий раздел из файлов конфигурации **HardwareStation.Shared.config** и **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 или более новая версия](#tab/retail-7-3-1)

    Удалите следующий раздел из файла конфигурации **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 или более новая версия](#tab/retail-10-0)

    Удалите следующий раздел из файла конфигурации **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---
