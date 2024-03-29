---
title: Создание мероприятий процесса для бережливого производства
description: Создайте мероприятие процесса для бережливого производства.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 214e54cc93379948e4c25b3b28d835bbbbd40b72
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570161"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Создание мероприятий процесса для бережливого производства

[!include [banner](../../includes/banner.md)]

Создайте мероприятие процесса для бережливого производства. 

Обязательные компоненты: 

1. Необходимо создать производственный поток и версию, которые будут неактивны.

2. Необходимо создать производственную ячейку.


## <a name="find-the-production-flow-version"></a>Поиск версии производственного потока
1. Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.

## <a name="create-a-new-activity"></a>Создание нового мероприятия
1. Щелкните "Мероприятия".
    * Убедитесь, что выбранный производственный поток содержит версию-черновик и выберите эту версию.  
2. Щелкните "Создание нового мероприятия плана".
3. Щелкните Далее.
4. В поле "Имя" введите значение.
5. В поле "Имя" введите значение.
    * Обратите внимание, что имя должно быть уникальным для данного производственного потока для всех версий.  
6. В поле "Количество процесса" введите число.
    * Обратите внимание, что независимо от того, какое количество задания будет обработано, это минимальное количество на задание для расчета трудовых затрат. Если количества для задания отличаются от этого количества, то будет создано отклонение стоимости.  
7. Щелкните Далее.

## <a name="select-the-work-cell"></a>Выбор производственной ячейки
1. В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
2. В списке перейдите по ссылке в выбранной строке.

## <a name="define-the-inventory-updates"></a>Определение обновлений запасов
1. Установите или снимите флажок "Обновление запасов в наличии при поступлении".
    * Если значение "Обновление запасов в наличии" — "Нет", можно определить мероприятие для получения полуфабриката (мероприятие не достигает следующего уровня спецификации).    Можно также выбрать потребление полуфабрикатов.  

## <a name="define-the-picking-activities"></a>Определение мероприятий комплектации
1. Щелкните Далее.
2. В списке пометьте выбранную строку.
    * Мероприятия комплектации по умолчанию создается для исходного местоположения выбранной производственной ячейки.  
3. Нажмите кнопку Добавить.
    * Можно создать дополнительные мероприятия комплектации для конкретных продуктов, которые не указаны в исходном мероприятии производственной ячейки.  
4. В списке найдите и выберите требуемую запись.
5. В поле "Код номенклатуры" введите значение.
6. В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
    * С этим определением все материалы, потребленные в мероприятии комплектуются из исходного склада и местоположения по умолчанию за исключением номенклатуры, которая определена во втором мероприятии комплектации. Эта номенклатура будет скомплектована из других склада и местоположения.  
7. В списке найдите и выберите требуемую запись.
8. В списке перейдите по ссылке в выбранной строке.
9. Установите или удалите флажок "Зарегистрировать отходы".
10. Щелкните Далее.

## <a name="define-the-activity-times"></a>Определение времени мероприятия
1. В списке найдите и выберите требуемую запись.
    * Требуется определение времени выполнения. Время выполнения используется для расчета затрат и времени пропускной способности заданий канбана. Времена выполнения не используются для расчета максимальной мощности и потребления, это рассчитывается временем цикла, производным от задачи версии производственного потока.  
2. В поле "Время" введите число.
3. В поле "Единица измерения" введите значение.
4. Выберите единицу времени.
5. В поле "На количество" введите число.
6. В списке найдите и выберите требуемую запись.
    * Время ожидания в очереди является необязательным.  
7. В поле "Время" введите число.
8. В поле "Единица измерения" введите значение.
9. Выберите единицу времени.
10. В поле "На количество" введите число.
11. Щелкните Далее.
12. Нажмите кнопку Готово.
13. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]