---
title: Создание поручения на безакцептное списание для клиента
description: В этом руководстве по задаче показано, как создать поручение на безакцептное списание и использовать его в накладной.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef9beae6769c361680832d81ddda00e1237d3297
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241642"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="9aa10-103">Создание поручения на безакцептное списание для клиента</span><span class="sxs-lookup"><span data-stu-id="9aa10-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9aa10-104">В этом руководстве по задаче показано, как создать поручение на безакцептное списание и использовать его в накладной.</span><span class="sxs-lookup"><span data-stu-id="9aa10-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="9aa10-105">Создание банковского счета</span><span class="sxs-lookup"><span data-stu-id="9aa10-105">Create a bank account</span></span>
1. <span data-ttu-id="9aa10-106">В **области перехода** выберите **Модули > Расчеты с клиентами > Клиенты > Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="9aa10-107">В списке выберите запись.</span><span class="sxs-lookup"><span data-stu-id="9aa10-107">In the list, select a record.</span></span> <span data-ttu-id="9aa10-108">Например, выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="9aa10-108">For example, select US-001</span></span>
3. <span data-ttu-id="9aa10-109">В области действий щелкните **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="9aa10-110">Щелкните **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="9aa10-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-111">Click **New**.</span></span>
6. <span data-ttu-id="9aa10-112">В поле **Банковский счет** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="9aa10-113">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="9aa10-114">В поле **IBAN** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="9aa10-115">В поле **Валюта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="9aa10-116">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-116">Click **Save**.</span></span>
11. <span data-ttu-id="9aa10-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9aa10-117">Close the page.</span></span>
12. <span data-ttu-id="9aa10-118">В **области переходов** выберите **Модули > Управление банком и кассовыми операциями > Банковские счета > Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="9aa10-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9aa10-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9aa10-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9aa10-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="9aa10-121">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-121">Click **Edit**.</span></span>
16. <span data-ttu-id="9aa10-122">Разверните экспресс-вкладку **Дополнительная идентификация**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="9aa10-123">В поле **Код прямого дебетования** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="9aa10-124">В поле **IBAN** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="9aa10-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9aa10-125">Close the page.</span></span>
20. <span data-ttu-id="9aa10-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9aa10-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="9aa10-127">Определение способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="9aa10-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="9aa10-128">В **области переходов** выберите **Модули > Расчеты с клиентами > Настройка платежей > Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="9aa10-129">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-129">Click **New**.</span></span>
3. <span data-ttu-id="9aa10-130">В поле **Способ оплаты** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="9aa10-131">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9aa10-132">В поле **Тип платежа** выберите "Электронный платеж".</span><span class="sxs-lookup"><span data-stu-id="9aa10-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="9aa10-133">Типом платежа для способа оплаты поручения на безакцептное списание должен быть электронный платеж.</span><span class="sxs-lookup"><span data-stu-id="9aa10-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="9aa10-134">Выберите значение "Да" в поле **Требуется поручение**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="9aa10-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9aa10-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="9aa10-136">Добавьте поручение на безакцептное списание к клиенту.</span><span class="sxs-lookup"><span data-stu-id="9aa10-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="9aa10-137">В **области перехода** выберите **Модули > Расчеты с клиентами > Клиенты > Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="9aa10-138">В списке выберите запись.</span><span class="sxs-lookup"><span data-stu-id="9aa10-138">In the list, select a record.</span></span> <span data-ttu-id="9aa10-139">Например, выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="9aa10-139">For example, select US-001</span></span>
3. <span data-ttu-id="9aa10-140">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-140">Click **Edit**.</span></span>
4. <span data-ttu-id="9aa10-141">Разверните экспресс-вкладку **Значения платежа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="9aa10-142">В поле **Способ оплаты** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="9aa10-143">Разверните экспресс-вкладку **Значения платежа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="9aa10-144">Разверните экспресс-вкладку **Поручения на безакцептное списание**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="9aa10-145">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-145">Click **Add**.</span></span>
9. <span data-ttu-id="9aa10-146">В поле **Банковский счет** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="9aa10-147">В поле **Банковский счет кредитора** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="9aa10-148">В поле **Частота платежей** введите количество платежей, которые ожидается обработать для этого поручения.</span><span class="sxs-lookup"><span data-stu-id="9aa10-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="9aa10-149">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-149">Click **OK**.</span></span>
13. <span data-ttu-id="9aa10-150">Нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-150">Click **Print**.</span></span>
14. <span data-ttu-id="9aa10-151">Щелкните **Отчет по поручению**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="9aa10-152">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9aa10-152">Close the page.</span></span>
16. <span data-ttu-id="9aa10-153">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-153">Click **Edit**.</span></span>
17. <span data-ttu-id="9aa10-154">В поле **Дата подписи** введите дату.</span><span class="sxs-lookup"><span data-stu-id="9aa10-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="9aa10-155">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-155">Click **Yes**.</span></span>
19. <span data-ttu-id="9aa10-156">Введите место подписания поручения.</span><span class="sxs-lookup"><span data-stu-id="9aa10-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="9aa10-157">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-157">Click **OK**.</span></span>
21. <span data-ttu-id="9aa10-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9aa10-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="9aa10-159">Создание накладной с произвольным текстом с поручением</span><span class="sxs-lookup"><span data-stu-id="9aa10-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="9aa10-160">В **области переходов** выберите **Модули > Расчеты с клиентами > Накладные > Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="9aa10-161">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9aa10-161">Click **New**.</span></span>
3. <span data-ttu-id="9aa10-162">Выберите клиента, к которому добавлено получение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="9aa10-163">В поле **Код поручения на безакцептное списание** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9aa10-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]