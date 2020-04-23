---
title: Гибкая политика резервирования аналитик на уровне склада
description: В этой теме описывается политика резервирования запасов, которая позволяет компаниям продавать продукты с отслеживанием партий и выполнять логистику в качестве конкретных партий резервирования операций с WMS для заказов на продажу клиентов, даже если иерархия резервирования, связанная с продуктами, запрещает резервирование конкретных партий.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0fe9ed9f2bebe8683f3b8bb37b33e8a63b9521f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205675"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="1d73b-103">Гибкая политика резервирования аналитик на уровне склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d73b-104">Когда иерархия резервирования запасов типа "партия-ниже\[местоположение\]" связана с продуктами, компании, которые продают продукты с отслеживанием партий и выполняют свою логистику в качестве операций, включенных для системы управления складом Microsoft Dynamics 365 (WMS), не могут резервировать отдельные партии этих продуктов для заказов на продажу для клиентов.</span><span class="sxs-lookup"><span data-stu-id="1d73b-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="1d73b-105">В этой теме описывается политика резервирования запасов, которая позволяет этим компаниям резервировать отдельные партии, даже если продукты связаны с иерархией резервирования "партия-ниже\[местоположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="1d73b-106">Иерархия резервирования запасов</span><span class="sxs-lookup"><span data-stu-id="1d73b-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="1d73b-107">В этом разделе содержится сводная информация о существующей иерархии резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="1d73b-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="1d73b-108">Основное внимание уделяется тому, как обрабатываются отслеживаемые партиями и последовательно отслеживаемые номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1d73b-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="1d73b-109">Иерархия резервирования запасов указывает, по мере отношения к аналитиками хранения, как заказ на спрос переносит обязательные аналитики сайта, склада и статус запасов, в то время как логика склада отвечает за назначение местоположения запрошенным количествам и резервирование местоположения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="1d73b-110">Другими словами, во взаимодействии между заказом спроса и складскими операциями должен быть заказ спроса, чтобы указать, откуда заказ должен быть отгружен (то есть, какой сайт и склад).</span><span class="sxs-lookup"><span data-stu-id="1d73b-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="1d73b-111">Склад затем полагается на логику для поиска требуемого количества на локальном складе.</span><span class="sxs-lookup"><span data-stu-id="1d73b-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="1d73b-112">Однако, чтобы отразить операционную модель бизнеса, аналитики отслеживания (номера партии и серийные номера) должно обладать большей гибкостью.</span><span class="sxs-lookup"><span data-stu-id="1d73b-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="1d73b-113">Иерархия резервирования запасов может соответствовать сценариям, в которых действуют следующие условия:</span><span class="sxs-lookup"><span data-stu-id="1d73b-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="1d73b-114">Деловые операции основаны на складских операциях для управления комплектацией количеств, которые содержат партии или серийные номера после того, как количества найдены в складских пространствах хранения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="1d73b-115">Эта модель часто называется *партия-ниже\[местоположение\]*.</span><span class="sxs-lookup"><span data-stu-id="1d73b-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="1d73b-116">Она обычно используется, когда идентификация партии или серийного номера продукта не важна для клиентов, которые размещают запрос для компании, осуществляющей продажу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="1d73b-117">Если партии или серийные номера являются частью спецификации заказа клиента и они записаны в заказе на спрос, складские операции, которые находят количества на складе, ограничиваются указанными запрошенными номерами и не могут изменять их.</span><span class="sxs-lookup"><span data-stu-id="1d73b-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="1d73b-118">Эта модель часто называется *партия-выше\[местоположение\]*.</span><span class="sxs-lookup"><span data-stu-id="1d73b-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="1d73b-119">В этих сценариях задача состоит в том, чтобы только одна иерархия резервирования запасов была назначена одному выпущенному продукту.</span><span class="sxs-lookup"><span data-stu-id="1d73b-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="1d73b-120">Таким образом, чтобы WMS обрабатывала отслеживаемые номенклатуры, после того, как назначение иерархии определяет, когда должны быть зарезервированы номер партии или серийный номер (когда используется заказ на спрос или в ходе комплектации по отгрузочной накладной), это время не может быть изменено специальным образом.</span><span class="sxs-lookup"><span data-stu-id="1d73b-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="1d73b-121">Гибкое резервирование для номенклатур, отслеживаемых партиями</span><span class="sxs-lookup"><span data-stu-id="1d73b-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="1d73b-122">Бизнес-сценарий</span><span class="sxs-lookup"><span data-stu-id="1d73b-122">Business scenario</span></span>

<span data-ttu-id="1d73b-123">В этом сценарии компания использует стратегию запасов, когда готовые товары отслеживаются по номерам партий.</span><span class="sxs-lookup"><span data-stu-id="1d73b-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="1d73b-124">Эта компания также использует рабочую нагрузку WMS.</span><span class="sxs-lookup"><span data-stu-id="1d73b-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="1d73b-125">Поскольку в этой рабочей нагрузке используется хорошо подготовленная логика для планирования и выполнения операций комплектации и отгрузки склада для номенклатур с поддержкой партий, большая часть готовых номенклатур связана с иерархией резервирования запасов склада "партия-ниже\[расположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="1d73b-126">Преимуществом этого типа настройки операций является то, что решения (которые являются эффективными решениями резервирования) о том, какие партии необходимо скомплектовать, и где их поместить на склад, откладываются до начала операции комплектации склада.</span><span class="sxs-lookup"><span data-stu-id="1d73b-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="1d73b-127">Они не выполняются при размещении заказа клиента.</span><span class="sxs-lookup"><span data-stu-id="1d73b-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="1d73b-128">Несмотря на то что иерархия резервирования "партия-ниже\[местоположение\]" хорошо подходит для бизнес-целей компании, многие из привычных клиентов компании требуют наличия той же партии, которую они ранее купили, при повторном заказе.</span><span class="sxs-lookup"><span data-stu-id="1d73b-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="1d73b-129">Таким образом, компания ищет гибкость в способе обработки правил резервирования партии, чтобы в зависимости от запроса клиента на одну и ту же номенклатуру, выполняются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="1d73b-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="1d73b-130">Номер партии может записываться и резервироваться, когда заказ извлекается с помощью обработчика продаж, и его нельзя изменить во время складских операций и/или передать к другой запрос.</span><span class="sxs-lookup"><span data-stu-id="1d73b-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="1d73b-131">Это позволяет гарантировать отгрузку заказанного номера партии клиенту.</span><span class="sxs-lookup"><span data-stu-id="1d73b-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="1d73b-132">Если номер партии неважен для клиента, складские операции могут определить номер партии во время комплектации, после того как регистрация и резервирование заказа на продажу выполнены.</span><span class="sxs-lookup"><span data-stu-id="1d73b-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="1d73b-133">Разрешение резервирования определенной партии по заказу на продажу</span><span class="sxs-lookup"><span data-stu-id="1d73b-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="1d73b-134">Для обеспечения необходимой гибкости в поведении резервирования партий номенклатур, связанных с иерархией резервирования запасов "партия-ниже\[местоположение\]", менеджеры по складу должны установить флажок **Разрешить резервирование заказа по заказу на спрос** для уровня **Номер партии** на странице **Иерархии резервирования запасов**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Обеспечение гибкости иерархии резервирования запасов](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="1d73b-136">Когда выбран уровень **Номер партии** в иерархии, будут автоматически выбраны все аналитики выше этого уровня и до уровня **Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="1d73b-137">(По умолчанию выбираются все аналитики выше уровня **Местоположение**.) Это поведение отражает логику, в которой все аналитики в диапазоне между номером партии и местоположением также автоматически резервируются после резервирования определенного номера партии в строке заказа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="1d73b-138">Флажок **Разрешить резервирование заказа по заказу на спрос** применяется только для уровней иерархии резервирования, расположенных ниже аналитики местоположения склада.</span><span class="sxs-lookup"><span data-stu-id="1d73b-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="1d73b-139">**Номер партии** — это единственный уровень в иерархии, открытый для политики гибкого резервирования.</span><span class="sxs-lookup"><span data-stu-id="1d73b-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="1d73b-140">Другими словами, невозможно установить флажок **Разрешить резервирование заказа по заказу на спрос** для уровня **Местоположение**, **Грузоместо** или **Серийный номер**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="1d73b-141">Если иерархия резервирования включает аналитику серийного номера (которая должна быть ниже уровня **Номер партии**) и если для номера партии включено резервирование определенной партии, система будет продолжать обрабатывать резервирование серийных номеров и операции комплектации на основе правил, которые применяются к политике резервирования "серийный-ниже\[местоположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="1d73b-142">В любой момент можно разрешить резервирование для существующей иерархии резервирования "партия-ниже\[местоположение\]" в вашем развертывании.</span><span class="sxs-lookup"><span data-stu-id="1d73b-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="1d73b-143">Это изменение не повлияет на резервирования и открытые складские работы, которые были созданы до того, как было внесено изменение.</span><span class="sxs-lookup"><span data-stu-id="1d73b-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="1d73b-144">Однако флажок **Разрешить резервирование заказа по заказу на спрос** не может быть снят, если для одной или нескольких номенклатур, связанных с этой иерархией резервирования, существуют проводки по запасам с типом выпуска **Зарезервировано в заказанных**, **Физически зарезервировано** или **Заказно**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="1d73b-145">Если существующая иерархия резервирования номенклатуры не разрешает спецификацию партии в заказе, ее можно переназначить в иерархию резервирования, которая поддерживает спецификацию партии при условии, что структура уровня иерархии одинакова в обеих иерархиях.</span><span class="sxs-lookup"><span data-stu-id="1d73b-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="1d73b-146">Для выполнения повторного назначения используется функция **Изменить иерархию резервирований для номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="1d73b-147">Это изменение может быть уместным, если необходимо защитить гибкое резервирование партии для подмножества номенклатур с отслеживанием партий, но разрешить для оставшейся части портфеля продуктов.</span><span class="sxs-lookup"><span data-stu-id="1d73b-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="1d73b-148">Независимо от того, установлен ли флажок **Разрешить резервирование заказа по заказу на спрос**, если не требуется зарезервировать конкретный номер партии для номенклатуры в строке заказа, будет применяться логика складских операций по умолчанию, которая является действительной для иерархии резервирования "партия-ниже\[местоположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="1d73b-149">Резервирование конкретного номера партии для заказа клиента</span><span class="sxs-lookup"><span data-stu-id="1d73b-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="1d73b-150">После того, как иерархия резервирования запасов "партия-ниже\[местоположение\]" номенклатуры с отслеживаемой партией, настроена на разрешение резервирования конкретных номеров партий по заказам на продажу, обработчики заказов на продажу могут взять заказы клиентов для одной и той же номенклатуры одним из следующих способов, в зависимости от запроса клиента:</span><span class="sxs-lookup"><span data-stu-id="1d73b-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="1d73b-151">**Ввод сведений о заказе без указания номера партии** — этот подход должен использоваться, когда спецификация партии продукта не имеет важности для клиента.</span><span class="sxs-lookup"><span data-stu-id="1d73b-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="1d73b-152">Все существующие процессы, связанные с обработкой заказа этого типа, не изменятся в системе.</span><span class="sxs-lookup"><span data-stu-id="1d73b-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="1d73b-153">При этом не требуются никаких дополнительных действий для части пользователей.</span><span class="sxs-lookup"><span data-stu-id="1d73b-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="1d73b-154">**Ввод сведений о заказе и резервирование определенного номера партии** — этот подход должен использоваться, когда клиент запрашивает конкретную партию.</span><span class="sxs-lookup"><span data-stu-id="1d73b-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="1d73b-155">Обычно клиенты запрашивают конкретную партию, когда они повторно заказывают ранее приобретенный продукт.</span><span class="sxs-lookup"><span data-stu-id="1d73b-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="1d73b-156">Этот тип резервирования с учетом партии называется *резервированием с подтверждением по заказу*.</span><span class="sxs-lookup"><span data-stu-id="1d73b-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="1d73b-157">Следующий набор правил допустим, когда количества обработаны, а номер партии фиксируется в конкретном заказе:</span><span class="sxs-lookup"><span data-stu-id="1d73b-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="1d73b-158">Чтобы разрешить резервирование определенного номера партии для номенклатуры в политике резервирования "партия-ниже\[местоположение\]", система должна зарезервировать все аналитики вплоть до местоположения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="1d73b-159">Этот диапазон обычно включает в себя аналитику грузоместа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="1d73b-160">Директивы местоположения не используются при создании операций комплектации для строки продаж, использующей резервирование с подтверждением по заказу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="1d73b-161">Во время обработки на складе работ для партий с подтверждением по заказу, ни пользователь, ни система не смогут изменить номер партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="1d73b-162">(Эта обработка включает обработку исключений.)</span><span class="sxs-lookup"><span data-stu-id="1d73b-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="1d73b-163">В следующем примере показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="1d73b-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1d73b-164">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="1d73b-164">Example scenario</span></span>

<span data-ttu-id="1d73b-165">Для этого примера необходимо установить демонстрационные данные, а также необходимо использовать компанию **USMF** с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="1d73b-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="1d73b-166">Настройка иерархии резервирования запасов для разрешения резервирования с учетом партии</span><span class="sxs-lookup"><span data-stu-id="1d73b-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="1d73b-167">Перейдите **Управление складом** \> **Настройка** \> **Запасы \> Иерархия резервирования**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="1d73b-168">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-168">Select **New**.</span></span>
3. <span data-ttu-id="1d73b-169">В поле **Имя** введите имя (например, **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="1d73b-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="1d73b-170">В поле **Описание** введите описание (например, **партия-ниже, гибкая**).</span><span class="sxs-lookup"><span data-stu-id="1d73b-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="1d73b-171">В поле **Выбрано** выберите **Серийный номер** и **Владелец**, а затем нажмите кнопку со стрелкой влево, чтобы переместить их поле **Доступно**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="1d73b-172">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-172">Select **OK**.</span></span>
7. <span data-ttu-id="1d73b-173">В строке уровня аналитики **Номер партии** установите флажок **Разрешить резервирование заказа по заказу на спрос**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="1d73b-174">Уровни **Грузоместо** и **Местонахождение** выбираются автоматически, и снять флажки для них нельзя.</span><span class="sxs-lookup"><span data-stu-id="1d73b-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="1d73b-175">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="1d73b-176">Создание нового выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="1d73b-176">Create a new released product</span></span>

1. <span data-ttu-id="1d73b-177">Задайте три основных параметра данных продукта, используя следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1d73b-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="1d73b-178">В поле **Группа аналитик хранения** выберите **Ware**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="1d73b-179">В поле **Группа аналитик отслеживания** выберите **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="1d73b-180">В форме **Иерархия резервирования** выберите **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="1d73b-181">Создайте два номера партии, например **B11** и **B22**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="1d73b-182">Добавьте количество номенклатур в запасы в наличии с использованием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1d73b-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="1d73b-183">Склад</span><span class="sxs-lookup"><span data-stu-id="1d73b-183">Warehouse</span></span> | <span data-ttu-id="1d73b-184">Номер пачки</span><span class="sxs-lookup"><span data-stu-id="1d73b-184">Batch number</span></span> | <span data-ttu-id="1d73b-185">Местоположение</span><span class="sxs-lookup"><span data-stu-id="1d73b-185">Location</span></span> | <span data-ttu-id="1d73b-186">Грузоместо</span><span class="sxs-lookup"><span data-stu-id="1d73b-186">License plate</span></span> | <span data-ttu-id="1d73b-187">Количество</span><span class="sxs-lookup"><span data-stu-id="1d73b-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="1d73b-188">24</span><span class="sxs-lookup"><span data-stu-id="1d73b-188">24</span></span>        | <span data-ttu-id="1d73b-189">B11</span><span class="sxs-lookup"><span data-stu-id="1d73b-189">B11</span></span>          | <span data-ttu-id="1d73b-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="1d73b-190">BULK-001</span></span> | <span data-ttu-id="1d73b-191">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-191">None</span></span>          | <span data-ttu-id="1d73b-192">10</span><span class="sxs-lookup"><span data-stu-id="1d73b-192">10</span></span>       |
    | <span data-ttu-id="1d73b-193">24</span><span class="sxs-lookup"><span data-stu-id="1d73b-193">24</span></span>        | <span data-ttu-id="1d73b-194">B11</span><span class="sxs-lookup"><span data-stu-id="1d73b-194">B11</span></span>          | <span data-ttu-id="1d73b-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="1d73b-195">FL-001</span></span>   | <span data-ttu-id="1d73b-196">LP11</span><span class="sxs-lookup"><span data-stu-id="1d73b-196">LP11</span></span>          | <span data-ttu-id="1d73b-197">10</span><span class="sxs-lookup"><span data-stu-id="1d73b-197">10</span></span>       |
    | <span data-ttu-id="1d73b-198">24</span><span class="sxs-lookup"><span data-stu-id="1d73b-198">24</span></span>        | <span data-ttu-id="1d73b-199">B22</span><span class="sxs-lookup"><span data-stu-id="1d73b-199">B22</span></span>          | <span data-ttu-id="1d73b-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="1d73b-200">FL-002</span></span>   | <span data-ttu-id="1d73b-201">LP22</span><span class="sxs-lookup"><span data-stu-id="1d73b-201">LP22</span></span>          | <span data-ttu-id="1d73b-202">10</span><span class="sxs-lookup"><span data-stu-id="1d73b-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="1d73b-203">Ввод сведений о заказах на продажу</span><span class="sxs-lookup"><span data-stu-id="1d73b-203">Enter sales order details</span></span>

1. <span data-ttu-id="1d73b-204">Перейдите в раздел **Продажи и маркетинг** \> **Заказы на продажу** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="1d73b-205">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-205">Select **New**.</span></span>
3. <span data-ttu-id="1d73b-206">В заголовке заказа на продажу в поле **Счет клиента** введите **US-003**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="1d73b-207">Добавьте строку для новой номенклатуры и введите **10** в качестве количества.</span><span class="sxs-lookup"><span data-stu-id="1d73b-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="1d73b-208">Убедитесь, что в поле **Склад** задано значение **24**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="1d73b-209">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы**, а затем в группе **Поддержка** выберите **Резервирование партии**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="1d73b-210">На странице **Резервирование партии** отображается список партий, доступных для резервирования для данной строки заказа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="1d73b-211">В данном примере отображается количество **20** для номера партии **B11** и количество **10** для номера партии **B22**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="1d73b-212">Обратите внимание, что страница **Резервирование партии** не может быть доступна из строки, если номенклатура в этой строке связана с иерархией резервирования "партия-ниже\[местоположение\]", если только она не настроена для разрешения резервирования с учетом партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1d73b-213">Чтобы зарезервировать конкретную партию для заказа на продажу, необходимо использовать страницу **Резервирование партии**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="1d73b-214">Если номер партии вводится непосредственно в строку заказа на продажу, система ведет себя так, как будто вы ввели конкретное значение для номенклатуры, в соответствии с политикой резервирования "партия-ниже\[местоположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="1d73b-215">При сохранении строки вы получите предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="1d73b-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="1d73b-216">Если вы подтверждаете, что номер партии должен быть указан непосредственно в строке заказа, эта строка не будет обрабатываться обычной логикой управления складом.</span><span class="sxs-lookup"><span data-stu-id="1d73b-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="1d73b-217">Если количество резервируется со страницы **Резервирование**, никакая специальная партия не будет зарезервирована, и выполнение складских операций для этой строки будет соответствовать правилам, которые применимы к политике резервирования "партия-ниже\[местоположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="1d73b-218">Как правило, эта страница работает и взаимодействует так же, как с номенклатурами со связанной иерархией резервирования типа "партия-ниже\[местоположение\]".</span><span class="sxs-lookup"><span data-stu-id="1d73b-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="1d73b-219">Однако применяются следующие исключения:</span><span class="sxs-lookup"><span data-stu-id="1d73b-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="1d73b-220">На экспресс-вкладке **Номера партий, связанные со строкой источника** показаны номера партий, зарезервированные для данной строки заказа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="1d73b-221">Значения партии в сетке будут отображаться в рамках цикла выполнения строки заказа, включая этапы обработки склада.</span><span class="sxs-lookup"><span data-stu-id="1d73b-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="1d73b-222">Напротив, на экспресс-вкладке **Обзор** регулярное резервирование строки заказа (то есть резервирование, выполняемое для аналитик выше уровня **Местоположение**) отображается в сетке вплоть до момента создания складских работ.</span><span class="sxs-lookup"><span data-stu-id="1d73b-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="1d73b-223">После этого рабочий объект занимает резервирование строки, и резервирование строки больше не отображается на странице.</span><span class="sxs-lookup"><span data-stu-id="1d73b-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="1d73b-224">Экспресс-вкладка **Номера партий, связанные со строкой источника** гарантирует, что обработчик заказов на продажу сможет просматривать номера партий, которые были зафиксированы в заказе клиента в любой момент во время его жизненного цикла вплоть до выставления накладной.</span><span class="sxs-lookup"><span data-stu-id="1d73b-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="1d73b-225">В дополнение к резервированию определенной партии пользователь может вручную выбрать конкретное местоположение и грузоместо для партии вместо того, чтобы дать системе выбрать их автоматически.</span><span class="sxs-lookup"><span data-stu-id="1d73b-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="1d73b-226">Эта возможность связана с разработкой механизма резервирования партий с подтверждением по заказу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="1d73b-227">Как уже было сказано, чтобы разрешить резервирование определенного номера партии для номенклатуры в политике резервирования "партия-ниже\[местоположение\]", система должна зарезервировать все аналитики вплоть до местоположения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="1d73b-228">Таким образом, работа склада будет выполнять те же аналитики хранения, которые были зарезервированы пользователями, работавшими с заказами, и она не всегда должна представлять удобное или даже возможное место хранения номенклатуры для операций комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="1d73b-229">Если обработчики заказов знают об ограничениях склада, они могут захотеть вручную выбрать определенные местоположения и грузоместа при резервировании партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="1d73b-230">В этом случае пользователь должен использовать функцию **Отобразить аналитики** в заголовке страницы и добавить в сетку местоположение и грузоместо на экспресс-вкладке **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="1d73b-231">На странице **Резервирование партии** выберите строку для партии **B11**, а затем выберите **Зарезервировать строку**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="1d73b-232">Не определена логика для назначения местоположений и грузомест во время автоматического резервирования.</span><span class="sxs-lookup"><span data-stu-id="1d73b-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="1d73b-233">Количество можно ввести вручную в поле **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="1d73b-234">Обратите внимание, что на экспресс-вкладке **Номера партий, связанные со строкой источника** партия **B11** отображается как **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Подтверждение определенного номера партии в строке заказа на продажу на странице резервирования партии](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="1d73b-236">Резервирование количества по строке заказа на продажу может выполняться в нескольких партиях.</span><span class="sxs-lookup"><span data-stu-id="1d73b-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="1d73b-237">Аналогично, резервирование одной и той же партии может быть выполнено по отношению к нескольким местоположениям и грузоместам (если для этих местоположений включены грузоместа).</span><span class="sxs-lookup"><span data-stu-id="1d73b-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="1d73b-238">Резервирование определенной партии для количества, указанного в строке заказа на продажу, также может быть частичным.</span><span class="sxs-lookup"><span data-stu-id="1d73b-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="1d73b-239">Например, общее количество единиц измерения 100 может быть зарезервировано таким образом, чтобы конкретная партия составила 20 единиц, в то время как единицы измерения 80 зарезервированы на уровне сайта и склада для любой доступной партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="1d73b-240">В этом случае WMS будет обрабатывать операции комплектации, используя две отдельные строки работы.</span><span class="sxs-lookup"><span data-stu-id="1d73b-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="1d73b-241">Щелкните **Управление сведениями о продукте** \> **Продукты** \> **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="1d73b-242">Выберите номенклатуру, а затем выберите **Управление складскими запасами** \> **Вид** \> **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Резервирование с повреждением по заказу в качестве типа складской проводки](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="1d73b-244">Просмотрите складские проводки по номенклатуре, которые связаны с резервированием строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="1d73b-245">Проводка, в которой поле **Ссылка** задано как **Заказ на продажу**, а поле **Выдача** имеет значение **Физически зарезервировано**, представляет резервирование строки заказа для складских аналитик выше уровня **Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="1d73b-246">В соответствии с иерархией резервирования запасов по номенклатуре эти аналитики являются сайтом, складом и статусом запасов.</span><span class="sxs-lookup"><span data-stu-id="1d73b-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="1d73b-247">Проводка, в которой поле **Ссылка** задано как **Резервирование с повреждением по заказу**, а поле **Выдача** имеет значение **Физически зарезервировано**, представляет резервирование строки заказа для конкретной партии и всех складских аналитик выше ее уровня.</span><span class="sxs-lookup"><span data-stu-id="1d73b-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="1d73b-248">В соответствии с иерархией резервирования запасов по номенклатуре эти аналитики являются номером партии и местоположением.</span><span class="sxs-lookup"><span data-stu-id="1d73b-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="1d73b-249">В этом примере местоположение — **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="1d73b-250">В заголовке заказа на продажу выберите **Склад** \> **Действия** \> **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="1d73b-251">Строка заказа теперь исключена и будут созданы загрузка и работа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="1d73b-252">Просмотрите и обработайте складские работы, для которых есть номера партий с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="1d73b-253">На экспресс-вкладке **Строки заказа на продажу** выберите **Склад** \> **Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="1d73b-254">Работа, обрабатывающая операцию комплектации для количеств партий, которые подтверждены в строке заказа на продажу, имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="1d73b-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="1d73b-255">Для создания работы система использует шаблоны работы, но не директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="1d73b-256">Все стандартные настройки, определенные для шаблонов работы, такие как максимальное число строк комплектации или определенная единица измерения, будут применяться для определения времени, когда создать новую работу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="1d73b-257">Однако правила, связанные с директивами местоположения для местоположений комплектации, не рассматриваются, так как резервирование по заказу уже содержит все складские аналитики.</span><span class="sxs-lookup"><span data-stu-id="1d73b-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="1d73b-258">Эти складские аналитики включают аналитики на уровне складского хранилища.</span><span class="sxs-lookup"><span data-stu-id="1d73b-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="1d73b-259">Таким образом, работа наследует эти аналитики без необходимости обращаться к директивам местоположения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="1d73b-260">Номер партии не отображается в строке комплектации (как в случае для строки работы, созданной для номенклатуры, которая связана с иерархией резервирования "партия-ниже\[местоположение\]"). Вместо этого номер партии "с номера партии" и все остальные аналитики хранения отображаются в складской проводке проводки по строкам работы, на которую имеется ссылка из соответствующих складских проводок.</span><span class="sxs-lookup"><span data-stu-id="1d73b-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Складская проводка склада для работы, созданная на основе реферирования с подтвержденным заказом](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="1d73b-262">После создания работы складская проводка номенклатуры, в которой поле **Ссылка** задано как **Резервирование с повреждением по заказу** удаляется.</span><span class="sxs-lookup"><span data-stu-id="1d73b-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="1d73b-263">Складская проводка, в которой поле **Ссылка** настроено как **Работа**, теперь содержит физическое резервирование для всех складских аналитик данного количества.</span><span class="sxs-lookup"><span data-stu-id="1d73b-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="1d73b-264">Складские операции могут продолжать обработку выполнения работы обычным способом.</span><span class="sxs-lookup"><span data-stu-id="1d73b-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="1d73b-265">Однако инструкции на мобильном устройстве будут давать указание сотруднику на комплектацию определенного номера партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="1d73b-266">В складских средах, где местоположения являются контролируемыми по грузоместу, после того как сотрудник достигнет места, в котором одна и та же партия хранится в нескольких грузоместах, он может скомплектовать из любого грузоместа, которое еще не было зарезервирована (например, другим резервированием с подтверждением по заказу или работой, созданной на основе резервирования этого типа).</span><span class="sxs-lookup"><span data-stu-id="1d73b-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="1d73b-267">Если кажется непрактичным комплектовать из местоположения, указанного в строке работы, операторы склада могут использовать одно из следующих действий для перенаправления комплектации определенной партии из более удобного местоположения:</span><span class="sxs-lookup"><span data-stu-id="1d73b-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="1d73b-268">Стандартное действие **Переопределение местонахождения** на мобильном устройстве (при условии, что для работника склада разрешена настройка **Разрешить переопределение местонахождения отгрузки**)</span><span class="sxs-lookup"><span data-stu-id="1d73b-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="1d73b-269">Действие **Изменить местонахождение** на странице **Сведения о списке работ**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="1d73b-270">На мобильном устройстве завершите комплектацию и поместите работу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="1d73b-271">Количество **10** для номера партии **B11** теперь скомплектовано для строки заказа на продажу и помещено местоположение **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="1d73b-272">На этом этапе оно готово к погрузке на грузовик и доставке по адресу клиента.</span><span class="sxs-lookup"><span data-stu-id="1d73b-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="1d73b-273">Обработка исключений складской работы, для которой есть номера партий с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="1d73b-274">Складская работа для комплектации номеров партий с подтверждением по заказу подлежит той же стандартной обработке исключений склада и действий, что и обычная работа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="1d73b-275">В общем случае можно отменить открытую работу или строку работы, поскольку она может быть прервана из-за того, что местоположение пользователя заполнено, можно скомплектовать недостающее количество номенклатуры из нескольких мест и можно обновить из-за перемещения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="1d73b-276">Аналогично, скомплектованное количество работы, которое уже было завершено, может быть уменьшено, или работа может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="1d73b-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="1d73b-277">Следующее ключевое правило применяется ко всем этим действиям по обработке исключений: номер партии, зарезервированный для клиента, никогда не может быть заменен на другой номер партии, но его аналитики хранения (местоположение и грузоместо) можно изменить с помощью обновления вручную пользователем или автоматического обновления системой.</span><span class="sxs-lookup"><span data-stu-id="1d73b-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="1d73b-278">Автоматическое обновление основано на том же случайном назначении аналитик хранения, которое применяется, когда конкретная партия была автоматически зарезервирована, но аналитики хранения не были указаны.</span><span class="sxs-lookup"><span data-stu-id="1d73b-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="1d73b-279">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="1d73b-279">Example scenario</span></span>

<span data-ttu-id="1d73b-280">Примером такого сценария является ситуация, когда ранее завершенная работа разукомплектована с помощью функции **Уменьшить скомплектованное количество**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="1d73b-281">В этом примере продолжается предыдущий пример в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1d73b-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="1d73b-282">Выберите **Управление складом** \> **Загрузки** \> **Активные загрузки**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="1d73b-283">Выбор загрузки, которая была создана в связи с отгрузкой заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1d73b-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="1d73b-284">На экспресс-вкладке **Строки заказа на загрузку** выберите **Уменьшить скомплектованное количество**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="1d73b-285">На странице **Уменьшить скомплектованное количество** в поле **Переместить в местоположение** выберите **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="1d73b-286">В поле **Перейти к грузоместу** выберите **LP33**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="1d73b-287">В сетке в поле количество **Количество запасов для разукомплектования** введите **10**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="1d73b-288">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-288">Select **OK**.</span></span>

<span data-ttu-id="1d73b-289">Результаты действия по разукомплектованию:</span><span class="sxs-lookup"><span data-stu-id="1d73b-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="1d73b-290">Статус ранее закрытой работы устанавливается как **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="1d73b-291">Новая работа типа **Перемещение запасов** создается для разукомплектованного количества **10** для номера партии **B11**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="1d73b-292">Эта работа представляет собой перемещение из местоположения **Baydoor** в грузоместо **LP33** в местоположении **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="1d73b-293">Статус задается как **Закрыто**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="1d73b-294">Система повторно резервирует номер партии, который был изначально заказан, и назначает коды местоположения и грузоместа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="1d73b-295">(Этот процесс аналогичен выполнению функции **Резервировать строку** для строки заказа для указанного номера партии).</span><span class="sxs-lookup"><span data-stu-id="1d73b-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="1d73b-296">В результате партия **B11** отображается как подтвержденная на экспресс-вкладке **Номера партий, связанные со строкой источника** на странице **Резервирование партии**, а поле **Резервирование** содержит количество **10** для номера партии **B11**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="1d73b-297">Кроме того, в поле **Местонахождение** указано значение **FL-001**, а в поле **Грузоместо** — значение **LP11**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="1d73b-298">(Если эти поля не видны, их можно добавить в сетку.)</span><span class="sxs-lookup"><span data-stu-id="1d73b-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="1d73b-299">В следующих таблицах представлен обзор, показывающий, как система обрабатывает резервирование с подтверждением по заказу для определенных складских действий.</span><span class="sxs-lookup"><span data-stu-id="1d73b-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="1d73b-300">Чтобы интерпретировать содержание в таблицах, предположим, что каждое действие склада выполняется в контексте существующего складской работы, которая происходит из резервирования партии с подтверждением по заказу, или что выполнение каждого складского действия оказывает влияние на работу этого типа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="1d73b-301">В этих таблицах в столбце "Доступное количество партий" указывается, доступно ли количество партии в дополнение к количеству, которое уже зарезервировано для текущего резервирования с подтверждением по заказу или уже зарезервировано для складской работы, которая создается из резервирований данного типа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="1d73b-302">Переопределение местоположения комплектации для открытой работы</span><span class="sxs-lookup"><span data-stu-id="1d73b-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-303">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-304">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-305">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-305">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-306">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-306">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-307">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-308">Параметр <strong>Разрешить переопределение местонахождения отгрузки</strong> включается для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="1d73b-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1d73b-309">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-310">Выберите пункт меню <strong>Переопределение местонахождения</strong> в приложении WMA, когда начинаете работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="1d73b-311">Выберите <strong>Предложить</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="1d73b-312">Подтвердите предлагаемое новое местоположение на основе доступного количества в партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-313">В текущей работе произойдут следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1d73b-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="1d73b-314">Местоположение в строке комплектации обновляется на новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="1d73b-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="1d73b-315">(Если местоположение контролируется грузоместом, для складской проводки работы назначается произвольное грузоместо и работник может выбрать любое грузоместо с доступным количеством.)</span><span class="sxs-lookup"><span data-stu-id="1d73b-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="1d73b-316">Если количество найдено в нескольких грузоместах в новом местоположении, первоначальная строка комплектации разделяется на несколько строк, чтобы соответствовать каждому из грузомест.</span><span class="sxs-lookup"><span data-stu-id="1d73b-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-317">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-318">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-319">Выберите пункт меню <strong>Переопределение местонахождения</strong> в приложении WMA, когда начинаете работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="1d73b-320">Введите местоположение вручную.</span><span class="sxs-lookup"><span data-stu-id="1d73b-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-321">Действие <strong>Переопределение местонахождения</strong> невозможно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="1d73b-322">Произойдет сбой, и будет выдано сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1d73b-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="1d73b-323">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="1d73b-324">Полная кнопка — разбиение строки работы из-за переполнения в местоположении пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-325">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-326">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-327">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-327">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-328">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-328">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-329">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d73b-330">Параметр <strong>Разрешить разделение работы</strong> включен в пункте меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="1d73b-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="1d73b-331">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-332">Выберите пункт меню <strong>Полный</strong> в приложении WMA, когда начинаете обработку работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="1d73b-333">В поле <strong>Скомплектовать количество</strong> введите частичное количество требуемой комплектации, чтобы указать полную мощность.</span><span class="sxs-lookup"><span data-stu-id="1d73b-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1d73b-334">В текущей работе количество обновляется на остающееся количество, которое необходимо скомплектовать.</span><span class="sxs-lookup"><span data-stu-id="1d73b-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="1d73b-335">Новая работа для скомплектованного количества создается и закрывается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="1d73b-336">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="1d73b-337">Уменьшение скомплектованного количества выполненной работы (с момента загрузки)</span><span class="sxs-lookup"><span data-stu-id="1d73b-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-338">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-339">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-340">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-340">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-341">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-341">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-342">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-343">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-343">Not applicable</span></span></td>
<td><span data-ttu-id="1d73b-344">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-345">Откройте страницу <strong>Уменьшить скомплектованное количество</strong> из строки загрузки.</span><span class="sxs-lookup"><span data-stu-id="1d73b-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="1d73b-346">Введите полное количество для разукомплектования.</span><span class="sxs-lookup"><span data-stu-id="1d73b-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="1d73b-347">Выберите "переместить в" местоположение/грузоместо.</span><span class="sxs-lookup"><span data-stu-id="1d73b-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="1d73b-348">Работа, которая связана со строкой загрузки, отменяется.</span><span class="sxs-lookup"><span data-stu-id="1d73b-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="1d73b-349">Новая работа для перемещения запасов создается и закрывается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-350">Количество повторно резервируется для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-351">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-352">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-352">No</span></span></td>
<td><span data-ttu-id="1d73b-353">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-353">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-354">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-354">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-355">Количество повторно резервируется для той же партии и для одного и того же местоположения и грузоместа (если местоположение управляется по грузоместу), введенных во время разукомплектования.</span><span class="sxs-lookup"><span data-stu-id="1d73b-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="1d73b-356">Перемещение номенклатуры на складе</span><span class="sxs-lookup"><span data-stu-id="1d73b-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="1d73b-357">Это складское действие применимо только для перемещения типа **Процесс создания работы**, а не для перемещения по шаблону.</span><span class="sxs-lookup"><span data-stu-id="1d73b-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-358">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-359">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-360">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-360">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-361">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-361">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-362">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-363">Параметр <strong>Разрешить перемещение запасов со связанной работой работника</strong> включен для работника.</span><span class="sxs-lookup"><span data-stu-id="1d73b-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1d73b-364">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-365">Начните перемещение в WMA.</span><span class="sxs-lookup"><span data-stu-id="1d73b-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="1d73b-366">Введите местоположения "из" и "в".</span><span class="sxs-lookup"><span data-stu-id="1d73b-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="1d73b-367">Для всей существующей работе, на которую влияет перемещение, местоположение комплектации обновляется на новое местоположение — "в".</span><span class="sxs-lookup"><span data-stu-id="1d73b-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="1d73b-368">Новая работа для перемещения запасов создается и закрывается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-369">Все существующие резервирования, затрагиваемые перемещением количества из данного местоположения, повторно резервируются для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-370">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-371">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-371">No</span></span></td>
<td><span data-ttu-id="1d73b-372">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-372">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-373">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-373">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-374">Все существующие резервирования, затрагиваемые перемещением количества из данного местоположения, зарезервированы повторно для той же партии и для нового местоположения "в" и для грузоместа (если местоположение управляется по грузоместу).</span><span class="sxs-lookup"><span data-stu-id="1d73b-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="1d73b-375">Реверсирование скомплектованного количества выполненной работы (с момента загрузки или волны)</span><span class="sxs-lookup"><span data-stu-id="1d73b-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-376">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-377">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-378">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-378">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-379">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-379">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-380">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="1d73b-381">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-381">Not applicable</span></span></td>
<td><span data-ttu-id="1d73b-382">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-383">Откройте страницу <strong>Изменить работу</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1d73b-384">На странице запроса выберите параметр <strong>Оставить номенклатуры в текущем местонахождении</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-385">Вся работа, которая связана с загрузкой, отменяется.</span><span class="sxs-lookup"><span data-stu-id="1d73b-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="1d73b-386">Количество повторно резервируется для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-387">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-388">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-388">No</span></span></td>
<td><span data-ttu-id="1d73b-389">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-389">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-390">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-390">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-391">Количество повторно резервируется для той же партии и для местоположения и грузоместа, когда количество было отправлено в реверсирование.</span><span class="sxs-lookup"><span data-stu-id="1d73b-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-392">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-393">Откройте страницу <strong>Изменить работу</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1d73b-394">На странице запроса выберите параметр <strong>Назначить номенклатуры этому местонахождению</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1d73b-395">Текущая работа отменена.</span><span class="sxs-lookup"><span data-stu-id="1d73b-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="1d73b-396">Новая работа для перемещения запасов создается и закрывается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-397">Количество повторно резервируется для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-398">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-399">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-399">No</span></span></td>
<td><span data-ttu-id="1d73b-400">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-400">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-401">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-401">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-402">Количество повторно резервируется для той же партии и для местоположения и грузоместа, когда количество было назначено в реверсирование.</span><span class="sxs-lookup"><span data-stu-id="1d73b-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-403">Да/Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-404">Откройте страницу <strong>Изменить работу</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1d73b-405">На странице запроса выберите параметр <strong>Переместить номенклатуры в это местонахождение</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-406">Реверсирование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="1d73b-407">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-408">Да/Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-409">Откройте страницу <strong>Изменить работу</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1d73b-410">На странице запроса выберите параметр <strong>Перемещать номенклатуры согласно директивам местонахождений</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-411">Реверсирование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="1d73b-412">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="1d73b-413">Комплектация недостающего количества — регистрация количества, физически не найденного в местоположении/грузоместе при выполнении работы комплектации</span><span class="sxs-lookup"><span data-stu-id="1d73b-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-414">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-415">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-416">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-416">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-417">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-417">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-418">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-419">Настраивается рабочее исключение для типа <strong>Комплектация недостающего количества</strong>, где <strong>Перераспределение номенклатур</strong> = <strong>Нет</strong>, <strong>Корректировка складских запасов</strong> = <strong>Да</strong> и <strong>Удалить резервирования</strong> = <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="1d73b-420">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-421">Выберите пункт меню <strong>Недоукомплектованность</strong> в приложении WMA, когда начинаете выполнять работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="1d73b-422">В поле <strong>Скомплектовать количество</strong> введите <strong>0</strong> (ноль).</span><span class="sxs-lookup"><span data-stu-id="1d73b-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1d73b-423">В поле <strong>Причина</strong> введите <strong>Без перераспределения</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1d73b-424">Текущая работа закрывается, и скомплектованное количество равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="1d73b-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1d73b-425">Для представления корректировки создается складская проводка с типом выдачи <strong>Инвентаризация</strong> и <strong>Продано</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-426">Количество повторно резервируется для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-427">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-428">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-428">No</span></span></td>
<td><span data-ttu-id="1d73b-429">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1d73b-430">Действие недоукомплектованности завершилось с ошибкой; будет выдано сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1d73b-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="1d73b-431">Текущая работа остается открытой.</span><span class="sxs-lookup"><span data-stu-id="1d73b-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-432">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-433">Настраивается рабочее исключение для типа <strong>Комплектация недостающего количества</strong>, где <strong>Перераспределение номенклатур</strong> = <strong>Нет</strong>, <strong>Корректировка складских запасов</strong> = <strong>Да</strong> и <strong>Удалить резервирования</strong> = <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="1d73b-434">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-435">Выберите пункт меню <strong>Недоукомплектованность</strong> в приложении WMA, когда начинаете выполнять работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="1d73b-436">В поле <strong>Скомплектовать количество</strong> введите <strong>0</strong> (ноль).</span><span class="sxs-lookup"><span data-stu-id="1d73b-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1d73b-437">В поле <strong>Причина</strong> введите <strong>Без перераспределения</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1d73b-438">Текущая работа закрывается, и скомплектованное количество равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="1d73b-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1d73b-439">Для представления корректировки создается складская проводка с типом выдачи <strong>Инвентаризация</strong> и <strong>Продано</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-440">Все существующие резервирования, затрагиваемые корректировкой количества в местоположении недоукомплектованности, повторно резервируются для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-441">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-442">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-442">No</span></span></td>
<td><span data-ttu-id="1d73b-443">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-443">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-444">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-444">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-445">Все существующие резервирования, затрагиваемые корректировкой количества в местоположении недоукомплектованности, удаляются.</span><span class="sxs-lookup"><span data-stu-id="1d73b-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-446">Настраивается рабочее исключение для типа <strong>Комплектация недостающего количества</strong>, где <strong>Перераспределение номенклатур</strong> = <strong>Вручную</strong>, <strong>Корректировка складских запасов</strong> = <strong>Да</strong> и <strong>Удалить резервирования</strong> = <strong>Нет/Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="1d73b-447">Кроме того, параметр <strong>Разрешить перераспределение номенклатур вручную</strong> включён вручную для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="1d73b-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1d73b-448">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-449">Выберите пункт меню <strong>Недоукомплектованность</strong> в приложении WMA, когда начинаете выполнять работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="1d73b-450">В поле <strong>Количество недоукомплектованности</strong> введите <strong>0</strong> (ноль).</span><span class="sxs-lookup"><span data-stu-id="1d73b-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1d73b-451">В поле <strong>Причина</strong> выберите <strong>Недоукомплектованность с перераспределением вручную</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="1d73b-452">Выберите местонахождение/грузоместо в списке.</span><span class="sxs-lookup"><span data-stu-id="1d73b-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1d73b-453">В текущей работе произойдут следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1d73b-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="1d73b-454">Строка работы закрывается, и скомплектованное количество равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="1d73b-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1d73b-455">Строка размещения отменена.</span><span class="sxs-lookup"><span data-stu-id="1d73b-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="1d73b-456">Создается новая строка комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-456">A new pick line is created.</span></span> <span data-ttu-id="1d73b-457">В ней используется местоположение/грузоместо, которые выбрал пользователь.</span><span class="sxs-lookup"><span data-stu-id="1d73b-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="1d73b-458">Создается новая строка размещения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1d73b-459">Для представления корректировки создается складская проводка с типом выдачи <strong>Инвентаризация</strong> и <strong>Продано</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-460">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-461">Настраивается рабочее исключение для типа <strong>Комплектация недостающего количества</strong>, где <strong>Перераспределение номенклатур</strong> = <strong>Вручную</strong>, <strong>Корректировка складских запасов</strong> = <strong>Да</strong> и <strong>Удалить резервирования</strong> = <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="1d73b-462">Кроме того, параметр <strong>Разрешить перераспределение номенклатур вручную</strong> включён вручную для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="1d73b-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1d73b-463">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-464">Выберите пункт меню <strong>Недоукомплектованность</strong> в приложении WMA, когда начинаете выполнять работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="1d73b-465">В поле <strong>Количество недоукомплектованности</strong> введите <strong>0</strong> (ноль).</span><span class="sxs-lookup"><span data-stu-id="1d73b-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1d73b-466">В поле <strong>Причина</strong> выберите <strong>Недоукомплектованность с перераспределением вручную</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-467">Действие недоукомплектованности завершилось с ошибкой; будет выдано сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1d73b-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="1d73b-468">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-469">Настраивается рабочее исключение для типа <strong>Комплектация недостающего количества</strong>, где <strong>Перераспределение номенклатур</strong> = <strong>Вручную</strong>, <strong>Корректировка складских запасов</strong> = <strong>Да</strong> и <strong>Удалить резервирования</strong> = <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="1d73b-470">Кроме того, параметр <strong>Разрешить перераспределение номенклатур вручную</strong> включён вручную для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="1d73b-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1d73b-471">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-472">Выберите пункт меню <strong>Недоукомплектованность</strong> в приложении WMA, когда начинаете выполнять работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="1d73b-473">В поле <strong>Количество недоукомплектованности</strong> введите <strong>0</strong> (ноль).</span><span class="sxs-lookup"><span data-stu-id="1d73b-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1d73b-474">В поле <strong>Причина</strong> выберите <strong>Недоукомплектованность с перераспределением вручную</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="1d73b-475">Выберите местонахождение/грузоместо в списке.</span><span class="sxs-lookup"><span data-stu-id="1d73b-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1d73b-476">В текущей работе произойдут следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1d73b-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="1d73b-477">Строка работы закрывается, и скомплектованное количество равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="1d73b-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1d73b-478">Строка размещения отменена.</span><span class="sxs-lookup"><span data-stu-id="1d73b-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1d73b-479">Для представления корректировки создается складская проводка с типом выдачи <strong>Инвентаризация</strong> и <strong>Продано</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1d73b-480">Все существующие резервирования, затрагиваемые корректировкой количества в местоположении/грузоместе недоукомплектованности, удаляются.</span><span class="sxs-lookup"><span data-stu-id="1d73b-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-481">Настраивается рабочее исключение для типа <strong>Комплектация недостающего количества</strong>, где <strong>Перераспределение номенклатур</strong> = <strong>Автоматически</strong>, <strong>Корректировка складских запасов</strong> = <strong>Да/Нет</strong> и <strong>Удалить резервирования</strong> = <strong>Да/Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="1d73b-482">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1d73b-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-483">Выберите пункт меню <strong>Недоукомплектованность</strong> в приложении WMA, когда начинаете выполнять работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1d73b-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="1d73b-484">В поле <strong>Количество недоукомплектованности</strong> введите <strong>0</strong> (ноль).</span><span class="sxs-lookup"><span data-stu-id="1d73b-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1d73b-485">В поле <strong>Причина</strong> выберите <strong>Недоукомплектованность с автоматическим перераспределением</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-486">Недоукомплектованность, которая включает автоматическое перераспределение, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="1d73b-487">Недоукомплектованность, которая включает автоматическое перераспределение, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d73b-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="1d73b-488">Изменить статус запасов</span><span class="sxs-lookup"><span data-stu-id="1d73b-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="1d73b-489">Это складское действие может быть выполнено из нескольких точек входа.</span><span class="sxs-lookup"><span data-stu-id="1d73b-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="1d73b-490">Показанный здесь пример использует действие **Изменение статуса запасов** на странице **В наличии по местонахождению**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d73b-491">Параметр настройки ключа</span><span class="sxs-lookup"><span data-stu-id="1d73b-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="1d73b-492">Доступное количество партий</span><span class="sxs-lookup"><span data-stu-id="1d73b-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1d73b-493">Основные шаги пользователя</span><span class="sxs-lookup"><span data-stu-id="1d73b-493">Key user steps</span></span></th>
<th><span data-ttu-id="1d73b-494">Работа склада</span><span class="sxs-lookup"><span data-stu-id="1d73b-494">Warehouse work</span></span></th>
<th><span data-ttu-id="1d73b-495">Резервирование партии с подтверждением по заказу</span><span class="sxs-lookup"><span data-stu-id="1d73b-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-496">На вкладке <strong>Склад</strong> в записи <strong>Склад</strong> для поля <strong>Удалить резервирования и маркировки</strong> задано значение <strong>Резервирования</strong> или <strong>Маркировка и резервирования</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="1d73b-497">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-498">Выберите конкретное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="1d73b-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="1d73b-499">Выберите строку, имеющую определенную номенклатуру, местоположение и грузоместо (если местоположение управляется по грузоместу).</span><span class="sxs-lookup"><span data-stu-id="1d73b-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="1d73b-500">Выберите <strong>Изменение статуса запасов</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="1d73b-501">Установите для поля <strong>Статус запасов</strong> значение <strong>Блокировка</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-502">Изменения статуса запасов не допускаются для количеств, зарезервированных для работы.</span><span class="sxs-lookup"><span data-stu-id="1d73b-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1d73b-503">Количество повторно резервируется для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-504">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="1d73b-505">Создаются две складские проводки типа <strong>Изменение статуса запасов</strong>, представляющие изменение в аналитике статуса запасов.</span><span class="sxs-lookup"><span data-stu-id="1d73b-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="1d73b-506">Создается складская проводка типа выдачи <strong>Блокировка запасов</strong> и <strong>Физически зарезервировано</strong>, которая представляет резервирование заблокированного количества.</span><span class="sxs-lookup"><span data-stu-id="1d73b-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-507">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-507">No</span></span></td>
<td><span data-ttu-id="1d73b-508">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-508">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-509">Изменения статуса запасов не допускаются для количеств, зарезервированных для работы.</span><span class="sxs-lookup"><span data-stu-id="1d73b-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1d73b-510">Резервирование удаляется.</span><span class="sxs-lookup"><span data-stu-id="1d73b-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="1d73b-511">Создаются две складские проводки типа <strong>Изменение статуса запасов</strong>, представляющие изменение в аналитике статуса запасов.</span><span class="sxs-lookup"><span data-stu-id="1d73b-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="1d73b-512">Создается складская проводка типа выдачи <strong>Блокировка запасов</strong> и <strong>Физически зарезервировано</strong>, которая представляет резервирование заблокированного количества.</span><span class="sxs-lookup"><span data-stu-id="1d73b-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="1d73b-513">На вкладке <strong>Склад</strong> в записи <strong>Склад</strong> для поля <strong>Удалить резервирования и маркировки</strong> задано значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="1d73b-514">Да</span><span class="sxs-lookup"><span data-stu-id="1d73b-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1d73b-515">Выберите конкретное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="1d73b-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="1d73b-516">Выберите строку, имеющую определенную номенклатуру, местоположение и грузоместо (если местоположение управляется по грузоместу).</span><span class="sxs-lookup"><span data-stu-id="1d73b-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="1d73b-517">Выберите <strong>Изменение статуса запасов</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="1d73b-518">Установите для поля <strong>Статус запасов</strong> значение <strong>Блокировка</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d73b-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1d73b-519">Изменения статуса запасов не допускаются для количеств, зарезервированных для работы.</span><span class="sxs-lookup"><span data-stu-id="1d73b-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="1d73b-520">Количество повторно резервируется для той же партии.</span><span class="sxs-lookup"><span data-stu-id="1d73b-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1d73b-521">Система случайным образом назначает местоположение и грузоместо (если местоположение управляется по грузоместу), где количество доступно.</span><span class="sxs-lookup"><span data-stu-id="1d73b-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d73b-522">Нет</span><span class="sxs-lookup"><span data-stu-id="1d73b-522">No</span></span></td>
<td><span data-ttu-id="1d73b-523">См. предыдущую строку.</span><span class="sxs-lookup"><span data-stu-id="1d73b-523">See the previous row.</span></span></td>
<td><span data-ttu-id="1d73b-524">Изменения статуса запасов не допускаются для количеств, зарезервированных для работы.</span><span class="sxs-lookup"><span data-stu-id="1d73b-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="1d73b-525">Изменения статуса запасов не допускаются.</span><span class="sxs-lookup"><span data-stu-id="1d73b-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="1d73b-526">Ограничения</span><span class="sxs-lookup"><span data-stu-id="1d73b-526">Limitations</span></span>

- <span data-ttu-id="1d73b-527">Функциональные возможности резервирования аналитики уровня склада не поддерживает следующие функции:</span><span class="sxs-lookup"><span data-stu-id="1d73b-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="1d73b-528">Управление учетом в двух единицах измерения</span><span class="sxs-lookup"><span data-stu-id="1d73b-528">Catch weight management</span></span>
    - <span data-ttu-id="1d73b-529">Физический отрицательный запас</span><span class="sxs-lookup"><span data-stu-id="1d73b-529">Physical negative inventory</span></span>
    - <span data-ttu-id="1d73b-530">Резервирование по заказанной поставке</span><span class="sxs-lookup"><span data-stu-id="1d73b-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="1d73b-531">Заказы на перемещение и комплектация сырья</span><span class="sxs-lookup"><span data-stu-id="1d73b-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="1d73b-532">Правило консолидации контейнера для комплектации по единице директивы имеет ограничения.</span><span class="sxs-lookup"><span data-stu-id="1d73b-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="1d73b-533">Для резервирований с подтверждением по заказу не рекомендуется использовать шаблоны построения контейнеров, в которых включено поле **Упаковывать по единице директивы**.</span><span class="sxs-lookup"><span data-stu-id="1d73b-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="1d73b-534">В текущей реализации директивы местоположения не используются при создании складских работ.</span><span class="sxs-lookup"><span data-stu-id="1d73b-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="1d73b-535">Таким образом, на этапе волны контейнеров применяется только наименьшая единица в группе упорядочения единиц (единица измерения складского учета).</span><span class="sxs-lookup"><span data-stu-id="1d73b-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
