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
ms.openlocfilehash: 711e2f445e043dc74cba0ee11f1ab2dc22215ff30f495e06dce1f6f3ab4a0a09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723807"
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