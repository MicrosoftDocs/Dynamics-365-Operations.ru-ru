--- 
title: "Настройка рабочего шаблона для заказов на покупку"
description: "Эта процедура описывает настройку простого шаблона работы, который следует использовать при размещении полученных номенклатур."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: aa561d558827e78529ef797b6df6dd3c1dcce34d
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Настройка рабочего шаблона для заказов на покупку

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура описывает настройку простого шаблона работы, который следует использовать при размещении полученных номенклатур. Шаблоны работы определяют набор инструкций, представленных работнику склада на мобильном устройстве при перемещении номенклатур из зоны получения. Эту процедуру можно использовать с данными в компании с демонстрационными данными USMF. Перед началом этого руководства создайте код пула работы. В этом примере используется код пула работы с названием "Входящие". Эта процедура предназначена для менеджера склада.

1. Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Шаблоны работ".
2. В поле "Тип заказа на выполнение работ" выберите "Заказ на покупку".

## <a name="create-a-work-template-header"></a>Создание заголовка шаблона работы
1. Щелкните "Создать".
2. В поле "Порядковый номер" введите число.
    * Это последовательность, в которой оцениваются шаблоны работы. При необходимости последовательность можно изменить.  
3. В поле "Шаблон работы" введите значение.
    * Это уникальный идентификатор для этого шаблона.  
4. В поле "Описание шаблона работы" введите значение.
    * Параметр "Допустимо" не должен быть установлен, пока не завершены все сведения, требуемые для шаблона и затем не нажато "Сохранить".  
    * Заказ на выполнение работ типа "заказ на покупку" не может быть автоматически обработан, поэтому оставьте значение параметра "Автоматическая обработка" как "Нет".  
5. В поле "Код пула работы" введите значение.
    * Коды пулов работ можно использовать для организации работы в группы. Значение, которые задано здесь, будет значением по умолчанию для любой работы, созданной с использованием этого шаблона.  
6. В поле "Приоритет работы" введите "1".
    * Это означает важность работы и значение, которое задано здесь, будет использоваться по умолчанию для любой работы, созданной с использованием этого шаблона.  
7. Нажмите кнопку "Сохранить".
    * Необходимо сохранить заголовок шаблона работы, прежде чем кнопка "Изменить запрос" становится доступной.  

## <a name="set-up-the-query-for-the-work-template"></a>Настройка запроса для шаблона работы
1. Щелкните "Изменить запрос".
    * Мы зададим ограничение, чтобы шаблон можно было использовать только в рамках конкретного склада.  
2. Нажмите кнопку Добавить.
3. В списке пометьте выбранную строку.
4. В поле "Поле" введите "склад".
5. В поле "Критерии" введите значение.
6. Нажмите кнопку "OК".
7. Щелкните Да.

## <a name="set-work-template-details"></a>Задание сведений шаблона работы
1. Щелкните "Создать".
2. В поле "Тип работы" выберите "Комплектация".
3. В поле "Код класса работы" введите "покупка".
    * Класс работы, заданный здесь, будет использоваться по умолчанию во всех строках работы типа "комплектация", созданных с использованием этого шаблона. Класс работы нельзя переопределить из строк заказа на выполнение работ. Классы работ используются для направления и/или ограничения типа строк заказа на выполнение работ, которые работник склада может обрабатывать на мобильном устройстве.  
4. Щелкните "Создать".
5. В поле "Тип работы" выберите "Поместить".
6. В поле "Код класса работы" введите значение.
    * Инструкции по комплектации и размещению являются набором. Пары "комплектация/размещение" должны иметь один и тот же класс работ. Используйте один и тот же класс работ, предоставленный для инструкции комплектации.  
7. Нажмите кнопку "Сохранить".
    * Обратите внимание, что теперь флажок "Допустимо" установлен.  

