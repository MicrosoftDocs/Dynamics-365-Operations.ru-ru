---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)
description: В этой теме описывается, как настроить формат электронной отчетности (ER), чтобы в выходных данных электронной отчетности использовать файлы управления документами (вложения). (Часть 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754922"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)

[!include [banner](../../includes/banner.md)]

В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности. Эти шаги можно выполнить в любой компании.

Для выполнения этих действий необходимо сначала выполнить шаги в руководстве по задаче "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)".

Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Расширение модели данных, чтобы представлять в ней файлы управления документами
1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
2. Щелкните "Конфигурации отчетности".
3. В дереве разверните "Модель накладной клиента".
4. В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".
5. Выберите Конструктор.
6. В дереве выберите "Накладная клиента(InvoiceCustomer)".
    * Мы расширим эту модель данных, чтобы представлять в ней любые файлы, которые были приложены к заказу на продажу, который относится к электронной обработке накладной.  
7. Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.
8. В поле "Имя" введите "Вложения накладной".
    * Вложения накладной  
9. В поле "Тип элемента" выберите "Список записей".
10. Нажмите кнопку Добавить.
11. Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.
12. В поле "Имя" введите "Содержимое файла".
    * Содержание файла  
13. В поле "Тип элемента" выберите "Контейнер".
14. Нажмите кнопку Добавить.
15. Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.
16. В поле "Имя" введите "Имя файла".
    * Имя файла  
17. В поле "Тип элемента" выберите "Строка".
18. Нажмите кнопку Добавить.

## <a name="map-new-data-model-elements-to-data-sources"></a>Сопоставление новых элементов модели данных с источниками данных
1. Щелкните "Сопоставить модель с источником данных".
2. Используйте экспресс-фильтр для фильтрации поля "Описание" со значением "InvoiceCustomer".
    * InvoiceCustomer  
    * Мы составим новые элементы модели с соответствующими источниками данных.  
3. Выберите Конструктор.
4. В дереве выберите "Вложения накладной".
5. В дереве разверните "Вложения накладной".
6. В дереве выберите "Вложения накладной\Имя файла".
7. Щелкните "Изменить".
8. В поле "Формула" введите "CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'".
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Нажмите кнопку "Сохранить".
10. Закройте страницу.
11. В дереве выберите "Вложения накладной\Содержимое файла".
12. Щелкните "Изменить".
13. В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Нажмите кнопку "Сохранить".
15. Закройте страницу.
16. В дереве выберите "Вложения накладной".
17. Щелкните "Изменить".
18. В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Нажмите кнопку "Сохранить".
20. Закройте страницу.
21. Нажмите кнопку "Сохранить".
22. Закройте страницу.
23. Закройте страницу.
24. Закройте страницу.
25. Щелкните "Изменить статус".
26. Щелкните "Завершить".
27. Нажмите кнопку "OК".



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]