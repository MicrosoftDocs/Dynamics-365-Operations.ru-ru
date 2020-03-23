---
title: Добавление поддержки сети доставки контента (CDN)
description: В этом разделе описывается, как добавить сеть доставки содержимого (CDN) в среду Microsoft Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001630"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Добавление поддержки сети доставки контента (CDN)


[!include [banner](includes/banner.md)]

В этом разделе описывается, как добавить сеть доставки содержимого (CDN) в среду Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

При настройке среды электронной коммерции в Dynamics 365 Commerce можно настроить ее для работы со службой CDN. 

Пользовательский домен может быть включен во время процесса подготовки к работе для среды электронной коммерции. Вместо этого можно использовать запрос на обслуживание, чтобы настроить его после завершения процесса подготовки. Процесс подготовки для среды электронной коммерции создает имя узла, связанное с данной средой. Имя этого узла имеет следующий формат, где *e-commerce-tenant-name* — это имя среды:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Имя узла или конечная точка, создаваемая в ходе процесса подготовки, поддерживает сертификат SSL только для \*commerce.dynamics.com. Оно не поддерживает SSL для пользовательских доменов. Поэтому необходимо завершить протокол SSL для пользовательских доменов в вашей сети CDN и передать трафик из CDN в имя хоста или конечную точку, созданную Commerce. 

Кроме того, *статические элементы* (файлы JavaScript или каскадных таблиц стилей \[CSS\]) из Commerce обслуживаются из конечной точки, созданной Commerce (\*.commerce.dynamics.com). Статические структуры могут кэшироваться только в том случае, если имя узла или конечной точки, которую создает Commerce, помещается позади сети CDN.

## <a name="set-up-ssl"></a>Настройка SSL

Чтобы гарантировать настройку SSL и правильность кэширования статических структур, необходимо настроить CDN так, чтобы он был связан с именем узла, созданным Commerce для вашей среды. Кроме того, необходимо кэшировать следующий шаблон только для статических структур: 

/\_msdyn365/\_scnr/\*

После подготовки вашей среды Commerce с предоставленным пользовательским доменом или после предоставления пользовательского домена для среды с помощью запроса на обслуживание направьте пользовательский домен на имя узла или конечную точку, которая была создана в Commerce.

Как уже упоминалось, созданное имя узла или конечная точка поддерживает сертификат SSL только для \*.commerce.dynamics.com. Оно не поддерживает SSL для пользовательских доменов.

## <a name="cdn-services"></a>Службы CDN

Со средой Commerce можно использовать любую службу CDN. Вот два примера:

- **Microsoft Azure Front Door Service** — решение Azure CDN. Дополнительные сведения о службе Azure Front Door Service см. в [документации по Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).
- **Ускоритель динамических сайтов Akamai** — для получения дополнительных сведений см. раздел [Ускоритель динамических сайтов](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>Настройка CDN

Процесс установки CDN состоит из следующих основных шагов:

1. Добавьте узел переднего плана.
1. Настройте серверный пул.
1. Настройте правила для маршрутизации и кэширования.

### <a name="add-a-front-end-host"></a>Добавление узла переднего плана

Можно использовать любую службу CDN, но для примера в этом разделе используется служба Azure Front Door Service. 

Сведения о настройке службы Azure Front Door Service см. в разделе [Краткое руководство: Создание службы Front Door для глобального веб-приложения с высокой доступностью](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Настройка серверного пула в службе Azure Front Door Service

Чтобы настроить серверный пул в службе Azure Front Door Service, выполните следующие действия.

1. Добавьте **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** в серверный пул в качестве пользовательского узла с пустым заголовком серверного узла.
1. В области **Зонды работоспособности** в поле **Путь** введите **/keepalive**.
1. В поле **Интервалы (с)** введите **255**.
1. В разделе **Балансировка нагрузки** оставьте значения по умолчанию.

На следующем рисунке показано диалоговое окно **Добавление серверного пула** в службе Azure Front Door Service.

![Диалоговое окно добавления серверного пула](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Настройка правил в службе Azure Front Door Service

Чтобы настроить правило маршрутизации в службе Azure Front Door Service, выполните следующие действия.

1. Добавьте правило маршрутизации.
1. В поле **Имя** введите **по умолчанию**.
1. В поле **Принятый протокол** выберите **HTTP и HTTPS**.
1. В поле **Интерфейсные узлы** введите **dynamics-ecom-tenant-name.azurefd.net**.
1. В области **Шаблоны для сопоставления** в верхнем поле введите **/\***.
1. В разделе **Сведения о маршруте** установите параметр **Тип маршрута** в значение **Прямой**.
1. В поле **Серверный пул** выберите **ecom-backend**.
1. В группе полей **Протокол переадресации** выберите параметр **Сопоставить запрос**. 
1. Установите для параметра **Перезапись URL** значение **Отключено**.
1. Установите для параметра **Кэширование** значение **Отключено**.

Чтобы настроить правило кэширования в службе Azure Front Door Service, выполните следующие действия.

1. Добавьте правило кэширования.
1. В поле **Имя** введите **статические**.
1. В поле **Принятый протокол** выберите **HTTP и HTTPS**.
1. В поле **Интерфейсные узлы** введите **dynamics-ecom-tenant-name.azurefd.net**.
1. В области **Шаблоны для сопоставления** в верхнем поле введите **/\_msdyn365/\_scnr/\***.
1. В разделе **Сведения о маршруте** установите параметр **Тип маршрута** в значение **Прямой**.
1. В поле **Серверный пул** выберите **ecom-backend**.
1. В группе полей **Протокол переадресации** выберите параметр **Сопоставить запрос**.
1. Установите для параметра **Перезапись URL** значение **Отключено**.
1. Установите для параметра **Кэширование** значение **Отключено**.
1. В поле поведение **Режим кэширования строк запросов** выберите **Кэшировать каждый уникальный URL-адрес**.
1. В группе полей **Динамическое сжатие** выберите **Включено**.

На следующем рисунке показано диалоговое окно **Добавление правила** в службе Azure Front Door Service.

![Диалоговое окно добавления правила](./media/CDN_CachingRule.png)

После развертывания первоначальной конфигурации необходимо добавить пользовательский домен в конфигурацию для службы Azure Front Door Service. Чтобы добавить пользовательский домен (например, `www.fabrikam.com`), необходимо настроить каноническое имя (CNAME) для домена.

На следующем рисунке показано диалоговое окно **Конфигурация CNAME** в службе Azure Front Door Service.

![Диалоговое окно конфигурации CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> Если домен, который вы будете использовать, уже активен и введен в действие, обратитесь в службу поддержки, чтобы включить этот домен в службе Azure Front Door Service и настроить проверку.

Можно использовать службу Azure Front Door Service для управления сертификатом, или можно использовать собственный сертификат для пользовательского домена.

На следующем рисунке показано диалоговое окно **HTTPS для личного домена** в службе Azure Front Door Service.

![Диалоговое окно "HTTPS для личного домена"](./media/Custom_Domain_HTTPS.png)

Сеть CDN теперь должна быть правильно настроена, чтобы ее можно было использовать с вашим сайтом Commerce.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка доменного имени](configure-your-domain-name.md)

[Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md)

[Создание сайта электронной коммерции](create-ecommerce-site.md)

[Связывание веб-сайта с каналом](associate-site-online-store.md)

[Управление файлами robots.txt](manage-robots-txt-files.md)

[Настройка специальных страниц для входа пользователей](custom-pages-user-logins.md)

[Включение обнаружения магазинов на основе местоположения](enable-store-detection.md)