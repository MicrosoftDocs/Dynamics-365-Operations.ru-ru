---
title: Распределения по бухгалтерским счетам и записи в журнале для накладных поставщиков
description: Распределения по бухгалтерским счетам используются, чтобы определить, как будет включена сумма. Например, как расходы, налоги или начисления будут включены в накладную поставщика. На каждую сумму, которая должна быть включена в накладную поставщика, будет приходится одно или несколько распределений по бухгалтерским счетам.
author: abruer
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 513066a597620450f0b482e98e36d31c6f2c980a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189101"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a><span data-ttu-id="610d1-104">Распределения по бухгалтерским счетам и записи в журнале для накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="610d1-104">Accounting distributions and journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="610d1-105">Распределения по бухгалтерским счетам используются, чтобы определить, как будет включена сумма. Например, как расходы, налоги или начисления будут включены в накладную поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="610d1-106">На каждую сумму, которая должна быть включена в накладную поставщика, будет приходится одно или несколько распределений по бухгалтерским счетам.</span><span class="sxs-lookup"><span data-stu-id="610d1-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

## <a name="accounting-distributions"></a><span data-ttu-id="610d1-107">Распределение по бухгалтерским счетам</span><span class="sxs-lookup"><span data-stu-id="610d1-107">Accounting distributions</span></span> 

<span data-ttu-id="610d1-108">Можно использовать следующие кнопки на странице "Накладная поставщика", чтобы просматривать и по возможности изменять распределения по бухгалтерским счетам для каждой суммы в накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="610d1-109">**Распределить суммы** – Просмотр и изменение распределений по бухгалтерским счетам для отдельной строки и любых дочерних строк, например для налогов и начислений.</span><span class="sxs-lookup"><span data-stu-id="610d1-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="610d1-110">Вы можете также просмотреть и изменить распределения по бухгалтерским счетам для дочерней строки непосредственно со страницы "Налоговые проводки" или "Проводки по накладным расходам".</span><span class="sxs-lookup"><span data-stu-id="610d1-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="610d1-111">Измените суммы заголовка накладной поставщика (например, начисления и суммы округления валюты).</span><span class="sxs-lookup"><span data-stu-id="610d1-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="610d1-112">Измените суммы строки накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="610d1-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="610d1-113">**Просмотр распределений** — Просмотр распределений по бухгалтерским счетам для всех строк документа.</span><span class="sxs-lookup"><span data-stu-id="610d1-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="610d1-114">В этом представлении изменять распределения по бухгалтерским счетам нельзя.</span><span class="sxs-lookup"><span data-stu-id="610d1-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="610d1-115">Просмотрите суммы заголовка и строк.</span><span class="sxs-lookup"><span data-stu-id="610d1-115">View header and line amounts.</span></span>

<span data-ttu-id="610d1-116">Если накладная поставщика ссылается на заказ на покупку, вы можете разделить и изменить распределения по бухгалтерским счетам для строк, в которых содержатся не учитываемые в запасах номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="610d1-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="610d1-117">Если строка накладной поставщика не ссылается на строку заказа на покупку, вы также можете удалить распределения по бухгалтерским счетам.</span><span class="sxs-lookup"><span data-stu-id="610d1-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="610d1-118">Вы не можете разделить или удалить строки для расходов, налогов и скидок по строкам.</span><span class="sxs-lookup"><span data-stu-id="610d1-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="610d1-119">Вы можете изменить счет учета, но не суммы или проценты.</span><span class="sxs-lookup"><span data-stu-id="610d1-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="610d1-120">Если родительская строка содержит не учитываемую в запасах номенклатуру и распределения по бухгалтерским счетам разделяются, дочерняя строка будет разделена автоматически в соответствии с финансовыми аналитиками родительской строки.</span><span class="sxs-lookup"><span data-stu-id="610d1-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="610d1-121">Распределения по бухгалтерским счетам для дочерней строки нельзя дополнительно разделить или удалить, однако, в зависимости от настройки дочерней строки, для ее распределений по бухгалтерским счетам можно изменить счет в книге учета.</span><span class="sxs-lookup"><span data-stu-id="610d1-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="610d1-122">Распределение сумм</span><span class="sxs-lookup"><span data-stu-id="610d1-122">Distributing amounts</span></span>
<span data-ttu-id="610d1-123">При вводе накладной поставщика каждая сумма распределяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="610d1-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="610d1-124">Тип строки накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="610d1-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="610d1-125">Порядок или приоритет, который определяет, откуда отображается счет ГК.</span><span class="sxs-lookup"><span data-stu-id="610d1-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="610d1-126">Порядок приоритетов, определяющий финансовую аналитику, отображаемую по умолчанию</span><span class="sxs-lookup"><span data-stu-id="610d1-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="610d1-127">Учитываемый в запасах продукт</span><span class="sxs-lookup"><span data-stu-id="610d1-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-128">Распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-129">Поле "Счет ГК", если на странице "Разноска" выбрано значение "Расход на покупку для продукта".</span><span class="sxs-lookup"><span data-stu-id="610d1-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-130">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-131">Используйте значения финансовой аналитики по умолчанию для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610d1-132">Категория закупки или продукта, не учитываемые в запасах</span><span class="sxs-lookup"><span data-stu-id="610d1-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-133">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-134">Поле "Счет ГК", если на странице "Разноска" выбрано значение "Расходы по закупкам для нескладируемой номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="610d1-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-135">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-136">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="610d1-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="610d1-137">Используйте значения финансовой аналитики по умолчанию для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="610d1-138">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-139">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="610d1-140">Актив</span><span class="sxs-lookup"><span data-stu-id="610d1-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-141">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-142">Если значение "Ввод в эксплуатацию" выбрано в поле "Тип проводки" в форме "Накладная поставщика", поле "Счет ГК", когда значение "Ввод в эксплуатацию" выбрано на странице "Профили разноски основных средств".</span><span class="sxs-lookup"><span data-stu-id="610d1-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="610d1-143">Если значение "Переоценка стоимости ввода в эксплуатацию" выбрано в поле "Тип проводки", поле "Счет ГК", когда значение "Переоценка стоимости ввода в эксплуатацию" выбрано на странице "Профили разноски основных средств".</span><span class="sxs-lookup"><span data-stu-id="610d1-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-144">Используйте распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-145">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-146">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610d1-147">Проект, определенные в строке накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="610d1-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-148">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-149">Если в поле "Разноска себестоимости - Номенклатура" выбрано значение "Сальдо", поле "Счет ГК", когда значение "Затраты" выбрано на странице "Настройка разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="610d1-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="610d1-150">Если в поле "Разноска себестоимости - Номенклатура" выбрано значение "Прибыли и убытки", поле "Счет ГК", когда значение "Себестоимость - Номенклатура" выбрано на странице "Настройка разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="610d1-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-151">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="610d1-152">Скидка по строке</span><span class="sxs-lookup"><span data-stu-id="610d1-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-153">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-154">Поле "Счет ГК", если на странице "Разноска" выбрано значение "Скидка".</span><span class="sxs-lookup"><span data-stu-id="610d1-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="610d1-155">Если счет ГК скидки не определен в профиле разноски, то распределение по бухгалтерским счетам для суммы без учета скидок и наценок будет в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-156">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-157">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-158">Используйте значения финансовой аналитики для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-159">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610d1-160">Расходы на покупку, введенные на вкладке "Цена и скидка" строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="610d1-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-161">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-162">Распределение по бухгалтерским счетам для суммы без учета скидок и наценок в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-163">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-164">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="610d1-165">Расходы по строке</span><span class="sxs-lookup"><span data-stu-id="610d1-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-166">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-167">Если "Счет ГК" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Дебетовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="610d1-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="610d1-168">Если выбрана "Номенклатура" в поле дебета "Тип" в форме "Код накладных расходов", распределение по бухгалтерским счетам для суммы без учета скидок и наценок в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-169">Если "Клиент/поставщик" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Кредитовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="610d1-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-170">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-171">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-172">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-173">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610d1-174">Налоги, со следующим условием:</span><span class="sxs-lookup"><span data-stu-id="610d1-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="610d1-175">Флажок "Применить правила налогообложения США" установлен на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="610d1-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="610d1-176">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-177">Распределение по бухгалтерским счетам суммы без учета скидок и наценок или расхода.</span><span class="sxs-lookup"><span data-stu-id="610d1-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-178">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-179">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-180">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="610d1-181">Налоги, со следующими условиями:</span><span class="sxs-lookup"><span data-stu-id="610d1-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="610d1-182">Флажок "Применить правила налогообложения США" снят на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="610d1-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="610d1-183">Поле "Налог за пользование" для налоговой группы очищено на странице "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="610d1-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="610d1-184">Если сумма налога подлежит возмещению, поле "Входящий налог" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="610d1-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="610d1-185">Если сумма налога не подлежит возмещению, то сумма без учета скидок и наценок или распределение для начислений.</span><span class="sxs-lookup"><span data-stu-id="610d1-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-186">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-187">Используйте финансовую аналитику из суммы без учета скидок и наценок или распределений по бухгалтерским счетам для расходов строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-188">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-189">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610d1-190">Налоги, со следующими условиями:</span><span class="sxs-lookup"><span data-stu-id="610d1-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="610d1-191">Флажок "Применить правила налогообложения США" снят на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="610d1-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="610d1-192">Поле "Налог за пользование" для налоговой группы выбрано на странице "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="610d1-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="610d1-193">Если сумма налога подлежит возмещению, поле "Входящий налог" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="610d1-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="610d1-194">Если сумма налога не подлежит возмещению, поле "Расходы по налогу за пользование" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="610d1-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-195">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-196">Используйте финансовую аналитику из суммы без учета скидок и наценок или распределений по бухгалтерским счетам для расходов строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-197">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-198">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="610d1-199">Расходы заголовка</span><span class="sxs-lookup"><span data-stu-id="610d1-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-200">Если "Счет ГК" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Дебетовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="610d1-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="610d1-201">Если "Клиент/поставщик" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Кредитовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="610d1-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-202">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-203">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="610d1-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="610d1-204">Используйте значения шаблона финансовой аналитики по умолчанию из заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="610d1-205">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-206">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610d1-207">Заголовок скидки</span><span class="sxs-lookup"><span data-stu-id="610d1-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="610d1-208">Поле "Счет ГК" для типа разноски "Скидка по накладной поставщика" на странице "Счета для автоматических проводок".</span><span class="sxs-lookup"><span data-stu-id="610d1-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="610d1-209">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="610d1-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="610d1-210">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-211">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="610d1-212">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="610d1-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a><span data-ttu-id="610d1-213">Распределение налогов</span><span class="sxs-lookup"><span data-stu-id="610d1-213">Distributing taxes</span></span>

<span data-ttu-id="610d1-214">До расчета налогов создать для них распределения по бухгалтерским счетам нельзя.</span><span class="sxs-lookup"><span data-stu-id="610d1-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="610d1-215">Чтобы рассчитать налоги, необходимо на странице "Накладная поставщика" выполнить одну из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="610d1-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="610d1-216">Просмотрите итоговую сумму по накладной.</span><span class="sxs-lookup"><span data-stu-id="610d1-216">View the invoice total.</span></span>
-   <span data-ttu-id="610d1-217">Просмотрите налог.</span><span class="sxs-lookup"><span data-stu-id="610d1-217">View the sales tax.</span></span>
-   <span data-ttu-id="610d1-218">Просмотрите журнал субкниги.</span><span class="sxs-lookup"><span data-stu-id="610d1-218">View the subledger journal.</span></span>
-   <span data-ttu-id="610d1-219">Просмотр распределений по бухгалтерским счетам для полной накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="610d1-220">Заблокируйте накладную поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="610d1-221">Выполните разноску журнала накладных поставщика.</span><span class="sxs-lookup"><span data-stu-id="610d1-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="610d1-222">Журналы субкниги для накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="610d1-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="610d1-223">Перед разноской накладной поставщика можно просмотреть полную запись учета накладной, которая включает в себя дебет и кредит, чтобы уточнить, что накладная была разнесено в правильные счета.</span><span class="sxs-lookup"><span data-stu-id="610d1-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="610d1-224">Это представление записи полного учета называется журналом субкниги.</span><span class="sxs-lookup"><span data-stu-id="610d1-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="610d1-225">Если запись в журнале субкниги при просмотре перед учетом накладной поставщика в субкниге неверна, ее нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="610d1-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="610d1-226">Вместо этого необходимо изменить распределения по бухгалтерским счетам или профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="610d1-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="610d1-227">Распределения по бухгалтерским счетам используются для определения одной из сторон записи по счету, дебетовой или кредитовой.</span><span class="sxs-lookup"><span data-stu-id="610d1-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="610d1-228">Корректирующая запись по счету в журнале субкниги создается с помощью профилей разноски, таких как счет поставщика или налоги.</span><span class="sxs-lookup"><span data-stu-id="610d1-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]