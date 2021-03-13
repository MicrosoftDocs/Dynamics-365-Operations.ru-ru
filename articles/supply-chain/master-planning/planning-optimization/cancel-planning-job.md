---
title: Отмена задания планирования
description: В этой теме объясняется, как отменить активное задание планирования, в котором используются функции оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008224"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="4539a-103">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="4539a-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4539a-104">В Microsoft Dynamics 365 Supply Chain Management можно отменить активное задание планирования, в котором используются функции оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="4539a-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="4539a-105">Если в диалоговом окне выбрать **Отмена**, когда задание оптимизации планирования запускается непосредственно из интерфейса пользователя (не в фоновом режиме), это не отменит задания оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="4539a-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="4539a-106">Даже если вы получаете предупреждение, например "операция отменена", вам все равно придется выполнить следующие шаги для отмены задания планирования с оптимизацией планирования.</span><span class="sxs-lookup"><span data-stu-id="4539a-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="4539a-107">Чтобы отменить активное задание планирования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4539a-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="4539a-108">Только активные задания могут быть отменены.</span><span class="sxs-lookup"><span data-stu-id="4539a-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="4539a-109">Перейдите **Сводное планирование \> Настройка \> Планы**.</span><span class="sxs-lookup"><span data-stu-id="4539a-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="4539a-110">Выберите соответствующий план для выполнения планирования.</span><span class="sxs-lookup"><span data-stu-id="4539a-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="4539a-111">Выберите **История**.</span><span class="sxs-lookup"><span data-stu-id="4539a-111">Select **History**.</span></span>
4. <span data-ttu-id="4539a-112">Выбор задания планирования для отмены.</span><span class="sxs-lookup"><span data-stu-id="4539a-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="4539a-113">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="4539a-113">Select **Cancel**.</span></span>

<span data-ttu-id="4539a-114">Статус задания будет **Отмена** до тех пор, пока служба оптимизации планирования не подтвердит, что задание отменено.</span><span class="sxs-lookup"><span data-stu-id="4539a-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="4539a-115">Затем статус будет изменен на **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="4539a-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="4539a-116">Чтобы просмотреть изменения статуса, необходимо обновить страницу, нажав кнопку **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="4539a-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4539a-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4539a-117">Additional resources</span></span>

[<span data-ttu-id="4539a-118">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="4539a-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="4539a-119">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="4539a-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="4539a-120">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="4539a-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="4539a-121">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="4539a-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="4539a-122">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="4539a-122">Apply filters to a plan</span></span>](plan-filters.md)
