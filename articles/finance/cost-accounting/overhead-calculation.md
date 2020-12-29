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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447312"
---
# <a name="overhead-calculation"></a><span data-ttu-id="c0a5b-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c0a5b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0a5b-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c0a5b-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-105">Term definition</span></span>
---------------

<span data-ttu-id="c0a5b-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c0a5b-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c0a5b-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c0a5b-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="c0a5b-109">Rent</span></span>
-   <span data-ttu-id="c0a5b-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-110">Electricity</span></span>
-   <span data-ttu-id="c0a5b-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="c0a5b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c0a5b-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c0a5b-112">Overhead calculation overview</span></span>
<span data-ttu-id="c0a5b-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c0a5b-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c0a5b-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c0a5b-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c0a5b-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c0a5b-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="c0a5b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c0a5b-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="c0a5b-119">Version type</span></span>
-   <span data-ttu-id="c0a5b-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="c0a5b-120">Date and time</span></span>
-   <span data-ttu-id="c0a5b-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c0a5b-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="c0a5b-122">Fiscal year</span></span>
-   <span data-ttu-id="c0a5b-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="c0a5b-123">Fiscal period</span></span>

<span data-ttu-id="c0a5b-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c0a5b-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c0a5b-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c0a5b-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c0a5b-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c0a5b-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c0a5b-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c0a5b-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c0a5b-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c0a5b-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c0a5b-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c0a5b-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c0a5b-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c0a5b-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="c0a5b-140">Main account</span></span></th>
<th><span data-ttu-id="c0a5b-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="c0a5b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-143">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-144">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-145">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-145">10001</span></span></td>
<td><span data-ttu-id="c0a5b-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-146">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c0a5b-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c0a5b-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c0a5b-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c0a5b-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c0a5b-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c0a5b-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c0a5b-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c0a5b-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="c0a5b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c0a5b-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c0a5b-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c0a5b-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c0a5b-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-160">Journal</span></span></th>
<th><span data-ttu-id="c0a5b-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="c0a5b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0a5b-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="c0a5b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0a5b-163">Версия</span><span class="sxs-lookup"><span data-stu-id="c0a5b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-164">00001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-164">00001</span></span></td>
<td><span data-ttu-id="c0a5b-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c0a5b-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="c0a5b-166">Fiscal</span></span></td>
<td><span data-ttu-id="c0a5b-167">2017</span><span class="sxs-lookup"><span data-stu-id="c0a5b-167">2017</span></span></td>
<td><span data-ttu-id="c0a5b-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-168">Period 1</span></span></td>
<td><span data-ttu-id="c0a5b-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0a5b-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-173">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-177">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-178">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-179">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-179">10001</span></span></td>
<td><span data-ttu-id="c0a5b-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-180">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="c0a5b-181">Unclassified</span></span></td>
<td><span data-ttu-id="c0a5b-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0a5b-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-185">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-187">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-189">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-190">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-191">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-191">10001</span></span></td>
<td><span data-ttu-id="c0a5b-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-192">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="c0a5b-193">Unclassified</span></span></td>
<td><span data-ttu-id="c0a5b-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-194">10,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-196">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-197">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-198">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-198">10001</span></span></td>
<td><span data-ttu-id="c0a5b-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-199">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="c0a5b-200">Unclassified</span></span></td>
<td><span data-ttu-id="c0a5b-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-203">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-204">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-205">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-205">10001</span></span></td>
<td><span data-ttu-id="c0a5b-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-206">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-208">1,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-210">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-211">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-212">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-212">10001</span></span></td>
<td><span data-ttu-id="c0a5b-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-213">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-214">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-215">9,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c0a5b-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c0a5b-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c0a5b-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c0a5b-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c0a5b-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c0a5b-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c0a5b-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c0a5b-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c0a5b-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c0a5b-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-228">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="c0a5b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-230">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-231">HR</span></span></td>
<td><span data-ttu-id="c0a5b-232">1000</span><span class="sxs-lookup"><span data-stu-id="c0a5b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-233">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-234">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-235">6,000</span><span class="sxs-lookup"><span data-stu-id="c0a5b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-236">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-237">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-238">0</span><span class="sxs-lookup"><span data-stu-id="c0a5b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-240">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-241">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-241">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-244">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-245">HR</span></span></td>
<td><span data-ttu-id="c0a5b-246">1000</span><span class="sxs-lookup"><span data-stu-id="c0a5b-246">1,000</span></span></td>
<td><span data-ttu-id="c0a5b-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-249">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-250">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-251">6,000</span><span class="sxs-lookup"><span data-stu-id="c0a5b-251">6,000</span></span></td>
<td><span data-ttu-id="c0a5b-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c0a5b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-254">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-255">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-256">0</span><span class="sxs-lookup"><span data-stu-id="c0a5b-256">0</span></span></td>
<td><span data-ttu-id="c0a5b-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-258">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c0a5b-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-261">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-262">Формула</span><span class="sxs-lookup"><span data-stu-id="c0a5b-262">Formula</span></span></th>
<th><span data-ttu-id="c0a5b-263">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-263">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-266">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-267">HR</span></span></td>
<td><span data-ttu-id="c0a5b-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0a5b-269">1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-269">1</span></span></td>
<td><span data-ttu-id="c0a5b-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-271">500.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-272">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-273">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0a5b-275">1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-275">1</span></span></td>
<td><span data-ttu-id="c0a5b-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-277">500.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-278">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-279">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0a5b-281">0</span><span class="sxs-lookup"><span data-stu-id="c0a5b-281">0</span></span></td>
<td><span data-ttu-id="c0a5b-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-283">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c0a5b-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-285">Journal</span></span></th>
<th><span data-ttu-id="c0a5b-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="c0a5b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0a5b-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="c0a5b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0a5b-288">Версия</span><span class="sxs-lookup"><span data-stu-id="c0a5b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-289">00002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-289">00002</span></span></td>
<td><span data-ttu-id="c0a5b-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c0a5b-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="c0a5b-291">Fiscal</span></span></td>
<td><span data-ttu-id="c0a5b-292">2017</span><span class="sxs-lookup"><span data-stu-id="c0a5b-292">2017</span></span></td>
<td><span data-ttu-id="c0a5b-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-293">Period 1</span></span></td>
<td><span data-ttu-id="c0a5b-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0a5b-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-298">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-302">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-303">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-304">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-304">10001</span></span></td>
<td><span data-ttu-id="c0a5b-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-305">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-309">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-310">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-311">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-311">10001</span></span></td>
<td><span data-ttu-id="c0a5b-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-312">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-313">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0a5b-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-317">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-319">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-321">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-322">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-323">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-323">10001</span></span></td>
<td><span data-ttu-id="c0a5b-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-324">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-328">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-329">HR</span></span></td>
<td><span data-ttu-id="c0a5b-330">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-330">10001</span></span></td>
<td><span data-ttu-id="c0a5b-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-331">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-333">500.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-333">500.00</span></span></td>
<td><span data-ttu-id="c0a5b-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-335">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-336">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-337">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-337">10001</span></span></td>
<td><span data-ttu-id="c0a5b-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-338">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-340">500.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-340">500.00</span></span></td>
<td><span data-ttu-id="c0a5b-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-342">CC099</span></span></td>
<td><span data-ttu-id="c0a5b-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a5b-343">Default cost center</span></span></td>
<td><span data-ttu-id="c0a5b-344">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-344">10001</span></span></td>
<td><span data-ttu-id="c0a5b-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-345">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-346">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c0a5b-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-349">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-350">HR</span></span></td>
<td><span data-ttu-id="c0a5b-351">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-351">10001</span></span></td>
<td><span data-ttu-id="c0a5b-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-352">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-353">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-354">1,285.71</span></span></td>
<td><span data-ttu-id="c0a5b-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-356">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-357">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-358">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-358">10001</span></span></td>
<td><span data-ttu-id="c0a5b-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-359">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-360">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c0a5b-361">7,714.29</span></span></td>
<td><span data-ttu-id="c0a5b-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c0a5b-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c0a5b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c0a5b-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c0a5b-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c0a5b-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c0a5b-367">Define the overhead rate</span></span>

<span data-ttu-id="c0a5b-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c0a5b-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-370">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-371">Часы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-372">Proj 1</span></span></td>
<td><span data-ttu-id="c0a5b-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-373">Project 1</span></span></td>
<td><span data-ttu-id="c0a5b-374">3</span><span class="sxs-lookup"><span data-stu-id="c0a5b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-375">Proj 2</span></span></td>
<td><span data-ttu-id="c0a5b-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-376">Project 2</span></span></td>
<td><span data-ttu-id="c0a5b-377">1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-379">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-380">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-382">Units</span></span></th>
<th><span data-ttu-id="c0a5b-383">По норме</span><span class="sxs-lookup"><span data-stu-id="c0a5b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-384">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-385">HR</span></span></td>
<td><span data-ttu-id="c0a5b-386">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-386">10001</span></span></td>
<td><span data-ttu-id="c0a5b-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-387">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-388">1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-388">1</span></span></td>
<td><span data-ttu-id="c0a5b-389">10</span><span class="sxs-lookup"><span data-stu-id="c0a5b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-391">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-392">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-392">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-393">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-396">Proj 1</span></span></td>
<td><span data-ttu-id="c0a5b-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-397">Project 1</span></span></td>
<td><span data-ttu-id="c0a5b-398">3</span><span class="sxs-lookup"><span data-stu-id="c0a5b-398">3</span></span></td>
<td><span data-ttu-id="c0a5b-399">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-399">10001</span></span></td>
<td><span data-ttu-id="c0a5b-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c0a5b-401">30.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-402">Proj 2</span></span></td>
<td><span data-ttu-id="c0a5b-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-403">Project 2</span></span></td>
<td><span data-ttu-id="c0a5b-404">1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-404">1</span></span></td>
<td><span data-ttu-id="c0a5b-405">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-405">10001</span></span></td>
<td><span data-ttu-id="c0a5b-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c0a5b-407">10,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c0a5b-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-409">Journal</span></span></th>
<th><span data-ttu-id="c0a5b-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="c0a5b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0a5b-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="c0a5b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0a5b-412">Версия</span><span class="sxs-lookup"><span data-stu-id="c0a5b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-413">00003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-413">00003</span></span></td>
<td><span data-ttu-id="c0a5b-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c0a5b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c0a5b-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="c0a5b-415">Fiscal</span></span></td>
<td><span data-ttu-id="c0a5b-416">2017</span><span class="sxs-lookup"><span data-stu-id="c0a5b-416">2017</span></span></td>
<td><span data-ttu-id="c0a5b-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-417">Period 1</span></span></td>
<td><span data-ttu-id="c0a5b-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c0a5b-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-421">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-422">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-424">Proj 1</span></span></td>
<td><span data-ttu-id="c0a5b-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c0a5b-426">3,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-428">Proj 2</span></span></td>
<td><span data-ttu-id="c0a5b-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c0a5b-430">1.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0a5b-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-433">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-435">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-437">CC0001</span></span></td>
<td><span data-ttu-id="c0a5b-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-438">HR</span></span></td>
<td><span data-ttu-id="c0a5b-439">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-439">10001</span></span></td>
<td><span data-ttu-id="c0a5b-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-440">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-441">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-442">-30.00</span></span></td>
<td><span data-ttu-id="c0a5b-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-444">Proj 1</span></span></td>
<td><span data-ttu-id="c0a5b-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c0a5b-446">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-446">10001</span></span></td>
<td><span data-ttu-id="c0a5b-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-447">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-448">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-449">30.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-449">30.00</span></span></td>
<td><span data-ttu-id="c0a5b-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-451">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-452">HR</span></span></td>
<td><span data-ttu-id="c0a5b-453">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-453">10001</span></span></td>
<td><span data-ttu-id="c0a5b-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-454">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-455">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-456">-10.00</span></span></td>
<td><span data-ttu-id="c0a5b-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-458">Proj 2</span></span></td>
<td><span data-ttu-id="c0a5b-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c0a5b-460">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-460">10001</span></span></td>
<td><span data-ttu-id="c0a5b-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-461">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-462">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-463">10.00</span></span></td>
<td><span data-ttu-id="c0a5b-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c0a5b-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c0a5b-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c0a5b-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="c0a5b-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c0a5b-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c0a5b-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c0a5b-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c0a5b-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c0a5b-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c0a5b-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-475">Define the cost allocation</span></span>

<span data-ttu-id="c0a5b-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c0a5b-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c0a5b-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-479">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-481">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-482">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-483">35</span><span class="sxs-lookup"><span data-stu-id="c0a5b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-484">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-485">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-486">55</span><span class="sxs-lookup"><span data-stu-id="c0a5b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-487">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-488">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-489">10</span><span class="sxs-lookup"><span data-stu-id="c0a5b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c0a5b-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-492">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="c0a5b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-494">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-495">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-496">65</span><span class="sxs-lookup"><span data-stu-id="c0a5b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-497">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-498">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-499">35</span><span class="sxs-lookup"><span data-stu-id="c0a5b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c0a5b-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-502">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-504">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-505">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-506">60</span><span class="sxs-lookup"><span data-stu-id="c0a5b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-507">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-508">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-509">20</span><span class="sxs-lookup"><span data-stu-id="c0a5b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c0a5b-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-512">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-514">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-515">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-516">80</span><span class="sxs-lookup"><span data-stu-id="c0a5b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-517">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-518">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-519">15</span><span class="sxs-lookup"><span data-stu-id="c0a5b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0a5b-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c0a5b-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c0a5b-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-523">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-524">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-524">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-526">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-528">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-529">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-530">35</span><span class="sxs-lookup"><span data-stu-id="c0a5b-530">35</span></span></td>
<td><span data-ttu-id="c0a5b-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0a5b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-532">175.00</span></span></td>
<td><span data-ttu-id="c0a5b-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-534">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-535">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-536">55</span><span class="sxs-lookup"><span data-stu-id="c0a5b-536">55</span></span></td>
<td><span data-ttu-id="c0a5b-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0a5b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-538">275.00</span></span></td>
<td><span data-ttu-id="c0a5b-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-540">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-541">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-542">10</span><span class="sxs-lookup"><span data-stu-id="c0a5b-542">10</span></span></td>
<td><span data-ttu-id="c0a5b-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0a5b-544">50,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-544">50.00</span></span></td>
<td><span data-ttu-id="c0a5b-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-546">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-547">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-548">35</span><span class="sxs-lookup"><span data-stu-id="c0a5b-548">35</span></span></td>
<td><span data-ttu-id="c0a5b-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0a5b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-550">436.00</span></span></td>
<td><span data-ttu-id="c0a5b-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-552">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-553">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-554">55</span><span class="sxs-lookup"><span data-stu-id="c0a5b-554">55</span></span></td>
<td><span data-ttu-id="c0a5b-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0a5b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c0a5b-556">685.14</span></span></td>
<td><span data-ttu-id="c0a5b-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-558">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-559">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-560">10</span><span class="sxs-lookup"><span data-stu-id="c0a5b-560">10</span></span></td>
<td><span data-ttu-id="c0a5b-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0a5b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c0a5b-562">124.57</span></span></td>
<td><span data-ttu-id="c0a5b-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-565">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-566">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-566">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-568">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-570">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-571">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-572">65</span><span class="sxs-lookup"><span data-stu-id="c0a5b-572">65</span></span></td>
<td><span data-ttu-id="c0a5b-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c0a5b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c0a5b-574">438.75</span></span></td>
<td><span data-ttu-id="c0a5b-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-576">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-577">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-578">35</span><span class="sxs-lookup"><span data-stu-id="c0a5b-578">35</span></span></td>
<td><span data-ttu-id="c0a5b-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c0a5b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c0a5b-580">236.25</span></span></td>
<td><span data-ttu-id="c0a5b-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-582">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-583">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-584">65</span><span class="sxs-lookup"><span data-stu-id="c0a5b-584">65</span></span></td>
<td><span data-ttu-id="c0a5b-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c0a5b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c0a5b-586">5,297.69</span></span></td>
<td><span data-ttu-id="c0a5b-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-588">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-589">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-590">35</span><span class="sxs-lookup"><span data-stu-id="c0a5b-590">35</span></span></td>
<td><span data-ttu-id="c0a5b-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c0a5b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c0a5b-592">2,852.60</span></span></td>
<td><span data-ttu-id="c0a5b-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-595">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-596">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-596">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-598">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-600">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-601">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-602">60</span><span class="sxs-lookup"><span data-stu-id="c0a5b-602">60</span></span></td>
<td><span data-ttu-id="c0a5b-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c0a5b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c0a5b-604">535.31</span></span></td>
<td><span data-ttu-id="c0a5b-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-606">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-607">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-608">20</span><span class="sxs-lookup"><span data-stu-id="c0a5b-608">20</span></span></td>
<td><span data-ttu-id="c0a5b-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c0a5b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c0a5b-610">178.44</span></span></td>
<td><span data-ttu-id="c0a5b-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-612">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-613">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-614">60</span><span class="sxs-lookup"><span data-stu-id="c0a5b-614">60</span></span></td>
<td><span data-ttu-id="c0a5b-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c0a5b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c0a5b-616">4,487.12</span></span></td>
<td><span data-ttu-id="c0a5b-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-618">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-619">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-620">20</span><span class="sxs-lookup"><span data-stu-id="c0a5b-620">20</span></span></td>
<td><span data-ttu-id="c0a5b-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c0a5b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-622">1,495.71</span></span></td>
<td><span data-ttu-id="c0a5b-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0a5b-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-625">Cost object</span></span></th>
<th><span data-ttu-id="c0a5b-626">Величина</span><span class="sxs-lookup"><span data-stu-id="c0a5b-626">Magnitude</span></span></th>
<th><span data-ttu-id="c0a5b-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="c0a5b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c0a5b-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-628">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-630">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-631">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-632">80</span><span class="sxs-lookup"><span data-stu-id="c0a5b-632">80</span></span></td>
<td><span data-ttu-id="c0a5b-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c0a5b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c0a5b-634">241.05</span></span></td>
<td><span data-ttu-id="c0a5b-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-636">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-637">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-638">15</span><span class="sxs-lookup"><span data-stu-id="c0a5b-638">15</span></span></td>
<td><span data-ttu-id="c0a5b-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c0a5b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c0a5b-640">45.20</span></span></td>
<td><span data-ttu-id="c0a5b-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-642">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-643">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-644">80</span><span class="sxs-lookup"><span data-stu-id="c0a5b-644">80</span></span></td>
<td><span data-ttu-id="c0a5b-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c0a5b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c0a5b-646">2,507.09</span></span></td>
<td><span data-ttu-id="c0a5b-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-648">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-649">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-650">15</span><span class="sxs-lookup"><span data-stu-id="c0a5b-650">15</span></span></td>
<td><span data-ttu-id="c0a5b-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c0a5b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c0a5b-652">470.08</span></span></td>
<td><span data-ttu-id="c0a5b-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0a5b-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="c0a5b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="c0a5b-655">Journal</span></span></th>
<th><span data-ttu-id="c0a5b-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="c0a5b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0a5b-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="c0a5b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0a5b-658">Версия</span><span class="sxs-lookup"><span data-stu-id="c0a5b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-659">00004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-659">00004</span></span></td>
<td><span data-ttu-id="c0a5b-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c0a5b-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="c0a5b-661">Fiscal</span></span></td>
<td><span data-ttu-id="c0a5b-662">2017</span><span class="sxs-lookup"><span data-stu-id="c0a5b-662">2017</span></span></td>
<td><span data-ttu-id="c0a5b-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-663">Period 1</span></span></td>
<td><span data-ttu-id="c0a5b-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c0a5b-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="c0a5b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0a5b-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-668">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-672">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-673">HR</span></span></td>
<td><span data-ttu-id="c0a5b-674">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-674">10001</span></span></td>
<td><span data-ttu-id="c0a5b-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-675">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-677">500.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-679">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-680">HR</span></span></td>
<td><span data-ttu-id="c0a5b-681">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-681">10001</span></span></td>
<td><span data-ttu-id="c0a5b-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-682">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-683">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-686">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-687">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-688">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-688">10001</span></span></td>
<td><span data-ttu-id="c0a5b-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-689">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-693">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-694">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-695">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-695">10001</span></span></td>
<td><span data-ttu-id="c0a5b-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-696">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-697">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c0a5b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-700">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-701">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-702">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-702">10001</span></span></td>
<td><span data-ttu-id="c0a5b-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-703">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c0a5b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-707">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-708">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-709">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-709">10001</span></span></td>
<td><span data-ttu-id="c0a5b-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-710">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-711">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c0a5b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-714">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-715">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-716">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-716">10001</span></span></td>
<td><span data-ttu-id="c0a5b-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-717">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c0a5b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-721">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-722">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-723">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-723">10001</span></span></td>
<td><span data-ttu-id="c0a5b-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-724">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-725">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c0a5b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-728">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-729">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-730">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-730">10001</span></span></td>
<td><span data-ttu-id="c0a5b-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-731">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c0a5b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-735">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-736">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-737">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-737">10001</span></span></td>
<td><span data-ttu-id="c0a5b-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-738">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-739">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c0a5b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-742">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-743">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-744">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-744">10001</span></span></td>
<td><span data-ttu-id="c0a5b-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-745">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c0a5b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0a5b-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-749">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-750">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-751">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-751">10001</span></span></td>
<td><span data-ttu-id="c0a5b-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-752">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-753">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c0a5b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0a5b-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0a5b-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0a5b-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-757">Cost element</span></span></th>
<th><span data-ttu-id="c0a5b-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c0a5b-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-759">Amount</span></span></th>
<th><span data-ttu-id="c0a5b-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="c0a5b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0a5b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-761">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-762">HR</span></span></td>
<td><span data-ttu-id="c0a5b-763">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-763">10001</span></span></td>
<td><span data-ttu-id="c0a5b-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-764">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-766">-500.00</span></span></td>
<td><span data-ttu-id="c0a5b-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-768">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-769">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-770">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-770">10001</span></span></td>
<td><span data-ttu-id="c0a5b-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-771">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-773">175.00</span></span></td>
<td><span data-ttu-id="c0a5b-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-775">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-776">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-777">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-777">10001</span></span></td>
<td><span data-ttu-id="c0a5b-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-778">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-780">275.00</span></span></td>
<td><span data-ttu-id="c0a5b-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-782">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-783">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-784">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-784">10001</span></span></td>
<td><span data-ttu-id="c0a5b-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-785">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-787">50,00</span></span></td>
<td><span data-ttu-id="c0a5b-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-789">CC001</span></span></td>
<td><span data-ttu-id="c0a5b-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="c0a5b-790">HR</span></span></td>
<td><span data-ttu-id="c0a5b-791">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-791">10001</span></span></td>
<td><span data-ttu-id="c0a5b-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-792">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-793">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c0a5b-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-796">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-797">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-798">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-798">10001</span></span></td>
<td><span data-ttu-id="c0a5b-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-799">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-800">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-801">436.00</span></span></td>
<td><span data-ttu-id="c0a5b-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-803">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-804">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-805">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-805">10001</span></span></td>
<td><span data-ttu-id="c0a5b-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-806">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-807">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c0a5b-808">685.14</span></span></td>
<td><span data-ttu-id="c0a5b-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-810">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-811">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-812">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-812">10001</span></span></td>
<td><span data-ttu-id="c0a5b-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-813">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-814">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c0a5b-815">124.57</span></span></td>
<td><span data-ttu-id="c0a5b-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-817">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-818">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-819">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-819">10001</span></span></td>
<td><span data-ttu-id="c0a5b-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-820">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-822">-675.00</span></span></td>
<td><span data-ttu-id="c0a5b-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-824">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-825">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-826">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-826">10001</span></span></td>
<td><span data-ttu-id="c0a5b-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-827">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c0a5b-829">438.75</span></span></td>
<td><span data-ttu-id="c0a5b-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-831">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-832">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-833">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-833">10001</span></span></td>
<td><span data-ttu-id="c0a5b-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-834">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c0a5b-836">236.25</span></span></td>
<td><span data-ttu-id="c0a5b-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-838">CC002</span></span></td>
<td><span data-ttu-id="c0a5b-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="c0a5b-839">Finance</span></span></td>
<td><span data-ttu-id="c0a5b-840">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-840">10001</span></span></td>
<td><span data-ttu-id="c0a5b-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-841">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-842">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="c0a5b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c0a5b-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-845">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-846">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-847">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-847">10001</span></span></td>
<td><span data-ttu-id="c0a5b-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-848">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-849">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c0a5b-850">5,297.69</span></span></td>
<td><span data-ttu-id="c0a5b-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-852">CC004</span></span></td>
<td><span data-ttu-id="c0a5b-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-853">Packaging</span></span></td>
<td><span data-ttu-id="c0a5b-854">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-854">10001</span></span></td>
<td><span data-ttu-id="c0a5b-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-855">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-856">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c0a5b-857">2,852.60</span></span></td>
<td><span data-ttu-id="c0a5b-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-859">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-860">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-861">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-861">10001</span></span></td>
<td><span data-ttu-id="c0a5b-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-862">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="c0a5b-864">-713.75</span></span></td>
<td><span data-ttu-id="c0a5b-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-866">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-867">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-868">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-868">10001</span></span></td>
<td><span data-ttu-id="c0a5b-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-869">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c0a5b-871">535.31</span></span></td>
<td><span data-ttu-id="c0a5b-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-873">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-874">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-875">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-875">10001</span></span></td>
<td><span data-ttu-id="c0a5b-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-876">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c0a5b-878">178.44</span></span></td>
<td><span data-ttu-id="c0a5b-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-880">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-881">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-882">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-882">10001</span></span></td>
<td><span data-ttu-id="c0a5b-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-883">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-884">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="c0a5b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c0a5b-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-887">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-888">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-889">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-889">10001</span></span></td>
<td><span data-ttu-id="c0a5b-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-890">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-891">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c0a5b-892">4,487.12</span></span></td>
<td><span data-ttu-id="c0a5b-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-894">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-895">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-896">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-896">10001</span></span></td>
<td><span data-ttu-id="c0a5b-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-897">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-898">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c0a5b-899">1,495.71</span></span></td>
<td><span data-ttu-id="c0a5b-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-901">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-902">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-903">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-903">10001</span></span></td>
<td><span data-ttu-id="c0a5b-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-904">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="c0a5b-906">-286.25</span></span></td>
<td><span data-ttu-id="c0a5b-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-908">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-909">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-910">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-910">10001</span></span></td>
<td><span data-ttu-id="c0a5b-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-911">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c0a5b-913">241.05</span></span></td>
<td><span data-ttu-id="c0a5b-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-915">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-916">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-917">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-917">10001</span></span></td>
<td><span data-ttu-id="c0a5b-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-918">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c0a5b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c0a5b-920">45.20</span></span></td>
<td><span data-ttu-id="c0a5b-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-922">CC003</span></span></td>
<td><span data-ttu-id="c0a5b-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0a5b-923">Assembly</span></span></td>
<td><span data-ttu-id="c0a5b-924">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-924">10001</span></span></td>
<td><span data-ttu-id="c0a5b-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-925">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-926">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="c0a5b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c0a5b-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-929">Prod 1</span></span></td>
<td><span data-ttu-id="c0a5b-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-930">Product 1</span></span></td>
<td><span data-ttu-id="c0a5b-931">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-931">10001</span></span></td>
<td><span data-ttu-id="c0a5b-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-932">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-933">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c0a5b-934">2,507.09</span></span></td>
<td><span data-ttu-id="c0a5b-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0a5b-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-936">Prod 2</span></span></td>
<td><span data-ttu-id="c0a5b-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-937">Product 2</span></span></td>
<td><span data-ttu-id="c0a5b-938">10001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-938">10001</span></span></td>
<td><span data-ttu-id="c0a5b-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-939">Electricity</span></span></td>
<td><span data-ttu-id="c0a5b-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-940">Variable cost</span></span></td>
<td><span data-ttu-id="c0a5b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c0a5b-941">470.08</span></span></td>
<td><span data-ttu-id="c0a5b-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="c0a5b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c0a5b-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="c0a5b-943">Conclusion</span></span>
<span data-ttu-id="c0a5b-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c0a5b-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c0a5b-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c0a5b-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c0a5b-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c0a5b-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="c0a5b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c0a5b-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="c0a5b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c0a5b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c0a5b-951">CC099</span></span></th>
<th><span data-ttu-id="c0a5b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c0a5b-952">CC001</span></span></th>
<th><span data-ttu-id="c0a5b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c0a5b-953">CC002</span></span></th>
<th><span data-ttu-id="c0a5b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c0a5b-954">CC003</span></span></th>
<th><span data-ttu-id="c0a5b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c0a5b-955">CC004</span></span></th>
<th><span data-ttu-id="c0a5b-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-956">Proj 1</span></span></th>
<th><span data-ttu-id="c0a5b-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-957">Proj 2</span></span></th>
<th><span data-ttu-id="c0a5b-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="c0a5b-958">Prod 1</span></span></th>
<th><span data-ttu-id="c0a5b-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="c0a5b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c0a5b-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="c0a5b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c0a5b-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="c0a5b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-971">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c0a5b-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-973">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-975">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c0a5b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c0a5b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c0a5b-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="c0a5b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-982">000</span><span class="sxs-lookup"><span data-stu-id="c0a5b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-983">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-984">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-985">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-987">30.00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-988">10,00</span><span class="sxs-lookup"><span data-stu-id="c0a5b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c0a5b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c0a5b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0a5b-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0a5b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0a5b-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c0a5b-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c0a5b-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c0a5b-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="c0a5b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c0a5b-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="c0a5b-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



