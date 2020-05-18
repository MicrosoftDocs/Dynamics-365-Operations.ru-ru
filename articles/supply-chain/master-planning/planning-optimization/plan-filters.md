---
title: Применение фильтров к плану
description: В этой теме объясняется, как использовать фильтры для плана, в котором используются функции оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ddf9934965bd06ec805731a1cc1a667846fa180
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323424"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="c539f-103">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="c539f-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c539f-104">При использовании функции оптимизации планирования можно применить фильтр к плану.</span><span class="sxs-lookup"><span data-stu-id="c539f-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="c539f-105">**Фильтр плана** всегда будет применяться во время выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="c539f-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="c539f-106">**Фильтр плана** полезен, когда требуется ограничить план определенной группой номенклатур и убедиться в том, что никакие другие номенклатуры не включены как часть результирующего сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="c539f-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="c539f-107">Если **фильтр плана** применяется и фильтр времени выполнения также применяется во время выполнения сводного планирования, то в процесс планирования включаются только пересечения двух фильтров.</span><span class="sxs-lookup"><span data-stu-id="c539f-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="c539f-108">**Фильтр плана** можно открыть из **Сводные планы**, когда используется оптимизация планирования.</span><span class="sxs-lookup"><span data-stu-id="c539f-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c539f-109">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="c539f-109">Example scenario</span></span>

<span data-ttu-id="c539f-110">Фильтр плана включает в себя номенклатуры A, B и C. Сводное планирование затем выполняется для одного и того же плана, но применяются разные фильтры времени выполнения:</span><span class="sxs-lookup"><span data-stu-id="c539f-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="c539f-111">**Фильтр времени выполнения, включающий номенклатуру D:** номенклатуры не планируются, так как между фильтром плана и фильтром времени выполнения не существует пересечения.</span><span class="sxs-lookup"><span data-stu-id="c539f-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="c539f-112">**Фильтр времени выполнения, включающий номенклатуру A и D:** только номенклатура A включается в выполнение планирования, так как номенклатура D не является частью фильтра плана.</span><span class="sxs-lookup"><span data-stu-id="c539f-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="c539f-113">**Фильтр времени выполнения, включающий номенклатуру B:** только номенклатура B включается в выполнение планирования и результат предыдущего планирования для номенклатуры A сохраняется.</span><span class="sxs-lookup"><span data-stu-id="c539f-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="c539f-114">**Фильтр времени выполнения, включающий все номенклатуры (пустой фильтр):** номенклатуры A, B и C включаются в выполнение планирования, а результаты предыдущего планирования для номенклатур A и B перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="c539f-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="c539f-115">Не следует задавать фильтр плана в плане, который выбран в качестве **Текущий динамический сводный план** на странице **Параметры сводного планирования**.</span><span class="sxs-lookup"><span data-stu-id="c539f-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="c539f-116">В противном случае динамический сводный план будет ограничиваться отфильтрованными номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="c539f-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="c539f-117">Например, если нетто-потребности обновляются для номенклатуры, которая не является частью фильтра плана, результаты создаваться не будут.</span><span class="sxs-lookup"><span data-stu-id="c539f-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c539f-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c539f-118">Related resources</span></span>

[<span data-ttu-id="c539f-119">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="c539f-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c539f-120">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="c539f-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c539f-121">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="c539f-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c539f-122">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="c539f-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c539f-123">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="c539f-123">Cancel a planning job</span></span>](cancel-planning-job.md)
