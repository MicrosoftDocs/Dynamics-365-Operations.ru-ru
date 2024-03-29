---
title: Настройка рабочего шаблона для заказов на покупку
description: В этой статье описывается настройка простого шаблона работы, который следует использовать при размещении полученных номенклатур.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee6bc896a979c326001e1596e4a463753005fabf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877373"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Настройка рабочего шаблона для заказов на покупку

[!include [banner](../../includes/banner.md)]

В этой статье описывается настройка простого шаблона работы, который следует использовать при размещении полученных номенклатур. Шаблоны работы определяют набор инструкций, представленных работнику склада на мобильном устройстве при перемещении номенклатур из зоны получения. Эту процедуру можно использовать с данными в компании с демонстрационными данными USMF. Перед началом этого руководства создайте код пула работы. В этом примере используется код пула работы с названием "Входящие". Эта процедура предназначена для менеджера склада.

1. В области перехода выберите **Модули > Управление складом > Настройка > Работа > Шаблоны работы**.
2. В поле **Тип заказа на работу** выберите **Заказ на покупку**.

## <a name="create-a-work-template-header"></a>Создание заголовка шаблона работы
1. Выберите **Создать**.
2. В поле **Порядковый номер** введите число. Это последовательность, в которой оцениваются шаблоны работы. При необходимости последовательность можно изменить.  
3. В поле **Шаблон работы** введите значение. Это уникальный идентификатор для этого шаблона.  
4. В поле **Описание шаблона работы** введите значение.
    - Параметр **Допустимо** не должен быть установлен, пока не завершены все сведения, требуемые для шаблона и затем не выбрано **Сохранить**.  
    - Заказ на выполнение работ типа **Заказ на покупку** не может быть автоматически обработан, поэтому оставьте значение параметра **Автоматическая обработка** как **Нет**.  
5. В поле **Код пула работы** введите значение. Коды пулов работ можно использовать для организации работы в группы. Значение, которые задано здесь, будет значением по умолчанию для любой работы, созданной с использованием этого шаблона.  
6. В поле **Приоритет работы** введите `1`. Это означает важность работы и значение, которое задано здесь, будет использоваться по умолчанию для любой работы, созданной с использованием этого шаблона.  
7. Нажмите **Сохранить**. Необходимо сохранить заголовок шаблона работы, прежде чем кнопка **Изменить запрос** становится доступной.  

## <a name="set-up-the-query-for-the-work-template"></a>Настройка запроса для шаблона работы
1. Выберите **Изменить запрос**. Мы зададим ограничение, чтобы шаблон можно было использовать только в рамках конкретного склада.  
2. Выберите **Добавить**.
3. В поле **Поля** новой строки введите `warehouse`.
4. В поле **Критерии** введите значение.
5. Нажмите **ОК**.
6. Выберите **Да**.

## <a name="set-work-template-details"></a>Задание сведений шаблона работы
1. Выберите **Создать**.
2. В поле **Тип работы** выберите **Комплектация**.
3. В поле **Код класса работы** введите `purchase`. Класс работы, заданный здесь, будет использоваться по умолчанию во всех строках работы типа "комплектация", созданных с использованием этого шаблона. Класс работы нельзя переопределить из строк заказа на выполнение работ. Классы работ используются для направления и/или ограничения типа строк заказа на выполнение работ, которые работник склада может обрабатывать на мобильном устройстве.  
4. Выберите **Создать**.
5. В поле **Тип работы** выберите **Поместить**.
6. В поле **Код класса работы** введите значение. Инструкции по комплектации и размещению являются набором. Пары "комплектация/размещение" должны иметь один и тот же класс работ. Используйте один и тот же класс работ, предоставленный для инструкции комплектации.  
7. Нажмите **Сохранить**. Обратите внимание, что теперь флажок **Допустимо** установлен.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]