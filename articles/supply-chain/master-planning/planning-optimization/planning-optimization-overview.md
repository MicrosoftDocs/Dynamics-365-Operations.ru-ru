---
title: Обзор оптимизации планирования
description: Этот раздел содержит обзор возможностей оптимизации планирования.
author: ChristianRytt
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 5ecfa8ac4db050ee1e38f3b420d81beba19b9409
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812963"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="d018f-103">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="d018f-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d018f-104">Надстройка оптимизации планирования для Microsoft Dynamics 365 Supply Chain Management включает вычисление сводного планирования вне Dynamics 365 Supply Chain Management и соответствующей базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d018f-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="d018f-105">Преимущества, связанные с функциональными возможностями оптимизации планирования, включают улучшенную производительность и минимальное воздействие на базу данных SQL во время выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="d018f-106">Быстрое планирование может выполняться даже во время работы в офисе, чтобы планировщики могли немедленно реагировать на изменения спроса или параметров.</span><span class="sxs-lookup"><span data-stu-id="d018f-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="d018f-107">Для использования оптимизации планирования необходимо установить надстройку оптимизации планирования из проекта в Microsoft Dynamics Lifecycle Services (LCS) и включить функцию оптимизации планирования в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d018f-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="d018f-108">Дополнительные сведения см. в разделе [Начало работы с оптимизацией планирования](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="d018f-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="d018f-109">На следующем рисунке показано преимущество выполнения оптимизации планирования в течение часов работы в офисе.</span><span class="sxs-lookup"><span data-stu-id="d018f-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Преимущества выполнения оптимизации планирования в течение часов работы в офисе](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="d018f-111">Улучшение производительности</span><span class="sxs-lookup"><span data-stu-id="d018f-111">Improved performance</span></span>

<span data-ttu-id="d018f-112">Оптимизация планирования может использоваться в сценариях, в которых используются продолжительные сводные планы.</span><span class="sxs-lookup"><span data-stu-id="d018f-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="d018f-113">Она разработана специально для очень быстрых вычислений очень больших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="d018f-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="d018f-114">Поскольку она создана как сверхмасштабируемая многоклиентская служба, несколько экземпляров могут одновременно работать вместе для вычисления плана.</span><span class="sxs-lookup"><span data-stu-id="d018f-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="d018f-115">Кроме того, служба планирования снимает загрузку сводного планирования с вашей системы и работает с потоком данных, что минимизирует нагрузку на сервер.</span><span class="sxs-lookup"><span data-stu-id="d018f-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="d018f-116">Оптимизация планирования может помочь в достижении следующих целей:</span><span class="sxs-lookup"><span data-stu-id="d018f-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="d018f-117">Повышение производительности планирования за счет сокращения времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d018f-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="d018f-118">Снижение воздействия на другие процессы в ходе выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="d018f-119">Выполнение более частого планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-119">Do more frequent planning runs.</span></span> <span data-ttu-id="d018f-120">(Вы не ограничены ежедневными выполнениями.)</span><span class="sxs-lookup"><span data-stu-id="d018f-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="d018f-121">Уверенность, что будущее развитие бизнеса не перегрузит систему планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="d018f-122">Архитектура и поток данных</span><span class="sxs-lookup"><span data-stu-id="d018f-122">Architecture and data flow</span></span>

<span data-ttu-id="d018f-123">При установке надстройки оптимизации планирования из LCS устанавливается безопасное подключение к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="d018f-124">Служба находится в той же стране или регионе центра обработки данных, что и связанный экземпляр Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d018f-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="d018f-125">После настройки оптимизации планирования при выполнении сводного планирования справочник и данные проводок отправляются из Supply Chain Management в службу оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="d018f-126">При удалении надстройки оптимизации планирования все соответствующие данные в службе оптимизации планирования удаляются.</span><span class="sxs-lookup"><span data-stu-id="d018f-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="d018f-127">Поток данных высокого уровня для выполнения пересоздания</span><span class="sxs-lookup"><span data-stu-id="d018f-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="d018f-128">Клиент Supply Chain Management отправляет сигнал для запроса выполнения планирования из оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="d018f-129">Оптимизация планирования запрашивает необходимые данные через интегрированный соединитель.</span><span class="sxs-lookup"><span data-stu-id="d018f-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="d018f-130">База данных SQL отправляет запрашиваемую информацию о настройке, справочнике и данных проводок в оптимизацию планирования через соединитель.</span><span class="sxs-lookup"><span data-stu-id="d018f-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="d018f-131">Соединитель передает информацию между Supply Chain Management и службой оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="d018f-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="d018f-132">Служба оптимизации планирования удерживает данные, имеющие отношение к планированию в памяти, и выполняет необходимые вычисления.</span><span class="sxs-lookup"><span data-stu-id="d018f-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="d018f-133">Результат планирования отсылается в базу данных Supply Chain Management через соединитель.</span><span class="sxs-lookup"><span data-stu-id="d018f-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="d018f-134">Результаты включают в себя такие сведения, как спланированные заказы и сведения о фиксации.</span><span class="sxs-lookup"><span data-stu-id="d018f-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="d018f-135">Оптимизация планирования отправляет сигнал в Supply Chain Management, указывая, что выполнение планирования завершено.</span><span class="sxs-lookup"><span data-stu-id="d018f-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="d018f-136">Она также отправляет все необходимые сообщения и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="d018f-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="d018f-137">На следующем рисунке показан поток данных.</span><span class="sxs-lookup"><span data-stu-id="d018f-137">The following illustration shows the data flow.</span></span>

![Поток данных для выполнения пересоздания](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="d018f-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d018f-139">Related resources</span></span>

[<span data-ttu-id="d018f-140">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="d018f-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="d018f-141">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="d018f-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="d018f-142">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="d018f-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="d018f-143">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="d018f-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="d018f-144">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="d018f-144">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]