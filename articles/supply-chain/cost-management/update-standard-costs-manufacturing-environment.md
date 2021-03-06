---
title: Обновление стандартных затрат в производственной среде
description: Эта статья содержит рекомендации по обновлению стандартных затрат в производственной среде.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66d08888e426c55fc775a1f2505772bca45e7802
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842137"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Обновление стандартных затрат в производственной среде

[!include [banner](../includes/banner.md)]

Эта статья содержит рекомендации по обновлению стандартных затрат в производственной среде. 

Обновления могут отражать новые номенклатуры, категории затрат или формулы расчета косвенных затрат. Они могут отражать также исправления и изменения затрат. Тип обновления будет определять действия, необходимые для обновления стандартных затрат, что иллюстрируется следующими примерами.

-   Введите ожидаемые изменения стандартных затрат для приобретенных номенклатур, а затем измените статус записей затрат на номенклатуру (на **активно**) на соответствующую дату. Но не перерассчитывайте затраты на произведенные номенклатуры, в которых используются приобретенные номенклатуры.
-   Введите стандартные затраты для новой приобретенной номенклатуры, но не перерассчитывайте затраты на произведенные номенклатуры с версией спецификации, содержащей новую приобретенную номенклатуру как компонент.
-   Исправьте или измените затраты на приобретенную номенклатуру или измените группу затрат, назначенную приобретенной номенклатуре, и рассчитайте затраты на все произведенные номенклатуры с версией спецификации, которая содержит приобретенную номенклатуру как компонент.
-   Измените затраты для категории затрат и рассчитайте затраты на все произведенные номенклатуры с версией маршрута, содержащей операции маршрута, которые используют категорию затрат.
-   Измените категории затрат, связанные с операциями маршрутизации, или группу затрат, связанные с категориями затрат. Затем рассчитайте затраты на все произведенные номенклатуры с версией маршрута, содержащей операции маршрута, которые используют категорию затрат.
-   Измените формулу расчета косвенных затрат и рассчитайте затраты для всех произведенных номенклатур, на которые влияет это изменение.
-   Измените или добавьте производственный узел для произведенной номенклатуры и рассчитайте затраты для произведенной номенклатуры для этого узла.
-   Рассчитайте (или перерассчитайте) затраты для произведенной номенклатуры и перерассчитайте затраты для всех произведенных номенклатур с версией спецификации, содержащей произведенную номенклатуру как компонент.
-   Рассчитайте затраты для новой произведенной номенклатуры на основе сведений о ее определенной, утвержденной и активной спецификации и о маршруте.

Каждый пример требует тщательного изучения способа обновления стандартных затрат.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]