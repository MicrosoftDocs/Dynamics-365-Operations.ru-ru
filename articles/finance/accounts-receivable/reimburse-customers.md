---
title: Зачет клиентов
description: В этом статье описан порядок создания проводок возмещения для группы клиентов. Если клиент имеет кредитовое сальдо, можно возместить клиенту сумму сальдо.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012147"
---
# <a name="reimburse-customers"></a><span data-ttu-id="8bb74-104">Зачет клиентов</span><span class="sxs-lookup"><span data-stu-id="8bb74-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bb74-105">В этом статье описан порядок создания проводок возмещения для группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="8bb74-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="8bb74-106">Если клиент имеет кредитовое сальдо, можно возместить клиенту сумму сальдо.</span><span class="sxs-lookup"><span data-stu-id="8bb74-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="8bb74-107">В следующей таблице показаны обязательные компоненты, которые должны быть подготовлены до начала работы.</span><span class="sxs-lookup"><span data-stu-id="8bb74-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="8bb74-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="8bb74-108">Prerequisite</span></span>                                                            | <span data-ttu-id="8bb74-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8bb74-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="8bb74-110">Укажите минимальную сумму возмещения для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="8bb74-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="8bb74-111">На странице **Параметры расчетов с клиентами** в области **Общее** в поле **Минимальный зачет** введите минимальную сумму, которую можно возместить по переплатам клиента.</span><span class="sxs-lookup"><span data-stu-id="8bb74-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="8bb74-112">(Необязательно) Добавьте счет поставщика к каждому клиенту, который может получать возмещение.</span><span class="sxs-lookup"><span data-stu-id="8bb74-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="8bb74-113">На странице **Клиенты** на экспресс-вкладке **Прочие подробные сведения** в поле **Счет поставщика** выберите счет поставщика для клиента.</span><span class="sxs-lookup"><span data-stu-id="8bb74-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="8bb74-114">При создании проводок возмещения создается накладная поставщика на сумму кредитового сальдо.</span><span class="sxs-lookup"><span data-stu-id="8bb74-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="8bb74-115">В процессе возмещения удаляется кредитового сальдо со счета клиента и создаются суммы задолженности для счета поставщика, который соответствует клиенту.</span><span class="sxs-lookup"><span data-stu-id="8bb74-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="8bb74-116">В модуле расчетов с клиентами запустите процесс **Возмещение** (**Расчеты с клиентами \> Периодические задачи \> Возмещение**).</span><span class="sxs-lookup"><span data-stu-id="8bb74-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="8bb74-117">Чтобы сгруппировать все проводки, независимо от аналитик книги учета, установите для параметра **Суммирование клиента** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="8bb74-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="8bb74-118">Чтобы сгруппировать только проводки с аналогичными аналитиками книги учета, установите для этого параметра значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="8bb74-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="8bb74-119">Выберите **Включить клиентов с невыполненными дебетовыми проводками** для выбора клиентов с несопоставленными суммами по дебету.</span><span class="sxs-lookup"><span data-stu-id="8bb74-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="8bb74-120">Для возмещения определенных счетов клиентов на экспресс-вкладке **Включаемые записи** выберите **Фильтр**, а затем укажите в запросе счета клиентов.</span><span class="sxs-lookup"><span data-stu-id="8bb74-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="8bb74-121">Кредитовые суммы переводятся на счета поставщиков клиентов и обрабатываются как стандартные платежи.</span><span class="sxs-lookup"><span data-stu-id="8bb74-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="8bb74-122">Если у клиента нет счета поставщика, автоматически создается одноразовый счет поставщика для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="8bb74-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="8bb74-123">Для просмотра созданных проводок возмещения используйте отчет **Возмещение** (**Расчеты с клиентами \> Запросы и отчеты \> Отчет о возмещении**).</span><span class="sxs-lookup"><span data-stu-id="8bb74-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="8bb74-124">В модуле "Расчеты с поставщиками" создайте платеж для накладных поставщика, которые были созданы в процессе возмещения.</span><span class="sxs-lookup"><span data-stu-id="8bb74-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="8bb74-125">Сведения о том, как заплатить поставщикам, см. в разделе [Обзор платежей поставщикам](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="8bb74-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
