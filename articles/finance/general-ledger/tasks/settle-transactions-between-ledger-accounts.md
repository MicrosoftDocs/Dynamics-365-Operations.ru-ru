---
title: Сопоставление проводок между счетами ГК
description: Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222103"
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