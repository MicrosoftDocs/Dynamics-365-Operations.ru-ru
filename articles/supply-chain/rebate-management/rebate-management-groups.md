---
title: Группы управления ретробонусами
description: В этой теме описывается, как настроить группы управления ретробонусами. Группы управления ретробонусами могут использоваться при расчетах ретробонусов и могут прикрепляться к главной записи.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271085"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="082d9-104">Группы управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="082d9-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="082d9-105">Расчеты управления ретробонусами могут управляться группами.</span><span class="sxs-lookup"><span data-stu-id="082d9-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="082d9-106">Группы управления ретробонусами могут создаваться для клиентов, поставщиков и номенклатур.</span><span class="sxs-lookup"><span data-stu-id="082d9-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="082d9-107">Они могут быть привязаны к главной записи.</span><span class="sxs-lookup"><span data-stu-id="082d9-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="082d9-108">Группы клиентов для управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="082d9-108">Rebate management customer groups</span></span>

<span data-ttu-id="082d9-109">Расчет для группы клиентов часто создается для цепочки компаний, например, сеть супермаркетов или франчайзинговая компания.</span><span class="sxs-lookup"><span data-stu-id="082d9-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="082d9-110">Этот тип расчета обычно относится к ретробонусу.</span><span class="sxs-lookup"><span data-stu-id="082d9-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="082d9-111">Вычет часто рассчитывается без учета того, кому был продан соответствующий заказ.</span><span class="sxs-lookup"><span data-stu-id="082d9-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="082d9-112">Однако есть исключения.</span><span class="sxs-lookup"><span data-stu-id="082d9-112">However, there are exceptions.</span></span> <span data-ttu-id="082d9-113">Например, лицензиат может создать схему вычетов, в которой группа клиентов A получит 4 процента, но группа клиентов B получит только 3 процента.</span><span class="sxs-lookup"><span data-stu-id="082d9-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="082d9-114">Настройка групп клиентов</span><span class="sxs-lookup"><span data-stu-id="082d9-114">Set up customer groups</span></span>

<span data-ttu-id="082d9-115">Для работы с группами клиентов по управлению ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="082d9-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="082d9-116">Можно использовать кнопки на панели операций для добавления и удаления групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="082d9-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="082d9-117">Для каждой группы установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="082d9-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="082d9-118">**Группа управления ретробонусами** — введите уникальное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="082d9-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="082d9-119">**Описание** — введите описание группы, чтобы предоставить дополнительную информацию о том, как она должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="082d9-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="082d9-120">Управление назначениями групп клиентов</span><span class="sxs-lookup"><span data-stu-id="082d9-120">Manage customer group assignments</span></span>

<span data-ttu-id="082d9-121">Каждый клиент может принадлежать любому числу групп управления ретробонусами.</span><span class="sxs-lookup"><span data-stu-id="082d9-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="082d9-122">Для просмотра и назначения участников группы можно начать со списка группы или списка клиентов.</span><span class="sxs-lookup"><span data-stu-id="082d9-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="082d9-123">Чтобы просмотреть, добавить или удалить клиентов для выбранной группы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="082d9-124">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="082d9-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="082d9-125">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="082d9-125">Select the group to manage.</span></span>
1. <span data-ttu-id="082d9-126">На панели операций выберите **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="082d9-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="082d9-127">Отображается страница **Группы управления ретробонусами**, на которой отображается список клиентов, которые уже являются участниками выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="082d9-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="082d9-128">Чтобы добавить нового клиента в группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="082d9-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="082d9-129">Затем задайте следующее поле для новой строки:</span><span class="sxs-lookup"><span data-stu-id="082d9-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="082d9-130">**Учетная запись клиента** — выберите идентификатор учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="082d9-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="082d9-131">Чтобы удалить клиента из группы, выберите клиента, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="082d9-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="082d9-132">Чтобы просмотреть, добавить или удалить назначения группы для выбранного клиента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="082d9-133">Перейдите в раздел **Расчеты с клиентами \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="082d9-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="082d9-134">Выберите клиента, с которым необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="082d9-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="082d9-135">В области действий на вкладке **Клиент** в группе **Управление ретробонусами** выберите **Группы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="082d9-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="082d9-136">Отображается страница **Группы управления ретробонусами**, на которой отображается список групп, в которые уже входит выбранный клиент.</span><span class="sxs-lookup"><span data-stu-id="082d9-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="082d9-137">Чтобы добавить клиента в новую группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="082d9-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="082d9-138">Затем задайте следующее поле для новой строки:</span><span class="sxs-lookup"><span data-stu-id="082d9-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="082d9-139">**Группа управления ретробонусами** — выберите группу, в которую требуется добавить клиента.</span><span class="sxs-lookup"><span data-stu-id="082d9-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="082d9-140">Чтобы удалить клиента из группы, выберите группу, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="082d9-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="082d9-141">Группы поставщиков для управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="082d9-141">Rebate management vendor groups</span></span>

<span data-ttu-id="082d9-142">Расчет для группы поставщиков часто создается для группы точек доставки.</span><span class="sxs-lookup"><span data-stu-id="082d9-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="082d9-143">Этот тип расчета обычно относится к ретробонусу.</span><span class="sxs-lookup"><span data-stu-id="082d9-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="082d9-144">Настройка групп поставщиков</span><span class="sxs-lookup"><span data-stu-id="082d9-144">Set up vendor groups</span></span>

<span data-ttu-id="082d9-145">Для работы с группами поставщиков по управлению ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="082d9-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="082d9-146">Можно использовать кнопки на панели операций для добавления и удаления групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="082d9-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="082d9-147">Для каждой группы установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="082d9-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="082d9-148">**Группа управления ретробонусами** — введите уникальное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="082d9-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="082d9-149">**Описание** — введите описание группы, чтобы предоставить дополнительную информацию о том, как она должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="082d9-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="082d9-150">Управление назначениями групп поставщиков</span><span class="sxs-lookup"><span data-stu-id="082d9-150">Manage vendor group assignments</span></span>

<span data-ttu-id="082d9-151">Каждый поставщик может принадлежать любому числу групп управления ретробонусами.</span><span class="sxs-lookup"><span data-stu-id="082d9-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="082d9-152">Для просмотра и назначения участников группы можно начать со списка группы или списка поставщиков.</span><span class="sxs-lookup"><span data-stu-id="082d9-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="082d9-153">Чтобы просмотреть, добавить или удалить поставщиков для выбранной группы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="082d9-154">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="082d9-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="082d9-155">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="082d9-155">Select the group to manage.</span></span>
1. <span data-ttu-id="082d9-156">На панели операций выберите **Поставщики**.</span><span class="sxs-lookup"><span data-stu-id="082d9-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="082d9-157">Отображается страница **Группы управления ретробонусами**, на которой отображается список поставщиков, которые уже являются участниками выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="082d9-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="082d9-158">Чтобы добавить поставщика в группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="082d9-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="082d9-159">Затем задайте следующее поле для новой строки:</span><span class="sxs-lookup"><span data-stu-id="082d9-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="082d9-160">**Учетная запись поставщика** — выберите идентификатор учетной записи поставщика.</span><span class="sxs-lookup"><span data-stu-id="082d9-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="082d9-161">Чтобы удалить поставщика из группы, выберите поставщика, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="082d9-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="082d9-162">Чтобы просмотреть, добавить или удалить назначения группы для выбранного поставщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="082d9-163">Перейдите в раздел **Расчеты с поставщиками \> Поставщики \> Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="082d9-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="082d9-164">Выберите поставщика, с которым необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="082d9-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="082d9-165">В области действий на вкладке **Поставщик** в группе **Управление ретробонусами** выберите **Группы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="082d9-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="082d9-166">Отображается страница **Группы управления ретробонусами**, на которой отображается список групп, в которые уже входит выбранный поставщик.</span><span class="sxs-lookup"><span data-stu-id="082d9-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="082d9-167">Чтобы добавить поставщика в новую группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="082d9-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="082d9-168">Затем задайте следующее поле для новой строки:</span><span class="sxs-lookup"><span data-stu-id="082d9-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="082d9-169">**Группа управления ретробонусами** — выберите группу, в которую требуется добавить поставщика.</span><span class="sxs-lookup"><span data-stu-id="082d9-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="082d9-170">Чтобы удалить поставщика из группы, выберите группу, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="082d9-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="082d9-171">Группы бонусов номенклатуры</span><span class="sxs-lookup"><span data-stu-id="082d9-171">Item rebate groups</span></span>

<span data-ttu-id="082d9-172">Путем группировки номенклатур обеспечивается большая гибкость при расчете ретробонусов и вычетов.</span><span class="sxs-lookup"><span data-stu-id="082d9-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="082d9-173">Такой подход часто является более эффективным способом настройки ретробонусов и вычетов для клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="082d9-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="082d9-174">Настройка групп номенклатуры</span><span class="sxs-lookup"><span data-stu-id="082d9-174">Set up item groups</span></span>

<span data-ttu-id="082d9-175">Для работы с группами номенклатур по управлению ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="082d9-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="082d9-176">Можно использовать кнопки на панели операций для добавления и удаления групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="082d9-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="082d9-177">Для каждой группы установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="082d9-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="082d9-178">**Группа управления ретробонусами** — введите уникальное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="082d9-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="082d9-179">**Описание** — введите описание группы, чтобы предоставить дополнительную информацию о том, как она должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="082d9-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="082d9-180">Управление назначениями групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="082d9-180">Manage item group assignments</span></span>

<span data-ttu-id="082d9-181">Каждая номенклатура может принадлежать любому числу групп управления ретробонусами.</span><span class="sxs-lookup"><span data-stu-id="082d9-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="082d9-182">Для просмотра и назначения участников группы можно начать со списка группы или списка номенклатур.</span><span class="sxs-lookup"><span data-stu-id="082d9-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="082d9-183">Можно также добавлять номенклатуры, используя иерархию категорий.</span><span class="sxs-lookup"><span data-stu-id="082d9-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="082d9-184">Чтобы просмотреть, добавить или удалить номенклатуры для выбранной группы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="082d9-185">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="082d9-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="082d9-186">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="082d9-186">Select the group to manage.</span></span>
1. <span data-ttu-id="082d9-187">В области действий выберите **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="082d9-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="082d9-188">Отображается страница **Группы управления ретробонусами**, на которой отображается список номенклатур, которые уже являются участниками выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="082d9-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="082d9-189">Чтобы добавить номенклатуру в группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="082d9-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="082d9-190">Затем задайте следующее поле для новой строки:</span><span class="sxs-lookup"><span data-stu-id="082d9-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="082d9-191">**Учетная запись номенклатуры** — выберите идентификатор учетной записи номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="082d9-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="082d9-192">Чтобы удалить номенклатуру из группы, выберите номенклатуру, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="082d9-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="082d9-193">Чтобы просмотреть, добавить или удалить назначения группы для выбранной номенклатуры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="082d9-194">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="082d9-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="082d9-195">Выберите номенклатуру, с которой необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="082d9-195">Select the item to work with.</span></span>
1. <span data-ttu-id="082d9-196">В области действий на вкладке **Продукт** в группе **Управление ретробонусами** выберите **Группы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="082d9-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="082d9-197">Отображается страница **Группы управления ретробонусами**, на которой отображается список групп, в которые уже входит выбранная номенклатура.</span><span class="sxs-lookup"><span data-stu-id="082d9-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="082d9-198">Чтобы добавить номенклатуру в новую группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="082d9-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="082d9-199">Затем задайте следующее поле для новой строки:</span><span class="sxs-lookup"><span data-stu-id="082d9-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="082d9-200">**Группа управления ретробонусами** — выберите группу, в которую требуется добавить номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="082d9-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="082d9-201">Чтобы удалить номенклатуру из группы, выберите группу, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="082d9-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="082d9-202">Чтобы добавить номенклатуры в группу на основе иерархии категорий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="082d9-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="082d9-203">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="082d9-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="082d9-204">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="082d9-204">Select the group to manage.</span></span>
1. <span data-ttu-id="082d9-205">В области действий выберите **Добавить номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="082d9-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="082d9-206">В диалоговом окне **Добавить номенклатуры** в поле **Иерархия категорий** выберите категорию верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="082d9-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="082d9-207">Иерархия номенклатур открывается в левой области.</span><span class="sxs-lookup"><span data-stu-id="082d9-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="082d9-208">Выберите уровень иерархии, который вы ищете.</span><span class="sxs-lookup"><span data-stu-id="082d9-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="082d9-209">Номенклатуры из выбранной иерархии и уровня иерархии отображаются в правой области.</span><span class="sxs-lookup"><span data-stu-id="082d9-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="082d9-210">Для работы с панелью выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="082d9-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="082d9-211">Установите флажок для каждой номенклатуры, которую следует добавить.</span><span class="sxs-lookup"><span data-stu-id="082d9-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="082d9-212">Установите флажок в заголовке сетки, чтобы выбрать все перечисленные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="082d9-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="082d9-213">Выберите кнопку **Показать выбранные**, чтобы выполнить фильтрацию сетки так, чтобы отображались только те номенклатуры, которые были выбраны на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="082d9-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="082d9-214">Снова выберите эту кнопку, чтобы вернуться к полному списку.</span><span class="sxs-lookup"><span data-stu-id="082d9-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="082d9-215">Выберите **ОК**, чтобы применить выбранные номенклатуры к выбранной группе.</span><span class="sxs-lookup"><span data-stu-id="082d9-215">Select **OK** to apply your item selection to the selected group.</span></span>
