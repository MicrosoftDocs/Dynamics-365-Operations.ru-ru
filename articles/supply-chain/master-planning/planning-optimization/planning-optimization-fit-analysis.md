---
title: Анализ пригодности оптимизации планирования
description: В этой теме объясняется, как проверить текущую настройку и данные с учетом возможностей функции оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
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
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774038"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="7e4e3-103">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="7e4e3-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="7e4e3-104">Чтобы узнать, насколько совместима текущая настройка и данные с функциями оптимизации планирования, перейдите **Сводное планирование** \> **Настройка** \> **Анализ пригодности оптимизации планирования**, а затем выберите команду **Выполнить анализ**.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="7e4e3-105">Если при анализе обнаружены несоответствия, они указываются на той же странице.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="7e4e3-106">(Для выполнения анализа может потребоваться несколько минут.)</span><span class="sxs-lookup"><span data-stu-id="7e4e3-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="7e4e3-107">Если обнаружены несоответствия, можно продолжить использовать оптимизацию планирования.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="7e4e3-108">В результатах анализа пригодности появятся места, где служба планирования не принимает текущие настройки.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="7e4e3-109">Другими словами, показаны места, в которых некоторые процессы могут быть пропущены или не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="7e4e3-110">Результаты анализа: пример 1</span><span class="sxs-lookup"><span data-stu-id="7e4e3-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="7e4e3-111">**Функция:** производство</span><span class="sxs-lookup"><span data-stu-id="7e4e3-111">**Feature:** Production</span></span>
- <span data-ttu-id="7e4e3-112">**Проблема:** номенклатуры с уровнем спецификации больше нуля: 56</span><span class="sxs-lookup"><span data-stu-id="7e4e3-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="7e4e3-113">**Объяснение:** анализ пригодности обнаружил 56 номенклатур с настройкой спецификации для производства.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="7e4e3-114">Поскольку текущая версия оптимизации планирования не поддерживает производство, оптимизация планирования создаст спланированные заказы на покупку вместо спланированных производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="7e4e3-115">Кроме того, будет показано предупреждение, в котором перечисляются затрагиваемые номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="7e4e3-116">Результаты анализа: пример 2</span><span class="sxs-lookup"><span data-stu-id="7e4e3-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="7e4e3-117">**Функция:** действия</span><span class="sxs-lookup"><span data-stu-id="7e4e3-117">**Feature:** Actions</span></span>
- <span data-ttu-id="7e4e3-118">**Проблема:** группы покрытия с включенным расчетом действий: 6</span><span class="sxs-lookup"><span data-stu-id="7e4e3-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="7e4e3-119">**Объяснение:** анализ пригодности нашел шесть групп покрытия, в которых был включен расчет действий.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="7e4e3-120">Поскольку текущая версия оптимизации планирования не поддерживает действия, никакие действия при сводном планировании создаваться не будут.</span><span class="sxs-lookup"><span data-stu-id="7e4e3-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="7e4e3-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e4e3-121">Related resources</span></span>

[<span data-ttu-id="7e4e3-122">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="7e4e3-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="7e4e3-123">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="7e4e3-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="7e4e3-124">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="7e4e3-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="7e4e3-125">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="7e4e3-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="7e4e3-126">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="7e4e3-126">Cancel a planning job</span></span>](cancel-planning-job.md)
