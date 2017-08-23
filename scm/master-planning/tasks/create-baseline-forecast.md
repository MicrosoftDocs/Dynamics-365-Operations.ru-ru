--- 
title: "Создание базового прогноза"
description: "Планировщик производства может создать базовый прогноз либо путем использования моделей прогнозирования временных рядов, либо путем копирования исторического спроса."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c94a9766319531bd8285cca04003225709ce2113
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-baseline-forecast"></a>Создание базового прогноза

[!include[task guide banner](../../includes/task-guide-banner.md)]

Планировщик производства может создать базовый прогноз либо путем использования моделей прогнозирования временных рядов, либо путем копирования исторического спроса. В этой процедуре показано, как скопировать исторический спрос, чтобы создать базовый прогноз для всех продуктов с использованием одного ключа распределения номенклатур. 


## <a name="set-up-an-item-allocation-key"></a>Настройка ключа распределения номенклатуры
1. Перейдите в раздел "Сводное планирование" > "Настройка" > "Группы внутрихолдингового планирования".
2. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Имя" по значению "10".
    * Прогнозирование спроса выполняется в разных юридических лицах. Поэтому необходимо настроить все компании, для которых требуется сформировать прогнозы, в виде одной группы внутрихолдингового планирования.  
3. В списке найдите и выберите требуемую запись.
4. Щелкните "Ключи распределения номенклатуры".
    * Выберите все ключи распределения номенклатур, для которых требуется создать прогнозы.  
5. В списке пометьте выбранную строку.
    * Выберите ключ распределения номенклатур D_Aloc.  
6. Щелкните >.
7. Закройте страницу.
8. Закройте страницу.

## <a name="set-up-the-demand-forecasting-paramters"></a>Настройка параметров прогнозирования спроса
1. Перейдите в раздел "Сводное планирование" > "Настройка" > "Прогнозирование спроса" > "Параметры прогнозирования спроса".
2. Разверните раздел "Параметры алгоритма прогнозирования".
3. В поле "Стратегия создания прогноза" выберите "Копировать поверх исторического спроса".
4. Нажмите кнопку "Сохранить".

## <a name="create-a-baseline-forecast"></a>Создание базового прогноза
1. Перейдите в раздел "Сводное планирование" > "Прогнозирование" > "Прогнозирование спроса" > "Сгенерировать статистический базовый прогноз".
2. В поле "Дата начала" введите дату.
    * Если заказы на продажу начинаются с 1 января 2015 г., введите эту дату. Если в противном случае введите самую раннюю дату заказов на продажу.  
3. В поле "Дата окончания" введите дату.
    * Введите последнюю дату заказов на продажу, например "2015-03-31".  
4. В поле "Дата начала" введите дату.
    * Введите "2015-04-01". Эта дата будет автоматически вычислена как дата начала следующего периода прогнозирования.  
5. Разверните раздел "Записи для добавления".
6. Щелкните "Фильтр".
7. В списке пометьте выбранную строку.
    * Отметьте строку, где Поле = Группа внутрихолдингового планирования.  
8. В поле "Критерии" введите значение.
    * Введите группу внутрихолдингового планирования — например, 10 — которая использовалась в первой задаче.  
9. В списке найдите и выберите требуемую запись.
    * Выберите строку, где Поле = Ключ распределения номенклатур.  
10. В поле "Критерии" введите значение.
11. Нажмите кнопку "OК".
12. Разверните раздел "Дополнительные параметры".
13. В поле "Период прогноза" выберите "Месяц".
14. В поле "Горизонт прогноза" введите "3".
15. В поле "Временная граница блокировки" введите значение "1".
16. Нажмите кнопку "OК".

## <a name="visualize-the-demand-forecast"></a>Визуализация прогноза спроса
1. Перейдите в раздел "Сводное планирование" > "Прогнозирование" > "Прогнозирование спроса" > "Скорректированный прогноз спроса".
2. В таблице агрегированного представления выберите ячейку в строке 1, столбце 2. Это второй месяц, для которого вы создали прогноз.
3. Установите QtyCell в значение "400".
    * Введите в ячейке число, отличное от спрогнозированного, — например, 400.  
4. Вы внесли вручную корректировку в прогноз. Обратите внимание на графическое указание на следующем шаге.
5. Щелкните "Сведения о строке прогноза".
    * На этой странице можно просмотреть значения точности, исторический спрос и прогноз. Также можно внести изменения в прогноз.  

