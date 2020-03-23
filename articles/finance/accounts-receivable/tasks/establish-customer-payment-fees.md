---
title: Определение сборов по платежам для клиентов
description: Создайте сборы по платежам для платежей клиентов.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5b94578e077834ce73c921dca18ad6e38c37659
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179634"
---
# <a name="establish-customer-payment-fees"></a>Определение сборов по платежам для клиентов

[!include [task guide banner](../../includes/task-guide-banner.md)]

Создайте сборы по платежам для платежей клиентов.

В этой задаче используется демонстрационная компания USMF.

1. В **области переходов** выберите **Модули > Расчеты с клиентами > Настройка платежей > Сбор по платежу**.
2. Нажмите кнопку **Создать**.
3. В поле **Код сбора** введите код сбора. Код сбора отображается в журналах платежей, поэтому присвойте ему описательное имя, чтобы пользователи понимали, какой сбор оценивается.  
4. В поле **Имя** введите имя сбора.
5. В поле **Описание сборов** введите описание сбора.
6. В поле **Начислять** выберите, будет ли сбор сниматься со счета клиента или счета ГК. Если сбор оценивается для клиента, выберите "Клиент". Если сбор оценивается в организации как расход, выберите "Главная книга". Для выполнения этой задачи выберите "Клиент".  
7. В поле **Тип журнала** выберите тип журнала, который может использовать этот сбор по платежам. Если эти сборы используются для платежей клиентов, типом журнала, скорее всего, будет "Клиентский платеж".  
8. Нажмите кнопку **Сохранить**.
9. Щелкните **Настройка сборов по платежам**. Настройка сборов по платежам используется для определения критериев времени оценки сборов по платежам.  Например, можно указать, что сбор будет рассчитываться, если используется банковский счет USMF OPER и способом оплаты является чек.  
10. В поле **Группировки** выберите значение "Таблица", "Группа" или "Все", чтобы определить, какие банковские счета будут оцениваться для этого сбора. Если выбрать значение "Все", все банковские счета могут быть оценены для этого сбора.  Если выбрать значение "Таблица", только выбранный банковский счет может быть оценен для этого сбора. Если выбрать значение "Группа", только банковские счета в выбранной банковской группе могут быть оценены для этого сбора.  
11. В поле **Связь с банком** выберите либо банковскую группу, либо банковский счет. Если выбрать значение "Таблица", в результатах поиска отобразятся банковские счета. Если выбрать значение "Группа", в результатах поиска отобразятся банковские группы.  
12. В списке перейдите по ссылке в выбранной строке.
13. В поле **Способ оплаты** выберите способ оплаты, для которого будет оценен этот сбор. Например, можно оценить сбор для клиентов, если они отправляют платежи в виде чека, а не электронного платежа.  
14. В списке найдите и выберите требуемую запись.
15. Если требуется, в поле **Валюта оплаты** введите валюту платежа. Валюта платежа используется в качестве дополнительных критериев для указания того, будет ли оцениваться сбор.  Например, ваш банк может взимать дополнительный сбор для платежей, получаемых в долларах США, поскольку обычно операции в банке выполняются только в евро.  
16. Выберите значение сбора: процент, сумма или интервал.
17. В поле **Процент/сумма** введите процент или сумму сбора. Если в поле "Процент/Сумма" выбрано значение "Процент", то вводимое здесь значение будет процентом. Если в поле "Процент/Сумма" выбрано значение "Сумма", то вводимое здесь значение будет суммой. Если в поле "Процент/Сумма" выбрано значение "Интервал", используйте вкладку "Интервал" для определения уровней.  
18. В поле **Валюта сбора** выберите валюту сбора. Это валюта, в которой будут создаваться сборы.  
19. Нажмите кнопку **Сохранить**.
