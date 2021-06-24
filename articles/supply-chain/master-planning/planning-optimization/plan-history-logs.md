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
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="41a8d-103">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="41a8d-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41a8d-104">В этой теме объясняется, как просматривать историю заданий планирования, которые запускаются функцией оптимизации планирования в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="41a8d-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="41a8d-105">Чтобы просмотреть историю плана, откройте план, перейдя **Сводное планирование** \> **Настройка** \> **Планы** \> **Сводные планы** и выбрав **История**.</span><span class="sxs-lookup"><span data-stu-id="41a8d-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="41a8d-106">В истории перечислены все задания для выбранного плана.</span><span class="sxs-lookup"><span data-stu-id="41a8d-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="41a8d-107">Список включает завершенные и активные задания.</span><span class="sxs-lookup"><span data-stu-id="41a8d-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="41a8d-108">История заданий для запусков сводного планирования оптимизации планирования сохраняет не более 60 записей на каждый сводный план.</span><span class="sxs-lookup"><span data-stu-id="41a8d-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="41a8d-109">При каждом запуске нового расчета сводного планирования удаляется запись с самой ранней датой создания плана.</span><span class="sxs-lookup"><span data-stu-id="41a8d-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="41a8d-110">В дополнение к просмотру времени начала и статуса заданий можно просмотреть журнал для конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="41a8d-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="41a8d-111">Журнал содержит дополнительные сведения и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="41a8d-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="41a8d-112">Журнал есть не для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="41a8d-112">Not all jobs have a log.</span></span> <span data-ttu-id="41a8d-113">Чтобы просмотреть журнал для задания, выберите **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="41a8d-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="41a8d-114">Записи журнала хранятся только в течение 30 дней после даты завершения задания, после чего они будут автоматически удалены.</span><span class="sxs-lookup"><span data-stu-id="41a8d-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="41a8d-115">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="41a8d-115">Related resources</span></span>

- [<span data-ttu-id="41a8d-116">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="41a8d-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="41a8d-117">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="41a8d-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="41a8d-118">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="41a8d-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="41a8d-119">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="41a8d-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="41a8d-120">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="41a8d-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]