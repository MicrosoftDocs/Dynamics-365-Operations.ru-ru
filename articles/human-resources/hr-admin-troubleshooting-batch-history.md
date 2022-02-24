---
title: Оптимизация производительности с помощью задач автоматической очистки
description: В этой статье объясняется, как решать некоторые проблемы с производительностью в Microsoft Dynamics 365 Human Resources, выполнив очистку журнала пакетных заданий.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420188"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Оптимизация производительности с помощью задач автоматической очистки

**Выдать**

Microsoft Dynamics 365 Human Resources может столкнуться с проблемами производительности, если журнал пакетных заданий стал слишком большим.

**Причина**

Часто выполняемые пакетные задания могут стать причиной неконтролируемого роста журнала пакетных заданий. Это может привести к проблемам с производительностью. 

**Приказ**

Запланируйте автоматическую задачу для очистки журнала пакетных заданий. Рекомендуется настроить задание на выполнение еженедельно, но, в зависимости от среды, может потребоваться выполнить очистку чаще или реже. Следующая процедура содержит рекомендуемые параметры, но их можно изменить в соответствии со своими потребностями.

1. В модуле Human Resources выберите **Администрирование системы**.

2. На панели **Поиск** введите **Очистка журнала пакетных заданий**.

   ![Поиск очистки журнала пакетных заданий](media/talent-batch-history-cleanup-search-bar.png)

3. В поле **Горизонт истории (дни)** введите **30**.

   ![Задание горизонта истории в 30 дней](media/talent-batch-history-cleanup-history-limit.png)

4. Выберите **Выполнять в фоновом режиме**, затем выберите **Повторение**.

   ![Задание повторения](media/talent-batch-history-cleanup-recurrence.png)

5. В области **Определение повторения** задайте поля **Дата начала** и **Время начала** на нерабочее время или выходные, затем выберите **НЕТ ДАТЫ ОКОНЧАНИЯ**. 

   ![Задание даты и времени начала повторения](media/talent-batch-history-cleanup-define-recurrence.png)

6. В области **ШАБЛОН ПОВТОРЕНИЯ** выберите **Дни** и задайте для параметра **ПОВТОРИТЬ ПОСЛЕ УКАЗАННОГО ИНТЕРВАЛА** значение **7**.

   ![Задание еженедельного повторения очистки](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Нажмите **ОК**.

8. При необходимости измените любые другие параметры в области **Выполнять в фоновом режиме**, затем выберите **ОК**.

