---
title: Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550771"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)

[!include [task guide banner](../../includes/task-guide-banner.md)]

В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных. Эти шаги можно выполнить в любой компании.

Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)".

Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Настройка этого отчета для использования сведений об инвентаризации и суммировании
1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
2. Щелкните "Конфигурации отчетности".
3. В дереве разверните узел "Модель Интрастат".
4. В дереве разверните узел "Модель Интрастат\Интрастат (DE)".
5. В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".
6. Выберите Конструктор.
7. Перейдите на вкладку "Сопоставление".
8. Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.
    * Добавьте новый источник данных для получения списка запомненных блоков.  
9. В дереве выберите "Функции\Вычисляемое поле".
10. В поле "Имя" введите "$BlocksList".
    * $BlocksList  
11. Щелкните "Изменить формулу".
12. В дереве выберите "Функции сбора данных\COLLECTEDLIST".
13. Щелкните "Добавить функцию".
14. Щелкните "Добавить источник данных".
15. В поле "Формула" введите "COLLECTEDLIST('$BlockName', ".
    * COLLECTEDLIST('$BlockName',  
16. В поле "Формула" введите "COLLECTEDLIST('$BlockName', "*")".
    * COLLECTEDLIST('$BlockName', "*")  
17. Нажмите кнопку "Сохранить".
    * Шаблон "*" означает, что все блоки будут включены в список для этой записи.  
18. Закройте страницу.
19. Нажмите кнопку "OК".
20. Перейдите на вкладку "Формат".
21. В дереве выберите "Интрастат\Данные".
22. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
23. В дереве выберите "Текст\Последовательность".
24. В поле "Имя" введите "Итого по блокам".
    * Итого по блокам  
25. В поле "Специальные знаки", выберите "Создать строку — Windows (CR LF)".
26. Нажмите кнопку OK.
27. В дереве выберите узел "Интрастат\Данные\Итого по блокам".
28. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
29. В дереве выберите "Текст\строка".
30. В поле "Имя" введите "Код блока".
    * Код блока  
31. Нажмите кнопку "OК".
32. Щелкните "Добавить строку".
33. В поле "Имя" введите "Инвентаризация строк".
    * Инвентаризация строк  
34. Нажмите кнопку "OК".
35. Щелкните "Добавить строку".
36. В поле "Имя" введите "Итоговая сумма".
    * Итоговая сумма  
37. Нажмите кнопку "OК".
38. Перейдите на вкладку "Сопоставление".
39. В дереве выберите "$BlocksList".
40. Щелкните "Связать".
    * Создайте сводную строка для каждого запомненного блока.  
41. Перейдите на вкладку "Формат".
42. В дереве выберите узел "Интрастат\Данные\Итого по блокам\Код блока".
43. Перейдите на вкладку "Сопоставление".
44. Щелкните "Изменить формулу".
45. В поле "Формула" введите «"Код блока: " & ».
    * "Код блока: " &  
46. В дереве разверните узел "$BlocksList".
47. В дереве выберите "$BlocksList\Значение".
48. Щелкните "Добавить источник данных".
49. Нажмите кнопку "Сохранить".
50. Закройте страницу.
51. Перейдите на вкладку "Формат".
52. В дереве выберите узел "Интрастат\Данные\Итого по блокам\Инвентаризация строк".
53. Перейдите на вкладку "Сопоставление".
54. Щелкните "Изменить формулу".
    * Создайте выходные данные для числа строк для каждого блока, представленного в этом отчете.  
55. В поле "Формула", введите «"Число строк в этом блоке: " & ».
    * "Число строк в этом блоке: " &  
56. В поле "Формула", введите «"Число строк в этом блоке: " & TEXT(».
    * "Число строк в этом блоке: " & TEXT(  
57. В дереве выберите "Функции сбора данных\COUNTIFS".
58. Щелкните "Добавить функцию".
59. Щелкните "Добавить источник данных".
60. В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', ».
    * "Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName',  
61. В дереве разверните узел "$BlocksList".
62. В дереве выберите "$BlocksList\Значение".
63. Щелкните "Добавить источник данных".
64. В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ».
    * "Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. В дереве выберите "$RecName".
66. Щелкните "Добавить источник данных".
67. В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))».
    * "Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Нажмите кнопку "Сохранить".
69. Закройте страницу.
70. Перейдите на вкладку "Формат".
71. В дереве выберите узел "Интрастат\Данные\Итого по блокам\Итоговая сумма".
72. Перейдите на вкладку "Сопоставление".
73. Щелкните "Изменить формулу".
    * Создайте выходные данные, которые будут итоговой суммой по выставленным накладным для каждого блока, представленного в этом отчете.  
74. В поле "Формула" введите «"Итого по выставленным накладным: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))».
    * "Итого по выставленным накладным: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Нажмите кнопку "Сохранить".
76. Закройте страницу.
77. Нажмите кнопку "Сохранить".
78. Закройте страницу.
