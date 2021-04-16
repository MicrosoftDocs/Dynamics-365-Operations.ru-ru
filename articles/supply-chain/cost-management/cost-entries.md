---
title: Записи затрат
description: В этой статье представлена информация о записях затрат и когда они созданы. Запись затрат — это запись, регистрирующая количество и стоимость данного события.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48c37e4355bc3448930a7cfa73ce08ac8e439b97
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839423"
---
# <a name="cost-entries"></a><span data-ttu-id="0a9f7-104">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="0a9f7-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a9f7-105">В этой статье представлена информация о записях затрат и когда они созданы.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="0a9f7-106">Запись затрат — это запись, регистрирующая количество и стоимость данного события.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="0a9f7-107">Записи затрат — это агрегирования проводок по запасам, которые записываются в активных финансовых складских аналитиках.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="0a9f7-108">Примеры</span><span class="sxs-lookup"><span data-stu-id="0a9f7-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="0a9f7-109">Пример 1: записи затрат не создаются</span><span class="sxs-lookup"><span data-stu-id="0a9f7-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="0a9f7-110">Регистрируется событие журнала перемещений.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-110">A transfer journal event is registered.</span></span> <span data-ttu-id="0a9f7-111">Событие перемещает одну часть номенклатуры А из местонахождения А в местонахождение B. Складская аналитика местонахождения не считается частью объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="0a9f7-112">Поэтому событие создает две проводки по запасам и не создает записей затрат.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="0a9f7-113">Пример 2: записи затрат создаются</span><span class="sxs-lookup"><span data-stu-id="0a9f7-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="0a9f7-114">Регистрируется событие журнала перемещений.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-114">A transfer journal event is registered.</span></span> <span data-ttu-id="0a9f7-115">Событие передает одну единицу номенклатуры А с сайта 1 на сайт 2.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="0a9f7-116">Складская аналитика сайта считается частью объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="0a9f7-117">Поэтому событие создает две проводки по запасам и две записи затрат.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="0a9f7-118">Пример 3: создается одна запись затрат</span><span class="sxs-lookup"><span data-stu-id="0a9f7-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="0a9f7-119">Событие поступления продуктов регистрируется для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="0a9f7-120">Событие регистрирует 100 частей номенклатуры А по цене за единицу 10,00 долларов США (USD).</span><span class="sxs-lookup"><span data-stu-id="0a9f7-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="0a9f7-121">Поскольку номенклатура А использует серийный номер для отслеживания цели управления запасами, уникальный серийный номер создается для каждой полученной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="0a9f7-122">Поэтому событие создает 100 проводок по запасам и одну запись затрат.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="0a9f7-123">Страница "Записи затрат"</span><span class="sxs-lookup"><span data-stu-id="0a9f7-123">Cost entries page</span></span>
<span data-ttu-id="0a9f7-124">Новая страница **Записи затрат** позволяет просматривать регистрации количеств и затрат и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="0a9f7-125">Эта страница дополняет страницы **Проводка по запасам** и **Сопоставление запасов**.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="0a9f7-126">Записи регистрируются в хронологическом порядке для события.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="0a9f7-127">Таким образом, можно быстро найти накопленные затраты определенного события или всех событий, связанных с документом, и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="0a9f7-128">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="0a9f7-128">Here is an example:</span></span>

-   <span data-ttu-id="0a9f7-129">Событие поступления продуктов регистрируется для номенклатуры A. Что частей получено по цене за единицу 10,00 долларов США.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="0a9f7-130">Несколько дней после регистрации события накладной цена увеличивается до 11,00 долларов США.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="0a9f7-131">Следовательно общая сумма равна 1100 долларов США.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="0a9f7-132">Второй ваучер создается для учета разницы в 100 долларов США.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="0a9f7-133">Несколько дней спустя регистрируются накладные расходы на сумму 15,00 долларов США для покрытия транспортных расходов по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="0a9f7-134">Ваучер</span><span class="sxs-lookup"><span data-stu-id="0a9f7-134">Voucher</span></span> | <span data-ttu-id="0a9f7-135">Дата</span><span class="sxs-lookup"><span data-stu-id="0a9f7-135">Date</span></span>       | <span data-ttu-id="0a9f7-136">Справка</span><span class="sxs-lookup"><span data-stu-id="0a9f7-136">Reference</span></span>      | <span data-ttu-id="0a9f7-137">По номеру</span><span class="sxs-lookup"><span data-stu-id="0a9f7-137">Number</span></span> | <span data-ttu-id="0a9f7-138">Номер лота</span><span class="sxs-lookup"><span data-stu-id="0a9f7-138">Lot ID</span></span>  | <span data-ttu-id="0a9f7-139">Количество</span><span class="sxs-lookup"><span data-stu-id="0a9f7-139">Quantity</span></span> | <span data-ttu-id="0a9f7-140">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="0a9f7-141">00001</span><span class="sxs-lookup"><span data-stu-id="0a9f7-141">00001</span></span>   | <span data-ttu-id="0a9f7-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="0a9f7-142">01-01-2015</span></span> | <span data-ttu-id="0a9f7-143">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="0a9f7-143">Purchase order</span></span> | <span data-ttu-id="0a9f7-144">100001</span><span class="sxs-lookup"><span data-stu-id="0a9f7-144">100001</span></span> | <span data-ttu-id="0a9f7-145">0000101</span><span class="sxs-lookup"><span data-stu-id="0a9f7-145">0000101</span></span> | <span data-ttu-id="0a9f7-146">100,00</span><span class="sxs-lookup"><span data-stu-id="0a9f7-146">100.00</span></span>   | <span data-ttu-id="0a9f7-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="0a9f7-147">1000.00</span></span> |
| <span data-ttu-id="0a9f7-148">00002</span><span class="sxs-lookup"><span data-stu-id="0a9f7-148">00002</span></span>   | <span data-ttu-id="0a9f7-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="0a9f7-149">20-01-2015</span></span> | <span data-ttu-id="0a9f7-150">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="0a9f7-150">Purchase order</span></span> | <span data-ttu-id="0a9f7-151">100001</span><span class="sxs-lookup"><span data-stu-id="0a9f7-151">100001</span></span> | <span data-ttu-id="0a9f7-152">0000101</span><span class="sxs-lookup"><span data-stu-id="0a9f7-152">0000101</span></span> |          | <span data-ttu-id="0a9f7-153">100,00</span><span class="sxs-lookup"><span data-stu-id="0a9f7-153">100.00</span></span>  |
| <span data-ttu-id="0a9f7-154">00003</span><span class="sxs-lookup"><span data-stu-id="0a9f7-154">00003</span></span>   | <span data-ttu-id="0a9f7-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="0a9f7-155">31-01-2015</span></span> | <span data-ttu-id="0a9f7-156">Корректировка</span><span class="sxs-lookup"><span data-stu-id="0a9f7-156">Adjustment</span></span>     | <span data-ttu-id="0a9f7-157">100001</span><span class="sxs-lookup"><span data-stu-id="0a9f7-157">100001</span></span> | <span data-ttu-id="0a9f7-158">0000101</span><span class="sxs-lookup"><span data-stu-id="0a9f7-158">0000101</span></span> |          | <span data-ttu-id="0a9f7-159">15,00</span><span class="sxs-lookup"><span data-stu-id="0a9f7-159">15.00</span></span>   |

<span data-ttu-id="0a9f7-160">На странице **Записи затрат** можно выполнить фильтрацию по коду и дате документа.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="0a9f7-161">Записи затрат доступны только для [объектов затрат](cost-object.md) или выпущенных продуктов.</span><span class="sxs-lookup"><span data-stu-id="0a9f7-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0a9f7-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a9f7-162">Additional resources</span></span>
--------

[<span data-ttu-id="0a9f7-163">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="0a9f7-163">Cost objects</span></span>](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]