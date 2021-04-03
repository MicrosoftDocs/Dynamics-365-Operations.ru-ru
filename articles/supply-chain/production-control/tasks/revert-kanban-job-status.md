---
title: Вернуть статус задания канбана
description: Эта процедура направлена на отмену неправильных статусов заданий канбана.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94618494b9c338ed27b2558c91dc662c853d3cda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261102"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="f43f1-103">Вернуть статус задания канбана</span><span class="sxs-lookup"><span data-stu-id="f43f1-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f43f1-104">Эта процедура направлена на отмену неправильных статусов заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="f43f1-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="f43f1-105">Это бывает полезно в случае, когда если оператор станка обновляет неправильное задание или настраивает неправильный статус по ошибке.</span><span class="sxs-lookup"><span data-stu-id="f43f1-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="f43f1-106">В этой процедуре задание канбана регистрируется как подготовленное по ошибке, и статус возвращается к предыдущему значению.</span><span class="sxs-lookup"><span data-stu-id="f43f1-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="f43f1-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="f43f1-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f43f1-108">Эта процедура предназначена для начальника цеха или оператор станка в компании, работающей в соответствии с принципами бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="f43f1-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="f43f1-109">Открытие панели процессов для производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="f43f1-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="f43f1-110">Перейдите на доску канбана для заданий обработки.</span><span class="sxs-lookup"><span data-stu-id="f43f1-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="f43f1-111">В поле "Производственная ячейка" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f43f1-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="f43f1-112">Выберите производственную ячейку 1260.</span><span class="sxs-lookup"><span data-stu-id="f43f1-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="f43f1-113">Подготовка задания канбана</span><span class="sxs-lookup"><span data-stu-id="f43f1-113">Prepare kanban job</span></span>
1. <span data-ttu-id="f43f1-114">Щелкните "Подготовить".</span><span class="sxs-lookup"><span data-stu-id="f43f1-114">Click Prepare.</span></span>
    * <span data-ttu-id="f43f1-115">Если не удается нажать "Подготовить", поскольку эта функция неактивна, убедитесь, что выбранное задание канбана имеет статус "Запланировано", о чем свидетельствует пустой значком канбана.</span><span class="sxs-lookup"><span data-stu-id="f43f1-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="f43f1-116">Если при подготовке происходит сбой, убедитесь, что доступны все материалы в отгрузочной накладной.</span><span class="sxs-lookup"><span data-stu-id="f43f1-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="f43f1-117">Выберите подготовленное задание из списка.</span><span class="sxs-lookup"><span data-stu-id="f43f1-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="f43f1-118">Выберите первое задание, которое вы только что подготовили.</span><span class="sxs-lookup"><span data-stu-id="f43f1-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="f43f1-119">Обратите внимание, что задание имеет статус "Подготовлено", на что указывает треугольник внутри значка канбана.</span><span class="sxs-lookup"><span data-stu-id="f43f1-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="f43f1-120">Возврат статуса подготовленного задания канбана</span><span class="sxs-lookup"><span data-stu-id="f43f1-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="f43f1-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f43f1-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f43f1-122">Выберите первое задание, которое было подготовлено.</span><span class="sxs-lookup"><span data-stu-id="f43f1-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="f43f1-123">В области действий щелкните "Производство".</span><span class="sxs-lookup"><span data-stu-id="f43f1-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="f43f1-124">Щелкните "Вернуть статус".</span><span class="sxs-lookup"><span data-stu-id="f43f1-124">Click Revert status.</span></span>
    * <span data-ttu-id="f43f1-125">Можно использовать другое правило канбана, если соблюдаются следующие условия:  — стратегия пополнения одинакова для обоих правил.</span><span class="sxs-lookup"><span data-stu-id="f43f1-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="f43f1-126">- Версия производственного потока одинакова для обоих правил.</span><span class="sxs-lookup"><span data-stu-id="f43f1-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="f43f1-127">- Продукт, который поставляется, одинаков для обоих правил.</span><span class="sxs-lookup"><span data-stu-id="f43f1-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="f43f1-128">- Все последующие мероприятия, настроенные для последнего действия правил канбана, должны быть одинаковыми для обоих правил.</span><span class="sxs-lookup"><span data-stu-id="f43f1-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="f43f1-129">- Для обоих правил должны быть настроены одинаковые поставленные складские аналитики.</span><span class="sxs-lookup"><span data-stu-id="f43f1-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="f43f1-130">- Статус единицы обработки должен быть "Не назначено".</span><span class="sxs-lookup"><span data-stu-id="f43f1-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="f43f1-131">- Конфигурация для событий канбанов должна быть одинаковой.</span><span class="sxs-lookup"><span data-stu-id="f43f1-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="f43f1-132">Убедитесь, что новый статус — "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="f43f1-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="f43f1-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f43f1-133">Click OK.</span></span>
5. <span data-ttu-id="f43f1-134">В списке снимите пометку выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="f43f1-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="f43f1-135">Выберите то же задание.</span><span class="sxs-lookup"><span data-stu-id="f43f1-135">Select the same job.</span></span>  
    * <span data-ttu-id="f43f1-136">Обратите внимание, что статус задания для задания канбана вернулся в значение "Запланировано", на что указывает пустой значок канбана.</span><span class="sxs-lookup"><span data-stu-id="f43f1-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]