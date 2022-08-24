---
ms.openlocfilehash: b17bd56f9f3e4def341658626915adbd7f5aada6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281547"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Рекомендации по развертыванию контрольно-кассовых машин для Норвегии (устарело)
---

title: Рекомендации по развертыванию контрольно-кассовых машин для Норвегии (устарело) [!include [banner](../includes/banner.md)]
description: В этой статье представлено руководство по развертыванию, в котором показано, как включить локализацию Microsoft Dynamics 365 Commerce для Норвегии.

author: EvgenyPopovMBS В этой статье представлено руководство по развертыванию, в котором показано, как включить локализацию Microsoft Dynamics 365 Commerce для Норвегии. Локализация состоит из нескольких расширений компонентов Commerce. Например, расширения позволяют печатать настраиваемые поля в чеках, регистрировать дополнительные события аудита, проводки по продажам и платежные проводки в POS-терминале, использовать цифровую подпись для проводок по продажам и печатать X и Z отчеты в локальных форматах. Дополнительные сведения о локализации для Норвегии см. в разделе [Функциональность контрольно-кассовой машины для Норвегии](./emea-nor-cash-registers.md).
ms.date: 20/12/2021

ms.topic: article Данный пример является частью пакета SDK Retail для розничной торговли. Сведения об этом SDK см. в разделе [Архитектура комплекта средств разработки программного обеспечения (SDK) для Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md).
audience: пользователь приложения, разработчик, ИТ-профессионал

ms.reviewer: v-chgriffin Этот пример состоит из расширений для Commerce Runtime (CRT), Retail Server и POS. Для работы с этим примером необходимо изменить и построить проекты CRT, Retail Server и POS. Для внесения изменений, описанных в этой статье, рекомендуется использовать немодифицированный пакет Retail SDK. Кроме того, рекомендуется использовать систему управления версиями, такую как Microsoft Visual Studio Online (VSO), в которой никакие файлы еще не были изменены.
ms.search.region: Глобальный

ms.author: josaw
> [!NOTE]
ms.search.validFrom: 2018-02-28 В Commerce 10.0.8 и более поздних версиях Retail Server называется Commerce Scale Unit. Поскольку эта статья применима к нескольким предыдущим версиям приложения, в ней используется термин *Retail Server*.
>
---
> Некоторые шаги в процедурах, описанных в этой статье, отличаются в зависимости от используемой версии Commerce. Дополнительные сведения см. в разделе [Что нового и что изменилось в Dynamics 365 Retail](../get-started/whats-new.md).


6. Обновите файл конфигурации Retail Server. В файле **RetailSDK\\Packages\\RetailServer\\Code\\web.config** добавьте следующие строки в раздел **extensionComposition**.
### <a name="using-certificate-profiles-in-commerce-channels"></a>Использование профилей сертификатов в каналах Commerce


    ``` xml
В Commerce версий 10.0.15 или более поздних можно использовать функцию [Определенные пользователем профили сертификатов для розничных магазинов](./certificate-profiles-for-retail-stores.md), которые поддерживают отработку отказа в автономном режиме в случае недоступности Key Vault или Commerce Headquarters. Функция расширяет функцию [Управление секретами для каналов Retail](../dev-itpro/manage-secrets.md).
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />

    ```
Чтобы применить эту функцию в расширении CRT, выполните следующие действия.


7. Выполните **msbuild** для всего пакета Retail SDK для создания развертываемых пакетов.
1. Создайте новый проект расширения CRT (тип проекта библиотеки классов C#). Используйте образцы шаблонов из пакета Retail SDK (RetailSDK\SampleExtensions\CommerceRuntime).
8. Примените пакеты через Microsoft Dynamics Lifecycle Services (LCS) или вручную. Дополнительные сведения см. в разделе [Создание развертываемых пакетов](../dev-itpro/retail-sdk/retail-sdk-packaging.md).


2. Добавление пользовательского обработчика для CertificateSignatureServiceRequest в проекте SequentialSignatureRegister.
### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Включение цифровой подписи в автономном режиме для Modern POS


3. Для чтения секретного вызова, `GetUserDefinedSecretCertificateServiceRequest` с использованием конструктора с параметром profileId. Это приведет к запуску функции, работающей с параметрами из профилей сертификатов. На основании настроек сертификат будет извлечен из хранилища Azure Key Vault или с локального компьютера.
Чтобы включить цифровую подпись в автономном режиме для Modern POS, необходимо выполнить следующие действия после активации Modern POS на новом устройстве.


    ```csharp
1. Sign in to POS.
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
2. On the **Database connection status** page, make sure that the offline database is fully synchronized. When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);
3. Sign out of POS.

4. Wait a while for the offline database to be fully synchronized.
    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
5. Sign in to POS.
    ```
6. На странице **Состояние подключения к базе данных** убедитесь, что автономная база данных полностью синхронизирована. Когда значение поля **Ожидающие проводки в автономной базе данных** равно **0** (нулю), база данных полностью синхронизирована.

7. Перезапустите Modern POS.
4. После извлечения сертификата переходите к подписыванию данных.



5. Постройте проект расширения CRT.
[!INCLUDE[footer-include](../../includes/footer-banner.md)]

6. Скопируйте выходную библиотеку классов и вставьте ее в ...\RetailServer\webroot\bin\Ext для ручного тестирования.

7. В файле CommerceRuntime.Ext.config обновите раздел композиции расширений, используя сведения о пользовательской библиотеке.

## <a name="development-environment"></a>Среда разработки

Выполните следующие процедуры для настройки среды разработки, чтобы можно было проверить и расширить пример.

### <a name="the-crt-extension-components"></a>Компоненты расширения CRT

Компоненты расширения CRT включены в образцы CRT. Чтобы выполнить следующие процедуры, откройте решение CRT, **CommerceRuntimeSamples.sln**, в папке **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>Компонент ReceiptsNorway

1. Найдите проект **Runtime.Extensions.ReceiptsNorway** и постройте его.
2. В папке **Extensions.ReceiptsNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта Microsoft Internet Information Services (IIS) Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salespaymenttransext-component"></a>Компонент SalesPaymentTransExt

1. Найдите проект **Runtime.Extensions.SalesPaymentTransExt** и постройте его.
2. В папке **Extensions.SalesPaymentTransExt\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="xzreportsnorway-component"></a>Компонент XZReportsNorway

1. Найдите проект **Runtime.Extensions.XZReportsNorway** и постройте его.
2. В папке **Extensions.XZReportsNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.XZReportsNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

# <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>Образец компонента RegisterAuditEvent

1. Найдите проект **Runtime.Extensions.RegisterAuditEventSample** и постройте его.
2. В папке **Extensions.RegisterAuditEventSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignature-sample-component"></a>Образец компонента SalesTransactionSignature

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureSample** и постройте его.
2. Измените файл **App. config**, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж.
3. Постройте проект.
4. В папке **Extensions.SalesTransactionSignatureSample\\bin\\Debug** найдите следующие файлы:

    - Файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Файл конфигурации **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Скопируйте эти файлы в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

6. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

7. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

# <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>Образец компонента RegisterAuditEvent

1. Найдите проект **Runtime.Extensions.RegisterAuditEventSample** и постройте его.
2. В папке **Extensions.RegisterAuditEventSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignature-sample-component"></a>Образец компонента SalesTransactionSignature

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureSample** и постройте его.
2. Измените файл **App. config**, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж.
3. Постройте проект.
4. В папке **Extensions.SalesTransactionSignatureSample\\bin\\Debug** найдите следующие файлы:

    - Файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Файл конфигурации **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Скопируйте эти файлы в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

6. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

7. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignaturesamplemessages-component"></a>Компонент SalesTransactionSignatureSample.Messages

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureSample.Messages**.
2. В папке **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>Образец компонента RegisterAuditEvent

1. Найдите проект **Runtime.Extensions.RegisterAuditEventSample** и постройте его.
2. В папке **Extensions.RegisterAuditEventSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignature-sample-component"></a>Образец компонента SalesTransactionSignature

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureSample** и постройте его.
2. Измените файл **App. config**, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж.
3. Постройте проект.
4. В папке **Extensions.SalesTransactionSignatureSample\\bin\\Debug** найдите следующие файлы:

    - Файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Файл конфигурации **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Скопируйте эти файлы в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

6. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

7. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregistercontracts-component"></a>Компонент SequentialSignatureRegister.Contracts

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. В папке **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>Образец компонента RegisterAuditEvent

1. Найдите проект **Runtime.Extensions.RegisterAuditEventSample** и постройте его.
2. В папке **Extensions.RegisterAuditEventSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregister-component"></a>Компонент SequentialSignatureRegister

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister**.
2. Измените файл **App. config**, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж.
3. Постройте проект.
4. В папке **Extensions.SequentialSignatureRegister\\bin\\Debug** найдите следующие файлы:

    - Файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Файл конфигурации **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Скопируйте эти файлы в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

6. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

7. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignaturenorway-component"></a>Компонент SalesTransactionSignatureNorway

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureNorway** и постройте его.
2. В папке **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregistercontracts-component"></a>Компонент SequentialSignatureRegister.Contracts

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. В папке **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

#### <a name="salespaymenttransextnorway-component"></a>Компонент SalesPaymentTransExtNorway

1. Найдите проект **Runtime.Extensions.SalesPaymentTransExtNorway** и постройте его.
2. В папке **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>Компонент RegisterAuditEventNorway

1. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

2. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregister-component"></a>Компонент SequentialSignatureRegister

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister**.
2. Измените файл **App. config**, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж.
3. Постройте проект.
4. В папке **Extensions.SequentialSignatureRegister\\bin\\Debug** найдите следующие файлы:

    - Файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Файл конфигурации **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Скопируйте эти файлы в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

6. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

7. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignaturenorway-component"></a>Компонент SalesTransactionSignatureNorway

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureNorway** и постройте его.
2. В папке **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregistercontracts-component"></a>Компонент SequentialSignatureRegister.Contracts

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. В папке **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

#### <a name="salespaymenttransextnorway-component"></a>Компонент SalesPaymentTransExtNorway

1. Найдите проект **Runtime.Extensions.SalesPaymentTransExtNorway** и постройте его.
2. В папке **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>Компонент RegisterAuditEventNorway

1. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

2. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregister-component"></a>Компонент SequentialSignatureRegister

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister**.
2. Измените файл **App. config**, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж.
3. Постройте проект.
4. В папке **Extensions.SequentialSignatureRegister\\bin\\Debug** найдите следующие файлы:

    - Файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Файл конфигурации **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Скопируйте эти файлы в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

6. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

7. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="salestransactionsignaturenorway-component"></a>Компонент SalesTransactionSignatureNorway

1. Найдите проект **Runtime.Extensions.SalesTransactionSignatureNorway** и постройте его.
2. В папке **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

#### <a name="sequentialsignatureregistercontracts-component"></a>Компонент SequentialSignatureRegister.Contracts

1. Найдите проект **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. В папке **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

#### <a name="salespaymenttransextnorway-component"></a>Компонент SalesPaymentTransExtNorway

1. Найдите проект **Runtime.Extensions.SalesPaymentTransExtNorway** и постройте его.
2. В папке **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Скопируйте этот файл сборки в папку расширений CRT:

    - **Retail Server:** скопируйте сборку в папку **\\bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** скопируйте сборку в папку **\\ext** в местоположении локального брокера клиента CRT.

4. Найдите файл конфигурации расширения для CRT:

    - **Retail Server:** файл называется **commerceruntime.ext.config**, он находится в папке **bin\\ext** в местоположении сайта IIS Retail Server.
    - **Локальный CRT на Modern POS:** файл называется **CommerceRuntime.MPOSOffline.Ext.config** и находится в местоположении локального брокера клиента CRT.

5. Зарегистрируйте изменение CRT в файле конфигурации расширения.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Не** изменяйте файлы commerceruntime.config и CommerceRuntime.MPOSOffline.config. Эти файлы не предназначены для каких-либо настроек.

---

### <a name="the-retail-server-extension-components"></a>Компоненты расширения Retail Server

#### <a name="salestransactionsignature-retail-server-sample-component"></a>Образец компонента SalesTransactionSignature Retail Server

1. В папке **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** найдите проект **RetailServer.Extensions.SalesTransactionSignatureSample** и постройте его.
2. В папке **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** найдите файл сборки **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. Скопируйте этот файл сборки в папку расширений Retail Server.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    Эта папка является папкой **\\bin**, расположенной в местоположении сайта IIS Retail Server.

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    Эта папка является папкой **\\bin**, расположенной в местоположении сайта IIS Retail Server.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Эта папка является папкой **\\bin\\ext**, расположенной в местоположении сайта IIS Retail Server.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    Эта папка является папкой **\\bin\\ext**, расположенной в местоположении сайта IIS Retail Server.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    Эта папка является папкой **\\bin\\ext**, расположенной в местоположении сайта IIS Retail Server.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    Эта папка является папкой **\\bin\\ext**, расположенной в местоположении сайта IIS Retail Server.

    ---

4. Найдите файл конфигурации расширения для Retail Server. Файл называется **web.config**, он находится в корневой папке в местоположении сайта IIS Retail Server.
5. Зарегистрируйте расширения Retail Server в разделе **extensionComposition** файла конфигурации.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Зарегистрируйте зависимости расширений Retail Server.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4/)

    1. В папке **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** найдите следующие файлы:

        - Файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - Файл конфигурации **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. Скопируйте файлы в папку **\\bin**, расположенную в местоположении сайта IIS Retail Server.
    3. Зарегистрируйте изменение CRT в файле конфигурации расширения для CRT. Файл называется **commerceruntime.ext.config**, он находится в папке **bin** в местоположении сайта IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later/)

    1. В папке **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** найдите файл сборки **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. Скопируйте файл в папку **\\bin**, расположенную в местоположении сайта IIS Retail Server.
    3. Зарегистрируйте изменение CRT в файле конфигурации расширения для CRT. Файл называется **commerceruntime.ext.config**, он находится в папке **bin** в местоположении сайта IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Никакие действия не требуются.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    > [!NOTE]
    > Никакие действия не требуются.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    > [!NOTE]
    > Никакие действия не требуются.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    > [!NOTE]
    > Никакие действия не требуются.

    ---

### <a name="the-modern-pos-extension-components"></a>Компоненты расширения Modern POS

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Реализация кода прокси-сервера для автономного режима

Эта часть эквивалентна контроллеру Retail Server, но она расширяет локальный CRT, который используется, когда клиент не подключен.

1. В файле **customization.settings** измените раздел **@(RetailServerLibraryPathForProxyGeneration)** так, чтобы он использовал новую сборку Retail Server для создания прокси.
2. Реализуйте следующие методы интерфейса в классе **StoreOperationsManager**. Для первой итерации добавьте следующий код:

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    ---

3. Чтобы повторно создать код прокси-сервера, создайте папку **Proxies** из командной строки с помощью команды **msbuild /t:Rebuild**.
4. Разрешите зависимости проекта **Proxies.RetailProxy**:

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    Откройте **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, добавьте проект **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** в решение и добавьте ссылку на проект в проект **RetailProxy**, чтобы она ссылкалась на **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    Откройте **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, добавьте проект **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** в решение и добавьте ссылку на проект в проект **RetailProxy**, чтобы она ссылкалась на **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    ---

5. Настройте методы интерфейса в классе **StoreOperationsManager**:

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    > [!NOTE]
    > Этот шаг неприменим к данной версии.

    ---

6. Обновите файл **dllhost.exe.config**, чтобы клиентский брокер загрузил новую сборку RetailProxy.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Компонент расширения прокси-сервера Retail (Retail 7.3.1 и более поздней версии)

Выполните следующую процедуру только при использовании Retail 7.3.1 или более поздней версии.

1. В папке **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** найдите проект **RetailServer.Extensions.SalesTransactionSignatureSample** и постройте его.
2. В папке **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** найдите файл сборки **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. Скопируйте файлы сборки в папку **\\ext** в местоположении локального брокера клиента CRT.
4. Зарегистрируйте изменение прокси-сервера Retail в файле конфигурации расширения. Файл называется **RetailProxy.MPOSOffline.ext.config** и находится в местоположении локального брокера клиента CRT.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Компоненты расширения Modern POS

1. Откройте решение в **RetailSdk\\POS\\ModernPOS.sln** и убедитесь, что оно может быть скомпилировано без ошибок. Кроме того, убедитесь, что вы можете запустить Modern POS из Microsoft Visual Studio, используя команду **Выполнить**.

    > [!NOTE]
    > Modern POS не должен быть настроен. Необходимо включить контроль учетных записей (UAC) и, при необходимости, необходимо удалить ранее установленные экземпляры Modern POS.

2. Включите следующие существующие папки исходного кода в проект **Pos.Extensions**.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Разрешите компиляцию расширений в **tsconfig.json**, удалив из списка исключений следующие папки.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Разрешите загрузку расширений в файле **extensions.json**, добавив следующие строки в соответствующее место.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Дополнительные сведения, а также примеры, демонстрирующие включение папок исходного кода и разрешение загрузки расширений, см. в инструкциях в файле readme.md в проекте **Pos.Extensions**.

5. Заново постройте решение.
6. Выполните Modern POS в отладчике и проверьте работу функций.

### <a name="cloud-pos-extension-components"></a>Компоненты расширения Cloud POS

1. Откройте решение в **RetailSdk\\POS\\CloudPOS.sln** и убедитесь, что оно может быть скомпилировано без ошибок.
2. Включите следующие существующие папки исходного кода в проект **Pos.Extensions**.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Разрешите компиляцию расширений в **tsconfig.json**, удалив из списка исключений следующие папки.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Разрешите загрузку расширений в файле **extensions.json**, добавив следующие строки в соответствующее место.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Дополнительные сведения, а также примеры, демонстрирующие включение папок исходного кода и разрешение загрузки расширений, см. в инструкциях в файле readme.md в проекте **Pos.Extensions**.

5. Заново постройте решение.
6. Выполните решение с помощью команды **Выполнить** и выполните шаги в руководству пакета Retail SDK.
7. Проверьте функциональность.

### <a name="set-up-required-parameters-in-headquarters"></a>Настройка необходимых параметров в Headquarters

Дополнительные сведения см. в разделе [Функциональность контрольно-кассовой машины для Норвегии](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Рабочая среда

Выполните следующие шаги, чтобы создать развертываемые пакеты, содержащие компоненты Commerce, и примените эти пакеты в производственной среде.

1. Выполните шаги в разделе [Компоненты расширения Cloud POS](#cloud-pos-extension-components) или [Компоненты расширения Modern POS](#modern-pos-extension-components) ранее в этой статье.
2. Выполните следующие изменения в файлах конфигурации пакетов в папке **RetailSdk\\Assets**:

    1. В файлах конфигурации **commerceruntime.ext.config** и **CommerceRuntime.MPOSOffline.Ext.config** добавьте следующие строки в раздел **composition**:

        # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Включите настройку прокси-сервера Commerce:

        # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

        В файле конфигурации **dllhost.exe.config** добавьте следующие строки в подраздел **appSettings** раздела **configuration**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

        В файле конфигурации **dllhost.exe.config** добавьте следующие строки в подраздел **appSettings** раздела **configuration**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        В файле конфигурации **RetailProxy.MPOSOffline.ext.config** добавьте следующие строки в раздел **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

        В файле конфигурации **RetailProxy.MPOSOffline.ext.config** добавьте следующие строки в раздел **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

        В файле конфигурации **RetailProxy.MPOSOffline.ext.config** добавьте следующие строки в раздел **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

        В файле конфигурации **RetailProxy.MPOSOffline.ext.config** добавьте следующие строки в раздел **composition**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Внесите следующие изменения в файл конфигурации настройки пакета **Customization.settings**:

    1. Включите настройку прокси-сервера Retail/

        # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

        Добавьте следующие строки в раздел **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

        Добавьте следующие строки в раздел **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Добавьте следующие строки в раздел **ItemGroup**, чтобы включить расширение прокси-сервера Retail в развертываемые пакеты:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

        Добавьте следующие строки в раздел **ItemGroup**, чтобы включить расширение прокси-сервера Retail в развертываемые пакеты:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

        Добавьте следующие строки в раздел **ItemGroup**, чтобы включить расширение прокси-сервера Retail в развертываемые пакеты:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

        Добавьте следующие строки в раздел **ItemGroup**, чтобы включить расширение прокси-сервера Retail в развертываемые пакеты:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Добавьте следующие строки в раздел **ItemGroup**, чтобы включить расширения CRT в развертываемые пакеты:

        # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Добавьте следующие строки в раздел **ItemGroup**, чтобы включить расширение Retail Server в развертываемые пакеты:

        # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Измените следующие файлы, чтобы включить файлы ресурсов для Норвегии в развертываемые пакеты:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - Для файла **Sdk.ModernPos.Shared.csproj** 
    - Добавление строки в раздел **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Вместо <File_name> укажите имя файла ресурсов. То же самое применимо для других примеров, приведенных ниже.
 
    - Добавьте строку в раздел **Target Name="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Для файла **Sdk.RetailServerSetup.proj** 
    - Добавление строки в раздел **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Добавьте строку в раздел **Target Name="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Измените файл конфигурации сертификата, указав отпечаток, местоположение магазина и имя магазина для сертификата, который должен использоваться для подписи проводок продаж. Затем скопируйте файл конфигурации в папку **References**.

    # <a name="application-update-4"></a>[Обновление приложения 4](#tab/app-update-4)

    Файл имеет имя **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** и находится в папке **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Обновление приложения 5 и позднее](#tab/app-update-5-and-later)

    Файл имеет имя **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** и находится в папке **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Файл имеет имя **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** и находится в папке **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 или более новая версия](#tab/retail-7-3-2)

    Файл имеет имя **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** и находится в папке **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 или более новая версия](#tab/retail-7-3-5)

    Файл имеет имя **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** и находится в папке **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 или более новая версия](#tab/retail-8-1-1)

    Файл имеет имя **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** и находится в папке **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---
