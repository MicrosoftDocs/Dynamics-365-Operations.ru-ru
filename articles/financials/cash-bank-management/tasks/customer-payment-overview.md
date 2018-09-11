--- 
title: "Обзор платежей клиентов"
description: "В этом проводнике по задаче иллюстрируются различные методы ввода платежей клиентов."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0e534a468a49f0221c3ee2b8999264a3fbeaf774
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="customer-payment-overview"></a><span data-ttu-id="9e65e-103">Обзор платежей клиентов</span><span class="sxs-lookup"><span data-stu-id="9e65e-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e65e-104">В этом проводнике по задаче иллюстрируются различные методы ввода платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="9e65e-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="9e65e-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="9e65e-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9e65e-106">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="9e65e-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9e65e-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9e65e-107">Click New.</span></span>
3. <span data-ttu-id="9e65e-108">Выберите журнал платежей, в котором будут сохранены платежи клиентов.</span><span class="sxs-lookup"><span data-stu-id="9e65e-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="9e65e-109">Выберите журнал или укажите его вручную.</span><span class="sxs-lookup"><span data-stu-id="9e65e-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="9e65e-110">Щелкните "Ввод платежей клиента".</span><span class="sxs-lookup"><span data-stu-id="9e65e-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="9e65e-111">Ввод платежей клиентов используется для записи платежей клиентов по одному.</span><span class="sxs-lookup"><span data-stu-id="9e65e-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="9e65e-112">Информация о платеже вводится в верхней части, после чего можно пометить оплаченные этим платежом накладные на той же странице.</span><span class="sxs-lookup"><span data-stu-id="9e65e-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="9e65e-113">Введите клиента, от которого вы получили платеж.</span><span class="sxs-lookup"><span data-stu-id="9e65e-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="9e65e-114">Если вы не знаете, кто клиент, но знаете, какая проводка была оплачена, для ввода платежа можно использовать поле "Проводка".</span><span class="sxs-lookup"><span data-stu-id="9e65e-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="9e65e-115">Введите или выберите накладную в поле "Проводка".</span><span class="sxs-lookup"><span data-stu-id="9e65e-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="9e65e-116">После выбора проводки клиент будет выбран автоматически.</span><span class="sxs-lookup"><span data-stu-id="9e65e-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="9e65e-117">В поле "Ссылка на платеж" введите ссылку на платеж.</span><span class="sxs-lookup"><span data-stu-id="9e65e-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="9e65e-118">Ссылка на платеж может представлять собой номер чека клиента или номер из электронного платежа клиента.</span><span class="sxs-lookup"><span data-stu-id="9e65e-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="9e65e-119">Ссылка на платеж требуется только в том случае, если платеж помечается для включения в бланк депозита.</span><span class="sxs-lookup"><span data-stu-id="9e65e-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="9e65e-120">Выберите, будет ли платеж включен в бланк депозита.</span><span class="sxs-lookup"><span data-stu-id="9e65e-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="9e65e-121">Введите сумма платежа клиента.</span><span class="sxs-lookup"><span data-stu-id="9e65e-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="9e65e-122">Сумма платежа автоматически проставлена не будет.</span><span class="sxs-lookup"><span data-stu-id="9e65e-122">The payment amount will not default.</span></span> <span data-ttu-id="9e65e-123">Ее необходимо ввести вручную.</span><span class="sxs-lookup"><span data-stu-id="9e65e-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="9e65e-124">Пометьте накладные, оплаченные клиентом.</span><span class="sxs-lookup"><span data-stu-id="9e65e-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="9e65e-125">Если платеж является предоплатой, нет необходимости отмечать какие-либо накладные для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9e65e-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="9e65e-126">Платеж все равно можно будет сохранить и разнести.</span><span class="sxs-lookup"><span data-stu-id="9e65e-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="9e65e-127">Сопоставление с накладной можно будет сделать позднее.</span><span class="sxs-lookup"><span data-stu-id="9e65e-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="9e65e-128">Введите сумму платежа, которая должна быть сопоставлена с помеченной накладной.</span><span class="sxs-lookup"><span data-stu-id="9e65e-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="9e65e-129">Это поле можно использовать, когда платеж представляет собой частичную оплату.</span><span class="sxs-lookup"><span data-stu-id="9e65e-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="9e65e-130">Если не ввести сумму, сумма для сопоставления будет определена автоматически.</span><span class="sxs-lookup"><span data-stu-id="9e65e-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="9e65e-131">Щелкните "Сохранить в журнале".</span><span class="sxs-lookup"><span data-stu-id="9e65e-131">Click Save in journal.</span></span>
    * <span data-ttu-id="9e65e-132">Перед сохранением платежа в журнал убедитесь, что определен корреспондирующий счет.</span><span class="sxs-lookup"><span data-stu-id="9e65e-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="9e65e-133">При использовании команды "Сохранить в журнале" платеж будет сохранен и перенесен в журнал.</span><span class="sxs-lookup"><span data-stu-id="9e65e-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="9e65e-134">После этого можно будет переходить к вводу следующего платежа.</span><span class="sxs-lookup"><span data-stu-id="9e65e-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="9e65e-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e65e-135">Close the page.</span></span>
14. <span data-ttu-id="9e65e-136">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="9e65e-136">Click Lines.</span></span>
    * <span data-ttu-id="9e65e-137">Открыв "Строки", вы увидите все платежи, записанные на странице "Ввод платежей клиента" и сохраненные в журнале.</span><span class="sxs-lookup"><span data-stu-id="9e65e-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="9e65e-138">Эту страницу также можно использовать для ввода новых платежей клиентов или для редактирования платежа клиента перед его разноской.</span><span class="sxs-lookup"><span data-stu-id="9e65e-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="9e65e-139">Щелкните "Создать", чтобы создать еще один платеж.</span><span class="sxs-lookup"><span data-stu-id="9e65e-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="9e65e-140">Выберите клиента, от которого вы получили платеж.</span><span class="sxs-lookup"><span data-stu-id="9e65e-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="9e65e-141">Если вы не знаете, кто клиент, но знаете, к какой накладной относится платеж, воспользуйтесь полем "Накладная", чтобы ввести накладную вручную или выбрать ее.</span><span class="sxs-lookup"><span data-stu-id="9e65e-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="9e65e-142">После выбора накладной клиент будет выбран автоматически.</span><span class="sxs-lookup"><span data-stu-id="9e65e-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="9e65e-143">Щелкните "Сопоставление проводок", чтобы пометить оплаченные накладные.</span><span class="sxs-lookup"><span data-stu-id="9e65e-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="9e65e-144">Сопоставлять платеж с какими-либо накладными не обязательно.</span><span class="sxs-lookup"><span data-stu-id="9e65e-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="9e65e-145">Если это предоплата или вы не знаете, какая накладная была оплачена, вы можете ввести и разнести платеж.</span><span class="sxs-lookup"><span data-stu-id="9e65e-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="9e65e-146">Платеж можно будет сопоставить с накладной на более позднем этапе.</span><span class="sxs-lookup"><span data-stu-id="9e65e-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="9e65e-147">Пометьте накладные, оплаченные этим платежом.</span><span class="sxs-lookup"><span data-stu-id="9e65e-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="9e65e-148">Введите сумму платежа, которая будет сопоставлена с помеченной накладной.</span><span class="sxs-lookup"><span data-stu-id="9e65e-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="9e65e-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9e65e-149">Click OK.</span></span>
21. <span data-ttu-id="9e65e-150">В поле "Ссылка на платеж" введите ссылку на платеж.</span><span class="sxs-lookup"><span data-stu-id="9e65e-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="9e65e-151">.</span><span class="sxs-lookup"><span data-stu-id="9e65e-151">.</span></span>
    * <span data-ttu-id="9e65e-152">Ссылка на платеж требуется только в том случае, если платеж помечается для включения в бланк депозита.</span><span class="sxs-lookup"><span data-stu-id="9e65e-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="9e65e-153">Разнесите платежи клиентов.</span><span class="sxs-lookup"><span data-stu-id="9e65e-153">Post the customer payments.</span></span> 


