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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Начисление за покупку с нулевой суммой разносится для поступления продукта с нулевым значением

Номер статьи базы знаний: 4612588

## <a name="symptoms"></a>Симптомы

При разноске поступления продуктов с нулевым значением система создает разноску на начисление покупок, если сумма равна 0 (нулю).

## <a name="resolution"></a>Приказ

По умолчанию для разноски ГК типа *Покупка, начисление* в поле `IsTransferredIndetail` всегда задано *Сводка* в проводках субкниги. Таким образом, система создает запись связанного ваучера, даже если сумма равна 0 (нулю).

Чтобы пропустить этот тип разноски, если сумма равна 0 (нулю), расширьте метод `subledgerJournalizer.markDoNotTransferEntries` так, чтобы он включал `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, как показано в следующем примере.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
