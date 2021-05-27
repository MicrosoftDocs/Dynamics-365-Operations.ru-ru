---
title: Пропущенные параметры поля при копировании групп номенклатурных моделей в другое юридическое лицо
description: Параметры поля отсутствуют при копировании групп номенклатурных моделей в другое юридическое лицо.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026842"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Пропущенные параметры поля при копировании групп номенклатурных моделей в другое юридическое лицо

Номер статьи базы знаний: 4612800

## <a name="symptoms"></a>Симптомы

При копировании групп номенклатурных моделей в другое юридическое лицо (компанию) с помощью сущности *Политики запасов группы номенклатурных моделей*, некоторые параметры полей (например, складская модель и описание) отсутствуют в новой группе моделей в целевом юридическом лице.

## <a name="resolution"></a>Приказ

Чтобы создать полную копию группы номенклатурных моделей для другого юридического лица, необходимо также выбрать и политики запасов группы номенклатурных моделей (`InventInventoryPolicyEntity`), и политики предположения потока затрат (`InventCostFlowAssumptionPolicyEntity`), связанные с группой номенклатурных моделей.
