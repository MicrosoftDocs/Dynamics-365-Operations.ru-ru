---
title: Сопоставление датированного будущим числом чека от клиента
description: Можно сопоставить чек, датированный задним числом, после того как банком был выполнен клиринг чека.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635a1c50390bca59cd1c9ba0cf0421c510b2998c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179602"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Сопоставление датированного будущим числом чека от клиента

[!include [task guide banner](../../includes/task-guide-banner.md)]

Можно сопоставить чек, датированный задним числом, после того как банком был выполнен клиринг чека. Эта финансовая проводка также приведет к очистке проводки на промежуточный счет для чека, датированного задним числом. 

Перед тем как начинать эту задачу, необходимо выполнить следующие задачи.

1) Настройка датированных будущим числом чеков

2) Регистрация и разноска датированного будущим числом чека для клиента 



Роль для выполнения этого руководства по задачам — казначей.



В данной процедуре используется демонстрационная компания USMF.

1. Перейдите в раздел "Кредит и коллекции" > "Запросы и отчеты" > "Платежи" > "Чеки клиента, датированные будущим числом".
2. Щелкните "Сопоставление".
3. Щелкните "Сопоставление записей клиринга".
    * Сопоставьте счет клиента для проводки чека.  
4. Закройте страницу.
5. Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".
6. В поле "Показать" выберите один из вариантов.
7. Установите или снимите флажок "Показать только созданное пользователем".
8. В списке найдите и выберите требуемую запись.
9. Выберите Строки.
10. Щелкните "Операция".
11. Закройте страницу.
