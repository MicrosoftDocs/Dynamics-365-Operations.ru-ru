---
title: Импорт входящих ASN через информационный объект V2
description: Эта тема объясняет, как управлять импортом входящих расширенных предварительных уведомлений об отгрузке (ASN) через входящий информационный объект ASN V2.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249159"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a>Импорт входящих ASN через информационный объект V2

[!include [banner](../../includes/banner.md)]

Предварительные уведомления об отгрузке (ASNs) уведомляют вас о поставках поставщиков. Они помогают отправителю описать содержимое груза и дополнительную информацию о нем, например, товары и упаковку.

ASN могут помочь работникам склада узнать, что прибывает и когда. Таким образом, они могут подготовиться. Кроме того, работники склада могут использовать ASN для хранения сведений отгрузки в связанном заказе на покупку, который был ранее создан.

В этом разделе представлена коллекция сценариев, демонстрирующих примеры работы с файлами ASN.

> [!IMPORTANT]
> Импорт *Входящий ASN* применяется только к товарам, которые включены для расширенного управления складом (WMS). Перед получением ASN, заказ на покупку должен быть зарегистрирован в системе для поставщика, который отправляет этот ASN.

## <a name="inbound-asn-v2-entity"></a>Сущность входящего ASN V2

Вы импортируете входящие ASN с помощью составного информационного объекта *Входящий ASN V2*. *Входящий ASN V2* использует следующие сущности:

- Заголовок входящей загрузки
- Заголовок входящей отгрузки
- Структуры упаковки входящей загрузки
- Ящики структуры упаковки входящей загрузки
- Строки ящика структуры упаковки входящей загрузки
- Строки структуры упаковки входящей загрузки

Композитный информационный объект *Входящий ASN V2* предназначен для сценариев асинхронной интеграции, в которых используется импорт на основе файлов XML.

## <a name="xml-format-for-importing-asns"></a>Формат XML для импортируемых ASN

Microsoft Dynamics 365 Supply Chain Management поддерживает следующий формат XML для импортируемых ASN. Каждый узел в файле XML представляет атрибут из отдельной сущности.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Примеры

Следующие подразделы предоставляют примеры файлов импорта ASN XML для отгрузок поставщиков.

### <a name="example-1"></a>Пример 1

В следующем примере показан файл XML для импорта отгрузок поставщиков для одного заказа на покупку, если не включены сведения о конкретном обращении.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Пример 2

В следующем примере показан файл XML для импорта отгрузок поставщиков для одного заказа на покупку, если включены сведения о конкретном обращении.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Пример 3

В следующем примере показан файл XML для импорта отгрузок поставщиков для нескольких заказов на покупку, если включены сведения об обращении.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Проверка результатов импорта файла ASN

Следуйте этим шагам, чтобы проверить результаты импорта файла ASN.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Найдите и откройте загрузку, которая была создана в рамках импорта ASN.
1. На экспресс-вкладке **Загрузка** указаны значения, основанные на файле XML.
1. На экспресс-вкладке **Строки загрузки** показаны номера заказов на покупку и сведения номенклатур, основанные на файле XML.
1. На панели действий на вкладке **Отгрузка и получение** в группе **Получение** выберите **Структура упаковки** для проверки структуры упаковки груза.
1. На экспресс-вкладке **Палеты** указаны грузоместа, основанные на файле XML.
1. На экспресс-вкладке **Обращения** указаны обращения, основанные на файле XML.
1. На экспресс-вкладке **Номенклатуры** указаны номенклатуры и количества, основанные на файле XML.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
