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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822911"
---
# <a name="overhead-calculation"></a><span data-ttu-id="37490-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="37490-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37490-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="37490-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="37490-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="37490-105">Term definition</span></span>
---------------

<span data-ttu-id="37490-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="37490-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="37490-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="37490-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="37490-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="37490-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="37490-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="37490-109">Rent</span></span>
-   <span data-ttu-id="37490-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-110">Electricity</span></span>
-   <span data-ttu-id="37490-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="37490-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="37490-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="37490-112">Overhead calculation overview</span></span>
<span data-ttu-id="37490-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="37490-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="37490-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="37490-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="37490-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="37490-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="37490-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="37490-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="37490-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="37490-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="37490-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="37490-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="37490-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="37490-119">Version type</span></span>
-   <span data-ttu-id="37490-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="37490-120">Date and time</span></span>
-   <span data-ttu-id="37490-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="37490-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="37490-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="37490-122">Fiscal year</span></span>
-   <span data-ttu-id="37490-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="37490-123">Fiscal period</span></span>

<span data-ttu-id="37490-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="37490-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="37490-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="37490-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="37490-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="37490-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="37490-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="37490-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="37490-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="37490-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="37490-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="37490-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="37490-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="37490-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="37490-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="37490-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="37490-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="37490-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="37490-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="37490-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="37490-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="37490-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="37490-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="37490-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="37490-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="37490-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="37490-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="37490-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="37490-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="37490-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="37490-140">Main account</span></span></th>
<th><span data-ttu-id="37490-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="37490-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="37490-143">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-143">CC099</span></span></td>
<td><span data-ttu-id="37490-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-144">Default cost center</span></span></td>
<td><span data-ttu-id="37490-145">10001</span><span class="sxs-lookup"><span data-stu-id="37490-145">10001</span></span></td>
<td><span data-ttu-id="37490-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-146">Electricity</span></span></td>
<td><span data-ttu-id="37490-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="37490-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="37490-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="37490-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="37490-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="37490-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="37490-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-151">Define the cost behavior rule</span></span>

<span data-ttu-id="37490-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="37490-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="37490-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="37490-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="37490-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="37490-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="37490-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="37490-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="37490-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="37490-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="37490-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="37490-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="37490-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-160">Journal</span></span></th>
<th><span data-ttu-id="37490-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="37490-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="37490-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="37490-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="37490-163">Версия</span><span class="sxs-lookup"><span data-stu-id="37490-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-164">00001</span><span class="sxs-lookup"><span data-stu-id="37490-164">00001</span></span></td>
<td><span data-ttu-id="37490-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="37490-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="37490-166">Fiscal</span></span></td>
<td><span data-ttu-id="37490-167">2017</span><span class="sxs-lookup"><span data-stu-id="37490-167">2017</span></span></td>
<td><span data-ttu-id="37490-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-168">Period 1</span></span></td>
<td><span data-ttu-id="37490-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="37490-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="37490-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="37490-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-173">Cost element</span></span></th>
<th><span data-ttu-id="37490-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-174">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="37490-177">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-177">CC099</span></span></td>
<td><span data-ttu-id="37490-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-178">Default cost center</span></span></td>
<td><span data-ttu-id="37490-179">10001</span><span class="sxs-lookup"><span data-stu-id="37490-179">10001</span></span></td>
<td><span data-ttu-id="37490-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-180">Electricity</span></span></td>
<td><span data-ttu-id="37490-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="37490-181">Unclassified</span></span></td>
<td><span data-ttu-id="37490-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="37490-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="37490-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="37490-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-185">Cost element</span></span></th>
<th><span data-ttu-id="37490-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-186">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-187">Amount</span></span></th>
<th><span data-ttu-id="37490-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-189">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-189">CC099</span></span></td>
<td><span data-ttu-id="37490-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-190">Default cost center</span></span></td>
<td><span data-ttu-id="37490-191">10001</span><span class="sxs-lookup"><span data-stu-id="37490-191">10001</span></span></td>
<td><span data-ttu-id="37490-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-192">Electricity</span></span></td>
<td><span data-ttu-id="37490-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="37490-193">Unclassified</span></span></td>
<td><span data-ttu-id="37490-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="37490-194">10,000.00</span></span></td>
<td><span data-ttu-id="37490-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-196">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-196">CC099</span></span></td>
<td><span data-ttu-id="37490-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-197">Default cost center</span></span></td>
<td><span data-ttu-id="37490-198">10001</span><span class="sxs-lookup"><span data-stu-id="37490-198">10001</span></span></td>
<td><span data-ttu-id="37490-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-199">Electricity</span></span></td>
<td><span data-ttu-id="37490-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="37490-200">Unclassified</span></span></td>
<td><span data-ttu-id="37490-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="37490-201">-10,000.00</span></span></td>
<td><span data-ttu-id="37490-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-203">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-203">CC099</span></span></td>
<td><span data-ttu-id="37490-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-204">Default cost center</span></span></td>
<td><span data-ttu-id="37490-205">10001</span><span class="sxs-lookup"><span data-stu-id="37490-205">10001</span></span></td>
<td><span data-ttu-id="37490-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-206">Electricity</span></span></td>
<td><span data-ttu-id="37490-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-207">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="37490-208">1,000.00</span></span></td>
<td><span data-ttu-id="37490-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-210">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-210">CC099</span></span></td>
<td><span data-ttu-id="37490-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-211">Default cost center</span></span></td>
<td><span data-ttu-id="37490-212">10001</span><span class="sxs-lookup"><span data-stu-id="37490-212">10001</span></span></td>
<td><span data-ttu-id="37490-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-213">Electricity</span></span></td>
<td><span data-ttu-id="37490-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-214">Variable cost</span></span></td>
<td><span data-ttu-id="37490-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="37490-215">9,000.00</span></span></td>
<td><span data-ttu-id="37490-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="37490-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="37490-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="37490-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="37490-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="37490-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-221">Define the cost distribution rule</span></span>

<span data-ttu-id="37490-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="37490-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="37490-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="37490-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="37490-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="37490-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="37490-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="37490-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="37490-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="37490-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="37490-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-228">Cost object</span></span></th>
<th><span data-ttu-id="37490-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="37490-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-230">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-230">CC001</span></span></td>
<td><span data-ttu-id="37490-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-231">HR</span></span></td>
<td><span data-ttu-id="37490-232">1000</span><span class="sxs-lookup"><span data-stu-id="37490-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-233">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-233">CC002</span></span></td>
<td><span data-ttu-id="37490-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-234">Finance</span></span></td>
<td><span data-ttu-id="37490-235">6,000</span><span class="sxs-lookup"><span data-stu-id="37490-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-236">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-236">CC003</span></span></td>
<td><span data-ttu-id="37490-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-237">Assembly</span></span></td>
<td><span data-ttu-id="37490-238">0</span><span class="sxs-lookup"><span data-stu-id="37490-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-240">Cost object</span></span></th>
<th><span data-ttu-id="37490-241">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-241">Magnitude</span></span></th>
<th><span data-ttu-id="37490-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-242">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-244">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-244">CC001</span></span></td>
<td><span data-ttu-id="37490-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-245">HR</span></span></td>
<td><span data-ttu-id="37490-246">1000</span><span class="sxs-lookup"><span data-stu-id="37490-246">1,000</span></span></td>
<td><span data-ttu-id="37490-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="37490-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="37490-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="37490-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-249">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-249">CC002</span></span></td>
<td><span data-ttu-id="37490-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-250">Finance</span></span></td>
<td><span data-ttu-id="37490-251">6,000</span><span class="sxs-lookup"><span data-stu-id="37490-251">6,000</span></span></td>
<td><span data-ttu-id="37490-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="37490-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="37490-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="37490-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-254">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-254">CC003</span></span></td>
<td><span data-ttu-id="37490-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-255">Assembly</span></span></td>
<td><span data-ttu-id="37490-256">0</span><span class="sxs-lookup"><span data-stu-id="37490-256">0</span></span></td>
<td><span data-ttu-id="37490-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="37490-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="37490-258">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="37490-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="37490-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-261">Cost object</span></span></th>
<th><span data-ttu-id="37490-262">Формула</span><span class="sxs-lookup"><span data-stu-id="37490-262">Formula</span></span></th>
<th><span data-ttu-id="37490-263">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-263">Magnitude</span></span></th>
<th><span data-ttu-id="37490-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-264">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-266">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-266">CC001</span></span></td>
<td><span data-ttu-id="37490-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-267">HR</span></span></td>
<td><span data-ttu-id="37490-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="37490-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="37490-269">1</span><span class="sxs-lookup"><span data-stu-id="37490-269">1</span></span></td>
<td><span data-ttu-id="37490-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="37490-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="37490-271">500.00</span><span class="sxs-lookup"><span data-stu-id="37490-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-272">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-272">CC002</span></span></td>
<td><span data-ttu-id="37490-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-273">Finance</span></span></td>
<td><span data-ttu-id="37490-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="37490-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="37490-275">1</span><span class="sxs-lookup"><span data-stu-id="37490-275">1</span></span></td>
<td><span data-ttu-id="37490-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="37490-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="37490-277">500.00</span><span class="sxs-lookup"><span data-stu-id="37490-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-278">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-278">CC003</span></span></td>
<td><span data-ttu-id="37490-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-279">Assembly</span></span></td>
<td><span data-ttu-id="37490-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="37490-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="37490-281">0</span><span class="sxs-lookup"><span data-stu-id="37490-281">0</span></span></td>
<td><span data-ttu-id="37490-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="37490-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="37490-283">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="37490-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-285">Journal</span></span></th>
<th><span data-ttu-id="37490-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="37490-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="37490-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="37490-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="37490-288">Версия</span><span class="sxs-lookup"><span data-stu-id="37490-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-289">00002</span><span class="sxs-lookup"><span data-stu-id="37490-289">00002</span></span></td>
<td><span data-ttu-id="37490-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="37490-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="37490-291">Fiscal</span></span></td>
<td><span data-ttu-id="37490-292">2017</span><span class="sxs-lookup"><span data-stu-id="37490-292">2017</span></span></td>
<td><span data-ttu-id="37490-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-293">Period 1</span></span></td>
<td><span data-ttu-id="37490-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="37490-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="37490-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="37490-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-298">Cost element</span></span></th>
<th><span data-ttu-id="37490-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-299">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-302">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-302">CC099</span></span></td>
<td><span data-ttu-id="37490-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-303">Default cost center</span></span></td>
<td><span data-ttu-id="37490-304">10001</span><span class="sxs-lookup"><span data-stu-id="37490-304">10001</span></span></td>
<td><span data-ttu-id="37490-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-305">Electricity</span></span></td>
<td><span data-ttu-id="37490-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-306">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="37490-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-309">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-309">CC099</span></span></td>
<td><span data-ttu-id="37490-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-310">Default cost center</span></span></td>
<td><span data-ttu-id="37490-311">10001</span><span class="sxs-lookup"><span data-stu-id="37490-311">10001</span></span></td>
<td><span data-ttu-id="37490-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-312">Electricity</span></span></td>
<td><span data-ttu-id="37490-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-313">Variable cost</span></span></td>
<td><span data-ttu-id="37490-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="37490-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="37490-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="37490-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-317">Cost element</span></span></th>
<th><span data-ttu-id="37490-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-318">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-319">Amount</span></span></th>
<th><span data-ttu-id="37490-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-321">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-321">CC099</span></span></td>
<td><span data-ttu-id="37490-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-322">Default cost center</span></span></td>
<td><span data-ttu-id="37490-323">10001</span><span class="sxs-lookup"><span data-stu-id="37490-323">10001</span></span></td>
<td><span data-ttu-id="37490-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-324">Electricity</span></span></td>
<td><span data-ttu-id="37490-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-325">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="37490-326">-1,000.00</span></span></td>
<td><span data-ttu-id="37490-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-328">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-328">CC001</span></span></td>
<td><span data-ttu-id="37490-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-329">HR</span></span></td>
<td><span data-ttu-id="37490-330">10001</span><span class="sxs-lookup"><span data-stu-id="37490-330">10001</span></span></td>
<td><span data-ttu-id="37490-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-331">Electricity</span></span></td>
<td><span data-ttu-id="37490-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-332">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-333">500.00</span><span class="sxs-lookup"><span data-stu-id="37490-333">500.00</span></span></td>
<td><span data-ttu-id="37490-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-335">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-335">CC002</span></span></td>
<td><span data-ttu-id="37490-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-336">Finance</span></span></td>
<td><span data-ttu-id="37490-337">10001</span><span class="sxs-lookup"><span data-stu-id="37490-337">10001</span></span></td>
<td><span data-ttu-id="37490-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-338">Electricity</span></span></td>
<td><span data-ttu-id="37490-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-339">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-340">500.00</span><span class="sxs-lookup"><span data-stu-id="37490-340">500.00</span></span></td>
<td><span data-ttu-id="37490-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-342">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-342">CC099</span></span></td>
<td><span data-ttu-id="37490-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="37490-343">Default cost center</span></span></td>
<td><span data-ttu-id="37490-344">10001</span><span class="sxs-lookup"><span data-stu-id="37490-344">10001</span></span></td>
<td><span data-ttu-id="37490-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-345">Electricity</span></span></td>
<td><span data-ttu-id="37490-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-346">Variable cost</span></span></td>
<td><span data-ttu-id="37490-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="37490-347">-9,000.00</span></span></td>
<td><span data-ttu-id="37490-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-349">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-349">CC001</span></span></td>
<td><span data-ttu-id="37490-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-350">HR</span></span></td>
<td><span data-ttu-id="37490-351">10001</span><span class="sxs-lookup"><span data-stu-id="37490-351">10001</span></span></td>
<td><span data-ttu-id="37490-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-352">Electricity</span></span></td>
<td><span data-ttu-id="37490-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-353">Variable cost</span></span></td>
<td><span data-ttu-id="37490-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="37490-354">1,285.71</span></span></td>
<td><span data-ttu-id="37490-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-356">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-356">CC002</span></span></td>
<td><span data-ttu-id="37490-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-357">Finance</span></span></td>
<td><span data-ttu-id="37490-358">10001</span><span class="sxs-lookup"><span data-stu-id="37490-358">10001</span></span></td>
<td><span data-ttu-id="37490-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-359">Electricity</span></span></td>
<td><span data-ttu-id="37490-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-360">Variable cost</span></span></td>
<td><span data-ttu-id="37490-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="37490-361">7,714.29</span></span></td>
<td><span data-ttu-id="37490-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="37490-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="37490-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="37490-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="37490-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="37490-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="37490-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="37490-367">Define the overhead rate</span></span>

<span data-ttu-id="37490-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="37490-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="37490-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="37490-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-370">Cost object</span></span></th>
<th><span data-ttu-id="37490-371">Часы</span><span class="sxs-lookup"><span data-stu-id="37490-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-372">Proj 1</span></span></td>
<td><span data-ttu-id="37490-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-373">Project 1</span></span></td>
<td><span data-ttu-id="37490-374">3</span><span class="sxs-lookup"><span data-stu-id="37490-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-375">Proj 2</span></span></td>
<td><span data-ttu-id="37490-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-376">Project 2</span></span></td>
<td><span data-ttu-id="37490-377">1</span><span class="sxs-lookup"><span data-stu-id="37490-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-379">Cost object</span></span></th>
<th><span data-ttu-id="37490-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-380">Cost element</span></span></th>
<th><span data-ttu-id="37490-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-381">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="37490-382">Units</span></span></th>
<th><span data-ttu-id="37490-383">По норме</span><span class="sxs-lookup"><span data-stu-id="37490-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-384">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-384">CC001</span></span></td>
<td><span data-ttu-id="37490-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-385">HR</span></span></td>
<td><span data-ttu-id="37490-386">10001</span><span class="sxs-lookup"><span data-stu-id="37490-386">10001</span></span></td>
<td><span data-ttu-id="37490-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-387">Variable cost</span></span></td>
<td><span data-ttu-id="37490-388">1</span><span class="sxs-lookup"><span data-stu-id="37490-388">1</span></span></td>
<td><span data-ttu-id="37490-389">10</span><span class="sxs-lookup"><span data-stu-id="37490-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-391">Cost object</span></span></th>
<th><span data-ttu-id="37490-392">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-392">Magnitude</span></span></th>
<th><span data-ttu-id="37490-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-393">Cost element</span></span></th>
<th><span data-ttu-id="37490-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-394">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-396">Proj 1</span></span></td>
<td><span data-ttu-id="37490-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-397">Project 1</span></span></td>
<td><span data-ttu-id="37490-398">3</span><span class="sxs-lookup"><span data-stu-id="37490-398">3</span></span></td>
<td><span data-ttu-id="37490-399">10001</span><span class="sxs-lookup"><span data-stu-id="37490-399">10001</span></span></td>
<td><span data-ttu-id="37490-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="37490-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="37490-401">30.00</span><span class="sxs-lookup"><span data-stu-id="37490-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-402">Proj 2</span></span></td>
<td><span data-ttu-id="37490-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-403">Project 2</span></span></td>
<td><span data-ttu-id="37490-404">1</span><span class="sxs-lookup"><span data-stu-id="37490-404">1</span></span></td>
<td><span data-ttu-id="37490-405">10001</span><span class="sxs-lookup"><span data-stu-id="37490-405">10001</span></span></td>
<td><span data-ttu-id="37490-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="37490-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="37490-407">10,00</span><span class="sxs-lookup"><span data-stu-id="37490-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="37490-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-409">Journal</span></span></th>
<th><span data-ttu-id="37490-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="37490-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="37490-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="37490-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="37490-412">Версия</span><span class="sxs-lookup"><span data-stu-id="37490-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-413">00003</span><span class="sxs-lookup"><span data-stu-id="37490-413">00003</span></span></td>
<td><span data-ttu-id="37490-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="37490-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="37490-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="37490-415">Fiscal</span></span></td>
<td><span data-ttu-id="37490-416">2017</span><span class="sxs-lookup"><span data-stu-id="37490-416">2017</span></span></td>
<td><span data-ttu-id="37490-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-417">Period 1</span></span></td>
<td><span data-ttu-id="37490-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="37490-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="37490-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="37490-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-421">Cost object</span></span></th>
<th><span data-ttu-id="37490-422">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-424">Proj 1</span></span></td>
<td><span data-ttu-id="37490-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="37490-426">3,00</span><span class="sxs-lookup"><span data-stu-id="37490-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-428">Proj 2</span></span></td>
<td><span data-ttu-id="37490-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="37490-430">1.00</span><span class="sxs-lookup"><span data-stu-id="37490-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="37490-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="37490-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-433">Cost element</span></span></th>
<th><span data-ttu-id="37490-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-434">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-435">Amount</span></span></th>
<th><span data-ttu-id="37490-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="37490-437">CC0001</span></span></td>
<td><span data-ttu-id="37490-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-438">HR</span></span></td>
<td><span data-ttu-id="37490-439">10001</span><span class="sxs-lookup"><span data-stu-id="37490-439">10001</span></span></td>
<td><span data-ttu-id="37490-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-440">Electricity</span></span></td>
<td><span data-ttu-id="37490-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-441">Variable cost</span></span></td>
<td><span data-ttu-id="37490-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="37490-442">-30.00</span></span></td>
<td><span data-ttu-id="37490-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-444">Proj 1</span></span></td>
<td><span data-ttu-id="37490-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="37490-446">10001</span><span class="sxs-lookup"><span data-stu-id="37490-446">10001</span></span></td>
<td><span data-ttu-id="37490-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-447">Electricity</span></span></td>
<td><span data-ttu-id="37490-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-448">Variable cost</span></span></td>
<td><span data-ttu-id="37490-449">30.00</span><span class="sxs-lookup"><span data-stu-id="37490-449">30.00</span></span></td>
<td><span data-ttu-id="37490-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-451">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-451">CC001</span></span></td>
<td><span data-ttu-id="37490-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-452">HR</span></span></td>
<td><span data-ttu-id="37490-453">10001</span><span class="sxs-lookup"><span data-stu-id="37490-453">10001</span></span></td>
<td><span data-ttu-id="37490-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-454">Electricity</span></span></td>
<td><span data-ttu-id="37490-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-455">Variable cost</span></span></td>
<td><span data-ttu-id="37490-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="37490-456">-10.00</span></span></td>
<td><span data-ttu-id="37490-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-458">Proj 2</span></span></td>
<td><span data-ttu-id="37490-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="37490-460">10001</span><span class="sxs-lookup"><span data-stu-id="37490-460">10001</span></span></td>
<td><span data-ttu-id="37490-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-461">Electricity</span></span></td>
<td><span data-ttu-id="37490-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-462">Variable cost</span></span></td>
<td><span data-ttu-id="37490-463">10.00</span><span class="sxs-lookup"><span data-stu-id="37490-463">10.00</span></span></td>
<td><span data-ttu-id="37490-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="37490-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="37490-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="37490-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="37490-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="37490-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="37490-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="37490-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="37490-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="37490-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="37490-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="37490-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="37490-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="37490-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="37490-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="37490-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="37490-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="37490-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-475">Define the cost allocation</span></span>

<span data-ttu-id="37490-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="37490-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="37490-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="37490-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-479">Cost object</span></span></th>
<th><span data-ttu-id="37490-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="37490-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-481">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-481">CC002</span></span></td>
<td><span data-ttu-id="37490-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-482">Finance</span></span></td>
<td><span data-ttu-id="37490-483">35</span><span class="sxs-lookup"><span data-stu-id="37490-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-484">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-484">CC003</span></span></td>
<td><span data-ttu-id="37490-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-485">Assembly</span></span></td>
<td><span data-ttu-id="37490-486">55</span><span class="sxs-lookup"><span data-stu-id="37490-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-487">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-487">CC004</span></span></td>
<td><span data-ttu-id="37490-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-488">Packaging</span></span></td>
<td><span data-ttu-id="37490-489">10</span><span class="sxs-lookup"><span data-stu-id="37490-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="37490-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="37490-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-492">Cost object</span></span></th>
<th><span data-ttu-id="37490-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="37490-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-494">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-494">CC003</span></span></td>
<td><span data-ttu-id="37490-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-495">Assembly</span></span></td>
<td><span data-ttu-id="37490-496">65</span><span class="sxs-lookup"><span data-stu-id="37490-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-497">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-497">CC004</span></span></td>
<td><span data-ttu-id="37490-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-498">Packaging</span></span></td>
<td><span data-ttu-id="37490-499">35</span><span class="sxs-lookup"><span data-stu-id="37490-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="37490-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="37490-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-502">Cost object</span></span></th>
<th><span data-ttu-id="37490-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="37490-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-504">Prod 1</span></span></td>
<td><span data-ttu-id="37490-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-505">Product 1</span></span></td>
<td><span data-ttu-id="37490-506">60</span><span class="sxs-lookup"><span data-stu-id="37490-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-507">Prod 2</span></span></td>
<td><span data-ttu-id="37490-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-508">Product 2</span></span></td>
<td><span data-ttu-id="37490-509">20</span><span class="sxs-lookup"><span data-stu-id="37490-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="37490-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="37490-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-512">Cost object</span></span></th>
<th><span data-ttu-id="37490-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="37490-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-514">Prod 1</span></span></td>
<td><span data-ttu-id="37490-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-515">Product 1</span></span></td>
<td><span data-ttu-id="37490-516">80</span><span class="sxs-lookup"><span data-stu-id="37490-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-517">Prod 2</span></span></td>
<td><span data-ttu-id="37490-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-518">Product 2</span></span></td>
<td><span data-ttu-id="37490-519">15</span><span class="sxs-lookup"><span data-stu-id="37490-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="37490-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="37490-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="37490-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="37490-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="37490-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="37490-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-523">Cost object</span></span></th>
<th><span data-ttu-id="37490-524">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-524">Magnitude</span></span></th>
<th><span data-ttu-id="37490-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-525">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-526">Amount</span></span></th>
<th><span data-ttu-id="37490-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-528">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-528">CC002</span></span></td>
<td><span data-ttu-id="37490-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-529">Finance</span></span></td>
<td><span data-ttu-id="37490-530">35</span><span class="sxs-lookup"><span data-stu-id="37490-530">35</span></span></td>
<td><span data-ttu-id="37490-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="37490-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="37490-532">175.00</span><span class="sxs-lookup"><span data-stu-id="37490-532">175.00</span></span></td>
<td><span data-ttu-id="37490-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-534">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-534">CC003</span></span></td>
<td><span data-ttu-id="37490-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-535">Assembly</span></span></td>
<td><span data-ttu-id="37490-536">55</span><span class="sxs-lookup"><span data-stu-id="37490-536">55</span></span></td>
<td><span data-ttu-id="37490-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="37490-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="37490-538">275.00</span><span class="sxs-lookup"><span data-stu-id="37490-538">275.00</span></span></td>
<td><span data-ttu-id="37490-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-540">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-540">CC004</span></span></td>
<td><span data-ttu-id="37490-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-541">Packaging</span></span></td>
<td><span data-ttu-id="37490-542">10</span><span class="sxs-lookup"><span data-stu-id="37490-542">10</span></span></td>
<td><span data-ttu-id="37490-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="37490-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="37490-544">50,00</span><span class="sxs-lookup"><span data-stu-id="37490-544">50.00</span></span></td>
<td><span data-ttu-id="37490-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-546">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-546">CC002</span></span></td>
<td><span data-ttu-id="37490-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-547">Finance</span></span></td>
<td><span data-ttu-id="37490-548">35</span><span class="sxs-lookup"><span data-stu-id="37490-548">35</span></span></td>
<td><span data-ttu-id="37490-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="37490-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="37490-550">436.00</span><span class="sxs-lookup"><span data-stu-id="37490-550">436.00</span></span></td>
<td><span data-ttu-id="37490-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-552">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-552">CC003</span></span></td>
<td><span data-ttu-id="37490-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-553">Assembly</span></span></td>
<td><span data-ttu-id="37490-554">55</span><span class="sxs-lookup"><span data-stu-id="37490-554">55</span></span></td>
<td><span data-ttu-id="37490-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="37490-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="37490-556">685.14</span><span class="sxs-lookup"><span data-stu-id="37490-556">685.14</span></span></td>
<td><span data-ttu-id="37490-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-558">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-558">CC004</span></span></td>
<td><span data-ttu-id="37490-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-559">Packaging</span></span></td>
<td><span data-ttu-id="37490-560">10</span><span class="sxs-lookup"><span data-stu-id="37490-560">10</span></span></td>
<td><span data-ttu-id="37490-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="37490-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="37490-562">124.57</span><span class="sxs-lookup"><span data-stu-id="37490-562">124.57</span></span></td>
<td><span data-ttu-id="37490-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="37490-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-565">Cost object</span></span></th>
<th><span data-ttu-id="37490-566">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-566">Magnitude</span></span></th>
<th><span data-ttu-id="37490-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-567">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-568">Amount</span></span></th>
<th><span data-ttu-id="37490-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-570">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-570">CC003</span></span></td>
<td><span data-ttu-id="37490-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-571">Assembly</span></span></td>
<td><span data-ttu-id="37490-572">65</span><span class="sxs-lookup"><span data-stu-id="37490-572">65</span></span></td>
<td><span data-ttu-id="37490-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="37490-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="37490-574">438.75</span><span class="sxs-lookup"><span data-stu-id="37490-574">438.75</span></span></td>
<td><span data-ttu-id="37490-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-576">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-576">CC004</span></span></td>
<td><span data-ttu-id="37490-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-577">Packaging</span></span></td>
<td><span data-ttu-id="37490-578">35</span><span class="sxs-lookup"><span data-stu-id="37490-578">35</span></span></td>
<td><span data-ttu-id="37490-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="37490-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="37490-580">236.25</span><span class="sxs-lookup"><span data-stu-id="37490-580">236.25</span></span></td>
<td><span data-ttu-id="37490-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-582">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-582">CC003</span></span></td>
<td><span data-ttu-id="37490-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-583">Assembly</span></span></td>
<td><span data-ttu-id="37490-584">65</span><span class="sxs-lookup"><span data-stu-id="37490-584">65</span></span></td>
<td><span data-ttu-id="37490-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="37490-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="37490-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="37490-586">5,297.69</span></span></td>
<td><span data-ttu-id="37490-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-588">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-588">CC004</span></span></td>
<td><span data-ttu-id="37490-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-589">Packaging</span></span></td>
<td><span data-ttu-id="37490-590">35</span><span class="sxs-lookup"><span data-stu-id="37490-590">35</span></span></td>
<td><span data-ttu-id="37490-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="37490-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="37490-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="37490-592">2,852.60</span></span></td>
<td><span data-ttu-id="37490-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="37490-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-595">Cost object</span></span></th>
<th><span data-ttu-id="37490-596">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-596">Magnitude</span></span></th>
<th><span data-ttu-id="37490-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-597">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-598">Amount</span></span></th>
<th><span data-ttu-id="37490-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-600">Prod 1</span></span></td>
<td><span data-ttu-id="37490-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-601">Product 1</span></span></td>
<td><span data-ttu-id="37490-602">60</span><span class="sxs-lookup"><span data-stu-id="37490-602">60</span></span></td>
<td><span data-ttu-id="37490-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="37490-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="37490-604">535.31</span><span class="sxs-lookup"><span data-stu-id="37490-604">535.31</span></span></td>
<td><span data-ttu-id="37490-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-606">Prod 2</span></span></td>
<td><span data-ttu-id="37490-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-607">Product 2</span></span></td>
<td><span data-ttu-id="37490-608">20</span><span class="sxs-lookup"><span data-stu-id="37490-608">20</span></span></td>
<td><span data-ttu-id="37490-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="37490-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="37490-610">178.44</span><span class="sxs-lookup"><span data-stu-id="37490-610">178.44</span></span></td>
<td><span data-ttu-id="37490-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-612">Prod 1</span></span></td>
<td><span data-ttu-id="37490-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-613">Product 1</span></span></td>
<td><span data-ttu-id="37490-614">60</span><span class="sxs-lookup"><span data-stu-id="37490-614">60</span></span></td>
<td><span data-ttu-id="37490-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="37490-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="37490-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="37490-616">4,487.12</span></span></td>
<td><span data-ttu-id="37490-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-618">Prod 2</span></span></td>
<td><span data-ttu-id="37490-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-619">Product 2</span></span></td>
<td><span data-ttu-id="37490-620">20</span><span class="sxs-lookup"><span data-stu-id="37490-620">20</span></span></td>
<td><span data-ttu-id="37490-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="37490-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="37490-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="37490-622">1,495.71</span></span></td>
<td><span data-ttu-id="37490-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37490-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="37490-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-625">Cost object</span></span></th>
<th><span data-ttu-id="37490-626">Величина</span><span class="sxs-lookup"><span data-stu-id="37490-626">Magnitude</span></span></th>
<th><span data-ttu-id="37490-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="37490-627">Allocation factor</span></span></th>
<th><span data-ttu-id="37490-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-628">Amount</span></span></th>
<th><span data-ttu-id="37490-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-630">Prod 1</span></span></td>
<td><span data-ttu-id="37490-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-631">Product 1</span></span></td>
<td><span data-ttu-id="37490-632">80</span><span class="sxs-lookup"><span data-stu-id="37490-632">80</span></span></td>
<td><span data-ttu-id="37490-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="37490-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="37490-634">241.05</span><span class="sxs-lookup"><span data-stu-id="37490-634">241.05</span></span></td>
<td><span data-ttu-id="37490-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-636">Prod 2</span></span></td>
<td><span data-ttu-id="37490-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-637">Product 2</span></span></td>
<td><span data-ttu-id="37490-638">15</span><span class="sxs-lookup"><span data-stu-id="37490-638">15</span></span></td>
<td><span data-ttu-id="37490-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="37490-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="37490-640">45.20</span><span class="sxs-lookup"><span data-stu-id="37490-640">45.20</span></span></td>
<td><span data-ttu-id="37490-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-642">Prod 1</span></span></td>
<td><span data-ttu-id="37490-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-643">Product 1</span></span></td>
<td><span data-ttu-id="37490-644">80</span><span class="sxs-lookup"><span data-stu-id="37490-644">80</span></span></td>
<td><span data-ttu-id="37490-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="37490-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="37490-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="37490-646">2,507.09</span></span></td>
<td><span data-ttu-id="37490-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-648">Prod 2</span></span></td>
<td><span data-ttu-id="37490-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-649">Product 2</span></span></td>
<td><span data-ttu-id="37490-650">15</span><span class="sxs-lookup"><span data-stu-id="37490-650">15</span></span></td>
<td><span data-ttu-id="37490-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="37490-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="37490-652">470.08</span><span class="sxs-lookup"><span data-stu-id="37490-652">470.08</span></span></td>
<td><span data-ttu-id="37490-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="37490-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="37490-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="37490-655">Journal</span></span></th>
<th><span data-ttu-id="37490-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="37490-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="37490-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="37490-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="37490-658">Версия</span><span class="sxs-lookup"><span data-stu-id="37490-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-659">00004</span><span class="sxs-lookup"><span data-stu-id="37490-659">00004</span></span></td>
<td><span data-ttu-id="37490-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="37490-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="37490-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="37490-661">Fiscal</span></span></td>
<td><span data-ttu-id="37490-662">2017</span><span class="sxs-lookup"><span data-stu-id="37490-662">2017</span></span></td>
<td><span data-ttu-id="37490-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-663">Period 1</span></span></td>
<td><span data-ttu-id="37490-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="37490-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="37490-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="37490-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37490-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="37490-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-668">Cost element</span></span></th>
<th><span data-ttu-id="37490-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-669">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-672">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-672">CC001</span></span></td>
<td><span data-ttu-id="37490-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-673">HR</span></span></td>
<td><span data-ttu-id="37490-674">10001</span><span class="sxs-lookup"><span data-stu-id="37490-674">10001</span></span></td>
<td><span data-ttu-id="37490-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-675">Electricity</span></span></td>
<td><span data-ttu-id="37490-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-676">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-677">500.00</span><span class="sxs-lookup"><span data-stu-id="37490-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-679">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-679">CC001</span></span></td>
<td><span data-ttu-id="37490-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-680">HR</span></span></td>
<td><span data-ttu-id="37490-681">10001</span><span class="sxs-lookup"><span data-stu-id="37490-681">10001</span></span></td>
<td><span data-ttu-id="37490-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-682">Electricity</span></span></td>
<td><span data-ttu-id="37490-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-683">Variable cost</span></span></td>
<td><span data-ttu-id="37490-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="37490-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-686">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-686">CC002</span></span></td>
<td><span data-ttu-id="37490-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-687">Finance</span></span></td>
<td><span data-ttu-id="37490-688">10001</span><span class="sxs-lookup"><span data-stu-id="37490-688">10001</span></span></td>
<td><span data-ttu-id="37490-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-689">Electricity</span></span></td>
<td><span data-ttu-id="37490-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-690">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-691">675.00</span><span class="sxs-lookup"><span data-stu-id="37490-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-693">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-693">CC002</span></span></td>
<td><span data-ttu-id="37490-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-694">Finance</span></span></td>
<td><span data-ttu-id="37490-695">10001</span><span class="sxs-lookup"><span data-stu-id="37490-695">10001</span></span></td>
<td><span data-ttu-id="37490-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-696">Electricity</span></span></td>
<td><span data-ttu-id="37490-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-697">Variable cost</span></span></td>
<td><span data-ttu-id="37490-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="37490-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-700">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-700">CC003</span></span></td>
<td><span data-ttu-id="37490-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-701">Assembly</span></span></td>
<td><span data-ttu-id="37490-702">10001</span><span class="sxs-lookup"><span data-stu-id="37490-702">10001</span></span></td>
<td><span data-ttu-id="37490-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-703">Electricity</span></span></td>
<td><span data-ttu-id="37490-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-704">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-705">713.75</span><span class="sxs-lookup"><span data-stu-id="37490-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-707">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-707">CC003</span></span></td>
<td><span data-ttu-id="37490-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-708">Assembly</span></span></td>
<td><span data-ttu-id="37490-709">10001</span><span class="sxs-lookup"><span data-stu-id="37490-709">10001</span></span></td>
<td><span data-ttu-id="37490-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-710">Electricity</span></span></td>
<td><span data-ttu-id="37490-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-711">Variable cost</span></span></td>
<td><span data-ttu-id="37490-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="37490-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-714">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-714">CC003</span></span></td>
<td><span data-ttu-id="37490-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-715">Packaging</span></span></td>
<td><span data-ttu-id="37490-716">10001</span><span class="sxs-lookup"><span data-stu-id="37490-716">10001</span></span></td>
<td><span data-ttu-id="37490-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-717">Electricity</span></span></td>
<td><span data-ttu-id="37490-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-718">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-719">286.25</span><span class="sxs-lookup"><span data-stu-id="37490-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-721">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-721">CC003</span></span></td>
<td><span data-ttu-id="37490-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-722">Packaging</span></span></td>
<td><span data-ttu-id="37490-723">10001</span><span class="sxs-lookup"><span data-stu-id="37490-723">10001</span></span></td>
<td><span data-ttu-id="37490-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-724">Electricity</span></span></td>
<td><span data-ttu-id="37490-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-725">Variable cost</span></span></td>
<td><span data-ttu-id="37490-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="37490-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-728">Prod 1</span></span></td>
<td><span data-ttu-id="37490-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-729">Product 1</span></span></td>
<td><span data-ttu-id="37490-730">10001</span><span class="sxs-lookup"><span data-stu-id="37490-730">10001</span></span></td>
<td><span data-ttu-id="37490-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-731">Electricity</span></span></td>
<td><span data-ttu-id="37490-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-732">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-733">776.36</span><span class="sxs-lookup"><span data-stu-id="37490-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-735">Prod 1</span></span></td>
<td><span data-ttu-id="37490-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-736">Product 1</span></span></td>
<td><span data-ttu-id="37490-737">10001</span><span class="sxs-lookup"><span data-stu-id="37490-737">10001</span></span></td>
<td><span data-ttu-id="37490-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-738">Electricity</span></span></td>
<td><span data-ttu-id="37490-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-739">Variable cost</span></span></td>
<td><span data-ttu-id="37490-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="37490-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-742">Prod 2</span></span></td>
<td><span data-ttu-id="37490-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-743">Product 1</span></span></td>
<td><span data-ttu-id="37490-744">10001</span><span class="sxs-lookup"><span data-stu-id="37490-744">10001</span></span></td>
<td><span data-ttu-id="37490-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-745">Electricity</span></span></td>
<td><span data-ttu-id="37490-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-746">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-747">223.64</span><span class="sxs-lookup"><span data-stu-id="37490-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="37490-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-749">Prod 2</span></span></td>
<td><span data-ttu-id="37490-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-750">Product 1</span></span></td>
<td><span data-ttu-id="37490-751">10001</span><span class="sxs-lookup"><span data-stu-id="37490-751">10001</span></span></td>
<td><span data-ttu-id="37490-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-752">Electricity</span></span></td>
<td><span data-ttu-id="37490-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-753">Variable cost</span></span></td>
<td><span data-ttu-id="37490-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="37490-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="37490-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="37490-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="37490-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="37490-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-757">Cost element</span></span></th>
<th><span data-ttu-id="37490-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="37490-758">Cost behavior</span></span></th>
<th><span data-ttu-id="37490-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="37490-759">Amount</span></span></th>
<th><span data-ttu-id="37490-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="37490-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37490-761">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-761">CC001</span></span></td>
<td><span data-ttu-id="37490-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-762">HR</span></span></td>
<td><span data-ttu-id="37490-763">10001</span><span class="sxs-lookup"><span data-stu-id="37490-763">10001</span></span></td>
<td><span data-ttu-id="37490-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-764">Electricity</span></span></td>
<td><span data-ttu-id="37490-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-765">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="37490-766">-500.00</span></span></td>
<td><span data-ttu-id="37490-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-768">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-768">CC002</span></span></td>
<td><span data-ttu-id="37490-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-769">Finance</span></span></td>
<td><span data-ttu-id="37490-770">10001</span><span class="sxs-lookup"><span data-stu-id="37490-770">10001</span></span></td>
<td><span data-ttu-id="37490-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-771">Electricity</span></span></td>
<td><span data-ttu-id="37490-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-772">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-773">175.00</span><span class="sxs-lookup"><span data-stu-id="37490-773">175.00</span></span></td>
<td><span data-ttu-id="37490-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-775">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-775">CC003</span></span></td>
<td><span data-ttu-id="37490-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-776">Assembly</span></span></td>
<td><span data-ttu-id="37490-777">10001</span><span class="sxs-lookup"><span data-stu-id="37490-777">10001</span></span></td>
<td><span data-ttu-id="37490-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-778">Electricity</span></span></td>
<td><span data-ttu-id="37490-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-779">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-780">275.00</span><span class="sxs-lookup"><span data-stu-id="37490-780">275.00</span></span></td>
<td><span data-ttu-id="37490-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-782">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-782">CC004</span></span></td>
<td><span data-ttu-id="37490-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-783">Packaging</span></span></td>
<td><span data-ttu-id="37490-784">10001</span><span class="sxs-lookup"><span data-stu-id="37490-784">10001</span></span></td>
<td><span data-ttu-id="37490-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-785">Electricity</span></span></td>
<td><span data-ttu-id="37490-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-786">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-787">50,00</span><span class="sxs-lookup"><span data-stu-id="37490-787">50,00</span></span></td>
<td><span data-ttu-id="37490-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-789">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-789">CC001</span></span></td>
<td><span data-ttu-id="37490-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="37490-790">HR</span></span></td>
<td><span data-ttu-id="37490-791">10001</span><span class="sxs-lookup"><span data-stu-id="37490-791">10001</span></span></td>
<td><span data-ttu-id="37490-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-792">Electricity</span></span></td>
<td><span data-ttu-id="37490-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-793">Variable cost</span></span></td>
<td><span data-ttu-id="37490-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="37490-794">-1,245.71</span></span></td>
<td><span data-ttu-id="37490-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-796">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-796">CC002</span></span></td>
<td><span data-ttu-id="37490-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-797">Finance</span></span></td>
<td><span data-ttu-id="37490-798">10001</span><span class="sxs-lookup"><span data-stu-id="37490-798">10001</span></span></td>
<td><span data-ttu-id="37490-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-799">Electricity</span></span></td>
<td><span data-ttu-id="37490-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-800">Variable cost</span></span></td>
<td><span data-ttu-id="37490-801">436.00</span><span class="sxs-lookup"><span data-stu-id="37490-801">436.00</span></span></td>
<td><span data-ttu-id="37490-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-803">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-803">CC003</span></span></td>
<td><span data-ttu-id="37490-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-804">Assembly</span></span></td>
<td><span data-ttu-id="37490-805">10001</span><span class="sxs-lookup"><span data-stu-id="37490-805">10001</span></span></td>
<td><span data-ttu-id="37490-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-806">Electricity</span></span></td>
<td><span data-ttu-id="37490-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-807">Variable cost</span></span></td>
<td><span data-ttu-id="37490-808">685.14</span><span class="sxs-lookup"><span data-stu-id="37490-808">685.14</span></span></td>
<td><span data-ttu-id="37490-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-810">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-810">CC004</span></span></td>
<td><span data-ttu-id="37490-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-811">Packaging</span></span></td>
<td><span data-ttu-id="37490-812">10001</span><span class="sxs-lookup"><span data-stu-id="37490-812">10001</span></span></td>
<td><span data-ttu-id="37490-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-813">Electricity</span></span></td>
<td><span data-ttu-id="37490-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-814">Variable cost</span></span></td>
<td><span data-ttu-id="37490-815">124.57</span><span class="sxs-lookup"><span data-stu-id="37490-815">124.57</span></span></td>
<td><span data-ttu-id="37490-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-817">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-817">CC002</span></span></td>
<td><span data-ttu-id="37490-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-818">Finance</span></span></td>
<td><span data-ttu-id="37490-819">10001</span><span class="sxs-lookup"><span data-stu-id="37490-819">10001</span></span></td>
<td><span data-ttu-id="37490-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-820">Electricity</span></span></td>
<td><span data-ttu-id="37490-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-821">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="37490-822">-675.00</span></span></td>
<td><span data-ttu-id="37490-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-824">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-824">CC003</span></span></td>
<td><span data-ttu-id="37490-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-825">Assembly</span></span></td>
<td><span data-ttu-id="37490-826">10001</span><span class="sxs-lookup"><span data-stu-id="37490-826">10001</span></span></td>
<td><span data-ttu-id="37490-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-827">Electricity</span></span></td>
<td><span data-ttu-id="37490-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-828">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-829">438.75</span><span class="sxs-lookup"><span data-stu-id="37490-829">438.75</span></span></td>
<td><span data-ttu-id="37490-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-831">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-831">CC004</span></span></td>
<td><span data-ttu-id="37490-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-832">Packaging</span></span></td>
<td><span data-ttu-id="37490-833">10001</span><span class="sxs-lookup"><span data-stu-id="37490-833">10001</span></span></td>
<td><span data-ttu-id="37490-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-834">Electricity</span></span></td>
<td><span data-ttu-id="37490-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-835">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-836">236.25</span><span class="sxs-lookup"><span data-stu-id="37490-836">236.25</span></span></td>
<td><span data-ttu-id="37490-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-838">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-838">CC002</span></span></td>
<td><span data-ttu-id="37490-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="37490-839">Finance</span></span></td>
<td><span data-ttu-id="37490-840">10001</span><span class="sxs-lookup"><span data-stu-id="37490-840">10001</span></span></td>
<td><span data-ttu-id="37490-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-841">Electricity</span></span></td>
<td><span data-ttu-id="37490-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-842">Variable cost</span></span></td>
<td><span data-ttu-id="37490-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="37490-843">-8,150.29</span></span></td>
<td><span data-ttu-id="37490-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-845">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-845">CC003</span></span></td>
<td><span data-ttu-id="37490-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-846">Assembly</span></span></td>
<td><span data-ttu-id="37490-847">10001</span><span class="sxs-lookup"><span data-stu-id="37490-847">10001</span></span></td>
<td><span data-ttu-id="37490-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-848">Electricity</span></span></td>
<td><span data-ttu-id="37490-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-849">Variable cost</span></span></td>
<td><span data-ttu-id="37490-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="37490-850">5,297.69</span></span></td>
<td><span data-ttu-id="37490-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-852">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-852">CC004</span></span></td>
<td><span data-ttu-id="37490-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="37490-853">Packaging</span></span></td>
<td><span data-ttu-id="37490-854">10001</span><span class="sxs-lookup"><span data-stu-id="37490-854">10001</span></span></td>
<td><span data-ttu-id="37490-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-855">Electricity</span></span></td>
<td><span data-ttu-id="37490-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-856">Variable cost</span></span></td>
<td><span data-ttu-id="37490-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="37490-857">2,852.60</span></span></td>
<td><span data-ttu-id="37490-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-859">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-859">CC003</span></span></td>
<td><span data-ttu-id="37490-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-860">Assembly</span></span></td>
<td><span data-ttu-id="37490-861">10001</span><span class="sxs-lookup"><span data-stu-id="37490-861">10001</span></span></td>
<td><span data-ttu-id="37490-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-862">Electricity</span></span></td>
<td><span data-ttu-id="37490-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-863">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="37490-864">-713.75</span></span></td>
<td><span data-ttu-id="37490-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-866">Prod 1</span></span></td>
<td><span data-ttu-id="37490-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-867">Product 1</span></span></td>
<td><span data-ttu-id="37490-868">10001</span><span class="sxs-lookup"><span data-stu-id="37490-868">10001</span></span></td>
<td><span data-ttu-id="37490-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-869">Electricity</span></span></td>
<td><span data-ttu-id="37490-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-870">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-871">535.31</span><span class="sxs-lookup"><span data-stu-id="37490-871">535.31</span></span></td>
<td><span data-ttu-id="37490-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-873">Prod 2</span></span></td>
<td><span data-ttu-id="37490-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-874">Product 2</span></span></td>
<td><span data-ttu-id="37490-875">10001</span><span class="sxs-lookup"><span data-stu-id="37490-875">10001</span></span></td>
<td><span data-ttu-id="37490-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-876">Electricity</span></span></td>
<td><span data-ttu-id="37490-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-877">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-878">178.44</span><span class="sxs-lookup"><span data-stu-id="37490-878">178.44</span></span></td>
<td><span data-ttu-id="37490-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-880">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-880">CC003</span></span></td>
<td><span data-ttu-id="37490-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-881">Assembly</span></span></td>
<td><span data-ttu-id="37490-882">10001</span><span class="sxs-lookup"><span data-stu-id="37490-882">10001</span></span></td>
<td><span data-ttu-id="37490-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-883">Electricity</span></span></td>
<td><span data-ttu-id="37490-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-884">Variable cost</span></span></td>
<td><span data-ttu-id="37490-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="37490-885">-5,982.83</span></span></td>
<td><span data-ttu-id="37490-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-887">Prod 1</span></span></td>
<td><span data-ttu-id="37490-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-888">Product 1</span></span></td>
<td><span data-ttu-id="37490-889">10001</span><span class="sxs-lookup"><span data-stu-id="37490-889">10001</span></span></td>
<td><span data-ttu-id="37490-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-890">Electricity</span></span></td>
<td><span data-ttu-id="37490-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-891">Variable cost</span></span></td>
<td><span data-ttu-id="37490-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="37490-892">4,487.12</span></span></td>
<td><span data-ttu-id="37490-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-894">Prod 2</span></span></td>
<td><span data-ttu-id="37490-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-895">Product 2</span></span></td>
<td><span data-ttu-id="37490-896">10001</span><span class="sxs-lookup"><span data-stu-id="37490-896">10001</span></span></td>
<td><span data-ttu-id="37490-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-897">Electricity</span></span></td>
<td><span data-ttu-id="37490-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-898">Variable cost</span></span></td>
<td><span data-ttu-id="37490-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="37490-899">1,495.71</span></span></td>
<td><span data-ttu-id="37490-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-901">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-901">CC003</span></span></td>
<td><span data-ttu-id="37490-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-902">Assembly</span></span></td>
<td><span data-ttu-id="37490-903">10001</span><span class="sxs-lookup"><span data-stu-id="37490-903">10001</span></span></td>
<td><span data-ttu-id="37490-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-904">Electricity</span></span></td>
<td><span data-ttu-id="37490-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-905">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="37490-906">-286.25</span></span></td>
<td><span data-ttu-id="37490-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-908">Prod 1</span></span></td>
<td><span data-ttu-id="37490-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-909">Product 1</span></span></td>
<td><span data-ttu-id="37490-910">10001</span><span class="sxs-lookup"><span data-stu-id="37490-910">10001</span></span></td>
<td><span data-ttu-id="37490-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-911">Electricity</span></span></td>
<td><span data-ttu-id="37490-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-912">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-913">241.05</span><span class="sxs-lookup"><span data-stu-id="37490-913">241.05</span></span></td>
<td><span data-ttu-id="37490-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-915">Prod 2</span></span></td>
<td><span data-ttu-id="37490-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-916">Product 2</span></span></td>
<td><span data-ttu-id="37490-917">10001</span><span class="sxs-lookup"><span data-stu-id="37490-917">10001</span></span></td>
<td><span data-ttu-id="37490-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-918">Electricity</span></span></td>
<td><span data-ttu-id="37490-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-919">Fixed cost</span></span></td>
<td><span data-ttu-id="37490-920">45.20</span><span class="sxs-lookup"><span data-stu-id="37490-920">45.20</span></span></td>
<td><span data-ttu-id="37490-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-922">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-922">CC003</span></span></td>
<td><span data-ttu-id="37490-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="37490-923">Assembly</span></span></td>
<td><span data-ttu-id="37490-924">10001</span><span class="sxs-lookup"><span data-stu-id="37490-924">10001</span></span></td>
<td><span data-ttu-id="37490-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-925">Electricity</span></span></td>
<td><span data-ttu-id="37490-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-926">Variable cost</span></span></td>
<td><span data-ttu-id="37490-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="37490-927">-2,977.17</span></span></td>
<td><span data-ttu-id="37490-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-929">Prod 1</span></span></td>
<td><span data-ttu-id="37490-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="37490-930">Product 1</span></span></td>
<td><span data-ttu-id="37490-931">10001</span><span class="sxs-lookup"><span data-stu-id="37490-931">10001</span></span></td>
<td><span data-ttu-id="37490-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-932">Electricity</span></span></td>
<td><span data-ttu-id="37490-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-933">Variable cost</span></span></td>
<td><span data-ttu-id="37490-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="37490-934">2,507.09</span></span></td>
<td><span data-ttu-id="37490-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37490-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-936">Prod 2</span></span></td>
<td><span data-ttu-id="37490-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="37490-937">Product 2</span></span></td>
<td><span data-ttu-id="37490-938">10001</span><span class="sxs-lookup"><span data-stu-id="37490-938">10001</span></span></td>
<td><span data-ttu-id="37490-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-939">Electricity</span></span></td>
<td><span data-ttu-id="37490-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-940">Variable cost</span></span></td>
<td><span data-ttu-id="37490-941">470.08</span><span class="sxs-lookup"><span data-stu-id="37490-941">470.08</span></span></td>
<td><span data-ttu-id="37490-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="37490-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="37490-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="37490-943">Conclusion</span></span>
<span data-ttu-id="37490-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="37490-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="37490-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="37490-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="37490-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="37490-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="37490-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="37490-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="37490-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="37490-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="37490-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="37490-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="37490-951">CC099</span><span class="sxs-lookup"><span data-stu-id="37490-951">CC099</span></span></th>
<th><span data-ttu-id="37490-952">CC001</span><span class="sxs-lookup"><span data-stu-id="37490-952">CC001</span></span></th>
<th><span data-ttu-id="37490-953">CC002</span><span class="sxs-lookup"><span data-stu-id="37490-953">CC002</span></span></th>
<th><span data-ttu-id="37490-954">CC003</span><span class="sxs-lookup"><span data-stu-id="37490-954">CC003</span></span></th>
<th><span data-ttu-id="37490-955">CC004</span><span class="sxs-lookup"><span data-stu-id="37490-955">CC004</span></span></th>
<th><span data-ttu-id="37490-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="37490-956">Proj 1</span></span></th>
<th><span data-ttu-id="37490-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="37490-957">Proj 2</span></span></th>
<th><span data-ttu-id="37490-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="37490-958">Prod 1</span></span></th>
<th><span data-ttu-id="37490-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="37490-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="37490-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="37490-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="37490-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="37490-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="37490-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="37490-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="37490-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-971">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="37490-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-973">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-974">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-975">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-976">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-977">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="37490-978">776.36</span><span class="sxs-lookup"><span data-stu-id="37490-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-979">223.64</span><span class="sxs-lookup"><span data-stu-id="37490-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="37490-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="37490-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-982">000</span><span class="sxs-lookup"><span data-stu-id="37490-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-983">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-984">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-985">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-986">0,00</span><span class="sxs-lookup"><span data-stu-id="37490-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-987">30.00</span><span class="sxs-lookup"><span data-stu-id="37490-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-988">10,00</span><span class="sxs-lookup"><span data-stu-id="37490-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="37490-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="37490-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="37490-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="37490-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="37490-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="37490-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="37490-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="37490-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="37490-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="37490-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="37490-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="37490-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="37490-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]