---
title: Процесс выпуска оптимизации планирования и история выпуска
description: В этом разделе приводятся сведения о процессе выпуска и истории выпуска для оптимизации планирования.
author: crytt
ms.date: 7/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 64c8cd3ed6ff522a9ef90831ae502c5d50fbc05816aaa764d2a8e122934fc2bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722399"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Процесс выпуска оптимизации планирования и история выпуска

[!include [banner](../../includes/banner.md)]

Оптимизация планирования обновлений Microsoft на ежемесячной основе. Однако в зависимости от бизнес-требований периодически выпускаются дополнительные обновления для запланированных выпусков.

Каждый выпуск публикуется в отдельных регионах, где доступна оптимизация планирования. Процесс обычно занимает три дня.

При обновлении оптимизации планирования сводное планирование может выполняться немного медленнее, чем обычно.

Среды, в которых используется оптимизация планирования, автоматически получают последний выпуск. Действия пользователя не требуются: служба обновляется автоматически. Однако функциональные возможности критического изменения никогда не передаются автоматически в среды. По умолчанию все изменения, которые считаются критическими, отключаются и должны быть явно включены с помощью [управления функциями](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Поэтому эти изменения не будут отображаться в средах, пока не будет выбрано их включение.

Поскольку уведомления не отображаются при обновлении оптимизации планирования в вашей среде, можно просмотреть заметки о выпуске в следующей таблице, чтобы определить, когда были выпущены изменения и какие функции они ввели. В этой таблице показаны изменения, которые были выпущены для оптимизации планирования, независимо от того, связаны ли эти изменения с функцией в управлении функциями и датой выпуска.

| Изменения | Подробно об управлении функциями | Дата запуска в производство |
|---|---|---|
| <p>Потребности в типе ресурсов для планирования неограниченной мощности</p><p>Эффективность использования ресурсов и эффективность календаря для планирования неограниченной мощности</p><p>Дополнительные сведения см. в разделе [Планирование с бесконечной мощностью](infinite-capacity-planning.md). | <p>Доступно в управлении функциями версии 10.0.20.</p><p>Имя функции: *Планирование неограниченной мощности для оптимизации планирования*</p> | 6 июля 2021 г. |
| Общие улучшения качества | Управление функциями не является обязательным. | 6 июля 2021 г. |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]