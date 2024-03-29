---
title: Закрытие финансового года
description: В этой процедуре описывается процесс закрытия на конец конца, который переносит сальдо в новый финансовый год.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779821"
---
# <a name="close-the-fiscal-year"></a>Закрытие финансового года

[!include [banner](../../includes/banner.md)]

В этой процедуре описывается процесс закрытия на конец конца, который переносит сальдо в новый финансовый год.


## <a name="validate-year-end-close-parameters"></a>Проверьте параметры закрытия на конец года
1. Выберите **Область переходов > Модули > Главная книга > Настройка главной книги > Параметры главной книги**.
2. Разверните раздел **Закрытие финансового года**.
3. Выберите **Да** или **Нет** для параметра **Удаление закрывающих проводок при переносе**.
    
Если финансового года уже был закрыт и закрытие на конец года выполняется повторно, эта настройка важна. Если задано значение **Да**, ваучер для предыдущего закрытия конца года будет удален, и новый ваучер будет создан для всех начальных сальдо счетов. Если задано значение **Нет**, предыдущий ваучер сохраняется, и новый ваучер создается только для корректирующих записей, которые были разнесены после последнего закрытия на конец года.

4. Выберите **Да** или **Нет** для параметра **Создать закрывающие проводки при переносе**.

Если задано значение **Да**, создаются две проводки. Один ваучер создается в закрываемом финансовом году, чтобы привести сальдо всех счетов ГК к нулевому значению, а другой ваучер создается в следующем финансовом году для начальных сальдо. Если задано значение **Нет**, создается один ваучер в следующем финансовом году для начальных сальдо.  

5. Выберите **Да** или **Нет** для параметра **Задать для финансового года статус закрытого на постоянной основе**.

Если задано значение **Да**, статус финансового года будет установлен на **Закрыт на постоянной основе**. Поскольку постоянно закрытый год не может быть повторно открыт, рекомендуется установить для этого параметра значение **Нет**.  

6. Выберите **Да** или **Нет** для параметра **Код ваучера должен быть заполнен во время закрытия на конец года**.

Если задано значение **Да**, код ваучера необходимо вручную ввести во время процесса закрытия на конец года. Номерная серия не используется для создания этого кода ваучера. Рекомендуется установить для этого параметра значение **Да**.  

7. Закройте страницу.
8. Перейдите в раздел **Главная книга > Закрытие периода > Закрытие на конец года**.
9. Нажмите **Создать** для создания шаблона закрытия на конец года.

Шаблон может быть создан для группы юридических лиц, для которых требуется выполнить закрытие на конец года. Этот шаблон можно повторно использовать каждый год.  

10. В поле **Имя группы** введите имя шаблона закрытия на конец года.
11. В поле **Финансовый календарь** выберите финансовый год, для которого будет создан шаблон.

Только юридические лица, использующие один и тот же финансовый год, можно сгруппировать вместе в шаблоне закрытия на конец года. Это необходимо, поскольку закрытие на конец года производится путем выбора финансового года, а не даты.  

12. В области **Панель операций** щелкните **Сохранить**.
13. В разделе **Юридические лица** щелкните **Добавить**, чтобы выбрать юридические лица для этого шаблона.
    
Юридические лица можно добавлять, выбирая юридические лица или выбирая организационную иерархию. Будут добавлены только юридические лица с организационной иерархией с одинаковым выбранным финансовым календарем.  

14. Выберите юридические лица или организационную иерархию.
15. Щелкните **OK**.
16. Выберите **Да** или **Нет** в параметре **Переместить аналитики балансового отчета**.

Рекомендуется задать для этого параметра значение **Да** для балансовых счетов. Это позволит сохранить финансовые аналитики в разнесенных проводках при создании начальных сальдо для балансовых счетов. Для счетов прибылей и убытков можно выбрать сохранение финансовых аналитик (**Закрыть все**), когда сальдо переносятся в нераспределенную прибыль, или можно выбрать, чтобы заменить финансовые аналитики на другое значение аналитики (**Закрыть один**). При выборе значения **Закрыть один** можно указать конкретное значение аналитики для каждой аналитики или даже оставить его пустым.  

17. Нажмите кнопку **Сохранить**.
18. Запустите закрытие на конец года, выбрав **Выполнить финансовое закрытие** в области **Панель операций**. Закрытие на конец года выполняется для выбранного шаблона.  
19. Выберите все или подмножество юридических лиц из шаблона, для которых требуется выполнить закрытие на конец года.

При первом выполнении закрытия на конец года для получения начальных сальдо большинство организаций могут выбрать выполнение закрытия на конец года для всех юридических лиц в шаблоне. Если записи корректировки выполняются после этого, можно выбрать выполнение закрытия на конец года только для юридических лиц, для которых имеются корректировки.  

20. Щелкните **OK**.
21. Выберите финансовый год, для которого требуется выполнить закрытие на конец года.
22. В поле **Ваучер** введите значение. Рекомендуется включать финансовый год в код ваучера, чтобы упростить поиск созданного ваучера закрытия на конец года.  
23. Закрытие на конец года по умолчанию выполняется в пакетном режиме. Рекомендуется выполнять длительные процессы в пакетном режиме. Обычно это один из таких процессов, поэтому по умолчанию задано использование пакетного режима.  
24. Щелкните **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
