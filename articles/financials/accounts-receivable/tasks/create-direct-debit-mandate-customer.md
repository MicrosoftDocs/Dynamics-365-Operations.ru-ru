--- 
title: "Создание поручения на безакцептное списание для клиента"
description: "В этом руководстве по задаче показано, как создать поручение на безакцептное списание и использовать его в накладной."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 66aa30e88cec914a9cd4d02a0992ff7570d1ced2
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="df0a2-103">Создание поручения на безакцептное списание для клиента</span><span class="sxs-lookup"><span data-stu-id="df0a2-103">Create a direct debit mandate for a customer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df0a2-104">В этом руководстве по задаче показано, как создать поручение на безакцептное списание и использовать его в накладной.</span><span class="sxs-lookup"><span data-stu-id="df0a2-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="df0a2-105">Создание банковского счета</span><span class="sxs-lookup"><span data-stu-id="df0a2-105">Create a bank account</span></span>
1. <span data-ttu-id="df0a2-106">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="df0a2-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="df0a2-107">Например, выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="df0a2-107">For example, select US-001</span></span>
3. <span data-ttu-id="df0a2-108">В области действий щелкните "Клиент".</span><span class="sxs-lookup"><span data-stu-id="df0a2-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="df0a2-109">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="df0a2-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="df0a2-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="df0a2-110">Click New.</span></span>
6. <span data-ttu-id="df0a2-111">В поле "Банковский счет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="df0a2-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="df0a2-113">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="df0a2-114">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="df0a2-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="df0a2-115">Click Save.</span></span>
11. <span data-ttu-id="df0a2-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="df0a2-116">Close the page.</span></span>
12. <span data-ttu-id="df0a2-117">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="df0a2-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="df0a2-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="df0a2-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="df0a2-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="df0a2-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="df0a2-120">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="df0a2-120">Click Edit.</span></span>
16. <span data-ttu-id="df0a2-121">Разверните раздел "Дополнительная идентификация".</span><span class="sxs-lookup"><span data-stu-id="df0a2-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="df0a2-122">В поле "Код прямого дебетования" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="df0a2-123">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="df0a2-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="df0a2-124">Close the page.</span></span>
20. <span data-ttu-id="df0a2-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="df0a2-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="df0a2-126">Определение способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="df0a2-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="df0a2-127">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="df0a2-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="df0a2-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="df0a2-128">Click New.</span></span>
3. <span data-ttu-id="df0a2-129">В поле "Способ оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="df0a2-130">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="df0a2-131">Типом платежа для способа оплаты поручения на безакцептное списание должен быть электронный платеж.</span><span class="sxs-lookup"><span data-stu-id="df0a2-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="df0a2-132">Выберите значение "Да" в поле "Требуется поручение".</span><span class="sxs-lookup"><span data-stu-id="df0a2-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="df0a2-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="df0a2-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="df0a2-134">Добавьте поручение на безакцептное списание к клиенту.</span><span class="sxs-lookup"><span data-stu-id="df0a2-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="df0a2-135">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="df0a2-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="df0a2-136">Например, выберите US-001.</span><span class="sxs-lookup"><span data-stu-id="df0a2-136">For example, select US-001</span></span>
3. <span data-ttu-id="df0a2-137">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="df0a2-137">Click Edit.</span></span>
4. <span data-ttu-id="df0a2-138">Разверните раздел "Значения платежа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="df0a2-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="df0a2-139">В поле "Способ оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="df0a2-140">Разверните раздел "Значения платежа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="df0a2-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="df0a2-141">Разверните раздел "Поручения на безакцептное списание".</span><span class="sxs-lookup"><span data-stu-id="df0a2-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="df0a2-142">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="df0a2-142">Click Add.</span></span>
9. <span data-ttu-id="df0a2-143">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="df0a2-144">В поле "Банковский счет кредитора" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="df0a2-145">Введите количество платежей, которые ожидается обработать для этого поручения.</span><span class="sxs-lookup"><span data-stu-id="df0a2-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="df0a2-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="df0a2-146">Click OK.</span></span>
13. <span data-ttu-id="df0a2-147">Нажмите кнопку Печать.</span><span class="sxs-lookup"><span data-stu-id="df0a2-147">Click Print.</span></span>
14. <span data-ttu-id="df0a2-148">Щелкните "Отчет по поручению".</span><span class="sxs-lookup"><span data-stu-id="df0a2-148">Click Mandate report.</span></span>
15. <span data-ttu-id="df0a2-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="df0a2-149">Close the page.</span></span>
16. <span data-ttu-id="df0a2-150">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="df0a2-150">Click Edit.</span></span>
17. <span data-ttu-id="df0a2-151">В поле "Дата подписи" введите дату.</span><span class="sxs-lookup"><span data-stu-id="df0a2-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="df0a2-152">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="df0a2-152">Click Yes.</span></span>
19. <span data-ttu-id="df0a2-153">Введите место подписания поручения.</span><span class="sxs-lookup"><span data-stu-id="df0a2-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="df0a2-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="df0a2-154">Click OK.</span></span>
21. <span data-ttu-id="df0a2-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="df0a2-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="df0a2-156">Создание накладной с произвольным текстом с поручением</span><span class="sxs-lookup"><span data-stu-id="df0a2-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="df0a2-157">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Все накладные с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="df0a2-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="df0a2-158">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="df0a2-158">Click New.</span></span>
3. <span data-ttu-id="df0a2-159">Выберите клиента, к которому добавлено получение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="df0a2-160">В поле код предписания прямого дебетования введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="df0a2-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


