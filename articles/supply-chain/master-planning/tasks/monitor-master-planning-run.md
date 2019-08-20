---
title: Мониторинг выполнения сводного планирования
description: Планировщик производства хочет просмотреть, выполняется ли сводное планирование.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845122"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="0e48b-103">Мониторинг выполнения сводного планирования</span><span class="sxs-lookup"><span data-stu-id="0e48b-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e48b-104">Планировщик производства хочет просмотреть, выполняется ли сводное планирование.</span><span class="sxs-lookup"><span data-stu-id="0e48b-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="0e48b-105">Для выполнения этой процедуры используйте компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="0e48b-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="0e48b-106">Запуск сводного планирования</span><span class="sxs-lookup"><span data-stu-id="0e48b-106">Run master planning</span></span>
1. <span data-ttu-id="0e48b-107">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="0e48b-107">Click Master planning.</span></span>
    * <span data-ttu-id="0e48b-108">Эти сведения можно просмотреть на панели мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e48b-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="0e48b-109">В поле "План" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0e48b-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="0e48b-110">Пример: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="0e48b-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="0e48b-111">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="0e48b-111">Click Run.</span></span>
4. <span data-ttu-id="0e48b-112">Выберите значение "Да" в поле "Отслеживать время обработки".</span><span class="sxs-lookup"><span data-stu-id="0e48b-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="0e48b-113">Если поле уже выбрано, пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="0e48b-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="0e48b-114">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="0e48b-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="0e48b-115">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="0e48b-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="0e48b-116">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="0e48b-116">Click Filter.</span></span>
8. <span data-ttu-id="0e48b-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="0e48b-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0e48b-118">Пометьте строку, в которой поле = код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0e48b-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="0e48b-119">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0e48b-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="0e48b-120">Пример: T0001</span><span class="sxs-lookup"><span data-stu-id="0e48b-120">Example: T0001</span></span>  
10. <span data-ttu-id="0e48b-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0e48b-121">Click OK.</span></span>
11. <span data-ttu-id="0e48b-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0e48b-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="0e48b-123">Мониторинг выполнения сводного планирования</span><span class="sxs-lookup"><span data-stu-id="0e48b-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="0e48b-124">Щелкните "История".</span><span class="sxs-lookup"><span data-stu-id="0e48b-124">Click History.</span></span>
2. <span data-ttu-id="0e48b-125">Щелкните Запросы.</span><span class="sxs-lookup"><span data-stu-id="0e48b-125">Click Inquiries.</span></span>
3. <span data-ttu-id="0e48b-126">Щелкните "Длительность задачи процесса".</span><span class="sxs-lookup"><span data-stu-id="0e48b-126">Click Process task duration.</span></span>
4. <span data-ttu-id="0e48b-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0e48b-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0e48b-128">Для каждой номенклатуры можно просмотреть, сколько времени необходимого для выполнения каждого шага планирования.</span><span class="sxs-lookup"><span data-stu-id="0e48b-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

