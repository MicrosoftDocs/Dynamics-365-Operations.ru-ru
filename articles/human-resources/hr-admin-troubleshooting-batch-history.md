---
title: Оптимизация производительности с помощью задач автоматической очистки
description: В этой теме объясняется, как улучшить производительность в Microsoft Dynamics 365 Human Resources, выполнив очистку журнала пакетных заданий.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a293b128364b8b0b293da03495d55e46f6b01fd6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066101"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Оптимизация производительности с помощью задач автоматической очистки


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Выдать**

Microsoft Dynamics 365 Human Resources может столкнуться с проблемами производительности, если журнал пакетных заданий стал слишком большим.

**Причина**

Часто выполняемые пакетные задания могут стать причиной неконтролируемого роста журнала пакетных заданий. Это может привести к проблемам с производительностью. 

**Приказ**

Запланируйте автоматическую задачу для очистки журнала пакетных заданий. Рекомендуется настроить задание на выполнение еженедельно, но, в зависимости от среды, может потребоваться выполнить очистку чаще или реже. Следующая процедура содержит рекомендуемые параметры, но их можно изменить в соответствии со своими потребностями.

1. В модуле Human Resources выберите **Администрирование системы**.

2. На панели **Поиск** введите **Очистка журнала пакетных заданий**.

   ![Поиск очистки журнала пакетных заданий.](media/talent-batch-history-cleanup-search-bar.png)

3. В поле **Горизонт истории (дни)** введите **30**.

   ![Задание горизонта истории в 30 дней.](media/talent-batch-history-cleanup-history-limit.png)

4. Выберите **Выполнять в фоновом режиме**, затем выберите **Повторение**.

   ![Задание повторения.](media/talent-batch-history-cleanup-recurrence.png)

5. В области **Определение повторения** задайте поля **Дата начала** и **Время начала** на нерабочее время или выходные, затем выберите **НЕТ ДАТЫ ОКОНЧАНИЯ**. 

   ![Задание даты и времени начала повторения.](media/talent-batch-history-cleanup-define-recurrence.png)

6. В области **ШАБЛОН ПОВТОРЕНИЯ** выберите **Дни** и задайте для параметра **ПОВТОРИТЬ ПОСЛЕ УКАЗАННОГО ИНТЕРВАЛА** значение **7**.

   ![Задание еженедельного повторения очистки.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Нажмите **ОК**.

8. При необходимости измените любые другие параметры в области **Выполнять в фоновом режиме**, затем выберите **ОК**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
