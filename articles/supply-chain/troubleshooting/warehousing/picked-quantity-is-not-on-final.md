---
title: Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы
description: Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938539"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="f5a5b-103">Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы</span><span class="sxs-lookup"><span data-stu-id="f5a5b-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="f5a5b-104">Код ошибки: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="f5a5b-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="f5a5b-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="f5a5b-105">Symptoms</span></span>

<span data-ttu-id="f5a5b-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="f5a5b-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f5a5b-107">Некоторые из номенклатур, которые требуются для загрузки %1, еще не скомплектованы и не перемещены в местонахождение конечной отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="f5a5b-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f5a5b-109">Причина</span><span class="sxs-lookup"><span data-stu-id="f5a5b-109">Cause</span></span>

<span data-ttu-id="f5a5b-110">Невозможно подтвердить загрузку в ее текущем состоянии, так как могут существовать следующие условия:</span><span class="sxs-lookup"><span data-stu-id="f5a5b-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="f5a5b-111">Связанная работа еще не скомплектована и не перемещена в конечную ячейку отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="f5a5b-112">Скомплектованное количество работы не соответствует созданному количеству работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="f5a5b-113">Приказ</span><span class="sxs-lookup"><span data-stu-id="f5a5b-113">Resolution</span></span>

<span data-ttu-id="f5a5b-114">Проверьте соответствующие заказы на продажу или заказы на перемещение для загрузки или отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="f5a5b-115">Убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="f5a5b-116">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f5a5b-117">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f5a5b-118">На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="f5a5b-119">Запишите значение поля **Созданное количество работы**.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="f5a5b-120">В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="f5a5b-121">Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="f5a5b-122">Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.</span><span class="sxs-lookup"><span data-stu-id="f5a5b-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
