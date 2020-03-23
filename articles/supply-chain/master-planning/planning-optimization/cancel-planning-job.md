---
title: Отмена задания планирования
description: В этой теме объясняется, как отменить активное задание планирования, в котором используются функции оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 18c5c7b8030fc6adbc548dab750e4f454aebc867
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076358"
---
# <a name="cancel-a-planning-job"></a>Отмена задания планирования

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

В Microsoft Dynamics 365 Supply Chain Management можно отменить активное задание планирования, в котором используются функции оптимизации планирования. Если в диалоговом окне выбрать **Отмена**, когда задание оптимизации планирования запускается непосредственно из интерфейса пользователя (не в фоновом режиме), это не отменит задания оптимизации планирования. Даже если вы получаете предупреждение, например "операция отменена", вам все равно придется выполнить следующие шаги для отмены задания планирования с оптимизацией планирования.


Чтобы отменить активное задание планирования, выполните следующие действия. 

> [!NOTE]
> Только активные задания могут быть отменены.

1. Перейдите **Сводное планирование \> Настройка \> Планы**.
2. Выберите соответствующий план для выполнения планирования.
3. Выберите **История**.
4. Выбор задания планирования для отмены.
5. Выберите **Отмена**.

Статус задания будет **Отмена** до тех пор, пока служба оптимизации планирования не подтвердит, что задание отменено. Затем статус будет изменен на **Отменено**.

> [!NOTE]
> Чтобы просмотреть изменения статуса, необходимо обновить страницу, нажав кнопку **Обновить**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор оптимизации планирования](planning-optimization-overview.md)

[Начало работы с оптимизацией планирования](get-started.md)

[Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md)

[Просмотр журнала плана и журналов планирования](plan-history-logs.md)

[Применение фильтров к плану](plan-filters.md)