---
title: Невозможно подтвердить отгрузку, поскольку количество превышает процент недопоставки
description: Невозможно подтвердить отгрузку, поскольку количество превышает процент недопоставки
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123827"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="b3d45-103">Невозможно подтвердить отгрузку, поскольку количество превышает процент недопоставки</span><span class="sxs-lookup"><span data-stu-id="b3d45-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="b3d45-104">Код ошибки: WAX1686</span><span class="sxs-lookup"><span data-stu-id="b3d45-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="b3d45-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="b3d45-105">Symptoms</span></span>

<span data-ttu-id="b3d45-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="b3d45-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="b3d45-107">Не удалось подтвердить отгрузку для загрузки %1, так как количество номенклатуры %2 превышает процент, определенный для недопоставки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="b3d45-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="b3d45-109">Причина</span><span class="sxs-lookup"><span data-stu-id="b3d45-109">Cause</span></span>

<span data-ttu-id="b3d45-110">Количество загрузки или отгрузки было частично скомплектовано.</span><span class="sxs-lookup"><span data-stu-id="b3d45-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="b3d45-111">Количество в настоящее время меньше скомплектованного количества на процент, выходящий за пределы разрешенного процента недопоставки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="b3d45-112">Приказ</span><span class="sxs-lookup"><span data-stu-id="b3d45-112">Resolution</span></span>

<span data-ttu-id="b3d45-113">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="b3d45-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="b3d45-114">Задание количества в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-114">Set the load line quantity.</span></span>
- <span data-ttu-id="b3d45-115">Настройка процента недопоставки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="b3d45-116">Задание количества в строке загрузки</span><span class="sxs-lookup"><span data-stu-id="b3d45-116">Set the load line quantity</span></span>

<span data-ttu-id="b3d45-117">Чтобы задать количество в строке загрузки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b3d45-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="b3d45-118">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b3d45-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b3d45-119">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="b3d45-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="b3d45-120">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="b3d45-121">На экспресс-вкладке **Сведения строки** выберите **Заказ**.</span><span class="sxs-lookup"><span data-stu-id="b3d45-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="b3d45-122">В поле **Количество** установите значение для скомплектованного количества (то есть **Созданное количество работы**), чтобы можно было дать подтверждение на отгрузку.</span><span class="sxs-lookup"><span data-stu-id="b3d45-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="b3d45-123">Настройка процента недопоставки</span><span class="sxs-lookup"><span data-stu-id="b3d45-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="b3d45-124">Чтобы задать процент недопоставки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b3d45-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="b3d45-125">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b3d45-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b3d45-126">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="b3d45-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="b3d45-127">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="b3d45-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="b3d45-128">На экспресс-вкладке **Сведения строки** выберите **Общее**.</span><span class="sxs-lookup"><span data-stu-id="b3d45-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="b3d45-129">В поле **Недопоставка** задайте в качестве значения большее процентное значение, которое будет соответствовать количеству, выбранному относительно количества загрузки, чтобы можно было подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="b3d45-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
