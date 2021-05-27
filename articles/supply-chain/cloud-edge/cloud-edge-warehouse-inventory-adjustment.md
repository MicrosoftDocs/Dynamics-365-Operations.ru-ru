---
title: Корректировка запасов склада
description: В этой теме приводятся сведения о журнале корректировки запасов склада и обработке при использовании единиц масштабирования.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026141"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="2e000-103">Корректировка запасов склада</span><span class="sxs-lookup"><span data-stu-id="2e000-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2e000-104">Функция корректировки запасов склада используются при выполнении облачных и пограничных единиц масштабирования для [производственных рабочих нагрузок](cloud-edge-workload-manufacturing.md) и [рабочих нагрузок управления складом](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="2e000-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="2e000-105">Когда работник выполняет корректировку запасов, используя приложение склада по отношению к рабочей нагрузке управления складом единиц масштабирования, физическое обновление в наличии должно быть обработано пакетным заданием **Журнал корректировки запасов склада**, которое выполняется и планируется путем перехода к **Управление складом > Периодические задачи > Журнал корректировки запасов склада**.</span><span class="sxs-lookup"><span data-stu-id="2e000-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="2e000-106">Следующие рабочие процессы приложения склада в настоящее время используют **Журнал корректировки запасов склада** для рабочих нагрузок единиц масштабирования:</span><span class="sxs-lookup"><span data-stu-id="2e000-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="2e000-107">Корректировка (входящая/исходящая)</span><span class="sxs-lookup"><span data-stu-id="2e000-107">Adjustment in/out</span></span>
- <span data-ttu-id="2e000-108">Цикличный подсчет</span><span class="sxs-lookup"><span data-stu-id="2e000-108">Cycle counting</span></span>
- <span data-ttu-id="2e000-109">Загрузка грузоместа</span><span class="sxs-lookup"><span data-stu-id="2e000-109">License plate loading</span></span>

<span data-ttu-id="2e000-110">Несколько проводок по запасам создаются как часть каждого процесса корректировки запасов, так как развертывания концентратора и единиц масштабирования совместно используют записи запасов.</span><span class="sxs-lookup"><span data-stu-id="2e000-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="2e000-111">Пример корректировки запасов</span><span class="sxs-lookup"><span data-stu-id="2e000-111">Inventory adjustment example</span></span>

<span data-ttu-id="2e000-112">В этом примере складской работник использовал приложение склада, чтобы зарегистрировать добавление запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="2e000-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="2e000-113">Во-первых, рабочая нагрузка единиц масштабирования создает проводку корректировки складских запасов для положительной физической корректировки, которая затем синхронизируется с концентратором и приводит к увеличению запасов в наличии в концентраторе.</span><span class="sxs-lookup"><span data-stu-id="2e000-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="2e000-114">Вид</span><span class="sxs-lookup"><span data-stu-id="2e000-114">Type</span></span>                                    | <span data-ttu-id="2e000-115">Единица масштабирования</span><span class="sxs-lookup"><span data-stu-id="2e000-115">Scale unit</span></span> | <span data-ttu-id="2e000-116">Направление</span><span class="sxs-lookup"><span data-stu-id="2e000-116">Direction</span></span> | <span data-ttu-id="2e000-117">Узел</span><span class="sxs-lookup"><span data-stu-id="2e000-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="2e000-118">Корректировка запасов склада</span><span class="sxs-lookup"><span data-stu-id="2e000-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="2e000-119">+1</span><span class="sxs-lookup"><span data-stu-id="2e000-119">+1</span></span>         | ->        | <span data-ttu-id="2e000-120">+1</span><span class="sxs-lookup"><span data-stu-id="2e000-120">+1</span></span>  |

<span data-ttu-id="2e000-121">Затем концентратор обрабатывает разноску журнала учета, которая получается через [сообщения обработчика сообщений](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="2e000-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="2e000-122">Это приводит к обновлению дополнительных запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="2e000-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="2e000-123">Чтобы исключить двойных запасов в наличии, концентратор создает корреспондирующую проводку в рамках этого процесса и удаляет ранее записанные запасы в наличии, которые связаны с корректировкой складских запасов.</span><span class="sxs-lookup"><span data-stu-id="2e000-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="2e000-124">Вид</span><span class="sxs-lookup"><span data-stu-id="2e000-124">Type</span></span>                                    | <span data-ttu-id="2e000-125">Единица масштабирования</span><span class="sxs-lookup"><span data-stu-id="2e000-125">Scale unit</span></span> | <span data-ttu-id="2e000-126">Направление</span><span class="sxs-lookup"><span data-stu-id="2e000-126">Direction</span></span> | <span data-ttu-id="2e000-127">Узел</span><span class="sxs-lookup"><span data-stu-id="2e000-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="2e000-128">Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="2e000-128">Counting</span></span>                                | <span data-ttu-id="2e000-129">+1</span><span class="sxs-lookup"><span data-stu-id="2e000-129">+1</span></span>         | <-        | <span data-ttu-id="2e000-130">+1</span><span class="sxs-lookup"><span data-stu-id="2e000-130">+1</span></span>  |
| <span data-ttu-id="2e000-131">Корректировка складских запасов (корр. счет)</span><span class="sxs-lookup"><span data-stu-id="2e000-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="2e000-132">-1</span><span class="sxs-lookup"><span data-stu-id="2e000-132">-1</span></span>         | <-        | <span data-ttu-id="2e000-133">-1</span><span class="sxs-lookup"><span data-stu-id="2e000-133">-1</span></span>  |

<span data-ttu-id="2e000-134">После того как единица масштабирования создала **Журнал корректировки запасов склада** в концентраторе, можно проверить и **Журнал учета**, и **Журнал корр. счета**, которые создаются концентратором в рамках процесса корректировки.</span><span class="sxs-lookup"><span data-stu-id="2e000-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="2e000-135">Можно проверить каждую из этих записей журнала и проводки в Supply Chain Management, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2e000-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="2e000-136">Выполните вход в единицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2e000-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="2e000-137">Перейдите **Управление складом \> Периодические задачи \> Журнал корректировки складских запасов**.</span><span class="sxs-lookup"><span data-stu-id="2e000-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="2e000-138">На странице **Журнал корректировки запасов склада** найдите и откройте журнал, в котором записано изменение запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="2e000-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="2e000-139">В разделе **Строки журнала** отображается каждая корректировка, записанная данным журналом.</span><span class="sxs-lookup"><span data-stu-id="2e000-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="2e000-140">Выполните вход в концентратор.</span><span class="sxs-lookup"><span data-stu-id="2e000-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="2e000-141">Перейдите **Управление складом \> Периодические задачи \> Журнал корректировки складских запасов**.</span><span class="sxs-lookup"><span data-stu-id="2e000-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="2e000-142">На странице **Журнал корректировки запасов склада** должен отобразиться тот же самый журнал, если концентратор и единица масштабирования синхронизованы.</span><span class="sxs-lookup"><span data-stu-id="2e000-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="2e000-143">Откройте журнал.</span><span class="sxs-lookup"><span data-stu-id="2e000-143">Open the journal.</span></span> <span data-ttu-id="2e000-144">Если [сообщения обработчика сообщений](cloud-edge-message-processor-messages.md) обработаны, в заголовке будут отображаться ссылки на **Журнал учета** и **Журнал корр. счета**.</span><span class="sxs-lookup"><span data-stu-id="2e000-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="2e000-145">В **Журнале учета** должны отображаться те же значения аналитики, что и в строках журнала.</span><span class="sxs-lookup"><span data-stu-id="2e000-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="2e000-146">В **Журнале корр.счета** должен отображать корр. счет, который удаляет двойную корректировку запасов.</span><span class="sxs-lookup"><span data-stu-id="2e000-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="2e000-147">После завершения всей синхронизации и обработки **Журнал учета** и **Журнал корр. счета** синхронизируются с единицей масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2e000-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="2e000-148">Их также можно просмотреть на соответствующей странице **Журнал корректировки запасов склада**.</span><span class="sxs-lookup"><span data-stu-id="2e000-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
