---
title: Домены в Dynamics 365 Commerce
description: В этом разделе описывается, как обрабатываются домены в Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 84becee12363ca38951ff13073d87d1b1f14b616
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765009"
---
# <a name="domains-in-dynamics-365-commerce"></a>Домены в Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

В этом разделе описывается, как обрабатываются домены в Microsoft Dynamics 365 Commerce.

Домены — это веб-адреса, используемые для перехода к сайтам Dynamics 365 Commerce в веб-браузере. Управление доменом можно контролировать с помощью выбранного поставщика сервера доменных имен DNS (Domain Name Server). Домены упоминаются в сборщике сайтов Dynamics 365 Commerce для координации того, как при публикации будет осуществляться доступ к сайту. В этом разделе рассматриваются способы обработки и использования доменов в жизненном цикле разработки и запуска веб-сайта Commerce.

## <a name="provisioning-and-supported-host-names"></a>Подготовка и поддерживаемые имена узлов

При подготовке среды электронной коммерции в [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) поле **Поддерживаемые имена узлов** на экране подготовки электронной коммерции служит для ввода доменов, которые будут связаны с развернутой средой Commerce. Эти домены являются предназначенными для клиентов именами серверов доменных имен DNS, на которых будут размещаться веб-сайты электронной коммерции. Ввод домена на этом этапе не запускает передачу трафика для этого домена в Dynamics 365 Commerce. Трафик для домена будет перенаправлен в конечную точку Commerce при обновлении DNS-записи CNAME для использования конечной точки Commerce с этим доменом.

> [!NOTE]
> В поле **Поддерживаемые имена узлов** можно ввести несколько доменов, разделяя их точкой с запятой.

На следующем рисунке показан экран LCS подготовки электронной коммерции с выделенным полем **Поддерживаемые имена узлов**. 

![Экран LCS подготовки электронной коммерции с выделенным полем **Поддерживаемые имена узлов**](./media/Domains_ProvisioningeCommerceScreen.png)

Если подготовка уже выполнена, можно создать запрос на обслуживание для добавления дополнительных доменов в среду. Чтобы создать запрос на обслуживание в LCS, в вашей среде перейдите к пункту **Поддержка \> Проблемы поддержки** и выберите **Отправить инцидент**.

## <a name="commerce-generated-urls"></a>Создаваемые Commerce URL-адреса

При подготовке среды электронной коммерции в Commerce создается URL-адрес, который будет использоваться в качестве рабочего адреса для среды. Ссылка на этот URL-адрес содержится в ссылке сайта электронной коммерции, указанной в LCS после подготовки среды. Генерируемый Commerce URL-адрес указывается в формате `https://<e-Commerce tenant name>.commerce.dynamics.com`, где название клиента электронной коммерции является именем, введенным в LCS для среды Commerce.

Можно также использовать имена узлов производственного сайта в среде "песочницы". Этот вариант идеально подходит для копирования сайта из среды "песочницы" в производственную среду.

## <a name="site-setup"></a>Настройка сайта

После подготовки среды электронной коммерции необходимо настроить сайт в конфигураторе сайта Commerce, чтобы связать сайт с работающим URL-адресом.

При первой настройке сайта в конфигураторе сайтов появится диалоговое окно **Настройка сайта**.

На следующем рисунке показано диалоговое окно **Настройка сайта** для сайта с именем "по умолчанию" при первом обращении к сайту в конструкторе сайтов.

![Диалоговое окно **Настройка сайта**](./media/Domains_SetupyoursiteScreen.png)

Поле **Выберите домен** позволяет сопоставить одно из поддерживаемых имен узла, предоставленных для вашего сайта в LCS, сайту в конструкторе сайтов.

Поле **Путь** можно оставить пустым или добавить дополнительную строку пути, которая будет отражена в рабочем URL-адресе. Если поле **Путь** не заполнено, созданный в Commerce базовый URL-адрес связывается с сайтом, настраиваемым в конструкторе сайтов. Пути для каждой пары сайт-домен должны быть уникальными. В выбранном сайте и домене только один сайт в среде может использовать пустой путь или быть связанным с уникальной строкой пути. Любая строка, добавляемая к полю **Путь** во время настройки сайта, становится подпутем к создаваемому в Commerce базовому URL-адресу, используемому для доступа к сайту в веб-браузере.

> [!NOTE]
> Этот путь известен также как **Путь соответствия** при добавлении канала в раздел конфигурации **Параметры сайта \> Каналы** в конструкторе сайтов.

Например, если в конструкторе сайтов имеется сайт под названием "fabrikam" в клиенте электронной коммерции с именем "xyz", и если сайт настроен с пустым путем, то можно получить доступ к опубликованному содержимому сайта в веб-браузере, перейдя непосредственно по созданному в Commerce базовому URL-адресу:

`https://xyz.commerce.dynamics.com`

Кроме того, если в настройку этого сайта был добавлен путь "fabrikam", то к опубликованному содержимому сайта можно получить доступ в веб-браузере, используя следующий URL-адрес:

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Страницы и URL-адреса

После того как сайт настроен с помощью пути, все URL-адреса, связанные со страницами в конструкторе сайтов, будут построены на рабочем URL-адресе (созданный в Commerce URL-адрес или созданный в Commerce URL-адрес плюс путь) для сайта. При создании нового URL-адреса в конструкторе сайтов (**URL-адреса /> +Создать**) путем выбора страницы из списка в диалоговом окне **Создание URL-адреса** и ввода URL-пути для этой страницы будет связан этот URL-адрес с выбранной страницей. Значение URL-пути затем добавляется к рабочему URL-адресу сайта для доступа к странице и помечается как `./<URL path>` в списке URL-адресов страницы **URL-адреса** в конструкторе сайтов.

На следующем рисунке показано диалоговое окно **Создание URL-адреса** в конструкторе сайтов с выбранным примером URL-пути. 

![Диалоговое окно **Создание URL-адреса** в конструкторе сайтов](./media/Domains_PageSetup2a.png)

На следующем рисунке показана страница **URL-адреса** в конструкторе сайтов с выбранным примером URL-адреса в списке.

![Параметр выполнения потока пользователей в потоке политик](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Домены в конструкторе сайтов

Поддерживаемые значения имен узлов можно связать в качестве домена при настройке сайта. При выборе поддерживаемого значения имени узла в качестве домена вы увидите выбранный домен, указанный в конструкторе сайтов. Этот домен представляет собой только ссылку в среде Commerce, настоящий трафик для этого домена еще не будет переадресован в Dynamics 365 Commerce.

Если при работе с сайтами в конструкторе сайтов имеются два сайта с настроенными двумя разными доменами, можно добавить атрибут **?domain=** к рабочему URL-адресу, чтобы получить доступ к опубликованному содержимому сайта в браузере.

Например, была подготовлена среда "xyz", и в конструкторе сайтов были созданы два сайта: один с доменом `www.fabrikam.com`, а другой — с доменом `www.constoso.com`. Каждый сайт был настроен с использованием пустого пути. В этом случае в веб-браузере можно будет получить доступ к этим двум сайтам, используя атрибут **?domain=**:
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Если строка запроса домена не указана в среде с несколькими доменами, в Commerce используется первый предоставленный домен. Например, если путь "fabrikam" был указан первым во время настройки сайта, URL-адрес `https://xyz.commerce.dynamics.com` может быть использован для доступа к опубликованному контенту сайта `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Пересылка трафика в производственной среде

Можно смоделировать несколько доменов, используя параметры строки запроса домена для самой конечной точки commerce.dynamics.com. Но если необходимо перейти к эксплуатации в производстве, необходимо переадресовать трафик для пользовательского домена на конечную точку `<e-Commerce tenant name>.commerce.dynamics.com`.

Конечная точка `<e-Commerce tenant name>.commerce.dynamics.com` не поддерживает пользовательские домены SSL, поэтому необходимо настроить пользовательские домены с помощью службы точки входа или сети доставки содержимого (CDN). 

Для настройки пользовательских доменов с помощью службы точки входа или сети CDN существует две возможности:

- Настройте службу точки входа, например, Azure Front Door для обработки клиентского трафика и подключения к среде Commerce. Это обеспечивает больший контроль над доменом и управлением сертификатами и более детализированные политики безопасности.
- Используйте экземпляр Azure Front Door, поставляемый в Commerce. Для этого требуется координирование действий с рабочей группой Dynamics 365 Commerce для проверки доменов и получения сертификатов SSL для производственного домена.

Сведения о непосредственной настройке службы CDN см. в разделе [Добавление поддержки сети доставки содержимого (CDN)](add-cdn-support.md).

Чтобы использовать экземпляр службы Azure Front Door, поставляемый Commerce, необходимо создать запрос на обслуживание для помощи в настройке CDN со стороны рабочей группы с помощью команды подключения Commerce. 

- Необходимо указать название компании, производственный домен, идентификатор среды и наименование производственного клиента электронной коммерции. 
- Необходимо подтвердить, что это существующий домен (используемый для активного в данный момент сайта) или новый домен. 
- Для нового домена проверка домена и SSL-сертификат могут быть выполнены за один шаг. 
- Для домена, обслуживающего существующий веб-сайт, существует многошаговый процесс, необходимый для выполнения проверки домена и получения SSL-сертификата. Этот процесс имеет соглашение об уровне обслуживания (SLA) на 7 рабочих дней для ввода домена в действие, поскольку он включает несколько последовательных шагов.

Чтобы создать запрос на обслуживание в LCS, в вашей среде перейдите к пункту **Поддержка \> Проблемы поддержки** и выберите **Отправить инцидент**.

> [!NOTE]
> Пользовательские домены с SSL поддерживаются только в производственных средах. Для непроизводственных сред, таких как "песочница" и пользовательское приемочное тестирование (UAT), используйте созданный Commerce URL-адрес для доступа к опубликованному содержимому в веб-браузере.

## <a name="ssl-certificate-process"></a>Процесс получения SSL-сертификата

Когда подается запрос на обслуживание, рабочая группа Commerce будет координировать следующие шаги с вами.

Для новых доменов:
- Рабочая группа Commerce настроит экземпляр службы Azure Front Door (размещаемый в Commerce).
- Затем рабочая группа Commerce предоставит запись CNAME для указания вашего пользовательского домена.
- После обновления записи CNAME экземпляр службы Azure Front Door, размещенный в Commerce, сможет проверить владельца домена и получить сертификат SSL.

Для существующих или активных доменов:
- Рабочая группа Commerce поможет вам добавить запись CNAME `afdverify.<custom-domain>` для предоставления поставщику DNS вашего домена.
- По завершении рабочая группа Commerce добавит домен в экземпляр службы Azure Front Door и предоставит дополнительные записи DNS TXT для добавления в DNS для этого домена.
- После заполнения записей TXT рабочая группа Commerce выполнит обновления службы Azure Front Door для домена, в результате чего будет настроен SSL-сертификат.

## <a name="apex-domains"></a>Вершинные домены

Предоставленный Commerce экземпляр службы Azure Front Door не поддерживает вершинные домены Апекс (корневые домены, не содержащие вложенных доменов). Вершинным доменам требуется IP-адрес для разрешения, а экземпляр Commerce службы Azure Front Door существует только с виртуальными конечными точками. Для использования вершинного домена имеются две возможности:

- **Вариант 1** — используйте поставщика DNS для перенаправления вершинного домена в домен "www". Например, fabrikam.com перенаправляет на `www.fabrikam.com`, где `www.fabrikam.com` — это запись CNAME, указывающая на экземпляр Azure Front Door, размещенной в Commerce.

- **Вариант 2** — настройте свой собственный экземпляр CDN/точки входа для размещения вершинного домена.

> [!NOTE]
> Если используется служба Azure Front Door, необходимо также настроить DNS-сервер Azure в этой же подписке. Вершинный домен, размещенный в Azure DNS, может указывать на службу Azure Front Door в качестве записи-псевдонима. Это единственный обходной путь, так как вершинные домены должны всегда указывать на IP-адрес.

  ## <a name="additional-resources"></a>Дополнительные ресурсы

  [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md)

  [Настройка канала интернет-магазина](online-stores.md)

  [Создание сайта электронной коммерции](create-ecommerce-site.md)

  [Связывание веб-сайта с каналом](associate-site-online-store.md)

  [Управление файлами robots.txt](manage-robots-txt-files.md)

  [Пакетная отправка перенаправлений URL-адресов](upload-bulk-redirects.md)

  [Настройка клиента B2C в Commerce](set-up-B2C-tenant.md)

  [Настройка специальных страниц для входа пользователей](custom-pages-user-logins.md)

  [Настройка нескольких клиентов B2C в среде Commerce](configure-multi-B2C-tenants.md)

  [Добавление поддержки сети доставки контента (CDN)](add-cdn-support.md)

  [Включение обнаружения магазинов на основе местоположения](enable-store-detection.md)