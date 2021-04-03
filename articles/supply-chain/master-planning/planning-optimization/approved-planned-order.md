---
title: Утвердить спланированные заказы
description: В этой теме описывается утверждение спланированных заказов, которые поддерживаются в оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 8745a461986c1f16f2b3f9fd23011701d104a30c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264026"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="67409-103">Утвердить спланированные заказы</span><span class="sxs-lookup"><span data-stu-id="67409-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67409-104">В этой теме приводятся сведения о том, как обновить статус спланированных заказов при оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="67409-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="67409-105">Обратите внимание, что утверждение спланированных заказов является необязательным шагом на пути создания подтвержденного заказа из спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="67409-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="67409-106">Рекомендуется утверждать измененные спланированные заказы, в противном случае изменения будут пропущены и перезаписаны при следующем выполнении планирования.</span><span class="sxs-lookup"><span data-stu-id="67409-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Поток спланированного заказа](media/approved-planned-orders-1.png)

<span data-ttu-id="67409-108">Поле **Статус** помогает отмечать ход выполнения с помощью следующих значений:</span><span class="sxs-lookup"><span data-stu-id="67409-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="67409-109">**Не обработано.** Когда система сводного планирования создает спланированные заказы, они имеют статус *Не обработано*.</span><span class="sxs-lookup"><span data-stu-id="67409-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="67409-110">Спланированные заказы с этим статусом будут удалены в ходе следующего выполнения планирования.</span><span class="sxs-lookup"><span data-stu-id="67409-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="67409-111">**Завершено.** Если решено не утверждать спланированный заказ, можно изменить статус на *Завершено*, чтобы указать, что оценка этого спланированного заказа завершена.</span><span class="sxs-lookup"><span data-stu-id="67409-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="67409-112">Обратите внимание, что значения статуса *Не обработано* и *Завершено* обрабатываются системой одинаково.</span><span class="sxs-lookup"><span data-stu-id="67409-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="67409-113">**Утверждено.** Если необходимо сохранить изменения или планируется утвердить спланированный заказ, измените статус на *Утверждено*.</span><span class="sxs-lookup"><span data-stu-id="67409-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="67409-114">Спланированные заказы со статусом *Утверждено* считаются фиксированной и ожидаемой поставкой в сводном планировании, поэтому они не изменяются и не удаляются во время последующих запусков сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="67409-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="67409-115">Для достижения этой цели логика планирования копирует спланированные заказы *Одобрено* из старой версии плана в новую версию плана во время сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="67409-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="67409-116">Обратите внимание, что *утвержденные* спланированные заказы рассматриваются как поставки только в рамках указанного сводного плана.</span><span class="sxs-lookup"><span data-stu-id="67409-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="67409-117">Вы можете управлять запланированными заказами в рабочей области **Сводное планирование**, списке **Спланированный заказ** или списках **Спланированный производственный заказ**, **Спланированный заказ на покупку** и **Спланированное перемещение**.</span><span class="sxs-lookup"><span data-stu-id="67409-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]