---
title: "Предварительные требования для стандартных затрат"
description: "Этот раздел описывает основные шаги по использованию стандартных затрат."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d5a4a4e49ef1cee923011ddab24497c65f85c1e3
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="e62a3-103">Предварительные требования для стандартных затрат</span><span class="sxs-lookup"><span data-stu-id="e62a3-103">Prerequisites for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e62a3-104">Этот раздел описывает основные шаги по использованию стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="e62a3-105">Последующие шаги зависят от операционной деятельности компании.</span><span class="sxs-lookup"><span data-stu-id="e62a3-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="e62a3-106">Например, шаги различаются для непроизводственной среды, производственной среды, в которой не используется маршрутизация и производственной среды, в которой маршрутизация используется.</span><span class="sxs-lookup"><span data-stu-id="e62a3-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="e62a3-107">Для настройки стандартных затрат выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="e62a3-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="e62a3-108">**1. Создайте группу номенклатурных моделей для стандартных затрат.**</span><span class="sxs-lookup"><span data-stu-id="e62a3-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="e62a3-109">Используйте страницу **Группы номенклатурных моделей**, чтобы создать новую группу для стандартных затрат и назначить ей складскую модель **Стандартные затраты**.</span><span class="sxs-lookup"><span data-stu-id="e62a3-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="e62a3-110">Идентификатор группы номенклатурных моделей должен быть информативным, таким как **Std Cost**.</span><span class="sxs-lookup"><span data-stu-id="e62a3-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="e62a3-111">Установите флажки, указывающие, что группа должна допускать отрицательные финансовые запасы и должна выполнять разноску физических запасов и финансовых запасов.</span><span class="sxs-lookup"><span data-stu-id="e62a3-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="e62a3-112">Эта группа стандартных затрат будет назначаться номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="e62a3-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="e62a3-113">**2. Определите счета ГК, которые имеют отношение к отклонениям от стандартных затрат.**</span><span class="sxs-lookup"><span data-stu-id="e62a3-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="e62a3-114">Используйте страницу **План счетов**, чтобы определить счета ГК, которые имеют отношение к отклонениям от стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="e62a3-115">Эти счета ГК должны быть определены до того, как появится возможность назначать их на странице **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="e62a3-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="e62a3-116">Счета ГК могут отражать номенклатурные группы и группы затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="e62a3-117">**3. Назначьте счета учета разноскам номенклатур, связанным с отклонениями от стандартных затрат.**</span><span class="sxs-lookup"><span data-stu-id="e62a3-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="e62a3-118">Используйте страницу **Разноска**, чтобы назначить счета ГК, которые имеют отношение к отклонениям от стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="e62a3-119">Можно указывать счет ГК для отклонений по номенклатуре (или номенклатурной группе) и по группе затрат (или типу группы затрат) или можно указывать, что счет ГК применяется ко всем номенклатурам и всем группам затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="e62a3-120">Эти варианты согласовываются с отношениями затрат для таблиц, групп и так далее.</span><span class="sxs-lookup"><span data-stu-id="e62a3-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="e62a3-121">Перед определением правил разноски номенклатуры используйте страницу **Комбинации проводок**, чтобы разрешить использование отношений затрат (для таблиц, групп и всего).</span><span class="sxs-lookup"><span data-stu-id="e62a3-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="e62a3-122">**4. Определите параметры запасов, которые относятся к стандартным затратам.**</span><span class="sxs-lookup"><span data-stu-id="e62a3-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="e62a3-123">Используйте вкладку **Учет запасов** на странице **Настройка учетных политик запасов > Параметры** для определения двух параметров, которые имеют отношение к стандартным затратам.</span><span class="sxs-lookup"><span data-stu-id="e62a3-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="e62a3-124">В поле **Детализация затрат** выберите **Нет** или **Вспомогательная книга**.</span><span class="sxs-lookup"><span data-stu-id="e62a3-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="e62a3-125">При выборе варианта **Вспомогательная книга** детализация затрат является *активной* детализацией затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="e62a3-126">Активная детализация затрат важна для расчета, сохранения и просмотра сегментации по группам затрат в разрезе многоуровневой структуры продуктов для номенклатур со стандартными затратами.</span><span class="sxs-lookup"><span data-stu-id="e62a3-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="e62a3-127">Когда детализация затрат активная, можно составлять отчеты и выполнять анализ запасов, незавершенного производства (НЗП) и себестоимости реализованной продукции по группам затрат на одном уровне, нескольких уровнях или в итоговом формате.</span><span class="sxs-lookup"><span data-stu-id="e62a3-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="e62a3-128">Когда детализация затрат активная означает, если включить затраты по произведенной номенклатуре, сегментация по группам затрат сохраняется в записи затрат по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="e62a3-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="e62a3-129">При выборе **Нет** сегментация групп затрат не будет поддерживаться для номенклатур со стандартными затратами.</span><span class="sxs-lookup"><span data-stu-id="e62a3-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="e62a3-130">Другими словами, стандартные затраты по произведенной номенклатуре будут рассчитываться и поддерживаться как единая сумма без сегментации по группам затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="e62a3-131">Вклады затрат произведенных компонентов будет суммироваться в единую сумму.</span><span class="sxs-lookup"><span data-stu-id="e62a3-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="e62a3-132">В поле **Расхождения со стандартными значениями** выберите **Суммированные** или **По группе затрат**.</span><span class="sxs-lookup"><span data-stu-id="e62a3-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="e62a3-133">Если выбран вариант **По группе затрат**, можно определять расхождения закупочных цен и отклонения цены производства от себестоимости по группам затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="e62a3-134">Можно также определить 4 типа отклонений цены производства от себестоимости: размер лота, количество, цена и расхождения в подстановке.</span><span class="sxs-lookup"><span data-stu-id="e62a3-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="e62a3-135">Если выбран вариант **Суммированные**, вы не можете определять расхождения по группам затрат, и вы не можете определить 4 типа отклонений цены производства от себестоимости.</span><span class="sxs-lookup"><span data-stu-id="e62a3-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="e62a3-136">Можно только просматривать суммарное отклонение цены производства от себестоимости.</span><span class="sxs-lookup"><span data-stu-id="e62a3-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="e62a3-137">Политика в отношении расхождения со стандартом работает независимо от политики в отношении детализации затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="e62a3-138">Другими словами, можно выбрать политику детализации затрат **Нет** и выбрать расхождения по группам затрат, при этом отклонения цены производства от себестоимости будут регистрироваться по группам затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="e62a3-139">**5. Создайте версии цены для стандартных затрат.**</span><span class="sxs-lookup"><span data-stu-id="e62a3-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="e62a3-140">Используйте страницу **Настройка версии калькуляции издержек** для создания одной или нескольких версий цены для стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="e62a3-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="e62a3-141">Каждая версия цены должна иметь обозначение, указывающее на то, что типом калькуляции являются **Стандартные затраты**, а также должна допускать информационное наполнение для включения данных по затратам.</span><span class="sxs-lookup"><span data-stu-id="e62a3-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="e62a3-142">**6. Подготовьте существующего клиента системы к использованию стандартных затрат.**</span><span class="sxs-lookup"><span data-stu-id="e62a3-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="e62a3-143">Клиенты, желающие изменить свои существующие номенклатуры на складскую модель стандартных затрат, должны использовать страницу **Преобразования стандартной себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="e62a3-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="e62a3-144">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="e62a3-144">Related topics</span></span>
--------

[<span data-ttu-id="e62a3-145">Обзор преобразования в стандартную себестоимость</span><span class="sxs-lookup"><span data-stu-id="e62a3-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="e62a3-146">Блоги</span><span class="sxs-lookup"><span data-stu-id="e62a3-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="e62a3-147">Блоги сообщества</span><span class="sxs-lookup"><span data-stu-id="e62a3-147">Community blogs</span></span>

- [<span data-ttu-id="e62a3-148">Порядок настройки стандартных затрат для основных материалов в Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e62a3-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="e62a3-149">Стандартные прямые трудовые затраты в Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e62a3-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)

