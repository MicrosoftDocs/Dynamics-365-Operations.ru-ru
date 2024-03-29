---
title: Создание заявки, связанной с запросом предложения
description: В этой статье объясняется, как добавить сведения о цене и поставщике в заявку на покупку из процесса запроса предложения.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecde250e3517464611b68fe3c960bfbfdf06319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846021"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Создание заявки, связанной с запросом предложения

[!include [banner](../../includes/banner.md)]

В этой статье объясняется, как добавить сведения о цене и поставщике в заявку на покупку из процесса запроса предложения. Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF, при этом вы должны выполнить вход в систему как администратор, чтобы завершить выполнение всех шагов. Задачи в этом руководстве обычно выполняются специалистами по закупкам.


## <a name="create-a-requisition"></a>Создание заявки
1. В области переходов выберите **Модули > Закупки и источники > Заявки на закупку > Заявки на покупку, подготовленные мной**.
2. Выберите **Создать**.
3. В поле **Имя** введите значение.
4. В поле **Запрошенная дата** введите дату.
5. В поле **Дата учета** введите дату.
6. Нажмите **ОК**.
7. В поле **Причина** введите или выберите значение.
8. Выберите **Добавить строку**.
9. В поле **Категория закупаемой продукции** выберите категорию в дереве и выберите **ОК**.
10. В поле **Имя продукта** введите значение.
11. В поле **Количество** введите число.
12. В поле **Единица измерения** введите или выберите значение.
13. Нажмите **Сохранить**.
14. Выберите **Документооборот**, чтобы открыть ниспадающее диалоговое окно.
15. Выберите **Отправить**.
16. Закройте страницу.
17. Выберите **Отправить**.

## <a name="reassign-a-workflow-task"></a>Повторное назначение задачи workflow-процесса
Следующая задача — создание запроса предложения для получения предложений от поставщиков относительно продукта. В компании с демонстрационными данными USMF workflow-процесс заявки настроен с правилом, согласно которому, если поставщик не выбран или цена за единицу равна 0 для строки, задача назначается определенному работнику для создания запроса предложения. Для продолжения выполнения этого руководства необходимо повторно назначить эту задачу другому пользователю (самостоятельно). Это можно сделать, только если вы выполнили вход в систему как администратор.  

1. Выберите **Документооборот**, чтобы открыть ниспадающее диалоговое окно.
2. Выберите **Просмотр журнала**.
3. Обновите страницу.
4. Разверните раздел **Отслеживание сведений**.
5. В дереве выберите строку, которая начинается со слов "Рабочий процесс строки активирован для".
6. Выберите **Просмотреть сведения о workflow-процессе**.
7. Разверните раздел **Рабочие элементы**.
8. Выберите **Назначить повторно**.
9. В поле **Пользователь** выберите **Администратор**.
10. Выберите **Назначить повторно**.
11. Закройте две страницы.

## <a name="create-an-rfq"></a>Создание запроса предложения

1. Обновите страницу.
2. Выберите **Запрос предложения**.
3. В поле **Юридическое лицо-покупатель** выберите **USMF**. Следует выбрать то же юридическое лицо, которое выбрано в строке заявки.  
4. В списке пометьте выбранную строку. При наличии нескольких строк в заявке на покупку выберите все строки, которые следует добавить в запрос предложения.  
5. Нажмите **ОК**.
6. Обновите страницу.
7. Убедитесь, что открыто информационное поле, затем разверните раздел **Связанные документы**.
8. Выберите ссылку в поле **Запрос предложения**, чтобы открыть созданный запрос предложения.
9. Выберите **Заголовок**.
10. Выберите **Добавить**.
11. В поле **Счет поставщика** введите или выберите значение.
12. Выберите **Добавить**.
13. В поле **Счет поставщика** введите или выберите значение.
14. Выберите **Отправить**.
15. Нажмите **ОК**.
16. Выберите **Введите ответ**.
17. В области действий выберите **Ответ**.
18. Выберите **Копировать данные в ответ**. В результате будут скопированы данные, такие как количество и даты, из запроса предложения в ответ.  
19. В поле **Цена за единицу** введите число. Это цена, что полученная от поставщика. Может также потребоваться ввести дополнительную информацию от поставщика.  
20. Выберите **Принять**.
21. Нажмите **ОК**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Проверьте, что цена и поставщик были перенесены в заявку.
1. Закройте страницу.
2. Выберите **Строки**.
3. Выберите **Связанные сведения**.
4. Выберите **Заявка на покупку**.
5. Выберите строку, которая была перенесена в запрос предложения. Проверьте, что цена и поставщик были скопированы в заявку.  
6. Выберите **Документооборот**, чтобы открыть ниспадающее диалоговое окно.
7. Выберите "Завершить".
8. Выберите страницу.
9. Выберите "Завершить".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]