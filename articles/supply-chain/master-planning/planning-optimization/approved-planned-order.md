---
title: Просмотр, управление и утверждение спланированных заказов
description: В этой теме приводятся сведения о том, как просматривать, управлять и утверждать спланированные заказы при оптимизации планирования.
author: ChristianRytt
ms.date: 04/07/2021
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
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935665"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="81478-103">Просмотр, управление и утверждение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="81478-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81478-104">В этой теме приводятся сведения о том, как просматривать, управлять и утверждать спланированные заказы при оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="81478-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="81478-105">Просмотр и управление спланированными заказами</span><span class="sxs-lookup"><span data-stu-id="81478-105">View and manage planned orders</span></span>

<span data-ttu-id="81478-106">Можно просматривать спланированные заказы и управлять ими на любой странице списка спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="81478-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="81478-107">Перейдите к одному из следующих мест, в зависимости от типа спланированных заказов, с которыми необходимо работать:</span><span class="sxs-lookup"><span data-stu-id="81478-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="81478-108">Сводное планирование \> Рабочие области \> Сводное планирование</span><span class="sxs-lookup"><span data-stu-id="81478-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="81478-109">Сводное планирование \> Сводное планирование \> Спланированные заказы</span><span class="sxs-lookup"><span data-stu-id="81478-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="81478-110">Управление производством \> Производственные заказы \> Спланированные производственные заказы</span><span class="sxs-lookup"><span data-stu-id="81478-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="81478-111">Закупки и источники \> Заказы на покупку \> Спланированные заказы на покупку</span><span class="sxs-lookup"><span data-stu-id="81478-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="81478-112">Управление запасами \> Входящие заказы \> Спланированные перемещения</span><span class="sxs-lookup"><span data-stu-id="81478-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="81478-113">Управление запасами \> Исходящие заказы \> Спланированные перемещения</span><span class="sxs-lookup"><span data-stu-id="81478-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="81478-114">Просмотр и изменение статуса запланированных заказов</span><span class="sxs-lookup"><span data-stu-id="81478-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="81478-115">Можно использовать поле **Статус** для каждого спланированного заказа, чтобы отслеживать ход выполнения работ или изменять способ обработки спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="81478-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="81478-116">Доступны следующие значения **Статус**:</span><span class="sxs-lookup"><span data-stu-id="81478-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="81478-117">**Не обработано** — когда система сводного планирования создает спланированные заказы, им дается этот статус.</span><span class="sxs-lookup"><span data-stu-id="81478-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="81478-118">Спланированные заказы с этим статусом будут удалены в ходе следующего выполнения планирования.</span><span class="sxs-lookup"><span data-stu-id="81478-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="81478-119">**Завершено** — этот статус указывает, что спланированный заказ был завершен.</span><span class="sxs-lookup"><span data-stu-id="81478-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="81478-120">Если решено не утверждать спланированный заказ, ему можно вручную изменить статус на *Завершено*.</span><span class="sxs-lookup"><span data-stu-id="81478-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="81478-121">Обратите внимание, что значения статуса *Не обработано* и *Завершено* обрабатываются системой одинаково.</span><span class="sxs-lookup"><span data-stu-id="81478-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="81478-122">**Утверждено** — этот статус указывает, что спланированный заказ утвержден для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="81478-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="81478-123">Если необходимо утвердить спланированный заказ, можно изменить статус на *Утверждено*.</span><span class="sxs-lookup"><span data-stu-id="81478-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="81478-124">Если необходимо сохранить изменения, сделанные в спланированном заказе, или если планируется подтвердить спланированный заказ, измените его статус на *Утверждено*.</span><span class="sxs-lookup"><span data-stu-id="81478-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="81478-125">Спланированные заказы со статусом *Утверждено* считаются фиксированными и ожидающими поставки системой сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="81478-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="81478-126">Поэтому они не изменяются и не удаляются в дальнейшем при выполнении сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="81478-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="81478-127">Для достижения этого поведения логика планирования копирует спланированные заказы со статусом *Одобрено* из старой версии плана в новую версию плана во время сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="81478-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="81478-128">Обратите внимание, что спланированные заказы со статусом *Утверждено* рассматриваются как поставки только в рамках указанного сводного плана.</span><span class="sxs-lookup"><span data-stu-id="81478-128">Note that planned orders that have a status of *Approved*\* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="81478-129">Чтобы изменить статус одного спланированного заказа, [откройте страницу списка спланированных заказов](#view-planned-orders), откройте заказ, а затем выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="81478-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="81478-130">На экспресс-вкладке **Общее** измените значение в поле **Статус**.</span><span class="sxs-lookup"><span data-stu-id="81478-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="81478-131">В области действий на вкладке **Спланированный заказ** в группе **Обработка** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="81478-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="81478-132">В области действий выберите **Утвердить**, чтобы отметить заказ как утвержденный.</span><span class="sxs-lookup"><span data-stu-id="81478-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="81478-133">Чтобы изменить статус нескольких спланированных заказов одновременно, [откройте страницу списка спланированных заказов](#view-planned-orders), установите флажок для каждого заказа, который необходимо изменить, а затем выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="81478-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="81478-134">В области действий на вкладке **Спланированный заказ** в группе **Обработка** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="81478-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="81478-135">В области действий выберите **Утвердить**, чтобы отметить заказы как утвержденные.</span><span class="sxs-lookup"><span data-stu-id="81478-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="81478-136">Утверждение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="81478-136">Approve planned orders</span></span>

<span data-ttu-id="81478-137">Утверждение спланированных заказов является необязательным шагом на пути создания подтвержденного заказа из спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="81478-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="81478-138">На следующем рисунке показано, как можно использовать значение **Статус**, которое назначено для каждого спланированного заказа для реализации рабочего процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="81478-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="81478-139">Для реализации процесса утверждения вручную скорректируйте значение **Статус** для каждого спланированного заказа, как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="81478-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Поток спланированного заказа](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="81478-141">Рекомендуется утверждать любые измененные спланированные заказы.</span><span class="sxs-lookup"><span data-stu-id="81478-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="81478-142">В противном случае изменения будут проигнорированы и перезаписаны при следующем выполнении планирования.</span><span class="sxs-lookup"><span data-stu-id="81478-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81478-143">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="81478-143">Additional resources</span></span>

- [<span data-ttu-id="81478-144">Утверждение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="81478-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
