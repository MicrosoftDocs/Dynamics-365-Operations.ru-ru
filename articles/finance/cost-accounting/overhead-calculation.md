---
title: Расчет накладных расходов
description: В этом разделе описываются типовые процессы расчета и распределения накладных расходов.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208855"
---
# <a name="overhead-calculation"></a><span data-ttu-id="2813f-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="2813f-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2813f-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="2813f-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="2813f-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="2813f-105">Term definition</span></span>
---------------

<span data-ttu-id="2813f-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="2813f-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="2813f-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="2813f-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="2813f-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="2813f-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="2813f-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="2813f-109">Rent</span></span>
-   <span data-ttu-id="2813f-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-110">Electricity</span></span>
-   <span data-ttu-id="2813f-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="2813f-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="2813f-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="2813f-112">Overhead calculation overview</span></span>
<span data-ttu-id="2813f-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="2813f-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="2813f-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="2813f-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="2813f-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="2813f-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="2813f-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="2813f-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="2813f-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="2813f-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="2813f-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="2813f-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="2813f-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="2813f-119">Version type</span></span>
-   <span data-ttu-id="2813f-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="2813f-120">Date and time</span></span>
-   <span data-ttu-id="2813f-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="2813f-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="2813f-122">Fiscal year</span></span>
-   <span data-ttu-id="2813f-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="2813f-123">Fiscal period</span></span>

<span data-ttu-id="2813f-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="2813f-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="2813f-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="2813f-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="2813f-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2813f-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="2813f-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="2813f-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="2813f-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="2813f-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="2813f-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="2813f-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="2813f-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="2813f-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="2813f-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="2813f-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="2813f-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="2813f-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="2813f-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="2813f-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="2813f-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="2813f-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="2813f-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="2813f-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="2813f-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="2813f-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2813f-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="2813f-140">Main account</span></span></th>
<th><span data-ttu-id="2813f-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="2813f-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="2813f-143">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-143">CC099</span></span></td>
<td><span data-ttu-id="2813f-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-144">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-145">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-145">10001</span></span></td>
<td><span data-ttu-id="2813f-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-146">Electricity</span></span></td>
<td><span data-ttu-id="2813f-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="2813f-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="2813f-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="2813f-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="2813f-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="2813f-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="2813f-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-151">Define the cost behavior rule</span></span>

<span data-ttu-id="2813f-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="2813f-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="2813f-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="2813f-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="2813f-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="2813f-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="2813f-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="2813f-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="2813f-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="2813f-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="2813f-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="2813f-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-160">Journal</span></span></th>
<th><span data-ttu-id="2813f-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="2813f-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2813f-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="2813f-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2813f-163">Версия</span><span class="sxs-lookup"><span data-stu-id="2813f-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-164">00001</span><span class="sxs-lookup"><span data-stu-id="2813f-164">00001</span></span></td>
<td><span data-ttu-id="2813f-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="2813f-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="2813f-166">Fiscal</span></span></td>
<td><span data-ttu-id="2813f-167">2017</span><span class="sxs-lookup"><span data-stu-id="2813f-167">2017</span></span></td>
<td><span data-ttu-id="2813f-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-168">Period 1</span></span></td>
<td><span data-ttu-id="2813f-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2813f-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="2813f-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-173">Cost element</span></span></th>
<th><span data-ttu-id="2813f-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-174">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="2813f-177">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-177">CC099</span></span></td>
<td><span data-ttu-id="2813f-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-178">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-179">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-179">10001</span></span></td>
<td><span data-ttu-id="2813f-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-180">Electricity</span></span></td>
<td><span data-ttu-id="2813f-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="2813f-181">Unclassified</span></span></td>
<td><span data-ttu-id="2813f-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="2813f-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2813f-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-185">Cost element</span></span></th>
<th><span data-ttu-id="2813f-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-186">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-187">Amount</span></span></th>
<th><span data-ttu-id="2813f-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-189">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-189">CC099</span></span></td>
<td><span data-ttu-id="2813f-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-190">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-191">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-191">10001</span></span></td>
<td><span data-ttu-id="2813f-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-192">Electricity</span></span></td>
<td><span data-ttu-id="2813f-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="2813f-193">Unclassified</span></span></td>
<td><span data-ttu-id="2813f-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="2813f-194">10,000.00</span></span></td>
<td><span data-ttu-id="2813f-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-196">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-196">CC099</span></span></td>
<td><span data-ttu-id="2813f-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-197">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-198">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-198">10001</span></span></td>
<td><span data-ttu-id="2813f-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-199">Electricity</span></span></td>
<td><span data-ttu-id="2813f-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="2813f-200">Unclassified</span></span></td>
<td><span data-ttu-id="2813f-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-201">-10,000.00</span></span></td>
<td><span data-ttu-id="2813f-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-203">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-203">CC099</span></span></td>
<td><span data-ttu-id="2813f-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-204">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-205">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-205">10001</span></span></td>
<td><span data-ttu-id="2813f-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-206">Electricity</span></span></td>
<td><span data-ttu-id="2813f-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-207">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-208">1,000.00</span></span></td>
<td><span data-ttu-id="2813f-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-210">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-210">CC099</span></span></td>
<td><span data-ttu-id="2813f-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-211">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-212">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-212">10001</span></span></td>
<td><span data-ttu-id="2813f-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-213">Electricity</span></span></td>
<td><span data-ttu-id="2813f-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-214">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="2813f-215">9,000.00</span></span></td>
<td><span data-ttu-id="2813f-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="2813f-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="2813f-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="2813f-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="2813f-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="2813f-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-221">Define the cost distribution rule</span></span>

<span data-ttu-id="2813f-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="2813f-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="2813f-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="2813f-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="2813f-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="2813f-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="2813f-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="2813f-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="2813f-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="2813f-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="2813f-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-228">Cost object</span></span></th>
<th><span data-ttu-id="2813f-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="2813f-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-230">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-230">CC001</span></span></td>
<td><span data-ttu-id="2813f-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-231">HR</span></span></td>
<td><span data-ttu-id="2813f-232">1000</span><span class="sxs-lookup"><span data-stu-id="2813f-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-233">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-233">CC002</span></span></td>
<td><span data-ttu-id="2813f-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-234">Finance</span></span></td>
<td><span data-ttu-id="2813f-235">6,000</span><span class="sxs-lookup"><span data-stu-id="2813f-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-236">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-236">CC003</span></span></td>
<td><span data-ttu-id="2813f-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-237">Assembly</span></span></td>
<td><span data-ttu-id="2813f-238">0</span><span class="sxs-lookup"><span data-stu-id="2813f-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-240">Cost object</span></span></th>
<th><span data-ttu-id="2813f-241">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-241">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-242">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-244">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-244">CC001</span></span></td>
<td><span data-ttu-id="2813f-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-245">HR</span></span></td>
<td><span data-ttu-id="2813f-246">1000</span><span class="sxs-lookup"><span data-stu-id="2813f-246">1,000</span></span></td>
<td><span data-ttu-id="2813f-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2813f-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="2813f-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-249">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-249">CC002</span></span></td>
<td><span data-ttu-id="2813f-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-250">Finance</span></span></td>
<td><span data-ttu-id="2813f-251">6,000</span><span class="sxs-lookup"><span data-stu-id="2813f-251">6,000</span></span></td>
<td><span data-ttu-id="2813f-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2813f-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="2813f-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-254">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-254">CC003</span></span></td>
<td><span data-ttu-id="2813f-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-255">Assembly</span></span></td>
<td><span data-ttu-id="2813f-256">0</span><span class="sxs-lookup"><span data-stu-id="2813f-256">0</span></span></td>
<td><span data-ttu-id="2813f-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2813f-258">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="2813f-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="2813f-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-261">Cost object</span></span></th>
<th><span data-ttu-id="2813f-262">Формула</span><span class="sxs-lookup"><span data-stu-id="2813f-262">Formula</span></span></th>
<th><span data-ttu-id="2813f-263">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-263">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-264">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-266">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-266">CC001</span></span></td>
<td><span data-ttu-id="2813f-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-267">HR</span></span></td>
<td><span data-ttu-id="2813f-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2813f-269">1</span><span class="sxs-lookup"><span data-stu-id="2813f-269">1</span></span></td>
<td><span data-ttu-id="2813f-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2813f-271">500.00</span><span class="sxs-lookup"><span data-stu-id="2813f-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-272">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-272">CC002</span></span></td>
<td><span data-ttu-id="2813f-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-273">Finance</span></span></td>
<td><span data-ttu-id="2813f-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2813f-275">1</span><span class="sxs-lookup"><span data-stu-id="2813f-275">1</span></span></td>
<td><span data-ttu-id="2813f-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2813f-277">500.00</span><span class="sxs-lookup"><span data-stu-id="2813f-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-278">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-278">CC003</span></span></td>
<td><span data-ttu-id="2813f-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-279">Assembly</span></span></td>
<td><span data-ttu-id="2813f-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2813f-281">0</span><span class="sxs-lookup"><span data-stu-id="2813f-281">0</span></span></td>
<td><span data-ttu-id="2813f-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2813f-283">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="2813f-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-285">Journal</span></span></th>
<th><span data-ttu-id="2813f-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="2813f-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2813f-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="2813f-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2813f-288">Версия</span><span class="sxs-lookup"><span data-stu-id="2813f-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-289">00002</span><span class="sxs-lookup"><span data-stu-id="2813f-289">00002</span></span></td>
<td><span data-ttu-id="2813f-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="2813f-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="2813f-291">Fiscal</span></span></td>
<td><span data-ttu-id="2813f-292">2017</span><span class="sxs-lookup"><span data-stu-id="2813f-292">2017</span></span></td>
<td><span data-ttu-id="2813f-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-293">Period 1</span></span></td>
<td><span data-ttu-id="2813f-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2813f-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="2813f-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-298">Cost element</span></span></th>
<th><span data-ttu-id="2813f-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-299">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-302">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-302">CC099</span></span></td>
<td><span data-ttu-id="2813f-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-303">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-304">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-304">10001</span></span></td>
<td><span data-ttu-id="2813f-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-305">Electricity</span></span></td>
<td><span data-ttu-id="2813f-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-306">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-309">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-309">CC099</span></span></td>
<td><span data-ttu-id="2813f-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-310">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-311">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-311">10001</span></span></td>
<td><span data-ttu-id="2813f-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-312">Electricity</span></span></td>
<td><span data-ttu-id="2813f-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-313">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="2813f-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2813f-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-317">Cost element</span></span></th>
<th><span data-ttu-id="2813f-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-318">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-319">Amount</span></span></th>
<th><span data-ttu-id="2813f-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-321">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-321">CC099</span></span></td>
<td><span data-ttu-id="2813f-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-322">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-323">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-323">10001</span></span></td>
<td><span data-ttu-id="2813f-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-324">Electricity</span></span></td>
<td><span data-ttu-id="2813f-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-325">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-326">-1,000.00</span></span></td>
<td><span data-ttu-id="2813f-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-328">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-328">CC001</span></span></td>
<td><span data-ttu-id="2813f-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-329">HR</span></span></td>
<td><span data-ttu-id="2813f-330">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-330">10001</span></span></td>
<td><span data-ttu-id="2813f-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-331">Electricity</span></span></td>
<td><span data-ttu-id="2813f-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-332">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-333">500.00</span><span class="sxs-lookup"><span data-stu-id="2813f-333">500.00</span></span></td>
<td><span data-ttu-id="2813f-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-335">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-335">CC002</span></span></td>
<td><span data-ttu-id="2813f-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-336">Finance</span></span></td>
<td><span data-ttu-id="2813f-337">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-337">10001</span></span></td>
<td><span data-ttu-id="2813f-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-338">Electricity</span></span></td>
<td><span data-ttu-id="2813f-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-339">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-340">500.00</span><span class="sxs-lookup"><span data-stu-id="2813f-340">500.00</span></span></td>
<td><span data-ttu-id="2813f-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-342">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-342">CC099</span></span></td>
<td><span data-ttu-id="2813f-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2813f-343">Default cost center</span></span></td>
<td><span data-ttu-id="2813f-344">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-344">10001</span></span></td>
<td><span data-ttu-id="2813f-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-345">Electricity</span></span></td>
<td><span data-ttu-id="2813f-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-346">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="2813f-347">-9,000.00</span></span></td>
<td><span data-ttu-id="2813f-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-349">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-349">CC001</span></span></td>
<td><span data-ttu-id="2813f-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-350">HR</span></span></td>
<td><span data-ttu-id="2813f-351">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-351">10001</span></span></td>
<td><span data-ttu-id="2813f-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-352">Electricity</span></span></td>
<td><span data-ttu-id="2813f-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-353">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="2813f-354">1,285.71</span></span></td>
<td><span data-ttu-id="2813f-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-356">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-356">CC002</span></span></td>
<td><span data-ttu-id="2813f-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-357">Finance</span></span></td>
<td><span data-ttu-id="2813f-358">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-358">10001</span></span></td>
<td><span data-ttu-id="2813f-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-359">Electricity</span></span></td>
<td><span data-ttu-id="2813f-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-360">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="2813f-361">7,714.29</span></span></td>
<td><span data-ttu-id="2813f-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="2813f-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="2813f-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="2813f-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="2813f-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="2813f-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="2813f-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="2813f-367">Define the overhead rate</span></span>

<span data-ttu-id="2813f-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="2813f-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="2813f-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="2813f-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-370">Cost object</span></span></th>
<th><span data-ttu-id="2813f-371">Часы</span><span class="sxs-lookup"><span data-stu-id="2813f-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-372">Proj 1</span></span></td>
<td><span data-ttu-id="2813f-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-373">Project 1</span></span></td>
<td><span data-ttu-id="2813f-374">3</span><span class="sxs-lookup"><span data-stu-id="2813f-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-375">Proj 2</span></span></td>
<td><span data-ttu-id="2813f-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-376">Project 2</span></span></td>
<td><span data-ttu-id="2813f-377">1</span><span class="sxs-lookup"><span data-stu-id="2813f-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-379">Cost object</span></span></th>
<th><span data-ttu-id="2813f-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-380">Cost element</span></span></th>
<th><span data-ttu-id="2813f-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-381">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="2813f-382">Units</span></span></th>
<th><span data-ttu-id="2813f-383">По норме</span><span class="sxs-lookup"><span data-stu-id="2813f-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-384">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-384">CC001</span></span></td>
<td><span data-ttu-id="2813f-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-385">HR</span></span></td>
<td><span data-ttu-id="2813f-386">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-386">10001</span></span></td>
<td><span data-ttu-id="2813f-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-387">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-388">1</span><span class="sxs-lookup"><span data-stu-id="2813f-388">1</span></span></td>
<td><span data-ttu-id="2813f-389">10</span><span class="sxs-lookup"><span data-stu-id="2813f-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-391">Cost object</span></span></th>
<th><span data-ttu-id="2813f-392">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-392">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-393">Cost element</span></span></th>
<th><span data-ttu-id="2813f-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-394">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-396">Proj 1</span></span></td>
<td><span data-ttu-id="2813f-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-397">Project 1</span></span></td>
<td><span data-ttu-id="2813f-398">3</span><span class="sxs-lookup"><span data-stu-id="2813f-398">3</span></span></td>
<td><span data-ttu-id="2813f-399">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-399">10001</span></span></td>
<td><span data-ttu-id="2813f-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="2813f-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="2813f-401">30.00</span><span class="sxs-lookup"><span data-stu-id="2813f-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-402">Proj 2</span></span></td>
<td><span data-ttu-id="2813f-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-403">Project 2</span></span></td>
<td><span data-ttu-id="2813f-404">1</span><span class="sxs-lookup"><span data-stu-id="2813f-404">1</span></span></td>
<td><span data-ttu-id="2813f-405">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-405">10001</span></span></td>
<td><span data-ttu-id="2813f-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="2813f-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="2813f-407">10,00</span><span class="sxs-lookup"><span data-stu-id="2813f-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="2813f-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-409">Journal</span></span></th>
<th><span data-ttu-id="2813f-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="2813f-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2813f-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="2813f-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2813f-412">Версия</span><span class="sxs-lookup"><span data-stu-id="2813f-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-413">00003</span><span class="sxs-lookup"><span data-stu-id="2813f-413">00003</span></span></td>
<td><span data-ttu-id="2813f-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="2813f-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="2813f-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="2813f-415">Fiscal</span></span></td>
<td><span data-ttu-id="2813f-416">2017</span><span class="sxs-lookup"><span data-stu-id="2813f-416">2017</span></span></td>
<td><span data-ttu-id="2813f-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-417">Period 1</span></span></td>
<td><span data-ttu-id="2813f-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="2813f-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="2813f-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-421">Cost object</span></span></th>
<th><span data-ttu-id="2813f-422">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-424">Proj 1</span></span></td>
<td><span data-ttu-id="2813f-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="2813f-426">3,00</span><span class="sxs-lookup"><span data-stu-id="2813f-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-428">Proj 2</span></span></td>
<td><span data-ttu-id="2813f-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="2813f-430">1.00</span><span class="sxs-lookup"><span data-stu-id="2813f-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2813f-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-433">Cost element</span></span></th>
<th><span data-ttu-id="2813f-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-434">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-435">Amount</span></span></th>
<th><span data-ttu-id="2813f-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="2813f-437">CC0001</span></span></td>
<td><span data-ttu-id="2813f-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-438">HR</span></span></td>
<td><span data-ttu-id="2813f-439">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-439">10001</span></span></td>
<td><span data-ttu-id="2813f-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-440">Electricity</span></span></td>
<td><span data-ttu-id="2813f-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-441">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="2813f-442">-30.00</span></span></td>
<td><span data-ttu-id="2813f-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-444">Proj 1</span></span></td>
<td><span data-ttu-id="2813f-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="2813f-446">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-446">10001</span></span></td>
<td><span data-ttu-id="2813f-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-447">Electricity</span></span></td>
<td><span data-ttu-id="2813f-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-448">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-449">30.00</span><span class="sxs-lookup"><span data-stu-id="2813f-449">30.00</span></span></td>
<td><span data-ttu-id="2813f-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-451">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-451">CC001</span></span></td>
<td><span data-ttu-id="2813f-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-452">HR</span></span></td>
<td><span data-ttu-id="2813f-453">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-453">10001</span></span></td>
<td><span data-ttu-id="2813f-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-454">Electricity</span></span></td>
<td><span data-ttu-id="2813f-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-455">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="2813f-456">-10.00</span></span></td>
<td><span data-ttu-id="2813f-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-458">Proj 2</span></span></td>
<td><span data-ttu-id="2813f-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="2813f-460">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-460">10001</span></span></td>
<td><span data-ttu-id="2813f-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-461">Electricity</span></span></td>
<td><span data-ttu-id="2813f-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-462">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-463">10.00</span><span class="sxs-lookup"><span data-stu-id="2813f-463">10.00</span></span></td>
<td><span data-ttu-id="2813f-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="2813f-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="2813f-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="2813f-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="2813f-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="2813f-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="2813f-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="2813f-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="2813f-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="2813f-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="2813f-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="2813f-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="2813f-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="2813f-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="2813f-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="2813f-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="2813f-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="2813f-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-475">Define the cost allocation</span></span>

<span data-ttu-id="2813f-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="2813f-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="2813f-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="2813f-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-479">Cost object</span></span></th>
<th><span data-ttu-id="2813f-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-481">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-481">CC002</span></span></td>
<td><span data-ttu-id="2813f-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-482">Finance</span></span></td>
<td><span data-ttu-id="2813f-483">35</span><span class="sxs-lookup"><span data-stu-id="2813f-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-484">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-484">CC003</span></span></td>
<td><span data-ttu-id="2813f-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-485">Assembly</span></span></td>
<td><span data-ttu-id="2813f-486">55</span><span class="sxs-lookup"><span data-stu-id="2813f-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-487">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-487">CC004</span></span></td>
<td><span data-ttu-id="2813f-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-488">Packaging</span></span></td>
<td><span data-ttu-id="2813f-489">10</span><span class="sxs-lookup"><span data-stu-id="2813f-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="2813f-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="2813f-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-492">Cost object</span></span></th>
<th><span data-ttu-id="2813f-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="2813f-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-494">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-494">CC003</span></span></td>
<td><span data-ttu-id="2813f-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-495">Assembly</span></span></td>
<td><span data-ttu-id="2813f-496">65</span><span class="sxs-lookup"><span data-stu-id="2813f-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-497">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-497">CC004</span></span></td>
<td><span data-ttu-id="2813f-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-498">Packaging</span></span></td>
<td><span data-ttu-id="2813f-499">35</span><span class="sxs-lookup"><span data-stu-id="2813f-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="2813f-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="2813f-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-502">Cost object</span></span></th>
<th><span data-ttu-id="2813f-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="2813f-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-504">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-505">Product 1</span></span></td>
<td><span data-ttu-id="2813f-506">60</span><span class="sxs-lookup"><span data-stu-id="2813f-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-507">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-508">Product 2</span></span></td>
<td><span data-ttu-id="2813f-509">20</span><span class="sxs-lookup"><span data-stu-id="2813f-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="2813f-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="2813f-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-512">Cost object</span></span></th>
<th><span data-ttu-id="2813f-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="2813f-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-514">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-515">Product 1</span></span></td>
<td><span data-ttu-id="2813f-516">80</span><span class="sxs-lookup"><span data-stu-id="2813f-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-517">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-518">Product 2</span></span></td>
<td><span data-ttu-id="2813f-519">15</span><span class="sxs-lookup"><span data-stu-id="2813f-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2813f-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="2813f-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="2813f-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="2813f-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="2813f-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="2813f-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-523">Cost object</span></span></th>
<th><span data-ttu-id="2813f-524">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-524">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-525">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-526">Amount</span></span></th>
<th><span data-ttu-id="2813f-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-528">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-528">CC002</span></span></td>
<td><span data-ttu-id="2813f-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-529">Finance</span></span></td>
<td><span data-ttu-id="2813f-530">35</span><span class="sxs-lookup"><span data-stu-id="2813f-530">35</span></span></td>
<td><span data-ttu-id="2813f-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2813f-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2813f-532">175.00</span><span class="sxs-lookup"><span data-stu-id="2813f-532">175.00</span></span></td>
<td><span data-ttu-id="2813f-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-534">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-534">CC003</span></span></td>
<td><span data-ttu-id="2813f-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-535">Assembly</span></span></td>
<td><span data-ttu-id="2813f-536">55</span><span class="sxs-lookup"><span data-stu-id="2813f-536">55</span></span></td>
<td><span data-ttu-id="2813f-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2813f-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2813f-538">275.00</span><span class="sxs-lookup"><span data-stu-id="2813f-538">275.00</span></span></td>
<td><span data-ttu-id="2813f-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-540">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-540">CC004</span></span></td>
<td><span data-ttu-id="2813f-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-541">Packaging</span></span></td>
<td><span data-ttu-id="2813f-542">10</span><span class="sxs-lookup"><span data-stu-id="2813f-542">10</span></span></td>
<td><span data-ttu-id="2813f-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2813f-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2813f-544">50,00</span><span class="sxs-lookup"><span data-stu-id="2813f-544">50.00</span></span></td>
<td><span data-ttu-id="2813f-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-546">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-546">CC002</span></span></td>
<td><span data-ttu-id="2813f-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-547">Finance</span></span></td>
<td><span data-ttu-id="2813f-548">35</span><span class="sxs-lookup"><span data-stu-id="2813f-548">35</span></span></td>
<td><span data-ttu-id="2813f-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="2813f-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2813f-550">436.00</span><span class="sxs-lookup"><span data-stu-id="2813f-550">436.00</span></span></td>
<td><span data-ttu-id="2813f-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-552">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-552">CC003</span></span></td>
<td><span data-ttu-id="2813f-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-553">Assembly</span></span></td>
<td><span data-ttu-id="2813f-554">55</span><span class="sxs-lookup"><span data-stu-id="2813f-554">55</span></span></td>
<td><span data-ttu-id="2813f-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="2813f-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2813f-556">685.14</span><span class="sxs-lookup"><span data-stu-id="2813f-556">685.14</span></span></td>
<td><span data-ttu-id="2813f-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-558">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-558">CC004</span></span></td>
<td><span data-ttu-id="2813f-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-559">Packaging</span></span></td>
<td><span data-ttu-id="2813f-560">10</span><span class="sxs-lookup"><span data-stu-id="2813f-560">10</span></span></td>
<td><span data-ttu-id="2813f-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="2813f-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2813f-562">124.57</span><span class="sxs-lookup"><span data-stu-id="2813f-562">124.57</span></span></td>
<td><span data-ttu-id="2813f-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="2813f-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-565">Cost object</span></span></th>
<th><span data-ttu-id="2813f-566">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-566">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-567">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-568">Amount</span></span></th>
<th><span data-ttu-id="2813f-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-570">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-570">CC003</span></span></td>
<td><span data-ttu-id="2813f-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-571">Assembly</span></span></td>
<td><span data-ttu-id="2813f-572">65</span><span class="sxs-lookup"><span data-stu-id="2813f-572">65</span></span></td>
<td><span data-ttu-id="2813f-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="2813f-574">438.75</span><span class="sxs-lookup"><span data-stu-id="2813f-574">438.75</span></span></td>
<td><span data-ttu-id="2813f-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-576">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-576">CC004</span></span></td>
<td><span data-ttu-id="2813f-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-577">Packaging</span></span></td>
<td><span data-ttu-id="2813f-578">35</span><span class="sxs-lookup"><span data-stu-id="2813f-578">35</span></span></td>
<td><span data-ttu-id="2813f-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="2813f-580">236.25</span><span class="sxs-lookup"><span data-stu-id="2813f-580">236.25</span></span></td>
<td><span data-ttu-id="2813f-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-582">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-582">CC003</span></span></td>
<td><span data-ttu-id="2813f-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-583">Assembly</span></span></td>
<td><span data-ttu-id="2813f-584">65</span><span class="sxs-lookup"><span data-stu-id="2813f-584">65</span></span></td>
<td><span data-ttu-id="2813f-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="2813f-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="2813f-586">5,297.69</span></span></td>
<td><span data-ttu-id="2813f-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-588">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-588">CC004</span></span></td>
<td><span data-ttu-id="2813f-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-589">Packaging</span></span></td>
<td><span data-ttu-id="2813f-590">35</span><span class="sxs-lookup"><span data-stu-id="2813f-590">35</span></span></td>
<td><span data-ttu-id="2813f-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="2813f-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="2813f-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="2813f-592">2,852.60</span></span></td>
<td><span data-ttu-id="2813f-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="2813f-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-595">Cost object</span></span></th>
<th><span data-ttu-id="2813f-596">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-596">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-597">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-598">Amount</span></span></th>
<th><span data-ttu-id="2813f-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-600">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-601">Product 1</span></span></td>
<td><span data-ttu-id="2813f-602">60</span><span class="sxs-lookup"><span data-stu-id="2813f-602">60</span></span></td>
<td><span data-ttu-id="2813f-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="2813f-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="2813f-604">535.31</span><span class="sxs-lookup"><span data-stu-id="2813f-604">535.31</span></span></td>
<td><span data-ttu-id="2813f-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-606">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-607">Product 2</span></span></td>
<td><span data-ttu-id="2813f-608">20</span><span class="sxs-lookup"><span data-stu-id="2813f-608">20</span></span></td>
<td><span data-ttu-id="2813f-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="2813f-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="2813f-610">178.44</span><span class="sxs-lookup"><span data-stu-id="2813f-610">178.44</span></span></td>
<td><span data-ttu-id="2813f-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-612">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-613">Product 1</span></span></td>
<td><span data-ttu-id="2813f-614">60</span><span class="sxs-lookup"><span data-stu-id="2813f-614">60</span></span></td>
<td><span data-ttu-id="2813f-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="2813f-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="2813f-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="2813f-616">4,487.12</span></span></td>
<td><span data-ttu-id="2813f-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-618">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-619">Product 2</span></span></td>
<td><span data-ttu-id="2813f-620">20</span><span class="sxs-lookup"><span data-stu-id="2813f-620">20</span></span></td>
<td><span data-ttu-id="2813f-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="2813f-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="2813f-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="2813f-622">1,495.71</span></span></td>
<td><span data-ttu-id="2813f-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2813f-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="2813f-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-625">Cost object</span></span></th>
<th><span data-ttu-id="2813f-626">Величина</span><span class="sxs-lookup"><span data-stu-id="2813f-626">Magnitude</span></span></th>
<th><span data-ttu-id="2813f-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="2813f-627">Allocation factor</span></span></th>
<th><span data-ttu-id="2813f-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-628">Amount</span></span></th>
<th><span data-ttu-id="2813f-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-630">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-631">Product 1</span></span></td>
<td><span data-ttu-id="2813f-632">80</span><span class="sxs-lookup"><span data-stu-id="2813f-632">80</span></span></td>
<td><span data-ttu-id="2813f-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="2813f-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="2813f-634">241.05</span><span class="sxs-lookup"><span data-stu-id="2813f-634">241.05</span></span></td>
<td><span data-ttu-id="2813f-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-636">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-637">Product 2</span></span></td>
<td><span data-ttu-id="2813f-638">15</span><span class="sxs-lookup"><span data-stu-id="2813f-638">15</span></span></td>
<td><span data-ttu-id="2813f-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="2813f-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="2813f-640">45.20</span><span class="sxs-lookup"><span data-stu-id="2813f-640">45.20</span></span></td>
<td><span data-ttu-id="2813f-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-642">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-643">Product 1</span></span></td>
<td><span data-ttu-id="2813f-644">80</span><span class="sxs-lookup"><span data-stu-id="2813f-644">80</span></span></td>
<td><span data-ttu-id="2813f-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="2813f-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="2813f-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="2813f-646">2,507.09</span></span></td>
<td><span data-ttu-id="2813f-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-648">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-649">Product 2</span></span></td>
<td><span data-ttu-id="2813f-650">15</span><span class="sxs-lookup"><span data-stu-id="2813f-650">15</span></span></td>
<td><span data-ttu-id="2813f-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="2813f-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="2813f-652">470.08</span><span class="sxs-lookup"><span data-stu-id="2813f-652">470.08</span></span></td>
<td><span data-ttu-id="2813f-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2813f-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="2813f-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="2813f-655">Journal</span></span></th>
<th><span data-ttu-id="2813f-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="2813f-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2813f-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="2813f-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2813f-658">Версия</span><span class="sxs-lookup"><span data-stu-id="2813f-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-659">00004</span><span class="sxs-lookup"><span data-stu-id="2813f-659">00004</span></span></td>
<td><span data-ttu-id="2813f-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="2813f-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="2813f-661">Fiscal</span></span></td>
<td><span data-ttu-id="2813f-662">2017</span><span class="sxs-lookup"><span data-stu-id="2813f-662">2017</span></span></td>
<td><span data-ttu-id="2813f-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-663">Period 1</span></span></td>
<td><span data-ttu-id="2813f-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="2813f-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="2813f-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="2813f-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2813f-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-668">Cost element</span></span></th>
<th><span data-ttu-id="2813f-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-669">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-672">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-672">CC001</span></span></td>
<td><span data-ttu-id="2813f-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-673">HR</span></span></td>
<td><span data-ttu-id="2813f-674">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-674">10001</span></span></td>
<td><span data-ttu-id="2813f-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-675">Electricity</span></span></td>
<td><span data-ttu-id="2813f-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-676">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-677">500.00</span><span class="sxs-lookup"><span data-stu-id="2813f-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-679">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-679">CC001</span></span></td>
<td><span data-ttu-id="2813f-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-680">HR</span></span></td>
<td><span data-ttu-id="2813f-681">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-681">10001</span></span></td>
<td><span data-ttu-id="2813f-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-682">Electricity</span></span></td>
<td><span data-ttu-id="2813f-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-683">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="2813f-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-686">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-686">CC002</span></span></td>
<td><span data-ttu-id="2813f-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-687">Finance</span></span></td>
<td><span data-ttu-id="2813f-688">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-688">10001</span></span></td>
<td><span data-ttu-id="2813f-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-689">Electricity</span></span></td>
<td><span data-ttu-id="2813f-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-690">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-691">675.00</span><span class="sxs-lookup"><span data-stu-id="2813f-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-693">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-693">CC002</span></span></td>
<td><span data-ttu-id="2813f-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-694">Finance</span></span></td>
<td><span data-ttu-id="2813f-695">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-695">10001</span></span></td>
<td><span data-ttu-id="2813f-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-696">Electricity</span></span></td>
<td><span data-ttu-id="2813f-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-697">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="2813f-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-700">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-700">CC003</span></span></td>
<td><span data-ttu-id="2813f-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-701">Assembly</span></span></td>
<td><span data-ttu-id="2813f-702">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-702">10001</span></span></td>
<td><span data-ttu-id="2813f-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-703">Electricity</span></span></td>
<td><span data-ttu-id="2813f-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-704">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-705">713.75</span><span class="sxs-lookup"><span data-stu-id="2813f-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-707">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-707">CC003</span></span></td>
<td><span data-ttu-id="2813f-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-708">Assembly</span></span></td>
<td><span data-ttu-id="2813f-709">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-709">10001</span></span></td>
<td><span data-ttu-id="2813f-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-710">Electricity</span></span></td>
<td><span data-ttu-id="2813f-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-711">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="2813f-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-714">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-714">CC003</span></span></td>
<td><span data-ttu-id="2813f-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-715">Packaging</span></span></td>
<td><span data-ttu-id="2813f-716">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-716">10001</span></span></td>
<td><span data-ttu-id="2813f-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-717">Electricity</span></span></td>
<td><span data-ttu-id="2813f-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-718">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-719">286.25</span><span class="sxs-lookup"><span data-stu-id="2813f-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-721">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-721">CC003</span></span></td>
<td><span data-ttu-id="2813f-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-722">Packaging</span></span></td>
<td><span data-ttu-id="2813f-723">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-723">10001</span></span></td>
<td><span data-ttu-id="2813f-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-724">Electricity</span></span></td>
<td><span data-ttu-id="2813f-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-725">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="2813f-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-728">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-729">Product 1</span></span></td>
<td><span data-ttu-id="2813f-730">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-730">10001</span></span></td>
<td><span data-ttu-id="2813f-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-731">Electricity</span></span></td>
<td><span data-ttu-id="2813f-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-732">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-733">776.36</span><span class="sxs-lookup"><span data-stu-id="2813f-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-735">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-736">Product 1</span></span></td>
<td><span data-ttu-id="2813f-737">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-737">10001</span></span></td>
<td><span data-ttu-id="2813f-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-738">Electricity</span></span></td>
<td><span data-ttu-id="2813f-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-739">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="2813f-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-742">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-743">Product 1</span></span></td>
<td><span data-ttu-id="2813f-744">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-744">10001</span></span></td>
<td><span data-ttu-id="2813f-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-745">Electricity</span></span></td>
<td><span data-ttu-id="2813f-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-746">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-747">223.64</span><span class="sxs-lookup"><span data-stu-id="2813f-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="2813f-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-749">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-750">Product 1</span></span></td>
<td><span data-ttu-id="2813f-751">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-751">10001</span></span></td>
<td><span data-ttu-id="2813f-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-752">Electricity</span></span></td>
<td><span data-ttu-id="2813f-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-753">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="2813f-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2813f-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2813f-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2813f-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-757">Cost element</span></span></th>
<th><span data-ttu-id="2813f-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-758">Cost behavior</span></span></th>
<th><span data-ttu-id="2813f-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="2813f-759">Amount</span></span></th>
<th><span data-ttu-id="2813f-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="2813f-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2813f-761">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-761">CC001</span></span></td>
<td><span data-ttu-id="2813f-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-762">HR</span></span></td>
<td><span data-ttu-id="2813f-763">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-763">10001</span></span></td>
<td><span data-ttu-id="2813f-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-764">Electricity</span></span></td>
<td><span data-ttu-id="2813f-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-765">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="2813f-766">-500.00</span></span></td>
<td><span data-ttu-id="2813f-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-768">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-768">CC002</span></span></td>
<td><span data-ttu-id="2813f-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-769">Finance</span></span></td>
<td><span data-ttu-id="2813f-770">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-770">10001</span></span></td>
<td><span data-ttu-id="2813f-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-771">Electricity</span></span></td>
<td><span data-ttu-id="2813f-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-772">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-773">175.00</span><span class="sxs-lookup"><span data-stu-id="2813f-773">175.00</span></span></td>
<td><span data-ttu-id="2813f-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-775">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-775">CC003</span></span></td>
<td><span data-ttu-id="2813f-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-776">Assembly</span></span></td>
<td><span data-ttu-id="2813f-777">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-777">10001</span></span></td>
<td><span data-ttu-id="2813f-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-778">Electricity</span></span></td>
<td><span data-ttu-id="2813f-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-779">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-780">275.00</span><span class="sxs-lookup"><span data-stu-id="2813f-780">275.00</span></span></td>
<td><span data-ttu-id="2813f-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-782">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-782">CC004</span></span></td>
<td><span data-ttu-id="2813f-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-783">Packaging</span></span></td>
<td><span data-ttu-id="2813f-784">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-784">10001</span></span></td>
<td><span data-ttu-id="2813f-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-785">Electricity</span></span></td>
<td><span data-ttu-id="2813f-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-786">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-787">50,00</span><span class="sxs-lookup"><span data-stu-id="2813f-787">50,00</span></span></td>
<td><span data-ttu-id="2813f-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-789">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-789">CC001</span></span></td>
<td><span data-ttu-id="2813f-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="2813f-790">HR</span></span></td>
<td><span data-ttu-id="2813f-791">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-791">10001</span></span></td>
<td><span data-ttu-id="2813f-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-792">Electricity</span></span></td>
<td><span data-ttu-id="2813f-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-793">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="2813f-794">-1,245.71</span></span></td>
<td><span data-ttu-id="2813f-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-796">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-796">CC002</span></span></td>
<td><span data-ttu-id="2813f-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-797">Finance</span></span></td>
<td><span data-ttu-id="2813f-798">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-798">10001</span></span></td>
<td><span data-ttu-id="2813f-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-799">Electricity</span></span></td>
<td><span data-ttu-id="2813f-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-800">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-801">436.00</span><span class="sxs-lookup"><span data-stu-id="2813f-801">436.00</span></span></td>
<td><span data-ttu-id="2813f-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-803">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-803">CC003</span></span></td>
<td><span data-ttu-id="2813f-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-804">Assembly</span></span></td>
<td><span data-ttu-id="2813f-805">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-805">10001</span></span></td>
<td><span data-ttu-id="2813f-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-806">Electricity</span></span></td>
<td><span data-ttu-id="2813f-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-807">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-808">685.14</span><span class="sxs-lookup"><span data-stu-id="2813f-808">685.14</span></span></td>
<td><span data-ttu-id="2813f-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-810">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-810">CC004</span></span></td>
<td><span data-ttu-id="2813f-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-811">Packaging</span></span></td>
<td><span data-ttu-id="2813f-812">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-812">10001</span></span></td>
<td><span data-ttu-id="2813f-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-813">Electricity</span></span></td>
<td><span data-ttu-id="2813f-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-814">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-815">124.57</span><span class="sxs-lookup"><span data-stu-id="2813f-815">124.57</span></span></td>
<td><span data-ttu-id="2813f-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-817">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-817">CC002</span></span></td>
<td><span data-ttu-id="2813f-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-818">Finance</span></span></td>
<td><span data-ttu-id="2813f-819">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-819">10001</span></span></td>
<td><span data-ttu-id="2813f-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-820">Electricity</span></span></td>
<td><span data-ttu-id="2813f-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-821">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="2813f-822">-675.00</span></span></td>
<td><span data-ttu-id="2813f-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-824">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-824">CC003</span></span></td>
<td><span data-ttu-id="2813f-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-825">Assembly</span></span></td>
<td><span data-ttu-id="2813f-826">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-826">10001</span></span></td>
<td><span data-ttu-id="2813f-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-827">Electricity</span></span></td>
<td><span data-ttu-id="2813f-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-828">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-829">438.75</span><span class="sxs-lookup"><span data-stu-id="2813f-829">438.75</span></span></td>
<td><span data-ttu-id="2813f-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-831">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-831">CC004</span></span></td>
<td><span data-ttu-id="2813f-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-832">Packaging</span></span></td>
<td><span data-ttu-id="2813f-833">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-833">10001</span></span></td>
<td><span data-ttu-id="2813f-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-834">Electricity</span></span></td>
<td><span data-ttu-id="2813f-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-835">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-836">236.25</span><span class="sxs-lookup"><span data-stu-id="2813f-836">236.25</span></span></td>
<td><span data-ttu-id="2813f-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-838">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-838">CC002</span></span></td>
<td><span data-ttu-id="2813f-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="2813f-839">Finance</span></span></td>
<td><span data-ttu-id="2813f-840">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-840">10001</span></span></td>
<td><span data-ttu-id="2813f-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-841">Electricity</span></span></td>
<td><span data-ttu-id="2813f-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-842">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="2813f-843">-8,150.29</span></span></td>
<td><span data-ttu-id="2813f-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-845">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-845">CC003</span></span></td>
<td><span data-ttu-id="2813f-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-846">Assembly</span></span></td>
<td><span data-ttu-id="2813f-847">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-847">10001</span></span></td>
<td><span data-ttu-id="2813f-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-848">Electricity</span></span></td>
<td><span data-ttu-id="2813f-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-849">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="2813f-850">5,297.69</span></span></td>
<td><span data-ttu-id="2813f-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-852">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-852">CC004</span></span></td>
<td><span data-ttu-id="2813f-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="2813f-853">Packaging</span></span></td>
<td><span data-ttu-id="2813f-854">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-854">10001</span></span></td>
<td><span data-ttu-id="2813f-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-855">Electricity</span></span></td>
<td><span data-ttu-id="2813f-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-856">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="2813f-857">2,852.60</span></span></td>
<td><span data-ttu-id="2813f-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-859">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-859">CC003</span></span></td>
<td><span data-ttu-id="2813f-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-860">Assembly</span></span></td>
<td><span data-ttu-id="2813f-861">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-861">10001</span></span></td>
<td><span data-ttu-id="2813f-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-862">Electricity</span></span></td>
<td><span data-ttu-id="2813f-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-863">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="2813f-864">-713.75</span></span></td>
<td><span data-ttu-id="2813f-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-866">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-867">Product 1</span></span></td>
<td><span data-ttu-id="2813f-868">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-868">10001</span></span></td>
<td><span data-ttu-id="2813f-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-869">Electricity</span></span></td>
<td><span data-ttu-id="2813f-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-870">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-871">535.31</span><span class="sxs-lookup"><span data-stu-id="2813f-871">535.31</span></span></td>
<td><span data-ttu-id="2813f-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-873">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-874">Product 2</span></span></td>
<td><span data-ttu-id="2813f-875">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-875">10001</span></span></td>
<td><span data-ttu-id="2813f-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-876">Electricity</span></span></td>
<td><span data-ttu-id="2813f-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-877">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-878">178.44</span><span class="sxs-lookup"><span data-stu-id="2813f-878">178.44</span></span></td>
<td><span data-ttu-id="2813f-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-880">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-880">CC003</span></span></td>
<td><span data-ttu-id="2813f-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-881">Assembly</span></span></td>
<td><span data-ttu-id="2813f-882">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-882">10001</span></span></td>
<td><span data-ttu-id="2813f-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-883">Electricity</span></span></td>
<td><span data-ttu-id="2813f-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-884">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="2813f-885">-5,982.83</span></span></td>
<td><span data-ttu-id="2813f-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-887">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-888">Product 1</span></span></td>
<td><span data-ttu-id="2813f-889">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-889">10001</span></span></td>
<td><span data-ttu-id="2813f-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-890">Electricity</span></span></td>
<td><span data-ttu-id="2813f-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-891">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="2813f-892">4,487.12</span></span></td>
<td><span data-ttu-id="2813f-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-894">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-895">Product 2</span></span></td>
<td><span data-ttu-id="2813f-896">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-896">10001</span></span></td>
<td><span data-ttu-id="2813f-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-897">Electricity</span></span></td>
<td><span data-ttu-id="2813f-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-898">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="2813f-899">1,495.71</span></span></td>
<td><span data-ttu-id="2813f-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-901">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-901">CC003</span></span></td>
<td><span data-ttu-id="2813f-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-902">Assembly</span></span></td>
<td><span data-ttu-id="2813f-903">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-903">10001</span></span></td>
<td><span data-ttu-id="2813f-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-904">Electricity</span></span></td>
<td><span data-ttu-id="2813f-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-905">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="2813f-906">-286.25</span></span></td>
<td><span data-ttu-id="2813f-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-908">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-909">Product 1</span></span></td>
<td><span data-ttu-id="2813f-910">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-910">10001</span></span></td>
<td><span data-ttu-id="2813f-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-911">Electricity</span></span></td>
<td><span data-ttu-id="2813f-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-912">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-913">241.05</span><span class="sxs-lookup"><span data-stu-id="2813f-913">241.05</span></span></td>
<td><span data-ttu-id="2813f-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-915">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-916">Product 2</span></span></td>
<td><span data-ttu-id="2813f-917">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-917">10001</span></span></td>
<td><span data-ttu-id="2813f-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-918">Electricity</span></span></td>
<td><span data-ttu-id="2813f-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-919">Fixed cost</span></span></td>
<td><span data-ttu-id="2813f-920">45.20</span><span class="sxs-lookup"><span data-stu-id="2813f-920">45.20</span></span></td>
<td><span data-ttu-id="2813f-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-922">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-922">CC003</span></span></td>
<td><span data-ttu-id="2813f-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="2813f-923">Assembly</span></span></td>
<td><span data-ttu-id="2813f-924">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-924">10001</span></span></td>
<td><span data-ttu-id="2813f-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-925">Electricity</span></span></td>
<td><span data-ttu-id="2813f-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-926">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="2813f-927">-2,977.17</span></span></td>
<td><span data-ttu-id="2813f-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-929">Prod 1</span></span></td>
<td><span data-ttu-id="2813f-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="2813f-930">Product 1</span></span></td>
<td><span data-ttu-id="2813f-931">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-931">10001</span></span></td>
<td><span data-ttu-id="2813f-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-932">Electricity</span></span></td>
<td><span data-ttu-id="2813f-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-933">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="2813f-934">2,507.09</span></span></td>
<td><span data-ttu-id="2813f-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2813f-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-936">Prod 2</span></span></td>
<td><span data-ttu-id="2813f-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="2813f-937">Product 2</span></span></td>
<td><span data-ttu-id="2813f-938">10001</span><span class="sxs-lookup"><span data-stu-id="2813f-938">10001</span></span></td>
<td><span data-ttu-id="2813f-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-939">Electricity</span></span></td>
<td><span data-ttu-id="2813f-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-940">Variable cost</span></span></td>
<td><span data-ttu-id="2813f-941">470.08</span><span class="sxs-lookup"><span data-stu-id="2813f-941">470.08</span></span></td>
<td><span data-ttu-id="2813f-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="2813f-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="2813f-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="2813f-943">Conclusion</span></span>
<span data-ttu-id="2813f-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="2813f-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="2813f-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="2813f-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="2813f-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="2813f-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="2813f-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="2813f-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="2813f-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="2813f-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="2813f-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2813f-951">CC099</span><span class="sxs-lookup"><span data-stu-id="2813f-951">CC099</span></span></th>
<th><span data-ttu-id="2813f-952">CC001</span><span class="sxs-lookup"><span data-stu-id="2813f-952">CC001</span></span></th>
<th><span data-ttu-id="2813f-953">CC002</span><span class="sxs-lookup"><span data-stu-id="2813f-953">CC002</span></span></th>
<th><span data-ttu-id="2813f-954">CC003</span><span class="sxs-lookup"><span data-stu-id="2813f-954">CC003</span></span></th>
<th><span data-ttu-id="2813f-955">CC004</span><span class="sxs-lookup"><span data-stu-id="2813f-955">CC004</span></span></th>
<th><span data-ttu-id="2813f-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="2813f-956">Proj 1</span></span></th>
<th><span data-ttu-id="2813f-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="2813f-957">Proj 2</span></span></th>
<th><span data-ttu-id="2813f-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="2813f-958">Prod 1</span></span></th>
<th><span data-ttu-id="2813f-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="2813f-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="2813f-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="2813f-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="2813f-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="2813f-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="2813f-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-971">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="2813f-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-973">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-974">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-975">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-976">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-977">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="2813f-978">776.36</span><span class="sxs-lookup"><span data-stu-id="2813f-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-979">223.64</span><span class="sxs-lookup"><span data-stu-id="2813f-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="2813f-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="2813f-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-982">000</span><span class="sxs-lookup"><span data-stu-id="2813f-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-983">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-984">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-985">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-986">0,00</span><span class="sxs-lookup"><span data-stu-id="2813f-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-987">30.00</span><span class="sxs-lookup"><span data-stu-id="2813f-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-988">10,00</span><span class="sxs-lookup"><span data-stu-id="2813f-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="2813f-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="2813f-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2813f-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="2813f-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2813f-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="2813f-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="2813f-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="2813f-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="2813f-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="2813f-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="2813f-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="2813f-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="2813f-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]