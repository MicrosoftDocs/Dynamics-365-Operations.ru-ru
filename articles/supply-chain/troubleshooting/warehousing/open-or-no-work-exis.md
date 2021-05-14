---
title: Невозможно подтвердить отгрузку из-за незавершенной или отсутствующей работы
description: Невозможно подтвердить отгрузку из-за незавершенной или отсутствующей работы
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938540"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="4cc74-103">Невозможно подтвердить отгрузку из-за незавершенной или отсутствующей работы</span><span class="sxs-lookup"><span data-stu-id="4cc74-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="4cc74-104">Код ошибки: WAX515</span><span class="sxs-lookup"><span data-stu-id="4cc74-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="4cc74-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="4cc74-105">Symptoms</span></span>

<span data-ttu-id="4cc74-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="4cc74-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4cc74-107">Не удалось подтвердить отгрузку для загрузки %1, поскольку для данной загрузки должна быть завершена вся работа.</span><span class="sxs-lookup"><span data-stu-id="4cc74-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="4cc74-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="4cc74-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4cc74-109">Причина</span><span class="sxs-lookup"><span data-stu-id="4cc74-109">Cause</span></span>

<span data-ttu-id="4cc74-110">Загрузка или отгрузка в данный момент находится в состоянии, когда подтверждение отгрузки завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="4cc74-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="4cc74-111">Прежде чем можно будет подтвердить отгрузку, для загрузки должна существовать по крайней мере какая-то работа, и вся работа должна иметь статус *Закрыто* или *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="4cc74-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="4cc74-112">Приказ</span><span class="sxs-lookup"><span data-stu-id="4cc74-112">Resolution</span></span>

<span data-ttu-id="4cc74-113">Проверьте связанные заказы на продажу или заказы на перемещение для загрузки или отгрузки и убедитесь, что все соответствующие работы завершены или отменены.</span><span class="sxs-lookup"><span data-stu-id="4cc74-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="4cc74-114">Можно работать с отгрузками и загрузками на нескольких страницах.</span><span class="sxs-lookup"><span data-stu-id="4cc74-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="4cc74-115">В следующих подразделах представлено несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="4cc74-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="4cc74-116">Страница всех загрузок</span><span class="sxs-lookup"><span data-stu-id="4cc74-116">All loads page</span></span>

1. <span data-ttu-id="4cc74-117">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="4cc74-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4cc74-118">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="4cc74-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4cc74-119">В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="4cc74-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="4cc74-120">Проверьте статус каждого кода работы.</span><span class="sxs-lookup"><span data-stu-id="4cc74-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="4cc74-121">Обработка результатов каждого кода работ, у которого нет статуса *Закрыто* или *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="4cc74-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="4cc74-122">Когда у каждого кода работы есть статус *Закрыто* или *Отменено*, повторите попытку для подтверждения отгрузки.</span><span class="sxs-lookup"><span data-stu-id="4cc74-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="4cc74-123">Страница "Все отгрузки"</span><span class="sxs-lookup"><span data-stu-id="4cc74-123">All shipments page</span></span>

1. <span data-ttu-id="4cc74-124">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="4cc74-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="4cc74-125">Выберите отгрузку, которую невозможно подтвердить.</span><span class="sxs-lookup"><span data-stu-id="4cc74-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="4cc74-126">В области действий на вкладке **Отгрузки** в группе **Работа** выберите **Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="4cc74-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="4cc74-127">Проверьте статус каждого кода работы.</span><span class="sxs-lookup"><span data-stu-id="4cc74-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="4cc74-128">Обработка результатов каждого кода работ, у которого нет статуса *Закрыто* или *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="4cc74-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="4cc74-129">Когда у каждого кода работы есть статус *Закрыто* или *Отменено*, повторите попытку для подтверждения отгрузки.</span><span class="sxs-lookup"><span data-stu-id="4cc74-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="4cc74-130">Страница "Все работы"</span><span class="sxs-lookup"><span data-stu-id="4cc74-130">All work page</span></span>

1. <span data-ttu-id="4cc74-131">Перейдите в раздел **Управление складом \> Работа \> Все работы**.</span><span class="sxs-lookup"><span data-stu-id="4cc74-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="4cc74-132">Выбор работу для номера заказа, для которого невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="4cc74-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4cc74-133">В области действий на вкладке **Отгрузка** в группе **Отгрузка** выберите **Подтвердить отгрузку**.</span><span class="sxs-lookup"><span data-stu-id="4cc74-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="4cc74-134">Проверьте статус каждого кода работы.</span><span class="sxs-lookup"><span data-stu-id="4cc74-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="4cc74-135">Обработка результатов каждого кода работ, у которого нет статуса *Закрыто* или *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="4cc74-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="4cc74-136">Когда у каждого кода работы есть статус *Закрыто* или *Отменено*, повторите попытку для подтверждения отгрузки.</span><span class="sxs-lookup"><span data-stu-id="4cc74-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
