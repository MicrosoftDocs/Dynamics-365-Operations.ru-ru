---
title: "Настройка и обработка платежных поручений для России"
description: "В этой теме рассматривается, как настраивать и обрабатывать платежные поручения для России."
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 003b7eac16c1be50bc982da0672df42a87a69722
ms.openlocfilehash: ebc663d0c8b9c24648c2bca5fd38806bf301606c
ms.contentlocale: ru-ru
ms.lasthandoff: 11/05/2018

---

# <a name="set-up-and-process-payment-orders-for-russia"></a><span data-ttu-id="4e27f-103">Настройка и обработка платежных поручений для России</span><span class="sxs-lookup"><span data-stu-id="4e27f-103">Set up and process payment orders for Russia</span></span>

[!include [banner](../includes/banner.md)]

## <a name="setup-for-generating-payment-orders"></a><span data-ttu-id="4e27f-104">Настройка для формирования платежных поручений</span><span class="sxs-lookup"><span data-stu-id="4e27f-104">Setup for generating payment orders</span></span>

<span data-ttu-id="4e27f-105">Прежде чем формировать платежные поручения, необходимо настроить следующее:</span><span class="sxs-lookup"><span data-stu-id="4e27f-105">Before you can generate payment orders, you must complete the following setup:</span></span>

- <span data-ttu-id="4e27f-106">Настроить банки и банковские счета для компании.</span><span class="sxs-lookup"><span data-stu-id="4e27f-106">Set up banks and bank accounts for the company.</span></span> <span data-ttu-id="4e27f-107">Дополнительные сведения см. в разделе [Локальные настройки и реквизиты для модуля "Банк"](rus-local-settings-requisites-bank-module.md).</span><span class="sxs-lookup"><span data-stu-id="4e27f-107">For more information, see [Local settings and requisites for Bank module](rus-local-settings-requisites-bank-module.md).</span></span>
- <span data-ttu-id="4e27f-108">Настроить банковские счета поставщиков и банковские счета клиентов:</span><span class="sxs-lookup"><span data-stu-id="4e27f-108">Set up vendor bank accounts and customer bank accounts:</span></span>

    1. <span data-ttu-id="4e27f-109">На странице "Все клиенты" или "Все поставщики" выберите **Банковские счета** на вкладке **ПОСТАВЩИК**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-109">In the All customers or All vendors page, select **Bank accounts** on **VENDOR** tab.</span></span>
    2. <span data-ttu-id="4e27f-110">Создайте банковский счет и введите все необходимые данные.</span><span class="sxs-lookup"><span data-stu-id="4e27f-110">Create a bank account, and fill in all the required information.</span></span>
    3. <span data-ttu-id="4e27f-111">В случае банковских счетов зарубежных клиентов или поставщиков на экспресс-вкладке **Общие** в разделе **Иностранный банк** в поле **Банковские группы** выберите код иностранного банка, в котором зарегистрирован банковский счет клиента.</span><span class="sxs-lookup"><span data-stu-id="4e27f-111">For foreign customer or vendor bank accounts, on the **General** FastTab, in the **Foreign bank** section, in the **Bank groups** field, select the code of the foreign bank that the customer bank account is registered with.</span></span> <span data-ttu-id="4e27f-112">В поле **Номер банковского счета** введите номер иностранного банковского счета, на который будут поступать платежи.</span><span class="sxs-lookup"><span data-stu-id="4e27f-112">In the **Bank account number** field, enter the foreign bank account number for the account that receives payments.</span></span> <span data-ttu-id="4e27f-113">Наконец, в поле **SWIFT** введите SWIFT-код банка, получающего платежи.</span><span class="sxs-lookup"><span data-stu-id="4e27f-113">Finally, in the **SWIFT** field, enter the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of the bank that receives payments.</span></span>

    ![Банковский счет поставщика](media/rus-vendor-bank-account-screenshot-5.jpg)

- <span data-ttu-id="4e27f-115">Для формирования платежей поставщикам настройте способ оплаты в разделе **Расчеты с поставщиками \> Настройка платежей \> Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-115">To generate payments to vendors, set up a method of payment at **Accounts payable \> Payment setup \> Methods of payment**.</span></span> <span data-ttu-id="4e27f-116">Для формирования возвратов платежей клиентам настройте способ оплаты в разделе **Расчеты с клиентами \> Настройка платежей \> Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-116">To generate payment returns to customers, set up a method of payment at **Accounts receivable \> Payment setup \> Methods of payment**.</span></span>
- <span data-ttu-id="4e27f-117">Для печати платежных поручений в российских рублях в соответствии с форматом бумаги на странице **Способы оплаты** на экспресс-вкладке **Форматы файлов** в поле **Формат экспорта** выберите **Платежное поручение в рублях**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-117">To print payment orders in Russian rubles according to the paper format, on the **Methods of payment** page, on the **File formats** FastTab, in the **Export format** field, select **Payment order in RUB**.</span></span> <span data-ttu-id="4e27f-118">Для печати платежных поручений в иностранной валюте в соответствии с шаблоном конкретного банка в поле **Формат экспорта** выберите **Валютное платежное поручение**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-118">To print payment orders in a foreign currency according to a bank-specific template, in the **Export format** field, select **Payment order in currency**.</span></span> <span data-ttu-id="4e27f-119">(Шаблон для конкретного банка определяется в банковском счете).</span><span class="sxs-lookup"><span data-stu-id="4e27f-119">(The bank-specific template is defined in the bank account.)</span></span>

## <a name="generate-a-payment-order-in-russian-rubles-for-a-payment-to-a-vendor"></a><span data-ttu-id="4e27f-120">Создание платежного поручения в российских рублях для платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="4e27f-120">Generate a payment order in Russian rubles for a payment to a vendor</span></span>

### <a name="create-payment-order-lines"></a><span data-ttu-id="4e27f-121">Создание строк платежного поручения</span><span class="sxs-lookup"><span data-stu-id="4e27f-121">Create payment order lines</span></span>
<span data-ttu-id="4e27f-122">Прежде чем формировать платежное поручение, необходимо создать строки платежного поручения.</span><span class="sxs-lookup"><span data-stu-id="4e27f-122">Before you can generate a payment order, you must create payment order lines.</span></span>

1. <span data-ttu-id="4e27f-123">Выберите **Расчеты с поставщиками \> Платежи \> Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-123">Select **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="4e27f-124">Создайте журнал, а затем в области действий выберите **Строки**, чтобы открыть страницу **Платежи поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-124">Create a journal, and then, on the Action Pane, select **Lines** to open the **Vendor payments** page.</span></span>
3. <span data-ttu-id="4e27f-125">Создайте строку платежа поставщику.</span><span class="sxs-lookup"><span data-stu-id="4e27f-125">Create a vendor payment line.</span></span>
4. <span data-ttu-id="4e27f-126">В поле **Дата** укажите дату платежа.</span><span class="sxs-lookup"><span data-stu-id="4e27f-126">In the **Date** field, select the date of payment.</span></span>
5. <span data-ttu-id="4e27f-127">В поле **Счет** выберите счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="4e27f-127">In the **Account** field, select the vendor account.</span></span>
6. <span data-ttu-id="4e27f-128">В поле **Текст проводки** введите описание проводки.</span><span class="sxs-lookup"><span data-stu-id="4e27f-128">In the **Transaction text** field, enter text that describes the transaction.</span></span>
7. <span data-ttu-id="4e27f-129">В поле **Дебет** введите сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="4e27f-129">In the **Debit** field, enter the sum of the payment.</span></span>
8. <span data-ttu-id="4e27f-130">В поле **Валюта** выберите код валюты.</span><span class="sxs-lookup"><span data-stu-id="4e27f-130">In the **Currency** field, select the currency code.</span></span>
9. <span data-ttu-id="4e27f-131">В поле **Тип корр. счета** выберите тип выбранного счета.</span><span class="sxs-lookup"><span data-stu-id="4e27f-131">In the **Offset account type** field, select the account type for the selected account.</span></span>
10. <span data-ttu-id="4e27f-132">В поле **Корр. счет** выберите корреспондентский счет для проводки.</span><span class="sxs-lookup"><span data-stu-id="4e27f-132">In the **Offset account** field, select the offset account for the transaction.</span></span>
11. <span data-ttu-id="4e27f-133">В поле **Валюта** выберите код валюты.</span><span class="sxs-lookup"><span data-stu-id="4e27f-133">In the **Currency** field, select the currency code.</span></span>
12. <span data-ttu-id="4e27f-134">В поле **Способ оплаты** выберите способ оплаты, который будет использоваться для поставщика.</span><span class="sxs-lookup"><span data-stu-id="4e27f-134">In the **Method of payment** field, select the method of payment to use for the vendor.</span></span>
13. <span data-ttu-id="4e27f-135">В поле **Код договора** выберите регистрационный номер договора.</span><span class="sxs-lookup"><span data-stu-id="4e27f-135">In the **Agreement ID** field, select the registration number of the contract.</span></span>
14. <span data-ttu-id="4e27f-136">В полях **Налоговая группа** и **Налоговая группа номенклатур** выберите налоговые группы для вычисления НДС.</span><span class="sxs-lookup"><span data-stu-id="4e27f-136">In the **Sales tax group** and **Item sales tax group** fields, select the tax groups for the calculation of value-added tax (VAT).</span></span>
15. <span data-ttu-id="4e27f-137">На вкладке **Банк** в поле **Тип банковской проводки** выберите тип проводки.</span><span class="sxs-lookup"><span data-stu-id="4e27f-137">On the **Bank** tab, in the **Bank transaction type** field, select the transaction type.</span></span>
16. <span data-ttu-id="4e27f-138">В поле **Идентификатор счета** выберите банковский счет получателя.</span><span class="sxs-lookup"><span data-stu-id="4e27f-138">In the **Account identification** field, select the bank account of the recipient.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4e27f-139">Если платежное поручение создается для юридического лица поставщика, необходимо ввести счет поставщика в поле **Платежка на**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-139">If you're generating a payment order for a legal representative of the vendor, you must enter the vendor account in the **Payment documented on** field.</span></span> <span data-ttu-id="4e27f-140">В этом случае бланк платежного поручения будет ссылаться на банк поставщика, указанный в поле **Платежка на**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-140">In this case, the payment order slip will refer to the bank of the vendor that is specified in the **Payment documented on** field.</span></span> <span data-ttu-id="4e27f-141">Однако проводка будет произведена для поставщика, указанного в поле **Счета**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-141">However, the transaction will be performed for the vendor that is specified in the **Account** field.</span></span>

17. <span data-ttu-id="4e27f-142">На вкладке **Платежное поручение** в поле **Назначение платежа** введите текст, который должен быть отражен в платежном поручении.</span><span class="sxs-lookup"><span data-stu-id="4e27f-142">On the **Payment order** tab, in the **Purpose text** field, enter any text that must be reflected on the payment order.</span></span>

    <span data-ttu-id="4e27f-143">Если выбрать **НДС в платежном поручении** будет введен текст.</span><span class="sxs-lookup"><span data-stu-id="4e27f-143">If you select **VAT in payment order**, the text will be entered.</span></span> <span data-ttu-id="4e27f-144">Этот текст включает в себя сумму НДС в поле **Назначение платежа**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-144">This text includes the VAT amount in the **Purpose text** field.</span></span>

19. <span data-ttu-id="4e27f-145">Задайте следующие поля: **Очередность платежа**, **Код статуса**, **Код доходов бюджета**, **Основание платежа**, **Вид платежа**, **УИН**, а также поля в разделе **Период** (**Код периода**, **Номер периода**, **Год**, **Дата периода**).</span><span class="sxs-lookup"><span data-stu-id="4e27f-145">Set the following fields: **Order of payment**, **Number status**, **Budget revenue code**, **Origin payment**, **Payment type**, **UCI**, and the fields in the **Period** section (**Period code**, **Period number**, **Year**, **Period date**).</span></span> <span data-ttu-id="4e27f-146">Эти значения будут напечатаны в соответствующих полях платежного поручения для поставщика или налогового органа.</span><span class="sxs-lookup"><span data-stu-id="4e27f-146">The values will be printed in the corresponding boxes on the payment order for the vendor or tax authority.</span></span>

    ![Платежи поставщикам](media/rus-vendor-payments-screenshot-4.jpg)

### <a name="generate-a-payment-order"></a><span data-ttu-id="4e27f-148">Создание платежного поручения</span><span class="sxs-lookup"><span data-stu-id="4e27f-148">Generate a payment order</span></span>
<span data-ttu-id="4e27f-149">После создания строк платежного поручения можно сформировать платежное поручение.</span><span class="sxs-lookup"><span data-stu-id="4e27f-149">After you've created payment order lines, you can generate the payment order.</span></span>

1. <span data-ttu-id="4e27f-150">На странице **Платежи поставщикам** в области действий выберите **Создание платежей**, чтобы открыть диалоговое окно **Создание платежей**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-150">On the **Vendor payments** page, on the Action Pane, select **Generate payments** to open the **Generate payments** dialog box.</span></span>
2. <span data-ttu-id="4e27f-151">В поле **Способ оплаты** выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="4e27f-151">In the **Method of payment** field, select the method of payment.</span></span> <span data-ttu-id="4e27f-152">Другой вариант — в поле **Формат экспорта** выберите **Платежное поручение в рублях**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-152">Alternatively, in the **Export format** field, select **Payment order in RUB**.</span></span>
3. <span data-ttu-id="4e27f-153">В поле **Банковский счет** выберите банковский счет, с которого будет произведен платеж.</span><span class="sxs-lookup"><span data-stu-id="4e27f-153">In the **Bank account** field, select the bank account that the payment should be made from.</span></span>
4. <span data-ttu-id="4e27f-154">Выберите **OK**, чтобы открыть диалоговое окно **Настройка платежного поручения**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-154">Select **OK** to open the **Payment order setup** dialog box.</span></span> 
5. <span data-ttu-id="4e27f-155">Установите для параметра **Документ** значение **Да**, чтобы напечатать платежное поручение, и установите для параметра **Текст доверенности** значение **Да**, чтобы напечатать текст.</span><span class="sxs-lookup"><span data-stu-id="4e27f-155">Set the **Document** option to **Yes** to print the payment order, and set the **Proxy text** option to **Yes** to print the text.</span></span>
6. <span data-ttu-id="4e27f-156">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-156">Select **OK**.</span></span> <span data-ttu-id="4e27f-157">Создается платежное поручение, а статус платежа для соответствующей строки журнала платежей изменяется на **Отправлено**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-157">The payment order is generated, and the payment status of the appropriate payment journal line is changed to **Sent**.</span></span>

### <a name="void-a-payment-order"></a><span data-ttu-id="4e27f-158">Аннулирование платежного поручения</span><span class="sxs-lookup"><span data-stu-id="4e27f-158">Void a payment order</span></span>

<span data-ttu-id="4e27f-159">Аннулировать платежное поручение можно в журнале платежей.</span><span class="sxs-lookup"><span data-stu-id="4e27f-159">You can void a payment order in the payment journal.</span></span> <span data-ttu-id="4e27f-160">На странице **Платежи поставщикам** в области действий выберите **Функции \> Аннулировать п/п**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-160">On the **Vendor payments** page, on the Action Pane, select **Functions \> Void payment order**.</span></span> <span data-ttu-id="4e27f-161">Статус оплаты строки журнала платежей для аннулированного платежа меняется на **Нет**, и аннулированное платежное поручение удаляется из реестра платежных поручений.</span><span class="sxs-lookup"><span data-stu-id="4e27f-161">The payment status of the payment journal line for the voided payment order is changed to **None**, and the voided payment order is deleted from the registry of payment orders.</span></span>

### <a name="reprint-a-payment-order"></a><span data-ttu-id="4e27f-162">Повторная печать платежного поручения</span><span class="sxs-lookup"><span data-stu-id="4e27f-162">Reprint a payment order</span></span>

<span data-ttu-id="4e27f-163">Платежное поручение можно напечатать повторно.</span><span class="sxs-lookup"><span data-stu-id="4e27f-163">You can reprint a payment order.</span></span> <span data-ttu-id="4e27f-164">На странице **Платежи поставщикам** в области действий выберите **Печать \> Печать платежного поручения**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-164">On the **Vendor payments** page, on the Action Pane, select **Print \> Print payment order**.</span></span> <span data-ttu-id="4e27f-165">Платежные поручения можно также повторно напечатать со страницы **Банковские проводки**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-165">You can also reprint payment orders from the **Bank transactions** page.</span></span> <span data-ttu-id="4e27f-166">Выберите ваучер платежного поручения, затем выберите **Печать \> Платежное поручение**, чтобы распечатать документ.</span><span class="sxs-lookup"><span data-stu-id="4e27f-166">Select the voucher for the payment order, and then select **Print \> Payment order** to print the document.</span></span>

### <a name="view-generated-payment-orders"></a><span data-ttu-id="4e27f-167">Просмотр сформированных платежных поручений</span><span class="sxs-lookup"><span data-stu-id="4e27f-167">View generated payment orders</span></span>

<span data-ttu-id="4e27f-168">Сформированные платежные поручения можно просмотреть на странице **Реестр платежных поручений** (**Расчеты с поставщиками \> Запросы и отчеты \> Платеж \> Реестр платежных поручений**).</span><span class="sxs-lookup"><span data-stu-id="4e27f-168">You can review generated payment orders on the **Registry of payment orders** page (**Accounts payable \> Inquiries and reports \> Payment \> Payment order register**).</span></span> <span data-ttu-id="4e27f-169">На вкладке **Реквизиты** просмотрите информацию о плательщике и получателе.</span><span class="sxs-lookup"><span data-stu-id="4e27f-169">On the **Essential elements** tab, review the information about the payer and the recipient.</span></span>

## <a name="generate-a-payment-order-for-a-payment-return-to-a-customer"></a><span data-ttu-id="4e27f-170">Создание платежного поручения клиента для возврата платежа клиенту</span><span class="sxs-lookup"><span data-stu-id="4e27f-170">Generate a payment order for a payment return to a customer</span></span>

<span data-ttu-id="4e27f-171">Можно сформировать платежное поручение для возврата средств клиенту.</span><span class="sxs-lookup"><span data-stu-id="4e27f-171">You can generate a payment order for a money return to a customer.</span></span>

1. <span data-ttu-id="4e27f-172">Выберите **Расчеты с клиентами \> Платежи \> Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-172">Select **Accounts receivable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="4e27f-173">Создайте журнал, а затем в области действий выберите **Строки**, чтобы открыть страницу **Платежи клиентов**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-173">Create a journal, and then, on the Action Pane, select **Lines** to open the **Customer payments** page.</span></span>
3. <span data-ttu-id="4e27f-174">Создайте строку платежа клиенту.</span><span class="sxs-lookup"><span data-stu-id="4e27f-174">Create a customer payment line.</span></span> <span data-ttu-id="4e27f-175">Введите информацию так же, как при создании строки платежа поставщику ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="4e27f-175">Enter information as you did when you created a vendor payment line earlier in this topic.</span></span>
4. <span data-ttu-id="4e27f-176">На вкладке **Банк** в поле **Идентификатор счета** введите номер банковского счета, соответствующий счету клиента, который должен получить возврат платежа.</span><span class="sxs-lookup"><span data-stu-id="4e27f-176">On the **Bank** tab, in the **Account identification** field, enter the bank account number of the customer account that should receive the payment return.</span></span>
5. <span data-ttu-id="4e27f-177">В поле **Платежка на** выберите счет клиента, который должен получить возврат платежа.</span><span class="sxs-lookup"><span data-stu-id="4e27f-177">In the **Payment documented on** field, select the customer account that should receive the payment return.</span></span>
6. <span data-ttu-id="4e27f-178">В области действий выберите **Функции \> Создание платежей**, чтобы создать платежное поручение.</span><span class="sxs-lookup"><span data-stu-id="4e27f-178">On the Action Pane, select **Functions \> Generate payments** to generate a payment order.</span></span>

<span data-ttu-id="4e27f-179">Сформированные платежные поручения для клиентов можно просмотреть на странице **Реестр платежных поручений** (**Расчеты с клиентами \> Запросы и отчеты \> Платеж \> Реестр платежных поручений**).</span><span class="sxs-lookup"><span data-stu-id="4e27f-179">You can review generated payment orders for customers on the **Registry of payment orders** page (**Accounts receivable \> Inquiries \> Payment \> Payment order register**).</span></span> 


## <a name="review-registry-of-payment-orders"></a><span data-ttu-id="4e27f-180">Просмотр реестра платежных поручений</span><span class="sxs-lookup"><span data-stu-id="4e27f-180">Review Registry of payment orders</span></span>

<span data-ttu-id="4e27f-181">Отчет реестра платежных поручений содержит список платежных поручений для банковского счета за период.</span><span class="sxs-lookup"><span data-stu-id="4e27f-181">The registry of payment orders report contains the list of payment orders for a bank account in a period.</span></span> <span data-ttu-id="4e27f-182">Этот отчет содержит следующие данные для каждого платежного поручения:</span><span class="sxs-lookup"><span data-stu-id="4e27f-182">This report includes the following data for each payment order:</span></span>

- <span data-ttu-id="4e27f-183">Номер и дата</span><span class="sxs-lookup"><span data-stu-id="4e27f-183">Number and date</span></span>
- <span data-ttu-id="4e27f-184">Наименование и номер банковского счета контрагента</span><span class="sxs-lookup"><span data-stu-id="4e27f-184">Name and bank account number of counteragent</span></span>
- <span data-ttu-id="4e27f-185">Назн. плат.</span><span class="sxs-lookup"><span data-stu-id="4e27f-185">Payment purpose</span></span>
- <span data-ttu-id="4e27f-186">Сумма платежа и код валюты</span><span class="sxs-lookup"><span data-stu-id="4e27f-186">Payment amount and currency code</span></span>
- <span data-ttu-id="4e27f-187">Статус платежа</span><span class="sxs-lookup"><span data-stu-id="4e27f-187">Status of payment</span></span>
- <span data-ttu-id="4e27f-188">Примечание, указывающее, является ли платеж электронным</span><span class="sxs-lookup"><span data-stu-id="4e27f-188">Note indicating if the payment is electronic</span></span>

<span data-ttu-id="4e27f-189">Чтобы запустить отчет, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="4e27f-189">To run the report, complete the following steps.</span></span>
1. <span data-ttu-id="4e27f-190">Выберите **Расчеты с поставщиками > Запросы и отчеты > Платеж > Реестр платежных поручений** или **Расчеты с клиентами > Запросы > Платеж > Реестр платежных поручений**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-190">Go to **Accounts payable > Inquiries and reports > Payment > Payment order register** or **Accounts receivable > Inquiries > Payment > Payment order register**.</span></span>
2. <span data-ttu-id="4e27f-191">Щелкните **Печать > Реестр платежных поручений**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-191">Click **Print > Registry of payment orders**.</span></span>
3. <span data-ttu-id="4e27f-192">Выберите **Начальная дата** и **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="4e27f-192">Select the **From date** and **To date**.</span></span>
4. <span data-ttu-id="4e27f-193">Определите следующие фильтры для платежных поручений: **Статус платежного поручения**, **Код валюты**, **Банковский счет** и примечание **Электронный платеж** (Все, Электронный, Печатная форма).</span><span class="sxs-lookup"><span data-stu-id="4e27f-193">Define the following filters for payment orders: **Payment order status**, **Curreny code**, **Bank account** and **Electronic payment** remark (All, Electronic, Printout form).</span></span>
5. <span data-ttu-id="4e27f-194">Щелкните **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="4e27f-194">Click **OK** to generate the report.</span></span>


