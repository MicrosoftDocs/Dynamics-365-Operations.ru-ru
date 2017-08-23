--- 
title: "Создание операционного ресурса"
description: "Операционный ресурс участвует в мероприятиях проекта или производственного процесса."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 12e4a93f908c348a848e056df00115bf2dc50635
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-operations-resource"></a>Создание операционного ресурса

[!include[task guide banner](../../includes/task-guide-banner.md)]

Операционный ресурс участвует в мероприятиях проекта или производственного процесса. В этой процедуре показано, как определить операционный ресурс. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.

1. Перейдите в раздел "Ресурсы".
2. Щелкните "Создать".
3. В поле "Ресурс" введите значение.
4. В поле "Описание" введите значение.

## <a name="define-capacity-and-consumption-parameters"></a>Определение параметров мощности и потребления
1. Разверните раздел "Операция".
2. В поле "Процент отходов" введите число.
3. В поле "Категория настройки" введите или выберите значение.
    * Укажите категорию затрат, которая определяет способ учета затрат на настройку.  
4. В поле "Категория времени выполнения" введите или выберите значение.
    * Укажите категорию затрат, которая определяет способ учета затрат на время выполнения.  
5. В поле "Количественная категория" введите или выберите значение.
    * Укажите категорию затрат, которая определяет способ учета стоимости ресурсов на основании выпускаемого количества.  
6. В поле "Ед. изм. мощности" выберите вариант.
    * Укажите единицу измерения, в которой выражается мощность операционного ресурса.  
7. В поле "Мощность" введите число.
8. В поле "Процент эффективности" введите число.
    * Укажите процент эффективности, ожидаемый от операционного ресурса. Процент эффективности корректирует пропускную способность операционного ресурса и влияет на время, зарезервированное для ресурса.  
9. В поле "Процент планирования операций" введите число.
    * Укажите максимальный процент мощности операционного ресурса, который требуется использовать при планировании операций.  
10. Выберите значение "Да" в поле "Ограничение по мощности".
    * Задайте для этого параметра значение "Да", если операционный ресурс должен планироваться на основании фактической доступной мощности и если должны учитываться существующие резервирования мощностей. Если для этого параметра задать значение "Нет", будет предполагаться, что операционный ресурс имеет неограниченную мощность и может быть зарезервирован с превышением.  
11. Выберите значение "Да" в поле "Минимальный ресурс".

## <a name="define-working-times"></a>Определение рабочего времени
1. Разверните раздел "Календари".
2. Нажмите кнопку Добавить.
3. В поле "Календарь" введите или выберите значение.
    * Укажите календарь рабочего времени, определяющий мощность ресурса (в часах).  
4. В списке найдите и выберите требуемую запись.
5. В списке перейдите по ссылке в выбранной строке.

## <a name="define-resource-capabilities"></a>Определение возможностей ресурса
1. Разверните раздел "Возможности".
2. Нажмите кнопку Добавить.
    * Возможность — это способность операционного ресурса участвовать в определенном мероприятии. Механизм планирования распределяет ресурсы, сопоставляя требования каждого мероприятия к ресурсам с возможностями доступных операционных ресурсов.  
3. В поле "Возможность" введите или выберите значение.
4. В поле "Уровень" введите число.
    * Укажите уровень квалификации, по которому обрабатывается возможность ресурса.  
5. В поле "Приоритет" введите число.
    * Укажите приоритет операционного ресурса по отношению к возможности. При планировании по приоритету операционный ресурс с наивысшим приоритетом (наименьшим числовым значением) выбирается первым.  

## <a name="assign-resource-to-resource-group"></a>Назначение ресурса группе ресурсов
1. Разверните раздел "Группы ресурсов".
2. Нажмите кнопку Добавить.
    * Группа ресурсов определяет сайт, производственное подразделение и контекст склада для операционных ресурсов. Операционный ресурс можно запланировать, только если он назначен группе ресурсов и только на сайте, на котором находится группа ресурсов.  
3. В поле "Группа ресурсов" введите или выберите значение.
4. В поле "Место хранения на складе получения" введите или выберите значение.
    * Укажите местонахождение склада, из которого операционный ресурс потребляет материалы.  

