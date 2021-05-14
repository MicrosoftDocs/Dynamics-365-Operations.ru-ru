---
title: Невозможно подтвердить отгрузку из-за проблемы с календарем
description: Невозможно подтвердить отгрузку из-за проблемы с календарем
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938541"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="c04e8-103">Невозможно подтвердить отгрузку из-за проблемы с календарем</span><span class="sxs-lookup"><span data-stu-id="c04e8-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="c04e8-104">Код ошибки: TRX2716</span><span class="sxs-lookup"><span data-stu-id="c04e8-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="c04e8-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="c04e8-105">Symptoms</span></span>

<span data-ttu-id="c04e8-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="c04e8-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="c04e8-107">Тип календаря %1 требует отметки прихода на встречу %2 и ухода с нее.</span><span class="sxs-lookup"><span data-stu-id="c04e8-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="c04e8-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="c04e8-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c04e8-109">Причина</span><span class="sxs-lookup"><span data-stu-id="c04e8-109">Cause</span></span>

<span data-ttu-id="c04e8-110">Для данной загрузки имеются активные встречи.</span><span class="sxs-lookup"><span data-stu-id="c04e8-110">Active appointments for the load exist.</span></span> <span data-ttu-id="c04e8-111">Например, имеется правило, требующее прибытия водителя.</span><span class="sxs-lookup"><span data-stu-id="c04e8-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="c04e8-112">Поэтому загрузка в данный момент находится в состоянии, когда подтверждение отгрузки не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c04e8-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="c04e8-113">Приказ</span><span class="sxs-lookup"><span data-stu-id="c04e8-113">Resolution</span></span>

<span data-ttu-id="c04e8-114">Необходимо изучить и устранить все проблемы с активными встречами, связанными с данной загрузкой.</span><span class="sxs-lookup"><span data-stu-id="c04e8-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="c04e8-115">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="c04e8-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c04e8-116">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="c04e8-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c04e8-117">В области действий на вкладке **Транспортировка** в группе **Встречи** выберите **Планирование встречи**.</span><span class="sxs-lookup"><span data-stu-id="c04e8-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="c04e8-118">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c04e8-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="c04e8-119">Убедитесь, что для встречи завершено прибытие/отбытие водителя.</span><span class="sxs-lookup"><span data-stu-id="c04e8-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="c04e8-120">Завершите или отмените встречу.</span><span class="sxs-lookup"><span data-stu-id="c04e8-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="c04e8-121">Отключите параметр **Требуется регистрация прибытия водителя** для соответствующего правила встречи.</span><span class="sxs-lookup"><span data-stu-id="c04e8-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
