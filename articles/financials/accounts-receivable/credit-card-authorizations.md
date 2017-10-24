---
title: "Настройка, авторизация и захват кредитной карточки"
description: "Эта статья содержит обзор авторизации кредитной карты в Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Она включает информацию о том, как настроить службу платежей, добавить кредитную карту в заказ на продажу и аннулировать авторизацию."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dad3964003d0be0c22b0346aba2b3319278ffaa9
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="a3fbd-104">Настройка, авторизация и захват кредитной карточки</span><span class="sxs-lookup"><span data-stu-id="a3fbd-104">Credit card setup, authorization, and capture</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="a3fbd-105">Эта статья содержит обзор авторизации кредитной карты в Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="a3fbd-106">Она включает информацию о том, как настроить службу платежей, добавить кредитную карту в заказ на продажу и аннулировать авторизацию.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="a3fbd-107">Настройка службы оплаты по кредитной карточке</span><span class="sxs-lookup"><span data-stu-id="a3fbd-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="a3fbd-108">Для использования кредитных карточек вы должны настроить и активировать службу оплаты на странице "Службы платежей".</span><span class="sxs-lookup"><span data-stu-id="a3fbd-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="a3fbd-109">Служба платежей действует как мост между вашим юридическим лицом и банком, который обрабатывает платежи по кредитной карточке клиента.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="a3fbd-110">Вы должны работать с поставщиком кредитных карточек, который указан в поле "Соединитель платежей" и настроить учетную запись у этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="a3fbd-111">Вы должны после этого настроить другие параметры на странице "Службы платежей", настроить типы кредитной карт для American Express, Discover, MasterCard и Discover на странице "Типы кредитных карт" и активировать поставщика как поставщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="a3fbd-112">Вы должны также выполнить следующие шаги для того, чтобы завершить вашу установку:</span><span class="sxs-lookup"><span data-stu-id="a3fbd-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="a3fbd-113">На странице "Параметры модуля расчетов с клиентами" определите параметры для использования авторизаций кредитной карты.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="a3fbd-114">На странице "Условия оплаты" настройте условия платежа для кредитных карт.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="a3fbd-115">В поле "Вид платежа" выберите "Кредитная карта".</span><span class="sxs-lookup"><span data-stu-id="a3fbd-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="a3fbd-116">На странице "Кредитные карты клиента" введите сведения о кредитной карте для клиентов.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="a3fbd-117">Добавление новой кредитной карты</span><span class="sxs-lookup"><span data-stu-id="a3fbd-117">Adding a new credit card</span></span>
<span data-ttu-id="a3fbd-118">Вы можете создать новые записи кредитной карточки на странице "Клиенты" путем использования пунктов "Клиент", "Настройка", "Кредитная карта".</span><span class="sxs-lookup"><span data-stu-id="a3fbd-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="a3fbd-119">Вы можете также создать записи кредитной карты, когда вы вводите заказы на продажу на странице "Заказ на продажу", путем использования пунктов "Управление", "Клиент", "Кредитная карта", "Регистрация".</span><span class="sxs-lookup"><span data-stu-id="a3fbd-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>
<span data-ttu-id="a3fbd-120">Добавление кредитной карточки к заказу на продажу</span><span class="sxs-lookup"><span data-stu-id="a3fbd-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="a3fbd-121">Вы можете добавить кредитную карточку к заказу на продажу путем выбора кредитной карточки в функции поиска кредитной карточки на экспресс-вкладке "Цена и скидки" на странице "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="a3fbd-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="a3fbd-122">Чтобы начать процесс авторизации на панели действия на вкладке "Управление" выберите "Кредитная карточка" и "Авторизовать".</span><span class="sxs-lookup"><span data-stu-id="a3fbd-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>
<span data-ttu-id="a3fbd-123">Авторизация кредитной карты</span><span class="sxs-lookup"><span data-stu-id="a3fbd-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="a3fbd-124">Когда кредитная карта авторизуется, проверяется номер карты и имя ее владельца и подтверждается доступное сальдо по кредиту.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="a3fbd-125">Также возможна необязательная проверка контрольного кода карты и адреса владельца карты.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="a3fbd-126">Доступное клиенту кредитовое сальдо затем уменьшается на сумму, указанную в накладной.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="a3fbd-127">Служба платежей отправляет сведения о подтверждении или отклонении кредитной карты.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="a3fbd-128">Когда выставляется накладная по заказу на продажу, на кредитную карту возлагается (на ней блокируется) расход на сумму накладной.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="a3fbd-129">Контрольный код карты</span><span class="sxs-lookup"><span data-stu-id="a3fbd-129">Card verification value</span></span>

<span data-ttu-id="a3fbd-130">Вы можете запросить контрольный код карты, иногда называемый кодом безопасности карты.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="a3fbd-131">Для карты American Express это четырехзначное число.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="a3fbd-132">Для карт Discover, MasterCard и Visa это трехзначное число.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="a3fbd-133">Проверка адреса</span><span class="sxs-lookup"><span data-stu-id="a3fbd-133">Address verification</span></span>

<span data-ttu-id="a3fbd-134">Сведения о проверке адреса всегда отправляются поставщику платежных услуг.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="a3fbd-135">Вы можете решить, какой объем информации необходим для принятия проводки.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="a3fbd-136">Обязательно проверьте у вашего поставщика, принимает ли он эту информацию.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="a3fbd-137">Ниже приведены варианты для проверки адреса:</span><span class="sxs-lookup"><span data-stu-id="a3fbd-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="a3fbd-138">**Всегда принимать проводки**. Принимать проводку независимо от результатов проверки адреса.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="a3fbd-139">**Держатель счета**. Сравнить имя владельца карты, указанное в проводке, со сведениями компании, выпустившей кредитную карту.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="a3fbd-140">**Адрес выставления счета**. Сравнить имя владельца карты и адрес выставления счета, указанные в проводке, со сведениями компании, выпустившей кредитную карту.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="a3fbd-141">**Почтовый индекс выставления счетов**. Сравнить имя владельца карты, адрес выставления счета и почтовый индекс, указанные в проводке, со сведениями компании, выпустившей кредитную карту.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="a3fbd-142">Поддержка данных</span><span class="sxs-lookup"><span data-stu-id="a3fbd-142">Data support</span></span>
<span data-ttu-id="a3fbd-143">Для каждого поддерживаемого типа кредитной карты можно указать уровень поддержки данных.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="a3fbd-144">Этот уровень определяет, какой объем информации о проводке передается службе платежей.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="a3fbd-145">Обязательно проверьте у вашего поставщика, может ли он предоставить эту информацию.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="a3fbd-146">Ниже приведены варианты для уровня поддержки данных:</span><span class="sxs-lookup"><span data-stu-id="a3fbd-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="a3fbd-147">**Уровень 1**. Передача даты проводки, суммы проводки и описания.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="a3fbd-148">**Уровень 2**. Передача данных уровня 1, а также адреса отгрузки, адреса продавца и сведений о налогах.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="a3fbd-149">**Уровень 3**. Передача всех информации уровня 2 плюс сведений о строке заказа.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="a3fbd-150">Частичные платежи</span><span class="sxs-lookup"><span data-stu-id="a3fbd-150">Partial payments</span></span>
<span data-ttu-id="a3fbd-151">Если вы отгружаете часть заказа, регистрируется сумма частичного заказа и авторизация, проведенная для суммы целого заказа, закрывается.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="a3fbd-152">Затем производится новая авторизация для оставшейся суммы неотгруженного заказа.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="a3fbd-153">Аннулирование авторизации</span><span class="sxs-lookup"><span data-stu-id="a3fbd-153">Voiding an authorization</span></span>
<span data-ttu-id="a3fbd-154">Чтобы аннулировать авторизацию кредитной карты, вы можете изменить метод платежа на другой метод, который не имеет типа кредитной карточки.</span><span class="sxs-lookup"><span data-stu-id="a3fbd-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>






