---
title: Начисление за покупку с нулевой суммой разносится для поступления продукта с нулевым значением
description: При разноске поступления продуктов с нулевым значением система создает разноску на начисление покупок, если сумма равна 0 (нулю).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026863"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="c7eb0-103">Начисление за покупку с нулевой суммой разносится для поступления продукта с нулевым значением</span><span class="sxs-lookup"><span data-stu-id="c7eb0-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="c7eb0-104">Номер статьи базы знаний: 4612588</span><span class="sxs-lookup"><span data-stu-id="c7eb0-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="c7eb0-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="c7eb0-105">Symptoms</span></span>

<span data-ttu-id="c7eb0-106">При разноске поступления продуктов с нулевым значением система создает разноску на начисление покупок, если сумма равна 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="c7eb0-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="c7eb0-107">Resolution</span></span>

<span data-ttu-id="c7eb0-108">По умолчанию для разноски ГК типа *Покупка, начисление* в поле `IsTransferredIndetail` всегда задано *Сводка* в проводках субкниги.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="c7eb0-109">Таким образом, система создает запись связанного ваучера, даже если сумма равна 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="c7eb0-110">Чтобы пропустить этот тип разноски, если сумма равна 0 (нулю), расширьте метод `subledgerJournalizer.markDoNotTransferEntries` так, чтобы он включал `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
