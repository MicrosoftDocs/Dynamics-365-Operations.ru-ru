---
title: Автоматическое подтверждение при оптимизации планирования
description: В этой теме объясняется, как использовать автоматическое подтверждение при оптимизации планирования.
author: ChristianRytt
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 3542e343de29c9fd9d19ed99cab4b4eebacd2899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813011"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="7166c-103">Автоматическое подтверждение при оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="7166c-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7166c-104">Автоматическое подтверждение позволяет утверждать (то есть выпускать) спланированные заказы в рамках процесса сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="7166c-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="7166c-105">При подтверждении спланированных заказов они преобразуются в фактические заказы на покупку, заказы на перемещение или производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="7166c-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="7166c-106">При использовании оптимизации планирования спланированные заказы подтверждаются во время выполнения сводного планирования, когда дата заказа (то есть дата начала) находится в пределах временной границы для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7166c-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="7166c-107">Автоматическое подтверждение спланированного заказа на покупку может выполняться только в том случае, если номенклатура связана с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="7166c-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>
> 
> <span data-ttu-id="7166c-108">Утвержденные производные заказы (субподрядные заказы на покупку) будут показывать статус *На рассмотрении*, когда включено отслеживание изменений в обращении.</span><span class="sxs-lookup"><span data-stu-id="7166c-108">Firmed derived orders (subcontract purchase orders) will show a status of *In-review* when case change tracking is enabled.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="7166c-109">Включение автоматического подтверждения</span><span class="sxs-lookup"><span data-stu-id="7166c-109">Turn on autofirming</span></span>

<span data-ttu-id="7166c-110">Чтобы включить автоматическое подтверждение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7166c-110">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="7166c-111">В рабочей области **Управление функциями** на вкладке **Создать** выберите **Автоматическое подтверждение для оптимизации планирования** в списке.</span><span class="sxs-lookup"><span data-stu-id="7166c-111">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="7166c-112">Если эта функция не отображается на вкладке **Создать**, проверьте вкладки **Не включено** и **Все**.</span><span class="sxs-lookup"><span data-stu-id="7166c-112">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="7166c-113">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="7166c-113">Select **Enable now**.</span></span> <span data-ttu-id="7166c-114">Вместо этого выберите **План**, а затем выберите время, когда необходимо включить функцию.</span><span class="sxs-lookup"><span data-stu-id="7166c-114">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="7166c-115">Настройка временной границы подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7166c-115">Set up the firming time fence</span></span>

<span data-ttu-id="7166c-116">Временная граница подтверждения рассчитывается вперед от даты выполнения сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="7166c-116">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="7166c-117">Это определяется числом указанных дней.</span><span class="sxs-lookup"><span data-stu-id="7166c-117">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="7166c-118">Временную границу подтверждения можно контролировать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7166c-118">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="7166c-119">Чтобы определить временную границу подтверждения по умолчанию для группы покрытия, перейдите **Сводное планирование** \> **Настройка** \> **Покрытие** \> **Группы покрытия** и выберите группу покрытия.</span><span class="sxs-lookup"><span data-stu-id="7166c-119">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="7166c-120">Затем на экспресс-вкладке **Прочие** в поле **Временная граница автоматического подтверждения (в днях)** введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="7166c-120">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="7166c-121">Чтобы перезаписать временную границу подтверждения, которая определена для группы покрытия для конкретной номенклатуры, перейдите **Управление сведениями о продукте** \> **Выпущенные продукты**, затем на панели операций выберите **План**, а затем выберите **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="7166c-121">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="7166c-122">Затем на вкладке **Общие** выберите **Перекрытие временных границ** и в поле **Временная граница автоматического подтверждения (в днях)** введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="7166c-122">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="7166c-123">Чтобы перезаписать временную границу подтверждения, определенную для группы покрытия и покрытия номенклатуры для конкретного сводного плана, перейдите **Сводное планирование** \> **Настройка** \> **Сводные планы** и выберите сводный план.</span><span class="sxs-lookup"><span data-stu-id="7166c-123">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="7166c-124">Затем на экспресс-вкладке **Временная граница в днях** выберите **Утверждение** как **Да** и введите количество дней.</span><span class="sxs-lookup"><span data-stu-id="7166c-124">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="7166c-125">Если включено автоматическое подтверждение для выполнения сводного планирования, в котором используется оптимизация планирования, процесс автоматического подтверждения выполняется в соответствии с настройкой автоматического подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7166c-125">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="7166c-126">Если автоматическое подтверждение не включено или если планирование начато со страницы **Нетто-потребности**, процесс автоматического подтверждения пропускается.</span><span class="sxs-lookup"><span data-stu-id="7166c-126">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="7166c-127">Оптимизация планирования в сравнении со встроенным механизмом планирования Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7166c-127">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="7166c-128">Для автоматического подтверждения спланированных заказов можно использовать как оптимизацию планирования, так и механизм планирования, встроенный в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7166c-128">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="7166c-129">Однако существуют некоторые важные различия.</span><span class="sxs-lookup"><span data-stu-id="7166c-129">However, there are some important differences.</span></span> <span data-ttu-id="7166c-130">Например, в то время как в оптимизации планирования используется дату заказа (то есть дата начала), чтобы определить, какие спланированные заказы должны быть подтверждены, во встроенном механизме планирования Supply Chain Management" используется дата потребности (то есть дата окончания).</span><span class="sxs-lookup"><span data-stu-id="7166c-130">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="7166c-131">Ниже дана сводка отличий.</span><span class="sxs-lookup"><span data-stu-id="7166c-131">Here is a summary of the differences.</span></span>

<span data-ttu-id="7166c-132">**Оптимизация планирования**</span><span class="sxs-lookup"><span data-stu-id="7166c-132">**Planning Optimization**</span></span>

- <span data-ttu-id="7166c-133">Автоматическое подтверждение основано на дате заказа (дате начала).</span><span class="sxs-lookup"><span data-stu-id="7166c-133">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="7166c-134">Так как дата заказа (дата начала) инициирует подтверждение, нет необходимости учитывать время упреждения как часть временной границы подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7166c-134">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="7166c-135">Если необходимо утвердить все заказы, которые должны быть запущены в течение текущей недели, временная граница подтверждения должна быть равна одной неделе.</span><span class="sxs-lookup"><span data-stu-id="7166c-135">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="7166c-136">**Встроенный механизм планирования Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="7166c-136">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="7166c-137">Автоматическое подтверждение основано на дате потребности (дате окончания).</span><span class="sxs-lookup"><span data-stu-id="7166c-137">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="7166c-138">Чтобы помочь гарантировать, что заказы подтверждаются вовремя, временная граница подтверждения должна быть длиннее времени упреждения.</span><span class="sxs-lookup"><span data-stu-id="7166c-138">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="7166c-139">Если необходимо утвердить все заказы, которые должны быть запущены в течение текущей недели, временная граница подтверждения должна быть равна времени упреждения плюс одна неделя.</span><span class="sxs-lookup"><span data-stu-id="7166c-139">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
