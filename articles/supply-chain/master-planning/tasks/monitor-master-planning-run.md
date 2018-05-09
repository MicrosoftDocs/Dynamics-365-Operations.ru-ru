--- 
title: "Мониторинг выполнения сводного планирования"
description: "Планировщик производства хочет просмотреть, выполняется ли сводное планирование."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 550e2de01187d889ef968a4ff6828f93bb44a8a1
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="18957-103">Мониторинг выполнения сводного планирования</span><span class="sxs-lookup"><span data-stu-id="18957-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18957-104">Планировщик производства хочет просмотреть, выполняется ли сводное планирование.</span><span class="sxs-lookup"><span data-stu-id="18957-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="18957-105">Для выполнения этой процедуры используйте компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="18957-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="18957-106">Запуск сводного планирования</span><span class="sxs-lookup"><span data-stu-id="18957-106">Run master planning</span></span>
1. <span data-ttu-id="18957-107">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="18957-107">Click Master planning.</span></span>
    * <span data-ttu-id="18957-108">Эти сведения можно просмотреть на панели мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18957-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="18957-109">В поле "План" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="18957-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="18957-110">Пример: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="18957-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="18957-111">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="18957-111">Click Run.</span></span>
4. <span data-ttu-id="18957-112">Выберите значение "Да" в поле "Отслеживать время обработки".</span><span class="sxs-lookup"><span data-stu-id="18957-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="18957-113">Если поле уже выбрано, пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="18957-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="18957-114">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="18957-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="18957-115">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="18957-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="18957-116">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="18957-116">Click Filter.</span></span>
8. <span data-ttu-id="18957-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="18957-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="18957-118">Пометьте строку, в которой поле = код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="18957-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="18957-119">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="18957-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="18957-120">Пример: T0001</span><span class="sxs-lookup"><span data-stu-id="18957-120">Example: T0001</span></span>  
10. <span data-ttu-id="18957-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="18957-121">Click OK.</span></span>
11. <span data-ttu-id="18957-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="18957-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="18957-123">Мониторинг выполнения сводного планирования</span><span class="sxs-lookup"><span data-stu-id="18957-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="18957-124">Щелкните "История".</span><span class="sxs-lookup"><span data-stu-id="18957-124">Click History.</span></span>
2. <span data-ttu-id="18957-125">Щелкните Запросы.</span><span class="sxs-lookup"><span data-stu-id="18957-125">Click Inquiries.</span></span>
3. <span data-ttu-id="18957-126">Щелкните "Длительность задачи процесса".</span><span class="sxs-lookup"><span data-stu-id="18957-126">Click Process task duration.</span></span>
4. <span data-ttu-id="18957-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="18957-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18957-128">Для каждой номенклатуры можно просмотреть, сколько времени необходимого для выполнения каждого шага планирования.</span><span class="sxs-lookup"><span data-stu-id="18957-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


