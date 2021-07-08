---
title: Десятичное округление количества физического обновления неверно
description: При создании отборочной накладной исходящая загрузка содержит количество, которое не соответствует десятичной точности, которая определяется в единице.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248801"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="f67df-103">Десятичное округление количества физического обновления неверно</span><span class="sxs-lookup"><span data-stu-id="f67df-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="f67df-104">Код ошибки: SYS19589</span><span class="sxs-lookup"><span data-stu-id="f67df-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="f67df-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="f67df-105">Symptoms</span></span>

<span data-ttu-id="f67df-106">При создании отборочной накладной исходящая загрузка содержит количество, которое не соответствует десятичной точности, которая определяется в единице.</span><span class="sxs-lookup"><span data-stu-id="f67df-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="f67df-107">При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="f67df-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="f67df-108">Неверное десятичное округление физически обновляемого количества в единице учета %1.</span><span class="sxs-lookup"><span data-stu-id="f67df-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="f67df-109">Поэтому невозможно создать отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="f67df-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f67df-110">Причина</span><span class="sxs-lookup"><span data-stu-id="f67df-110">Cause</span></span>

<span data-ttu-id="f67df-111">Система оценивает, соответствует ли десятичное округление количества отгрузки десятичной точности, определенной для единицы отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f67df-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="f67df-112">Когда система округляет количество отгрузки до заданного количества десятичных знаком, если она находит что округленное количество отгрузки не соответствует фактическому количеству отгрузки, вы не можете создать отборочную накладную.</span><span class="sxs-lookup"><span data-stu-id="f67df-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="f67df-113">Например, эта проблема может возникнуть, если количество продаж составляет 1,75 килограмм (кг), но десятичная точность установлена на *1*.</span><span class="sxs-lookup"><span data-stu-id="f67df-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="f67df-114">Решение</span><span class="sxs-lookup"><span data-stu-id="f67df-114">Resolution</span></span>

<span data-ttu-id="f67df-115">Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="f67df-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="f67df-116">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="f67df-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="f67df-117">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без десятичных чисел и любых других проблем округления.</span><span class="sxs-lookup"><span data-stu-id="f67df-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="f67df-118">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.</span><span class="sxs-lookup"><span data-stu-id="f67df-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="f67df-119">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без десятичных чисел и любых других проблем округления.</span><span class="sxs-lookup"><span data-stu-id="f67df-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="f67df-120">С помощью следующей процедуры проверьте строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без десятичных чисел и любых других проблем округления.</span><span class="sxs-lookup"><span data-stu-id="f67df-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="f67df-121">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f67df-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f67df-122">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="f67df-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="f67df-123">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="f67df-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="f67df-124">На вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая вызывает проблему.</span><span class="sxs-lookup"><span data-stu-id="f67df-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="f67df-125">Выберите **Уменьшить скомплектованное количество** для корректировки скомплектованного количества.</span><span class="sxs-lookup"><span data-stu-id="f67df-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="f67df-126">На вкладке  **Сведения строки** выберите **Заказ**.</span><span class="sxs-lookup"><span data-stu-id="f67df-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="f67df-127">В поле **Количество** установите значение для скомплектованного количества (то есть значение в поле **Созданное количество работы**), чтобы можно было продолжить создание отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="f67df-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="f67df-128">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.</span><span class="sxs-lookup"><span data-stu-id="f67df-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="f67df-129">С помощью следующей процедуры проверьте строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.</span><span class="sxs-lookup"><span data-stu-id="f67df-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="f67df-130">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f67df-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f67df-131">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="f67df-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="f67df-132">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая вызывает проблему.</span><span class="sxs-lookup"><span data-stu-id="f67df-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="f67df-133">Запишите значение полей **Количество** и **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="f67df-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="f67df-134">Перейдите в раздел **Управление организацией \> Единицы \> Единицы**.</span><span class="sxs-lookup"><span data-stu-id="f67df-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="f67df-135">Выберите единицу, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="f67df-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="f67df-136">При необходимости скорректируйте значение в поле **Десятичная точность**.</span><span class="sxs-lookup"><span data-stu-id="f67df-136">Adjust the value of the **Decimal precision** field as required.</span></span>
