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
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="d781e-103">Импорт входящих ASN через информационный объект V2</span><span class="sxs-lookup"><span data-stu-id="d781e-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d781e-104">Предварительные уведомления об отгрузке (ASNs) уведомляют вас о поставках поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d781e-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="d781e-105">Они помогают отправителю описать содержимое груза и дополнительную информацию о нем, например, товары и упаковку.</span><span class="sxs-lookup"><span data-stu-id="d781e-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="d781e-106">ASN могут помочь работникам склада узнать, что прибывает и когда.</span><span class="sxs-lookup"><span data-stu-id="d781e-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="d781e-107">Таким образом, они могут подготовиться.</span><span class="sxs-lookup"><span data-stu-id="d781e-107">Therefore, they can prepare.</span></span> <span data-ttu-id="d781e-108">Кроме того, работники склада могут использовать ASN для хранения сведений отгрузки в связанном заказе на покупку, который был ранее создан.</span><span class="sxs-lookup"><span data-stu-id="d781e-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="d781e-109">В этом разделе представлена коллекция сценариев, демонстрирующих примеры работы с файлами ASN.</span><span class="sxs-lookup"><span data-stu-id="d781e-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d781e-110">Импорт *Входящий ASN* применяется только к товарам, которые включены для расширенного управления складом (WMS).</span><span class="sxs-lookup"><span data-stu-id="d781e-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="d781e-111">Перед получением ASN, заказ на покупку должен быть зарегистрирован в системе для поставщика, который отправляет этот ASN.</span><span class="sxs-lookup"><span data-stu-id="d781e-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="d781e-112">Сущность входящего ASN V2</span><span class="sxs-lookup"><span data-stu-id="d781e-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="d781e-113">Вы импортируете входящие ASN с помощью составного информационного объекта *Входящий ASN V2*.</span><span class="sxs-lookup"><span data-stu-id="d781e-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="d781e-114">*Входящий ASN V2* использует следующие сущности:</span><span class="sxs-lookup"><span data-stu-id="d781e-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="d781e-115">Заголовок входящей загрузки</span><span class="sxs-lookup"><span data-stu-id="d781e-115">Inbound load header</span></span>
- <span data-ttu-id="d781e-116">Заголовок входящей отгрузки</span><span class="sxs-lookup"><span data-stu-id="d781e-116">Inbound shipment header</span></span>
- <span data-ttu-id="d781e-117">Структуры упаковки входящей загрузки</span><span class="sxs-lookup"><span data-stu-id="d781e-117">Inbound load packing structures</span></span>
- <span data-ttu-id="d781e-118">Ящики структуры упаковки входящей загрузки</span><span class="sxs-lookup"><span data-stu-id="d781e-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="d781e-119">Строки ящика структуры упаковки входящей загрузки</span><span class="sxs-lookup"><span data-stu-id="d781e-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="d781e-120">Строки структуры упаковки входящей загрузки</span><span class="sxs-lookup"><span data-stu-id="d781e-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="d781e-121">Композитный информационный объект *Входящий ASN V2* предназначен для сценариев асинхронной интеграции, в которых используется импорт на основе файлов XML.</span><span class="sxs-lookup"><span data-stu-id="d781e-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="d781e-122">Формат XML для импортируемых ASN</span><span class="sxs-lookup"><span data-stu-id="d781e-122">XML format for importing ASNs</span></span>

<span data-ttu-id="d781e-123">Microsoft Dynamics 365 Supply Chain Management поддерживает следующий формат XML для импортируемых ASN.</span><span class="sxs-lookup"><span data-stu-id="d781e-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="d781e-124">Каждый узел в файле XML представляет атрибут из отдельной сущности.</span><span class="sxs-lookup"><span data-stu-id="d781e-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

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

## <a name="examples"></a><span data-ttu-id="d781e-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="d781e-125">Examples</span></span>

<span data-ttu-id="d781e-126">Следующие подразделы предоставляют примеры файлов импорта ASN XML для отгрузок поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d781e-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="d781e-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d781e-127">Example 1</span></span>

<span data-ttu-id="d781e-128">В следующем примере показан файл XML для импорта отгрузок поставщиков для одного заказа на покупку, если не включены сведения о конкретном обращении.</span><span class="sxs-lookup"><span data-stu-id="d781e-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

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

### <a name="example-2"></a><span data-ttu-id="d781e-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d781e-129">Example 2</span></span>

<span data-ttu-id="d781e-130">В следующем примере показан файл XML для импорта отгрузок поставщиков для одного заказа на покупку, если включены сведения о конкретном обращении.</span><span class="sxs-lookup"><span data-stu-id="d781e-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

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

### <a name="example-3"></a><span data-ttu-id="d781e-131">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d781e-131">Example 3</span></span>

<span data-ttu-id="d781e-132">В следующем примере показан файл XML для импорта отгрузок поставщиков для нескольких заказов на покупку, если включены сведения об обращении.</span><span class="sxs-lookup"><span data-stu-id="d781e-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

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

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="d781e-133">Проверка результатов импорта файла ASN</span><span class="sxs-lookup"><span data-stu-id="d781e-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="d781e-134">Следуйте этим шагам, чтобы проверить результаты импорта файла ASN.</span><span class="sxs-lookup"><span data-stu-id="d781e-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="d781e-135">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="d781e-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d781e-136">Найдите и откройте загрузку, которая была создана в рамках импорта ASN.</span><span class="sxs-lookup"><span data-stu-id="d781e-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="d781e-137">На экспресс-вкладке **Загрузка** указаны значения, основанные на файле XML.</span><span class="sxs-lookup"><span data-stu-id="d781e-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="d781e-138">На экспресс-вкладке **Строки загрузки** показаны номера заказов на покупку и сведения номенклатур, основанные на файле XML.</span><span class="sxs-lookup"><span data-stu-id="d781e-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="d781e-139">На панели действий на вкладке **Отгрузка и получение** в группе **Получение** выберите **Структура упаковки** для проверки структуры упаковки груза.</span><span class="sxs-lookup"><span data-stu-id="d781e-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="d781e-140">На экспресс-вкладке **Палеты** указаны грузоместа, основанные на файле XML.</span><span class="sxs-lookup"><span data-stu-id="d781e-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="d781e-141">На экспресс-вкладке **Обращения** указаны обращения, основанные на файле XML.</span><span class="sxs-lookup"><span data-stu-id="d781e-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="d781e-142">На экспресс-вкладке **Номенклатуры** указаны номенклатуры и количества, основанные на файле XML.</span><span class="sxs-lookup"><span data-stu-id="d781e-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
