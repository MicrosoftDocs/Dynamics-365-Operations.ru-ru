---
title: Общедоступные интерфейсы API Inventory Visibility
description: В этой статье описываются открытые API, предоставляемые видимостью запасов.
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
ms.openlocfilehash: 14812fc201ba1038a78ea3317686dbe189ffa687
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423604"
---
# <a name="inventory-visibility-public-apis"></a>Общедоступные интерфейсы API Inventory Visibility

[!include [banner](../includes/banner.md)]


В этой статье описываются открытые API, предоставляемые видимостью запасов.

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
| /api/environment/{environmentId}/onhand/unreserve | Разнести | [Реверсирование одного события резервирования](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Разнести | [Реверсирование нескольких событий резервирования](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Разнести | [Создание одного запланированного изменения запасов в наличии](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Разнести | [Создание нескольких запланированных изменений запасов в наличии](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Разнести | [Запрос с использованием метода POST](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Получить | [Запрос с использованием метода GET](#query-with-get-method) |
| /api/environment/{environmentId}/allocation/allocate | Разнести | [Создание одного события распределения](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/unallocate | Разнести | [Создание одного события нераспределения](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/reallocate | Разнести | [Создание одного события перераспределения](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/consume | Разнести | [Создание одного события потребления](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/query | Разнести | [Запрос результата распределения](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Частью пути {environmentId} является идентификатор среды в Microsoft Dynamics Lifecycle Services (LCS).
> 
> Массовый API-интерфейс может возвращать максимум 512 записей для каждого запроса.

Корпорация Майкрософт представила готовую коллекцию запросов *Postman*. Эту коллекцию можно импортировать в программное обеспечение *Postman*, используя следующую общую ссылку: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

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

Маркер безопасности платформы используется для вызова открытых API видимости запасов. Таким образом, необходимо создать маркер _Azure Active Directory (Azure AD)_ с помощью приложения Azure AD. Затем необходимо использовать маркер Azure AD, чтобы получить _маркер доступа_ из службы безопасности.

Корпорация Майкрософт представила готовую коллекцию токенов получения *Postman*. Эту коллекцию можно импортировать в программное обеспечение *Postman*, используя следующую общую ссылку: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Чтобы получить маркер службы безопасности, выполните следующие действия.

1. Выполните вход на портал Azure и используйте его, чтобы найти значения `clientId` и `clientSecret` для вашего приложения Dynamics 365 Supply Chain Management.
1. Получите токен Azure AD (`aadToken`), отправив HTTP-запрос со следующими свойствами:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
   - **Метод:** `GET`
   - **Содержимое основной части (данные формы):**

     | Ключ           | значение                                            |
     | ------------- | -------------------------------------------------|
     | client_id     | ${aadAppId}                                      |
     | client_secret | ${aadAppSecret}                                  |
     | grant_type    | client_credentials                               |
     | область         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

   В ответе должен быть получен маркер Azure AD (`aadToken`). Она должна быть похожа на следующий пример.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
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
       "context": "{$LCS_environment_id}",
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

   В ответе должен быть получен маркер доступа (`access_token`). Следует использовать этот маркер в качестве маркера носителя для вызова API видимости запасов. Рассмотрим пример.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> При использовании коллекции запросов *Postman* для вызова общедоступных интерфейсов API видимости запасов необходимо добавить маркер носителя для каждого запроса. Чтобы найти маркер носителя, выберите вкладку **Авторизация** в URL-адресе запроса, выберите тип **Маркер носителя** и скопируйте токен доступа, который был извлечен на последнем шаге. В последующих разделах этой статьи токен `$access_token` будет использоваться для представления токена, который был выбран на последнем шаге.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Создание событий изменения в наличии

Существуют два интерфейса API для создания событий изменения в наличии:

- Создать одну запись: `/api/environment/{environmentId}/onhand`
- Создание нескольких записей: `/api/environment/{environmentId}/onhand/bulk`

В следующей таблице дана сводка значение каждого поля в тексте JSON.

| FieldID | Описание |
|---|---|
| `id` | Уникальный код для конкретного события изменения. Если из-за сбои системы происходит повторная отправка, этот код используется, чтобы гарантировать, что одно и то же событие не будет дважды учитываться в системе. |
| `organizationId` | Идентификатор организации, связанной с событием. Это значение сопоставляется с организацией или идентификатором области данных в Supply Chain Management. |
| `productId` | Идентификатор продукта. |
| `quantities` | Это количество, на которое должно быть уменьшено количество в наличии. Например, если на полку добавлено 10 новых книг, это значение будет равно `quantities:{ shelf:{ received: 10 }}`. Если с полки убраны или проданы три книги, это значение будет равно `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Источник данных для аналитик, используемых в разноске события изменения и запроса. Если указан источник данных, можно использовать настраиваемые аналитики из указанного источника данных. С помощью конфигурации аналитик видимость запасов может сопоставлять пользовательские аналитики с общими аналитиками по умолчанию. Если значение `dimensionDataSource` не указано, в запросах могут использоваться только универсальные [базовые аналитики](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Динамическая пара "ключ-значение". Значения сопоставляются с некоторыми аналитиками в Supply Chain Management. Однако можно также добавить пользовательские аналитики (например, _Источник_), чтобы указать, поступает ли событие из модуля Supply Chain Management или из внешней системы. |

> [!NOTE]
> Параметры `siteId` и `locationId` создают [конфигурацию раздела](inventory-visibility-configuration.md#partition-configuration). Поэтому при создании событий изменения запасов в наличии необходимо задать их в аналитиках, установить или переопределить количества в наличии или создать события резервирования.

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
    "organizationId": "SCM_IV",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "posMachineId": "0001",
        "colorId&quot;: &quot;red"
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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red"
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
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "posSite1",
            "posLocationId": "posLocation1",
            "posMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_2",
        "dimensions": {
            "siteId": "iv_postman_site",
            "locationId": "iv_postman_location",
            "colorId&quot;: &quot;black"
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

В следующем примере показано содержимое текста примера. Поведение этого API отличается от поведения интерфейсов API, описанных в разделе [Создание событий изменения в наличии](#create-onhand-change-event) ранее в этой статье. В этом примере количество продукта *Футболка* будет задано как 1.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "iv_postman_site",
            "posLocationId": "iv_postman_location",
            "posMachineId": "0001"
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

Для использования API *Резервирование* необходимо включить функцию резервирования и выполнить настройку резервирования. Дополнительные сведения см. в [Конфигурация резервирования (необязательно)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Создание одного события резервирования

Можно выполнить резервирование для других параметров источника данных. Чтобы настроить этот тип резервирования, сначала укажите источник данных в параметре `dimensionDataSource`. Затем в параметре `dimensions` задайте аналитики в соответствии с параметрами аналитик в целевом источнике данных.

При вызове API резервирования можно контролировать проверку резервирования путем указания логического параметра `ifCheckAvailForReserv` в тексте запроса. Значение `True` означает, что проверка является обязательной, а значение `False` означает, что проверка не является обязательной. Значение по умолчанию — `True`.

Если необходимо реверсировать резервирование или отказаться от указанного количества запасов, установите отрицательное значение количества и задайте для параметра `ifCheckAvailForReserv` значение `False` для пропуска проверки. Также имеется выделенный API-интерфейс отмены резервирования для выполнения той же задачи. Разница заключается только в способе вызова двух интерфейсов API. Конкретное событие резервирования проще реверсировать, используя `reservationId` с API-интерфейсом *отмены резервирования*. Дополнительные сведения см. в разделе [_Отмена резервирования одного события резервирования_](#reverse-reservation-events).

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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

В следующем примере показан успешный ответ.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Создание нескольких событий резервирования

Этот интерфейс API представляет собой массовую версию [API одного события](#create-reservation-events).

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

## <a name="reverse-reservation-events"></a>Реверсирование событий резервирования

API-интерфейс *Отмена резервирования* выступает в качестве обратной операции для событий [*Резервирование*](#create-reservation-events). Он предоставляет способ сторнирования события резервирования, указанного по `reservationId`, или для уменьшения количества резервирования.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Реверсирование одного события резервирования

Когда создается резервирование, `reservationId` будет включен в тело ответа. Для отмены резервирования необходимо указать то же самое значение `reservationId`, и включить те же значения `organizationId` и `dimensions`, которые использовались для вызова API-интерфейса резервирования. Наконец, укажите значение `OffsetQty`, представляющее число номенклатур, которое должно быть освобождено из предыдущего резервирования. Резервирование может быть полностью или частично отменено в зависимости от указанного значения `OffsetQty`. Например, если *100* единиц номенклатуры было зарезервировано, можно указать `OffsetQty: 10`, чтобы отменить резервирование *10* из первоначально зарезервированной суммы.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

В следующем коде показан пример содержимого текста.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

В следующем коде показан пример текста успешного ответа.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Когда в тексте ответа значение `OffsetQty` меньше или равно количеству резервирования, `processingStatus` будет "*success*" и `totalInvalidOffsetQtyByReservId` будет равно *0*.
>
> Если `OffsetQty` больше зарезервированной суммы, `processingStatus` будет "*partialSuccess*" и `totalInvalidOffsetQtyByReservId` будет разницей между `OffsetQty` и зарезервированным количеством.
>
>Например, если резервирование имеет количество *10*, а `OffsetQty` равно *12*, `totalInvalidOffsetQtyByReservId` будет *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Реверсирование нескольких событий резервирования

Этот интерфейс API представляет собой массовую версию [API одного события](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Запрос в наличии

Используйте API *Запрос в наличии* для получения текущих данных запасов в наличии для вашей продукции. В настоящее время API поддерживает запросы до 5000 отдельных номенклатур по значению `productID`. В каждом запросе также может быть указано несколько значений `siteID` и `locationID`. Максимальное ограничение определяется следующим уравнением:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

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

- `organizationId` должен содержать только одно значение, но все еще является массивом.
- `productId` может содержать одно или несколько значений. Если оно является пустым массивом, будут возвращаться все продукты.
- `siteId` и `locationId` используются для секционирования в видимости запасов. Вы можете указать более одного значения `siteId` и `locationId` в запросе *Запрос в наличии*. В текущем выпуске необходимо указать оба значения `siteId` и `locationId`.

Мы рекомендуем использовать параметр `groupByValues`, чтобы соответствовать вашей конфигурации для индексирования. Дополнительные сведения см. в [Конфигурация иерархии индекса продуктов](./inventory-visibility-configuration.md#index-configuration).

Этот параметр `returnNegative` определяет, содержат ли результаты отрицательные значения.

> [!NOTE]
> Если вы включили функции графика изменения запасов в наличии и количеств, доступных для заказа (ATP), запрос также может включать логический параметр `QueryATP`, который управляет тем, содержат ли результаты запроса сведения ATP. Дополнительные сведения и примеры см. в разделе [Графики изменения запасов в наличии и доступность для заказа](inventory-visibility-available-to-promise.md).

В следующем примере показано содержимое текста примера.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

В следующем примере показано, как запросить все продукты на конкретном сайте и в местонахождении.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
    },
    "groupByValues": ["colorId", "sizeId"],
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
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Доступно для резервирования

Можно настроить видимость запасов, чтобы можно было планировать будущие изменения запасов в наличии и рассчитывать количества ATP. ATP — это количество номенклатуры, которое доступно и может быть зарезервировано для клиента в следующем периоде. Использование расчета ATP может значительно повысить возможности выполнения заказов. Сведения о том, как включить эту функцию и как работать с видимостью запасов через его API после включения функции, см. в разделе [Графики изменения запасов в наличии и доступность для заказа](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Распределение

Интерфейсы API, связанные с распределением, настраиваются в разделе [Распределение видимости запасов](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
