---
title: Группы управления ретробонусами
description: В этой теме описывается, как настроить группы управления ретробонусами. Группы управления ретробонусами могут использоваться при расчетах ретробонусов и могут прикрепляться к главной записи.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 2d1f8ed9def03afc97c0b4c5ea86430ff089aac6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819240"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="5ff4b-104">Группы управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="5ff4b-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5ff4b-105">Расчеты ретробонусов и вычетов могут управляться группами.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="5ff4b-106">Группы управления ретробонусами могут создаваться для клиентов, поставщиков и номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="5ff4b-107">Они могут быть привязаны к главной записи.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="5ff4b-108">Группы клиентов для управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="5ff4b-108">Rebate management customer groups</span></span>

<span data-ttu-id="5ff4b-109">Расчет для группы клиентов часто создается для цепочки компаний, например, сеть супермаркетов или франчайзинговая компания.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="5ff4b-110">Этот тип расчета обычно относится к ретробонусу.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="5ff4b-111">Вычет часто рассчитывается без учета того, кому был продан соответствующий заказ.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="5ff4b-112">Однако есть исключения.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-112">However, there are exceptions.</span></span> <span data-ttu-id="5ff4b-113">Например, лицензиат может создать схему вычетов, в которой группа клиентов A получит 4 процента, но группа клиентов B получит только 3 процента.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="5ff4b-114">Настройка групп клиентов</span><span class="sxs-lookup"><span data-stu-id="5ff4b-114">Set up customer groups</span></span>

<span data-ttu-id="5ff4b-115">Для работы с группами клиентов по управлению ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="5ff4b-116">Можно использовать кнопки на панели операций для добавления и удаления групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5ff4b-117">Для каждой группы установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="5ff4b-118">**Группа управления ретробонусами** — введите уникальное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5ff4b-119">**Описание** — введите описание группы, чтобы предоставить дополнительную информацию о том, как она должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="5ff4b-120">Управление назначениями групп клиентов</span><span class="sxs-lookup"><span data-stu-id="5ff4b-120">Manage customer group assignments</span></span>

<span data-ttu-id="5ff4b-121">Каждый клиент может принадлежать любому числу групп управления ретробонусами.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5ff4b-122">Для просмотра и назначения участников группы можно начать со списка группы или списка клиентов.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="5ff4b-123">Чтобы просмотреть, добавить или удалить клиентов для выбранной группы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-124">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы клиентов**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="5ff4b-125">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-125">Select the group to manage.</span></span>
1. <span data-ttu-id="5ff4b-126">На панели операций выберите **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="5ff4b-127">Отображается страница **Группы управления ретробонусами**, на которой отображается список клиентов, которые уже являются участниками выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="5ff4b-128">Чтобы добавить нового клиента в группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5ff4b-129">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5ff4b-130">**Учетная запись клиента** — выберите идентификатор учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="5ff4b-131">**Имя** — введите имя и/или описание клиента.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="5ff4b-132">Чтобы удалить клиента из группы, выберите клиента, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5ff4b-133">Чтобы просмотреть, добавить или удалить назначения группы для выбранного клиента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-134">Перейдите в раздел **Расчеты с клиентами \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="5ff4b-135">Выберите клиента, с которым необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="5ff4b-136">В области действий на вкладке **Клиент** в группе **Управление ретробонусами** выберите **Группы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5ff4b-137">Отображается страница **Группы управления ретробонусами**, на которой отображается список групп, в которые уже входит выбранный клиент.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="5ff4b-138">Чтобы добавить клиента в новую группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5ff4b-139">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5ff4b-140">**Группа управления ретробонусами** — выберите группу, в которую требуется добавить клиента.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="5ff4b-141">**Описание** — введите описание группы (например, чтобы объяснить, почему клиент является ее участником).</span><span class="sxs-lookup"><span data-stu-id="5ff4b-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="5ff4b-142">Чтобы удалить клиента из группы, выберите группу, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="5ff4b-143">Группы поставщиков для управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="5ff4b-143">Rebate management vendor groups</span></span>

<span data-ttu-id="5ff4b-144">Расчет для группы поставщиков часто создается для группы точек доставки.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="5ff4b-145">Этот тип расчета обычно относится к ретробонусу.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="5ff4b-146">Настройка групп поставщиков</span><span class="sxs-lookup"><span data-stu-id="5ff4b-146">Set up vendor groups</span></span>

<span data-ttu-id="5ff4b-147">Для работы с группами поставщиков по управлению ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="5ff4b-148">Можно использовать кнопки на панели операций для добавления и удаления групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5ff4b-149">Для каждой группы установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="5ff4b-150">**Группа управления ретробонусами** — введите уникальное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5ff4b-151">**Описание** — введите описание группы, чтобы предоставить дополнительную информацию о том, как она должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="5ff4b-152">Управление назначениями групп поставщиков</span><span class="sxs-lookup"><span data-stu-id="5ff4b-152">Manage vendor group assignments</span></span>

<span data-ttu-id="5ff4b-153">Каждый поставщик может принадлежать любому числу групп управления ретробонусами.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5ff4b-154">Для просмотра и назначения участников группы можно начать со списка группы или списка поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="5ff4b-155">Чтобы просмотреть, добавить или удалить поставщиков для выбранной группы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-156">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="5ff4b-157">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-157">Select the group to manage.</span></span>
1. <span data-ttu-id="5ff4b-158">На панели операций выберите **Поставщики**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="5ff4b-159">Отображается страница **Группы управления ретробонусами**, на которой отображается список поставщиков, которые уже являются участниками выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="5ff4b-160">Чтобы добавить поставщика в группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5ff4b-161">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5ff4b-162">**Учетная запись поставщика** — выберите идентификатор учетной записи поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="5ff4b-163">**Имя** — введите имя и/или описание поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="5ff4b-164">Чтобы удалить поставщика из группы, выберите поставщика, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5ff4b-165">Чтобы просмотреть, добавить или удалить назначения группы для выбранного поставщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-166">Перейдите в раздел **Расчеты с поставщиками \> Поставщики \> Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="5ff4b-167">Выберите поставщика, с которым необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="5ff4b-168">В области действий на вкладке **Поставщик** в группе **Управление ретробонусами** выберите **Группы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5ff4b-169">Отображается страница **Группы управления ретробонусами**, на которой отображается список групп, в которые уже входит выбранный поставщик.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="5ff4b-170">Чтобы добавить поставщика в новую группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5ff4b-171">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5ff4b-172">**Группа управления ретробонусами** — выберите группу, в которую требуется добавить поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="5ff4b-173">**Описание** — введите описание группы (например, чтобы объяснить, почему поставщик является ее участником).</span><span class="sxs-lookup"><span data-stu-id="5ff4b-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="5ff4b-174">Чтобы удалить поставщика из группы, выберите группу, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="5ff4b-175">Группы бонусов номенклатуры</span><span class="sxs-lookup"><span data-stu-id="5ff4b-175">Item rebate groups</span></span>

<span data-ttu-id="5ff4b-176">Путем группировки номенклатур обеспечивается большая гибкость при расчете ретробонусов и вычетов.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="5ff4b-177">Такой подход часто является более эффективным способом настройки ретробонусов и вычетов для клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="5ff4b-178">Настройка групп номенклатуры</span><span class="sxs-lookup"><span data-stu-id="5ff4b-178">Set up item groups</span></span>

<span data-ttu-id="5ff4b-179">Для работы с группами номенклатур по управлению ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="5ff4b-180">Можно использовать кнопки на панели операций для добавления и удаления групп по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="5ff4b-181">Для каждой группы установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="5ff4b-182">**Группа управления ретробонусами** — введите уникальное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="5ff4b-183">**Описание** — введите описание группы, чтобы предоставить дополнительную информацию о том, как она должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="5ff4b-184">Управление назначениями групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="5ff4b-184">Manage item group assignments</span></span>

<span data-ttu-id="5ff4b-185">Каждая номенклатура может принадлежать любому числу групп управления ретробонусами.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="5ff4b-186">Для просмотра и назначения участников группы можно начать со списка группы или списка номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="5ff4b-187">Можно также добавлять номенклатуры, используя иерархию категорий.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="5ff4b-188">Чтобы просмотреть, добавить или удалить номенклатуры для выбранной группы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-189">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="5ff4b-190">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-190">Select the group to manage.</span></span>
1. <span data-ttu-id="5ff4b-191">В области действий выберите **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="5ff4b-192">Отображается страница **Группы управления ретробонусами**, на которой отображается список номенклатур, которые уже являются участниками выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="5ff4b-193">Чтобы добавить номенклатуру в группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5ff4b-194">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5ff4b-195">**Учетная запись номенклатуры** — выберите идентификатор учетной записи номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="5ff4b-196">**Название продукта** — введите название и/или описание продукта.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="5ff4b-197">Чтобы удалить номенклатуру из группы, выберите номенклатуру, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5ff4b-198">Чтобы просмотреть, добавить или удалить назначения группы для выбранной номенклатуры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-199">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5ff4b-200">Выберите номенклатуру, с которой необходимо работать.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-200">Select the item to work with.</span></span>
1. <span data-ttu-id="5ff4b-201">В области действий на вкладке **Продукт** в группе **Управление ретробонусами** выберите **Группы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="5ff4b-202">Отображается страница **Группы управления ретробонусами**, на которой отображается список групп, в которые уже входит выбранная номенклатура.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="5ff4b-203">Чтобы добавить номенклатуру в новую группу, выберите **Создать** на панели действий, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="5ff4b-204">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5ff4b-205">**Группа управления ретробонусами** — выберите группу, в которую требуется добавить номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="5ff4b-206">**Описание** — введите описание группы (например, чтобы объяснить, почему номенклатура является ее участником).</span><span class="sxs-lookup"><span data-stu-id="5ff4b-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="5ff4b-207">Чтобы удалить номенклатуру из группы, выберите группу, затем выберите **Удалить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="5ff4b-208">Чтобы добавить номенклатуры в группу на основе иерархии категорий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5ff4b-209">Перейдите в раздел **Управление ретробонусами \> Настройка групп управления ретробонусами \> Группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="5ff4b-210">Выберите группу для управления.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-210">Select the group to manage.</span></span>
1. <span data-ttu-id="5ff4b-211">В области действий выберите **Добавить номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="5ff4b-212">В диалоговом окне **Добавить номенклатуры** в поле **Иерархия категорий** выберите категорию верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="5ff4b-213">Иерархия номенклатур открывается в левой области.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="5ff4b-214">Выберите уровень иерархии, который вы ищете.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="5ff4b-215">Номенклатуры из выбранной иерархии и уровня иерархии отображаются в правой области.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="5ff4b-216">Для работы с панелью выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5ff4b-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="5ff4b-217">Установите флажок для каждой номенклатуры, которую следует добавить.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="5ff4b-218">Установите флажок в заголовке сетки, чтобы выбрать все перечисленные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="5ff4b-219">Выберите кнопку **Показать выбранные**, чтобы выполнить фильтрацию сетки так, чтобы отображались только те номенклатуры, которые были выбраны на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="5ff4b-220">Снова выберите эту кнопку, чтобы вернуться к полному списку.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="5ff4b-221">Выберите **ОК**, чтобы применить выбранные номенклатуры к выбранной группе.</span><span class="sxs-lookup"><span data-stu-id="5ff4b-221">Select **OK** to apply your item selection to the selected group.</span></span>
