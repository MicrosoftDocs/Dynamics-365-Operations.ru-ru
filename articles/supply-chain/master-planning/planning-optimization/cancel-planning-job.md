---
title: Отмена задания планирования
description: В этой теме объясняется, как отменить активное задание планирования, в котором используются функции оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774040"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="332c9-103">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="332c9-103">Cancel a planning job</span></span>

<span data-ttu-id="332c9-104">В Microsoft Dynamics 365 Supply Chain Management можно отменить активное задание планирования, в котором используются функции оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="332c9-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="332c9-105">Чтобы отменить активное задание планирования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="332c9-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="332c9-106">Только активные задания могут быть отменены.</span><span class="sxs-lookup"><span data-stu-id="332c9-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="332c9-107">Перейдите **Сводное планирование \> Настройка \> Планы**.</span><span class="sxs-lookup"><span data-stu-id="332c9-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="332c9-108">Выберите соответствующий план для выполнения планирования.</span><span class="sxs-lookup"><span data-stu-id="332c9-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="332c9-109">Выберите **История**.</span><span class="sxs-lookup"><span data-stu-id="332c9-109">Select **History**.</span></span>
4. <span data-ttu-id="332c9-110">Выбор задания планирования для отмены.</span><span class="sxs-lookup"><span data-stu-id="332c9-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="332c9-111">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="332c9-111">Select **Cancel**.</span></span>

<span data-ttu-id="332c9-112">Статус задания будет **Отмена** до тех пор, пока служба оптимизации планирования не подтвердит, что задание отменено.</span><span class="sxs-lookup"><span data-stu-id="332c9-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="332c9-113">Затем статус будет изменен на **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="332c9-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="332c9-114">Чтобы просмотреть изменения статуса, необходимо обновить страницу, нажав кнопку **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="332c9-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="332c9-115">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="332c9-115">Related resources</span></span>

[<span data-ttu-id="332c9-116">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="332c9-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="332c9-117">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="332c9-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="332c9-118">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="332c9-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="332c9-119">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="332c9-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="332c9-120">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="332c9-120">Apply filters to a plan</span></span>](plan-filters.md)
