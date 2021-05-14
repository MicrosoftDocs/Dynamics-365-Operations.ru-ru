---
title: Невозможно подтвердить отгрузку, поскольку количество превышает процент перепоставки
description: Невозможно подтвердить отгрузку, поскольку количество превышает процент перепоставки
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938542"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="efb58-103">Невозможно подтвердить отгрузку, поскольку количество превышает процент перепоставки</span><span class="sxs-lookup"><span data-stu-id="efb58-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="efb58-104">Код ошибки: WAX1687</span><span class="sxs-lookup"><span data-stu-id="efb58-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="efb58-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="efb58-105">Symptoms</span></span>

<span data-ttu-id="efb58-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="efb58-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="efb58-107">Не удалось подтвердить отгрузку для загрузки %1, так как количество номенклатуры %2 превышает процент, определенный для перепоставки.</span><span class="sxs-lookup"><span data-stu-id="efb58-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="efb58-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="efb58-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="efb58-109">Причина</span><span class="sxs-lookup"><span data-stu-id="efb58-109">Cause</span></span>

<span data-ttu-id="efb58-110">Количество загрузки или отгрузки было частично скомплектовано.</span><span class="sxs-lookup"><span data-stu-id="efb58-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="efb58-111">Количество в настоящее время превышает скомплектованное количество на процент, выходящий за пределы разрешенного процента перепоставки.</span><span class="sxs-lookup"><span data-stu-id="efb58-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="efb58-112">Приказ</span><span class="sxs-lookup"><span data-stu-id="efb58-112">Resolution</span></span>

<span data-ttu-id="efb58-113">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="efb58-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="efb58-114">Задание количества в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="efb58-114">Set the load line quantity.</span></span>
- <span data-ttu-id="efb58-115">Настройка процента перепоставки.</span><span class="sxs-lookup"><span data-stu-id="efb58-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="efb58-116">Задание количества в строке загрузки</span><span class="sxs-lookup"><span data-stu-id="efb58-116">Set the load line quantity</span></span>

<span data-ttu-id="efb58-117">Чтобы задать количество в строке загрузки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="efb58-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="efb58-118">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="efb58-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="efb58-119">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="efb58-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="efb58-120">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="efb58-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="efb58-121">На экспресс-вкладке **Сведения строки** выберите **Заказ**.</span><span class="sxs-lookup"><span data-stu-id="efb58-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="efb58-122">В поле **Количество** установите значение для скомплектованного количества (то есть **Созданное количество работы**), чтобы можно было дать подтверждение на отгрузку.</span><span class="sxs-lookup"><span data-stu-id="efb58-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="efb58-123">Настройка процента перепоставки</span><span class="sxs-lookup"><span data-stu-id="efb58-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="efb58-124">Чтобы задать процент недопоставки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="efb58-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="efb58-125">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="efb58-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="efb58-126">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="efb58-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="efb58-127">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="efb58-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="efb58-128">На экспресс-вкладке **Сведения строки** выберите **Общее**.</span><span class="sxs-lookup"><span data-stu-id="efb58-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="efb58-129">В поле **Перепоставка** задайте в качестве значения большее процентное значение, которое будет соответствовать количеству, выбранному относительно количества загрузки, чтобы можно было подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="efb58-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
