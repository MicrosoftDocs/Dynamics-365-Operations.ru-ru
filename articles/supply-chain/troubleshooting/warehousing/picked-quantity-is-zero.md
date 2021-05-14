---
title: Невозможно подтвердить отгрузку, так как имеется нулевое количество
description: Невозможно подтвердить отгрузку, так как имеется нулевое количество
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938538"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="4e8ef-103">Невозможно подтвердить отгрузку, так как имеется нулевое количество</span><span class="sxs-lookup"><span data-stu-id="4e8ef-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="4e8ef-104">Код ошибки: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="4e8ef-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="4e8ef-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="4e8ef-105">Symptoms</span></span>

<span data-ttu-id="4e8ef-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="4e8ef-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4e8ef-107">Строка загрузки для номенклатуры %1 и отгрузки %2 обновлена и теперь имеет нулевое количество из-за настройки недопоставки, что позволяет не отгружать какие-либо количества для этого номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="4e8ef-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4e8ef-109">Причина</span><span class="sxs-lookup"><span data-stu-id="4e8ef-109">Cause</span></span>

<span data-ttu-id="4e8ef-110">Система проверяет, находится ли скомплектованное количество в ожидаемых пределах на основе скомплектованного количества, количества в строке загрузки и процента недопоставки.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="4e8ef-111">Если система обнаруживает, что скомплектованное количество в строке загрузки равно 0 (нулю), невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="4e8ef-112">Например, эта проблема может возникнуть, если работа была отменена, а процент недопоставки в строке загрузки равен 100 процентам.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e8ef-113">Приказ</span><span class="sxs-lookup"><span data-stu-id="4e8ef-113">Resolution</span></span>

<span data-ttu-id="4e8ef-114">Проверьте строки загрузки, чтобы убедиться, что процент недопоставки и количества недопоставки соответствуют скомплектованной работе.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="4e8ef-115">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4e8ef-116">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4e8ef-117">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="4e8ef-118">Измените значение в поле **Недопоставка** или в поле **Количество**, как необходимо.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="4e8ef-119">Если проблема все еще не исправлена, возможно, придется выполнить дополнительную работу комплектации для соответствующих заказов на продажу или заказов на перемещение до тех пор, пока доступное количество не будет соответствовать загрузке или отгрузке.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
