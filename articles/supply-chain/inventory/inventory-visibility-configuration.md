---
title: Конфигурация видимости запасов
description: В этой теме описывается, как настроить видимость запасов.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345041"
---
# <a name="inventory-visibility-configuration"></a>Конфигурация видимости запасов

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

В этой теме описывается, как настроить видимость запасов.

## <a name="introduction"></a><a name="introduction"></a>Введение

Прежде чем приступить к работе с видимостью запасов, необходимо выполнить следующую конфигурацию, как описано в этой теме:

- [Конфигурация источника данных](#data-source-configuration)
- [Конфигурация раздела](#partition-configuration)
- [Конфигурация иерархии индекса продуктов](#index-configuration)
- [Конфигурация резервирования (необязательно)](#reservation-configuration)
- [Пример конфигурации по умолчанию](#default-configuration-sample)

> [!NOTE]
> Можно просмотреть и изменить настройки видимости запасов в [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). После завершения настройки выберите **Обновить конфигурацию** в приложении.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Конфигурация источника данных

Источник данных представляет систему, из которой поступают данные. Примерами являются `fno` (то есть "приложения Dynamics 365 Finance and Operations") и `pos` (то есть "POS").

Конфигурация источника данных включает следующие компоненты:

- Аналитика (сопоставление аналитики)
- Физическая мера
- Рассчитанная мера

> [!NOTE]
> Источник данных `fno` зарезервирован для Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Аналитика (сопоставление аналитики)

Целью настройки аналитики является стандартизация интеграции нескольких систем для разноски событий и запросов, основанным на сочетании аналитик.

Видимость запасов поддерживает следующие общие базовые аналитики.

| Тип аналитики | Базовая аналитика |
|---|---|
| Продукт | `ColorId` |
| Продукт | `SizeId` |
| Продукт | `StyleId` |
| Продукт | `ConfigId` |
| Отслеживание | `BatchId` |
| Отслеживание | `SerialId` |
| Расположение | `LocationId` |
| Расположение | `SiteId` |
| Статус запасов | `StatusId` |
| Зависит от склада | `WMSLocationId` |
| Зависит от склада | `WMSPalletId` |
| Зависит от склада | `LicensePlateId` |
| Прочее | `VersionId` |
| Запасы (настраиваемый) | `InventDimension1` через `InventDimension12` |
| Добавочный номер | `ExtendedDimension1` через `ExtendedDimension8` |

> [!NOTE]
> Типы аналитики, приведенные в предыдущей таблице, используются только для справки. Вам не нужно определять их в видимости запасов.
>
> Аналитики запасов (настраиваемые) могут быть зарезервированы для Supply Chain Management. В этом случае вместо этого можно использовать расширенные аналитики.

Внешние системы могут получить доступ к видимости запасов через интерфейсы API RESTFUL. Для интеграции видимость запасов позволяет настроить _внешний источник данных_ и сопоставление из _внешних аналитик_ для _базовых аналитик_. Ниже приведен пример таблицы сопоставления аналитик.

| Внешняя аналитика | Базовая аналитика |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Настроив сопоставление аналитики, можно отправлять внешние аналитики непосредственно в видимость запасов. После этого видимость запасов будет автоматически преобразовывать внешние аналитики в базовые аналитики.

### <a name="physical-measures"></a>Физические меры

Физические меры изменяют количество и отображают статус запасов. В зависимости от потребностей можно определить собственные физические меры.

Видимость запасов предоставляет список физических мер по умолчанию, связанных с Supply Chain Management (источник данных `fno`). В следующей таблице представлен пример физических мер.

| Имя физической меры | описание |
|---|---|
| `NotSpecified` | Не указано |
| `Arrived` | Прибыло |
| `AvailOrdered` | Доступно заказанного |
| `AvailPhysical` | Физ. доступно |
| `Deducted` | Отпущено |
| `OnOrder` | OnOrder |
| `Ordered` | Занято |
| `PhysicalInvent` | Физические запасы |
| `Picked` | Скомплектовано |
| `PostedQty` | Разнесенное количество |
| `QuotationIssue` | Расход по предложению |
| `QuotationReceipt` | Принятие предложения |
| `Received` | Получение |
| `Registered` | Зарегистрировано |
| `ReservOrdered` | Зарезервировано в заказанных |
| `ReservPhysical` | Физически зарезервировано |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Рассчитанные меры

Вычисляемые меры дают настраиваемую формулу вычислений, которая состоит из комбинации физических мер. Эта функция позволяют определить набор физических мер, которые будут добавлены, и/или набор физических мер, которые будут вычтены, чтобы сформировать настраиваемую меру.

Например, есть следующий результат запроса.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Затем выполняется настройка вычисляемой меры с именем `MyCustomAvailableforReservation`, как показано в следующей таблице. Эта рассчитанная мера будет потреблена системой потребления.

| Система потребления | Рассчитанная мера | Иcточник данных | Физическая мера | Тип расчета |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

При использовании этой расчетной формулы новый результат запроса будет включать настроенную меру.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Выходные данные `MyCustomAvailableforReservation` основаны на параметрах расчета в настраиваемых измерениях следующим образом: 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Конфигурация раздела

Конфигурация раздела состоит из комбинации базовых аналитик. Она определяет шаблон распределения данных. Операции с данными в одном и том же разделе поддерживают высокую производительность и стоят не слишком много. Таким образом, качественные шаблоны разделов могут значительно повлиять на производительность.

Видимость запасов обеспечивает следующую конфигурацию раздела по умолчанию.

| Базовая аналитика | Иерархия |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Конфигурация разделов по умолчанию используется только для справки. Вам не нужно определять это в видимости запасов. В настоящее время обновление конфигурации раздела не поддерживается.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Конфигурация иерархии индекса продуктов

В большинстве случаев запрос запасов в наличии не будет иметь самый высокий "итоговый" уровень. Вместо этого, возможно, потребуется просмотреть результаты, агрегированные на основе складских аналитик.

Видимость запасов обеспечивает гибкость, позволяя настраивать _индексы_. Эти индексы основаны на аналитике или комбинации аналитик. Индекс состоит из *номера набора*, *аналитики* и *иерархии*, как определено в следующей таблице.

| ФИО | описание |
|---|---|
| Номер набора | Аналитики, которые относятся к одному набору (индекс), будут сгруппированы вместе и для них будут добавлены одинаковые номера наборов. |
| Аналитика | Базовые аналитики, по которым выполняется агрегирование результатов запроса. |
| Иерархия | Иерархия используется для определения поддерживаемых комбинаций аналитик, которые могут запрашиваться. Например, можно настроить набор аналитик, который имеет последовательность иерархии `(ColorId, SizeId, StyleId)`. В этом случае система поддерживает запросы четырех комбинаций аналитик. Первое сочетание пустое, второе — `(ColorId)`, третье, `(ColorId, SizeId)`, а четвертое — `(ColorId, SizeId, StyleId)`. Другие сочетания не поддерживаются. Дополнительные сведения см. в следующих примерах. |

### <a name="example"></a>Пример

В этом разделе представлен пример работы иерархии.

Имеются следующие номенклатуры в запасах.

| Номенклатура | ColorId | SizeId | StyleId | Количество |
|---|---|---|---|---|
| Футболка | Черный | Небольшой | Широк. | 1 |
| Футболка | Черный | Небольшой | Обычная | 2 |
| Футболка | Черный | Большое | Широк. | 3 |
| Футболка | Черный | Большое | Обычная | 4 |
| Футболка | Красный | Небольшой | Широк. | 5 |
| Футболка | Красный | Небольшой | Обычная | 6 |
| Футболка | Красный | Большое | Обычная | 7 |

Вот индекс.

| Номер набора | Аналитика | Иерархия |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Индекс позволяет выполнять запросы запасов в наличии следующими способами:

- `()` — сгруппированы по всем

    - Футболка, 28

- `(ColorId)` — сгруппированы по `ColorId`

    - Футболка, черная, 10
    - Футболка, красная, 18

- `(ColorId, SizeId)` — группирование по сочетанию `ColorId` и `SizeId`

    - Футболка, черная, малая, 3
    - Футболка, черная, большая, 7
    - Футболка, красная, малая, 11
    - Футболка, красная, большая, 7

- `(ColorId, SizeId, StyleId)` — группирование по сочетанию `ColorId`, `SizeId` и `StyleId`

    - Футболка, черная, малая, широкая, 1
    - Футболка, черная, малая, обычная, 2
    - Футболка, черная, большая, широкая, 3
    - Футболка, черная, большая, обычная, 4
    - Футболка, красная, малая, широкая, 5
    - Футболка, красная, малая, обычная, 6
    - Футболка, красная, большая, обычная, 7

> [!NOTE]
> Базовые аналитики, которые определены в конфигурации разделов, не должны определяться в конфигурациях индекса.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Конфигурация резервирования (необязательно)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Конфигурация резервирования требуется, если нужно использовать функцию "предварительное резервирование". Конфигурация состоит из двух фундаментальных частей:

- Сопоставление предварительного резервирования
- Иерархия предварительного резервирования

### <a name="soft-reservation-mapping"></a>Сопоставление предварительного резервирования

При резервировании может возникнуть необходимость узнать, доступны ли в данный момент запасы в наличии для резервирования. Проверка связана с вычисляемой мерой, которая представляет собой формулу вычисления комбинации физических мер.

Например, мера резервирования базируется на физической мере `SoftReservOrdered` из источника данных `iv` (видимость запасов). В этом случае можно настроить рассчитанную меру `AvailableToReserve` источника данных `iv`, как показано ниже.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `AvailPhysical` |
| Сложение | `pos` | `Inbound` |
| Вычитание | `pos` | `Outbound` |
| Вычитание | `iv` | `SoftReservOrdered` |

Затем настройте сопоставление предварительного резервирования для обеспечения сопоставления меры резервирования `SoftReservOrdered` с рассчитанной мерой `AvailableToReserve`.

| Источник данных физической меры | Физическая мера | Доступно для источника данных резервирования | Доступно для рассчитанной меры резервирования |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Теперь, когда выполняется резервирование в `SoftReservOrdered`, видимость запасов будет автоматически выполнять поиск `AvailableToReserve` и связанной формулы вычислений для проверки резервирования.

Например, в видимости запасов имеются следующие запасы в наличии.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

В этом случае применяются следующие вычисления:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Таким образом, при попытке выполнить резервирование в `iv.SoftReservOrdered` и количестве меньше или равно `AvailableToReserve` (10), можно выполнить резервирование.

### <a name="soft-reservation-hierarchy"></a>Иерархия предварительного резервирования

Иерархия резервирования описывает последовательность аналитик, которая должна быть указана при выполнении резервирования. Это функционирует так же, как и иерархия индексов продуктов для запросов в наличии.

Иерархия резервирования не зависит от иерархии индексов продуктов. Эта независимость позволяет реализовать управление категориями, когда пользователи могут разбить аналитики на детали, чтобы указать требования для более точного резервирования.

Ниже приведен пример иерархии предварительного резервирования.

| Базовая аналитика | Иерархия |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

В этом примере можно выполнять резервирование по следующим последовательностям аналитик:

- `()` – аналитика не указана.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Допустимая последовательность аналитик должен строго следовать иерархии резервирования, аналитика за аналитикой. Например, последовательность иерархии `(SiteId, LocationId, SizeId)` недействительная, так как отсутствует `ColorId`.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Пример конфигурации по умолчанию

На стадии инициализации видимость запасов устанавливает конфигурацию по умолчанию. Эту конфигурацию можно изменить.

### <a name="data-source-configuration"></a>Конфигурация источника данных

#### <a name="configuration-of-the-iv-data-source"></a>Конфигурация источника данных iv

В этом разделе описывается, как настроить источник данных `iv`.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Физические меры, настроенные для источника данных IV

Для источника данных `iv` настроены следующие физические меры:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Вычисляемая мера OrderedTotal

Вычисляемая мера `OrderedTotal` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `Ordered` |
| Сложение | `fno` | `Arrived` |
| Сложение | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Рассчитанная мера OnHand

Вычисляемая мера `OnHand` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `PhysicalInvent` |
| Сложение | `iom` | `OnHand` |
| Сложение | `erp` | `Unrestricted` |
| Сложение | `erp` | `QualityInspection` |
| Сложение | `pos` | `PosInbound` |
| Вычитание | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Вычисляемая мера ReservedTotal

Вычисляемая мера `ReservedTotal` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `ReservPhysical` |
| Сложение | `fno` | `ReservOrdered` |
| Сложение | `iv` | `SoftReservPhysical` |
| Сложение | `iv` | `SoftReservOrdered` |
| Сложение | `iv` | `ReservPhysical` |
| Сложение | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Вычисляемая мера SoftReserved

Вычисляемая мера `SoftReserved` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `iv` | `SoftReservPhysical` |
| Сложение | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Вычисляемая мера HardReserved

Вычисляемая мера `HardReserved` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `ReservPhysical` |
| Сложение | `fno` | `ReservOrdered` |
| Сложение | `iv` | `ReservPhysical` |
| Сложение | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Вычисляемая мера OpenOrder

Вычисляемая мера `OpenOrder` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `OnOrder` |
| Сложение | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Вычисляемая мера OnHandAvailable

Вычисляемая мера `OnHandAvailable` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `PhysicalInvent` |
| Сложение | `iom` | `OnHand` |
| Сложение | `erp` | `Unrestricted` |
| Сложение | `erp` | `QualityInspection` |
| Сложение | `pos` | `PosInbound` |
| Вычитание | `fno` | `ReservPhysical` |
| Вычитание | `iv` | `SoftReservPhysical` |
| Вычитание | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Вычисляемая мера AvailableToReserve

Вычисляемая мера `AvailableToReserve` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `PhysicalInvent` |
| Сложение | `iom` | `OnHand` |
| Сложение | `erp` | `Unrestricted` |
| Сложение | `erp` | `QualityInspection` |
| Сложение | `pos` | `PosInbound` |
| Сложение | `fno` | `Ordered` |
| Сложение | `fno` | `Arrived` |
| Сложение | `iv` | `Ordered` |
| Вычитание | `fno` | `ReservPhysical` |
| Вычитание | `fno` | `ReservOrdered` |
| Вычитание | `iv` | `SoftReservPhysical` |
| Вычитание | `iv` | `SoftReservOrdered` |
| Вычитание | `iv` | `ReservPhysical` |
| Вычитание | `iv` | `ReservOrdered` |
| Вычитание | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Вычисляемая мера InventorySupply

Вычисляемая мера `InventorySupply` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `Ordered` |
| Сложение | `fno` | `Arrived` |
| Сложение | `iv` | `Ordered` |
| Сложение | `fno` | `PhysicalInvent` |
| Сложение | `iom` | `OnHand` |
| Сложение | `erp` | `Unrestricted` |
| Сложение | `erp` | `QualityInspection` |
| Сложение | `pos` | `PosInbound` |
| Вычитание | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Вычисляемая мера InventoryDemand

Вычисляемая мера `InventoryDemand` настраиваемся для источника данных `iv`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `OnOrder` |
| Сложение | `iom` | `OnOrder` |
| Сложение | `iv` | `SoftReservPhysical` |
| Сложение | `iv` | `SoftReservOrdered` |
| Сложение | `fno` | `ReservPhysical` |
| Сложение | `fno` | `ReservOrdered` |
| Сложение | `iv` | `ReservPhysical` |
| Сложение | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Конфигурация источника данных fno

В этом разделе описывается, как настроить источник данных `fno`.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Сопоставления аналитик для источника данных fno

Сопоставления аналитик, перечисленные в следующей таблице, настроены для источника данных `fno`.

| Внешняя аналитика | Базовая аналитика |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Физические меры, настроенные для источника данных fno

Для источника данных `fno` настроены следующие физические меры:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Конфигурация источника данных pos

В этом разделе описывается, как настроить источник данных `pos`.

##### <a name="physical-measures-for-the-pos-data-source"></a>Физические меры, настроенные для источника данных pos

Для источника данных `pos` настроены следующие физические меры:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Вычисляемая мера AvailQuantity

Вычисляемая мера `AvailQuantity` настраиваемся для источника данных `pos`, как показано в следующей таблице.

| Тип расчета | Иcточник данных | Физическая мера |
|---|---|---|
| Сложение | `fno` | `AvailPhysical` |
| Сложение | `pos` | `PosInbound` |
| Вычитание | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Конфигурация источника данных iom

Следующие физические меры настраиваются для источника данных `iom` (Intelligent Order Management):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Конфигурация источника данных erp

Следующие физические меры настраиваются для источника данных `erp` (планирование ресурсов предприятия):

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Конфигурация раздела

В следующей таблице показана конфигурация раздела по умолчанию.

| Базовая аналитика | Иерархия |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Конфигурация индекса

В следующей таблице показана конфигурация индекса по умолчанию.

| Номер набора | Аналитика | Иерархия |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Конфигурация резервирования

В этом разделе описывается конфигурация резервирования по умолчанию.

#### <a name="reservation-mapping"></a>Сопоставление резервирования

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

В следующей таблице показано сопоставление резервирования по умолчанию.

| Источник данных физической меры | Физическая мера | Доступно для источника данных резервирования | Доступно для рассчитанной меры резервирования |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Иерархия резервирования

В следующей таблице показана иерархия резервирования по умолчанию.

| Базовая аналитика | Иерархия |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
