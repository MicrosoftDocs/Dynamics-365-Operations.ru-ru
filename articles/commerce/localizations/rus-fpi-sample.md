---
title: Пример интеграции фискальных принтеров для России
description: В этой теме представлен обзор примера финансовой интеграции для России в Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
manager: annbe
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2021-8-2
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c004b5d7c4355d12e148bd1b0686b49738974887
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076950"
---
# <a name="fiscal-printer-integration-sample-for-russia"></a>Пример интеграции фискальных принтеров для России

[!include [banner](../includes/banner.md)]

В этой теме представлен обзор примера финансовой интеграции для России в Microsoft Dynamics 365 Commerce.

Функции Dynamics 365 Commerce для России включают в себя пример интеграции POS с финансовым принтером. Этот пример расширяет [возможности финансовой интеграции](fiscal-integration-for-retail-channel.md) и поддерживает API финансовых принтеров от [АТОЛ](http://integration.atol.ru/). В нем включается связь с фискальным принтером, подключенным через порт (COM), с помощью собственного программного драйвера. Пример представлен в форме исходного кода и является частью пакета SDK Retail.

Корпорация Майкрософт не выпускает никакое оборудование, программное обеспечение или документацию из АТОЛ. Для получения сведений о получении и работе финансового принтера обратитесь в [АТОЛ](https://www.atol.ru/).

> [!NOTE]
> Пример кода предназначен для использования с определенным программным обеспечением для контрольно-кассовой машины от АТОЛ, третьей стороны. Вы несете ответственность за использование услуг АТОЛ, и любое применение регулируется отдельным [соглашением с конечным пользователем](http://integration.atol.ru/eula/) между вами и АТОЛ. Важно понимать, что АТОЛ может иметь стандарты обработки данных, соответствия требованиям и безопасности, отличные от стандартов Dynamics 365 Commerce. Мы заботимся о конфиденциальности ваших данных. Чтобы получить дополнительные сведения, ознакомьтесь с нашим [заявлением о конфиденциальности](https://go.microsoft.com/fwlink/?LinkId=521839).

Дополнительные сведения о функциях Commerce, доступных для клиентов в России, см. в разделе [Локализация Commerce для России](rus-commerce-localization.md).

## <a name="scenarios"></a>Сценарии

Пример интеграции финансового принтера для России покрывает следующие сценарии.

### <a name="sales-scenarios"></a>Сценарии продаж

- Печать финансового чека для продаж и возвратов с кассовыми проводками.
- Фиксация отклика от финансового принтера и хранение его в базе данных канала.
- Налоги:

    - Сопоставление ставок налогов с типами налога финансового принтера.
    - Перенос сопоставленных налоговых данных в финансовый принтер.

- Платежи:

    - Сопоставление способов оплаты магазина с типами платежей финансового принтера.
    - Печать платежей на финансовом чеке.
    - Печать сведений об изменениях.

- Печать сведений о скидке по строке.
- Отправка сведений о клиенте, указанного для проводки по продажам, вместе с финансовым чеком. Примером такой информации является адрес электронной почты клиента. Дополнительные сведения см. в разделе [Управление сведениями о клиентах для России](rus-customer-information.md).

### <a name="daily-reports"></a>Ежедневные отчеты

- Финансовые X- и Z-отчеты.

### <a name="error-handling"></a>Обработка ошибок

- Если возможно, повторите попытку выполнения финансовой регистрации в тех случаях, когда финансовый принтер не подключен, не готов или не отвечает, принтер не имеет бумаги или в нем застряла бумага.
- Откладывание финансовой регистрации.
- Пропустите финансовую регистрацию или пометьте проводку как зарегистрированную и включите коды сведений для фиксации причины сбоя и дополнительной информации.
- Проверка доступности финансового принтера до открытия новой проводки по продажам или завершения проводки по продажам.

## <a name="limitations-of-the-sample"></a>Ограничения примера

- Финансовый принтер поддерживает только ситуации, в которых налог включается в цену. Поэтому параметр **Цена включает налог** должен быть установлен в значение **Да** как для магазинов, так и для клиентов.
- Финансовые чеки в настоящее время не могут быть распечатаны для операций с заказами клиентов (например, депозит, самовывоз или отгрузка). Однако поддержка операций с заказами клиентов может быть добавлена в более поздних версиях.
- Финансовые чеки не могут в настоящее время быть распечатаны для кассовых операций с наличными средствами (например, декларирование платежных средств, внесение денежных средств или удаление платежного средства). Однако поддержка кассовых операций с наличными средствами может быть добавлена в более поздних версиях.
- Ежедневные отчеты (фискальные X и фискальные Z) печатаются с использованием внедренного формата фискального принтера.
- Фискальный принтер не поддерживает смешанные проводки. Параметр **Запретить смешивание продаж и возвратов в одной приходной накладной** должен иметь значение **Да** в профилях функциональности POS.

## <a name="default-data-mapping"></a>Сопоставление данных по умолчанию

Следующее сопоставление данных по умолчанию включено в конфигурацию поставщика фискальных документов, которая предоставляется в составе образца финансовой интеграции:

- Сопоставление способов оплаты:

    ```json
    {
        "PaymentMethods": [
            {"StorePaymentMethod":"1", "AtolPaymentType":0},
            {"StorePaymentMethod":"2", "AtolPaymentType":4},
            {"StorePaymentMethod":"3", "AtolPaymentType":1},
            {"StorePaymentMethod":"4", "AtolPaymentType":3},
            {"StorePaymentMethod":"5", "AtolPaymentType":0},
            {"StorePaymentMethod":"6", "AtolPaymentType":0},
            {"StorePaymentMethod":"7", "AtolPaymentType":4},
            {"StorePaymentMethod":"8", "AtolPaymentType":4},
            {"StorePaymentMethod":"10", "AtolPaymentType":4},
            {"StorePaymentMethod":"11", "AtolPaymentType":4}
        ]
    }
    ```

    Сопоставление метода платежа по умолчанию основано на конфигурации метода платежа магазина в демонстрационных данных. Возможно, потребуется изменить сопоставление в функциональном профиле соединителя на основе настроек способов оплаты для ваших магазинов. Дополнительные сведения о типах платежей, которые поддерживают финансовые принтеры АТОЛ, см. в [документации по интеграции АТОЛ](http://integration.atol.ru/).

## <a name="set-up-fiscal-integration-for-russia"></a>Настройка финансовой интеграции для России

Дополнительные сведения об общих параметрах Commerce для России см. в разделе [Настройка локализации Commerce для России](rus-commerce-setup.md).

Чтобы настроить финансовую интеграцию для России, выполните шаги настройки финансовой регистрации, которые описаны в разделе [Настройка финансовой интеграции для каналов Commerce](./setting-up-fiscal-integration-for-retail-channel.md).

1. [Настройте процесс финансовой регистрации](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Обязательно запишите настройки процесса финансовой регистрации, которые [относятся к России](#configure-the-fiscal-registration-process).
1. [Задайте параметры обработки ошибок](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Настройте финансовые отчеты X/Z на POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Включите выполнение вручную отложенной финансовой регистрации](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Настройте функции для управления сведениями о клиентах в POS-терминале](rus-customer-information.md#setup).
1. [Настройте компоненты каналов](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Настройка процесса финансовой регистрации

Чтобы включить процесс финансовой регистрации для России в Commerce Headquarters, выполните следующие действия.

1. Загрузите файлы конфигурации для поставщика фискальных документов и финансового соединителя из пакета Commerce SDK:

    1. Откройте репозиторий [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Откройте последнюю доступную ветвь выпуска (например, **[release/9.31](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.31)**).
    1. Откройте **src \> FiscalIntegration \> AtolFiscalPrinterSample**.
    1. Загрузите файл конфигурации финансового соединителя по пути **HardwareStation \> Connector.AtolSample \> ConfigurationTemplate \> ConnectorAtolSample.xml** (например, [файл для release/9.31](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.31/src/FiscalIntegration/AtolFiscalPrinterSample/HardwareStation/Connector.AtolSample/ConfigurationTemplate/ConnectorAtolSample.xml)).
    1. Загрузите файл конфигурации поставщика финансовых документов по пути **CommerceRuntime \> DocumentProvider.AtolSample \> ConfigurationTemplate \> DocumentProviderAtolSample.xml** (например, [файл для release/9.31](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.31/src/FiscalIntegration/AtolFiscalPrinterSample/CommerceRuntime/DocumentProvider.AtolSample/ConfigurationTemplate/DocumentProviderAtolSample.xml)).

1. Перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Общие параметры**. На вкладке **Общие** задайте для параметра **Включить финансовую интеграцию** значение **Да**.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Финансовые соединители** и загрузите ранее скаченный файл конфигурации финансового соединителя.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Поставщики финансовых документов** и загрузите ранее скаченный файл конфигурации поставщика финансовых документов.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Функциональные профили соединителей**. Создайте новый функциональный профиль соединителя и выберите поставщика документов и соединитель, которые были загружены ранее. При необходимости обновите параметры сопоставления данных.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Технические профили соединителей**. Создайте новый технический профиль соединителя и выберите соединитель, который был загружен ранее. Задайте тип соединителя **Внутренний**. При необходимости обновите другие параметры соединителя.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Группы финансовых соединителей** и создайте новую группу фискальных соединителей для функционального профиля соединителя, который был создан ранее.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Финансовая интеграция \> Процессы финансовой регистрации**. Создайте новый процесс финансовой регистрации, создайте шаг процесса финансовой регистрации и выберите созданную ранее группу фискальных соединителей.
1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка POS \> Профили POS \> Профили функциональности**. Открывает профиль функциональности, связанный с магазином, в котором должен быть активирован процесс регистрации. На экспресс-вкладке **Процесс финансовой регистрации** выберите ранее созданный процесс регистрации.
1. Перейдите **Retail и Commerce \> Настройка канала \> Настройка POS \> Профили POS \> Профили оборудования**. Откройте профиль оборудования, который связан с Commerce Hardware Station, с которой будет связан фискальный принтер. На экспресс-вкладке **Фискальная периферия** выберите технический профиль соединителя.
1. Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**. Откройте график распределения и выберите задания **1070** и **1090** для передачи данных в базу данных канала.

### <a name="configure-channel-components"></a>Настройка компонентов канала

Пример интеграции финансового принтера для России является частью пакета Retail SDK. Пример находится в папке **src\\FiscalIntegration\\AtolFiscalPrinterSample** репозитория [Решения Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (например, [пример в выпуске release/9.31](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.31/src/FiscalIntegration/AtolFiscalPrinterSample)). Пример [состоит](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) из поставщика финансового документа, который является расширением среды выполнения Commerce Runtime (CRT), и финансового соединителя, который является расширением Commerce Hardware Station. Для получения дополнительных сведений о способах использования пакета Retail SDK см. разделы [Архитектура пакета Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) и [Настройка конвейера сборки для пакета SDK независимой упаковки](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Вследствие ограничений [новой модели независимой упаковки и расширения](../dev-itpro/build-pipeline.md), она не может использоваться для этого образца финансовой интеграции. Необходимо использовать предыдущую версию пакета Retail SDK на виртуальной машине (ВМ) разработчика в Microsoft Dynamics Lifecycle Services (LCS). В следующих разделах описывается, как использовать предыдущую версию пакета Retail SDK для включения примера.

#### <a name="adjust-package-sources-in-nugetconfig"></a>Настройка источников пакетов в nuget.config

1. Откройте файл **RetailSDK\\src\\nuget.config**.
1. Добавьте следующую строку в конец раздела **packageSources**.

    ``` xml
    <add key="dynamics365-commerce" value="https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json" />
    ```        

#### <a name="copy-sample-files-to-retail-sdk"></a>Копирование файлов примера в пакет Retail SDK

1. Для вспомогательных файлов:

    1. Скопируйте файл **repo.props** из **Dynamics365Commerce.Solutions** в папку **RetailSDK\\src\\SampleExtensions**.
    1. Скопируйте файл **CustomizationPackage.props** из **Dynamics365Commerce.Solutions\\src\\FiscalIntegration\\AtolFiscalPrinterSample** в папку **RetailSDK\\src\\SampleExtensions**.
    1. Откройте файл **CustomizationPackage.props** и найдите следующую строку:

        ``` xml
        <Import Project="..\..\..\repo.props" />
        ```

        Замените ее на следующую строку.

        ``` xml
        <Import Project="repo.props" />
        ```

1. Для файлов расширения CRT: скопируйте папку **DocumentProvider.AtolSample** из **Dynamics365Commerce.Solutions\\src\\FiscalIntegration\\AtolFiscalPrinterSample\\CommerceRuntime** в папку **RetailSDK\\src\\SampleExtensions\\CommerceRuntime**.
1. Для файлов расширения Hardware Station: скопируйте папку **Connector.AtolSample** из **Dynamics365Commerce.Solutions\\src\\FiscalIntegration\\AtolFiscalPrinterSample\\HardwareStation** в папку **RetailSDK\\src\\SampleExtensions\\HardwareStation**.

#### <a name="include-extension-projects-in-solutions"></a>Включение проектов расширений в решения

1. Для решения CRT:

    1. В папке **RetailSDK\\src\\SampleExtensions\\CommerceRuntime** найдите решение **CommerceRuntimeSamples.sln** и откройте его.
    1. Добавьте проект **DocumentProvider.AtolSample.csproj**, расположенный в папке **RetailSDK\\src\\SampleExtensions\\CommerceRuntime\\DocumentProvider.AtolSample**.

1. Для решения Hardware Station:

    1. В папке **RetailSDK\\src\\SampleExtensions\\HardwareStation** найдите решение **HardwareStationSamples.sln** и откройте его.
    1. Добавьте проект **Connector.AtolSample.csproj**, расположенный в папке **RetailSDK\\src\\SampleExtensions\\HardwareStation\\Connector.AtolSample**.

#### <a name="adjust-extension-projects"></a>Настройка проектов расширений

1. Для проекта расширения CRT:

    1. В папке **RetailSDK\\src\\SampleExtensions\\CommerceRuntime\\DocumentProvider.AtolSample** найдите файл **DocumentProvider.AtolSample.csproj** и откройте его как текстовый файл.
    1. Добавьте следующие строки в начало раздела **Project**.

        ``` xml
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.props" />
        <Import Project="..\..\..\BuildTools\Common.props" />
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.settings" />
        ```

    1. Добавьте следующую строку в конец раздела **Project**.

        ``` xml
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.targets" />
        ```

1. Для проекта расширения Hardware Station:

    1. В папке **RetailSDK\\src\\SampleExtensions\\HardwareStation\\Connector.AtolSample** найдите файл **Connector.AtolSample.csproj** и откройте его как текстовый файл.
    1. Добавьте следующие строки в начало раздела **Project**.

        ``` xml
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.props" />
        <Import Project="..\..\..\BuildTools\Common.props" />
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.settings" />
        ```

    1. Добавьте следующую строку в конец раздела **Project**.

        ``` xml
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.targets" />
        ```

#### <a name="build-extension-projects"></a>Сборка проектов расширений

1. Для компонентов расширения CRT:

    1. В папке **RetailSDK\\src\\SampleExtensions\\CommerceRuntime** найдите решение **CommerceRuntimeSamples.sln** и откройте его.
    1. Найдите проект **DocumentProvider.AtolSample** и выполните его сборку.
    1. В папке **DocumentProvider.AtolSample\\bin\\Debug** найдите файл сборки **Contoso.CommerceRuntime.DocumentProvider.AtolSample.dll**.
    1. Скопируйте этот файл сборки в папку расширения CRT:

        - **Commerce Scale Unit:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта Microsoft Internet Information Services (IIS) Commerce Scale Unit.
        - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

    1. Найдите файл конфигурации расширения для CRT:

        - **Commerce Scale Unit:** файл называется **commerceruntime.ext.config**, он находится в папке bin\\ext в местоположении сайта IIS Commerce Scale Unit.
        - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

    1. Зарегистрируйте изменение CRT в файле конфигурации расширения. Добавьте **source="assembly" value="Contoso.CommerceRuntime.DocumentProvider.AtolSample"**.
    1. Перезапустите Commerce Scale Unit:

        - **Commerce Scale Unit:** перезапустите сайт Commerce Scale Unit из диспетчера IIS.
        - **Брокер клиента:** завершите процесс **dllhost.exe** в диспетчере задач, затем перезапустите Modern POS.

1. Для компонентов расширения Hardware Station:

    1. В папке **RetailSDK\\src\\SampleExtensions\\HardwareStation** найдите решение **HardwareStationSamples.sln** и откройте его.
    1. Найдите проект **Connector.AtolSample** и выполните его сборку.
    1. В папке **Connector.AtolSample\\bin\\Debug** найдите файл сборки **Contoso.HardwareStation.Connector.AtolSample.dll**.
    1. Скопируйте файл сборки на развернутый компьютер Hardware Station:

        - **Удаленная Hardware Station:** скопируйте файл в папку **bin** в местоположении сайта IIS Hardware Station.
        - **Локальная Hardware Station:** скопируйте файл в местоположение брокера клиента Modern POS.

    1. Найдите файл конфигурации расширения для Hardware Station. Файл называется **HardwareStation.Extension.config**.

        - **Удаленная Hardware Station:** файл находится в местоположении сайта IIS Hardware Station.
        - **Локальная Hardware Station:** файл находится в местоположении брокера клиента Modern POS.

    1. В файле конфигурации добавьте следующий раздел в раздел **composition**.

        ```xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample" />
        ```

    1. Перезапустите службу Hardware Station:

        - **Удаленная Hardware Station:** перезапустите сайт Hardware Station из диспетчера IIS.
        - **Локальная Hardware Station:** завершите процесс **dllhost.exe** в диспетчере задач, затем перезапустите Modern POS.

#### <a name="install-the-fiscal-printer-driver"></a>Установка драйвера финансового принтера

Установите драйвер финансового принтера на компьютер Hardware Station. Подробные указания см. в документации изготовителя.

> [!NOTE]
> Если используется 64-разрядный драйвер, установите для параметра **Разрешены 32-разрядные приложения** значение **False** для пула приложений Hardware Station в диспетчере IIS. Если используется 32-разрядный драйвер, установите для параметра **Разрешены 32-разрядные приложения** значение **True**.

#### <a name="production-environment"></a>Рабочая среда

Выполните следующие дополнительные шаги, чтобы создать развертываемые пакеты, содержащие компоненты Commerce, и примените эти пакеты в производственной среде.

1. Выполните следующие изменения в файлах конфигурации пакетов в папке **RetailSdk\\Assets**:

    - В файлах конфигурации **commerceruntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.CommerceRuntime.DocumentProvider.AtolSample" />
        ```

    - В файле конфигурации **HardwareStation.Extension.config** добавьте следующую строку в раздел **composition**.

        ``` xml
        <add source="assembly" value="Contoso.HardwareStation.Connector.AtolSample" />
        ```

1. Внесите следующие изменения в файл конфигурации настройки пакета **Customization.settings** в папке **BuildTools**:

    - Добавьте следующую строку, чтобы включить расширения CRT в развертываемые пакеты.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.CommerceRuntime.DocumentProvider.AtolSample.dll" />
        ```

    - Добавьте следующую строку, чтобы включить расширение Hardware Station в развертываемые пакеты.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.HardwareStation.Connector.AtolSample.dll" />
        ```

1. Запустите утилиту командной строки MSBuild для Visual Studio и запустите **msbuild** в папке Retail SDK, чтобы создать развертываемые пакеты.
1. Примените пакеты через LCS или вручную. Дополнительные сведения см. в разделе [Создание развертываемых пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор финансовой интеграции для каналов Commerce](fiscal-integration-for-retail-channel.md)

[Локализация Commerce для России](rus-commerce-localization.md)

[Управление информацией по клиентам для России](rus-customer-information.md)

[Настройка локализации Commerce для России](rus-commerce-setup.md)

[Настройка финансовой интеграции для каналов Commerce](./setting-up-fiscal-integration-for-retail-channel.md)

[Архитектура Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)

[Настройка конвейера сборки для пакета SDK независимой упаковки](../dev-itpro/build-pipeline.md)

[Создание готовых к развертыванию пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md)
