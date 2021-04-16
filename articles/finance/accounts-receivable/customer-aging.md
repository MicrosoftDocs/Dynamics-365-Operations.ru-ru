---
title: Отчет по срокам оплаты по клиентам
description: Отчет "Распределение клиентов по срокам оплаты" содержит дебетовые сальдо клиентов, отсортированные по интервалу дат или периоду распределения по срокам.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b80345513d355115a182c108bf3843963e9a59d9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840349"
---
# <a name="customer-aging-report"></a><span data-ttu-id="ed1e5-103">Отчет по срокам оплаты по клиентам</span><span class="sxs-lookup"><span data-stu-id="ed1e5-103">Customer aging report</span></span> 

<span data-ttu-id="ed1e5-104">Отчет **Распределение клиентов по срокам оплаты** содержит дебетовые сальдо клиентов, отсортированные по интервалу дат или периоду распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="ed1e5-105">При создании этого отчета отображаются следующие параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="ed1e5-106">Эти параметры можно использовать для фильтрации данных, которые будут отображаться в отчете.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="ed1e5-107">Дополнительные сведения см. в разделе [Настройка коллекций](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="ed1e5-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed1e5-108">Поле</span><span class="sxs-lookup"><span data-stu-id="ed1e5-108">Field</span></span></p></th>
<th><p><span data-ttu-id="ed1e5-109">описание</span><span class="sxs-lookup"><span data-stu-id="ed1e5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-110"><strong>Классификация выставления счетов</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-111">Выбор одной или нескольких классификаций выставления счетов для включения в отчет.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ed1e5-112">**Примечание.** Этот элемент управления доступен, только если выбран конфигурационный ключ <STRONG>Государственный сектор</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-113"><strong>Включение транзакций без классификации выставления счетов</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-114">Если этот флажок установлен, в отчете будут отображены все проводки, у которых нет назначенной им классификации выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ed1e5-115">**Примечание.** Этот элемент управления доступен, только если выбран конфигурационный ключ <STRONG>Государственный сектор</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-116"><strong>Распределение по срокам оплаты на дату</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-117">Ввод даты, используемой в текущем периоде распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-118"><strong>Сальдо на дату</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-119">Ввод даты, для которой требуется просмотреть сальдо клиентов.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="ed1e5-120">Это также называется датой прекращения проводок.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-121"><strong>Начальная дата</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-122">Ввод даты, находящейся в интервале первого периода или периода распределения по срокам, для включения в отчет.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-123"><strong>Критерии</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-124">Выбор типа даты, на котором будет базироваться отчет.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="ed1e5-125"><strong>Дата проводки</strong> — дата разноски проводок.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="ed1e5-126">Например, это может быть дата накладной, которая является базой для расчета срока выполнения.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="ed1e5-127"><strong>Срок выполнения</strong> — срок выполнения проводок с учетом условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="ed1e5-128"><strong>Дата документа</strong> — определяемая пользователем дата по документу, которая является базой для расчета срока оплаты.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-129"><strong>Определение периода распределения по срокам</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-130">Выбор определения периода распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-130">Select an aging period definition.</span></span> <span data-ttu-id="ed1e5-131">Если выбрано определение периода распределения по срокам, поле <strong>Интервал</strong> не используется.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="ed1e5-132">Определения периода распределения по строкам, которые имеют более 6 периодов распределения по срокам, нельзя использовать в распечатанном отчете.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="ed1e5-133">**Примечание.** Периоды распределения по срокам можно настроить на странице <STRONG>Определения периодов распределения по срокам</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-134"><strong>Печать описания периода распределения по срокам</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-135">Выберите <strong>Да</strong> для включения описаний периодов распределения по срокам в верхней части каждого столбца периода распределения по срокам в отчете.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="ed1e5-136">Выберите <strong>Нет</strong> для печати отчета без заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-137"><strong>Диапазон</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-138">Чтобы задать период, который следует использовать, нужно ввести число дней или месяцев в каждом периоде.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="ed1e5-139">Например, для просмотра сведений о понедельном распределении по срокам введите 7 в этом поле и выберите <strong>День</strong> в поле <strong>День/мес.</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="ed1e5-140">**Примечание.** Сведения, указанные в данном поле, используются только в том случае, если определение периода распределения по срокам не выбрано.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="ed1e5-141">В противном случае направление печати определяется в определении периодов распределения по срокам оплаты.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-142"><strong>День/мес.</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-143">Выбор единицы времени: <strong>День</strong> или <strong>Месяц</strong>, которая будет определять период в поле <strong>Интервал</strong>.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-144"><strong>Направление печати</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-145">Выберите, следует ли рассчитывать сальдо и распечатать отчет по распределению по срокам для прошлых или будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="ed1e5-146">Даты оцениваются по отношению к дате, выбранной в поле <strong>Сальдо на</strong>.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="ed1e5-147">Выберите <strong>Назад</strong>, чтобы показать сведения для прошлых периодов.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="ed1e5-148">Выберите <strong>Вперед</strong>, чтобы показать сведения для будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="ed1e5-149">
  
<STRONG>Примечание.</STRONG> Сведения, указанные в данном поле, используются только в том случае, если определение периода распределения по срокам не выбрано.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-150"><strong>Подробности</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-151">Выберите, чтобы показать список проводок, которые включены в сальдо, показанные в отчете.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-152"><strong>Включить суммы в валюте проводки</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-153">Выберите, чтобы включить суммы в валюте проводки в дополнение к суммам в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="ed1e5-154">Если этот флажок не установлен, суммы в отчете отображается только в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-155"><strong>Отрицательное сальдо</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-156">Выберите, чтобы включить счета клиента с отрицательными сальдо.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1e5-157"><strong>Исключить счета с нулевым сальдо</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-158">Выберите, чтобы исключить счета клиента с нулевым сальдо.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1e5-159"><strong>Размещение платежей</strong></span><span class="sxs-lookup"><span data-stu-id="ed1e5-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1e5-160">Выберите, чтобы показать платежи, которые не были сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="ed1e5-161">Они отображаются в первом столбце отчета.</span><span class="sxs-lookup"><span data-stu-id="ed1e5-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]