---
title: "Обзор заказов клиентов"
description: "В этом разделе представлена информация о заказах клиентов в современном терминале розничной торговли Retail Modern POS (MPOS). Заказы клиентов также называются специальными заказами. Раздел включает в себя обсуждение связанных параметров и потоков проводки."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f46cf7d4df4a8cb0ad1846882292965aa492239b
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="customer-orders-overview"></a><span data-ttu-id="e4332-105">Обзор заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="e4332-105">Customer orders overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4332-106">В этом разделе представлена информация о заказах клиентов в современном терминале розничной торговли Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="e4332-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="e4332-107">Заказы клиентов также называются специальными заказами.</span><span class="sxs-lookup"><span data-stu-id="e4332-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="e4332-108">Раздел включает в себя обсуждение связанных параметров и потоков проводки.</span><span class="sxs-lookup"><span data-stu-id="e4332-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="e4332-109">В мире многоканальной розничной торговли многие компании розничной торговли предоставляют возможность заказов клиента или специальных заказов для удовлетворения требований разных продуктов и требований выполнения.</span><span class="sxs-lookup"><span data-stu-id="e4332-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="e4332-110">Вот некоторые типовые сценарии:</span><span class="sxs-lookup"><span data-stu-id="e4332-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="e4332-111">Клиент хочет, чтобы продукты были доставлены по определенному адресу на определенную дату.</span><span class="sxs-lookup"><span data-stu-id="e4332-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="e4332-112">Клиент хочет забрать продукты из магазина или местоположения, отличных от магазина или местоположения, где клиент приобрел эти продукты.</span><span class="sxs-lookup"><span data-stu-id="e4332-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="e4332-113">Клиент хочет, чтобы приобретенные им продукты забрал другой пользователь.</span><span class="sxs-lookup"><span data-stu-id="e4332-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="e4332-114">Предприятия розничной торговли также используют заказы клиентов для уменьшения упущенных продаж, которые в противном случае могли бы возникнуть из-за отсутствия запасов на складе, поскольку товар может быть доставлен или получен в другое время или в другом месте.</span><span class="sxs-lookup"><span data-stu-id="e4332-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="e4332-115">Настройка заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="e4332-115">Set up customer orders</span></span>
<span data-ttu-id="e4332-116">Ниже перечислены параметры, которые могут быть заданы на странице **Параметры розничной торговли**, чтобы определить, как будут выполняться заказы клиентов:</span><span class="sxs-lookup"><span data-stu-id="e4332-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="e4332-117">**Процент депозита по умолчанию** – укажите сумму, которую клиент должен заплатить как депозит, чтобы заказ мог быть подтвержден.</span><span class="sxs-lookup"><span data-stu-id="e4332-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="e4332-118">Депозит по умолчанию рассчитывается как процент от суммы заказа.</span><span class="sxs-lookup"><span data-stu-id="e4332-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="e4332-119">В зависимости от привилегий, сотрудник магазина может переопределить сумму с помощью функции **Переопределение депозита**.</span><span class="sxs-lookup"><span data-stu-id="e4332-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="e4332-120">**Процент сбора за аннулирование** — если при отмене заказа клиента будет взиматься сбор, укажите сумму такого сбора.</span><span class="sxs-lookup"><span data-stu-id="e4332-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="e4332-121">**Код сбора за аннулирование** — если при отмене заказа клиента будет применяться сбор, этот сбор будут отражаться с кодом сборов для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="e4332-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="e4332-122">Этот параметр используется, чтобы определить код сбора за аннулирование.</span><span class="sxs-lookup"><span data-stu-id="e4332-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="e4332-123">**Код расходов на поставку** — предприятия розничной торговли могут взимать дополнительную плату за отгрузку товаров клиенту.</span><span class="sxs-lookup"><span data-stu-id="e4332-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="e4332-124">Сумма платы за доставку будут отражаться с кодом сбора по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="e4332-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="e4332-125">Этот параметр используется для сопоставления кода расходов на поставку с расходами на доставку по заказу клиента.</span><span class="sxs-lookup"><span data-stu-id="e4332-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="e4332-126">**Возмещение расходов на поставку** — укажите, подлежат ли возмещению расходы на доставку, связанные с заказом клиента.</span><span class="sxs-lookup"><span data-stu-id="e4332-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="e4332-127">**Максимальная сумма без утверждения** — если расходы на доставку подлежат возмещению, укажите максимальную сумму возмещения расходов на доставку для всех заказов на возврат.</span><span class="sxs-lookup"><span data-stu-id="e4332-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="e4332-128">Если эта сумма будет превышен, для продолжения возмещения требуется переопределение от менеджера.</span><span class="sxs-lookup"><span data-stu-id="e4332-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="e4332-129">Для учета указанных ниже сценариев возмещение расходов на доставку может превышать исходную уплаченную сумму:</span><span class="sxs-lookup"><span data-stu-id="e4332-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="e4332-130">Расходы применяются на уровне заголовка заказа на продажу, и при возврате некоторого количества строк продуктов максимальное возмещение расходов на доставку, разрешенное для этих продуктов и количества, не может быть определено способом, подходящим для всех розничных клиентов.</span><span class="sxs-lookup"><span data-stu-id="e4332-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="e4332-131">Расходы на доставку возникают для каждого экземпляра отгрузки.</span><span class="sxs-lookup"><span data-stu-id="e4332-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="e4332-132">Если клиент возвращает продукты несколько раз, и политика предприятия розничной торговли указывает, что предприятие розничной торговли несет затраты на доставку возврата, расходы на доставку возврата будут больше, чем фактический сбор за доставку.</span><span class="sxs-lookup"><span data-stu-id="e4332-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="e4332-133">Порядок проводки для клиентских заказов</span><span class="sxs-lookup"><span data-stu-id="e4332-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="e4332-134">Создайте клиентский заказ в Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="e4332-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="e4332-135">Добавьте клиента к этой проводке.</span><span class="sxs-lookup"><span data-stu-id="e4332-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="e4332-136">Добавить продукты в корзину.</span><span class="sxs-lookup"><span data-stu-id="e4332-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="e4332-137">Щелкните **Создать заказ клиента**, затем выберите тип заказа.</span><span class="sxs-lookup"><span data-stu-id="e4332-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="e4332-138">Тип заказа может быть **Клиентский заказ** или **Предложение с расценками**.</span><span class="sxs-lookup"><span data-stu-id="e4332-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="e4332-139">Щелкните **Отгрузить выбранные** или **Отгрузить все** для отгрузки продуктов по адресу из счета клиента, укажите запрошенную дата отгрузки и укажите расходы на доставку.</span><span class="sxs-lookup"><span data-stu-id="e4332-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="e4332-140">Щелкните **Скомплектовать выбранные** или **Скомплектовать все**, чтобы выбрать продукты, которые клиент заберет из текущего магазина или другого магазина в определенную дату.</span><span class="sxs-lookup"><span data-stu-id="e4332-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="e4332-141">Получите сумму депозита, если требуется депозит.</span><span class="sxs-lookup"><span data-stu-id="e4332-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="e4332-142">Изменение существующего заказа клиента</span><span class="sxs-lookup"><span data-stu-id="e4332-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="e4332-143">На домашней странице нажмите кнопку **Найти заказ**.</span><span class="sxs-lookup"><span data-stu-id="e4332-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e4332-144">Найдите и выберите заказ, который требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="e4332-144">Find and select the order to edit.</span></span> <span data-ttu-id="e4332-145">Внизу страницы нажмите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="e4332-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="e4332-146">Скомплектуйте заказ</span><span class="sxs-lookup"><span data-stu-id="e4332-146">Pick up an order</span></span>

1.  <span data-ttu-id="e4332-147">На домашней странице нажмите кнопку **Найти заказ**.</span><span class="sxs-lookup"><span data-stu-id="e4332-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e4332-148">Выберите заказ для комплектации.</span><span class="sxs-lookup"><span data-stu-id="e4332-148">Select the order to pick up.</span></span> <span data-ttu-id="e4332-149">Внизу страницы нажмите **Комплектация и упаковка**.</span><span class="sxs-lookup"><span data-stu-id="e4332-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="e4332-150">Нажмите **Самовывоз**.</span><span class="sxs-lookup"><span data-stu-id="e4332-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="e4332-151">Отмена заказа</span><span class="sxs-lookup"><span data-stu-id="e4332-151">Cancel an order</span></span>

1.  <span data-ttu-id="e4332-152">На домашней странице нажмите кнопку **Найти заказ**.</span><span class="sxs-lookup"><span data-stu-id="e4332-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e4332-153">Выбор заказ для отмены.</span><span class="sxs-lookup"><span data-stu-id="e4332-153">Select the order to cancel.</span></span> <span data-ttu-id="e4332-154">Внизу страницы нажмите **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="e4332-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="e4332-155">Создание заказа на возврат</span><span class="sxs-lookup"><span data-stu-id="e4332-155">Create a return order</span></span>

1.  <span data-ttu-id="e4332-156">На домашней странице нажмите кнопку **Найти заказ**.</span><span class="sxs-lookup"><span data-stu-id="e4332-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e4332-157">Выберите заказ для возврата, выберите накладную для этого заказа, затем выберите строку продукта для возвращаемого товара.</span><span class="sxs-lookup"><span data-stu-id="e4332-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="e4332-158">Внизу страницы нажмите **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="e4332-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="e4332-159">Порядок асинхронной проводки для клиентских заказов</span><span class="sxs-lookup"><span data-stu-id="e4332-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="e4332-160">Клиентские заказы можно создавать в клиенте POS в синхронном или асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="e4332-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="e4332-161">Включение возможности создания заказов клиентов в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="e4332-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="e4332-162">Нажмите **Розничная торговля** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Профиль POS** &gt; **Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="e4332-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="e4332-163">На экспресс-вкладке **Общие** задайте для параметра **Создать клиентский заказ в асинхронном режиме** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e4332-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="e4332-164">Если для параметра **Создать клиентский заказ в асинхронном режиме** задано значение **Да**, клиентские заказы всегда создаются в асинхронном режиме, даже когда служба Retail Transaction Service (RTS) доступна.</span><span class="sxs-lookup"><span data-stu-id="e4332-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="e4332-165">Если для этого параметра задано значение **Нет**, клиентские заказы всегда создаются в синхронном режиме с помощью службы RTS.</span><span class="sxs-lookup"><span data-stu-id="e4332-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="e4332-166">При создании клиентских заказов в асинхронном режиме они извлекаются и вставляются в Retail с помощью заданий извлечения (P).</span><span class="sxs-lookup"><span data-stu-id="e4332-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="e4332-167">Соответствующие заказы на продажу создаются в Retail при выполнении команды **Синхронизация заказов** либо вручную, либо с помощью пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e4332-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="additional-resources"></a><span data-ttu-id="e4332-168">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e4332-168">Additional resources</span></span>
--------

[<span data-ttu-id="e4332-169">Гибридные клиентские заказы</span><span class="sxs-lookup"><span data-stu-id="e4332-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




