---
title: Разработка выражений электронной отчетности для вызова методов классов приложений
description: В этом руководстве описывается повторное использование существующей логики в конфигурациях электронной отчетности (ER) путем вызова требуемых методов классов приложения в выражениях ER.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f61228d328521d0c6fe8e0ae704001a65d03151f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249235"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Разработка выражений электронной отчетности для вызова методов классов приложений

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этом руководстве описывается повторное использование существующей логики в конфигурациях электронной отчетности (ER) путем вызова требуемых методов классов приложения в выражениях ER. Значения аргументов для вызова классов могут определяться динамически во время выполнения: например, на основе информации в документе анализа для гарантии ее правильности. В этом проводнике вам предстоит создать необходимые конфигурации ER для демонстрационной компании Litware, Inc. Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности". 

Эти шаги можно выполнить с использованием любого набора данных. Необходимо также загрузить и сохранить следующий файл на локальном компьютере: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Электронная отчетность — создание поставщика конфигурации и пометка его как активного".

1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
    * Убедитесь, что поставщик конфигурации для примера компании Litware, Inc. доступен и помечен как активный. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Электронная отчетность — создание поставщика конфигурации и пометка его как активного".   
    * Разрабатывается процесс для анализа входящих банковских выписок для обновления данных приложения. Вы будете получать входящие банковские выписки как TXT-файлы, содержащие коды IBAN. В рамках процесса импорта банковской выписки необходимо проверить правильность этих кодов IBAN с помощью логики, которая уже доступна.   

## <a name="import-a-new-er-model-configuration"></a>Импорт новой конфигурации модели ER
1. В списке найдите и выберите требуемую запись.
    * Выберите плитку поставщика Майкрософт.  
2. Щелкните "Репозитории".
3. Щелкните "Показать фильтры".
4. Добавьте поле фильтра "Имя типа". В поле "Имя" введите значение "ресурсы", выберите оператор фильтра "содержит" и нажмите кнопку "Применить".
5. Щелкните Открыть.
6. В дереве выберите "Модель платежа".
    * Если кнопка "Импорт" на экспресс-вкладке "Версии" не включена, вы уже импортировали версию 1 конфигурации ER "Модель платежа". Остальные шаги в этой подзадаче можно пропустить.   
7. Нажмите кнопку Импорт.
8. Щелкните Да.
9. Закройте страницу.
10. Закройте страницу.

## <a name="add-a-new-er-format-configuration"></a>Добавление новой конфигурации формата электронной отчетности
1. Щелкните "Конфигурации отчетности".
    * Добавьте новый формат ER для анализа входящих банковских выписок в формате TXT.  
2. В дереве выберите "Модель платежа".
3. Щелкните "Создать конфигурацию", чтобы открыть диалоговое меню.
4. В поле "Создать" введите "Формат, основанный на модели данных PaymentModel".
5. В поле "Имя" введите "Формат импорта банковской выписки (образец)".
    * Формат импорта банковской выписки (образец)  
6. Выберите "Да" в поле "Поддерживает импорт данных".
7. Нажмите Создать конфигурацию.

## <a name="design-the-er-format-configuration---format"></a>Разработка конфигурации формата ER — формат
1. Выберите Конструктор.
    * Созданный формат представляет ожидаемую структуру внешнего файла в формате TXT.  
2. Щелкните "Добавить корень", чтобы открыть диалоговое меню.
3. В дереве выберите "Текст\Последовательность".
4. В поле "Имя" введите "Корень".
    * Корневой  
5. В поле "Специальные знаки", выберите "Создать строку — Windows (CR LF)".
    * В поле "Специальные знаки" выбран параметр "Создать строку — Windows (CR LF)". На основании этого параметра каждая строка в файле анализа рассматривается как отдельная запись.  
6. Нажмите кнопку "OК".
7. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
8. В дереве выберите "Текст\Последовательность".
9. Введите "Строки" в поле "Имя".
    * Строки  
10. В поле "Кратность" выберите "Один — много".
    * В поле "Кратность" выбран параметр "Один — много". На основании этого параметра ожидается, что по крайней мере одна строка будет представлена в файле анализа.  
11. Нажмите кнопку "OК".
12. В дереве выберите "Корень\Строки".
13. Нажмите кнопку "Добавить последовательность".
14. Введите "Поля" в поле "Имя".
    * Поля  
15. В поле "Кратность" выберите "Ровно один".
16. Нажмите кнопку "OК".
17. В дереве выберите "Корень\Строки\Поля".
18. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
19. В дереве выберите "Текст\строка".
20. В поле "Имя" введите "IBAN".
    * Номер IBAN  
21. Нажмите кнопку "OК".
    * Он был настроен для каждой строки в файле анализа, содержащей только код IBAN.  
22. Нажмите кнопку "Сохранить".

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Разработка конфигурации формата ER — сопоставление с моделью данных
1. Щелкните "Сопоставить формат модели".
2. Щелкните "Создать".
3. В поле "Определение" введите BankToCustomerDebitCreditNotificationInitiation.
    * BankToCustomerDebitCreditNotificationInitiation  
4. Разрешить изменения определения.
5. В поле "Имя" введите "Сопоставление с моделью данных".
    * Сопоставление с моделью данных  
6. Нажмите кнопку "Сохранить".
7. Выберите Конструктор.
8. В дереве выберите "Dynamics 365 for Operations\Класс".
9. Щелкните "Добавить корень".
    * Добавьте новый источник данных для вызова существующей логики приложения для проверки кодов IBAN.  
10. В поле "Имя" введите check_codes.
    * проверка кода  
11. В поле "Класс" введите ISO7064.
    * ISO7064  
12. Нажмите кнопку "OК".
13. В дереве разверните "формат".
14. В дереве разверните "формат\Корень: Последовательность(корень)".
15. В дереве выберите "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)".
16. Щелкните "Связать".
17. В дереве разверните "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)".
18. В дереве разверните "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)\Поля: последовательность 1..1 (поля)".
19. В дереве выберите "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)\Поля: последовательность 1..1 (поля)\IBAN: строка(IBAN)".
20. В дереве разверните "Платежи = format.Root.Rows".
21. В дереве разверните "Платежи = format.Root.Rows\Счет кредитора(счет кредитора)".
22. В дереве разверните "Платежи = format.Root.Rows\Счет кредитора(счет кредитора)\Идентификация".
23. В дереве выберите "Платежи = format.Root.Rows\Счет кредитора(счет кредитора)\Идентификация\IBAN".
24. Щелкните "Связать".
25. Перейдите на вкладку "Проверки".
26. Щелкните "Создать".
    * Добавьте новое правило проверки, которое отображает ошибку для любой строки в файле анализа, которая содержит недопустимый код IBAN.  
27. Щелкните "Изменить условие".
28. В дереве разверните check_codes.
29. В дереве выберите "check_codes\verifyMOD1271_36".
30. Щелкните "Добавить источник данных".
31. В поле "Формула" введите check_codes.verifyMOD1271_36(.
    * check_codes.verifyMOD1271_36(  
32. В дереве разверните "формат".
33. В дереве разверните "формат\Корень: Последовательность(корень)".
34. В дереве разверните "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)".
35. В дереве разверните "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)\Поля: последовательность 1..1 (поля)".
36. В дереве выберите "формат\Корень: Последовательность(корень)\Строки: последовательность 1.. * (строки)\Поля: последовательность 1..1 (поля)\IBAN: строка(IBAN)".
37. Щелкните "Добавить источник данных".
38. В поле "Формула" введите check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN).
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Нажмите кнопку "Сохранить".
40. Закройте страницу.
    * Условие проверки настроено для возврата значения FALSE для любого недопустимого кода IBAN путем вызова существующего метода verifyMOD1271_36 класса приложения ISO7064. Обратите внимание, что значение кода IBAN определяется динамически во время выполнения в качестве аргумента метода вызова на основе содержимого TXT-файла анализа.   
41. Нажмите кнопку "Изменить сообщение".
42. В поле "Формула введите "CONCATENATE("Обнаружен недопустимый код IBAN:  ", format.Root.Rows.Fields.IBAN)".
    * CONCATENATE("Обнаружен недопустимый код IBAN:  ", format.Root.Rows.Fields.IBAN)  
43. Нажмите кнопку "Сохранить".
44. Закройте страницу.
45. Нажмите кнопку "Сохранить".
46. Закройте страницу.

## <a name="run-the-format-mapping"></a>Выполнение сопоставления формата
В целях тестирования выполните сопоставление формата с помощью загруженного файла SampleIncomingMessage.txt. Созданные выходные данные включают данные, импортируемые из выбранного TXT-файла и заполняющие модель пользовательских данных в реальном импорте.   
1. Щелкните "Выполнить".
    * Нажмите кнопку "Обзор" и перейдите к ранее загруженному файлу SampleIncomingMessage.txt.  
2. Нажмите кнопку "OК".
    * Просмотрите выходные данные в формате XML, представляющем данные, которые были импортированы из выбранного файла, а затем перенесены в модель данных. Обратите внимание, что были обработаны только 3 строки импортированного TXT-файла. Недопустимый код IBAN в строке 4 был пропущен, и отобразилось сообщение об ошибке в журнале Infolog.  
