---
title: Сопоставление датированного будущим числом чека для поставщика
description: Сопоставьте датированный будущим числом чек, выдаваемый поставщику, когда банк осуществляет клиринг проводки по чеку, после того как чек стал просроченным и был подвергнут клирингу в банке.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e3816a2f1c95d568a173cb07daad0473703da9c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779510"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Сопоставление датированного будущим числом чека для поставщика

[!include [banner](../../includes/banner.md)]

Сопоставьте датированный будущим числом чек, выдаваемый поставщику, когда банк осуществляет клиринг проводки по чеку, после того как чек стал просроченным и был подвергнут клирингу в банке. 

Перед тем как начинать эту процедуру, необходимо выполнить следующие процедуры.

1) Настройка датированных будущим числом чеков

2) Регистрация и разноска датированного будущим числом чека для поставщика



Роль для выполнения этой процедуры — казначей. В данной процедуре используется демонстрационная компания USMF.

1. Перейдите в раздел **Расчеты с поставщиками > Платежи > Чеки для поставщика, датированные будущим числом**.
2. Щелкните **Сопоставление**.
3. Щелкните **Сопоставление записей клиринга**.
    * Сопоставьте счет поставщика для проводки чека.  
4. Закройте страницу.
5. Перейдите в раздел **Главная книга > Записи в журнале > Общие журналы**.
6. В поле **Показать** выберите **Все**.
7. Установите или снимите флажок **Показать только созданное пользователем**.
8. В списке пометьте выбранную строку.
9. Выберите **Строки**.
10. Щелкните **Операция**.
11. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
