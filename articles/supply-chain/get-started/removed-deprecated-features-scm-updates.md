---
title: Удаленные или устаревшие функции Dynamics 365 Supply Chain Management
description: В этом разделе описываются возможности, который удалены или которые планируется удалить в Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597124"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Удаленные или устаревшие функции Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Этот раздел будет обновлен в соответствии с документированием новых удаленных или устаревших функций для Dynamics 365 Supply Chain Management.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.

> [!NOTE]
> Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Функции, удаленные или устаревшие в выпуске Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Для сценариев распределения используйте встроенный механизм сводного планирования Supply Chain Management.

|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Для повышения производительности и минимизации нагрузки на базу данных SQL во время сводного планирования, встроенный механизм сводного планирования Supply Chain Management заменяется оптимизацией планирования. Оптимизация планирования позволяет быстро планировать даже в рабочие часы. Это позволяет планировщикам быстро реагировать на изменения в параметрах спроса или планирования. |
| **Заменена другой функцией?**   | Да, оптимизация планирования заменит существующий встроенный механизм сводного планирования Supply Chain Management. |
| **Затрагиваемые области продукта**         | Supply Chain Management — сводное планирование |
| **Вариант развертывания**              | Только облако. Оптимизация планирования не поддерживается в локальном развертывании. |
| **Состояние**                         | Устарело. В апреле 2021 сценарии распределения больше не будут поддерживаться встроенным механизмом сводного планирования Dynamics 365 Supply Chain Management. Для сценариев распределения клиенты должны использовать оптимизацию планирования при расчетах сводного планирования. Дополнительные сведения см. в разделе [Документация оптимизации планирования](https://go.microsoft.com/fwlink/?linkid=2105830). Клиенты с локальным развертыванием Dynamics 365 Supply Chain Management могут и дальше использовать механизм сводного планирования Supply Chain Management для сценариев распределения после апреля 2021 года. Однако эти функции больше не будут улучшаться. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Предыдущие объявления об удаленных или устаревших функциях

Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
