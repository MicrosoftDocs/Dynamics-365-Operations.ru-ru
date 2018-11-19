---
title: "Управление мелкими наличными деньгами для Retail для Восточной Европы"
description: "В этом разделе описывается, как настроить и использовать возможности управления кассой в Retail для Восточной Европы."
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: c198cedba9268229dc1057711d9f16ca33acebac
ms.contentlocale: ru-ru
ms.lasthandoff: 10/24/2018

---

# <a name="petty-cash-management-for-retail-for-eastern-europe"></a><span data-ttu-id="bc3e1-103">Управление мелкими наличными деньгами для Retail для Восточной Европы</span><span class="sxs-lookup"><span data-stu-id="bc3e1-103">Petty cash management for Retail for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc3e1-104">Данная статья содержит сведения о локализации для Восточной Европы, специфичной для отрасли розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-104">This article contains information about Eastern European localization specific for the Retail industry.</span></span> 

<span data-ttu-id="bc3e1-105">В соответствии с требованиями бухгалтерской отчетности Восточной Европы можно настроить операции для наличных счетов, чтобы автоматизировать процессы, кассовые документы и кассовые отчеты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-105">In accordance with the Eastern Europe accounting requirements, you can set up operations for cash accounts to automate the processes for receipts, cash documents and cash reports.</span></span> <span data-ttu-id="bc3e1-106">Дополнительные сведения см. в разделе [(EEUR) Настройка параметров управления кассами](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span><span class="sxs-lookup"><span data-stu-id="bc3e1-106">For more information, go to [(EEUR) Set up parameters for cash management](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span></span> 

<span data-ttu-id="bc3e1-107">Продавцы могут принимать различные типы платежей в обмен на продукты и услуги, которые они продают.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-107">Retailers can accept various types of payment in exchange for the products and services that they sell.</span></span> <span data-ttu-id="bc3e1-108">Хотя наличные деньги — наиболее распространенная форма оплаты, розничные магазины также могут принимать чеки, карты или ваучеры.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-108">Although cash is the most common form of payment, retailers can also receive payment in the form of checks, cards, or vouchers.</span></span> <span data-ttu-id="bc3e1-109">В розничном POS-терминале наличные деньги, платежи по кредитным картам и другие платежи обрабатываются в операционной кассе.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-109">In Retail point of sale (POS), cash, credit card receipts, and other payments are processed through a cash office.</span></span>

<span data-ttu-id="bc3e1-110">С помощью функцию управления кассами в Retail можно выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bc3e1-110">You can do the following by using Cash management in Retail:</span></span>

- <span data-ttu-id="bc3e1-111">Создание кассы для выбранного способа оплаты для каждого розничного магазина.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-111">Create a cash account for the selected payment method for each retail store.</span></span>
- <span data-ttu-id="bc3e1-112">Использование кассовых журналов для разноски проводок по кассе и платежей клиентов, получаемые в розничном POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-112">Use cash journals to post cash transactions and customer payments that are received at a retail POS.</span></span>
- <span data-ttu-id="bc3e1-113">Объединение проводок в строку отчета при разноске журнала операций розницы.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-113">Aggregate transactions in a statement line when you post a retail statement.</span></span> <span data-ttu-id="bc3e1-114">Можно объединять сдачи наличных в сейф, инкассации, проводки по ваучерам, проводки удаления платежных средств, проводки внесения денежных средств, проводки доходов, проводки расходов, платежи клиентов, проводки по продажам и проводки возврата.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-114">You can aggregate safe drops, bank drops, voucher transactions, remove tender transactions, float entry transactions, income transactions, expense transactions, customer payments, sales transactions, and return transactions.</span></span>

<span data-ttu-id="bc3e1-115">Все проводки, которые выполняются в розничном POS-терминале, разносятся с использованием журнала ГК.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-115">All transactions that take place in Retail POS are posted using a ledger journal.</span></span> <span data-ttu-id="bc3e1-116">Можно воспользоваться журналами наличной оплаты, журналами платежей клиентов и общими журналами для создания и разноски отчетов.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-116">You can use cash payment journals, customer payment journals, and general journals to create and post the statements.</span></span> <span data-ttu-id="bc3e1-117">Дополнительные сведения см. в разделе [Создание, расчет и разноска журналов операций для розничного магазина](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span><span class="sxs-lookup"><span data-stu-id="bc3e1-117">For more information, go to [Create, calculate, and post statements for a retail store](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span></span>

<span data-ttu-id="bc3e1-118">На странице **Разнесенные журналы операций** в области действий можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bc3e1-118">On the **Posted statements** page, on the Action Pane, you can do the following:</span></span>
  - <span data-ttu-id="bc3e1-119">Выберите **Запросы > Журнал наличных платежей**, чтобы получить доступ к журналу наличных платежей, связанных с отчетом.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-119">Go to **Inquiries > Cash payment journal** to access the cash payment journals that are related to the statement.</span></span>
  - <span data-ttu-id="bc3e1-120">Выберите **Запросы > Общий журнал**, чтобы получить доступ к журналам ГК по отчету, за исключением платежей клиентов или кассовых платежей.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-120">Go to **Inquiries > General journal** to access the ledger journals that are related to the statement, other than customer payments and cash payments.</span></span>

## <a name="set-up-for-cash-management-for-retail-pos"></a><span data-ttu-id="bc3e1-121">Настройка управления денежными средствами для Retail POS</span><span class="sxs-lookup"><span data-stu-id="bc3e1-121">Set up for cash management for Retail POS</span></span>

<span data-ttu-id="bc3e1-122">Необходимо выполнить следующую процедуру настройки, прежде чем можно будет использовать управление денежными средствами в модуле Retail:</span><span class="sxs-lookup"><span data-stu-id="bc3e1-122">You must complete the following setup procedure before you use cash management in Retail:</span></span>
- <span data-ttu-id="bc3e1-123">Настройте способ оплаты для каждого типа платежа, принимаемого продавцом, на странице **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-123">Set up a payment method for each payment type that the retailer accepts on the **Payment methods** page.</span></span> <span data-ttu-id="bc3e1-124">Для разности проводок в Retail POS можно использовать различные методы оплаты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-124">You can use different payment methods for posting transactions in Retail POS.</span></span> <span data-ttu-id="bc3e1-125">Дополнительные сведения о способах оплаты в Retail см. в разделе [Способы оплаты](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).</span><span class="sxs-lookup"><span data-stu-id="bc3e1-125">For more information about payment methods in Retail, see [Payment methods](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).</span></span>

- <span data-ttu-id="bc3e1-126">Настройка розничных параметров кассовых операций.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-126">Set up retail parameters for cash operations.</span></span>

- <span data-ttu-id="bc3e1-127">Настройка способа оплаты наличными в розничном магазине.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-127">Set up a payment method for cash payments in a retail store.</span></span>

### <a name="set-up-retail-parameters-for-cash-operations"></a><span data-ttu-id="bc3e1-128">Настройка розничных параметров кассовых операций</span><span class="sxs-lookup"><span data-stu-id="bc3e1-128">Set up retail parameters for cash operations</span></span>

<span data-ttu-id="bc3e1-129">Можно настроить параметры для создания и разноски проводок по кассе в модуле Retail.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-129">You can set up parameters to create and post cash transactions in Retail.</span></span> <span data-ttu-id="bc3e1-130">Можно использовать журналы оплаты наличными, журналы платежей клиентов или общие журналы для разноски проводок по продажам и платежам в Retail POS.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-130">You can use cash payment journals, customer payment journals, or general journals to post sales transactions and payment transactions in the Retail POS.</span></span> <span data-ttu-id="bc3e1-131">Можно объединять проводок с одинаковыми свойствами при разноске отчета.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-131">You can aggregate transactions that have the same properties when you post a statement.</span></span> 

1. <span data-ttu-id="bc3e1-132">Перейдите в раздел **Розничная торговля > Настройка центрального офиса > Параметры > Параметры розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-132">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="bc3e1-133">В левой области щелкните **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-133">In the left pane, click **Posting**</span></span>

2. <span data-ttu-id="bc3e1-134">В области **Разноска** на экспресс-вкладке **Агрегирование** установите для параметра **Внесение/изъятие наличности** значение **Да**, чтобы объединять проводки удаления платежного средства или внесения остатка, связанные со строкой отчета, при разноске отчета.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-134">In the **Posting** area, on the **Aggregation** FastTab, set **Tender remove/float** to **Yes** to aggregate the remove tender transactions or float entry transactions that are associated with a statement line when you post the statement.</span></span> <span data-ttu-id="bc3e1-135">Проводка удаления платежного средства создается при изъятии наличности из ящика POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-135">A remove tender transaction is created when you withdraw cash from the POS cash drawer.</span></span> <span data-ttu-id="bc3e1-136">Проводка внесения остатка создается при помещении наличности в ящик POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-136">A float entry transaction is created when you deposit cash in the POS cash drawer.</span></span>

3. <span data-ttu-id="bc3e1-137">Включите отдельные параметры, перечисленные ниже, для суммирования проводок, связанных со строкой отчета, при разноске отчета:</span><span class="sxs-lookup"><span data-stu-id="bc3e1-137">Activate the individual parameters listed below to aggregate the transactions that are associated with a statement line when you post the statement:</span></span>
   - <span data-ttu-id="bc3e1-138">**Инкассация** — суммируются банковские проводки.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-138">**Bank drop** – Aggregate bank transactions.</span></span>
   - <span data-ttu-id="bc3e1-139">**Сдача наличных средств в сейф** — суммируются сейфовые проводки.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-139">**Safe drop** – Aggregate safe transactions.</span></span>
   - <span data-ttu-id="bc3e1-140">**Проводки по доходам/расходам** — суммируются проводки по доходам или проводки по расходам.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-140">**Income/Expense transactions** – Aggregate income transactions or expense transactions.</span></span>
   - <span data-ttu-id="bc3e1-141">**Проводки ваучера** — суммируются проводки по ваучерам.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-141">**Voucher transactions** – Aggregate voucher transactions.</span></span>
   - <span data-ttu-id="bc3e1-142">**Платежи клиентов** — суммируются платежи клиентов.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-142">**Customer payments** – Aggregate customer payments.</span></span>
   - <span data-ttu-id="bc3e1-143">**Продажи и возвраты** — суммируются проводки продаж и возвратов.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-143">**Sales and returns** – Aggregate sales and returns transactions.</span></span>

4. <span data-ttu-id="bc3e1-144">На экспресс-вкладке **Платежи** выберите наименование журнала по умолчанию для следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="bc3e1-144">On the **Payments** FastTab, select a default journal name for the following options:</span></span>
     - <span data-ttu-id="bc3e1-145">**Журнал платежей клиентов** — этот журнал используется для разноски оплаты клиентов.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-145">**Customer payment journal** – This journal is used to post customer payments.</span></span>
     - <span data-ttu-id="bc3e1-146">**Журнал наличных платежей** — этот журнал используется для разноски наличных платежей.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-146">**Cash payment journal** – This journal is used to post cash payments.</span></span>
     - <span data-ttu-id="bc3e1-147">**Общий журнал** — этот журнал используется для разноски проводок, не являющихся проводками оплаты клиентов или проводками наличной оплаты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-147">**General journal** – This journal is used to post transactions other than cash payments and customer payments.</span></span>

### <a name="set-up-a-payment-method-for-cash-payments-in-a-retail-store"></a><span data-ttu-id="bc3e1-148">Настройка способа оплаты наличными в розничном магазине</span><span class="sxs-lookup"><span data-stu-id="bc3e1-148">Set up a payment method for cash payments in a retail store</span></span>

<span data-ttu-id="bc3e1-149">Следующая процедура служит для настройки способа оплаты наличными в розничном магазине.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-149">Use the following procedure to set up a payment method for cash payments in a retail store.</span></span>

1. <span data-ttu-id="bc3e1-150">Перейдите в раздел **Розничная торговля > Розничные магазины > Все розничные магазины**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-150">Go to **Retail > Channels > Retail stores > All retail stores**.</span></span>

2. <span data-ttu-id="bc3e1-151">На странице списка **Все розничные магазины** выберите магазин, для которого необходимо настроить способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-151">On the **All retail stores** list page, select the store to set up a payment method for.</span></span>

3. <span data-ttu-id="bc3e1-152">На панели области действий на вкладке **Настройка** в группе **Настройка** щелкните **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-152">On the Action Pane, on the **Set up** tab, in the **Set up** group, click **Payment methods**.</span></span>

4. <span data-ttu-id="bc3e1-153">На странице **Способ оплаты** создайте или выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-153">On the **Payment method** page, create or select a payment method.</span></span> 

5. <span data-ttu-id="bc3e1-154">На экспресс-вкладке **Разноска** в группе полей **Счет** в поле **Тип счета** выберите **Кассовый счет**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-154">On the **Posting** FastTab, in the **Account** field group, in the **Account type** field, select **Cash account**.</span></span>

   > [!NOTE]
    > <span data-ttu-id="bc3e1-155">Можно выбрать **Кассовый счет** в поле **Тип счета** только в том случае, если выбрано значение **Обычная** или **Внесение/изъятие наличности** в поле **Функция**.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-155">You can select **Cash account** in the **Account type** field only if you select **Normal** or **Tender remove/float** in the **Function** field.</span></span>

6. <span data-ttu-id="bc3e1-156">В поле **Номер счета** выберите номер кассового счета для способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-156">In the **Account number** field, select a cash account number for the payment method.</span></span>

7. <span data-ttu-id="bc3e1-157">В группе полей **Внесение/изъятие наличности** в поле **Корр. счет** выберите корр. счета для разноски проводок удаления платежного средства или ввода остатка для способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-157">In the **Tender remove/float** field group, in the **Offset account** field, select the offset account to post remove tender or float entry transactions for the payment method.</span></span>

> [!NOTE]
> <span data-ttu-id="bc3e1-158">Необходимо настроить корр. счета как для способ оплаты наличными, так и для способа оплаты удаления платежного средства и ввода остатка для магазина.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-158">You must set up offset accounts for both the cash tender payment method and the remove tender or float entry payment method for a store.</span></span> <span data-ttu-id="bc3e1-159">При этом создаются сбалансированные записи ГК для проводок удаления платежного средства и ввода остатка.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-159">This creates balanced general ledger entries for remove tender or float entry transactions.</span></span>

