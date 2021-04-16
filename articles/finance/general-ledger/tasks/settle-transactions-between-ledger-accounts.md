---
title: Сопоставление проводок между счетами ГК
description: Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2594b90ed58a1e7f12c8a94d3c48266faef557f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817061"
---
# <a name="settle-transactions-between-ledger-accounts"></a>Сопоставление проводок между счетами ГК

[!include [banner](../../includes/banner.md)]

Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК. В этой процедуре используется компания с демонстрационными данными USMF.


## <a name="settle-transaction-between-ledger-accounts"></a>Сопоставление проводки между счетами ГК
1. Перейдите в раздел "Главная книга" > "Периодические задачи" > "Сопоставления ГК".
2. В списке найдите проводку, которую требуется сопоставить.
   > [!NOTE]
   > Сальдо должно быть равно нулю.  
3. Щелкните "Включить".
4. Щелкните "Принять".

## <a name="cancel-a-ledger-settlement"></a>Отмена сопоставления операций

1. Перейдите в раздел "Главная книга" > "Запросы и отчеты" > "Пробный баланс".
2. Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.
3. Щелкните Обновить.
4. В списке найдите счет, в котором есть сопоставленные проводки.
5. Щелкните "Все проводки".
6. Используйте фильтр для упрощения поиска проводки в списке.
7. Щелкните "Сопоставления ГК".
8. В списке пометьте выбранную строку.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]