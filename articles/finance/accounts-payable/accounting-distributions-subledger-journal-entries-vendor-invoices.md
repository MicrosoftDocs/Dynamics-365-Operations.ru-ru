---
title: Распределения по бухгалтерским счетам и записи в журнале субкниги для накладных поставщиков
description: Распределения по бухгалтерским счетам используются, чтобы определить, как будет включена сумма. Например, как расходы, налоги или начисления будут включены в накладную поставщика. На каждую сумму, которая должна быть включена в накладную поставщика, будет приходится одно или несколько распределений по бухгалтерским счетам.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447346"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="ee44c-104">Распределения по бухгалтерским счетам и записи в журнале субкниги для накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="ee44c-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee44c-105">Распределения по бухгалтерским счетам используются, чтобы определить, как будет включена сумма. Например, как расходы, налоги или начисления будут включены в накладную поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="ee44c-106">На каждую сумму, которая должна быть включена в накладную поставщика, будет приходится одно или несколько распределений по бухгалтерским счетам.</span><span class="sxs-lookup"><span data-stu-id="ee44c-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="ee44c-107">Распределение по бухгалтерским счетам</span><span class="sxs-lookup"><span data-stu-id="ee44c-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="ee44c-108">Можно использовать следующие кнопки на странице "Накладная поставщика", чтобы просматривать и по возможности изменять распределения по бухгалтерским счетам для каждой суммы в накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="ee44c-109">**Распределить суммы** – Просмотр и изменение распределений по бухгалтерским счетам для отдельной строки и любых дочерних строк, например для налогов и начислений.</span><span class="sxs-lookup"><span data-stu-id="ee44c-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="ee44c-110">Вы можете также просмотреть и изменить распределения по бухгалтерским счетам для дочерней строки непосредственно со страницы "Налоговые проводки" или "Проводки по накладным расходам".</span><span class="sxs-lookup"><span data-stu-id="ee44c-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="ee44c-111">Измените суммы заголовка накладной поставщика (например, начисления и суммы округления валюты).</span><span class="sxs-lookup"><span data-stu-id="ee44c-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="ee44c-112">Измените суммы строки накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="ee44c-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="ee44c-113">**Просмотр распределений** — Просмотр распределений по бухгалтерским счетам для всех строк документа.</span><span class="sxs-lookup"><span data-stu-id="ee44c-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="ee44c-114">В этом представлении изменять распределения по бухгалтерским счетам нельзя.</span><span class="sxs-lookup"><span data-stu-id="ee44c-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="ee44c-115">Просмотрите суммы заголовка и строк.</span><span class="sxs-lookup"><span data-stu-id="ee44c-115">View header and line amounts.</span></span>

<span data-ttu-id="ee44c-116">Если накладная поставщика ссылается на заказ на покупку, вы можете разделить и изменить распределения по бухгалтерским счетам для строк, в которых содержатся не учитываемые в запасах номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ee44c-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="ee44c-117">Если строка накладной поставщика не ссылается на строку заказа на покупку, вы также можете удалить распределения по бухгалтерским счетам.</span><span class="sxs-lookup"><span data-stu-id="ee44c-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="ee44c-118">Вы не можете разделить или удалить строки для расходов, налогов и скидок по строкам.</span><span class="sxs-lookup"><span data-stu-id="ee44c-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="ee44c-119">Вы можете изменить счет учета, но не суммы или проценты.</span><span class="sxs-lookup"><span data-stu-id="ee44c-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="ee44c-120">Если родительская строка содержит не учитываемую в запасах номенклатуру и распределения по бухгалтерским счетам разделяются, дочерняя строка будет разделена автоматически в соответствии с финансовыми аналитиками родительской строки.</span><span class="sxs-lookup"><span data-stu-id="ee44c-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="ee44c-121">Распределения по бухгалтерским счетам для дочерней строки нельзя дополнительно разделить или удалить, однако, в зависимости от настройки дочерней строки, для ее распределений по бухгалтерским счетам можно изменить счет в книге учета.</span><span class="sxs-lookup"><span data-stu-id="ee44c-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="ee44c-122">Распределение сумм</span><span class="sxs-lookup"><span data-stu-id="ee44c-122">Distributing amounts</span></span>
<span data-ttu-id="ee44c-123">При вводе накладной поставщика каждая сумма распределяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ee44c-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee44c-124">Тип строки накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="ee44c-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="ee44c-125">Порядок или приоритет, который определяет, откуда отображается счет ГК.</span><span class="sxs-lookup"><span data-stu-id="ee44c-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="ee44c-126">Порядок приоритетов, определяющий финансовую аналитику, отображаемую по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee44c-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee44c-127">Учитываемый в запасах продукт</span><span class="sxs-lookup"><span data-stu-id="ee44c-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-128">Распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-129">Поле "Счет ГК", если на странице "Разноска" выбрано значение "Расход на покупку для продукта".</span><span class="sxs-lookup"><span data-stu-id="ee44c-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-130">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-131">Используйте значения финансовой аналитики по умолчанию для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee44c-132">Категория закупки или продукта, не учитываемые в запасах</span><span class="sxs-lookup"><span data-stu-id="ee44c-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-133">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-134">Поле "Счет ГК", если на странице "Разноска" выбрано значение "Расходы по закупкам для нескладируемой номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="ee44c-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-135">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-136">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="ee44c-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="ee44c-137">Используйте значения финансовой аналитики по умолчанию для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="ee44c-138">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-139">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee44c-140">Актив</span><span class="sxs-lookup"><span data-stu-id="ee44c-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-141">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-142">Если значение "Ввод в эксплуатацию" выбрано в поле "Тип проводки" в форме "Накладная поставщика", поле "Счет ГК", когда значение "Ввод в эксплуатацию" выбрано на странице "Профили разноски основных средств".</span><span class="sxs-lookup"><span data-stu-id="ee44c-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="ee44c-143">Если значение "Переоценка стоимости ввода в эксплуатацию" выбрано в поле "Тип проводки", поле "Счет ГК", когда значение "Переоценка стоимости ввода в эксплуатацию" выбрано на странице "Профили разноски основных средств".</span><span class="sxs-lookup"><span data-stu-id="ee44c-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-144">Используйте распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-145">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-146">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee44c-147">Проект, определенные в строке накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="ee44c-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-148">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-149">Если в поле "Разноска себестоимости - Номенклатура" выбрано значение "Сальдо", поле "Счет ГК", когда значение "Затраты" выбрано на странице "Настройка разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="ee44c-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="ee44c-150">Если в поле "Разноска себестоимости - Номенклатура" выбрано значение "Прибыли и убытки", поле "Счет ГК", когда значение "Себестоимость - Номенклатура" выбрано на странице "Настройка разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="ee44c-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-151">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee44c-152">Скидка по строке</span><span class="sxs-lookup"><span data-stu-id="ee44c-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-153">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-154">Поле "Счет ГК", если на странице "Разноска" выбрано значение "Скидка".</span><span class="sxs-lookup"><span data-stu-id="ee44c-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="ee44c-155">Если счет ГК скидки не определен в профиле разноски, то распределение по бухгалтерским счетам для суммы без учета скидок и наценок будет в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-156">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-157">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-158">Используйте значения финансовой аналитики для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-159">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee44c-160">Расходы на покупку, введенные на вкладке "Цена и скидка" строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="ee44c-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-161">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-162">Распределение по бухгалтерским счетам для суммы без учета скидок и наценок в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-163">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-164">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee44c-165">Расходы по строке</span><span class="sxs-lookup"><span data-stu-id="ee44c-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-166">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-167">Если "Счет ГК" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Дебетовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="ee44c-168">Если выбрана "Номенклатура" в поле дебета "Тип" в форме "Код накладных расходов", распределение по бухгалтерским счетам для суммы без учета скидок и наценок в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-169">Если "Клиент/поставщик" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Кредитовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-170">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-171">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-172">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-173">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee44c-174">Налоги, со следующим условием:</span><span class="sxs-lookup"><span data-stu-id="ee44c-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="ee44c-175">Флажок "Применить правила налогообложения США" установлен на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="ee44c-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="ee44c-176">Распределение по бухгалтерским счетам для строки заказа на покупку, если строка накладной ссылается на строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-177">Распределение по бухгалтерским счетам суммы без учета скидок и наценок или расхода.</span><span class="sxs-lookup"><span data-stu-id="ee44c-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-178">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-179">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-180">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee44c-181">Налоги, со следующими условиями:</span><span class="sxs-lookup"><span data-stu-id="ee44c-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="ee44c-182">Флажок "Применить правила налогообложения США" снят на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="ee44c-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="ee44c-183">Поле "Налог за пользование" для налоговой группы очищено на странице "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="ee44c-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="ee44c-184">Если сумма налога подлежит возмещению, поле "Входящий налог" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="ee44c-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="ee44c-185">Если сумма налога не подлежит возмещению, то сумма без учета скидок и наценок или распределение для начислений.</span><span class="sxs-lookup"><span data-stu-id="ee44c-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-186">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-187">Используйте финансовую аналитику из суммы без учета скидок и наценок или распределений по бухгалтерским счетам для расходов строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-188">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-189">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee44c-190">Налоги, со следующими условиями:</span><span class="sxs-lookup"><span data-stu-id="ee44c-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="ee44c-191">Флажок "Применить правила налогообложения США" снят на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="ee44c-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="ee44c-192">Поле "Налог за пользование" для налоговой группы выбрано на странице "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="ee44c-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="ee44c-193">Если сумма налога подлежит возмещению, поле "Входящий налог" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="ee44c-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="ee44c-194">Если сумма налога не подлежит возмещению, поле "Расходы по налогу за пользование" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="ee44c-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-195">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-196">Используйте финансовую аналитику из суммы без учета скидок и наценок или распределений по бухгалтерским счетам для расходов строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-197">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-198">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee44c-199">Расходы заголовка</span><span class="sxs-lookup"><span data-stu-id="ee44c-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-200">Если "Счет ГК" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Дебетовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="ee44c-201">Если "Клиент/поставщик" выбран в поле "Тип дебетования" в форме "Код накладных расходов", поле "Кредитовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-202">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-203">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="ee44c-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="ee44c-204">Используйте значения шаблона финансовой аналитики по умолчанию из заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="ee44c-205">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-206">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee44c-207">Заголовок скидки</span><span class="sxs-lookup"><span data-stu-id="ee44c-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="ee44c-208">Поле "Счет ГК" для типа разноски "Скидка по накладной поставщика" на странице "Счета для автоматических проводок".</span><span class="sxs-lookup"><span data-stu-id="ee44c-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ee44c-209">Если строка накладной ссылается на строку заказа на покупку, используйте распределение по бухгалтерским счетам для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ee44c-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ee44c-210">Используйте финансовую аналитику из распределений по бухгалтерским счетам для строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-211">Используйте значения финансовой аналитики из строки накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ee44c-212">Используйте значения финансовой аналитики по умолчанию из счета ГК на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="ee44c-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="ee44c-213">Распределение налогов</span><span class="sxs-lookup"><span data-stu-id="ee44c-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="ee44c-214">До расчета налогов создать для них распределения по бухгалтерским счетам нельзя.</span><span class="sxs-lookup"><span data-stu-id="ee44c-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="ee44c-215">Чтобы рассчитать налоги, необходимо на странице "Накладная поставщика" выполнить одну из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="ee44c-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="ee44c-216">Просмотрите итоговую сумму по накладной.</span><span class="sxs-lookup"><span data-stu-id="ee44c-216">View the invoice total.</span></span>
-   <span data-ttu-id="ee44c-217">Просмотрите налог.</span><span class="sxs-lookup"><span data-stu-id="ee44c-217">View the sales tax.</span></span>
-   <span data-ttu-id="ee44c-218">Просмотрите журнал субкниги.</span><span class="sxs-lookup"><span data-stu-id="ee44c-218">View the subledger journal.</span></span>
-   <span data-ttu-id="ee44c-219">Просмотр распределений по бухгалтерским счетам для полной накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="ee44c-220">Заблокируйте накладную поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="ee44c-221">Выполните разноску журнала накладных поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee44c-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="ee44c-222">Журналы субкниги для накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="ee44c-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="ee44c-223">Перед разноской накладной поставщика можно просмотреть полную запись учета накладной, которая включает в себя дебет и кредит, чтобы уточнить, что накладная была разнесено в правильные счета.</span><span class="sxs-lookup"><span data-stu-id="ee44c-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="ee44c-224">Это представление записи полного учета называется журналом субкниги.</span><span class="sxs-lookup"><span data-stu-id="ee44c-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="ee44c-225">Если запись в журнале субкниги при просмотре перед учетом накладной поставщика в субкниге неверна, ее нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="ee44c-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="ee44c-226">Вместо этого необходимо изменить распределения по бухгалтерским счетам или профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="ee44c-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="ee44c-227">Распределения по бухгалтерским счетам используются для определения одной из сторон записи по счету, дебетовой или кредитовой.</span><span class="sxs-lookup"><span data-stu-id="ee44c-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="ee44c-228">Корректирующая запись по счету в журнале субкниги создается с помощью профилей разноски, таких как счет поставщика или налоги.</span><span class="sxs-lookup"><span data-stu-id="ee44c-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





