---
title: Обзор системы бизнес-правил
description: В этой теме описывается система рабочих процессов.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068f464fe5385486827b2f904114eb663e08b2e8
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697977"
---
# <a name="workflow-system-overview"></a>Обзор системы бизнес-правил

[!include [banner](../includes/banner.md)]

В этой теме описывается система рабочих процессов.

## <a name="what-is-workflow"></a>Что такое Wokrflow?

Термин *workflow-процесс* можно определить 2 способами: как система и как бизнес-процесс.

### <a name="workflow-is-a-system"></a>Документооборот как система

Рабочий процесс — это система, которая выполняется на сервере Application Object Server (AOS). Система workflow-процессов предоставляет функции, позволяющие создавать отдельные workflow-процессы, или бизнес-процессы.

### <a name="workflow-is-a-business-process"></a>Документооборот как бизнес-процесс

workflow-процесс представляет бизнес-процесс. Он определяет потоки, или перемещения, документа по системе, показывая, кто должен выполнить задачу, принять решение или утвердить документ. Например, на следующем рисунке показан workflow-процесс для отчетов о расходах.

![Workflow-процесс с элементами, назначенными пользователям](./media/workflow_user.gif)

Для прояснения этого workflow-процесса предположим, что Сэм подает отчет о расходах на сумму USD 7000. В этом случае Иван должен рассмотреть приходы, направленные ему Сэмом. Затем Фрэнк и Сью должны утвердить отчет о расходах. Теперь предположим, что Сэм подает отчет о расходах на сумму 11 000 USD. В этом случае Иван должен рассмотреть чеки, а Фрэнк, Сью и Анна должны утвердить отчет о расходах.

## <a name="benefits-of-using-the-workflow-system"></a>Преимущества использования системы workflow-процессов

Имеется несколько преимуществ использования системы workflow-процессов в организации:

- **Непротиворечивые процессы** - можно определить как обрабатываются определенные документы, таких как заявки на покупку и отчеты по расходам. Использование системы workflow-процессов может обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.
- **Видимость процессов** - можно отслеживать статус, историю и метрики производительности экземпляров workflow-процесса. Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.
- **Централизованный список работ** — Пользователи могут просматривать централизованный список работ, отображающий задачи workflow-процесса и утверждения, назначенные им.


## <a name="workflow-content"></a>Содержимое workflow-процесса

+ [Архитектура системы бизнес-правил](workflow-system-architecture.md)
+ [Элементы бизнес-правила](workflow-elements.md)
+ [Действия в процессах утверждения бизнес-правил](workflow-actions.md)
+ [Обзор создания бизнес-правил](create-workflow.md)
+ [Настройка свойств рабочего процесса](configure-workflow-properties.md)
+ [Настройка ручных задач в workflow-процессе](configure-manual-task-workflow.md)
+ [Настройка автоматизированных задач в workflow-процессе](configure-automated-task-workflow.md)
+ [Настройка процессов утверждения в workflow-процессе](configure-approval-process-workflow.md)
+ [Настройка этапов утверждения в workflow-процессе](configure-approval-step-workflow.md)
+ [Настройка ручных решений в workflow-процессе](configure-manual-decision-workflow.md)
+ [Настройка условных решений в workflow-процессе](configure-conditional-decision-workflow.md)
+ [Настройка параллельных действий в workflow-процессе](configure-parallel-activity-workflow.md)
+ [Настройка параллельных ветвей в workflow-процессе](configure-parallel-branch-workflow.md)
+ [Настройка бизнес-правил по строке](configure-line-item-workflow.md)
+ [Вопросы и ответы по рабочим процессам](workflow-FAQ.md)
