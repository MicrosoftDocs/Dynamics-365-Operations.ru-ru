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
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009526"
---
# <a name="overhead-calculation"></a><span data-ttu-id="083df-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="083df-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="083df-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="083df-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="083df-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="083df-105">Term definition</span></span>
---------------

<span data-ttu-id="083df-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="083df-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="083df-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="083df-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="083df-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="083df-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="083df-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="083df-109">Rent</span></span>
-   <span data-ttu-id="083df-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-110">Electricity</span></span>
-   <span data-ttu-id="083df-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="083df-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="083df-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="083df-112">Overhead calculation overview</span></span>
<span data-ttu-id="083df-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="083df-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="083df-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="083df-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="083df-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="083df-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="083df-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="083df-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="083df-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="083df-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="083df-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="083df-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="083df-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="083df-119">Version type</span></span>
-   <span data-ttu-id="083df-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="083df-120">Date and time</span></span>
-   <span data-ttu-id="083df-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="083df-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="083df-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="083df-122">Fiscal year</span></span>
-   <span data-ttu-id="083df-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="083df-123">Fiscal period</span></span>

<span data-ttu-id="083df-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="083df-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="083df-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="083df-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="083df-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="083df-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="083df-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="083df-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="083df-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="083df-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="083df-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="083df-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="083df-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="083df-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="083df-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="083df-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="083df-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="083df-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="083df-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="083df-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="083df-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="083df-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="083df-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="083df-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="083df-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="083df-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="083df-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="083df-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="083df-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="083df-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="083df-140">Main account</span></span></th>
<th><span data-ttu-id="083df-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="083df-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="083df-143">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-143">CC099</span></span></td>
<td><span data-ttu-id="083df-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-144">Default cost center</span></span></td>
<td><span data-ttu-id="083df-145">10001</span><span class="sxs-lookup"><span data-stu-id="083df-145">10001</span></span></td>
<td><span data-ttu-id="083df-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-146">Electricity</span></span></td>
<td><span data-ttu-id="083df-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="083df-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="083df-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="083df-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="083df-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="083df-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="083df-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-151">Define the cost behavior rule</span></span>

<span data-ttu-id="083df-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="083df-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="083df-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="083df-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="083df-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="083df-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="083df-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="083df-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="083df-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="083df-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="083df-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="083df-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="083df-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-160">Journal</span></span></th>
<th><span data-ttu-id="083df-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="083df-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="083df-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="083df-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="083df-163">Версия</span><span class="sxs-lookup"><span data-stu-id="083df-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-164">00001</span><span class="sxs-lookup"><span data-stu-id="083df-164">00001</span></span></td>
<td><span data-ttu-id="083df-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="083df-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="083df-166">Fiscal</span></span></td>
<td><span data-ttu-id="083df-167">2017</span><span class="sxs-lookup"><span data-stu-id="083df-167">2017</span></span></td>
<td><span data-ttu-id="083df-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-168">Period 1</span></span></td>
<td><span data-ttu-id="083df-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="083df-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="083df-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="083df-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-173">Cost element</span></span></th>
<th><span data-ttu-id="083df-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-174">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="083df-177">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-177">CC099</span></span></td>
<td><span data-ttu-id="083df-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-178">Default cost center</span></span></td>
<td><span data-ttu-id="083df-179">10001</span><span class="sxs-lookup"><span data-stu-id="083df-179">10001</span></span></td>
<td><span data-ttu-id="083df-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-180">Electricity</span></span></td>
<td><span data-ttu-id="083df-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="083df-181">Unclassified</span></span></td>
<td><span data-ttu-id="083df-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="083df-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="083df-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="083df-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-185">Cost element</span></span></th>
<th><span data-ttu-id="083df-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-186">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-187">Amount</span></span></th>
<th><span data-ttu-id="083df-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-189">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-189">CC099</span></span></td>
<td><span data-ttu-id="083df-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-190">Default cost center</span></span></td>
<td><span data-ttu-id="083df-191">10001</span><span class="sxs-lookup"><span data-stu-id="083df-191">10001</span></span></td>
<td><span data-ttu-id="083df-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-192">Electricity</span></span></td>
<td><span data-ttu-id="083df-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="083df-193">Unclassified</span></span></td>
<td><span data-ttu-id="083df-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="083df-194">10,000.00</span></span></td>
<td><span data-ttu-id="083df-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-196">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-196">CC099</span></span></td>
<td><span data-ttu-id="083df-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-197">Default cost center</span></span></td>
<td><span data-ttu-id="083df-198">10001</span><span class="sxs-lookup"><span data-stu-id="083df-198">10001</span></span></td>
<td><span data-ttu-id="083df-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-199">Electricity</span></span></td>
<td><span data-ttu-id="083df-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="083df-200">Unclassified</span></span></td>
<td><span data-ttu-id="083df-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="083df-201">-10,000.00</span></span></td>
<td><span data-ttu-id="083df-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-203">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-203">CC099</span></span></td>
<td><span data-ttu-id="083df-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-204">Default cost center</span></span></td>
<td><span data-ttu-id="083df-205">10001</span><span class="sxs-lookup"><span data-stu-id="083df-205">10001</span></span></td>
<td><span data-ttu-id="083df-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-206">Electricity</span></span></td>
<td><span data-ttu-id="083df-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-207">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="083df-208">1,000.00</span></span></td>
<td><span data-ttu-id="083df-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-210">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-210">CC099</span></span></td>
<td><span data-ttu-id="083df-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-211">Default cost center</span></span></td>
<td><span data-ttu-id="083df-212">10001</span><span class="sxs-lookup"><span data-stu-id="083df-212">10001</span></span></td>
<td><span data-ttu-id="083df-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-213">Electricity</span></span></td>
<td><span data-ttu-id="083df-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-214">Variable cost</span></span></td>
<td><span data-ttu-id="083df-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="083df-215">9,000.00</span></span></td>
<td><span data-ttu-id="083df-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="083df-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="083df-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="083df-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="083df-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="083df-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-221">Define the cost distribution rule</span></span>

<span data-ttu-id="083df-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="083df-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="083df-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="083df-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="083df-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="083df-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="083df-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="083df-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="083df-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="083df-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="083df-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-228">Cost object</span></span></th>
<th><span data-ttu-id="083df-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="083df-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-230">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-230">CC001</span></span></td>
<td><span data-ttu-id="083df-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-231">HR</span></span></td>
<td><span data-ttu-id="083df-232">1000</span><span class="sxs-lookup"><span data-stu-id="083df-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-233">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-233">CC002</span></span></td>
<td><span data-ttu-id="083df-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-234">Finance</span></span></td>
<td><span data-ttu-id="083df-235">6,000</span><span class="sxs-lookup"><span data-stu-id="083df-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-236">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-236">CC003</span></span></td>
<td><span data-ttu-id="083df-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-237">Assembly</span></span></td>
<td><span data-ttu-id="083df-238">0</span><span class="sxs-lookup"><span data-stu-id="083df-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-240">Cost object</span></span></th>
<th><span data-ttu-id="083df-241">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-241">Magnitude</span></span></th>
<th><span data-ttu-id="083df-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-242">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-244">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-244">CC001</span></span></td>
<td><span data-ttu-id="083df-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-245">HR</span></span></td>
<td><span data-ttu-id="083df-246">1000</span><span class="sxs-lookup"><span data-stu-id="083df-246">1,000</span></span></td>
<td><span data-ttu-id="083df-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="083df-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="083df-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="083df-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-249">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-249">CC002</span></span></td>
<td><span data-ttu-id="083df-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-250">Finance</span></span></td>
<td><span data-ttu-id="083df-251">6,000</span><span class="sxs-lookup"><span data-stu-id="083df-251">6,000</span></span></td>
<td><span data-ttu-id="083df-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="083df-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="083df-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="083df-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-254">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-254">CC003</span></span></td>
<td><span data-ttu-id="083df-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-255">Assembly</span></span></td>
<td><span data-ttu-id="083df-256">0</span><span class="sxs-lookup"><span data-stu-id="083df-256">0</span></span></td>
<td><span data-ttu-id="083df-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="083df-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="083df-258">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="083df-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="083df-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-261">Cost object</span></span></th>
<th><span data-ttu-id="083df-262">Формула</span><span class="sxs-lookup"><span data-stu-id="083df-262">Formula</span></span></th>
<th><span data-ttu-id="083df-263">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-263">Magnitude</span></span></th>
<th><span data-ttu-id="083df-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-264">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-266">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-266">CC001</span></span></td>
<td><span data-ttu-id="083df-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-267">HR</span></span></td>
<td><span data-ttu-id="083df-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="083df-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="083df-269">1</span><span class="sxs-lookup"><span data-stu-id="083df-269">1</span></span></td>
<td><span data-ttu-id="083df-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="083df-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="083df-271">500.00</span><span class="sxs-lookup"><span data-stu-id="083df-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-272">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-272">CC002</span></span></td>
<td><span data-ttu-id="083df-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-273">Finance</span></span></td>
<td><span data-ttu-id="083df-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="083df-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="083df-275">1</span><span class="sxs-lookup"><span data-stu-id="083df-275">1</span></span></td>
<td><span data-ttu-id="083df-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="083df-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="083df-277">500.00</span><span class="sxs-lookup"><span data-stu-id="083df-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-278">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-278">CC003</span></span></td>
<td><span data-ttu-id="083df-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-279">Assembly</span></span></td>
<td><span data-ttu-id="083df-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="083df-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="083df-281">0</span><span class="sxs-lookup"><span data-stu-id="083df-281">0</span></span></td>
<td><span data-ttu-id="083df-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="083df-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="083df-283">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="083df-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-285">Journal</span></span></th>
<th><span data-ttu-id="083df-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="083df-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="083df-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="083df-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="083df-288">Версия</span><span class="sxs-lookup"><span data-stu-id="083df-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-289">00002</span><span class="sxs-lookup"><span data-stu-id="083df-289">00002</span></span></td>
<td><span data-ttu-id="083df-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="083df-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="083df-291">Fiscal</span></span></td>
<td><span data-ttu-id="083df-292">2017</span><span class="sxs-lookup"><span data-stu-id="083df-292">2017</span></span></td>
<td><span data-ttu-id="083df-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-293">Period 1</span></span></td>
<td><span data-ttu-id="083df-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="083df-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="083df-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="083df-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-298">Cost element</span></span></th>
<th><span data-ttu-id="083df-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-299">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-302">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-302">CC099</span></span></td>
<td><span data-ttu-id="083df-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-303">Default cost center</span></span></td>
<td><span data-ttu-id="083df-304">10001</span><span class="sxs-lookup"><span data-stu-id="083df-304">10001</span></span></td>
<td><span data-ttu-id="083df-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-305">Electricity</span></span></td>
<td><span data-ttu-id="083df-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-306">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="083df-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-309">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-309">CC099</span></span></td>
<td><span data-ttu-id="083df-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-310">Default cost center</span></span></td>
<td><span data-ttu-id="083df-311">10001</span><span class="sxs-lookup"><span data-stu-id="083df-311">10001</span></span></td>
<td><span data-ttu-id="083df-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-312">Electricity</span></span></td>
<td><span data-ttu-id="083df-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-313">Variable cost</span></span></td>
<td><span data-ttu-id="083df-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="083df-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="083df-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="083df-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-317">Cost element</span></span></th>
<th><span data-ttu-id="083df-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-318">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-319">Amount</span></span></th>
<th><span data-ttu-id="083df-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-321">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-321">CC099</span></span></td>
<td><span data-ttu-id="083df-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-322">Default cost center</span></span></td>
<td><span data-ttu-id="083df-323">10001</span><span class="sxs-lookup"><span data-stu-id="083df-323">10001</span></span></td>
<td><span data-ttu-id="083df-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-324">Electricity</span></span></td>
<td><span data-ttu-id="083df-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-325">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="083df-326">-1,000.00</span></span></td>
<td><span data-ttu-id="083df-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-328">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-328">CC001</span></span></td>
<td><span data-ttu-id="083df-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-329">HR</span></span></td>
<td><span data-ttu-id="083df-330">10001</span><span class="sxs-lookup"><span data-stu-id="083df-330">10001</span></span></td>
<td><span data-ttu-id="083df-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-331">Electricity</span></span></td>
<td><span data-ttu-id="083df-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-332">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-333">500.00</span><span class="sxs-lookup"><span data-stu-id="083df-333">500.00</span></span></td>
<td><span data-ttu-id="083df-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-335">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-335">CC002</span></span></td>
<td><span data-ttu-id="083df-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-336">Finance</span></span></td>
<td><span data-ttu-id="083df-337">10001</span><span class="sxs-lookup"><span data-stu-id="083df-337">10001</span></span></td>
<td><span data-ttu-id="083df-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-338">Electricity</span></span></td>
<td><span data-ttu-id="083df-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-339">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-340">500.00</span><span class="sxs-lookup"><span data-stu-id="083df-340">500.00</span></span></td>
<td><span data-ttu-id="083df-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-342">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-342">CC099</span></span></td>
<td><span data-ttu-id="083df-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="083df-343">Default cost center</span></span></td>
<td><span data-ttu-id="083df-344">10001</span><span class="sxs-lookup"><span data-stu-id="083df-344">10001</span></span></td>
<td><span data-ttu-id="083df-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-345">Electricity</span></span></td>
<td><span data-ttu-id="083df-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-346">Variable cost</span></span></td>
<td><span data-ttu-id="083df-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="083df-347">-9,000.00</span></span></td>
<td><span data-ttu-id="083df-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-349">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-349">CC001</span></span></td>
<td><span data-ttu-id="083df-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-350">HR</span></span></td>
<td><span data-ttu-id="083df-351">10001</span><span class="sxs-lookup"><span data-stu-id="083df-351">10001</span></span></td>
<td><span data-ttu-id="083df-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-352">Electricity</span></span></td>
<td><span data-ttu-id="083df-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-353">Variable cost</span></span></td>
<td><span data-ttu-id="083df-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="083df-354">1,285.71</span></span></td>
<td><span data-ttu-id="083df-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-356">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-356">CC002</span></span></td>
<td><span data-ttu-id="083df-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-357">Finance</span></span></td>
<td><span data-ttu-id="083df-358">10001</span><span class="sxs-lookup"><span data-stu-id="083df-358">10001</span></span></td>
<td><span data-ttu-id="083df-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-359">Electricity</span></span></td>
<td><span data-ttu-id="083df-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-360">Variable cost</span></span></td>
<td><span data-ttu-id="083df-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="083df-361">7,714.29</span></span></td>
<td><span data-ttu-id="083df-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="083df-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="083df-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="083df-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="083df-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="083df-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="083df-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="083df-367">Define the overhead rate</span></span>

<span data-ttu-id="083df-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="083df-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="083df-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="083df-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-370">Cost object</span></span></th>
<th><span data-ttu-id="083df-371">Часы</span><span class="sxs-lookup"><span data-stu-id="083df-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-372">Proj 1</span></span></td>
<td><span data-ttu-id="083df-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-373">Project 1</span></span></td>
<td><span data-ttu-id="083df-374">3</span><span class="sxs-lookup"><span data-stu-id="083df-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-375">Proj 2</span></span></td>
<td><span data-ttu-id="083df-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-376">Project 2</span></span></td>
<td><span data-ttu-id="083df-377">1</span><span class="sxs-lookup"><span data-stu-id="083df-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-379">Cost object</span></span></th>
<th><span data-ttu-id="083df-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-380">Cost element</span></span></th>
<th><span data-ttu-id="083df-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-381">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="083df-382">Units</span></span></th>
<th><span data-ttu-id="083df-383">По норме</span><span class="sxs-lookup"><span data-stu-id="083df-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-384">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-384">CC001</span></span></td>
<td><span data-ttu-id="083df-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-385">HR</span></span></td>
<td><span data-ttu-id="083df-386">10001</span><span class="sxs-lookup"><span data-stu-id="083df-386">10001</span></span></td>
<td><span data-ttu-id="083df-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-387">Variable cost</span></span></td>
<td><span data-ttu-id="083df-388">1</span><span class="sxs-lookup"><span data-stu-id="083df-388">1</span></span></td>
<td><span data-ttu-id="083df-389">10</span><span class="sxs-lookup"><span data-stu-id="083df-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-391">Cost object</span></span></th>
<th><span data-ttu-id="083df-392">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-392">Magnitude</span></span></th>
<th><span data-ttu-id="083df-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-393">Cost element</span></span></th>
<th><span data-ttu-id="083df-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-394">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-396">Proj 1</span></span></td>
<td><span data-ttu-id="083df-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-397">Project 1</span></span></td>
<td><span data-ttu-id="083df-398">3</span><span class="sxs-lookup"><span data-stu-id="083df-398">3</span></span></td>
<td><span data-ttu-id="083df-399">10001</span><span class="sxs-lookup"><span data-stu-id="083df-399">10001</span></span></td>
<td><span data-ttu-id="083df-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="083df-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="083df-401">30.00</span><span class="sxs-lookup"><span data-stu-id="083df-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-402">Proj 2</span></span></td>
<td><span data-ttu-id="083df-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-403">Project 2</span></span></td>
<td><span data-ttu-id="083df-404">1</span><span class="sxs-lookup"><span data-stu-id="083df-404">1</span></span></td>
<td><span data-ttu-id="083df-405">10001</span><span class="sxs-lookup"><span data-stu-id="083df-405">10001</span></span></td>
<td><span data-ttu-id="083df-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="083df-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="083df-407">10,00</span><span class="sxs-lookup"><span data-stu-id="083df-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="083df-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-409">Journal</span></span></th>
<th><span data-ttu-id="083df-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="083df-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="083df-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="083df-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="083df-412">Версия</span><span class="sxs-lookup"><span data-stu-id="083df-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-413">00003</span><span class="sxs-lookup"><span data-stu-id="083df-413">00003</span></span></td>
<td><span data-ttu-id="083df-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="083df-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="083df-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="083df-415">Fiscal</span></span></td>
<td><span data-ttu-id="083df-416">2017</span><span class="sxs-lookup"><span data-stu-id="083df-416">2017</span></span></td>
<td><span data-ttu-id="083df-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-417">Period 1</span></span></td>
<td><span data-ttu-id="083df-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="083df-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="083df-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="083df-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-421">Cost object</span></span></th>
<th><span data-ttu-id="083df-422">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-424">Proj 1</span></span></td>
<td><span data-ttu-id="083df-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="083df-426">3,00</span><span class="sxs-lookup"><span data-stu-id="083df-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-428">Proj 2</span></span></td>
<td><span data-ttu-id="083df-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="083df-430">1.00</span><span class="sxs-lookup"><span data-stu-id="083df-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="083df-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="083df-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-433">Cost element</span></span></th>
<th><span data-ttu-id="083df-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-434">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-435">Amount</span></span></th>
<th><span data-ttu-id="083df-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="083df-437">CC0001</span></span></td>
<td><span data-ttu-id="083df-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-438">HR</span></span></td>
<td><span data-ttu-id="083df-439">10001</span><span class="sxs-lookup"><span data-stu-id="083df-439">10001</span></span></td>
<td><span data-ttu-id="083df-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-440">Electricity</span></span></td>
<td><span data-ttu-id="083df-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-441">Variable cost</span></span></td>
<td><span data-ttu-id="083df-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="083df-442">-30.00</span></span></td>
<td><span data-ttu-id="083df-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-444">Proj 1</span></span></td>
<td><span data-ttu-id="083df-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="083df-446">10001</span><span class="sxs-lookup"><span data-stu-id="083df-446">10001</span></span></td>
<td><span data-ttu-id="083df-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-447">Electricity</span></span></td>
<td><span data-ttu-id="083df-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-448">Variable cost</span></span></td>
<td><span data-ttu-id="083df-449">30.00</span><span class="sxs-lookup"><span data-stu-id="083df-449">30.00</span></span></td>
<td><span data-ttu-id="083df-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-451">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-451">CC001</span></span></td>
<td><span data-ttu-id="083df-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-452">HR</span></span></td>
<td><span data-ttu-id="083df-453">10001</span><span class="sxs-lookup"><span data-stu-id="083df-453">10001</span></span></td>
<td><span data-ttu-id="083df-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-454">Electricity</span></span></td>
<td><span data-ttu-id="083df-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-455">Variable cost</span></span></td>
<td><span data-ttu-id="083df-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="083df-456">-10.00</span></span></td>
<td><span data-ttu-id="083df-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-458">Proj 2</span></span></td>
<td><span data-ttu-id="083df-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="083df-460">10001</span><span class="sxs-lookup"><span data-stu-id="083df-460">10001</span></span></td>
<td><span data-ttu-id="083df-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-461">Electricity</span></span></td>
<td><span data-ttu-id="083df-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-462">Variable cost</span></span></td>
<td><span data-ttu-id="083df-463">10.00</span><span class="sxs-lookup"><span data-stu-id="083df-463">10.00</span></span></td>
<td><span data-ttu-id="083df-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="083df-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="083df-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="083df-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="083df-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="083df-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="083df-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="083df-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="083df-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="083df-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="083df-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="083df-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="083df-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="083df-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="083df-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="083df-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="083df-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="083df-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-475">Define the cost allocation</span></span>

<span data-ttu-id="083df-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="083df-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="083df-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="083df-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-479">Cost object</span></span></th>
<th><span data-ttu-id="083df-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="083df-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-481">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-481">CC002</span></span></td>
<td><span data-ttu-id="083df-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-482">Finance</span></span></td>
<td><span data-ttu-id="083df-483">35</span><span class="sxs-lookup"><span data-stu-id="083df-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-484">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-484">CC003</span></span></td>
<td><span data-ttu-id="083df-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-485">Assembly</span></span></td>
<td><span data-ttu-id="083df-486">55</span><span class="sxs-lookup"><span data-stu-id="083df-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-487">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-487">CC004</span></span></td>
<td><span data-ttu-id="083df-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-488">Packaging</span></span></td>
<td><span data-ttu-id="083df-489">10</span><span class="sxs-lookup"><span data-stu-id="083df-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="083df-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="083df-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-492">Cost object</span></span></th>
<th><span data-ttu-id="083df-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="083df-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-494">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-494">CC003</span></span></td>
<td><span data-ttu-id="083df-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-495">Assembly</span></span></td>
<td><span data-ttu-id="083df-496">65</span><span class="sxs-lookup"><span data-stu-id="083df-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-497">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-497">CC004</span></span></td>
<td><span data-ttu-id="083df-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-498">Packaging</span></span></td>
<td><span data-ttu-id="083df-499">35</span><span class="sxs-lookup"><span data-stu-id="083df-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="083df-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="083df-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-502">Cost object</span></span></th>
<th><span data-ttu-id="083df-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="083df-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-504">Prod 1</span></span></td>
<td><span data-ttu-id="083df-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-505">Product 1</span></span></td>
<td><span data-ttu-id="083df-506">60</span><span class="sxs-lookup"><span data-stu-id="083df-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-507">Prod 2</span></span></td>
<td><span data-ttu-id="083df-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-508">Product 2</span></span></td>
<td><span data-ttu-id="083df-509">20</span><span class="sxs-lookup"><span data-stu-id="083df-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="083df-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="083df-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-512">Cost object</span></span></th>
<th><span data-ttu-id="083df-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="083df-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-514">Prod 1</span></span></td>
<td><span data-ttu-id="083df-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-515">Product 1</span></span></td>
<td><span data-ttu-id="083df-516">80</span><span class="sxs-lookup"><span data-stu-id="083df-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-517">Prod 2</span></span></td>
<td><span data-ttu-id="083df-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-518">Product 2</span></span></td>
<td><span data-ttu-id="083df-519">15</span><span class="sxs-lookup"><span data-stu-id="083df-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="083df-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="083df-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="083df-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="083df-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="083df-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="083df-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-523">Cost object</span></span></th>
<th><span data-ttu-id="083df-524">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-524">Magnitude</span></span></th>
<th><span data-ttu-id="083df-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-525">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-526">Amount</span></span></th>
<th><span data-ttu-id="083df-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-528">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-528">CC002</span></span></td>
<td><span data-ttu-id="083df-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-529">Finance</span></span></td>
<td><span data-ttu-id="083df-530">35</span><span class="sxs-lookup"><span data-stu-id="083df-530">35</span></span></td>
<td><span data-ttu-id="083df-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="083df-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="083df-532">175.00</span><span class="sxs-lookup"><span data-stu-id="083df-532">175.00</span></span></td>
<td><span data-ttu-id="083df-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-534">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-534">CC003</span></span></td>
<td><span data-ttu-id="083df-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-535">Assembly</span></span></td>
<td><span data-ttu-id="083df-536">55</span><span class="sxs-lookup"><span data-stu-id="083df-536">55</span></span></td>
<td><span data-ttu-id="083df-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="083df-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="083df-538">275.00</span><span class="sxs-lookup"><span data-stu-id="083df-538">275.00</span></span></td>
<td><span data-ttu-id="083df-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-540">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-540">CC004</span></span></td>
<td><span data-ttu-id="083df-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-541">Packaging</span></span></td>
<td><span data-ttu-id="083df-542">10</span><span class="sxs-lookup"><span data-stu-id="083df-542">10</span></span></td>
<td><span data-ttu-id="083df-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="083df-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="083df-544">50,00</span><span class="sxs-lookup"><span data-stu-id="083df-544">50.00</span></span></td>
<td><span data-ttu-id="083df-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-546">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-546">CC002</span></span></td>
<td><span data-ttu-id="083df-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-547">Finance</span></span></td>
<td><span data-ttu-id="083df-548">35</span><span class="sxs-lookup"><span data-stu-id="083df-548">35</span></span></td>
<td><span data-ttu-id="083df-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="083df-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="083df-550">436.00</span><span class="sxs-lookup"><span data-stu-id="083df-550">436.00</span></span></td>
<td><span data-ttu-id="083df-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-552">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-552">CC003</span></span></td>
<td><span data-ttu-id="083df-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-553">Assembly</span></span></td>
<td><span data-ttu-id="083df-554">55</span><span class="sxs-lookup"><span data-stu-id="083df-554">55</span></span></td>
<td><span data-ttu-id="083df-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="083df-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="083df-556">685.14</span><span class="sxs-lookup"><span data-stu-id="083df-556">685.14</span></span></td>
<td><span data-ttu-id="083df-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-558">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-558">CC004</span></span></td>
<td><span data-ttu-id="083df-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-559">Packaging</span></span></td>
<td><span data-ttu-id="083df-560">10</span><span class="sxs-lookup"><span data-stu-id="083df-560">10</span></span></td>
<td><span data-ttu-id="083df-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="083df-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="083df-562">124.57</span><span class="sxs-lookup"><span data-stu-id="083df-562">124.57</span></span></td>
<td><span data-ttu-id="083df-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="083df-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-565">Cost object</span></span></th>
<th><span data-ttu-id="083df-566">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-566">Magnitude</span></span></th>
<th><span data-ttu-id="083df-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-567">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-568">Amount</span></span></th>
<th><span data-ttu-id="083df-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-570">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-570">CC003</span></span></td>
<td><span data-ttu-id="083df-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-571">Assembly</span></span></td>
<td><span data-ttu-id="083df-572">65</span><span class="sxs-lookup"><span data-stu-id="083df-572">65</span></span></td>
<td><span data-ttu-id="083df-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="083df-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="083df-574">438.75</span><span class="sxs-lookup"><span data-stu-id="083df-574">438.75</span></span></td>
<td><span data-ttu-id="083df-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-576">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-576">CC004</span></span></td>
<td><span data-ttu-id="083df-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-577">Packaging</span></span></td>
<td><span data-ttu-id="083df-578">35</span><span class="sxs-lookup"><span data-stu-id="083df-578">35</span></span></td>
<td><span data-ttu-id="083df-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="083df-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="083df-580">236.25</span><span class="sxs-lookup"><span data-stu-id="083df-580">236.25</span></span></td>
<td><span data-ttu-id="083df-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-582">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-582">CC003</span></span></td>
<td><span data-ttu-id="083df-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-583">Assembly</span></span></td>
<td><span data-ttu-id="083df-584">65</span><span class="sxs-lookup"><span data-stu-id="083df-584">65</span></span></td>
<td><span data-ttu-id="083df-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="083df-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="083df-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="083df-586">5,297.69</span></span></td>
<td><span data-ttu-id="083df-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-588">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-588">CC004</span></span></td>
<td><span data-ttu-id="083df-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-589">Packaging</span></span></td>
<td><span data-ttu-id="083df-590">35</span><span class="sxs-lookup"><span data-stu-id="083df-590">35</span></span></td>
<td><span data-ttu-id="083df-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="083df-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="083df-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="083df-592">2,852.60</span></span></td>
<td><span data-ttu-id="083df-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="083df-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-595">Cost object</span></span></th>
<th><span data-ttu-id="083df-596">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-596">Magnitude</span></span></th>
<th><span data-ttu-id="083df-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-597">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-598">Amount</span></span></th>
<th><span data-ttu-id="083df-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-600">Prod 1</span></span></td>
<td><span data-ttu-id="083df-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-601">Product 1</span></span></td>
<td><span data-ttu-id="083df-602">60</span><span class="sxs-lookup"><span data-stu-id="083df-602">60</span></span></td>
<td><span data-ttu-id="083df-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="083df-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="083df-604">535.31</span><span class="sxs-lookup"><span data-stu-id="083df-604">535.31</span></span></td>
<td><span data-ttu-id="083df-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-606">Prod 2</span></span></td>
<td><span data-ttu-id="083df-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-607">Product 2</span></span></td>
<td><span data-ttu-id="083df-608">20</span><span class="sxs-lookup"><span data-stu-id="083df-608">20</span></span></td>
<td><span data-ttu-id="083df-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="083df-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="083df-610">178.44</span><span class="sxs-lookup"><span data-stu-id="083df-610">178.44</span></span></td>
<td><span data-ttu-id="083df-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-612">Prod 1</span></span></td>
<td><span data-ttu-id="083df-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-613">Product 1</span></span></td>
<td><span data-ttu-id="083df-614">60</span><span class="sxs-lookup"><span data-stu-id="083df-614">60</span></span></td>
<td><span data-ttu-id="083df-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="083df-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="083df-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="083df-616">4,487.12</span></span></td>
<td><span data-ttu-id="083df-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-618">Prod 2</span></span></td>
<td><span data-ttu-id="083df-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-619">Product 2</span></span></td>
<td><span data-ttu-id="083df-620">20</span><span class="sxs-lookup"><span data-stu-id="083df-620">20</span></span></td>
<td><span data-ttu-id="083df-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="083df-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="083df-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="083df-622">1,495.71</span></span></td>
<td><span data-ttu-id="083df-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="083df-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="083df-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-625">Cost object</span></span></th>
<th><span data-ttu-id="083df-626">Величина</span><span class="sxs-lookup"><span data-stu-id="083df-626">Magnitude</span></span></th>
<th><span data-ttu-id="083df-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="083df-627">Allocation factor</span></span></th>
<th><span data-ttu-id="083df-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-628">Amount</span></span></th>
<th><span data-ttu-id="083df-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-630">Prod 1</span></span></td>
<td><span data-ttu-id="083df-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-631">Product 1</span></span></td>
<td><span data-ttu-id="083df-632">80</span><span class="sxs-lookup"><span data-stu-id="083df-632">80</span></span></td>
<td><span data-ttu-id="083df-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="083df-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="083df-634">241.05</span><span class="sxs-lookup"><span data-stu-id="083df-634">241.05</span></span></td>
<td><span data-ttu-id="083df-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-636">Prod 2</span></span></td>
<td><span data-ttu-id="083df-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-637">Product 2</span></span></td>
<td><span data-ttu-id="083df-638">15</span><span class="sxs-lookup"><span data-stu-id="083df-638">15</span></span></td>
<td><span data-ttu-id="083df-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="083df-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="083df-640">45.20</span><span class="sxs-lookup"><span data-stu-id="083df-640">45.20</span></span></td>
<td><span data-ttu-id="083df-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-642">Prod 1</span></span></td>
<td><span data-ttu-id="083df-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-643">Product 1</span></span></td>
<td><span data-ttu-id="083df-644">80</span><span class="sxs-lookup"><span data-stu-id="083df-644">80</span></span></td>
<td><span data-ttu-id="083df-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="083df-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="083df-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="083df-646">2,507.09</span></span></td>
<td><span data-ttu-id="083df-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-648">Prod 2</span></span></td>
<td><span data-ttu-id="083df-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-649">Product 2</span></span></td>
<td><span data-ttu-id="083df-650">15</span><span class="sxs-lookup"><span data-stu-id="083df-650">15</span></span></td>
<td><span data-ttu-id="083df-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="083df-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="083df-652">470.08</span><span class="sxs-lookup"><span data-stu-id="083df-652">470.08</span></span></td>
<td><span data-ttu-id="083df-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="083df-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="083df-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="083df-655">Journal</span></span></th>
<th><span data-ttu-id="083df-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="083df-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="083df-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="083df-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="083df-658">Версия</span><span class="sxs-lookup"><span data-stu-id="083df-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-659">00004</span><span class="sxs-lookup"><span data-stu-id="083df-659">00004</span></span></td>
<td><span data-ttu-id="083df-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="083df-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="083df-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="083df-661">Fiscal</span></span></td>
<td><span data-ttu-id="083df-662">2017</span><span class="sxs-lookup"><span data-stu-id="083df-662">2017</span></span></td>
<td><span data-ttu-id="083df-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-663">Period 1</span></span></td>
<td><span data-ttu-id="083df-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="083df-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="083df-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="083df-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="083df-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="083df-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-668">Cost element</span></span></th>
<th><span data-ttu-id="083df-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-669">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-672">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-672">CC001</span></span></td>
<td><span data-ttu-id="083df-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-673">HR</span></span></td>
<td><span data-ttu-id="083df-674">10001</span><span class="sxs-lookup"><span data-stu-id="083df-674">10001</span></span></td>
<td><span data-ttu-id="083df-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-675">Electricity</span></span></td>
<td><span data-ttu-id="083df-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-676">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-677">500.00</span><span class="sxs-lookup"><span data-stu-id="083df-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-679">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-679">CC001</span></span></td>
<td><span data-ttu-id="083df-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-680">HR</span></span></td>
<td><span data-ttu-id="083df-681">10001</span><span class="sxs-lookup"><span data-stu-id="083df-681">10001</span></span></td>
<td><span data-ttu-id="083df-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-682">Electricity</span></span></td>
<td><span data-ttu-id="083df-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-683">Variable cost</span></span></td>
<td><span data-ttu-id="083df-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="083df-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-686">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-686">CC002</span></span></td>
<td><span data-ttu-id="083df-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-687">Finance</span></span></td>
<td><span data-ttu-id="083df-688">10001</span><span class="sxs-lookup"><span data-stu-id="083df-688">10001</span></span></td>
<td><span data-ttu-id="083df-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-689">Electricity</span></span></td>
<td><span data-ttu-id="083df-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-690">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-691">675.00</span><span class="sxs-lookup"><span data-stu-id="083df-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-693">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-693">CC002</span></span></td>
<td><span data-ttu-id="083df-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-694">Finance</span></span></td>
<td><span data-ttu-id="083df-695">10001</span><span class="sxs-lookup"><span data-stu-id="083df-695">10001</span></span></td>
<td><span data-ttu-id="083df-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-696">Electricity</span></span></td>
<td><span data-ttu-id="083df-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-697">Variable cost</span></span></td>
<td><span data-ttu-id="083df-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="083df-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-700">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-700">CC003</span></span></td>
<td><span data-ttu-id="083df-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-701">Assembly</span></span></td>
<td><span data-ttu-id="083df-702">10001</span><span class="sxs-lookup"><span data-stu-id="083df-702">10001</span></span></td>
<td><span data-ttu-id="083df-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-703">Electricity</span></span></td>
<td><span data-ttu-id="083df-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-704">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-705">713.75</span><span class="sxs-lookup"><span data-stu-id="083df-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-707">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-707">CC003</span></span></td>
<td><span data-ttu-id="083df-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-708">Assembly</span></span></td>
<td><span data-ttu-id="083df-709">10001</span><span class="sxs-lookup"><span data-stu-id="083df-709">10001</span></span></td>
<td><span data-ttu-id="083df-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-710">Electricity</span></span></td>
<td><span data-ttu-id="083df-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-711">Variable cost</span></span></td>
<td><span data-ttu-id="083df-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="083df-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-714">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-714">CC003</span></span></td>
<td><span data-ttu-id="083df-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-715">Packaging</span></span></td>
<td><span data-ttu-id="083df-716">10001</span><span class="sxs-lookup"><span data-stu-id="083df-716">10001</span></span></td>
<td><span data-ttu-id="083df-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-717">Electricity</span></span></td>
<td><span data-ttu-id="083df-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-718">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-719">286.25</span><span class="sxs-lookup"><span data-stu-id="083df-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-721">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-721">CC003</span></span></td>
<td><span data-ttu-id="083df-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-722">Packaging</span></span></td>
<td><span data-ttu-id="083df-723">10001</span><span class="sxs-lookup"><span data-stu-id="083df-723">10001</span></span></td>
<td><span data-ttu-id="083df-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-724">Electricity</span></span></td>
<td><span data-ttu-id="083df-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-725">Variable cost</span></span></td>
<td><span data-ttu-id="083df-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="083df-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-728">Prod 1</span></span></td>
<td><span data-ttu-id="083df-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-729">Product 1</span></span></td>
<td><span data-ttu-id="083df-730">10001</span><span class="sxs-lookup"><span data-stu-id="083df-730">10001</span></span></td>
<td><span data-ttu-id="083df-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-731">Electricity</span></span></td>
<td><span data-ttu-id="083df-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-732">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-733">776.36</span><span class="sxs-lookup"><span data-stu-id="083df-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-735">Prod 1</span></span></td>
<td><span data-ttu-id="083df-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-736">Product 1</span></span></td>
<td><span data-ttu-id="083df-737">10001</span><span class="sxs-lookup"><span data-stu-id="083df-737">10001</span></span></td>
<td><span data-ttu-id="083df-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-738">Electricity</span></span></td>
<td><span data-ttu-id="083df-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-739">Variable cost</span></span></td>
<td><span data-ttu-id="083df-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="083df-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-742">Prod 2</span></span></td>
<td><span data-ttu-id="083df-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-743">Product 1</span></span></td>
<td><span data-ttu-id="083df-744">10001</span><span class="sxs-lookup"><span data-stu-id="083df-744">10001</span></span></td>
<td><span data-ttu-id="083df-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-745">Electricity</span></span></td>
<td><span data-ttu-id="083df-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-746">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-747">223.64</span><span class="sxs-lookup"><span data-stu-id="083df-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="083df-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-749">Prod 2</span></span></td>
<td><span data-ttu-id="083df-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-750">Product 1</span></span></td>
<td><span data-ttu-id="083df-751">10001</span><span class="sxs-lookup"><span data-stu-id="083df-751">10001</span></span></td>
<td><span data-ttu-id="083df-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-752">Electricity</span></span></td>
<td><span data-ttu-id="083df-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-753">Variable cost</span></span></td>
<td><span data-ttu-id="083df-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="083df-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="083df-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="083df-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="083df-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="083df-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-757">Cost element</span></span></th>
<th><span data-ttu-id="083df-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="083df-758">Cost behavior</span></span></th>
<th><span data-ttu-id="083df-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="083df-759">Amount</span></span></th>
<th><span data-ttu-id="083df-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="083df-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="083df-761">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-761">CC001</span></span></td>
<td><span data-ttu-id="083df-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-762">HR</span></span></td>
<td><span data-ttu-id="083df-763">10001</span><span class="sxs-lookup"><span data-stu-id="083df-763">10001</span></span></td>
<td><span data-ttu-id="083df-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-764">Electricity</span></span></td>
<td><span data-ttu-id="083df-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-765">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="083df-766">-500.00</span></span></td>
<td><span data-ttu-id="083df-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-768">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-768">CC002</span></span></td>
<td><span data-ttu-id="083df-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-769">Finance</span></span></td>
<td><span data-ttu-id="083df-770">10001</span><span class="sxs-lookup"><span data-stu-id="083df-770">10001</span></span></td>
<td><span data-ttu-id="083df-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-771">Electricity</span></span></td>
<td><span data-ttu-id="083df-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-772">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-773">175.00</span><span class="sxs-lookup"><span data-stu-id="083df-773">175.00</span></span></td>
<td><span data-ttu-id="083df-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-775">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-775">CC003</span></span></td>
<td><span data-ttu-id="083df-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-776">Assembly</span></span></td>
<td><span data-ttu-id="083df-777">10001</span><span class="sxs-lookup"><span data-stu-id="083df-777">10001</span></span></td>
<td><span data-ttu-id="083df-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-778">Electricity</span></span></td>
<td><span data-ttu-id="083df-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-779">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-780">275.00</span><span class="sxs-lookup"><span data-stu-id="083df-780">275.00</span></span></td>
<td><span data-ttu-id="083df-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-782">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-782">CC004</span></span></td>
<td><span data-ttu-id="083df-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-783">Packaging</span></span></td>
<td><span data-ttu-id="083df-784">10001</span><span class="sxs-lookup"><span data-stu-id="083df-784">10001</span></span></td>
<td><span data-ttu-id="083df-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-785">Electricity</span></span></td>
<td><span data-ttu-id="083df-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-786">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-787">50,00</span><span class="sxs-lookup"><span data-stu-id="083df-787">50,00</span></span></td>
<td><span data-ttu-id="083df-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-789">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-789">CC001</span></span></td>
<td><span data-ttu-id="083df-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="083df-790">HR</span></span></td>
<td><span data-ttu-id="083df-791">10001</span><span class="sxs-lookup"><span data-stu-id="083df-791">10001</span></span></td>
<td><span data-ttu-id="083df-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-792">Electricity</span></span></td>
<td><span data-ttu-id="083df-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-793">Variable cost</span></span></td>
<td><span data-ttu-id="083df-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="083df-794">-1,245.71</span></span></td>
<td><span data-ttu-id="083df-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-796">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-796">CC002</span></span></td>
<td><span data-ttu-id="083df-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-797">Finance</span></span></td>
<td><span data-ttu-id="083df-798">10001</span><span class="sxs-lookup"><span data-stu-id="083df-798">10001</span></span></td>
<td><span data-ttu-id="083df-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-799">Electricity</span></span></td>
<td><span data-ttu-id="083df-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-800">Variable cost</span></span></td>
<td><span data-ttu-id="083df-801">436.00</span><span class="sxs-lookup"><span data-stu-id="083df-801">436.00</span></span></td>
<td><span data-ttu-id="083df-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-803">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-803">CC003</span></span></td>
<td><span data-ttu-id="083df-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-804">Assembly</span></span></td>
<td><span data-ttu-id="083df-805">10001</span><span class="sxs-lookup"><span data-stu-id="083df-805">10001</span></span></td>
<td><span data-ttu-id="083df-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-806">Electricity</span></span></td>
<td><span data-ttu-id="083df-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-807">Variable cost</span></span></td>
<td><span data-ttu-id="083df-808">685.14</span><span class="sxs-lookup"><span data-stu-id="083df-808">685.14</span></span></td>
<td><span data-ttu-id="083df-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-810">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-810">CC004</span></span></td>
<td><span data-ttu-id="083df-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-811">Packaging</span></span></td>
<td><span data-ttu-id="083df-812">10001</span><span class="sxs-lookup"><span data-stu-id="083df-812">10001</span></span></td>
<td><span data-ttu-id="083df-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-813">Electricity</span></span></td>
<td><span data-ttu-id="083df-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-814">Variable cost</span></span></td>
<td><span data-ttu-id="083df-815">124.57</span><span class="sxs-lookup"><span data-stu-id="083df-815">124.57</span></span></td>
<td><span data-ttu-id="083df-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-817">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-817">CC002</span></span></td>
<td><span data-ttu-id="083df-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-818">Finance</span></span></td>
<td><span data-ttu-id="083df-819">10001</span><span class="sxs-lookup"><span data-stu-id="083df-819">10001</span></span></td>
<td><span data-ttu-id="083df-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-820">Electricity</span></span></td>
<td><span data-ttu-id="083df-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-821">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="083df-822">-675.00</span></span></td>
<td><span data-ttu-id="083df-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-824">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-824">CC003</span></span></td>
<td><span data-ttu-id="083df-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-825">Assembly</span></span></td>
<td><span data-ttu-id="083df-826">10001</span><span class="sxs-lookup"><span data-stu-id="083df-826">10001</span></span></td>
<td><span data-ttu-id="083df-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-827">Electricity</span></span></td>
<td><span data-ttu-id="083df-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-828">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-829">438.75</span><span class="sxs-lookup"><span data-stu-id="083df-829">438.75</span></span></td>
<td><span data-ttu-id="083df-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-831">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-831">CC004</span></span></td>
<td><span data-ttu-id="083df-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-832">Packaging</span></span></td>
<td><span data-ttu-id="083df-833">10001</span><span class="sxs-lookup"><span data-stu-id="083df-833">10001</span></span></td>
<td><span data-ttu-id="083df-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-834">Electricity</span></span></td>
<td><span data-ttu-id="083df-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-835">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-836">236.25</span><span class="sxs-lookup"><span data-stu-id="083df-836">236.25</span></span></td>
<td><span data-ttu-id="083df-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-838">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-838">CC002</span></span></td>
<td><span data-ttu-id="083df-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="083df-839">Finance</span></span></td>
<td><span data-ttu-id="083df-840">10001</span><span class="sxs-lookup"><span data-stu-id="083df-840">10001</span></span></td>
<td><span data-ttu-id="083df-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-841">Electricity</span></span></td>
<td><span data-ttu-id="083df-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-842">Variable cost</span></span></td>
<td><span data-ttu-id="083df-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="083df-843">-8,150.29</span></span></td>
<td><span data-ttu-id="083df-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-845">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-845">CC003</span></span></td>
<td><span data-ttu-id="083df-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-846">Assembly</span></span></td>
<td><span data-ttu-id="083df-847">10001</span><span class="sxs-lookup"><span data-stu-id="083df-847">10001</span></span></td>
<td><span data-ttu-id="083df-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-848">Electricity</span></span></td>
<td><span data-ttu-id="083df-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-849">Variable cost</span></span></td>
<td><span data-ttu-id="083df-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="083df-850">5,297.69</span></span></td>
<td><span data-ttu-id="083df-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-852">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-852">CC004</span></span></td>
<td><span data-ttu-id="083df-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="083df-853">Packaging</span></span></td>
<td><span data-ttu-id="083df-854">10001</span><span class="sxs-lookup"><span data-stu-id="083df-854">10001</span></span></td>
<td><span data-ttu-id="083df-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-855">Electricity</span></span></td>
<td><span data-ttu-id="083df-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-856">Variable cost</span></span></td>
<td><span data-ttu-id="083df-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="083df-857">2,852.60</span></span></td>
<td><span data-ttu-id="083df-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-859">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-859">CC003</span></span></td>
<td><span data-ttu-id="083df-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-860">Assembly</span></span></td>
<td><span data-ttu-id="083df-861">10001</span><span class="sxs-lookup"><span data-stu-id="083df-861">10001</span></span></td>
<td><span data-ttu-id="083df-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-862">Electricity</span></span></td>
<td><span data-ttu-id="083df-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-863">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="083df-864">-713.75</span></span></td>
<td><span data-ttu-id="083df-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-866">Prod 1</span></span></td>
<td><span data-ttu-id="083df-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-867">Product 1</span></span></td>
<td><span data-ttu-id="083df-868">10001</span><span class="sxs-lookup"><span data-stu-id="083df-868">10001</span></span></td>
<td><span data-ttu-id="083df-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-869">Electricity</span></span></td>
<td><span data-ttu-id="083df-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-870">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-871">535.31</span><span class="sxs-lookup"><span data-stu-id="083df-871">535.31</span></span></td>
<td><span data-ttu-id="083df-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-873">Prod 2</span></span></td>
<td><span data-ttu-id="083df-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-874">Product 2</span></span></td>
<td><span data-ttu-id="083df-875">10001</span><span class="sxs-lookup"><span data-stu-id="083df-875">10001</span></span></td>
<td><span data-ttu-id="083df-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-876">Electricity</span></span></td>
<td><span data-ttu-id="083df-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-877">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-878">178.44</span><span class="sxs-lookup"><span data-stu-id="083df-878">178.44</span></span></td>
<td><span data-ttu-id="083df-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-880">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-880">CC003</span></span></td>
<td><span data-ttu-id="083df-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-881">Assembly</span></span></td>
<td><span data-ttu-id="083df-882">10001</span><span class="sxs-lookup"><span data-stu-id="083df-882">10001</span></span></td>
<td><span data-ttu-id="083df-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-883">Electricity</span></span></td>
<td><span data-ttu-id="083df-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-884">Variable cost</span></span></td>
<td><span data-ttu-id="083df-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="083df-885">-5,982.83</span></span></td>
<td><span data-ttu-id="083df-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-887">Prod 1</span></span></td>
<td><span data-ttu-id="083df-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-888">Product 1</span></span></td>
<td><span data-ttu-id="083df-889">10001</span><span class="sxs-lookup"><span data-stu-id="083df-889">10001</span></span></td>
<td><span data-ttu-id="083df-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-890">Electricity</span></span></td>
<td><span data-ttu-id="083df-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-891">Variable cost</span></span></td>
<td><span data-ttu-id="083df-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="083df-892">4,487.12</span></span></td>
<td><span data-ttu-id="083df-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-894">Prod 2</span></span></td>
<td><span data-ttu-id="083df-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-895">Product 2</span></span></td>
<td><span data-ttu-id="083df-896">10001</span><span class="sxs-lookup"><span data-stu-id="083df-896">10001</span></span></td>
<td><span data-ttu-id="083df-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-897">Electricity</span></span></td>
<td><span data-ttu-id="083df-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-898">Variable cost</span></span></td>
<td><span data-ttu-id="083df-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="083df-899">1,495.71</span></span></td>
<td><span data-ttu-id="083df-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-901">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-901">CC003</span></span></td>
<td><span data-ttu-id="083df-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-902">Assembly</span></span></td>
<td><span data-ttu-id="083df-903">10001</span><span class="sxs-lookup"><span data-stu-id="083df-903">10001</span></span></td>
<td><span data-ttu-id="083df-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-904">Electricity</span></span></td>
<td><span data-ttu-id="083df-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-905">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="083df-906">-286.25</span></span></td>
<td><span data-ttu-id="083df-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-908">Prod 1</span></span></td>
<td><span data-ttu-id="083df-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-909">Product 1</span></span></td>
<td><span data-ttu-id="083df-910">10001</span><span class="sxs-lookup"><span data-stu-id="083df-910">10001</span></span></td>
<td><span data-ttu-id="083df-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-911">Electricity</span></span></td>
<td><span data-ttu-id="083df-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-912">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-913">241.05</span><span class="sxs-lookup"><span data-stu-id="083df-913">241.05</span></span></td>
<td><span data-ttu-id="083df-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-915">Prod 2</span></span></td>
<td><span data-ttu-id="083df-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-916">Product 2</span></span></td>
<td><span data-ttu-id="083df-917">10001</span><span class="sxs-lookup"><span data-stu-id="083df-917">10001</span></span></td>
<td><span data-ttu-id="083df-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-918">Electricity</span></span></td>
<td><span data-ttu-id="083df-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-919">Fixed cost</span></span></td>
<td><span data-ttu-id="083df-920">45.20</span><span class="sxs-lookup"><span data-stu-id="083df-920">45.20</span></span></td>
<td><span data-ttu-id="083df-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-922">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-922">CC003</span></span></td>
<td><span data-ttu-id="083df-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="083df-923">Assembly</span></span></td>
<td><span data-ttu-id="083df-924">10001</span><span class="sxs-lookup"><span data-stu-id="083df-924">10001</span></span></td>
<td><span data-ttu-id="083df-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-925">Electricity</span></span></td>
<td><span data-ttu-id="083df-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-926">Variable cost</span></span></td>
<td><span data-ttu-id="083df-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="083df-927">-2,977.17</span></span></td>
<td><span data-ttu-id="083df-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-929">Prod 1</span></span></td>
<td><span data-ttu-id="083df-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="083df-930">Product 1</span></span></td>
<td><span data-ttu-id="083df-931">10001</span><span class="sxs-lookup"><span data-stu-id="083df-931">10001</span></span></td>
<td><span data-ttu-id="083df-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-932">Electricity</span></span></td>
<td><span data-ttu-id="083df-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-933">Variable cost</span></span></td>
<td><span data-ttu-id="083df-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="083df-934">2,507.09</span></span></td>
<td><span data-ttu-id="083df-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="083df-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-936">Prod 2</span></span></td>
<td><span data-ttu-id="083df-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="083df-937">Product 2</span></span></td>
<td><span data-ttu-id="083df-938">10001</span><span class="sxs-lookup"><span data-stu-id="083df-938">10001</span></span></td>
<td><span data-ttu-id="083df-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-939">Electricity</span></span></td>
<td><span data-ttu-id="083df-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-940">Variable cost</span></span></td>
<td><span data-ttu-id="083df-941">470.08</span><span class="sxs-lookup"><span data-stu-id="083df-941">470.08</span></span></td>
<td><span data-ttu-id="083df-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="083df-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="083df-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="083df-943">Conclusion</span></span>
<span data-ttu-id="083df-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="083df-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="083df-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="083df-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="083df-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="083df-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="083df-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="083df-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="083df-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="083df-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="083df-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="083df-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="083df-951">CC099</span><span class="sxs-lookup"><span data-stu-id="083df-951">CC099</span></span></th>
<th><span data-ttu-id="083df-952">CC001</span><span class="sxs-lookup"><span data-stu-id="083df-952">CC001</span></span></th>
<th><span data-ttu-id="083df-953">CC002</span><span class="sxs-lookup"><span data-stu-id="083df-953">CC002</span></span></th>
<th><span data-ttu-id="083df-954">CC003</span><span class="sxs-lookup"><span data-stu-id="083df-954">CC003</span></span></th>
<th><span data-ttu-id="083df-955">CC004</span><span class="sxs-lookup"><span data-stu-id="083df-955">CC004</span></span></th>
<th><span data-ttu-id="083df-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="083df-956">Proj 1</span></span></th>
<th><span data-ttu-id="083df-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="083df-957">Proj 2</span></span></th>
<th><span data-ttu-id="083df-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="083df-958">Prod 1</span></span></th>
<th><span data-ttu-id="083df-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="083df-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="083df-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="083df-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="083df-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="083df-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="083df-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="083df-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="083df-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-971">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="083df-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-973">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-974">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-975">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-976">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-977">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="083df-978">776.36</span><span class="sxs-lookup"><span data-stu-id="083df-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-979">223.64</span><span class="sxs-lookup"><span data-stu-id="083df-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="083df-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="083df-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-982">000</span><span class="sxs-lookup"><span data-stu-id="083df-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-983">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-984">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-985">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-986">0,00</span><span class="sxs-lookup"><span data-stu-id="083df-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-987">30.00</span><span class="sxs-lookup"><span data-stu-id="083df-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-988">10,00</span><span class="sxs-lookup"><span data-stu-id="083df-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="083df-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="083df-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="083df-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="083df-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="083df-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="083df-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="083df-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="083df-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="083df-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="083df-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="083df-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="083df-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="083df-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



