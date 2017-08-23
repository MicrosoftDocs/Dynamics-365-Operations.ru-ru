--- 
title: "Разработка конфигурации для создания отчетов в формате Microsoft Word для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить форматы электронной отчетности (ER) для создания отчетов как файлов Microsoft Word."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5adf1d6e6314ac7ea4084cfb3fcde8b83168c7ae
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a>Разработка конфигурации для создания отчетов в формате Microsoft Word для электронной отчетности (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить форматы электронной отчетности (ER) для создания отчетов как файлов Microsoft Word. Эти шаги можно выполнить в компании GBSI.

Для выполнения этих шагов необходимо сначала выполнить шаги в руководстве по задаче "Создание конфигурации электронной отчетности для создания отчетов в формате OPENXML". Необходимо заранее загрузить и сохранить локально для следующие шаблоны для примера отчета:

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx

Эта процедура предназначена для функции, которая была добавлена в версии 1611 Microsoft Dynamics 365 for Operations.


## <a name="select-the-existing-er-report-configuration"></a>Выбор существующей конфигурации отчета электронной отчетности
1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
    * Убедитесь, что поставщик конфигураций Litware, Inc. выбран как активный.  
2. Щелкните "Конфигурации отчетности".
    * Мы повторно используем существующую конфигурацию ER, которая изначально была создана для создания выходных данных отчета в формате OPENXML.  
3. В дереве разверните узел "Модель платежа".
4. В дереве выберите "Модель платежа\Пример отчета о листе".
5. Выберите Конструктор.

## <a name="replace-the-excel-template-with-the-word-template"></a>Замена шаблона Excel на шаблон Word
    * В настоящее время документ Excel используется как шаблон для создания выходных данных в формате OPENXML. Мы импортируем шаблон отчета в формате Word.  
1. Нажмите кнопку Вложения.
    * Замените существующий шаблон Excel на ранее загруженный шаблон Word — SampleVendPaymDocReport.docx. Обратите внимание, что этот шаблон содержит только макет документа, который требуется создать как выходные данные ER.  
2. Нажмите кнопку Удалить.
3. Щелкните Да.
4. Щелкните "Создать".
5. Щелкните "Файл".
6. Щелкните Обзор. Найдите и выберите ранее загруженный шаблон SampleVendPaymDocReport.docx. Нажмите кнопку "OК".
    * Выберите шаблон, загруженный на предыдущем шаге.  
7. В поле "Шаблон" введите или выберите значение.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Расширение шаблона Word путем добавления пользовательской XML-части
1. Нажмите кнопку "Сохранить".
    * В дополнение к сохранению изменений конфигурации действие "Сохранить" также обновит присоединенный шаблон Word. Структура созданного формата передается в документ Word в качестве новой пользовательской XML-части с именем "Отчет". Обратите внимание, что присоединенный шаблон Word содержит не только макет документа, который требуется создать как выходные данные ER, но он также содержит структуру данных, которую ER заполнит в этот шаблон во время выполнения.  
2. Нажмите кнопку Вложения.
    * Теперь необходимо привязать элементы пользовательской XML-части "Отчет" к частям документа Word.  
    * Если вы знакомы с документами Word, которые можно создать как формы, содержащие элементы управления содержимым, связанные с элементами пользовательских XML-частей, воспроизведите все шаги следующей подзадачи для создания такого документа. Дополнительные сведения см. по следующей ссылке: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. В противном случае пропустите все действия, указанные в следующей подзадаче.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Получение Word с пользовательской XML-частью для привязки данных
    * Откройте этот документ в Word и выполните следующие действия:  - Откройте вкладку "Разработчик Word" (настройте ленту, если она еще не включена).  - Выберите область сопоставления XML.  - Выберите пользовательскую XML-часть "Отчет" в поиске.  - Выполните сопоставление элементов выбранной пользовательской XML-части и элементов управления содержимым документа Word.  - Сохраните обновленный документ Word на локальном диске.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Отправка шаблона Word с пользовательской XML-частью, связанной с элементами управления содержимым
1. Нажмите кнопку Удалить.
2. Щелкните Да.
    * Добавление нового шаблона. Если вы выполнили действия, описанные в предыдущей подзадаче, выберите документ Word, который был подготовлен и сохранен локально. В противном случае выберите ранее загруженный шаблон SampleVendPaymDocReportBounded.docx MS Word.  
3. Щелкните "Создать".
4. Щелкните "Файл".
5. Щелкните Обзор. Найдите и выберите ранее загруженный шаблон SampleVendPaymDocReportBounded.docx. Нажмите кнопку OK.
6. В поле "Шаблон" выберите документ, загруженный на предыдущем шаге.
7. Нажмите кнопку "Сохранить".
8. Закройте страницу.

## <a name="execute-the-format-to-create-word-output"></a>Выполнение формата для создания выходных данных Word
1. В области действий щелкните "Конфигурации".
2. Щелкните "Параметры пользователя".
3. Выберите "Да" в поле "Запустить настройки".
4. Нажмите кнопку "OК".
5. Щелкните "Изменить".
6. Выберите "Да" в поле "Запустить черновик".
7. Нажмите кнопку "Сохранить".
8. Закройте страницу.
9. Закройте страницу.
10. Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".
11. Щелкните "Строки".
12. В списке отметьте все строки или отмените отметку всех строк.
13. Щелкните "Статус платежа".
14. Щелкните "Нет".
15. Щелкните "Создать платежи".
16. Нажмите кнопку "OК".
17. Нажмите кнопку "OК".
    * Проанализируйте созданные выходные данные. Обратите внимание, что созданные выходные данные представлены в формате Word и содержат сведения об обработанных платежах.  

