--- 
title: "Создание правила фиксированного канбана для производства"
description: "Эта процедура описывает настройку, необходимую для создания фиксированного производственного правила канбана для включения действий преобразования, в производственной ячейке, в экономичной среде."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 865beb1ee8b418d71c46f1842fb96e73090fd511
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Создание правила фиксированного канбана для производства

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура описывает настройку, необходимую для создания фиксированного производственного правила канбана для включения действий преобразования, в производственной ячейке, в экономичной среде. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта.


## <a name="create-new-kanban-rule"></a>Создать новое правило канбана
1. Перейти к правилам канбана.
2. Щелкните "Создать".
    * Обратите внимание, что типом по умолчанию является производство, а стратегией пополнения — "фиксировано". Нет необходимости изменять эти параметры.  
3. В поле "Первое мероприятие плана" введите или выберите значение.
    * Это действие, которое будет выполняться для канбанов, созданных на основе этого правила канбана.  Выберите "SpeakerTestAndPackaging".  
4. Разверните раздел "Сведения".
5. В поле "Продукт" введите или выберите значение.
    * Выберите L0050.  
6. В поле "Единица измерения" введите или выберите значение.
    * Выберите минуты.  
7. В поле "Время упреждения" введите число.
    * Введите 5.  

## <a name="set-quantities"></a>Указание количества
1. Развернуть раздел "Количества".
2. Установите количество по умолчанию равным 10.
    * Это количество, которое будет передано для каждого канбана.  
3. Установите флажок "Отклонение по количеству продукта".
    * При этом, выбранные канбаны можно выполнить с расхождением от количества по умолчанию.  Чтобы разрешить выполнение канбанов с количеством от 8 до 12, установите оба отклонения как 2.  
4. Задайте расхождение ниже "2".
    * Это позволит выполнить вниз до 10 – 2 = 8  
5. Задайте расхождение выше "2".
    * Это позволит выполнить вверх до 10 + 2 = 12  
6. В поле "Фиксированное количество канбанов" введите число.
    * Это сумма канбанов, которые должны быть активными. В этом случае 5 канбанов обрабатывают 10 каждый.  
7. В поле "Минимальная граница оповещения" введите "2".
    * Используется для того, чтобы отслеживать минимальную сумму полных канбанов, которые должны находиться в месте назначения. Например, это используется при обзоре количества канбанов.  
8. В поле "Максимальная граница оповещения" введите "4".
    * Используется для того, чтобы отслеживать максимальную сумму полных канбанов, которые должны находиться в месте назначения. Например, это используется при обзоре количества канбанов.  
9. В поле "Автоматическое планирование количества" введите "1".
    * Если задать 1, это означает, что каждый канбан будет автоматически запланирован.   Если ввести 3, канбаны не будут запланированы, пока 3 пустых канбана готовы для планирования. Это полезно для группировки работ и упрощения настройки.  

## <a name="create-kanbans"></a>Создание канбанов
1. Разверните раздел "Канбаны".
2. Нажмите кнопку "Сохранить".
    * Правило канбана должно быть сохранено, прежде чем канбаны можно создать.  
3. Нажмите кнопку Добавить.
    * Обратите внимание, что нет активных канбанов, поэтому для количества новых канбанов предлагается 5. Это равно значению в поле "Фиксированное количество канбанов".  
4. Щелкните "Создать".
    * Это создаст 5 канбанов.  
    * Обратите внимание, что 5 канбанов, по 10 каждый, были созданы для этого производственного правила канбана. Это последний этап в этой процедуре.  

