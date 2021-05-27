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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="f5cc2-103">Пропущенные параметры поля при копировании групп номенклатурных моделей в другое юридическое лицо</span><span class="sxs-lookup"><span data-stu-id="f5cc2-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="f5cc2-104">Номер статьи базы знаний: 4612800</span><span class="sxs-lookup"><span data-stu-id="f5cc2-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="f5cc2-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="f5cc2-105">Symptoms</span></span>

<span data-ttu-id="f5cc2-106">При копировании групп номенклатурных моделей в другое юридическое лицо (компанию) с помощью сущности *Политики запасов группы номенклатурных моделей*, некоторые параметры полей (например, складская модель и описание) отсутствуют в новой группе моделей в целевом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="f5cc2-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="f5cc2-107">Resolution</span></span>

<span data-ttu-id="f5cc2-108">Чтобы создать полную копию группы номенклатурных моделей для другого юридического лица, необходимо также выбрать и политики запасов группы номенклатурных моделей (`InventInventoryPolicyEntity`), и политики предположения потока затрат (`InventCostFlowAssumptionPolicyEntity`), связанные с группой номенклатурных моделей.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
