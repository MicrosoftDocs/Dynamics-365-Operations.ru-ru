---
title: Расчет накладных расходов
description: В этом разделе описываются типовые процессы расчета и распределения накладных расходов.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188005"
---
# <a name="overhead-calculation"></a><span data-ttu-id="14145-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="14145-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14145-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="14145-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="14145-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="14145-105">Term definition</span></span>

<span data-ttu-id="14145-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="14145-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="14145-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="14145-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="14145-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="14145-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="14145-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="14145-109">Rent</span></span>
-   <span data-ttu-id="14145-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-110">Electricity</span></span>
-   <span data-ttu-id="14145-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="14145-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="14145-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="14145-112">Overhead calculation overview</span></span>
<span data-ttu-id="14145-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="14145-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="14145-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="14145-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="14145-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="14145-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="14145-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="14145-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="14145-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="14145-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="14145-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="14145-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="14145-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="14145-119">Version type</span></span>
-   <span data-ttu-id="14145-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="14145-120">Date and time</span></span>
-   <span data-ttu-id="14145-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="14145-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="14145-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="14145-122">Fiscal year</span></span>
-   <span data-ttu-id="14145-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="14145-123">Fiscal period</span></span>

<span data-ttu-id="14145-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="14145-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="14145-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="14145-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="14145-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="14145-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="14145-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="14145-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="14145-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="14145-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="14145-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="14145-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="14145-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="14145-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="14145-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="14145-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="14145-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="14145-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="14145-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="14145-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="14145-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="14145-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="14145-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="14145-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="14145-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="14145-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="14145-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="14145-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="14145-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="14145-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="14145-140">Main account</span></span></th>
<th><span data-ttu-id="14145-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="14145-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="14145-143">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-143">CC099</span></span></td>
<td><span data-ttu-id="14145-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-144">Default cost center</span></span></td>
<td><span data-ttu-id="14145-145">10001</span><span class="sxs-lookup"><span data-stu-id="14145-145">10001</span></span></td>
<td><span data-ttu-id="14145-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-146">Electricity</span></span></td>
<td><span data-ttu-id="14145-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="14145-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="14145-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="14145-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="14145-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="14145-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="14145-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-151">Define the cost behavior rule</span></span>

<span data-ttu-id="14145-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="14145-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="14145-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="14145-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="14145-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="14145-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="14145-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="14145-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="14145-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="14145-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="14145-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="14145-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="14145-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-160">Journal</span></span></th>
<th><span data-ttu-id="14145-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="14145-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="14145-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="14145-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="14145-163">Версия</span><span class="sxs-lookup"><span data-stu-id="14145-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-164">00001</span><span class="sxs-lookup"><span data-stu-id="14145-164">00001</span></span></td>
<td><span data-ttu-id="14145-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="14145-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="14145-166">Fiscal</span></span></td>
<td><span data-ttu-id="14145-167">2017</span><span class="sxs-lookup"><span data-stu-id="14145-167">2017</span></span></td>
<td><span data-ttu-id="14145-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-168">Period 1</span></span></td>
<td><span data-ttu-id="14145-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="14145-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="14145-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="14145-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-173">Cost element</span></span></th>
<th><span data-ttu-id="14145-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-174">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="14145-177">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-177">CC099</span></span></td>
<td><span data-ttu-id="14145-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-178">Default cost center</span></span></td>
<td><span data-ttu-id="14145-179">10001</span><span class="sxs-lookup"><span data-stu-id="14145-179">10001</span></span></td>
<td><span data-ttu-id="14145-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-180">Electricity</span></span></td>
<td><span data-ttu-id="14145-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="14145-181">Unclassified</span></span></td>
<td><span data-ttu-id="14145-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="14145-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="14145-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="14145-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-185">Cost element</span></span></th>
<th><span data-ttu-id="14145-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-186">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-187">Amount</span></span></th>
<th><span data-ttu-id="14145-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-189">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-189">CC099</span></span></td>
<td><span data-ttu-id="14145-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-190">Default cost center</span></span></td>
<td><span data-ttu-id="14145-191">10001</span><span class="sxs-lookup"><span data-stu-id="14145-191">10001</span></span></td>
<td><span data-ttu-id="14145-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-192">Electricity</span></span></td>
<td><span data-ttu-id="14145-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="14145-193">Unclassified</span></span></td>
<td><span data-ttu-id="14145-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="14145-194">10,000.00</span></span></td>
<td><span data-ttu-id="14145-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-196">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-196">CC099</span></span></td>
<td><span data-ttu-id="14145-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-197">Default cost center</span></span></td>
<td><span data-ttu-id="14145-198">10001</span><span class="sxs-lookup"><span data-stu-id="14145-198">10001</span></span></td>
<td><span data-ttu-id="14145-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-199">Electricity</span></span></td>
<td><span data-ttu-id="14145-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="14145-200">Unclassified</span></span></td>
<td><span data-ttu-id="14145-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="14145-201">-10,000.00</span></span></td>
<td><span data-ttu-id="14145-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-203">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-203">CC099</span></span></td>
<td><span data-ttu-id="14145-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-204">Default cost center</span></span></td>
<td><span data-ttu-id="14145-205">10001</span><span class="sxs-lookup"><span data-stu-id="14145-205">10001</span></span></td>
<td><span data-ttu-id="14145-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-206">Electricity</span></span></td>
<td><span data-ttu-id="14145-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-207">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="14145-208">1,000.00</span></span></td>
<td><span data-ttu-id="14145-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-210">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-210">CC099</span></span></td>
<td><span data-ttu-id="14145-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-211">Default cost center</span></span></td>
<td><span data-ttu-id="14145-212">10001</span><span class="sxs-lookup"><span data-stu-id="14145-212">10001</span></span></td>
<td><span data-ttu-id="14145-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-213">Electricity</span></span></td>
<td><span data-ttu-id="14145-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-214">Variable cost</span></span></td>
<td><span data-ttu-id="14145-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="14145-215">9,000.00</span></span></td>
<td><span data-ttu-id="14145-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="14145-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="14145-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="14145-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="14145-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="14145-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-221">Define the cost distribution rule</span></span>

<span data-ttu-id="14145-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="14145-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="14145-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="14145-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="14145-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="14145-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="14145-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="14145-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="14145-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="14145-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="14145-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-228">Cost object</span></span></th>
<th><span data-ttu-id="14145-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="14145-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-230">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-230">CC001</span></span></td>
<td><span data-ttu-id="14145-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-231">HR</span></span></td>
<td><span data-ttu-id="14145-232">1000</span><span class="sxs-lookup"><span data-stu-id="14145-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-233">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-233">CC002</span></span></td>
<td><span data-ttu-id="14145-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-234">Finance</span></span></td>
<td><span data-ttu-id="14145-235">6,000</span><span class="sxs-lookup"><span data-stu-id="14145-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-236">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-236">CC003</span></span></td>
<td><span data-ttu-id="14145-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-237">Assembly</span></span></td>
<td><span data-ttu-id="14145-238">0</span><span class="sxs-lookup"><span data-stu-id="14145-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-240">Cost object</span></span></th>
<th><span data-ttu-id="14145-241">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-241">Magnitude</span></span></th>
<th><span data-ttu-id="14145-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-242">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-244">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-244">CC001</span></span></td>
<td><span data-ttu-id="14145-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-245">HR</span></span></td>
<td><span data-ttu-id="14145-246">1000</span><span class="sxs-lookup"><span data-stu-id="14145-246">1,000</span></span></td>
<td><span data-ttu-id="14145-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="14145-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="14145-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="14145-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-249">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-249">CC002</span></span></td>
<td><span data-ttu-id="14145-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-250">Finance</span></span></td>
<td><span data-ttu-id="14145-251">6,000</span><span class="sxs-lookup"><span data-stu-id="14145-251">6,000</span></span></td>
<td><span data-ttu-id="14145-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="14145-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="14145-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="14145-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-254">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-254">CC003</span></span></td>
<td><span data-ttu-id="14145-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-255">Assembly</span></span></td>
<td><span data-ttu-id="14145-256">0</span><span class="sxs-lookup"><span data-stu-id="14145-256">0</span></span></td>
<td><span data-ttu-id="14145-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="14145-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="14145-258">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="14145-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="14145-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-261">Cost object</span></span></th>
<th><span data-ttu-id="14145-262">Формула</span><span class="sxs-lookup"><span data-stu-id="14145-262">Formula</span></span></th>
<th><span data-ttu-id="14145-263">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-263">Magnitude</span></span></th>
<th><span data-ttu-id="14145-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-264">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-266">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-266">CC001</span></span></td>
<td><span data-ttu-id="14145-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-267">HR</span></span></td>
<td><span data-ttu-id="14145-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="14145-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="14145-269">1</span><span class="sxs-lookup"><span data-stu-id="14145-269">1</span></span></td>
<td><span data-ttu-id="14145-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="14145-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="14145-271">500.00</span><span class="sxs-lookup"><span data-stu-id="14145-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-272">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-272">CC002</span></span></td>
<td><span data-ttu-id="14145-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-273">Finance</span></span></td>
<td><span data-ttu-id="14145-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="14145-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="14145-275">1</span><span class="sxs-lookup"><span data-stu-id="14145-275">1</span></span></td>
<td><span data-ttu-id="14145-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="14145-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="14145-277">500.00</span><span class="sxs-lookup"><span data-stu-id="14145-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-278">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-278">CC003</span></span></td>
<td><span data-ttu-id="14145-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-279">Assembly</span></span></td>
<td><span data-ttu-id="14145-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="14145-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="14145-281">0</span><span class="sxs-lookup"><span data-stu-id="14145-281">0</span></span></td>
<td><span data-ttu-id="14145-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="14145-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="14145-283">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="14145-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-285">Journal</span></span></th>
<th><span data-ttu-id="14145-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="14145-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="14145-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="14145-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="14145-288">Версия</span><span class="sxs-lookup"><span data-stu-id="14145-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-289">00002</span><span class="sxs-lookup"><span data-stu-id="14145-289">00002</span></span></td>
<td><span data-ttu-id="14145-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="14145-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="14145-291">Fiscal</span></span></td>
<td><span data-ttu-id="14145-292">2017</span><span class="sxs-lookup"><span data-stu-id="14145-292">2017</span></span></td>
<td><span data-ttu-id="14145-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-293">Period 1</span></span></td>
<td><span data-ttu-id="14145-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="14145-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="14145-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="14145-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-298">Cost element</span></span></th>
<th><span data-ttu-id="14145-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-299">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-302">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-302">CC099</span></span></td>
<td><span data-ttu-id="14145-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-303">Default cost center</span></span></td>
<td><span data-ttu-id="14145-304">10001</span><span class="sxs-lookup"><span data-stu-id="14145-304">10001</span></span></td>
<td><span data-ttu-id="14145-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-305">Electricity</span></span></td>
<td><span data-ttu-id="14145-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-306">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="14145-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-309">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-309">CC099</span></span></td>
<td><span data-ttu-id="14145-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-310">Default cost center</span></span></td>
<td><span data-ttu-id="14145-311">10001</span><span class="sxs-lookup"><span data-stu-id="14145-311">10001</span></span></td>
<td><span data-ttu-id="14145-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-312">Electricity</span></span></td>
<td><span data-ttu-id="14145-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-313">Variable cost</span></span></td>
<td><span data-ttu-id="14145-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="14145-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="14145-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="14145-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-317">Cost element</span></span></th>
<th><span data-ttu-id="14145-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-318">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-319">Amount</span></span></th>
<th><span data-ttu-id="14145-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-321">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-321">CC099</span></span></td>
<td><span data-ttu-id="14145-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-322">Default cost center</span></span></td>
<td><span data-ttu-id="14145-323">10001</span><span class="sxs-lookup"><span data-stu-id="14145-323">10001</span></span></td>
<td><span data-ttu-id="14145-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-324">Electricity</span></span></td>
<td><span data-ttu-id="14145-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-325">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="14145-326">-1,000.00</span></span></td>
<td><span data-ttu-id="14145-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-328">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-328">CC001</span></span></td>
<td><span data-ttu-id="14145-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-329">HR</span></span></td>
<td><span data-ttu-id="14145-330">10001</span><span class="sxs-lookup"><span data-stu-id="14145-330">10001</span></span></td>
<td><span data-ttu-id="14145-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-331">Electricity</span></span></td>
<td><span data-ttu-id="14145-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-332">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-333">500.00</span><span class="sxs-lookup"><span data-stu-id="14145-333">500.00</span></span></td>
<td><span data-ttu-id="14145-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-335">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-335">CC002</span></span></td>
<td><span data-ttu-id="14145-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-336">Finance</span></span></td>
<td><span data-ttu-id="14145-337">10001</span><span class="sxs-lookup"><span data-stu-id="14145-337">10001</span></span></td>
<td><span data-ttu-id="14145-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-338">Electricity</span></span></td>
<td><span data-ttu-id="14145-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-339">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-340">500.00</span><span class="sxs-lookup"><span data-stu-id="14145-340">500.00</span></span></td>
<td><span data-ttu-id="14145-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-342">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-342">CC099</span></span></td>
<td><span data-ttu-id="14145-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14145-343">Default cost center</span></span></td>
<td><span data-ttu-id="14145-344">10001</span><span class="sxs-lookup"><span data-stu-id="14145-344">10001</span></span></td>
<td><span data-ttu-id="14145-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-345">Electricity</span></span></td>
<td><span data-ttu-id="14145-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-346">Variable cost</span></span></td>
<td><span data-ttu-id="14145-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="14145-347">-9,000.00</span></span></td>
<td><span data-ttu-id="14145-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-349">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-349">CC001</span></span></td>
<td><span data-ttu-id="14145-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-350">HR</span></span></td>
<td><span data-ttu-id="14145-351">10001</span><span class="sxs-lookup"><span data-stu-id="14145-351">10001</span></span></td>
<td><span data-ttu-id="14145-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-352">Electricity</span></span></td>
<td><span data-ttu-id="14145-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-353">Variable cost</span></span></td>
<td><span data-ttu-id="14145-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="14145-354">1,285.71</span></span></td>
<td><span data-ttu-id="14145-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-356">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-356">CC002</span></span></td>
<td><span data-ttu-id="14145-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-357">Finance</span></span></td>
<td><span data-ttu-id="14145-358">10001</span><span class="sxs-lookup"><span data-stu-id="14145-358">10001</span></span></td>
<td><span data-ttu-id="14145-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-359">Electricity</span></span></td>
<td><span data-ttu-id="14145-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-360">Variable cost</span></span></td>
<td><span data-ttu-id="14145-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="14145-361">7,714.29</span></span></td>
<td><span data-ttu-id="14145-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="14145-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="14145-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="14145-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="14145-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="14145-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="14145-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="14145-367">Define the overhead rate</span></span>

<span data-ttu-id="14145-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="14145-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="14145-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="14145-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-370">Cost object</span></span></th>
<th><span data-ttu-id="14145-371">Часы</span><span class="sxs-lookup"><span data-stu-id="14145-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-372">Proj 1</span></span></td>
<td><span data-ttu-id="14145-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-373">Project 1</span></span></td>
<td><span data-ttu-id="14145-374">3</span><span class="sxs-lookup"><span data-stu-id="14145-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-375">Proj 2</span></span></td>
<td><span data-ttu-id="14145-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-376">Project 2</span></span></td>
<td><span data-ttu-id="14145-377">1</span><span class="sxs-lookup"><span data-stu-id="14145-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-379">Cost object</span></span></th>
<th><span data-ttu-id="14145-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-380">Cost element</span></span></th>
<th><span data-ttu-id="14145-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-381">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="14145-382">Units</span></span></th>
<th><span data-ttu-id="14145-383">По норме</span><span class="sxs-lookup"><span data-stu-id="14145-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-384">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-384">CC001</span></span></td>
<td><span data-ttu-id="14145-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-385">HR</span></span></td>
<td><span data-ttu-id="14145-386">10001</span><span class="sxs-lookup"><span data-stu-id="14145-386">10001</span></span></td>
<td><span data-ttu-id="14145-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-387">Variable cost</span></span></td>
<td><span data-ttu-id="14145-388">1</span><span class="sxs-lookup"><span data-stu-id="14145-388">1</span></span></td>
<td><span data-ttu-id="14145-389">10</span><span class="sxs-lookup"><span data-stu-id="14145-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-391">Cost object</span></span></th>
<th><span data-ttu-id="14145-392">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-392">Magnitude</span></span></th>
<th><span data-ttu-id="14145-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-393">Cost element</span></span></th>
<th><span data-ttu-id="14145-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-394">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-396">Proj 1</span></span></td>
<td><span data-ttu-id="14145-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-397">Project 1</span></span></td>
<td><span data-ttu-id="14145-398">3</span><span class="sxs-lookup"><span data-stu-id="14145-398">3</span></span></td>
<td><span data-ttu-id="14145-399">10001</span><span class="sxs-lookup"><span data-stu-id="14145-399">10001</span></span></td>
<td><span data-ttu-id="14145-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="14145-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="14145-401">30.00</span><span class="sxs-lookup"><span data-stu-id="14145-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-402">Proj 2</span></span></td>
<td><span data-ttu-id="14145-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-403">Project 2</span></span></td>
<td><span data-ttu-id="14145-404">1</span><span class="sxs-lookup"><span data-stu-id="14145-404">1</span></span></td>
<td><span data-ttu-id="14145-405">10001</span><span class="sxs-lookup"><span data-stu-id="14145-405">10001</span></span></td>
<td><span data-ttu-id="14145-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="14145-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="14145-407">10,00</span><span class="sxs-lookup"><span data-stu-id="14145-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="14145-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-409">Journal</span></span></th>
<th><span data-ttu-id="14145-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="14145-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="14145-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="14145-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="14145-412">Версия</span><span class="sxs-lookup"><span data-stu-id="14145-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-413">00003</span><span class="sxs-lookup"><span data-stu-id="14145-413">00003</span></span></td>
<td><span data-ttu-id="14145-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="14145-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="14145-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="14145-415">Fiscal</span></span></td>
<td><span data-ttu-id="14145-416">2017</span><span class="sxs-lookup"><span data-stu-id="14145-416">2017</span></span></td>
<td><span data-ttu-id="14145-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-417">Period 1</span></span></td>
<td><span data-ttu-id="14145-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="14145-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="14145-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="14145-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-421">Cost object</span></span></th>
<th><span data-ttu-id="14145-422">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-424">Proj 1</span></span></td>
<td><span data-ttu-id="14145-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="14145-426">3,00</span><span class="sxs-lookup"><span data-stu-id="14145-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-428">Proj 2</span></span></td>
<td><span data-ttu-id="14145-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="14145-430">1.00</span><span class="sxs-lookup"><span data-stu-id="14145-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="14145-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="14145-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-433">Cost element</span></span></th>
<th><span data-ttu-id="14145-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-434">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-435">Amount</span></span></th>
<th><span data-ttu-id="14145-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="14145-437">CC0001</span></span></td>
<td><span data-ttu-id="14145-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-438">HR</span></span></td>
<td><span data-ttu-id="14145-439">10001</span><span class="sxs-lookup"><span data-stu-id="14145-439">10001</span></span></td>
<td><span data-ttu-id="14145-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-440">Electricity</span></span></td>
<td><span data-ttu-id="14145-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-441">Variable cost</span></span></td>
<td><span data-ttu-id="14145-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="14145-442">-30.00</span></span></td>
<td><span data-ttu-id="14145-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-444">Proj 1</span></span></td>
<td><span data-ttu-id="14145-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="14145-446">10001</span><span class="sxs-lookup"><span data-stu-id="14145-446">10001</span></span></td>
<td><span data-ttu-id="14145-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-447">Electricity</span></span></td>
<td><span data-ttu-id="14145-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-448">Variable cost</span></span></td>
<td><span data-ttu-id="14145-449">30.00</span><span class="sxs-lookup"><span data-stu-id="14145-449">30.00</span></span></td>
<td><span data-ttu-id="14145-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-451">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-451">CC001</span></span></td>
<td><span data-ttu-id="14145-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-452">HR</span></span></td>
<td><span data-ttu-id="14145-453">10001</span><span class="sxs-lookup"><span data-stu-id="14145-453">10001</span></span></td>
<td><span data-ttu-id="14145-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-454">Electricity</span></span></td>
<td><span data-ttu-id="14145-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-455">Variable cost</span></span></td>
<td><span data-ttu-id="14145-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="14145-456">-10.00</span></span></td>
<td><span data-ttu-id="14145-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-458">Proj 2</span></span></td>
<td><span data-ttu-id="14145-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="14145-460">10001</span><span class="sxs-lookup"><span data-stu-id="14145-460">10001</span></span></td>
<td><span data-ttu-id="14145-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-461">Electricity</span></span></td>
<td><span data-ttu-id="14145-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-462">Variable cost</span></span></td>
<td><span data-ttu-id="14145-463">10.00</span><span class="sxs-lookup"><span data-stu-id="14145-463">10.00</span></span></td>
<td><span data-ttu-id="14145-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="14145-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="14145-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="14145-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="14145-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="14145-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="14145-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="14145-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="14145-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="14145-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="14145-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="14145-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="14145-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="14145-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="14145-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="14145-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="14145-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="14145-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-475">Define the cost allocation</span></span>

<span data-ttu-id="14145-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="14145-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="14145-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="14145-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-479">Cost object</span></span></th>
<th><span data-ttu-id="14145-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="14145-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-481">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-481">CC002</span></span></td>
<td><span data-ttu-id="14145-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-482">Finance</span></span></td>
<td><span data-ttu-id="14145-483">35</span><span class="sxs-lookup"><span data-stu-id="14145-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-484">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-484">CC003</span></span></td>
<td><span data-ttu-id="14145-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-485">Assembly</span></span></td>
<td><span data-ttu-id="14145-486">55</span><span class="sxs-lookup"><span data-stu-id="14145-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-487">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-487">CC004</span></span></td>
<td><span data-ttu-id="14145-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-488">Packaging</span></span></td>
<td><span data-ttu-id="14145-489">10</span><span class="sxs-lookup"><span data-stu-id="14145-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="14145-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="14145-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-492">Cost object</span></span></th>
<th><span data-ttu-id="14145-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="14145-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-494">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-494">CC003</span></span></td>
<td><span data-ttu-id="14145-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-495">Assembly</span></span></td>
<td><span data-ttu-id="14145-496">65</span><span class="sxs-lookup"><span data-stu-id="14145-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-497">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-497">CC004</span></span></td>
<td><span data-ttu-id="14145-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-498">Packaging</span></span></td>
<td><span data-ttu-id="14145-499">35</span><span class="sxs-lookup"><span data-stu-id="14145-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="14145-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="14145-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-502">Cost object</span></span></th>
<th><span data-ttu-id="14145-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="14145-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-504">Prod 1</span></span></td>
<td><span data-ttu-id="14145-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-505">Product 1</span></span></td>
<td><span data-ttu-id="14145-506">60</span><span class="sxs-lookup"><span data-stu-id="14145-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-507">Prod 2</span></span></td>
<td><span data-ttu-id="14145-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-508">Product 2</span></span></td>
<td><span data-ttu-id="14145-509">20</span><span class="sxs-lookup"><span data-stu-id="14145-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="14145-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="14145-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-512">Cost object</span></span></th>
<th><span data-ttu-id="14145-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="14145-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-514">Prod 1</span></span></td>
<td><span data-ttu-id="14145-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-515">Product 1</span></span></td>
<td><span data-ttu-id="14145-516">80</span><span class="sxs-lookup"><span data-stu-id="14145-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-517">Prod 2</span></span></td>
<td><span data-ttu-id="14145-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-518">Product 2</span></span></td>
<td><span data-ttu-id="14145-519">15</span><span class="sxs-lookup"><span data-stu-id="14145-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="14145-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="14145-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="14145-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="14145-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="14145-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="14145-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-523">Cost object</span></span></th>
<th><span data-ttu-id="14145-524">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-524">Magnitude</span></span></th>
<th><span data-ttu-id="14145-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-525">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-526">Amount</span></span></th>
<th><span data-ttu-id="14145-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-528">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-528">CC002</span></span></td>
<td><span data-ttu-id="14145-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-529">Finance</span></span></td>
<td><span data-ttu-id="14145-530">35</span><span class="sxs-lookup"><span data-stu-id="14145-530">35</span></span></td>
<td><span data-ttu-id="14145-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="14145-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="14145-532">175.00</span><span class="sxs-lookup"><span data-stu-id="14145-532">175.00</span></span></td>
<td><span data-ttu-id="14145-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-534">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-534">CC003</span></span></td>
<td><span data-ttu-id="14145-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-535">Assembly</span></span></td>
<td><span data-ttu-id="14145-536">55</span><span class="sxs-lookup"><span data-stu-id="14145-536">55</span></span></td>
<td><span data-ttu-id="14145-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="14145-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="14145-538">275.00</span><span class="sxs-lookup"><span data-stu-id="14145-538">275.00</span></span></td>
<td><span data-ttu-id="14145-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-540">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-540">CC004</span></span></td>
<td><span data-ttu-id="14145-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-541">Packaging</span></span></td>
<td><span data-ttu-id="14145-542">10</span><span class="sxs-lookup"><span data-stu-id="14145-542">10</span></span></td>
<td><span data-ttu-id="14145-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="14145-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="14145-544">50,00</span><span class="sxs-lookup"><span data-stu-id="14145-544">50.00</span></span></td>
<td><span data-ttu-id="14145-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-546">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-546">CC002</span></span></td>
<td><span data-ttu-id="14145-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-547">Finance</span></span></td>
<td><span data-ttu-id="14145-548">35</span><span class="sxs-lookup"><span data-stu-id="14145-548">35</span></span></td>
<td><span data-ttu-id="14145-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="14145-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="14145-550">436.00</span><span class="sxs-lookup"><span data-stu-id="14145-550">436.00</span></span></td>
<td><span data-ttu-id="14145-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-552">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-552">CC003</span></span></td>
<td><span data-ttu-id="14145-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-553">Assembly</span></span></td>
<td><span data-ttu-id="14145-554">55</span><span class="sxs-lookup"><span data-stu-id="14145-554">55</span></span></td>
<td><span data-ttu-id="14145-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="14145-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="14145-556">685.14</span><span class="sxs-lookup"><span data-stu-id="14145-556">685.14</span></span></td>
<td><span data-ttu-id="14145-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-558">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-558">CC004</span></span></td>
<td><span data-ttu-id="14145-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-559">Packaging</span></span></td>
<td><span data-ttu-id="14145-560">10</span><span class="sxs-lookup"><span data-stu-id="14145-560">10</span></span></td>
<td><span data-ttu-id="14145-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="14145-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="14145-562">124.57</span><span class="sxs-lookup"><span data-stu-id="14145-562">124.57</span></span></td>
<td><span data-ttu-id="14145-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="14145-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-565">Cost object</span></span></th>
<th><span data-ttu-id="14145-566">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-566">Magnitude</span></span></th>
<th><span data-ttu-id="14145-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-567">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-568">Amount</span></span></th>
<th><span data-ttu-id="14145-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-570">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-570">CC003</span></span></td>
<td><span data-ttu-id="14145-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-571">Assembly</span></span></td>
<td><span data-ttu-id="14145-572">65</span><span class="sxs-lookup"><span data-stu-id="14145-572">65</span></span></td>
<td><span data-ttu-id="14145-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="14145-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="14145-574">438.75</span><span class="sxs-lookup"><span data-stu-id="14145-574">438.75</span></span></td>
<td><span data-ttu-id="14145-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-576">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-576">CC004</span></span></td>
<td><span data-ttu-id="14145-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-577">Packaging</span></span></td>
<td><span data-ttu-id="14145-578">35</span><span class="sxs-lookup"><span data-stu-id="14145-578">35</span></span></td>
<td><span data-ttu-id="14145-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="14145-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="14145-580">236.25</span><span class="sxs-lookup"><span data-stu-id="14145-580">236.25</span></span></td>
<td><span data-ttu-id="14145-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-582">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-582">CC003</span></span></td>
<td><span data-ttu-id="14145-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-583">Assembly</span></span></td>
<td><span data-ttu-id="14145-584">65</span><span class="sxs-lookup"><span data-stu-id="14145-584">65</span></span></td>
<td><span data-ttu-id="14145-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="14145-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="14145-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="14145-586">5,297.69</span></span></td>
<td><span data-ttu-id="14145-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-588">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-588">CC004</span></span></td>
<td><span data-ttu-id="14145-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-589">Packaging</span></span></td>
<td><span data-ttu-id="14145-590">35</span><span class="sxs-lookup"><span data-stu-id="14145-590">35</span></span></td>
<td><span data-ttu-id="14145-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="14145-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="14145-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="14145-592">2,852.60</span></span></td>
<td><span data-ttu-id="14145-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="14145-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-595">Cost object</span></span></th>
<th><span data-ttu-id="14145-596">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-596">Magnitude</span></span></th>
<th><span data-ttu-id="14145-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-597">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-598">Amount</span></span></th>
<th><span data-ttu-id="14145-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-600">Prod 1</span></span></td>
<td><span data-ttu-id="14145-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-601">Product 1</span></span></td>
<td><span data-ttu-id="14145-602">60</span><span class="sxs-lookup"><span data-stu-id="14145-602">60</span></span></td>
<td><span data-ttu-id="14145-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="14145-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="14145-604">535.31</span><span class="sxs-lookup"><span data-stu-id="14145-604">535.31</span></span></td>
<td><span data-ttu-id="14145-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-606">Prod 2</span></span></td>
<td><span data-ttu-id="14145-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-607">Product 2</span></span></td>
<td><span data-ttu-id="14145-608">20</span><span class="sxs-lookup"><span data-stu-id="14145-608">20</span></span></td>
<td><span data-ttu-id="14145-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="14145-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="14145-610">178.44</span><span class="sxs-lookup"><span data-stu-id="14145-610">178.44</span></span></td>
<td><span data-ttu-id="14145-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-612">Prod 1</span></span></td>
<td><span data-ttu-id="14145-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-613">Product 1</span></span></td>
<td><span data-ttu-id="14145-614">60</span><span class="sxs-lookup"><span data-stu-id="14145-614">60</span></span></td>
<td><span data-ttu-id="14145-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="14145-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="14145-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="14145-616">4,487.12</span></span></td>
<td><span data-ttu-id="14145-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-618">Prod 2</span></span></td>
<td><span data-ttu-id="14145-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-619">Product 2</span></span></td>
<td><span data-ttu-id="14145-620">20</span><span class="sxs-lookup"><span data-stu-id="14145-620">20</span></span></td>
<td><span data-ttu-id="14145-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="14145-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="14145-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="14145-622">1,495.71</span></span></td>
<td><span data-ttu-id="14145-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="14145-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="14145-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-625">Cost object</span></span></th>
<th><span data-ttu-id="14145-626">Величина</span><span class="sxs-lookup"><span data-stu-id="14145-626">Magnitude</span></span></th>
<th><span data-ttu-id="14145-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="14145-627">Allocation factor</span></span></th>
<th><span data-ttu-id="14145-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-628">Amount</span></span></th>
<th><span data-ttu-id="14145-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-630">Prod 1</span></span></td>
<td><span data-ttu-id="14145-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-631">Product 1</span></span></td>
<td><span data-ttu-id="14145-632">80</span><span class="sxs-lookup"><span data-stu-id="14145-632">80</span></span></td>
<td><span data-ttu-id="14145-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="14145-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="14145-634">241.05</span><span class="sxs-lookup"><span data-stu-id="14145-634">241.05</span></span></td>
<td><span data-ttu-id="14145-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-636">Prod 2</span></span></td>
<td><span data-ttu-id="14145-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-637">Product 2</span></span></td>
<td><span data-ttu-id="14145-638">15</span><span class="sxs-lookup"><span data-stu-id="14145-638">15</span></span></td>
<td><span data-ttu-id="14145-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="14145-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="14145-640">45.20</span><span class="sxs-lookup"><span data-stu-id="14145-640">45.20</span></span></td>
<td><span data-ttu-id="14145-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-642">Prod 1</span></span></td>
<td><span data-ttu-id="14145-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-643">Product 1</span></span></td>
<td><span data-ttu-id="14145-644">80</span><span class="sxs-lookup"><span data-stu-id="14145-644">80</span></span></td>
<td><span data-ttu-id="14145-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="14145-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="14145-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="14145-646">2,507.09</span></span></td>
<td><span data-ttu-id="14145-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-648">Prod 2</span></span></td>
<td><span data-ttu-id="14145-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-649">Product 2</span></span></td>
<td><span data-ttu-id="14145-650">15</span><span class="sxs-lookup"><span data-stu-id="14145-650">15</span></span></td>
<td><span data-ttu-id="14145-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="14145-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="14145-652">470.08</span><span class="sxs-lookup"><span data-stu-id="14145-652">470.08</span></span></td>
<td><span data-ttu-id="14145-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="14145-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="14145-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="14145-655">Journal</span></span></th>
<th><span data-ttu-id="14145-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="14145-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="14145-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="14145-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="14145-658">Версия</span><span class="sxs-lookup"><span data-stu-id="14145-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-659">00004</span><span class="sxs-lookup"><span data-stu-id="14145-659">00004</span></span></td>
<td><span data-ttu-id="14145-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="14145-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="14145-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="14145-661">Fiscal</span></span></td>
<td><span data-ttu-id="14145-662">2017</span><span class="sxs-lookup"><span data-stu-id="14145-662">2017</span></span></td>
<td><span data-ttu-id="14145-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-663">Period 1</span></span></td>
<td><span data-ttu-id="14145-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="14145-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="14145-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="14145-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14145-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="14145-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-668">Cost element</span></span></th>
<th><span data-ttu-id="14145-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-669">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-672">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-672">CC001</span></span></td>
<td><span data-ttu-id="14145-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-673">HR</span></span></td>
<td><span data-ttu-id="14145-674">10001</span><span class="sxs-lookup"><span data-stu-id="14145-674">10001</span></span></td>
<td><span data-ttu-id="14145-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-675">Electricity</span></span></td>
<td><span data-ttu-id="14145-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-676">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-677">500.00</span><span class="sxs-lookup"><span data-stu-id="14145-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-679">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-679">CC001</span></span></td>
<td><span data-ttu-id="14145-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-680">HR</span></span></td>
<td><span data-ttu-id="14145-681">10001</span><span class="sxs-lookup"><span data-stu-id="14145-681">10001</span></span></td>
<td><span data-ttu-id="14145-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-682">Electricity</span></span></td>
<td><span data-ttu-id="14145-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-683">Variable cost</span></span></td>
<td><span data-ttu-id="14145-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="14145-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-686">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-686">CC002</span></span></td>
<td><span data-ttu-id="14145-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-687">Finance</span></span></td>
<td><span data-ttu-id="14145-688">10001</span><span class="sxs-lookup"><span data-stu-id="14145-688">10001</span></span></td>
<td><span data-ttu-id="14145-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-689">Electricity</span></span></td>
<td><span data-ttu-id="14145-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-690">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-691">675.00</span><span class="sxs-lookup"><span data-stu-id="14145-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-693">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-693">CC002</span></span></td>
<td><span data-ttu-id="14145-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-694">Finance</span></span></td>
<td><span data-ttu-id="14145-695">10001</span><span class="sxs-lookup"><span data-stu-id="14145-695">10001</span></span></td>
<td><span data-ttu-id="14145-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-696">Electricity</span></span></td>
<td><span data-ttu-id="14145-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-697">Variable cost</span></span></td>
<td><span data-ttu-id="14145-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="14145-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-700">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-700">CC003</span></span></td>
<td><span data-ttu-id="14145-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-701">Assembly</span></span></td>
<td><span data-ttu-id="14145-702">10001</span><span class="sxs-lookup"><span data-stu-id="14145-702">10001</span></span></td>
<td><span data-ttu-id="14145-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-703">Electricity</span></span></td>
<td><span data-ttu-id="14145-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-704">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-705">713.75</span><span class="sxs-lookup"><span data-stu-id="14145-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-707">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-707">CC003</span></span></td>
<td><span data-ttu-id="14145-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-708">Assembly</span></span></td>
<td><span data-ttu-id="14145-709">10001</span><span class="sxs-lookup"><span data-stu-id="14145-709">10001</span></span></td>
<td><span data-ttu-id="14145-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-710">Electricity</span></span></td>
<td><span data-ttu-id="14145-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-711">Variable cost</span></span></td>
<td><span data-ttu-id="14145-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="14145-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-714">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-714">CC003</span></span></td>
<td><span data-ttu-id="14145-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-715">Packaging</span></span></td>
<td><span data-ttu-id="14145-716">10001</span><span class="sxs-lookup"><span data-stu-id="14145-716">10001</span></span></td>
<td><span data-ttu-id="14145-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-717">Electricity</span></span></td>
<td><span data-ttu-id="14145-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-718">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-719">286.25</span><span class="sxs-lookup"><span data-stu-id="14145-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-721">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-721">CC003</span></span></td>
<td><span data-ttu-id="14145-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-722">Packaging</span></span></td>
<td><span data-ttu-id="14145-723">10001</span><span class="sxs-lookup"><span data-stu-id="14145-723">10001</span></span></td>
<td><span data-ttu-id="14145-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-724">Electricity</span></span></td>
<td><span data-ttu-id="14145-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-725">Variable cost</span></span></td>
<td><span data-ttu-id="14145-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="14145-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-728">Prod 1</span></span></td>
<td><span data-ttu-id="14145-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-729">Product 1</span></span></td>
<td><span data-ttu-id="14145-730">10001</span><span class="sxs-lookup"><span data-stu-id="14145-730">10001</span></span></td>
<td><span data-ttu-id="14145-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-731">Electricity</span></span></td>
<td><span data-ttu-id="14145-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-732">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-733">776.36</span><span class="sxs-lookup"><span data-stu-id="14145-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-735">Prod 1</span></span></td>
<td><span data-ttu-id="14145-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-736">Product 1</span></span></td>
<td><span data-ttu-id="14145-737">10001</span><span class="sxs-lookup"><span data-stu-id="14145-737">10001</span></span></td>
<td><span data-ttu-id="14145-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-738">Electricity</span></span></td>
<td><span data-ttu-id="14145-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-739">Variable cost</span></span></td>
<td><span data-ttu-id="14145-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="14145-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-742">Prod 2</span></span></td>
<td><span data-ttu-id="14145-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-743">Product 1</span></span></td>
<td><span data-ttu-id="14145-744">10001</span><span class="sxs-lookup"><span data-stu-id="14145-744">10001</span></span></td>
<td><span data-ttu-id="14145-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-745">Electricity</span></span></td>
<td><span data-ttu-id="14145-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-746">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-747">223.64</span><span class="sxs-lookup"><span data-stu-id="14145-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="14145-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-749">Prod 2</span></span></td>
<td><span data-ttu-id="14145-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-750">Product 1</span></span></td>
<td><span data-ttu-id="14145-751">10001</span><span class="sxs-lookup"><span data-stu-id="14145-751">10001</span></span></td>
<td><span data-ttu-id="14145-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-752">Electricity</span></span></td>
<td><span data-ttu-id="14145-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-753">Variable cost</span></span></td>
<td><span data-ttu-id="14145-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="14145-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="14145-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="14145-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="14145-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="14145-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-757">Cost element</span></span></th>
<th><span data-ttu-id="14145-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="14145-758">Cost behavior</span></span></th>
<th><span data-ttu-id="14145-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="14145-759">Amount</span></span></th>
<th><span data-ttu-id="14145-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="14145-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14145-761">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-761">CC001</span></span></td>
<td><span data-ttu-id="14145-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-762">HR</span></span></td>
<td><span data-ttu-id="14145-763">10001</span><span class="sxs-lookup"><span data-stu-id="14145-763">10001</span></span></td>
<td><span data-ttu-id="14145-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-764">Electricity</span></span></td>
<td><span data-ttu-id="14145-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-765">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="14145-766">-500.00</span></span></td>
<td><span data-ttu-id="14145-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-768">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-768">CC002</span></span></td>
<td><span data-ttu-id="14145-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-769">Finance</span></span></td>
<td><span data-ttu-id="14145-770">10001</span><span class="sxs-lookup"><span data-stu-id="14145-770">10001</span></span></td>
<td><span data-ttu-id="14145-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-771">Electricity</span></span></td>
<td><span data-ttu-id="14145-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-772">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-773">175.00</span><span class="sxs-lookup"><span data-stu-id="14145-773">175.00</span></span></td>
<td><span data-ttu-id="14145-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-775">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-775">CC003</span></span></td>
<td><span data-ttu-id="14145-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-776">Assembly</span></span></td>
<td><span data-ttu-id="14145-777">10001</span><span class="sxs-lookup"><span data-stu-id="14145-777">10001</span></span></td>
<td><span data-ttu-id="14145-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-778">Electricity</span></span></td>
<td><span data-ttu-id="14145-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-779">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-780">275.00</span><span class="sxs-lookup"><span data-stu-id="14145-780">275.00</span></span></td>
<td><span data-ttu-id="14145-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-782">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-782">CC004</span></span></td>
<td><span data-ttu-id="14145-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-783">Packaging</span></span></td>
<td><span data-ttu-id="14145-784">10001</span><span class="sxs-lookup"><span data-stu-id="14145-784">10001</span></span></td>
<td><span data-ttu-id="14145-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-785">Electricity</span></span></td>
<td><span data-ttu-id="14145-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-786">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-787">50,00</span><span class="sxs-lookup"><span data-stu-id="14145-787">50,00</span></span></td>
<td><span data-ttu-id="14145-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-789">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-789">CC001</span></span></td>
<td><span data-ttu-id="14145-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="14145-790">HR</span></span></td>
<td><span data-ttu-id="14145-791">10001</span><span class="sxs-lookup"><span data-stu-id="14145-791">10001</span></span></td>
<td><span data-ttu-id="14145-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-792">Electricity</span></span></td>
<td><span data-ttu-id="14145-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-793">Variable cost</span></span></td>
<td><span data-ttu-id="14145-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="14145-794">-1,245.71</span></span></td>
<td><span data-ttu-id="14145-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-796">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-796">CC002</span></span></td>
<td><span data-ttu-id="14145-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-797">Finance</span></span></td>
<td><span data-ttu-id="14145-798">10001</span><span class="sxs-lookup"><span data-stu-id="14145-798">10001</span></span></td>
<td><span data-ttu-id="14145-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-799">Electricity</span></span></td>
<td><span data-ttu-id="14145-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-800">Variable cost</span></span></td>
<td><span data-ttu-id="14145-801">436.00</span><span class="sxs-lookup"><span data-stu-id="14145-801">436.00</span></span></td>
<td><span data-ttu-id="14145-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-803">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-803">CC003</span></span></td>
<td><span data-ttu-id="14145-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-804">Assembly</span></span></td>
<td><span data-ttu-id="14145-805">10001</span><span class="sxs-lookup"><span data-stu-id="14145-805">10001</span></span></td>
<td><span data-ttu-id="14145-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-806">Electricity</span></span></td>
<td><span data-ttu-id="14145-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-807">Variable cost</span></span></td>
<td><span data-ttu-id="14145-808">685.14</span><span class="sxs-lookup"><span data-stu-id="14145-808">685.14</span></span></td>
<td><span data-ttu-id="14145-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-810">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-810">CC004</span></span></td>
<td><span data-ttu-id="14145-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-811">Packaging</span></span></td>
<td><span data-ttu-id="14145-812">10001</span><span class="sxs-lookup"><span data-stu-id="14145-812">10001</span></span></td>
<td><span data-ttu-id="14145-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-813">Electricity</span></span></td>
<td><span data-ttu-id="14145-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-814">Variable cost</span></span></td>
<td><span data-ttu-id="14145-815">124.57</span><span class="sxs-lookup"><span data-stu-id="14145-815">124.57</span></span></td>
<td><span data-ttu-id="14145-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-817">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-817">CC002</span></span></td>
<td><span data-ttu-id="14145-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-818">Finance</span></span></td>
<td><span data-ttu-id="14145-819">10001</span><span class="sxs-lookup"><span data-stu-id="14145-819">10001</span></span></td>
<td><span data-ttu-id="14145-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-820">Electricity</span></span></td>
<td><span data-ttu-id="14145-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-821">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="14145-822">-675.00</span></span></td>
<td><span data-ttu-id="14145-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-824">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-824">CC003</span></span></td>
<td><span data-ttu-id="14145-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-825">Assembly</span></span></td>
<td><span data-ttu-id="14145-826">10001</span><span class="sxs-lookup"><span data-stu-id="14145-826">10001</span></span></td>
<td><span data-ttu-id="14145-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-827">Electricity</span></span></td>
<td><span data-ttu-id="14145-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-828">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-829">438.75</span><span class="sxs-lookup"><span data-stu-id="14145-829">438.75</span></span></td>
<td><span data-ttu-id="14145-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-831">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-831">CC004</span></span></td>
<td><span data-ttu-id="14145-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-832">Packaging</span></span></td>
<td><span data-ttu-id="14145-833">10001</span><span class="sxs-lookup"><span data-stu-id="14145-833">10001</span></span></td>
<td><span data-ttu-id="14145-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-834">Electricity</span></span></td>
<td><span data-ttu-id="14145-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-835">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-836">236.25</span><span class="sxs-lookup"><span data-stu-id="14145-836">236.25</span></span></td>
<td><span data-ttu-id="14145-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-838">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-838">CC002</span></span></td>
<td><span data-ttu-id="14145-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="14145-839">Finance</span></span></td>
<td><span data-ttu-id="14145-840">10001</span><span class="sxs-lookup"><span data-stu-id="14145-840">10001</span></span></td>
<td><span data-ttu-id="14145-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-841">Electricity</span></span></td>
<td><span data-ttu-id="14145-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-842">Variable cost</span></span></td>
<td><span data-ttu-id="14145-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="14145-843">-8,150.29</span></span></td>
<td><span data-ttu-id="14145-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-845">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-845">CC003</span></span></td>
<td><span data-ttu-id="14145-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-846">Assembly</span></span></td>
<td><span data-ttu-id="14145-847">10001</span><span class="sxs-lookup"><span data-stu-id="14145-847">10001</span></span></td>
<td><span data-ttu-id="14145-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-848">Electricity</span></span></td>
<td><span data-ttu-id="14145-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-849">Variable cost</span></span></td>
<td><span data-ttu-id="14145-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="14145-850">5,297.69</span></span></td>
<td><span data-ttu-id="14145-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-852">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-852">CC004</span></span></td>
<td><span data-ttu-id="14145-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="14145-853">Packaging</span></span></td>
<td><span data-ttu-id="14145-854">10001</span><span class="sxs-lookup"><span data-stu-id="14145-854">10001</span></span></td>
<td><span data-ttu-id="14145-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-855">Electricity</span></span></td>
<td><span data-ttu-id="14145-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-856">Variable cost</span></span></td>
<td><span data-ttu-id="14145-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="14145-857">2,852.60</span></span></td>
<td><span data-ttu-id="14145-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-859">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-859">CC003</span></span></td>
<td><span data-ttu-id="14145-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-860">Assembly</span></span></td>
<td><span data-ttu-id="14145-861">10001</span><span class="sxs-lookup"><span data-stu-id="14145-861">10001</span></span></td>
<td><span data-ttu-id="14145-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-862">Electricity</span></span></td>
<td><span data-ttu-id="14145-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-863">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="14145-864">-713.75</span></span></td>
<td><span data-ttu-id="14145-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-866">Prod 1</span></span></td>
<td><span data-ttu-id="14145-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-867">Product 1</span></span></td>
<td><span data-ttu-id="14145-868">10001</span><span class="sxs-lookup"><span data-stu-id="14145-868">10001</span></span></td>
<td><span data-ttu-id="14145-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-869">Electricity</span></span></td>
<td><span data-ttu-id="14145-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-870">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-871">535.31</span><span class="sxs-lookup"><span data-stu-id="14145-871">535.31</span></span></td>
<td><span data-ttu-id="14145-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-873">Prod 2</span></span></td>
<td><span data-ttu-id="14145-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-874">Product 2</span></span></td>
<td><span data-ttu-id="14145-875">10001</span><span class="sxs-lookup"><span data-stu-id="14145-875">10001</span></span></td>
<td><span data-ttu-id="14145-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-876">Electricity</span></span></td>
<td><span data-ttu-id="14145-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-877">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-878">178.44</span><span class="sxs-lookup"><span data-stu-id="14145-878">178.44</span></span></td>
<td><span data-ttu-id="14145-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-880">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-880">CC003</span></span></td>
<td><span data-ttu-id="14145-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-881">Assembly</span></span></td>
<td><span data-ttu-id="14145-882">10001</span><span class="sxs-lookup"><span data-stu-id="14145-882">10001</span></span></td>
<td><span data-ttu-id="14145-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-883">Electricity</span></span></td>
<td><span data-ttu-id="14145-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-884">Variable cost</span></span></td>
<td><span data-ttu-id="14145-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="14145-885">-5,982.83</span></span></td>
<td><span data-ttu-id="14145-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-887">Prod 1</span></span></td>
<td><span data-ttu-id="14145-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-888">Product 1</span></span></td>
<td><span data-ttu-id="14145-889">10001</span><span class="sxs-lookup"><span data-stu-id="14145-889">10001</span></span></td>
<td><span data-ttu-id="14145-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-890">Electricity</span></span></td>
<td><span data-ttu-id="14145-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-891">Variable cost</span></span></td>
<td><span data-ttu-id="14145-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="14145-892">4,487.12</span></span></td>
<td><span data-ttu-id="14145-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-894">Prod 2</span></span></td>
<td><span data-ttu-id="14145-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-895">Product 2</span></span></td>
<td><span data-ttu-id="14145-896">10001</span><span class="sxs-lookup"><span data-stu-id="14145-896">10001</span></span></td>
<td><span data-ttu-id="14145-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-897">Electricity</span></span></td>
<td><span data-ttu-id="14145-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-898">Variable cost</span></span></td>
<td><span data-ttu-id="14145-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="14145-899">1,495.71</span></span></td>
<td><span data-ttu-id="14145-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-901">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-901">CC003</span></span></td>
<td><span data-ttu-id="14145-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-902">Assembly</span></span></td>
<td><span data-ttu-id="14145-903">10001</span><span class="sxs-lookup"><span data-stu-id="14145-903">10001</span></span></td>
<td><span data-ttu-id="14145-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-904">Electricity</span></span></td>
<td><span data-ttu-id="14145-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-905">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="14145-906">-286.25</span></span></td>
<td><span data-ttu-id="14145-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-908">Prod 1</span></span></td>
<td><span data-ttu-id="14145-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-909">Product 1</span></span></td>
<td><span data-ttu-id="14145-910">10001</span><span class="sxs-lookup"><span data-stu-id="14145-910">10001</span></span></td>
<td><span data-ttu-id="14145-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-911">Electricity</span></span></td>
<td><span data-ttu-id="14145-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-912">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-913">241.05</span><span class="sxs-lookup"><span data-stu-id="14145-913">241.05</span></span></td>
<td><span data-ttu-id="14145-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-915">Prod 2</span></span></td>
<td><span data-ttu-id="14145-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-916">Product 2</span></span></td>
<td><span data-ttu-id="14145-917">10001</span><span class="sxs-lookup"><span data-stu-id="14145-917">10001</span></span></td>
<td><span data-ttu-id="14145-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-918">Electricity</span></span></td>
<td><span data-ttu-id="14145-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-919">Fixed cost</span></span></td>
<td><span data-ttu-id="14145-920">45.20</span><span class="sxs-lookup"><span data-stu-id="14145-920">45.20</span></span></td>
<td><span data-ttu-id="14145-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-922">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-922">CC003</span></span></td>
<td><span data-ttu-id="14145-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="14145-923">Assembly</span></span></td>
<td><span data-ttu-id="14145-924">10001</span><span class="sxs-lookup"><span data-stu-id="14145-924">10001</span></span></td>
<td><span data-ttu-id="14145-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-925">Electricity</span></span></td>
<td><span data-ttu-id="14145-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-926">Variable cost</span></span></td>
<td><span data-ttu-id="14145-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="14145-927">-2,977.17</span></span></td>
<td><span data-ttu-id="14145-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-929">Prod 1</span></span></td>
<td><span data-ttu-id="14145-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="14145-930">Product 1</span></span></td>
<td><span data-ttu-id="14145-931">10001</span><span class="sxs-lookup"><span data-stu-id="14145-931">10001</span></span></td>
<td><span data-ttu-id="14145-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-932">Electricity</span></span></td>
<td><span data-ttu-id="14145-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-933">Variable cost</span></span></td>
<td><span data-ttu-id="14145-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="14145-934">2,507.09</span></span></td>
<td><span data-ttu-id="14145-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14145-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-936">Prod 2</span></span></td>
<td><span data-ttu-id="14145-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="14145-937">Product 2</span></span></td>
<td><span data-ttu-id="14145-938">10001</span><span class="sxs-lookup"><span data-stu-id="14145-938">10001</span></span></td>
<td><span data-ttu-id="14145-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-939">Electricity</span></span></td>
<td><span data-ttu-id="14145-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-940">Variable cost</span></span></td>
<td><span data-ttu-id="14145-941">470.08</span><span class="sxs-lookup"><span data-stu-id="14145-941">470.08</span></span></td>
<td><span data-ttu-id="14145-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="14145-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="14145-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="14145-943">Conclusion</span></span>
<span data-ttu-id="14145-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="14145-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="14145-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="14145-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="14145-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="14145-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="14145-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="14145-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="14145-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="14145-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="14145-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="14145-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="14145-951">CC099</span><span class="sxs-lookup"><span data-stu-id="14145-951">CC099</span></span></th>
<th><span data-ttu-id="14145-952">CC001</span><span class="sxs-lookup"><span data-stu-id="14145-952">CC001</span></span></th>
<th><span data-ttu-id="14145-953">CC002</span><span class="sxs-lookup"><span data-stu-id="14145-953">CC002</span></span></th>
<th><span data-ttu-id="14145-954">CC003</span><span class="sxs-lookup"><span data-stu-id="14145-954">CC003</span></span></th>
<th><span data-ttu-id="14145-955">CC004</span><span class="sxs-lookup"><span data-stu-id="14145-955">CC004</span></span></th>
<th><span data-ttu-id="14145-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="14145-956">Proj 1</span></span></th>
<th><span data-ttu-id="14145-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="14145-957">Proj 2</span></span></th>
<th><span data-ttu-id="14145-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="14145-958">Prod 1</span></span></th>
<th><span data-ttu-id="14145-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="14145-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="14145-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="14145-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="14145-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="14145-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="14145-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="14145-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="14145-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-971">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="14145-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-973">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-974">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-975">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-976">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-977">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="14145-978">776.36</span><span class="sxs-lookup"><span data-stu-id="14145-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-979">223.64</span><span class="sxs-lookup"><span data-stu-id="14145-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="14145-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="14145-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-982">000</span><span class="sxs-lookup"><span data-stu-id="14145-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-983">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-984">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-985">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-986">0,00</span><span class="sxs-lookup"><span data-stu-id="14145-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-987">30.00</span><span class="sxs-lookup"><span data-stu-id="14145-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-988">10,00</span><span class="sxs-lookup"><span data-stu-id="14145-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="14145-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="14145-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="14145-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="14145-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="14145-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="14145-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="14145-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="14145-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="14145-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="14145-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="14145-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="14145-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="14145-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]