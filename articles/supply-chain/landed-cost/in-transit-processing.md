---
title: Обработка товаров в пути
description: В этой теме описывается, как работать с заказами товаров в пути. Если заказ или рейс настроены для использования обработки товаров в пути, можно выставить накладные по товарам до того, как они будут получены на складе для потребления.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 77e30f8679c9422e895432c023997b5ff4768ebd
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500412"
---
# <a name="goods-in-transit-processing"></a><span data-ttu-id="14fbe-104">Обработка товаров в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-104">Goods-in-transit processing</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="14fbe-105">В этой теме описывается, как работать с заказами товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-105">This topic describes how to work with goods-in-transit orders.</span></span> <span data-ttu-id="14fbe-106">Этот тип заказа используется только для модуля **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-106">This type of order is used only by the **Landed cost** module.</span></span> <span data-ttu-id="14fbe-107">Если заказ или рейс настроены для использования обработки товаров в пути, не нужно ждать поступления товаров на складе для выставления по ним накладных.</span><span class="sxs-lookup"><span data-stu-id="14fbe-107">When an order or voyage is set up to use goods-in-transit processing, you don't have to wait until goods are received in the warehouse before you can invoice them.</span></span> <span data-ttu-id="14fbe-108">Вместо этого по товарам выставляются накладные, когда товары отправляются со склада поставщика или порта происхождения, и финансовые затраты определяются в начале рейса.</span><span class="sxs-lookup"><span data-stu-id="14fbe-108">Instead, the goods are invoiced when they leave the vendor's warehouse or port of origin, and the financial costs are recognized when the voyage begins.</span></span> <span data-ttu-id="14fbe-109">Эта функция позволяет правильно стать владельцем запасов, так как товары часто становятся собственностью вашей организации, когда они оставляют порт отгрузки.</span><span class="sxs-lookup"><span data-stu-id="14fbe-109">This functionality lets you correctly take ownership of inventory, because goods often become the property of your organization when they leave the shipping port.</span></span>

<span data-ttu-id="14fbe-110">Когда используются заказы товаров в пути, номенклатуры с обновленной финансовой информацией принимаются на промежуточном складе, который называется складом товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-110">When goods-in-transit orders are used, the financially updated items are received in an interim warehouse that is known as a goods-in-transit warehouse.</span></span> <span data-ttu-id="14fbe-111">Затем товары остаются на этом складе до тех пор, пока они не будут получены на последнем складе назначения (то есть, на складе, указанном в строке покупки).</span><span class="sxs-lookup"><span data-stu-id="14fbe-111">The goods then stay in this warehouse until they can be received at the final destination warehouse (that is, the warehouse that is defined on the purchase line).</span></span> <span data-ttu-id="14fbe-112">Их невозможно удалить вручную.</span><span class="sxs-lookup"><span data-stu-id="14fbe-112">They can't be manually removed.</span></span>

<span data-ttu-id="14fbe-113">Пока номенклатуры находятся в пути, они недоступны в запасах и не могут комплектоваться из запасов для доставки.</span><span class="sxs-lookup"><span data-stu-id="14fbe-113">As long as the items are in transit, they aren't available in inventory and can't be picked from inventory for a delivery.</span></span> <span data-ttu-id="14fbe-114">Однако можно просмотреть запасы товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-114">However, you can view the goods-in-transit inventory.</span></span> <span data-ttu-id="14fbe-115">Можно использовать товары для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="14fbe-115">You can also use the goods for master planning.</span></span> <span data-ttu-id="14fbe-116">В этом случае в качестве ожидаемой даты, когда запасы будут доступны для потребления, следует использовать подтвержденную дату доставки в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="14fbe-116">In this case, use the confirmed delivery date on the purchase order line as the expected date when the inventory will be available for consumption.</span></span>

<span data-ttu-id="14fbe-117">В следующих разделах описана настройка, необходимая для обработки запасов, и рейсы с использованием понятия товаров в пути и функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="14fbe-117">The following sections describe the setup that is required to process inventory and voyages by using the goods-in-transit concept and functionality.</span></span>

## <a name="terms-of-delivery"></a><span data-ttu-id="14fbe-118">Условия поставки</span><span class="sxs-lookup"><span data-stu-id="14fbe-118">Terms of delivery</span></span>

<span data-ttu-id="14fbe-119">При включении модуля **Стоимость на складе** объект стандартных *условий доставки* расширяется для поддержки функции товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-119">When you enable the **Landed cost** module, the standard *terms of delivery* entity is enhanced to support the goods-in-transit feature.</span></span>

<span data-ttu-id="14fbe-120">Когда параметр **Управление товарами в пути** задан как *Да* для записи применимых условий доставки, товары помещаются на склад товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-120">When the **Goods in transit management** option is set to *Yes* for the applicable terms of delivery record, the goods are put into the goods-in-transit warehouse.</span></span> <span data-ttu-id="14fbe-121">Это действие запускается только в том случае, если поступление на склад не обрабатывается до обработки накладной.</span><span class="sxs-lookup"><span data-stu-id="14fbe-121">This action is triggered only if the inventory receipt isn't processed before an invoice is processed.</span></span> <span data-ttu-id="14fbe-122">Когда условия доставки для заказа настроены на использование товаров в пути, пользователи больше не могут разносить поступление продуктов для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="14fbe-122">When the delivery terms for an order are set to use goods in transit, users can no longer post a product receipt for the purchase order.</span></span> <span data-ttu-id="14fbe-123">В случае попытки происходит ошибка.</span><span class="sxs-lookup"><span data-stu-id="14fbe-123">If they try, an error occurs.</span></span> <span data-ttu-id="14fbe-124">В сообщении об ошибке говорится, что для продолжения необходимо использовать функции товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-124">The error message states that they must use the goods-in-transit functionality to proceed.</span></span>

<span data-ttu-id="14fbe-125">Для работы с информацией об условиях поставки для товаров в пути перейдите к **Закупки и источники \> Настройка \> Распределение \> Условия поставки**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-125">To work with delivery terms information for goods in transit, go to **Procurement and Sourcing \> Setup \> Distribution \> Terms of delivery**.</span></span> <span data-ttu-id="14fbe-126">В следующей таблице описываются поля, добавляемые модулем **Стоимость на складе** на страницу **Условия поставки** для поддержки функций товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-126">The following table describes the fields that the **Landed cost** module adds to the **Terms of delivery** page to support the goods-in-transit functionality.</span></span> <span data-ttu-id="14fbe-127">Оба поля включены в экспресс-вкладку **Общее**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-127">Both fields are on the **General** FastTab.</span></span> <span data-ttu-id="14fbe-128">Дополнительные сведения о других полях на этой странице см. в разделе [Условия поставки (форма)](https://technet.microsoft.com/library/aa575567.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fbe-128">For more information about the other fields on this page, see [Terms of delivery (form)](https://technet.microsoft.com/library/aa575567.aspx).</span></span>

| <span data-ttu-id="14fbe-129">Поле</span><span class="sxs-lookup"><span data-stu-id="14fbe-129">Field</span></span> | <span data-ttu-id="14fbe-130">описание</span><span class="sxs-lookup"><span data-stu-id="14fbe-130">Description</span></span> |
|---|---|
| <span data-ttu-id="14fbe-131">Порт отгрузки обязателен</span><span class="sxs-lookup"><span data-stu-id="14fbe-131">Shipping port mandatory</span></span> | <span data-ttu-id="14fbe-132">Установите для этого параметра значение *Да*, если порт отгрузки является обязательным, когда применяются условия поставки.</span><span class="sxs-lookup"><span data-stu-id="14fbe-132">Set this option to *Yes* if a shipping port is mandatory when the delivery terms apply.</span></span> |
| <span data-ttu-id="14fbe-133">Управление товарами в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-133">Goods in transit management</span></span> | <span data-ttu-id="14fbe-134">Установите для этого параметра значение *Да*, чтобы использовать управление товарами в пути при применении условий поставки.</span><span class="sxs-lookup"><span data-stu-id="14fbe-134">Set this option to *Yes* to use goods-in-transit management when the delivery terms apply.</span></span> |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a><span data-ttu-id="14fbe-135">Склады для товаров в пути и недопоставка</span><span class="sxs-lookup"><span data-stu-id="14fbe-135">Warehouses for goods in transit and under-delivery</span></span>

<span data-ttu-id="14fbe-136">Когда вы включаете модуль **Стоимость на складе** стандартный объект *склады* расширяется для включения выставления накладных для заказов на покупку, когда товары находятся на складе товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-136">When you enable the **Landed cost** module, the standard *warehouses* entity is enhanced to enable purchase orders to be invoiced while the goods are in a goods-in-transit warehouse.</span></span>

<span data-ttu-id="14fbe-137">Стоимость на складе добавляет два новых типа склада: *товары в пути* и *недопоставка*.</span><span class="sxs-lookup"><span data-stu-id="14fbe-137">Landed cost adds two new types of warehouse: *goods in transit* and *under-delivery*.</span></span> <span data-ttu-id="14fbe-138">Склады обоих типов могут быть выбраны как склады по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14fbe-138">Warehouses of both types can be selected as default warehouses.</span></span> <span data-ttu-id="14fbe-139">Для успешной обработки заказов товаров в пути требуется, чтобы склад товаров в пути и склад недопоставки были настроены на странице **Склады**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-139">Successful processing of goods-in-transit orders requires that both the goods-in-transit warehouse and the under-delivery warehouse be configured on the **Warehouses** page.</span></span> <span data-ttu-id="14fbe-140">Затем для каждого склада по умолчанию, который будет использоваться со стоимостью на складе товарами в пути, необходимо выбрать склад товаров в пути и склад недопоставки для доступных складов каждого типа.</span><span class="sxs-lookup"><span data-stu-id="14fbe-140">Then, for each default warehouse that will be used with Landed cost and goods in transit, the goods-in-transit warehouse and under-delivery warehouse must be selected for the available warehouses of each type.</span></span>

<span data-ttu-id="14fbe-141">Тип склада *Товары в пути*, которые будут связаны со складом товаров в пути, и этот склад будут использоваться для обработки товаров в заказах товаров в пути до их получения на конечном складе.</span><span class="sxs-lookup"><span data-stu-id="14fbe-141">The *goods in transit* warehouse type will be associated with your goods-in-transit warehouse, and that warehouse will be used to process the goods on goods-in-transit orders before they are received at the final destination warehouse.</span></span> <span data-ttu-id="14fbe-142">Как правило, одного склада товаров в пути достаточно для каждого места, если место и склад являются единственными складскими аналитиками, используемыми для управления складом.</span><span class="sxs-lookup"><span data-stu-id="14fbe-142">In general, one goods-in-transit warehouse is enough for each site if Site and Warehouse are the only inventory dimensions that are used for inventory management.</span></span> <span data-ttu-id="14fbe-143">Если также используется складская аналитика местоположения, склад товаров в пути должен быть настроен для каждой комбинации места и склада, чтобы можно было также указать местоположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14fbe-143">If the Location inventory dimension is also used, a goods-in-transit warehouse must be set up for each combination of a site and warehouse, so that the default location can also be specified.</span></span>

<span data-ttu-id="14fbe-144">Для работы с настройками товаров в пути для складов перейдите в раздел **Управление запасами \> Настройка \> Разделение запасов \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-144">To work with goods-in-transit settings for your warehouses, go to **Inventory management \> Setup \> Inventory breakdown \> Warehouses**.</span></span> <span data-ttu-id="14fbe-145">В следующей таблице описываются поля, добавляемые модулем **Стоимость на складе** на страницу **Склады** для поддержки функций товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-145">The following table describes the fields that the **Landed cost** module adds to the **Warehouses** page to support the goods-in-transit functionality.</span></span> <span data-ttu-id="14fbe-146">Оба поля находятся на экспресс-вкладке **Общее**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-146">Both fields appear on the **General** FastTab.</span></span> <span data-ttu-id="14fbe-147">Дополнительные сведения о других полях на странице см. в разделе [Склады (форма)](https://technet.microsoft.com/library/aa620570.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fbe-147">For information about the other fields on the page, see [Warehouses (form)](https://technet.microsoft.com/library/aa620570.aspx).</span></span>

| <span data-ttu-id="14fbe-148">Поле</span><span class="sxs-lookup"><span data-stu-id="14fbe-148">Field</span></span> | <span data-ttu-id="14fbe-149">описание</span><span class="sxs-lookup"><span data-stu-id="14fbe-149">Description</span></span> |
|---|---|
| <span data-ttu-id="14fbe-150">Склад товаров в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-150">Goods in transit warehouse</span></span> | <span data-ttu-id="14fbe-151">Идентификация складов товаров в пути, которые связаны с главным складом.</span><span class="sxs-lookup"><span data-stu-id="14fbe-151">Identify the goods-in-transit warehouse that is related to the main warehouse.</span></span> |
| <span data-ttu-id="14fbe-152">Склад недопоставки</span><span class="sxs-lookup"><span data-stu-id="14fbe-152">Under delivery warehouse</span></span> | <span data-ttu-id="14fbe-153">Идентификация складов недопоставки, которые связаны с главным складом.</span><span class="sxs-lookup"><span data-stu-id="14fbe-153">Identify the under-delivery warehouse that is related to the main warehouse.</span></span> |

## <a name="posting-rules-for-landed-cost"></a><span data-ttu-id="14fbe-154">Правила разноски для стоимости на складе</span><span class="sxs-lookup"><span data-stu-id="14fbe-154">Posting rules for landed cost</span></span>

<span data-ttu-id="14fbe-155">Стоимость на складе добавляет два новых правила разноски, которые можно настроить.</span><span class="sxs-lookup"><span data-stu-id="14fbe-155">Landed cost adds two new posting rules that you can configure.</span></span> <span data-ttu-id="14fbe-156">Эти правила разноски используются для финансовой разноски сумм прямых накладных заказам на покупку, чтобы определить владение товаром, когда они покидают место происхождения.</span><span class="sxs-lookup"><span data-stu-id="14fbe-156">These posting rules are used to financially post the direct purchase order invoice amounts to identify ownership of the goods when they leave the point of origin.</span></span> <span data-ttu-id="14fbe-157">Этот процесс заменяет понятие *полученных товаров без выставления накладных*, поскольку перед получением товаров выставляется накладная.</span><span class="sxs-lookup"><span data-stu-id="14fbe-157">This process replaces the concept of *goods received not invoiced*, because the goods are invoiced before they are received.</span></span> <!-- KFM: Add a link to the related scenario when available. -->

<span data-ttu-id="14fbe-158">Для работы с профилями разноски перейдите **Управление запасами \> Настройка \> Разноска \> Разноска**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-158">To work with posting profiles, go to **Inventory management \> Setup \> Posting \> Posting**.</span></span> <span data-ttu-id="14fbe-159">На вкладке **Заказ на покупку** доступны следующие новые правила разноски:</span><span class="sxs-lookup"><span data-stu-id="14fbe-159">On the **Purchase Order** tab, the following new posting rules are available:</span></span>

- <span data-ttu-id="14fbe-160">**Стоимость на складе, товары в пути** — определение правил разноски для управления товарами в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-160">**Landed cost, goods in transit** – Specify the posting rules for goods-in-transit management.</span></span>
- <span data-ttu-id="14fbe-161">**Стоимость на складе, начисление накладных расходов по затратам** — определение правил разноски для начисления накладных расходов по затратам.</span><span class="sxs-lookup"><span data-stu-id="14fbe-161">**Landed cost, cost charge accrual** – Specify the posting rules for charge account accrual.</span></span>

## <a name="goods-in-transit-orders"></a><span data-ttu-id="14fbe-162">Заказы товаров в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-162">Goods-in-transit orders</span></span>

<span data-ttu-id="14fbe-163">Можно просматривать и управлять заказами товаров в пути непосредственно в модуле **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-163">You can review and manage goods-in-transit orders directly in the **Landed cost** module.</span></span> <span data-ttu-id="14fbe-164">Заказы товаров в пути можно обрабатывать непосредственно на странице **Заказы товаров в пути**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-164">You can process goods-in-transit orders directly from the **Goods in transit orders** page.</span></span> <span data-ttu-id="14fbe-165">Вместо этого можно перейти к рейсу, связанному с заказами товаров в пути, и обработать весь рейс, контейнер отгрузки или лист.</span><span class="sxs-lookup"><span data-stu-id="14fbe-165">Alternatively, you can go to the voyage that is associated with the goods-in-transit orders, and process the whole voyage, shipping container, or folio.</span></span> <span data-ttu-id="14fbe-166">При выставлении накладной по рейсу и создании заказов товаров в пути создается новый заказ товаров в пути для каждой комбинации запасов и складских аналитик, связанных со строкой заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="14fbe-166">When you invoice a voyage and create goods-in-transit orders, a new goods-in-transit order is created for each combination of inventory and inventory dimensions that is associated with the purchase order line.</span></span>

<span data-ttu-id="14fbe-167">Для управления товарами в пути стоимость на складе используется двухэтапную процедуру:</span><span class="sxs-lookup"><span data-stu-id="14fbe-167">To manage goods in transit, Landed cost uses a two-step procedure:</span></span>

1. <span data-ttu-id="14fbe-168">Номенклатура получается, когда накладная запасов обрабатывается и присваивается статус *В пути*.</span><span class="sxs-lookup"><span data-stu-id="14fbe-168">An item is received when a stock invoice is processed and assigned a status of *In transit*.</span></span>
1. <span data-ttu-id="14fbe-169">Заказ товаров в пути обрабатывается на странице **Заказы товаров в пути**, а затем получается на складе, указанном в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="14fbe-169">The goods-in-transit order is processed on the **Goods in transit orders** page and then received in the warehouse that is specified on the purchase order.</span></span> <span data-ttu-id="14fbe-170">В этот момент статус изменится на *Получено*.</span><span class="sxs-lookup"><span data-stu-id="14fbe-170">At that point, the status is changed to *Received*.</span></span>

<span data-ttu-id="14fbe-171">Для работы с заказами товаров в пути перейдите **Стоимость на складе \> Периодические задачи \> Заказы товаров в пути**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-171">To work with goods-in-transit orders, go to **Landed cost \> Periodic tasks \> Goods in transit orders**.</span></span>

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a><span data-ttu-id="14fbe-172">Получение запасов со склада товаров в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-172">Receiving stock from the goods-in-transit warehouse</span></span>

<span data-ttu-id="14fbe-173">Можно получать товары из заказа товаров в пути различными способами, в зависимости от настроек системы.</span><span class="sxs-lookup"><span data-stu-id="14fbe-173">You can receive goods from a goods-in-transit order in many ways, depending on the setup of your system.</span></span>

### <a name="in-transit-receiving"></a><span data-ttu-id="14fbe-174">Получение в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-174">In-transit receiving</span></span>

<span data-ttu-id="14fbe-175">Можно выполнить получение в пути на любой из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="14fbe-175">You can do in-transit receiving from any of the following pages:</span></span>

- <span data-ttu-id="14fbe-176">На странице **Товары в пути** выберите строку, а затем на панели операций выберите **Получить**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-176">On the **Goods in transit orders** page, select the line, and then, on the Action Pane, select **Receive**.</span></span>
- <span data-ttu-id="14fbe-177">На странице **Все рейсы** выберите или откройте рейс.</span><span class="sxs-lookup"><span data-stu-id="14fbe-177">On the **All voyages** page, select or open a voyage.</span></span> <span data-ttu-id="14fbe-178">Затем на панели операций на вкладке **Управление** в группе **Товары в пути** выберите **Получить товары в пути**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-178">Then, on the Action Pane, on the **Manage** tab, in the **Goods in transit** group, select **Receive goods in transit**.</span></span>
- <span data-ttu-id="14fbe-179">На странице **Все контейнеры отгрузки** выберите или откройте контейнер отгрузки.</span><span class="sxs-lookup"><span data-stu-id="14fbe-179">On the **All shipping containers** page, select or open a shipping container.</span></span> <span data-ttu-id="14fbe-180">Затем на панели операций на вкладке **Управление** в группе **Товары в пути** выберите **Получить товары в пути**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-180">Then, on the Action Pane, on the **Manage** tab, in the **Goods in transit** group, select **Receive goods in transit**.</span></span>
- <span data-ttu-id="14fbe-181">На странице **Все листы** выберите или откройте лист.</span><span class="sxs-lookup"><span data-stu-id="14fbe-181">On the **All folios** page, select or open a folio.</span></span> <span data-ttu-id="14fbe-182">Затем на панели операций на вкладке **Управление** в группе **Товары в пути** выберите **Получить товары в пути**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-182">Then, on the Action Pane, on the **Manage** tab, in the **Goods in transit** group, select **Receive goods in transit**.</span></span>

> [!NOTE]
> <span data-ttu-id="14fbe-183">Получение в пути обычно используется в ситуациях, когда местоположения и отслеживание партий/серийных номеров не используются.</span><span class="sxs-lookup"><span data-stu-id="14fbe-183">In-transit receiving is generally used in situations where locations and batch/serial tracking aren't used.</span></span>

### <a name="arrival-journal"></a><span data-ttu-id="14fbe-184">Журнал прибытия</span><span class="sxs-lookup"><span data-stu-id="14fbe-184">Arrival journal</span></span>

<span data-ttu-id="14fbe-185">Можно также получать товары путем создания журнала прибытия.</span><span class="sxs-lookup"><span data-stu-id="14fbe-185">You can also receive goods by creating an arrival journal.</span></span> <span data-ttu-id="14fbe-186">Можно создать журнал прибытия непосредственно на странице рейса.</span><span class="sxs-lookup"><span data-stu-id="14fbe-186">You can create an arrival journal directly from the voyage page.</span></span> <span data-ttu-id="14fbe-187">Рекомендации, установленные организацией, определяют, используется ли для получения товаров журнал прибытия.</span><span class="sxs-lookup"><span data-stu-id="14fbe-187">The best practices that your organization has established determine whether the arrival journal is used to receive goods.</span></span>

1. <span data-ttu-id="14fbe-188">Откройте рейс, контейнер или лист.</span><span class="sxs-lookup"><span data-stu-id="14fbe-188">Open the voyage, container, or folio.</span></span>
1. <span data-ttu-id="14fbe-189">В области действий на вкладке **Управление** в группе **Функции** выберите **Создать журнал прибытия**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-189">On the Action Pane, on the **Manage** tab, in the **Functions** group, select **Create arrival journal**.</span></span>
1. <span data-ttu-id="14fbe-190">В диалоговом окне **Создание журнала прибытия** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="14fbe-190">In the **Create arrival journal** dialog box, set the following values:</span></span>
    - <span data-ttu-id="14fbe-191">**Инициализировать количество** — установите для этого параметра значение *Да*, чтобы задать количество в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-191">**Initialize quantity** – Set this option to *Yes* to set the quantity from the in-transit quantity.</span></span> <span data-ttu-id="14fbe-192">Если для этого параметра установлено значение *Нет*, количество по умолчанию не задается из строках товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-192">If this option is set to *No*, no default quantity is set from the goods-in-transit lines.</span></span>
    - <span data-ttu-id="14fbe-193">**Создание из товаров в пути** — настройте этот параметр как *Да*, чтобы получить количества из выбранных строк в пути для выбранного рейса, контейнера или листа.</span><span class="sxs-lookup"><span data-stu-id="14fbe-193">**Create from goods in transit** - Set this option to *Yes* to take quantities from the selected in-transit lines for the selected voyage, container, or folio.</span></span>
    - <span data-ttu-id="14fbe-194">**Создать из строк заказа** — установите этот параметр как *Да*, чтобы задать количество по умолчанию в журнале прибытия из строк заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="14fbe-194">**Create from order lines** – Set this option to *Yes* to set the default quantity in the arrival journal from the purchase order lines.</span></span> <span data-ttu-id="14fbe-195">Количество по умолчанию в журнале прибытия можно настроить таким образом, только если количество в строке заказа на покупку совпадает с количеством в заказе товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-195">The default quantity in the arrival journal can be set in this way only if the quantity on the purchase order line matches the quantity on the goods-in-transit order.</span></span>

1. <span data-ttu-id="14fbe-196">Обработайте журнал прибытия, как описано в разделе [Регистрация прихода номенклатуры при помощи журнала прихода номенклатур](https://technet.microsoft.com/library/aa571129.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fbe-196">Process the arrival journal as described in [Register item receipts with an item arrival journal](https://technet.microsoft.com/library/aa571129.aspx).</span></span>

> [!NOTE]
> <span data-ttu-id="14fbe-197">Журнал прибытия обычно используется в ситуациях, когда используются местоположения, отслеживание партий/серийных номеров, но управление складом не используется.</span><span class="sxs-lookup"><span data-stu-id="14fbe-197">The arrival journal is generally used in situations where locations and batch/serial tracking are used, but warehouse management isn't used.</span></span>
>
> <span data-ttu-id="14fbe-198">Ячейки приемки по умолчанию не должны указываться в строках заказа, если в журнале прибытия будет указано местоположение размещения.</span><span class="sxs-lookup"><span data-stu-id="14fbe-198">Default receipt locations should not be specified on the order lines if a putaway location will be specified in the arrival journal.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="14fbe-199">Управление складом</span><span class="sxs-lookup"><span data-stu-id="14fbe-199">Warehouse management</span></span>

<span data-ttu-id="14fbe-200">При включении модуля **Стоимость на складе** несколько страниц в модуле **Управление складом** изменяются таким образом, что обработка заказов (в частности, обработка товаров в пути) может быть выполнена через модуль **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-200">When you enable the **Landed cost** module, several pages in the **Warehouse management** module are modified so that order processing (specifically, goods-in-transit processing) can be done through the **Landed cost** module.</span></span> <span data-ttu-id="14fbe-201">В этом разделе описываются поля и процессы, добавленные в модуль **Управление складом**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-201">This section outlines the fields and processes that are added in the **Warehouse management** module.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="14fbe-202">Пункты меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="14fbe-202">Mobile device menu items</span></span>

<span data-ttu-id="14fbe-203">Товары могут быть получены с помощью мобильного устройства, при условии, что меню мобильного устройства и модуль **Управление складом** настроены на получение товаров в заказе товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-203">Goods can be received by using a mobile device, provided that the mobile device menu and **Warehouse management** module have been set up to receive goods on a goods-in-transit order.</span></span> <span data-ttu-id="14fbe-204">В этом разделе описывается настройка, связанная с получением товаров в пути.</span><span class="sxs-lookup"><span data-stu-id="14fbe-204">This section describes the setup that is associated with goods-in-transit receiving.</span></span>

<span data-ttu-id="14fbe-205">Для настройки мобильных устройств для обработки товаров в пути перейдите на страницу **Управление складом \> Настройка \> Мобильное устройство \> Элементы меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-205">To set up mobile devices for goods-in-transit processing, go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>

<span data-ttu-id="14fbe-206">Стоимость на складе добавляет следующие процессы создания работ к пунктам меню мобильного устройства для поддержки обработки товаров в пути:</span><span class="sxs-lookup"><span data-stu-id="14fbe-206">Landed cost adds the following work creation processes to the mobile device menu items to support goods-in-transit processing:</span></span>

- <span data-ttu-id="14fbe-207">Получение номенклатуры товаров в пути</span><span class="sxs-lookup"><span data-stu-id="14fbe-207">Goods in transit item receiving</span></span>
- <span data-ttu-id="14fbe-208">Получение номенклатуры товаров в пути и размещение</span><span class="sxs-lookup"><span data-stu-id="14fbe-208">Goods in transit item receiving and putaway</span></span>

<span data-ttu-id="14fbe-209">Настройки конфигурации для этих процессов похожи на настройки для [процессов получения заказа на покупку и создания работы размещения](https://technet.microsoft.com/library/dn553216.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fbe-209">The configuration settings for these processes resemble the settings for the [purchase order receive and putaway work creation processes](https://technet.microsoft.com/library/dn553216.aspx).</span></span> <span data-ttu-id="14fbe-210">Однако процесс *Получение номенклатуры товаров в пути и размещение* также добавляют следующее поле.</span><span class="sxs-lookup"><span data-stu-id="14fbe-210">However, the *Goods in transit item receiving and putaway* process also adds the following field.</span></span>

- <span data-ttu-id="14fbe-211">**Разрешить заполнение контейнера отгрузки** — если этот параметр задан как *Да*, то после завершения работы размещения приложение склада предоставит дополнительный параметр **Контейнер отгрузки заполнен**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-211">**Enable shipping container complete** – If this option is set to *Yes*, when the putaway work is completed, the warehouse app will provide an additional option that is named **Shipping container complete**.</span></span> <span data-ttu-id="14fbe-212">Когда выбран этот параметр, работнику будет предложено подтвердить заполнение контейнера.</span><span class="sxs-lookup"><span data-stu-id="14fbe-212">When that option is selected, the worker will be asked to confirm that the container is complete.</span></span> <span data-ttu-id="14fbe-213">В этот момент все недоплаты будут обрабатываться как недостаточная проводка.</span><span class="sxs-lookup"><span data-stu-id="14fbe-213">At that point, all short receipts will be processed as an under transaction.</span></span>

### <a name="location-directives"></a><span data-ttu-id="14fbe-214">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="14fbe-214">Location directives</span></span>

<span data-ttu-id="14fbe-215">Стоимость на складе добавляет новый тип заказа на работу с именем *Товары в пути* на страницу **Директивы местонахождений**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-215">Landed cost adds a new work order type that is named *Goods in transit* to the **Location directives** page.</span></span> <span data-ttu-id="14fbe-216">Этот тип заказа на работу должен быть сконфигурирован таким же образом, как и [типы заказов на работу заказа на покупку](https://technet.microsoft.com/library/dn553184.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fbe-216">This work order type should be configured in the same manner as the [purchase order work order types](https://technet.microsoft.com/library/dn553184.aspx).</span></span>

### <a name="work-templates"></a><span data-ttu-id="14fbe-217">Шаблоны работ</span><span class="sxs-lookup"><span data-stu-id="14fbe-217">Work templates</span></span>

<span data-ttu-id="14fbe-218">Стоимость на складе добавляет новый тип заказа на работу с именем *Товары в пути* на страницу **Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="14fbe-218">Landed cost adds a new work order type that is named *Goods in transit* to the **Work templates** page.</span></span> <span data-ttu-id="14fbe-219">Этот тип заказа на работу должен быть сконфигурирован таким же образом, как и [шаблоны работы заказа на покупку](https://technet.microsoft.com/library/dn553184.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fbe-219">This work order type should be configured in the same manner as the [purchase order work templates](https://technet.microsoft.com/library/dn553184.aspx).</span></span>
