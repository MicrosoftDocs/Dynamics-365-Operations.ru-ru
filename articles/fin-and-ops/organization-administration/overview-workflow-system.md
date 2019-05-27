---
title: Система бизнес-правил
description: В этой теме описывается система workflow-процессов в Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
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
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545817"
---
# <a name="workflow-system"></a>Система бизнес-правил

[!include [banner](../includes/banner.md)]

В этой теме описывается система workflow-процессов в Microsoft Dynamics 365 for Finance and Operations.

## <a name="what-is-workflow"></a>Что такое Wokrflow?

Термин *workflow-процесс* можно определить 2 способами: как система и как бизнес-процесс.

### <a name="workflow-is-a-system"></a>Документооборот как система

Workflow-процесс — это система, которая устанавливается с Finance and Operations и выполняется на сервере Application Object Server (AOS). Система workflow-процессов предоставляет функции, позволяющие создавать отдельные workflow-процессы, или бизнес-процессы.

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

+ [Архитектура workflow-процесса](workflow-system-architecture.md)
+ [Элементы workflow-процесса](workflow-elements.md)
+ [Действия workflow-процесса](workflow-actions.md)
+ [Создание workflow-процесса](create-workflow.md)
+ [Настройка свойств workflow-процесса](configure-workflow-properties.md)
+ [Настройка ручной задачи в workflow-процессе](configure-manual-task-workflow.md)
+ [Настройка автоматизированной задачи в workflow-процессе](configure-automated-task-workflow.md)
+ [Настройка процесса утверждения в workflow-процессе](configure-approval-process-workflow.md)
+ [Настройка этапа утверждения в workflow-процессе](configure-approval-step-workflow.md)
+ [Настройка ручного решения в workflow-процессе](configure-manual-decision-workflow.md)
+ [Настройка условного решения в workflow-процессе](configure-conditional-decision-workflow.md)
+ [Настройка параллельного действия в workflow-процессе](configure-parallel-activity-workflow.md)
+ [Настройка параллельной ветви в workflow-процессе](configure-parallel-branch-workflow.md)
+ [Настройка workflow-процесса по номенклатуре строки](configure-line-item-workflow.md)
+ [Вопросы и ответы по workflow-процессу](workflow-FAQ.md)
