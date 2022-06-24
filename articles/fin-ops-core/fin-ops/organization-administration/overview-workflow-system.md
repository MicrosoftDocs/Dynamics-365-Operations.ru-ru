---
title: Обзор системы workflow-процессов
description: В этой статье описывается система workflow-процессов.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13dd4335a8b939a44ea7176a90f660999c32a83a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863198"
---
# <a name="workflow-system-overview"></a>Обзор системы workflow-процессов

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

В этой статье описывается система workflow-процессов.

## <a name="what-is-workflow"></a>Что такое Wokrflow?

Термин *workflow-процесс* можно определить 2 способами: как система и как бизнес-процесс.

### <a name="workflow-is-a-system"></a>Документооборот как система

Рабочий процесс — это система, которая выполняется на сервере Application Object Server (AOS). Система workflow-процессов предоставляет функции, позволяющие создавать отдельные workflow-процессы, или бизнес-процессы.

### <a name="workflow-is-a-business-process"></a>Документооборот как бизнес-процесс

workflow-процесс представляет бизнес-процесс. Он определяет потоки, или перемещения, документа по системе, показывая, кто должен выполнить задачу, принять решение или утвердить документ. Например, на следующем рисунке показан workflow-процесс для отчетов о расходах.

![Workflow-процесс с элементами, назначенными пользователям.](./media/workflow_user.gif)

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]