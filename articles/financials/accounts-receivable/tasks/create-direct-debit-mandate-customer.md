---
title: Создание поручения на безакцептное списание для клиента
description: В этом руководстве по задаче показано, как создать поручение на безакцептное списание и использовать его в накладной.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572543"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="bf0ea-103">Создание поручения на безакцептное списание для клиента</span><span class="sxs-lookup"><span data-stu-id="bf0ea-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf0ea-104">В этом руководстве по задаче показано, как создать поручение на безакцептное списание и использовать его в накладной.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="bf0ea-105">Создание банковского счета</span><span class="sxs-lookup"><span data-stu-id="bf0ea-105">Create a bank account</span></span>
1. <span data-ttu-id="bf0ea-106">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="bf0ea-107">Например, выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-107">For example, select US-001</span></span>
3. <span data-ttu-id="bf0ea-108">В области действий щелкните "Клиент".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="bf0ea-109">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="bf0ea-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-110">Click New.</span></span>
6. <span data-ttu-id="bf0ea-111">В поле "Банковский счет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="bf0ea-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="bf0ea-113">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="bf0ea-114">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="bf0ea-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-115">Click Save.</span></span>
11. <span data-ttu-id="bf0ea-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-116">Close the page.</span></span>
12. <span data-ttu-id="bf0ea-117">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="bf0ea-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="bf0ea-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="bf0ea-120">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-120">Click Edit.</span></span>
16. <span data-ttu-id="bf0ea-121">Разверните раздел "Дополнительная идентификация".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="bf0ea-122">В поле "Код прямого дебетования" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="bf0ea-123">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="bf0ea-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-124">Close the page.</span></span>
20. <span data-ttu-id="bf0ea-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="bf0ea-126">Определение способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="bf0ea-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="bf0ea-127">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="bf0ea-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-128">Click New.</span></span>
3. <span data-ttu-id="bf0ea-129">В поле "Способ оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="bf0ea-130">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bf0ea-131">Типом платежа для способа оплаты поручения на безакцептное списание должен быть электронный платеж.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="bf0ea-132">Выберите значение "Да" в поле "Требуется поручение".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="bf0ea-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="bf0ea-134">Добавьте поручение на безакцептное списание к клиенту.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="bf0ea-135">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="bf0ea-136">Например, выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-136">For example, select US-001</span></span>
3. <span data-ttu-id="bf0ea-137">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-137">Click Edit.</span></span>
4. <span data-ttu-id="bf0ea-138">Разверните раздел "Значения платежа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="bf0ea-139">В поле "Способ оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="bf0ea-140">Разверните раздел "Значения платежа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="bf0ea-141">Разверните раздел "Поручения на безакцептное списание".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="bf0ea-142">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-142">Click Add.</span></span>
9. <span data-ttu-id="bf0ea-143">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="bf0ea-144">В поле "Банковский счет кредитора" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="bf0ea-145">Введите количество платежей, которые ожидается обработать для этого поручения.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="bf0ea-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-146">Click OK.</span></span>
13. <span data-ttu-id="bf0ea-147">Нажмите кнопку Печать.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-147">Click Print.</span></span>
14. <span data-ttu-id="bf0ea-148">Щелкните "Отчет по поручению".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-148">Click Mandate report.</span></span>
15. <span data-ttu-id="bf0ea-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-149">Close the page.</span></span>
16. <span data-ttu-id="bf0ea-150">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-150">Click Edit.</span></span>
17. <span data-ttu-id="bf0ea-151">В поле "Дата подписи" введите дату.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="bf0ea-152">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-152">Click Yes.</span></span>
19. <span data-ttu-id="bf0ea-153">Введите место подписания поручения.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="bf0ea-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-154">Click OK.</span></span>
21. <span data-ttu-id="bf0ea-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="bf0ea-156">Создание накладной с произвольным текстом с поручением</span><span class="sxs-lookup"><span data-stu-id="bf0ea-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="bf0ea-157">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Все накладные с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="bf0ea-158">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bf0ea-158">Click New.</span></span>
3. <span data-ttu-id="bf0ea-159">Выберите клиента, к которому добавлено получение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="bf0ea-160">В поле код предписания прямого дебетования введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

