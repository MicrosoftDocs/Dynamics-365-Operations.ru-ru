---
title: Учет периодических журналов
description: Периодические журналы иногда называются повторяющимися журналами, поскольку сумма, текст и другие сведения повторяются при каждом извлечении периодического журнала.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dacf7f21d147b780d57b0e7a61b11d78d30fa52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834429"
---
# <a name="post-periodic-journals"></a>Учет периодических журналов

[!include [banner](../../includes/banner.md)]

Периодические журналы иногда называются повторяющимися журналами, поскольку сумма, текст и другие сведения повторяются при каждом извлечении периодического журнала. При создании периодического журнала следует указать интервал периода повторения, например в днях или месяцах. В этом руководстве по задаче будет создан периодический журнал с ежемесячным повторением.

1. Перейдите в раздел **Область переходов > Модули > Главная книга > Периодические задачи > Периодические журналы**.
2. Нажмите кнопку **Создать**.
3. В поле **Имя** введите или выберите значение.
4. В списке перейдите по ссылке в выбранной строке.
5. В поле **Описание** введите значение. Описанием будет имя периодического журнала при дальнейшем извлечении, поэтому присвойте ему соответствующее имя.
6. В **Панели операций** щелкните **Строки**. Периодический журнал обычно включает несколько строк журнала. Однако в этом руководстве по задаче будет добавлена только одна строка.
7. В поле **Дата** введите дату. В поле **Дата** указана дата разноски для следующего перемещения в ежедневный журнал. В случае журналов, которые будут извлекаться каждый месяц, рекомендуется использовать дату в месяце его разноски, обычно это первая или последняя дата в периоде. Можно оставить поле даты пустым и указать дату при извлечении журнала с помощью поля "Пустая дата". Поле автоматически обновляется для отображения следующей повторяющейся даты извлечения проводок. 
8. В поле **Счет** укажите требуемые значения.
9. В поле **Описание** введите или выберите значение.
10. Закройте страницу.
11. В поле **Дебет** введите число.
12. В поле **Корр.счет** укажите требуемые значения.
13. В поле **Единица измерения** выберите "Месяцы".
14. В поле **Число единиц** введите значение "1".
15. В поле **Последняя дата** введите дату. Ввод последней даты в предыдущем периоде поможет предотвратить создание повторяющегося журнала по ошибке в неправильном начальном периоде. Последняя дата в дальнейшем будет обновляться при каждом извлечении периодического журнала. 
16. Нажмите кнопку **Сохранить**.
17. Выберите **Область переходов > Модули > Главная книга > Записи журнала > Общие журналы**.
18. Нажмите кнопку **Создать**.
19. В поле **Имя** введите или выберите значение.
20. В списке найдите и выберите требуемую запись.
21. В списке перейдите по ссылке в выбранной строке.
22. В поле **Описание** введите значение.
23. В **Панели операций** щелкните **Строки**.
24. На **панели операций** щелкните **Периодический журнал**.
25. Щелкните **Восстановить журнал**.
26. В поле **Дата окончания** введите дату. **Дата окончания** служит в качестве даты прекращения для строк периодического ваучера. На основании настройки повторения, последней даты и даты окончания одна и та же строка может быть включена в итоговый журнал несколько раз. Дата окончания автоматически обновляется на основании даты сеанса последнего переноса периодической строки в журнал. 
27. В поле **Номер периодического журнала** введите или выберите значение.
28. В списке перейдите по ссылке в выбранной строке.
29. Щелкните **OK**. Периодический журнал теперь можно извлечь, утвердить или разнести в зависимости от требований и настройки.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]