---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3 — Создание формата)
description: В этой статье описывается, как настроить формат электронной отчетности, чтобы использовать файлы управления документами в выходных данных электронной отчетности. (Часть 3)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: b70f5ed74fd701be79daebbd2a8f246a0a0ab95e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290945"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3 — Создание формата)

[!include [banner](../../includes/banner.md)]

В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности. Эти шаги можно выполнить в любой компании.

Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)".

Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="create-a-format-to-process-invoices"></a>Создание формата для обработки накладных
1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
2. Щелкните "Конфигурации отчетности".
3. В дереве разверните "Модель накладной клиента".
4. В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".
    * Вы создадите формат для создания электронных сообщений со сведениями о любых файлах, которые были приложены к заказу на продажу, который связан электронной обработкой накладной.  
5. Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.
6. В поле "Создать" введите "Формат, основанный на модели данных Модель накладной клиента (настраиваемая)".
7. В поле "Имя" введите "Пример сообщения электронной накладной".
    * Пример сообщения электронной накладной  
8. В поле "Определение модели данных" введите или выберите значение.
    * InvoiceCustomer  
9. Нажмите Создать конфигурацию.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Разработка формата для заполнения вложений при создании сообщения в формате MIME
1. Выберите Конструктор.
2. Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.
3. В дереве выберите "XML\Элемент".
4. В поле "Имя" введите "Накладная".
    * Счет-фактура  
5. Нажмите кнопку "OК".
6. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
7. В дереве выберите "'XML\Атрибут".
8. В поле "Имя" введите "SalesOrder".
    * SalesOrder  
9. Нажмите кнопку "OК".
10. Щелкните "Добавить атрибут".
11. В поле "Имя" введите "InvoiceNumber".
    * InvoiceNumber  
12. Нажмите кнопку "OК".
13. Щелкните "Добавить атрибут".
14. В поле "Имя" введите "InvoiceAmount".
    * InvoiceAmount  
15. Нажмите кнопку "OК".
16. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
17. В дереве выберите "XML\Элемент".
18. В поле "Имя" введите "EnclosedDocs".
    * EnclosedDocs  
19. Нажмите кнопку "OК".
20. В дереве выберите "Накладная\EnclosedDocs".
21. Щелкните "Добавить элемент".
22. В поле "Имя" введите "Документ".
    * Документ  
23. Нажмите кнопку "OК".
24. В дереве выберите "Накладная\EnclosedDocs\Документ".
25. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
26. В дереве выберите "'XML\Атрибут".
27. В поле "Имя" введите "FileName".
    * FileName  
28. Нажмите кнопку "OК".
29. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
30. В дереве выберите "XML\Элемент".
31. В поле "Имя" введите "FileContent".
    * FileContent  
32. Нажмите кнопку "OК".
33. В дереве выберите "Накладная\EnclosedDocs\Документ\FileContent".
34. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
35. В дереве выберите "Текст\Base64".
36. Нажмите кнопку "OК".

## <a name="map-format-elements-to-data-model-as-data-source"></a>Сопоставление элементов формата с моделью данных в качестве источника данных
1. В дереве выберите "Накладная\SalesOrder".
2. Перейдите на вкладку "Сопоставление".
3. В дереве разверните узел "model".
4. В дереве выберите "модуль\Номер заказа на продажу(SalesId)".
5. Щелкните "Связать".
6. В дереве выберите "Накладная\InvoiceNumber".
7. В дереве разверните "модель\Базовая накладная(InvoiceBase)".
8. В дереве выберите "модель\Базовая накладная(InvoiceBase)\Номер накладной(Id)".
9. Щелкните "Связать".
10. В дереве выберите "Накладная\InvoiceAmount".
11. В дереве выберите "модель\Базовая накладная(InvoiceBase)\Сумма накладной(Amount)".
12. Щелкните "Связать".
13. В дереве разверните "модель\Вложения накладной".
14. В дереве выберите "модель\Вложения накладной\Содержимое файла".
15. В дереве выберите "Накладная\EnclosedDocs\Документ\FileContent\Base64".
16. Щелкните "Связать".
17. В дереве выберите "модель\Вложения накладной\Имя файла".
18. В дереве выберите "Накладная\EnclosedDocs\Документ\FileName".
19. Щелкните "Связать".
20. В дереве выберите "модель\Вложения накладной".
21. В дереве выберите "Накладная\EnclosedDocs\Документ".
22. Щелкните "Связать".
23. Нажмите кнопку "Сохранить".
24. Закройте страницу.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
