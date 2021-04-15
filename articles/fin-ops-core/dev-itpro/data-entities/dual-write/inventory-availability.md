---
title: Доступность запасов в двойной записи
description: В этой теме приводятся сведения о порядке проверки доступности запасов в случае двойной записи.
author: yijialuan
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748573"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="a6c2f-103">Доступность запасов в двойной записи</span><span class="sxs-lookup"><span data-stu-id="a6c2f-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6c2f-104">Используя доступность запасов, можно проверять запасы перед добавлением продукта на страницу **Предложения**, **Заказы** или **Накладные** в Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="a6c2f-105">Например, вы проверяете запасы и определяете дату выполнения как одну из ключевых задач в процессе [продажи перспективному клиенту](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="a6c2f-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="a6c2f-106">Если запасов не хватает, можно оценить дату поставки на основе прогнозируемых приходов и расходов на складе.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="a6c2f-107">Можно также проверить информацию о доступных для заказа продуктов (ATP), в которой можно найти количество ATP по заранее определенной временной границе.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="a6c2f-108">Запасы в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-108">On-hand inventory</span></span>

<span data-ttu-id="a6c2f-109">В Dynamics 365 Sales добавлена новая кнопка **Запасы в наличии** в заголовке страниц **Предложения**, **Заказы** и **Накладные**.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a6c2f-110">При выборе этой кнопки появляется диалоговое окно, в котором можно указать компанию и продукт, для которого необходимо проверить запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="a6c2f-111">В этом диалоговом окне отображаются те же сведения, что и в [Запасы в наличии](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="a6c2f-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="a6c2f-112">В диалоговом окне возвращаются сведения о запасах из Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a6c2f-113">Эта информация содержит следующие количества:</span><span class="sxs-lookup"><span data-stu-id="a6c2f-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="a6c2f-114">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-114">On-hand quantity</span></span>
- <span data-ttu-id="a6c2f-115">Зарезервированное количество в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="a6c2f-116">Доступное количество в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-116">Available on-hand quantity</span></span>
- <span data-ttu-id="a6c2f-117">Заказанное количество</span><span class="sxs-lookup"><span data-stu-id="a6c2f-117">Ordered quantity</span></span>
- <span data-ttu-id="a6c2f-118">Количество в заказе</span><span class="sxs-lookup"><span data-stu-id="a6c2f-118">On-order quantity</span></span>
- <span data-ttu-id="a6c2f-119">Зарезервированное заказанное количество</span><span class="sxs-lookup"><span data-stu-id="a6c2f-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="a6c2f-120">Общее доступное количество</span><span class="sxs-lookup"><span data-stu-id="a6c2f-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="a6c2f-121">Информация о "доступно для резервирования"</span><span class="sxs-lookup"><span data-stu-id="a6c2f-121">ATP information</span></span>

<span data-ttu-id="a6c2f-122">В Sales новая кнопка **Информация ATP** была добавлена в позиции строки на страницах **Предложения**, **Заказы** и **Накладные**.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a6c2f-123">При выборе этой кнопки появляется диалоговое окно, в котором можно указать компанию, продукт, сайт запасов, склад запасов и количество заказа.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="a6c2f-124">В этом диалоговом окне используются те же настройки, что и описанные в разделе [Резервирование по заказам](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="a6c2f-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="a6c2f-125">Диалоговое окно возвращает сведения о доступности для резервирования из модуля Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="a6c2f-126">Эта информация содержит следующие количества:</span><span class="sxs-lookup"><span data-stu-id="a6c2f-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="a6c2f-127">Количество "доступно для резервирования"</span><span class="sxs-lookup"><span data-stu-id="a6c2f-127">ATP quantity</span></span>
- <span data-ttu-id="a6c2f-128">Количество прихода</span><span class="sxs-lookup"><span data-stu-id="a6c2f-128">Receipt quantity</span></span>
- <span data-ttu-id="a6c2f-129">Количество расходов</span><span class="sxs-lookup"><span data-stu-id="a6c2f-129">Issue quantity</span></span>
- <span data-ttu-id="a6c2f-130">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="a6c2f-131">Как это работает</span><span class="sxs-lookup"><span data-stu-id="a6c2f-131">How it works</span></span>

<span data-ttu-id="a6c2f-132">При выборе кнопки **Запасы в наличии** на странице **Предложения с расценками**, **Заказы** или **Накладные** выполняется вызов двойной записи в режиме реального времени в интерфейс API **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="a6c2f-133">Интерфейс API рассчитывает запасы в наличии для данного продукта.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="a6c2f-134">Результат сохраняется в таблицах **InventCDSInventoryOnHandRequestEntity** и **InventCDSInventoryOnHandEntryEntity**, а затем записывается в Dataverse двойной записью.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="a6c2f-135">Для использования этих функциональных возможностей необходимо выполнить следующие две карты двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="a6c2f-136">Пропустите начальную синхронизацию при выполнении карт.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="a6c2f-137">Записи запасов в наличии CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="a6c2f-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="a6c2f-138">Запросы запасов в наличии CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="a6c2f-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="a6c2f-139">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="a6c2f-139">Templates</span></span>
<span data-ttu-id="a6c2f-140">Для доступа к данным запасов в наличии доступны следующие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="a6c2f-141">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c2f-141">Finance and Operations apps</span></span> | <span data-ttu-id="a6c2f-142">Приложение для взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="a6c2f-142">Customer engagement app</span></span> | <span data-ttu-id="a6c2f-143">описание</span><span class="sxs-lookup"><span data-stu-id="a6c2f-143">Description</span></span> 
---|---|---
[<span data-ttu-id="a6c2f-144">Записи CDS запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="a6c2f-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="a6c2f-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="a6c2f-146">Запросы CDS запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="a6c2f-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="a6c2f-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="a6c2f-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="a6c2f-148">Записи запасов в наличии CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="a6c2f-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="a6c2f-149">Этот шаблон синхронизирует данные между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a6c2f-150">Поле Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c2f-150">Finance and Operations field</span></span> | <span data-ttu-id="a6c2f-151">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="a6c2f-151">Map type</span></span> | <span data-ttu-id="a6c2f-152">Поле взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="a6c2f-152">Customer engagement field</span></span> | <span data-ttu-id="a6c2f-153">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a6c2f-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="a6c2f-154">Запросы запасов в наличии CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="a6c2f-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="a6c2f-155">Этот шаблон синхронизирует данные между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a6c2f-156">Поле Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c2f-156">Finance and Operations field</span></span> | <span data-ttu-id="a6c2f-157">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="a6c2f-157">Map type</span></span> | <span data-ttu-id="a6c2f-158">Поле взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="a6c2f-158">Customer engagement field</span></span> | <span data-ttu-id="a6c2f-159">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a6c2f-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]