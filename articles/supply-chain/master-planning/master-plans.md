---
title: Обзор сводных планов
description: Используйте разнообразные сводные планы, чтобы поддерживать ежедневную деятельность компании, моделировать различные стратегии планирования, которые вы хотите отслеживать, и реализовывать политику компании, например политику, касающуюся внутренней производительности или удовлетворенности потребителей.
author: t-benebo
ms.date: 05/28/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b3d30d9ef2f08c2cb7b2ca022ff1a816567a247
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468765"
---
# <a name="master-plans-overview"></a>Обзор сводных планов

[!include [banner](../includes/banner.md)]

Используйте разнообразные сводные планы, чтобы поддерживать ежедневную деятельность компании, моделировать различные стратегии планирования, которые вы хотите отслеживать, и реализовывать политику компании, например политику, касающуюся внутренней производительности или удовлетворенности потребителей.

Вы можете настроить сводные планы на странице **Сводные планы**.

Существует два типа планов:

- **Статический план** — при расчете сводного планирования используются текущие данные для формирования плана чистых потребностей. Этот план не изменится до следующего запуска вами компонента сводного планирования или изменения плана вручную. Это оперативный план, который используется различными сотрудниками компании, например закупщиками или составителями планов производства, для принятия решений и выполнения ежедневных операций.
- **Динамический план**. Этот план создается на основе того же плана чистых потребностей, который создается компонентом сводного планирования. В то же время вы можете обновлять динамический план каждый раз при изменении справочника. Это может происходить, например, при создании нового заказа на продажу. Это позволяет вам осуществлять мониторинг изменяющейся сети заказов и доступности номенклатур, не нарушая статический план, которые другие сотрудники используют в своих рабочих процессах.

При желании компания может работать как только с динамическим планом, так и со статическим и динамическим планами одновременно. Также любой сводный план можно изменять так, чтобы он отражал какую-либо стратегию или результат. Ниже приведены примеры.

- Установите более высокие уровни заказов, чтобы избежать отсутствия запасов.
- Установите более долгое резервное время в качестве меры предосторожности при работе с ненадежными поставщиками.

Также можно настроить исходный динамический план, который будет обновляться с учетом нового плана требований каждый раз при выполнении сводного планирования. Вы можете указать эти параметры на странице **Параметры сводного планирования**.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Параметры покрытия](coverage-settings.md)
- [Разделение тактического и оперативного планирования для сводного планирования](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [Сводное планирование: использовать статический и динамический сводные планы или использовать один план?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
