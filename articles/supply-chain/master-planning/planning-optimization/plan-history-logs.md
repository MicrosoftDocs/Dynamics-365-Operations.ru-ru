---
title: Просмотр журнала плана и журналов планирования
description: В этой теме объясняется, как просматривать историю заданий планирования, которые запускаются функцией оптимизации планирования.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187255"
---
# <a name="view-plan-history-and-planning-logs"></a>Просмотр журнала плана и журналов планирования

[!include [banner](../../includes/banner.md)]

В этой теме объясняется, как просматривать историю заданий планирования, которые запускаются функцией оптимизации планирования в Microsoft Dynamics 365 Supply Chain Management.

Чтобы просмотреть историю плана, откройте план, перейдя **Сводное планирование** \> **Настройка** \> **Планы** \> **Сводные планы** и выбрав **История**. В истории перечислены все задания для выбранного плана. Список включает завершенные и активные задания.

История заданий для запусков сводного планирования оптимизации планирования сохраняет не более 60 записей на каждый сводный план. При каждом запуске нового расчета сводного планирования удаляется запись с самой ранней датой создания плана.

В дополнение к просмотру времени начала и статуса заданий можно просмотреть журнал для конкретного задания. Журнал содержит дополнительные сведения и предупреждения. Журнал есть не для всех заданий. Чтобы просмотреть журнал для задания, выберите **Журнал**. Записи журнала хранятся только в течение 30 дней после даты завершения задания, после чего они будут автоматически удалены.

## <a name="related-resources"></a>Связанные ресурсы

- [Обзор оптимизации планирования](planning-optimization-overview.md)
- [Начало работы с оптимизацией планирования](get-started.md)
- [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md)
- [Применение фильтров к плану](plan-filters.md)
- [Отмена задания планирования](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]