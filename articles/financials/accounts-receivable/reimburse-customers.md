---
title: "Зачет клиентов"
description: "В этом статье описан порядок создания проводок возмещения для группы клиентов. Если клиент имеет кредитовое сальдо, можно возместить клиенту сумму сальдо."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2d1a05ffe39c208748a316bd711d9442f1ed875a
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="reimburse-customers"></a><span data-ttu-id="c768c-104">Зачет клиентов</span><span class="sxs-lookup"><span data-stu-id="c768c-104">Reimburse customers</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c768c-105">В этом статье описан порядок создания проводок возмещения для группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="c768c-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="c768c-106">Если клиент имеет кредитовое сальдо, можно возместить клиенту сумму сальдо.</span><span class="sxs-lookup"><span data-stu-id="c768c-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="c768c-107">В следующей таблице показаны обязательные компоненты, которые должны быть подготовлены до начала работы.</span><span class="sxs-lookup"><span data-stu-id="c768c-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="c768c-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="c768c-108">Prerequisite</span></span>                                                            | <span data-ttu-id="c768c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c768c-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c768c-110">Укажите минимальную сумму возмещения для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="c768c-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="c768c-111">На странице **Параметры расчетов с клиентами** в области **Общее** в поле **Минимальный зачет** введите минимальную сумму, которую можно возместить по переплатам клиента.</span><span class="sxs-lookup"><span data-stu-id="c768c-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="c768c-112">(Необязательно) Добавьте счет поставщика к каждому клиенту, который может получать возмещение.</span><span class="sxs-lookup"><span data-stu-id="c768c-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="c768c-113">На странице **Клиенты** на экспресс-вкладке **Прочие подробные сведения** в поле **Счет поставщика** выберите счет поставщика для клиента.</span><span class="sxs-lookup"><span data-stu-id="c768c-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="c768c-114">При создании проводок возмещения создается накладная поставщика на сумму кредитового сальдо.</span><span class="sxs-lookup"><span data-stu-id="c768c-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="c768c-115">В процессе возмещения удаляется кредитового сальдо со счета клиента и создаются суммы задолженности для счета поставщика, который соответствует клиенту.</span><span class="sxs-lookup"><span data-stu-id="c768c-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="c768c-116">В модуле "Расчеты с клиентами" выполните процесс **Возмещение**.</span><span class="sxs-lookup"><span data-stu-id="c768c-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="c768c-117">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c768c-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="c768c-118">Чтобы возвратить сумму на счета конкретного клиента, щелкните **Выбрать** и укажите счета клиента в запросе.</span><span class="sxs-lookup"><span data-stu-id="c768c-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="c768c-119">Для возврата средств на счета всех клиентов нажмите **OK**.</span><span class="sxs-lookup"><span data-stu-id="c768c-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="c768c-120">Кредитовые суммы переводятся на счета поставщиков клиентов и обрабатываются как стандартные платежи.</span><span class="sxs-lookup"><span data-stu-id="c768c-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="c768c-121">Если у клиента нет счета поставщика, автоматически создается одноразовый счет поставщика для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="c768c-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="c768c-122">Просмотреть созданные проводки возмещения можно на странице **Возмещение**.</span><span class="sxs-lookup"><span data-stu-id="c768c-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="c768c-123">В модуле "Расчеты с поставщиками" создайте платеж для накладных поставщика, которые были созданы в процессе возмещения.</span><span class="sxs-lookup"><span data-stu-id="c768c-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





