---
title: Отчеты о расходах и несколько утверждающих
description: В этом разделе представлены сведения об отчетах о расходах, которые требуют утверждения несколькими пользователями.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179591"
---
# <a name="expense-reports-and-multiple-approvers"></a>Отчеты о расходах и несколько утверждающих

[!include [banner](../includes/banner.md)]

В зависимости от политик утверждения расходов вашей организации может потребоваться, чтобы несколько человек утверждали отчет о расходах, переданный сотрудником. При настройке workflow-процесса для утверждения отчета о расходах можно добавить дополнительные элемента workflow-процесса, которые содержат задачи или шаги для одного или нескольких лиц, утверждающих отчет о расходах. Например, можно требовать, чтобы все отчеты о расходах сначала утверждались руководителем сотрудника, передавшего отчет, а затем — координатором расчетов с поставщиками.

Если вы решили использовать несколько лиц, утверждающих отчет о расходах, вы можете добавить элементы workflow-процесса следующими способами.

- Добавьте один элемент утверждения, который имеет один шаг. Например, шаг может требовать, чтобы отчет о расходах был назначен группе пользователей, и чтобы его утвердили 50 процентов участников этой группы.
- Добавьте один элемент утверждения, который имеет несколько шагов. Например, элемент утверждения может содержать следующие шаги:

    1. Руководитель сотрудника, создавшего отчет о расходах, утверждает его.
    2. Сотрудник отдела расчетов с поставщиками проверяет получения и номенклатуры отчета о расходах.
    3. Владелец бюджета утверждает отчет о расходах.

- Добавьте несколько элементов утверждения, каждый из которых содержит один шаг. Например, можно добавить отдельный элемент утверждения для каждого из следующих действий:

    1. Руководитель сотрудника утверждает отчет о расходах.
    2. Владелец бюджета утверждает отчет о расходах.