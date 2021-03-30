---
title: Устранение неполадок сводного планирования
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе со сводным планированием.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216113"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="1ae0d-103">Устранение неполадок сводного планирования</span><span class="sxs-lookup"><span data-stu-id="1ae0d-103">Troubleshoot master planning</span></span>

<span data-ttu-id="1ae0d-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе со сводным планированием.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="1ae0d-105">Развертывание спецификаций работает по-разному для утвержденных производственных заказов и для расчетных производственных заказов для созданной вручную работы.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ae0d-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-106">Issue description</span></span>

<span data-ttu-id="1ae0d-107">Когда производственный заказ утвержден, номенклатуры не разворачиваются при разворачивании спецификации.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="1ae0d-108">Однако при создании вручную заказа на работу и последующем выполнении оценки производственного заказа номенклатуры разворачиваются.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ae0d-109">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-109">Issue resolution</span></span>

<span data-ttu-id="1ae0d-110">Система работает ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-110">The system is working as expected.</span></span> <span data-ttu-id="1ae0d-111">Развертывание, которое происходит, когда производственный заказ утверждается, будет указывать на спланированный заказ, но не появляется, что запланированный заказ в данный момент утвержден в этом случае.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="1ae0d-112">Однако если производственный заказ оценен, развертывание запускается из выпущенного производственного заказа, для которого не существует спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="1ae0d-113">Значение задержки не обновляется при перепланировании спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="1ae0d-114">Чтобы обновить задержку для спланированных заказов, откройте диалоговое окно **Перепланирование** для спланированного заказа.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="1ae0d-115">На экспресс-вкладке **Развертывание** убедитесь, что параметр **Выполнить развертывание после перепланирования** имеет значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="1ae0d-116">Планирование производства не учитывает резервное время, установленное для покрытия номенклатуры, для фиксированного снабжения.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ae0d-117">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-117">Issue description</span></span>

<span data-ttu-id="1ae0d-118">При сводном планировании резервное время учитываются.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="1ae0d-119">Однако резервное время игнорируется, когда планируются запланированные производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ae0d-120">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-120">Issue resolution</span></span>

<span data-ttu-id="1ae0d-121">Резервы используются только при сводном планировании, но не во время планирования вручную.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="1ae0d-122">Резервы предназначены для работы в качестве буфера на этапе планирования, для предоставления некоторого "запаса" для фактического процесса.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="1ae0d-123">Чтобы получить нужный результат, можно удалить резерв.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="1ae0d-124">Затем маршрут должен быть обновлен так, чтобы он включал нужное время (например, время ожидания).</span><span class="sxs-lookup"><span data-stu-id="1ae0d-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="1ae0d-125">И сводное планирование, и планирование вручную должны давать одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="1ae0d-126">Спланированные заказы создаются даже в том случае, если имеются номенклатуры в запасах и производственные заказы уже существуют для них.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="1ae0d-127">Возможно, вы сможете устранить эту проблему, увеличив значение **Положительные дни** для соответствующих групп на странице **Группа покрытия**.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="1ae0d-128">Это изменение приведет к тому, что система определит, можно ли использовать запасы в наличии для спроса.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="1ae0d-129">Затем новый спланированный заказ не будет создаваться для номенклатур в наличии.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="1ae0d-130">Сводное планирование не учитывает ограничения по емкости и планирует больше, чем доступная емкость.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ae0d-131">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-131">Issue description</span></span>

<span data-ttu-id="1ae0d-132">При использовании планирования операций там, где имеется ограничение по емкости, и где маршрут определяет сочетание требований как для группы ресурсов, так и для отдельных ресурсов, существует небольшая вероятность избыточного резервирования из-за способа, которым алгоритм проверяет конфликты емкостей.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="1ae0d-133">Это избыточное резервирование может происходить при использовании помощников для выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="1ae0d-134">Чаще всего это возникает, если имеется много заданий, имеющих относительно короткое время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ae0d-135">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-135">Issue resolution</span></span>

<span data-ttu-id="1ae0d-136">Если важно, чтобы не было избыточного резервирования при планировании операций, можно сделать часть планирования в сводном планировании однопоточным, включив параметр **Точное ограничение по мощности для планирования операций** на странице **Параметры сводного планирования**.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="1ae0d-137">Этот параметр недоступен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-137">This option isn't available by default.</span></span> <span data-ttu-id="1ae0d-138">Его необходимо добавить на страницу вручную, используя возможности персонализации.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="1ae0d-139">При использовании этого параметра планирование будет выполняться медленнее из-за нехватки параллельной обработки.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="1ae0d-140">Обновление запланированных заказов занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ae0d-141">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-141">Issue description</span></span>

<span data-ttu-id="1ae0d-142">При обновлении требуемого количества и/или даты поставки по спланированному заказу для сохранения обновления обычно требуется по крайней мере 30 секунд на заказ.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ae0d-143">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="1ae0d-143">Issue resolution</span></span>

<span data-ttu-id="1ae0d-144">Это известная проблема встроенного механизма сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="1ae0d-145">Это обусловлено работой базовой функции автоматического развертывания через структуру спецификации во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="1ae0d-146">Эта проблема решена в оптимизации планирования, где планирующий может обновлять и утверждать соответствующие заказы и, при желании, запускать процесс планирования для обновления спланированных заказов для базовой структуры спецификации.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="1ae0d-147">Одним из способов повышения производительности при помощи встроенного механизма сводного планирования является выполнение следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1ae0d-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="1ae0d-148">Выберите **Сводное планирование \> Настройка \> Планы \> Сводные планы**.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="1ae0d-149">Выберите план.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-149">Select a plan.</span></span>
1. <span data-ttu-id="1ae0d-150">Разверните экспресс-вкладку **Временная граница в днях**.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="1ae0d-151">Задайте для параметра **Развертывание** значение *Да*, и в поле, расположенном под этим параметром, задайте значение "0" (ноль).</span><span class="sxs-lookup"><span data-stu-id="1ae0d-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="1ae0d-152">Это ограничит период для развертываний, выполняемых для этого сводного плана, до одного дня.</span><span class="sxs-lookup"><span data-stu-id="1ae0d-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]