---
title: Автоматическое подтверждение при оптимизации планирования
description: В этой теме объясняется, как использовать автоматическое подтверждение при оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783161"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="e2ce7-103">Автоматическое подтверждение при оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="e2ce7-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2ce7-104">Автоматическое подтверждение позволяет утверждать (то есть выпускать) спланированные заказы в рамках процесса сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="e2ce7-105">При подтверждении спланированных заказов они преобразуются в фактические заказы на покупку, заказы на перемещение или производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="e2ce7-106">При использовании оптимизации планирования спланированные заказы подтверждаются во время выполнения сводного планирования, когда дата заказа (то есть дата начала) находится в пределах временной границы для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="e2ce7-107">Автоматическое подтверждение спланированного заказа на покупку может выполняться только в том случае, если номенклатура связана с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="e2ce7-108">Включение автоматического подтверждения</span><span class="sxs-lookup"><span data-stu-id="e2ce7-108">Turn on auto-firming</span></span>

<span data-ttu-id="e2ce7-109">Чтобы включить автоматическое подтверждение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="e2ce7-110">В рабочей области **Управление функциями** на вкладке **Создать** выберите **Автоматическое подтверждение для оптимизации планирования** в списке.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="e2ce7-111">Если эта функция не отображается на вкладке **Создать**, проверьте вкладки **Не включено** и **Все**.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="e2ce7-112">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-112">Select **Enable now**.</span></span> <span data-ttu-id="e2ce7-113">Вместо этого выберите **План**, а затем выберите время, когда необходимо включить функцию.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="e2ce7-114">Настройка временной границы подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-114">Set up the firming time fence</span></span>

<span data-ttu-id="e2ce7-115">Временная граница подтверждения рассчитывается вперед от даты выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="e2ce7-116">Это определяется числом указанных дней.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="e2ce7-117">Временную границу подтверждения можно контролировать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="e2ce7-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="e2ce7-118">Чтобы определить временную границу подтверждения по умолчанию для группы покрытия, перейдите **Сводное планирование** \> **Настройка** \> **Покрытие** \> **Группы покрытия** и выберите группу покрытия.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="e2ce7-119">Затем на экспресс-вкладке **Прочие** в поле **Временная граница автоматического подтверждения (в днях)** введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="e2ce7-120">Чтобы перезаписать временную границу подтверждения, которая определена для группы покрытия для конкретной номенклатуры, перейдите **Управление сведениями о продукте** \> **Выпущенные продукты**, затем в области действий выберите **План**, а затем выберите **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the action pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="e2ce7-121">Затем на вкладке **Общие** выберите **Перекрытие временных границ** и в поле **Временная граница автоматического подтверждения (в днях)** введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="e2ce7-122">Чтобы перезаписать временную границу подтверждения, определенную для группы покрытия и покрытия номенклатуры для конкретного сводного плана, перейдите **Сводное планирование** \> **Настройка** \> **Сводные планы** и выберите сводный план.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="e2ce7-123">Затем на экспресс-вкладке **Временная граница в днях** выберите **Блокировка** как **Да** и введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="e2ce7-124">Если включено автоматическое подтверждение для выполнения сводного планирования, в котором используется оптимизация планирования, процесс автоматического подтверждения выполняется в соответствии с настройкой автоматического подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="e2ce7-125">Если автоматическое подтверждение не включено или если планирование начато со страницы **Нетто-потребности**, процесс автоматического подтверждения пропускается.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="e2ce7-126">Оптимизация планирования в сравнении со встроенным механизмом планирования Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e2ce7-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="e2ce7-127">Для автоматического подтверждения спланированных заказов можно использовать как оптимизацию планирования, так и механизм планирования, встроенный в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="e2ce7-128">Однако существуют некоторые важные различия.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-128">However, there are some important differences.</span></span> <span data-ttu-id="e2ce7-129">Например, в то время как в оптимизации планирования используется дату заказа (то есть дата начала), чтобы определить, какие спланированные заказы должны быть подтверждены, во встроенном механизме планирования Supply Chain Management" используется дата потребности (то есть дата окончания).</span><span class="sxs-lookup"><span data-stu-id="e2ce7-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="e2ce7-130">Ниже дана сводка отличий.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="e2ce7-131">**Оптимизация планирования**</span><span class="sxs-lookup"><span data-stu-id="e2ce7-131">**Planning Optimization**</span></span>

- <span data-ttu-id="e2ce7-132">Автоматическое подтверждение основано на дате заказа (дате начала).</span><span class="sxs-lookup"><span data-stu-id="e2ce7-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="e2ce7-133">Так как дата заказа (дата начала) инициирует подтверждение, нет необходимости учитывать время упреждения как часть временной границы подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="e2ce7-134">Если необходимо утвердить все заказы, которые должны быть запущены в течение текущей недели, временная граница подтверждения должна быть равна одной неделе.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="e2ce7-135">**Встроенный механизм планирования Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="e2ce7-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="e2ce7-136">Автоматическое подтверждение основано на дате потребности (дате окончания).</span><span class="sxs-lookup"><span data-stu-id="e2ce7-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="e2ce7-137">Чтобы помочь гарантировать, что заказы подтверждаются вовремя, временная граница подтверждения должна быть длиннее времени упреждения.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="e2ce7-138">Если необходимо утвердить все заказы, которые должны быть запущены в течение текущей недели, временная граница подтверждения должна быть равна времени упреждения плюс одна неделя.</span><span class="sxs-lookup"><span data-stu-id="e2ce7-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
