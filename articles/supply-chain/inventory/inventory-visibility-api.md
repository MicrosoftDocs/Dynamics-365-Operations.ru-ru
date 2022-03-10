---
title: Общедоступные интерфейсы API видимости запасов
description: В этой теме описываются открытые API, предоставляемые видимостью запасов.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f74bb4bd4ed66520c04261bd9f82faad7775817e
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062119"
---
# <a name="inventory-visibility-public-apis"></a>Общедоступные интерфейсы API видимости запасов

[!include [banner](../includes/banner.md)]


В этой теме описываются открытые API, предоставляемые видимостью запасов.

Открытый интерфейс REST API надстройки контроля запасов представляет несколько определенных конечных точек интеграции. Он поддерживает четыре основных типа взаимодействий:

- Разноска изменений запасов в наличии в надстройку из внешней системы
- Настройка или переопределение количества запасов в наличии в надстройке из внешней системы
- Разноска событий резервирования в надстройку из внешней системы
- Запрос текущих количеств в наличии из внешней системы

В следующей таблице перечислены API, которые сейчас доступны:

| Путь | Метод | описание |
|---|---|---|
| /api/environment/{environmentId}/onhand | Должность | [Создание одного события изменения в наличии](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Должность | [Создание нескольких событий изменения](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Должность | [Настройка/переопределение количеств в наличии](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Должность | [Создание одного события резервирования](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Должность | [Создание нескольких событий резервирования](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Должность | [Запрос с использованием метода POST](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Получить | [Запрос с использованием метода GET](#query-with-get-method) |

Корпорация Майкрософт представила готовую коллекцию запросов *Postman*. Эту коллекцию можно импортировать в программное обеспечение *Postman*, используя следующую общую ссылку: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

> [!NOTE]
> Частью пути {environmentId} является идентификатор среды в Microsoft Dynamics Lifecycle Services (LCS).
> 
> Массовый API-интерфейс может возвращать максимум 512 записей для каждого запроса.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Найдите конечную точку в соответствии с используемой средой Lifecycle Services

Микрослужба видимости запасов развернута в Microsoft Azure Service Fabric, в нескольких географических регионах и в нескольких странах/регионах. В настоящее время отсутствует центральная конечная точка, которая может автоматически перенаправлять запрос в соответствующие географический регион и страну/регион. Поэтому необходимо вставить фрагменты данных в URL-адрес, используя следующий шаблон:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Краткое наименование географического региона можно найти в среде Microsoft Dynamics Lifecycle Services (LCS). В следующей таблице перечислены географические регионы, которые сейчас доступны.

| Регион Azure        | Краткое название региона |
| ------------------- | ----------------- |
| Восточная Австралия      | eau               |
| Юго-восточная Австралия | seau              |
| Центральная Канада      | cca               |
| Восточная Канада         | eca               |
| Северная Европа        | neu               |
| Западная Европа         | weu               |
| Восточная часть США             | eus               |
| Западная часть США             | wus               |
| Южная часть Соединенного Королевства            | suk               |
| Западная часть Соединенного Королевства             | wuk               |
| Восточная Япония          | ejp               |
| Западная Япония          | wjp               |
| Южная Бразилия        | sbr               |
| Юго-центральный регион США    | scus              |

Номер остров — это место развертывания среды LCS в Service Fabric. В настоящее время невозможно получить эту информацию со стороны пользователя.

Корпорация Майкрософт создала интерфейс пользователя Power Apps, чтобы можно было получить полную конечную точку микрослужбы. Дополнительные сведения см. в [Поиск конечной точки службы](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Аутентификация

Маркер безопасности платформы используется для вызова открытых API видимости запасов. Таким образом, необходимо создать _Маркер Azure Active Directory (Azure AD)_ с помощью приложения Azure AD. Затем необходимо использовать маркер Azure AD, чтобы получить _маркер доступа_ из службы безопасности.

Корпорация Майкрософт представила готовую коллекцию токенов получения *Postman*. Эту коллекцию можно импортировать в программное обеспечение *Postman*, используя следующую общую ссылку: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Чтобы получить маркер службы безопасности, выполните следующие действия.

1. Выполните вход на портал Azure и используйте его, чтобы найти значения `clientId` и `clientSecret` для вашего приложения Dynamics 365 Supply Chain Management.
1. Получите токен Azure AD (`aadToken`), отправив HTTP-запрос со следующими свойствами:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Метод:** `GET`
   - **Содержимое основной части (данные формы):**

     | Ключ           | значение                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | ресурс      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   В ответе должен быть получен маркер Azure AD (`aadToken`). Она должна быть похожа на следующий пример.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
       "access_token": "eyJ0eX...8WQ"
   }
   ```

1. Сформулируйте запрос в формате JavaScript (JSON), который напоминает следующий пример.

   ```json
   {
       "grant_type": "client_credentials",
       "client_assertion_type": "aad_app",
       "client_assertion": "{Your_AADToken}",
       "scope": "https://inventoryservice.operations365.dynamics.com/.default",
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   Обратите внимание на следующие аспекты:

   - Значение `client_assertion` должно быть токеном Azure AD (`aadToken`), полученным на предыдущем шаге.
   - Значение `context` должно быть идентификатором среды LCS, в которой требуется развернуть надстройку.
   - Установите все остальные значения, как показано в примере.

1. Получите токен доступа (`access_token`), отправив HTTP-запрос со следующими свойствами:

   - **URL:** `https://securityservice.operations365.dynamics.com/token`
   - **Метод:** `POST`
   - **Заголовок HTTP:** включите версию API. (Ключ — `Api-Version`, и значение — `1.0`.)
   - **Основное содержимое** — включает запрос JSON, созданный на предыдущем шаге.

   В ответе должен быть получен маркер доступа (`access_token`). Следует использовать этот маркер в качестве маркера носителя для вызова API видимости запасов. Рассмотрим пример:

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> При использовании коллекции запросов *Postman* для вызова общедоступных интерфейсов API видимости запасов необходимо добавить маркер носителя для каждого запроса. Чтобы найти маркер носителя, выберите вкладку **Авторизация** в URL-адресе запроса, выберите тип **Маркер носителя** и скопируйте токен доступа, который был извлечен на последнем шаге. В последующих разделах этой темы токен `$access_token` будет использоваться для представления токена, который был выбран на последнем шаге.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Создание событий изменения в наличии

Существуют два интерфейса API для создания событий изменения в наличии:

- Создать одну запись: `/api/environment/{environmentId}/onhand`
- Создание нескольких записей: `/api/environment/{environmentId}/onhand/bulk`

В следующей таблице дана сводка значение каждого поля в тексте JSON.

| FieldID | описание |
|---|---|
| `id` | Уникальный код для конкретного события изменения. Этот код используется, чтобы гарантировать, что при возникновении ошибки при обмене данными со службой во время разноски то же событие не будет дважды учитываться в системе при повторной отправке. |
| `organizationId` | Идентификатор организации, связанной с событием. Это значение сопоставляется с организацией или идентификатором области данных в Supply Chain Management. |
| `productId` | Идентификатор продукта. |
| `quantities` | Это количество, на которое должно быть уменьшено количество в наличии. Например, если на полку добавлено 10 новых книг, это значение будет равно `quantities:{ shelf:{ received: 10 }}`. Если с полки убраны или проданы три книги, это значение будет равно `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Источник данных для аналитик, используемых в разноске события изменения и запроса. Если указан источник данных, можно использовать настраиваемые аналитики из указанного источника данных. С помощью конфигурации аналитик видимость запасов может сопоставлять пользовательские аналитики с общими аналитиками по умолчанию. Если значение `dimensionDataSource` не указано, в запросах могут использоваться только универсальные [базовые аналитики](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Динамическая пара "ключ-значение". Значения сопоставляются с некоторыми аналитиками в Supply Chain Management. Однако можно также добавить пользовательские аналитики (например, _Источник_), чтобы указать, поступает ли событие из модуля Supply Chain Management или из внешней системы. |

> [!NOTE]
> Параметры `SiteId` и `LocationId` создают [конфигурацию раздела](inventory-visibility-configuration.md#partition-configuration). Поэтому при создании событий изменения запасов в наличии необходимо задать их в аналитиках, установить или переопределить количества в наличии или создать события резервирования.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Создание одного события изменения в наличии

Этот API создает одно событие изменения в наличии.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

В следующем примере показано содержимое текста примера. В этом примере разносится событие изменения для продукта *Футболка*. Это событие берется из системы POS, и клиент вернул красную футболку в магазин. Это событие увеличит количество продукта *Футболка* на 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId&quot;: &quot;Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

В следующем примере показано содержимое текста примера без `dimensionDataSource`. В этом случае `dimensions` будет [базовой аналитикой](inventory-visibility-configuration.md#data-source-configuration-dimension). Если `dimensionDataSource` установлен, то `dimensions` могут быть либо аналитиками источника данных, либо базовыми аналитиками.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Создание нескольких событий изменения

Этот API может создавать несколько записей одновременно. Единственным различием между этим API и [API одного события](#create-one-onhand-change-event) являются значения `Path` и `Body`. Для этого API `Body` предоставляет массив записей. Максимальное число записей — 512, что означает, что API-интерфейс массовой обработки изменений запасов в наличии может поддерживать до 512 событий изменения за раз.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

В следующем примере показано содержимое текста примера.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Настройка/переопределение количеств в наличии

API _Задано в наличии_ переопределяет текущие данные для указанного продукта.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

В следующем примере показано содержимое текста примера. Поведение этого API отличается от поведения интерфейсов API, описанных в разделе [Создание событий изменения в наличии](#create-onhand-change-event) ранее в этой теме. В этом примере количество продукта *Футболка* будет задано как 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Создание событий резервирования

Для использования API *Резервирование* необходимо открыть функцию резервирование и выполнить настройку резервирования. Дополнительные сведения см. в [Конфигурация резервирования (необязательно)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Создание одного события резервирования

Можно выполнить резервирование для других параметров источника данных. Чтобы настроить этот тип резервирования, сначала укажите источник данных в параметре `dimensionDataSource`. Затем в параметре `dimensions` задайте аналитики в соответствии с параметрами аналитик в целевом источнике данных.

При вызове API резервирования можно контролировать проверку резервирования путем указания логического параметра `ifCheckAvailForReserv` в тексте запроса. Значение `True` означает, что проверка является обязательной, а значение `False` означает, что проверка не является обязательной. Значение по умолчанию — `True`.

Если необходимо отменить резервирование или отказаться от указанного количества запасов, установите отрицательное значение количества и задайте для параметра `ifCheckAvailForReserv` значение `False` для пропуска проверки.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

В следующем примере показано содержимое текста примера.

```json
{
    "id": "reserve-0",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Создание нескольких событий резервирования

Этот интерфейс API представляет собой массовую версию [API одного события](#create-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="query-on-hand"></a>Запрос в наличии

Используйте API _Запрос в наличии_ для получения текущих данных запасов в наличии для вашей продукции. В настоящее время API поддерживает запросы до 100 отдельных номенклатур по значению `ProductID`. В каждом запросе также может быть указано несколько значений `SiteID` и `LocationID`. Максимальное ограничение определяется как `NumOf(SiteID) * NumOf(LocationID) <= 100`.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Запрос с использованием метода POST

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

В части этого запроса `dimensionDataSource` по-прежнему является опциональным параметром. Если оно не задано, `filters` будет рассматриваться как *Базовая аналитика*. Имеется четыре обязательных поля для `filters`: `organizationId`, `productId`, `siteId` и `locationId`.

- `organizationId` должно содержать только одно значение, но все еще является массивом.
- `productId` может содержать одно или несколько значений. Если оно является пустым массивом, будут возвращаться все продукты.
- `siteId` и `locationId` используются для секционирования в видимости запасов. Вы можете указать более одного значения `siteId` и `locationId` в запросе *Запрос в наличии*. В текущем выпуске необходимо указать оба значения `siteId` и `locationId`.

Параметр `groupByValues` должен соответствовать вашей конфигурации для индексирования. Дополнительные сведения см. в [Конфигурация иерархии индекса продуктов](./inventory-visibility-configuration.md#index-configuration).

Этот параметр `returnNegative` определяет, содержат ли результаты отрицательные значения.

В следующем примере показано содержимое текста примера.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

В следующих примерах показано, как запросить все продукты на конкретном сайте и в местонахождении.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Запрос с использованием метода GET

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Пример URL-адреса GET. Этот запрос GET в точности совпадает с приведенным ранее примером POST.

```txt
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
