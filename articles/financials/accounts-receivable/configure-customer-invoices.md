---
title: "Создание накладной клиента"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="5fa46-102">Создание накладной клиента</span><span class="sxs-lookup"><span data-stu-id="5fa46-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5fa46-103">**Накладная клиента для заказа на продажу** — это счет, который организация выставляет клиенту в связи с продажей.</span><span class="sxs-lookup"><span data-stu-id="5fa46-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="5fa46-104">Этот тип накладной клиента создается на основе заказа на продажу, который содержит строки заказа и номера номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5fa46-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="5fa46-105">Коды номенклатур указываются и разносятся в главной книге.</span><span class="sxs-lookup"><span data-stu-id="5fa46-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="5fa46-106">Записи в журнале субкниги недоступны для накладной клиента для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="5fa46-107">Дополнительные сведения см. в разделе [Создание накладных по заказам на продажу](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="5fa46-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="5fa46-108">**Накладная с произвольным текстом** не связана с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="5fa46-109">Она содержит строки заказа, которые включают счета учета, описания с произвольным текстом и сумму продажи, которые вводятся пользователем.</span><span class="sxs-lookup"><span data-stu-id="5fa46-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="5fa46-110">Невозможно ввести код номенклатуры для такого типа накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="5fa46-111">Необходимо ввести соответствующие сведения о налогах.</span><span class="sxs-lookup"><span data-stu-id="5fa46-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="5fa46-112">Счет ГК для продажи показывается в каждой строке накладной, которую можно распределить по нескольким счетам ГК, щелкнув **Распределить суммы** на странице **Накладная с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="5fa46-113">Кроме того, сальдо клиента разносится на итоговый счет из профиля разноски, используемого для накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="5fa46-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="5fa46-114">Дополнительные сведения см. в </span><span class="sxs-lookup"><span data-stu-id="5fa46-114">For more information see:</span></span>

[<span data-ttu-id="5fa46-115">Создание накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="5fa46-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="5fa46-116">Создание шаблона с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="5fa46-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="5fa46-117">Назначение шаблона накладной с произвольным текстом клиенту</span><span class="sxs-lookup"><span data-stu-id="5fa46-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="5fa46-118">Формирование и разноска повторяющихся накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="5fa46-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="5fa46-119">**Предварительная накладная** — это накладная, которая подготавливается для оценки сумм в фактической накладной до того, как эта накладная будет разнесена.</span><span class="sxs-lookup"><span data-stu-id="5fa46-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="5fa46-120">Можно напечатать предварительную накладную для накладной клиента для заказа на продажу или для накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="5fa46-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="5fa46-121">Разноска и печать отдельных накладных клиентов на основании заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="5fa46-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="5fa46-122">Этот процесс используется для создания накладной, основанной на заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="5fa46-123">Это делается, если необходимо выставить накладную клиенту до доставки товаров или услуг.</span><span class="sxs-lookup"><span data-stu-id="5fa46-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="5fa46-124">При разноске накладной количество **Осталось отгрузить** для каждой номенклатуры обновляется в соответствии с итогом по количествам, по которым выставляется накладная, из выбранного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="5fa46-125">Если количества **Осталось отгрузить** и **К поставке** по всем номенклатурам заказа на продажу равны нулю, статус заказа на продажу изменяется на **Оприходовано**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="5fa46-126">Если количество **Осталось отгрузить** не равно нулю, статус заказа на продажу не меняется, и для этого заказа можно ввести дополнительные накладные.</span><span class="sxs-lookup"><span data-stu-id="5fa46-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="5fa46-127">Статус заказов на продажу можно просмотреть на странице списка **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="5fa46-128">На странице списка **Открытые накладные клиента** можно просмотреть разнесенные накладные.</span><span class="sxs-lookup"><span data-stu-id="5fa46-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="5fa46-129">Разноска и печать отдельных накладных клиентов на основе отборочных накладных и даты</span><span class="sxs-lookup"><span data-stu-id="5fa46-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="5fa46-130">Используйте этот процесс, когда для заказа на продажу разнесена одна или несколько отборочных накладных.</span><span class="sxs-lookup"><span data-stu-id="5fa46-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="5fa46-131">Накладная клиента создается на основе таких отборочных накладных и отражает внесенные в них количества.</span><span class="sxs-lookup"><span data-stu-id="5fa46-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="5fa46-132">Финансовая информация для накладной основывается на данных, введенных при разноске накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="5fa46-133">Накладную клиента можно создать на основе номенклатур строк отборочной накладной, которые уже поставлены на текущую дату, даже если по данному заказу на продажу все номенклатуры поставлены не полностью.</span><span class="sxs-lookup"><span data-stu-id="5fa46-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="5fa46-134">Например, это можно сделать, если юридическое лицо оформляет ежемесячно одну накладную для каждого клиента, в которой указываются все поставки, осуществленные в течение месяца.</span><span class="sxs-lookup"><span data-stu-id="5fa46-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="5fa46-135">Каждая отборочная накладная отражает частичную или полную поставку номенклатуры из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="5fa46-136">При разноске накладных количество **Осталось отгрузить** по каждой номенклатуре обновляется одновременно с общим количеством доставленных количеств из выбранных отборочных накладных.</span><span class="sxs-lookup"><span data-stu-id="5fa46-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="5fa46-137">Если количества **Осталось отгрузить** и **К поставке** по всем номенклатурам заказа на продажу равны нулю, статус заказа на продажу изменяется на **Оприходовано**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="5fa46-138">Если количество **Осталось отгрузить** не равно нулю, статус заказа на продажу не меняется, и для этого заказа можно ввести дополнительные накладные.</span><span class="sxs-lookup"><span data-stu-id="5fa46-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="5fa46-139">В проводки по запасам вносится номер накладной, и статус поля **Статус строки** в заказе на продажу изменяется на **Оприходовано**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="5fa46-140">Статус заказов на продажу можно просмотреть на странице списка **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="5fa46-141">Консолидация заказов на продажу или отборочных накладных для разноски</span><span class="sxs-lookup"><span data-stu-id="5fa46-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="5fa46-142">Используйте этот процесс, когда один или несколько заказов на продажу готовы к выставлению счета и требуется консолидировать их в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="5fa46-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="5fa46-143">Можно выбрать несколько накладных на странице списка **Заказ на продажу**, а затем использовать команду **Создать накладные** для их консолидации.</span><span class="sxs-lookup"><span data-stu-id="5fa46-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="5fa46-144">На странице **Разноска накладной** можно изменить параметр **Суммарный заказ**, чтобы суммировать по порядковому номеру (где для одного заказа на продажу существует несколько отборочных накладных) или по счету в накладной (где для одного счета в накладной существует несколько заказов на продажу).</span><span class="sxs-lookup"><span data-stu-id="5fa46-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="5fa46-145">Нажмите кнопку **Упорядочить**, чтобы консолидировать заказы на продажу в отдельные накладные фактуры на основании параметров **Суммарный заказ**.</span><span class="sxs-lookup"><span data-stu-id="5fa46-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="5fa46-146">Дополнительные параметры, которые изменяют поведение разноски</span><span class="sxs-lookup"><span data-stu-id="5fa46-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="5fa46-147">Следующие поля изменяют поведение процесса разноски.</span><span class="sxs-lookup"><span data-stu-id="5fa46-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fa46-148">Поле</span><span class="sxs-lookup"><span data-stu-id="5fa46-148">Field</span></span></th>
<th><span data-ttu-id="5fa46-149">Описание</span><span class="sxs-lookup"><span data-stu-id="5fa46-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fa46-150">Количество</span><span class="sxs-lookup"><span data-stu-id="5fa46-150">Quantity</span></span></td>
<td><span data-ttu-id="5fa46-151">Выберите количества, являющиеся основой для разноски документа.</span><span class="sxs-lookup"><span data-stu-id="5fa46-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="5fa46-152">Доступные параметры отличаются в зависимости от типа документа, разноска которого выполняется, такого как отборочная накладная или накладная.</span><span class="sxs-lookup"><span data-stu-id="5fa46-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="5fa46-153"><strong>Немедленная поставка</strong> — выбор всех количеств, которые были введены в поле <strong>Немедленная поставка</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="5fa46-154">Этот параметр служит для подтверждения или доставки неполного заказа.</span><span class="sxs-lookup"><span data-stu-id="5fa46-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="5fa46-155"><strong>Скомплектовано</strong> — выбор всех количеств, которые были скомплектованы.</span><span class="sxs-lookup"><span data-stu-id="5fa46-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="5fa46-156"><strong>Все</strong> — выбор всех количеств в заказе на продажу, которые еще не были обновлены в текущем типе документа.</span><span class="sxs-lookup"><span data-stu-id="5fa46-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="5fa46-157"><strong>Отборочная накладная</strong> — выбор всех количеств, которые были обновлены в отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="5fa46-158"><strong>Скомплектовано или не учитывается в запасах</strong> — выбор всех количеств, которые были скомплектованы, и всех количеств продукта, не учитываемых в запасах.</span><span class="sxs-lookup"><span data-stu-id="5fa46-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fa46-159">Разноска</span><span class="sxs-lookup"><span data-stu-id="5fa46-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="5fa46-160">Установите этот флажок, чтобы зафиксировать в журнале заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="5fa46-161">Снимите этот флажок, чтобы напечатать предварительный заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="5fa46-162"><strong>Примечание.</strong> Если достигнуто соглашение по графику оплаты, в предварительном заказе на продажу график оплаты отображаться не будет.</span><span class="sxs-lookup"><span data-stu-id="5fa46-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="5fa46-163">Графики платежей будут показаны только в фактических заказах на продажу.</span><span class="sxs-lookup"><span data-stu-id="5fa46-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fa46-164">Выбрать позднее</span><span class="sxs-lookup"><span data-stu-id="5fa46-164">Late selection</span></span></td>
<td><span data-ttu-id="5fa46-165">Этот флажок устанавливается, чтобы применить выбранный запрос позже.</span><span class="sxs-lookup"><span data-stu-id="5fa46-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="5fa46-166">Этот параметр используется для пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="5fa46-166">This option is used for batch jobs.</span></span> <span data-ttu-id="5fa46-167">Запрос выполняется при выполнении пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="5fa46-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fa46-168">Уменьшить количество</span><span class="sxs-lookup"><span data-stu-id="5fa46-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="5fa46-169">Этот параметр выбирается, чтобы автоматически уменьшить поставленное количество, когда документ разнесен, чтобы поставленное количество было равно доступным запасам.</span><span class="sxs-lookup"><span data-stu-id="5fa46-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fa46-170">Печать</span><span class="sxs-lookup"><span data-stu-id="5fa46-170">Print</span></span></td>
<td><span data-ttu-id="5fa46-171">Выберите, когда печатать документы:</span><span class="sxs-lookup"><span data-stu-id="5fa46-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="5fa46-172"><strong>Текущий</strong> — печать документов после обновления каждой накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="5fa46-173"><strong>После</strong> — печать документов после обновления всех накладных.</span><span class="sxs-lookup"><span data-stu-id="5fa46-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="5fa46-174">
<strong>Примечание.</strong> Поле <strong>Печать</strong> доступно только в том случае, если установлены флажки <strong>Печать накладной</strong>, <strong>Печать подтверждения</strong>, <strong>Печать отгрузочной накладной</strong> или <strong>Печать отборочной накладной</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="5fa46-175">Например, на странице <strong>Сортировка форм</strong> настраивается система для сортировки информации по счету в накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="5fa46-176">Можно выбрать <strong>После</strong> для печати документов партией, сортированной по счетам в накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="5fa46-177">В противном случае документы печатаются до завершения обработки, они не сортируются в порядке, указанном на странице <strong>Сортировка форм</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fa46-178">Печать накладной</span><span class="sxs-lookup"><span data-stu-id="5fa46-178">Print invoice</span></span></td>
<td><span data-ttu-id="5fa46-179">Установите этот флажок, чтобы напечатать накладную.</span><span class="sxs-lookup"><span data-stu-id="5fa46-179">Select this option to print the invoice.</span></span> <span data-ttu-id="5fa46-180">Если этот флажок не установлен, можно разнести накладную без печати.</span><span class="sxs-lookup"><span data-stu-id="5fa46-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fa46-181">Отправить сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="5fa46-181">Send e-mail</span></span></td>
<td><span data-ttu-id="5fa46-182">Установите этот флажок, чтобы отправить накладную для заказа на продажу клиенту как вложение электронной почты после разноски накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="5fa46-183">Вложения отправляются как файлы PDF и XML.</span><span class="sxs-lookup"><span data-stu-id="5fa46-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="5fa46-184">Этот флажок доступен, только если выбран параметр <strong>Включение CFD (электронные накладные)</strong> на странице <strong>Параметры электронных накладных</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="5fa46-185"><strong>Примечание.</strong> (MEX) Этот элемент управления доступен только юридическим лицам, основной адрес которых находится в Мексике.</span><span class="sxs-lookup"><span data-stu-id="5fa46-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fa46-186">Использовать назначение управления печатью</span><span class="sxs-lookup"><span data-stu-id="5fa46-186">Use print management destination</span></span></td>
<td><span data-ttu-id="5fa46-187">Установите этот флажок, чтобы использовать параметры печати, указанные для проводки, документа или модуля на странице <strong>Печать настройки управления</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fa46-188">Проверка кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="5fa46-188">Check credit limit</span></span></td>
<td><span data-ttu-id="5fa46-189">Выберите данные для анализа при выполнении проверки кредитного лимита.</span><span class="sxs-lookup"><span data-stu-id="5fa46-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="5fa46-190"><strong>Нет</strong> — проверка кредитного лимита не требуется.</span><span class="sxs-lookup"><span data-stu-id="5fa46-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="5fa46-191"><strong>Сальдо</strong> — кредитный лимит проверяется по сальдо клиента.</span><span class="sxs-lookup"><span data-stu-id="5fa46-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="5fa46-192"><strong>Сальдо + отборочная накладная или поступление продуктов</strong> — кредитный лимит проверяется по сальдо клиента и поставкам.</span><span class="sxs-lookup"><span data-stu-id="5fa46-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="5fa46-193"><strong>Сальдо+Все</strong> — кредитный лимит проверяется по сальдо клиента, поставкам и открытым заказам.</span><span class="sxs-lookup"><span data-stu-id="5fa46-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fa46-194">Корректировка по кредиту</span><span class="sxs-lookup"><span data-stu-id="5fa46-194">Credit correction</span></span></td>
<td><span data-ttu-id="5fa46-195">Установка этого флажка служит для отображения кредит-ноты в виде дебета в кодах операций.</span><span class="sxs-lookup"><span data-stu-id="5fa46-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fa46-196">Кредитовать оставшееся количество</span><span class="sxs-lookup"><span data-stu-id="5fa46-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="5fa46-197">При разноске кредит-ноты установка этого параметра позволяет сохранить остаток количества в заказе.</span><span class="sxs-lookup"><span data-stu-id="5fa46-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="5fa46-198">Если этот параметр снят, для остатка количества вводится значение ноль (0).</span><span class="sxs-lookup"><span data-stu-id="5fa46-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fa46-199">Суммарная обработка для</span><span class="sxs-lookup"><span data-stu-id="5fa46-199">Summary update for</span></span></td>
<td><span data-ttu-id="5fa46-200">Выберите способ суммирования нескольких заказов на продажу:</span><span class="sxs-lookup"><span data-stu-id="5fa46-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="5fa46-201"><strong>Нет</strong> — заказы на продажу не суммируются.</span><span class="sxs-lookup"><span data-stu-id="5fa46-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="5fa46-202">Например, для каждого заказа на продажу создается отдельная накладная.</span><span class="sxs-lookup"><span data-stu-id="5fa46-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="5fa46-203"><strong>Счет накладной</strong> — все выбранные заказы суммируются согласно критериям, заданным на странице <strong>Параметры суммарной обработки</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="5fa46-204"><strong>Заказ</strong> – выбранный диапазон заказов суммируется в один указанный заказ.</span><span class="sxs-lookup"><span data-stu-id="5fa46-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="5fa46-205">Заказы суммируются согласно критериям, заданным на странице <strong>Параметры суммарной обработки</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="5fa46-206">Если установить этот флажок, необходимо выбрать значение в поле <strong>Заказ на продажу</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="5fa46-207"><strong>Автоматически</strong> — все выбранные заказы суммируются в соответствии с критериями, заданными на странице <strong>Параметры суммарной обработки</strong>, но только если суммарная обработка была указана на странице <strong>Суммарная обработка</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="5fa46-208">Если суммарная обработка не указана, заказ разносится отдельно.</span><span class="sxs-lookup"><span data-stu-id="5fa46-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="5fa46-209"><strong>Отборочная накладная</strong> — выбранный диапазон заказов суммируется в одну накладную для каждой отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="5fa46-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="5fa46-210">Этот параметр доступен только в том случае, если выбрано значение <strong>Отборочная накладная</strong> в поле <strong>Количество</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fa46-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






