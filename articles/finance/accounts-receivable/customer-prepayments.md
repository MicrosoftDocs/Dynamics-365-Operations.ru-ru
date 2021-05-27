---
title: Предоплата клиента
description: В этой теме объясняется, как настраивать и обрабатывать предоплаты клиентов (также называемые депозитами клиентов).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019428"
---
# <a name="customer-prepayments"></a><span data-ttu-id="341a2-103">Предоплата клиента</span><span class="sxs-lookup"><span data-stu-id="341a2-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="341a2-104">Предоплаты клиента используются при получении платежа от клиента, но нет накладной, с которой может быть сопоставлен платеж.</span><span class="sxs-lookup"><span data-stu-id="341a2-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="341a2-105">Эти типы платежей также называются депозитами клиентов.</span><span class="sxs-lookup"><span data-stu-id="341a2-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="341a2-106">Процесс настройки предоплаты клиентов и работы с ней состоит из следующих основных шагов:</span><span class="sxs-lookup"><span data-stu-id="341a2-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="341a2-107">Создание профиля разноски клиента для предоплаты.</span><span class="sxs-lookup"><span data-stu-id="341a2-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="341a2-108">Настройка параметра **Профиль разноски с ваучером журнала предоплат**.</span><span class="sxs-lookup"><span data-stu-id="341a2-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="341a2-109">Создайте журнал платежей клиента и установите флажок **Ваучер журнала предоплат** в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="341a2-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="341a2-110">Разноска журнала платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="341a2-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="341a2-111">После создания накладной сопоставьте предоплату с ней, используя страницу **Сопоставление открытых проводок**.</span><span class="sxs-lookup"><span data-stu-id="341a2-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="341a2-112">Создание профиля разноски клиента для предоплаты</span><span class="sxs-lookup"><span data-stu-id="341a2-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="341a2-113">Обычно при принятии предоплат или депозитов от клиентов до поставки товаров или услуг или до того, как накладная существует в системе, вместо актива в плане счетов необходимо записать наличные деньги как задолженность.</span><span class="sxs-lookup"><span data-stu-id="341a2-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="341a2-114">Однако потребности в записи этих сумм в главной книге могут различаться в зависимости от страны или региона.</span><span class="sxs-lookup"><span data-stu-id="341a2-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="341a2-115">Поэтому необходимо проконсультироваться с бухгалтерами о применимых местных правилах.</span><span class="sxs-lookup"><span data-stu-id="341a2-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="341a2-116">В общем случае процесс создания профиля разноски, который может использоваться для предоплат, совпадает с процессом создания других профилей разноски.</span><span class="sxs-lookup"><span data-stu-id="341a2-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="341a2-117">Основное различие — это счет ГК, выбранный в поле **Суммарный счет**.</span><span class="sxs-lookup"><span data-stu-id="341a2-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="341a2-118">Дополнительную информацию см. в разделе [Профили разноски по клиенту](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="341a2-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="341a2-119">Определение параметров для предоплат клиентов</span><span class="sxs-lookup"><span data-stu-id="341a2-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="341a2-120">Существует два параметра модуля "расчеты с поставщиками", которые необходимо учитывать при настройке системы для предоплат клиентов.</span><span class="sxs-lookup"><span data-stu-id="341a2-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="341a2-121">Выполните следующие действия, чтобы настроить параметры.</span><span class="sxs-lookup"><span data-stu-id="341a2-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="341a2-122">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="341a2-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="341a2-123">Необязательно: На вкладке **Главная книга и налог** на экспресс-вкладке **Платеж** задайте для параметра **Налог по ваучеру журнала предоплат** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="341a2-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="341a2-124">В поле **Профиль разноски с ваучером журнала предоплат** выберите профиль разноски клиента, который будет использоваться при разноске предоплат клиента.</span><span class="sxs-lookup"><span data-stu-id="341a2-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="341a2-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="341a2-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="341a2-126">Создание ваучеров предоплат клиентов</span><span class="sxs-lookup"><span data-stu-id="341a2-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="341a2-127">При создании журнала платежей клиента для каждой предоплаты необходимо установить для параметра **Ваучер журнала предоплат** значение **Да** на странице **Журнал платежей клиентов**.</span><span class="sxs-lookup"><span data-stu-id="341a2-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="341a2-128">Чтобы создать предоплату клиента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="341a2-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="341a2-129">Перейдите в раздел **Расчеты с клиентами \> Платежи \> Журнал платежей клиентов**.</span><span class="sxs-lookup"><span data-stu-id="341a2-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="341a2-130">Выберите **Создать**, чтобы создать журнал.</span><span class="sxs-lookup"><span data-stu-id="341a2-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="341a2-131">В поле **Имя** выберите имя используемого журнала.</span><span class="sxs-lookup"><span data-stu-id="341a2-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="341a2-132">Если для параметра **Налог по ваучеру журнала предоплат** задано значение **Да** в предыдущей процедуре, следует выбрать имя журнала, в котором выбран параметр **Сумма включает налог**.</span><span class="sxs-lookup"><span data-stu-id="341a2-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="341a2-133">Необязательно: В поле **Описание** введите подробное описание.</span><span class="sxs-lookup"><span data-stu-id="341a2-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="341a2-134">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="341a2-134">Select **Lines**.</span></span>
6. <span data-ttu-id="341a2-135">Если пустая строка не существует, выберите **Создать**, чтобы создать строку.</span><span class="sxs-lookup"><span data-stu-id="341a2-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="341a2-136">В поле **Дата** введите дату, когда должна быть разнесена предоплата.</span><span class="sxs-lookup"><span data-stu-id="341a2-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="341a2-137">В поле **Счет** выберите клиента для предоплаты.</span><span class="sxs-lookup"><span data-stu-id="341a2-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="341a2-138">Необязательно: В поле **Описание** введите подробное описание проводки.</span><span class="sxs-lookup"><span data-stu-id="341a2-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="341a2-139">В поле **Кредит** введите сумму предоплаты.</span><span class="sxs-lookup"><span data-stu-id="341a2-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="341a2-140">В поле **Корр. счет** выберите счет для направления платежа.</span><span class="sxs-lookup"><span data-stu-id="341a2-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="341a2-141">Например, выберите банковский или счет ГК для разноски платежа.</span><span class="sxs-lookup"><span data-stu-id="341a2-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="341a2-142">В поле **Способ оплаты** выберите способ оплаты клиента.</span><span class="sxs-lookup"><span data-stu-id="341a2-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="341a2-143">На вкладке **Предоплата** задайте параметр **Ваучер журнала предоплат** как **Да**.</span><span class="sxs-lookup"><span data-stu-id="341a2-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="341a2-144">Повторите шаги с 7 по 13 для каждой дополнительной предоплаты, которая должна быть разнесена.</span><span class="sxs-lookup"><span data-stu-id="341a2-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="341a2-145">Выберите **Разнести**, чтобы завершить журнал.</span><span class="sxs-lookup"><span data-stu-id="341a2-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="341a2-146">Сопоставление предоплат с накладными</span><span class="sxs-lookup"><span data-stu-id="341a2-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="341a2-147">Рабочую область **Платежи клиентов** можно использовать для быстрого поиска и сопоставления платежей, которые не были полностью сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="341a2-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="341a2-148">На панели мониторинга **Главная** выберите плитку **Платежи клиентов**.</span><span class="sxs-lookup"><span data-stu-id="341a2-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="341a2-149">В разделе **Проводки клиента** на вкладке **Несопоставленные платежи** найдите и выберите сопоставляемый платеж.</span><span class="sxs-lookup"><span data-stu-id="341a2-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="341a2-150">Выберите **Сопоставить проводки**.</span><span class="sxs-lookup"><span data-stu-id="341a2-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="341a2-151">Установите флажок **Отметить** для накладной и платежа, который будет сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="341a2-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="341a2-152">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="341a2-152">Select **Post**.</span></span>

<span data-ttu-id="341a2-153">Дополнительные сведения о сопоставлении открытых проводок см. в разделе [Обзор сопоставления](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="341a2-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
