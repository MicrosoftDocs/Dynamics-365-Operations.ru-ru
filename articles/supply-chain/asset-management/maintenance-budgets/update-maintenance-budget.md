---
title: Обновление бюджетов обслуживания
description: В этом разделе объясняется, как обновить бюджет обслуживания в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 486782968816cc585d9cf2d753f32e82f85e4f7e
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874793"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="9f7b6-103">Обновление бюджетов обслуживания</span><span class="sxs-lookup"><span data-stu-id="9f7b6-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9f7b6-104">На странице **Строки бюджета обслуживания** отображаются все строки бюджета, которые были созданы для бюджета, выбранного на странице **Бюджеты обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="9f7b6-105">(Дополнительные сведения см. в разделе [Создание бюджетов обслуживания](create-maintenance-budget.md).) Строки бюджета обслуживания можно пересчитывать и корректировать до тех пор, пока бюджет обслуживания не утвержден.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="9f7b6-106">После прохождения бюджетного периода и разноски затрат в управлении активами можно также обновить строки бюджета фактическими затратами.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="9f7b6-107">Пересчет бюджета обслуживания</span><span class="sxs-lookup"><span data-stu-id="9f7b6-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="9f7b6-108">Пересчет бюджета обслуживания можно выполнить на странице **Строки бюджета обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="9f7b6-109">При пересчете бюджета обслуживания существующие строки бюджета удаляются, и выполняется новое вычисление.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="9f7b6-110">На странице **Строки бюджета обслуживания** выберите **Пересчитать**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="9f7b6-111">В диалоговом окне **Пересчитать бюджет** выполните необходимые изменения для нового расчета, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="9f7b6-112">Новые строки бюджета создаются в соответствии с заданными значениями.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="9f7b6-113">Корректировка строк бюджета</span><span class="sxs-lookup"><span data-stu-id="9f7b6-113">Adjust budget lines</span></span>

<span data-ttu-id="9f7b6-114">Вместо пересчета всего бюджета обслуживания можно скорректировать выбранные строки, которые относятся к бюджетным затратам.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="9f7b6-115">На странице **Строки бюджета обслуживания** выберите строки, для которых необходимо обновить бюджетные затраты.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="9f7b6-116">Выберите **Корректировка**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="9f7b6-117">Чтобы добавить сумму к выбранным строкам, установите флажок **Добавить затраты**, затем введите значение в поле **Добавить значение**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="9f7b6-118">Чтобы умножить бюджетные затраты в выбранных строках бюджета на коэффициент, установите флажок **Умножить затраты** и введите коэффициент в поле **Значение коэффициента**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="9f7b6-119">Например, если ввести **1,2** в поле **Значение коэффициента**, бюджетные затраты в выбранных строках будут увеличены на 20 процентов.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="9f7b6-120">Если ввести **0,7**, бюджетные затраты по выбранным строкам будут уменьшены на 30 процентов.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="9f7b6-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-121">Select **OK**.</span></span>

<span data-ttu-id="9f7b6-122">Выбранные строки бюджета обновляются в соответствии со значениями, заданными на шаге 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="9f7b6-123">Обновление фактических затрат</span><span class="sxs-lookup"><span data-stu-id="9f7b6-123">Update actual costs</span></span>

<span data-ttu-id="9f7b6-124">После прохождения дат строк бюджета разноски фактических затрат в управлении активами можно также обновить бюджет обслуживания с использованием фактических затрат.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="9f7b6-125">На странице **Строки бюджета обслуживания** выберите **Обновить затраты**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="9f7b6-126">В диалоговом окне **Вычислить фактические затраты** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="9f7b6-127">Поля **Фактические затраты** в строках бюджета обновляются, если фактические затраты были разнесены.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="9f7b6-128">Новые строки бюджета могут быть созданы, если новые типы активов были созданы после создания бюджета, и если эти типы активов были использованы в активах, для которых были созданы заказы на работу и для которых были разнесены соответствующие затраты.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="9f7b6-129">В новых строках бюджета отображаются только фактические затраты, поскольку для них не были рассчитаны бюджетные затраты.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="9f7b6-130">Чтобы просмотреть обзор фактических затрат, разделенных на профилактические, корректирующие и инвестиционные затраты, можно выполнить расчет для одного и того же периода на странице **Управление затратами по активам**.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="9f7b6-131">Добавление строк бюджета вручную</span><span class="sxs-lookup"><span data-stu-id="9f7b6-131">Manually add budget lines</span></span>

<span data-ttu-id="9f7b6-132">На странице **Строки бюджета обслуживания** можно вручную добавить новую строку бюджета, выбрав **Создать**, затем сделав выбор в строке.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="9f7b6-133">Ниже приведены несколько примеров ситуаций, в которых такой подход может быть полезен:</span><span class="sxs-lookup"><span data-stu-id="9f7b6-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="9f7b6-134">Известно, что ремонт некоторых активов в данный момент находится на этапе планирования, но в управлении активами еще не были созданы соответствующие задания.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="9f7b6-135">Однако требуется включить в бюджет обслуживания бюджетные затраты для этих заданий.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="9f7b6-136">Новые активы или типы активов были созданы после того, как был подготовлен бюджет обслуживания, но планы обслуживания еще не были настроены для этих активов или типов активов.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="9f7b6-137">Однако требуется включить в бюджет обслуживания бюджетные затраты для этих типов активов.</span><span class="sxs-lookup"><span data-stu-id="9f7b6-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>