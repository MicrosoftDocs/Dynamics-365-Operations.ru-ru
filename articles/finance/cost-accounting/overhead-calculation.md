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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976483"
---
# <a name="overhead-calculation"></a><span data-ttu-id="8b22d-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8b22d-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b22d-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="8b22d-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8b22d-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="8b22d-105">Term definition</span></span>
---------------

<span data-ttu-id="8b22d-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="8b22d-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8b22d-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="8b22d-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8b22d-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="8b22d-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8b22d-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="8b22d-109">Rent</span></span>
-   <span data-ttu-id="8b22d-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-110">Electricity</span></span>
-   <span data-ttu-id="8b22d-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="8b22d-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8b22d-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8b22d-112">Overhead calculation overview</span></span>
<span data-ttu-id="8b22d-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="8b22d-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8b22d-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="8b22d-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8b22d-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="8b22d-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8b22d-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="8b22d-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8b22d-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="8b22d-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8b22d-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="8b22d-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8b22d-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="8b22d-119">Version type</span></span>
-   <span data-ttu-id="8b22d-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="8b22d-120">Date and time</span></span>
-   <span data-ttu-id="8b22d-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8b22d-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="8b22d-122">Fiscal year</span></span>
-   <span data-ttu-id="8b22d-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="8b22d-123">Fiscal period</span></span>

<span data-ttu-id="8b22d-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="8b22d-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8b22d-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="8b22d-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8b22d-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8b22d-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8b22d-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="8b22d-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8b22d-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="8b22d-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8b22d-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="8b22d-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8b22d-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="8b22d-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8b22d-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8b22d-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8b22d-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="8b22d-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8b22d-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="8b22d-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8b22d-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8b22d-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8b22d-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="8b22d-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8b22d-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8b22d-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="8b22d-140">Main account</span></span></th>
<th><span data-ttu-id="8b22d-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="8b22d-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8b22d-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-143">CC099</span></span></td>
<td><span data-ttu-id="8b22d-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-144">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-145">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-145">10001</span></span></td>
<td><span data-ttu-id="8b22d-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-146">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8b22d-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8b22d-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8b22d-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="8b22d-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8b22d-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8b22d-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="8b22d-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8b22d-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="8b22d-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8b22d-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="8b22d-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8b22d-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="8b22d-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8b22d-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8b22d-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8b22d-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8b22d-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-160">Journal</span></span></th>
<th><span data-ttu-id="8b22d-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8b22d-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8b22d-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8b22d-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8b22d-163">Версия</span><span class="sxs-lookup"><span data-stu-id="8b22d-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-164">00001</span><span class="sxs-lookup"><span data-stu-id="8b22d-164">00001</span></span></td>
<td><span data-ttu-id="8b22d-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8b22d-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8b22d-166">Fiscal</span></span></td>
<td><span data-ttu-id="8b22d-167">2017</span><span class="sxs-lookup"><span data-stu-id="8b22d-167">2017</span></span></td>
<td><span data-ttu-id="8b22d-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-168">Period 1</span></span></td>
<td><span data-ttu-id="8b22d-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8b22d-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="8b22d-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-173">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8b22d-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-177">CC099</span></span></td>
<td><span data-ttu-id="8b22d-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-178">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-179">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-179">10001</span></span></td>
<td><span data-ttu-id="8b22d-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-180">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8b22d-181">Unclassified</span></span></td>
<td><span data-ttu-id="8b22d-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8b22d-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-185">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-187">Amount</span></span></th>
<th><span data-ttu-id="8b22d-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-189">CC099</span></span></td>
<td><span data-ttu-id="8b22d-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-190">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-191">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-191">10001</span></span></td>
<td><span data-ttu-id="8b22d-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-192">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8b22d-193">Unclassified</span></span></td>
<td><span data-ttu-id="8b22d-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-194">10,000.00</span></span></td>
<td><span data-ttu-id="8b22d-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-196">CC099</span></span></td>
<td><span data-ttu-id="8b22d-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-197">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-198">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-198">10001</span></span></td>
<td><span data-ttu-id="8b22d-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-199">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8b22d-200">Unclassified</span></span></td>
<td><span data-ttu-id="8b22d-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8b22d-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-203">CC099</span></span></td>
<td><span data-ttu-id="8b22d-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-204">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-205">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-205">10001</span></span></td>
<td><span data-ttu-id="8b22d-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-206">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-208">1,000.00</span></span></td>
<td><span data-ttu-id="8b22d-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-210">CC099</span></span></td>
<td><span data-ttu-id="8b22d-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-211">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-212">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-212">10001</span></span></td>
<td><span data-ttu-id="8b22d-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-213">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-214">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-215">9,000.00</span></span></td>
<td><span data-ttu-id="8b22d-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="8b22d-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8b22d-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8b22d-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8b22d-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8b22d-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-221">Define the cost distribution rule</span></span>

<span data-ttu-id="8b22d-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="8b22d-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8b22d-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="8b22d-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8b22d-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="8b22d-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8b22d-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="8b22d-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8b22d-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="8b22d-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8b22d-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-228">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="8b22d-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-230">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-230">CC001</span></span></td>
<td><span data-ttu-id="8b22d-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-231">HR</span></span></td>
<td><span data-ttu-id="8b22d-232">1000</span><span class="sxs-lookup"><span data-stu-id="8b22d-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-233">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-233">CC002</span></span></td>
<td><span data-ttu-id="8b22d-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-234">Finance</span></span></td>
<td><span data-ttu-id="8b22d-235">6,000</span><span class="sxs-lookup"><span data-stu-id="8b22d-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-236">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-236">CC003</span></span></td>
<td><span data-ttu-id="8b22d-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-237">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-238">0</span><span class="sxs-lookup"><span data-stu-id="8b22d-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-240">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-241">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-241">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-242">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-244">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-244">CC001</span></span></td>
<td><span data-ttu-id="8b22d-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-245">HR</span></span></td>
<td><span data-ttu-id="8b22d-246">1000</span><span class="sxs-lookup"><span data-stu-id="8b22d-246">1,000</span></span></td>
<td><span data-ttu-id="8b22d-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8b22d-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8b22d-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-249">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-249">CC002</span></span></td>
<td><span data-ttu-id="8b22d-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-250">Finance</span></span></td>
<td><span data-ttu-id="8b22d-251">6,000</span><span class="sxs-lookup"><span data-stu-id="8b22d-251">6,000</span></span></td>
<td><span data-ttu-id="8b22d-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8b22d-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8b22d-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-254">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-254">CC003</span></span></td>
<td><span data-ttu-id="8b22d-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-255">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-256">0</span><span class="sxs-lookup"><span data-stu-id="8b22d-256">0</span></span></td>
<td><span data-ttu-id="8b22d-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8b22d-258">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="8b22d-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8b22d-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-261">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-262">Формула</span><span class="sxs-lookup"><span data-stu-id="8b22d-262">Formula</span></span></th>
<th><span data-ttu-id="8b22d-263">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-263">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-264">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-266">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-266">CC001</span></span></td>
<td><span data-ttu-id="8b22d-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-267">HR</span></span></td>
<td><span data-ttu-id="8b22d-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8b22d-269">1</span><span class="sxs-lookup"><span data-stu-id="8b22d-269">1</span></span></td>
<td><span data-ttu-id="8b22d-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8b22d-271">500.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-272">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-272">CC002</span></span></td>
<td><span data-ttu-id="8b22d-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-273">Finance</span></span></td>
<td><span data-ttu-id="8b22d-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8b22d-275">1</span><span class="sxs-lookup"><span data-stu-id="8b22d-275">1</span></span></td>
<td><span data-ttu-id="8b22d-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8b22d-277">500.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-278">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-278">CC003</span></span></td>
<td><span data-ttu-id="8b22d-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-279">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8b22d-281">0</span><span class="sxs-lookup"><span data-stu-id="8b22d-281">0</span></span></td>
<td><span data-ttu-id="8b22d-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8b22d-283">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8b22d-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-285">Journal</span></span></th>
<th><span data-ttu-id="8b22d-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8b22d-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8b22d-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8b22d-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8b22d-288">Версия</span><span class="sxs-lookup"><span data-stu-id="8b22d-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-289">00002</span><span class="sxs-lookup"><span data-stu-id="8b22d-289">00002</span></span></td>
<td><span data-ttu-id="8b22d-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8b22d-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8b22d-291">Fiscal</span></span></td>
<td><span data-ttu-id="8b22d-292">2017</span><span class="sxs-lookup"><span data-stu-id="8b22d-292">2017</span></span></td>
<td><span data-ttu-id="8b22d-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-293">Period 1</span></span></td>
<td><span data-ttu-id="8b22d-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8b22d-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="8b22d-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-298">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-299">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-302">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-302">CC099</span></span></td>
<td><span data-ttu-id="8b22d-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-303">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-304">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-304">10001</span></span></td>
<td><span data-ttu-id="8b22d-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-305">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-306">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-309">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-309">CC099</span></span></td>
<td><span data-ttu-id="8b22d-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-310">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-311">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-311">10001</span></span></td>
<td><span data-ttu-id="8b22d-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-312">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-313">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8b22d-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-317">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-318">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-319">Amount</span></span></th>
<th><span data-ttu-id="8b22d-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-321">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-321">CC099</span></span></td>
<td><span data-ttu-id="8b22d-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-322">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-323">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-323">10001</span></span></td>
<td><span data-ttu-id="8b22d-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-324">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-325">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-326">-1,000.00</span></span></td>
<td><span data-ttu-id="8b22d-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-328">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-328">CC001</span></span></td>
<td><span data-ttu-id="8b22d-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-329">HR</span></span></td>
<td><span data-ttu-id="8b22d-330">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-330">10001</span></span></td>
<td><span data-ttu-id="8b22d-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-331">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-332">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-333">500.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-333">500.00</span></span></td>
<td><span data-ttu-id="8b22d-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-335">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-335">CC002</span></span></td>
<td><span data-ttu-id="8b22d-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-336">Finance</span></span></td>
<td><span data-ttu-id="8b22d-337">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-337">10001</span></span></td>
<td><span data-ttu-id="8b22d-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-338">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-339">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-340">500.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-340">500.00</span></span></td>
<td><span data-ttu-id="8b22d-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-342">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-342">CC099</span></span></td>
<td><span data-ttu-id="8b22d-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b22d-343">Default cost center</span></span></td>
<td><span data-ttu-id="8b22d-344">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-344">10001</span></span></td>
<td><span data-ttu-id="8b22d-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-345">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-346">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-347">-9,000.00</span></span></td>
<td><span data-ttu-id="8b22d-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-349">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-349">CC001</span></span></td>
<td><span data-ttu-id="8b22d-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-350">HR</span></span></td>
<td><span data-ttu-id="8b22d-351">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-351">10001</span></span></td>
<td><span data-ttu-id="8b22d-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-352">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-353">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8b22d-354">1,285.71</span></span></td>
<td><span data-ttu-id="8b22d-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-356">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-356">CC002</span></span></td>
<td><span data-ttu-id="8b22d-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-357">Finance</span></span></td>
<td><span data-ttu-id="8b22d-358">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-358">10001</span></span></td>
<td><span data-ttu-id="8b22d-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-359">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-360">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8b22d-361">7,714.29</span></span></td>
<td><span data-ttu-id="8b22d-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="8b22d-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8b22d-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8b22d-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8b22d-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8b22d-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8b22d-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8b22d-367">Define the overhead rate</span></span>

<span data-ttu-id="8b22d-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="8b22d-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8b22d-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8b22d-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-370">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-371">Часы</span><span class="sxs-lookup"><span data-stu-id="8b22d-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-372">Proj 1</span></span></td>
<td><span data-ttu-id="8b22d-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-373">Project 1</span></span></td>
<td><span data-ttu-id="8b22d-374">3</span><span class="sxs-lookup"><span data-stu-id="8b22d-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-375">Proj 2</span></span></td>
<td><span data-ttu-id="8b22d-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-376">Project 2</span></span></td>
<td><span data-ttu-id="8b22d-377">1</span><span class="sxs-lookup"><span data-stu-id="8b22d-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-379">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-380">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-381">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="8b22d-382">Units</span></span></th>
<th><span data-ttu-id="8b22d-383">По норме</span><span class="sxs-lookup"><span data-stu-id="8b22d-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-384">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-384">CC001</span></span></td>
<td><span data-ttu-id="8b22d-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-385">HR</span></span></td>
<td><span data-ttu-id="8b22d-386">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-386">10001</span></span></td>
<td><span data-ttu-id="8b22d-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-387">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-388">1</span><span class="sxs-lookup"><span data-stu-id="8b22d-388">1</span></span></td>
<td><span data-ttu-id="8b22d-389">10</span><span class="sxs-lookup"><span data-stu-id="8b22d-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-391">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-392">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-392">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-393">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-394">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-396">Proj 1</span></span></td>
<td><span data-ttu-id="8b22d-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-397">Project 1</span></span></td>
<td><span data-ttu-id="8b22d-398">3</span><span class="sxs-lookup"><span data-stu-id="8b22d-398">3</span></span></td>
<td><span data-ttu-id="8b22d-399">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-399">10001</span></span></td>
<td><span data-ttu-id="8b22d-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8b22d-401">30.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-402">Proj 2</span></span></td>
<td><span data-ttu-id="8b22d-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-403">Project 2</span></span></td>
<td><span data-ttu-id="8b22d-404">1</span><span class="sxs-lookup"><span data-stu-id="8b22d-404">1</span></span></td>
<td><span data-ttu-id="8b22d-405">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-405">10001</span></span></td>
<td><span data-ttu-id="8b22d-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8b22d-407">10,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8b22d-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-409">Journal</span></span></th>
<th><span data-ttu-id="8b22d-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8b22d-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8b22d-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8b22d-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8b22d-412">Версия</span><span class="sxs-lookup"><span data-stu-id="8b22d-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-413">00003</span><span class="sxs-lookup"><span data-stu-id="8b22d-413">00003</span></span></td>
<td><span data-ttu-id="8b22d-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8b22d-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8b22d-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8b22d-415">Fiscal</span></span></td>
<td><span data-ttu-id="8b22d-416">2017</span><span class="sxs-lookup"><span data-stu-id="8b22d-416">2017</span></span></td>
<td><span data-ttu-id="8b22d-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-417">Period 1</span></span></td>
<td><span data-ttu-id="8b22d-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8b22d-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="8b22d-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-421">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-422">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-424">Proj 1</span></span></td>
<td><span data-ttu-id="8b22d-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8b22d-426">3,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-428">Proj 2</span></span></td>
<td><span data-ttu-id="8b22d-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8b22d-430">1.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8b22d-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-433">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-434">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-435">Amount</span></span></th>
<th><span data-ttu-id="8b22d-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="8b22d-437">CC0001</span></span></td>
<td><span data-ttu-id="8b22d-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-438">HR</span></span></td>
<td><span data-ttu-id="8b22d-439">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-439">10001</span></span></td>
<td><span data-ttu-id="8b22d-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-440">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-441">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-442">-30.00</span></span></td>
<td><span data-ttu-id="8b22d-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-444">Proj 1</span></span></td>
<td><span data-ttu-id="8b22d-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8b22d-446">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-446">10001</span></span></td>
<td><span data-ttu-id="8b22d-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-447">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-448">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-449">30.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-449">30.00</span></span></td>
<td><span data-ttu-id="8b22d-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-451">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-451">CC001</span></span></td>
<td><span data-ttu-id="8b22d-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-452">HR</span></span></td>
<td><span data-ttu-id="8b22d-453">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-453">10001</span></span></td>
<td><span data-ttu-id="8b22d-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-454">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-455">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-456">-10.00</span></span></td>
<td><span data-ttu-id="8b22d-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-458">Proj 2</span></span></td>
<td><span data-ttu-id="8b22d-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8b22d-460">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-460">10001</span></span></td>
<td><span data-ttu-id="8b22d-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-461">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-462">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-463">10.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-463">10.00</span></span></td>
<td><span data-ttu-id="8b22d-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="8b22d-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8b22d-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8b22d-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8b22d-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="8b22d-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="8b22d-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8b22d-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="8b22d-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8b22d-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="8b22d-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8b22d-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="8b22d-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8b22d-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="8b22d-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8b22d-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8b22d-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8b22d-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-475">Define the cost allocation</span></span>

<span data-ttu-id="8b22d-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8b22d-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8b22d-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8b22d-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-479">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-481">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-481">CC002</span></span></td>
<td><span data-ttu-id="8b22d-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-482">Finance</span></span></td>
<td><span data-ttu-id="8b22d-483">35</span><span class="sxs-lookup"><span data-stu-id="8b22d-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-484">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-484">CC003</span></span></td>
<td><span data-ttu-id="8b22d-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-485">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-486">55</span><span class="sxs-lookup"><span data-stu-id="8b22d-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-487">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-487">CC004</span></span></td>
<td><span data-ttu-id="8b22d-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-488">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-489">10</span><span class="sxs-lookup"><span data-stu-id="8b22d-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8b22d-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8b22d-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-492">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="8b22d-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-494">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-494">CC003</span></span></td>
<td><span data-ttu-id="8b22d-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-495">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-496">65</span><span class="sxs-lookup"><span data-stu-id="8b22d-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-497">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-497">CC004</span></span></td>
<td><span data-ttu-id="8b22d-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-498">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-499">35</span><span class="sxs-lookup"><span data-stu-id="8b22d-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8b22d-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8b22d-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-502">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="8b22d-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-504">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-505">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-506">60</span><span class="sxs-lookup"><span data-stu-id="8b22d-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-507">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-508">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-509">20</span><span class="sxs-lookup"><span data-stu-id="8b22d-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8b22d-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8b22d-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-512">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="8b22d-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-514">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-515">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-516">80</span><span class="sxs-lookup"><span data-stu-id="8b22d-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-517">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-518">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-519">15</span><span class="sxs-lookup"><span data-stu-id="8b22d-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8b22d-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="8b22d-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8b22d-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="8b22d-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="8b22d-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8b22d-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-523">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-524">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-524">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-525">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-526">Amount</span></span></th>
<th><span data-ttu-id="8b22d-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-528">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-528">CC002</span></span></td>
<td><span data-ttu-id="8b22d-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-529">Finance</span></span></td>
<td><span data-ttu-id="8b22d-530">35</span><span class="sxs-lookup"><span data-stu-id="8b22d-530">35</span></span></td>
<td><span data-ttu-id="8b22d-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8b22d-532">175.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-532">175.00</span></span></td>
<td><span data-ttu-id="8b22d-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-534">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-534">CC003</span></span></td>
<td><span data-ttu-id="8b22d-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-535">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-536">55</span><span class="sxs-lookup"><span data-stu-id="8b22d-536">55</span></span></td>
<td><span data-ttu-id="8b22d-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8b22d-538">275.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-538">275.00</span></span></td>
<td><span data-ttu-id="8b22d-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-540">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-540">CC004</span></span></td>
<td><span data-ttu-id="8b22d-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-541">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-542">10</span><span class="sxs-lookup"><span data-stu-id="8b22d-542">10</span></span></td>
<td><span data-ttu-id="8b22d-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8b22d-544">50,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-544">50.00</span></span></td>
<td><span data-ttu-id="8b22d-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-546">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-546">CC002</span></span></td>
<td><span data-ttu-id="8b22d-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-547">Finance</span></span></td>
<td><span data-ttu-id="8b22d-548">35</span><span class="sxs-lookup"><span data-stu-id="8b22d-548">35</span></span></td>
<td><span data-ttu-id="8b22d-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8b22d-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8b22d-550">436.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-550">436.00</span></span></td>
<td><span data-ttu-id="8b22d-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-552">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-552">CC003</span></span></td>
<td><span data-ttu-id="8b22d-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-553">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-554">55</span><span class="sxs-lookup"><span data-stu-id="8b22d-554">55</span></span></td>
<td><span data-ttu-id="8b22d-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8b22d-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8b22d-556">685.14</span><span class="sxs-lookup"><span data-stu-id="8b22d-556">685.14</span></span></td>
<td><span data-ttu-id="8b22d-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-558">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-558">CC004</span></span></td>
<td><span data-ttu-id="8b22d-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-559">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-560">10</span><span class="sxs-lookup"><span data-stu-id="8b22d-560">10</span></span></td>
<td><span data-ttu-id="8b22d-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8b22d-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8b22d-562">124.57</span><span class="sxs-lookup"><span data-stu-id="8b22d-562">124.57</span></span></td>
<td><span data-ttu-id="8b22d-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8b22d-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-565">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-566">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-566">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-567">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-568">Amount</span></span></th>
<th><span data-ttu-id="8b22d-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-570">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-570">CC003</span></span></td>
<td><span data-ttu-id="8b22d-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-571">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-572">65</span><span class="sxs-lookup"><span data-stu-id="8b22d-572">65</span></span></td>
<td><span data-ttu-id="8b22d-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8b22d-574">438.75</span><span class="sxs-lookup"><span data-stu-id="8b22d-574">438.75</span></span></td>
<td><span data-ttu-id="8b22d-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-576">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-576">CC004</span></span></td>
<td><span data-ttu-id="8b22d-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-577">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-578">35</span><span class="sxs-lookup"><span data-stu-id="8b22d-578">35</span></span></td>
<td><span data-ttu-id="8b22d-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8b22d-580">236.25</span><span class="sxs-lookup"><span data-stu-id="8b22d-580">236.25</span></span></td>
<td><span data-ttu-id="8b22d-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-582">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-582">CC003</span></span></td>
<td><span data-ttu-id="8b22d-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-583">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-584">65</span><span class="sxs-lookup"><span data-stu-id="8b22d-584">65</span></span></td>
<td><span data-ttu-id="8b22d-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8b22d-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8b22d-586">5,297.69</span></span></td>
<td><span data-ttu-id="8b22d-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-588">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-588">CC004</span></span></td>
<td><span data-ttu-id="8b22d-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-589">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-590">35</span><span class="sxs-lookup"><span data-stu-id="8b22d-590">35</span></span></td>
<td><span data-ttu-id="8b22d-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8b22d-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8b22d-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8b22d-592">2,852.60</span></span></td>
<td><span data-ttu-id="8b22d-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8b22d-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-595">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-596">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-596">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-597">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-598">Amount</span></span></th>
<th><span data-ttu-id="8b22d-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-600">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-601">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-602">60</span><span class="sxs-lookup"><span data-stu-id="8b22d-602">60</span></span></td>
<td><span data-ttu-id="8b22d-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8b22d-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8b22d-604">535.31</span><span class="sxs-lookup"><span data-stu-id="8b22d-604">535.31</span></span></td>
<td><span data-ttu-id="8b22d-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-606">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-607">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-608">20</span><span class="sxs-lookup"><span data-stu-id="8b22d-608">20</span></span></td>
<td><span data-ttu-id="8b22d-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8b22d-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8b22d-610">178.44</span><span class="sxs-lookup"><span data-stu-id="8b22d-610">178.44</span></span></td>
<td><span data-ttu-id="8b22d-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-612">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-613">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-614">60</span><span class="sxs-lookup"><span data-stu-id="8b22d-614">60</span></span></td>
<td><span data-ttu-id="8b22d-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8b22d-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8b22d-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8b22d-616">4,487.12</span></span></td>
<td><span data-ttu-id="8b22d-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-618">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-619">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-620">20</span><span class="sxs-lookup"><span data-stu-id="8b22d-620">20</span></span></td>
<td><span data-ttu-id="8b22d-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8b22d-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8b22d-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8b22d-622">1,495.71</span></span></td>
<td><span data-ttu-id="8b22d-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b22d-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8b22d-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-625">Cost object</span></span></th>
<th><span data-ttu-id="8b22d-626">Величина</span><span class="sxs-lookup"><span data-stu-id="8b22d-626">Magnitude</span></span></th>
<th><span data-ttu-id="8b22d-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8b22d-627">Allocation factor</span></span></th>
<th><span data-ttu-id="8b22d-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-628">Amount</span></span></th>
<th><span data-ttu-id="8b22d-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-630">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-631">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-632">80</span><span class="sxs-lookup"><span data-stu-id="8b22d-632">80</span></span></td>
<td><span data-ttu-id="8b22d-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8b22d-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8b22d-634">241.05</span><span class="sxs-lookup"><span data-stu-id="8b22d-634">241.05</span></span></td>
<td><span data-ttu-id="8b22d-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-636">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-637">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-638">15</span><span class="sxs-lookup"><span data-stu-id="8b22d-638">15</span></span></td>
<td><span data-ttu-id="8b22d-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8b22d-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8b22d-640">45.20</span><span class="sxs-lookup"><span data-stu-id="8b22d-640">45.20</span></span></td>
<td><span data-ttu-id="8b22d-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-642">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-643">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-644">80</span><span class="sxs-lookup"><span data-stu-id="8b22d-644">80</span></span></td>
<td><span data-ttu-id="8b22d-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8b22d-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8b22d-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8b22d-646">2,507.09</span></span></td>
<td><span data-ttu-id="8b22d-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-648">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-649">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-650">15</span><span class="sxs-lookup"><span data-stu-id="8b22d-650">15</span></span></td>
<td><span data-ttu-id="8b22d-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8b22d-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8b22d-652">470.08</span><span class="sxs-lookup"><span data-stu-id="8b22d-652">470.08</span></span></td>
<td><span data-ttu-id="8b22d-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8b22d-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="8b22d-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="8b22d-655">Journal</span></span></th>
<th><span data-ttu-id="8b22d-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8b22d-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8b22d-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8b22d-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8b22d-658">Версия</span><span class="sxs-lookup"><span data-stu-id="8b22d-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-659">00004</span><span class="sxs-lookup"><span data-stu-id="8b22d-659">00004</span></span></td>
<td><span data-ttu-id="8b22d-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8b22d-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8b22d-661">Fiscal</span></span></td>
<td><span data-ttu-id="8b22d-662">2017</span><span class="sxs-lookup"><span data-stu-id="8b22d-662">2017</span></span></td>
<td><span data-ttu-id="8b22d-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-663">Period 1</span></span></td>
<td><span data-ttu-id="8b22d-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8b22d-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="8b22d-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8b22d-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-668">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-669">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-672">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-672">CC001</span></span></td>
<td><span data-ttu-id="8b22d-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-673">HR</span></span></td>
<td><span data-ttu-id="8b22d-674">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-674">10001</span></span></td>
<td><span data-ttu-id="8b22d-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-675">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-676">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-677">500.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-679">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-679">CC001</span></span></td>
<td><span data-ttu-id="8b22d-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-680">HR</span></span></td>
<td><span data-ttu-id="8b22d-681">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-681">10001</span></span></td>
<td><span data-ttu-id="8b22d-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-682">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-683">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8b22d-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-686">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-686">CC002</span></span></td>
<td><span data-ttu-id="8b22d-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-687">Finance</span></span></td>
<td><span data-ttu-id="8b22d-688">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-688">10001</span></span></td>
<td><span data-ttu-id="8b22d-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-689">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-690">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-691">675.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-693">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-693">CC002</span></span></td>
<td><span data-ttu-id="8b22d-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-694">Finance</span></span></td>
<td><span data-ttu-id="8b22d-695">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-695">10001</span></span></td>
<td><span data-ttu-id="8b22d-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-696">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-697">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8b22d-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-700">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-700">CC003</span></span></td>
<td><span data-ttu-id="8b22d-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-701">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-702">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-702">10001</span></span></td>
<td><span data-ttu-id="8b22d-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-703">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-704">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-705">713.75</span><span class="sxs-lookup"><span data-stu-id="8b22d-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-707">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-707">CC003</span></span></td>
<td><span data-ttu-id="8b22d-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-708">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-709">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-709">10001</span></span></td>
<td><span data-ttu-id="8b22d-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-710">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-711">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8b22d-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-714">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-714">CC003</span></span></td>
<td><span data-ttu-id="8b22d-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-715">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-716">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-716">10001</span></span></td>
<td><span data-ttu-id="8b22d-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-717">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-718">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-719">286.25</span><span class="sxs-lookup"><span data-stu-id="8b22d-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-721">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-721">CC003</span></span></td>
<td><span data-ttu-id="8b22d-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-722">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-723">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-723">10001</span></span></td>
<td><span data-ttu-id="8b22d-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-724">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-725">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8b22d-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-728">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-729">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-730">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-730">10001</span></span></td>
<td><span data-ttu-id="8b22d-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-731">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-732">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-733">776.36</span><span class="sxs-lookup"><span data-stu-id="8b22d-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-735">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-736">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-737">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-737">10001</span></span></td>
<td><span data-ttu-id="8b22d-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-738">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-739">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8b22d-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-742">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-743">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-744">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-744">10001</span></span></td>
<td><span data-ttu-id="8b22d-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-745">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-746">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-747">223.64</span><span class="sxs-lookup"><span data-stu-id="8b22d-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="8b22d-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-749">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-750">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-751">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-751">10001</span></span></td>
<td><span data-ttu-id="8b22d-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-752">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-753">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8b22d-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8b22d-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8b22d-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8b22d-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-757">Cost element</span></span></th>
<th><span data-ttu-id="8b22d-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-758">Cost behavior</span></span></th>
<th><span data-ttu-id="8b22d-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8b22d-759">Amount</span></span></th>
<th><span data-ttu-id="8b22d-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8b22d-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b22d-761">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-761">CC001</span></span></td>
<td><span data-ttu-id="8b22d-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-762">HR</span></span></td>
<td><span data-ttu-id="8b22d-763">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-763">10001</span></span></td>
<td><span data-ttu-id="8b22d-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-764">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-765">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-766">-500.00</span></span></td>
<td><span data-ttu-id="8b22d-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-768">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-768">CC002</span></span></td>
<td><span data-ttu-id="8b22d-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-769">Finance</span></span></td>
<td><span data-ttu-id="8b22d-770">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-770">10001</span></span></td>
<td><span data-ttu-id="8b22d-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-771">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-772">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-773">175.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-773">175.00</span></span></td>
<td><span data-ttu-id="8b22d-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-775">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-775">CC003</span></span></td>
<td><span data-ttu-id="8b22d-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-776">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-777">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-777">10001</span></span></td>
<td><span data-ttu-id="8b22d-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-778">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-779">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-780">275.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-780">275.00</span></span></td>
<td><span data-ttu-id="8b22d-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-782">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-782">CC004</span></span></td>
<td><span data-ttu-id="8b22d-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-783">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-784">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-784">10001</span></span></td>
<td><span data-ttu-id="8b22d-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-785">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-786">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-787">50,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-787">50,00</span></span></td>
<td><span data-ttu-id="8b22d-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-789">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-789">CC001</span></span></td>
<td><span data-ttu-id="8b22d-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8b22d-790">HR</span></span></td>
<td><span data-ttu-id="8b22d-791">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-791">10001</span></span></td>
<td><span data-ttu-id="8b22d-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-792">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-793">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="8b22d-794">-1,245.71</span></span></td>
<td><span data-ttu-id="8b22d-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-796">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-796">CC002</span></span></td>
<td><span data-ttu-id="8b22d-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-797">Finance</span></span></td>
<td><span data-ttu-id="8b22d-798">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-798">10001</span></span></td>
<td><span data-ttu-id="8b22d-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-799">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-800">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-801">436.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-801">436.00</span></span></td>
<td><span data-ttu-id="8b22d-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-803">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-803">CC003</span></span></td>
<td><span data-ttu-id="8b22d-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-804">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-805">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-805">10001</span></span></td>
<td><span data-ttu-id="8b22d-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-806">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-807">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-808">685.14</span><span class="sxs-lookup"><span data-stu-id="8b22d-808">685.14</span></span></td>
<td><span data-ttu-id="8b22d-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-810">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-810">CC004</span></span></td>
<td><span data-ttu-id="8b22d-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-811">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-812">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-812">10001</span></span></td>
<td><span data-ttu-id="8b22d-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-813">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-814">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-815">124.57</span><span class="sxs-lookup"><span data-stu-id="8b22d-815">124.57</span></span></td>
<td><span data-ttu-id="8b22d-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-817">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-817">CC002</span></span></td>
<td><span data-ttu-id="8b22d-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-818">Finance</span></span></td>
<td><span data-ttu-id="8b22d-819">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-819">10001</span></span></td>
<td><span data-ttu-id="8b22d-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-820">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-821">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-822">-675.00</span></span></td>
<td><span data-ttu-id="8b22d-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-824">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-824">CC003</span></span></td>
<td><span data-ttu-id="8b22d-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-825">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-826">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-826">10001</span></span></td>
<td><span data-ttu-id="8b22d-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-827">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-828">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-829">438.75</span><span class="sxs-lookup"><span data-stu-id="8b22d-829">438.75</span></span></td>
<td><span data-ttu-id="8b22d-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-831">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-831">CC004</span></span></td>
<td><span data-ttu-id="8b22d-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-832">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-833">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-833">10001</span></span></td>
<td><span data-ttu-id="8b22d-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-834">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-835">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-836">236.25</span><span class="sxs-lookup"><span data-stu-id="8b22d-836">236.25</span></span></td>
<td><span data-ttu-id="8b22d-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-838">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-838">CC002</span></span></td>
<td><span data-ttu-id="8b22d-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="8b22d-839">Finance</span></span></td>
<td><span data-ttu-id="8b22d-840">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-840">10001</span></span></td>
<td><span data-ttu-id="8b22d-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-841">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-842">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="8b22d-843">-8,150.29</span></span></td>
<td><span data-ttu-id="8b22d-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-845">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-845">CC003</span></span></td>
<td><span data-ttu-id="8b22d-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-846">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-847">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-847">10001</span></span></td>
<td><span data-ttu-id="8b22d-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-848">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-849">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8b22d-850">5,297.69</span></span></td>
<td><span data-ttu-id="8b22d-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-852">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-852">CC004</span></span></td>
<td><span data-ttu-id="8b22d-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8b22d-853">Packaging</span></span></td>
<td><span data-ttu-id="8b22d-854">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-854">10001</span></span></td>
<td><span data-ttu-id="8b22d-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-855">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-856">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8b22d-857">2,852.60</span></span></td>
<td><span data-ttu-id="8b22d-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-859">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-859">CC003</span></span></td>
<td><span data-ttu-id="8b22d-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-860">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-861">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-861">10001</span></span></td>
<td><span data-ttu-id="8b22d-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-862">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-863">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="8b22d-864">-713.75</span></span></td>
<td><span data-ttu-id="8b22d-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-866">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-867">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-868">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-868">10001</span></span></td>
<td><span data-ttu-id="8b22d-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-869">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-870">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-871">535.31</span><span class="sxs-lookup"><span data-stu-id="8b22d-871">535.31</span></span></td>
<td><span data-ttu-id="8b22d-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-873">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-874">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-875">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-875">10001</span></span></td>
<td><span data-ttu-id="8b22d-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-876">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-877">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-878">178.44</span><span class="sxs-lookup"><span data-stu-id="8b22d-878">178.44</span></span></td>
<td><span data-ttu-id="8b22d-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-880">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-880">CC003</span></span></td>
<td><span data-ttu-id="8b22d-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-881">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-882">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-882">10001</span></span></td>
<td><span data-ttu-id="8b22d-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-883">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-884">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="8b22d-885">-5,982.83</span></span></td>
<td><span data-ttu-id="8b22d-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-887">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-888">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-889">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-889">10001</span></span></td>
<td><span data-ttu-id="8b22d-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-890">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-891">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8b22d-892">4,487.12</span></span></td>
<td><span data-ttu-id="8b22d-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-894">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-895">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-896">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-896">10001</span></span></td>
<td><span data-ttu-id="8b22d-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-897">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-898">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8b22d-899">1,495.71</span></span></td>
<td><span data-ttu-id="8b22d-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-901">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-901">CC003</span></span></td>
<td><span data-ttu-id="8b22d-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-902">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-903">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-903">10001</span></span></td>
<td><span data-ttu-id="8b22d-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-904">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-905">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="8b22d-906">-286.25</span></span></td>
<td><span data-ttu-id="8b22d-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-908">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-909">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-910">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-910">10001</span></span></td>
<td><span data-ttu-id="8b22d-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-911">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-912">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-913">241.05</span><span class="sxs-lookup"><span data-stu-id="8b22d-913">241.05</span></span></td>
<td><span data-ttu-id="8b22d-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-915">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-916">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-917">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-917">10001</span></span></td>
<td><span data-ttu-id="8b22d-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-918">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-919">Fixed cost</span></span></td>
<td><span data-ttu-id="8b22d-920">45.20</span><span class="sxs-lookup"><span data-stu-id="8b22d-920">45.20</span></span></td>
<td><span data-ttu-id="8b22d-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-922">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-922">CC003</span></span></td>
<td><span data-ttu-id="8b22d-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="8b22d-923">Assembly</span></span></td>
<td><span data-ttu-id="8b22d-924">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-924">10001</span></span></td>
<td><span data-ttu-id="8b22d-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-925">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-926">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="8b22d-927">-2,977.17</span></span></td>
<td><span data-ttu-id="8b22d-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-929">Prod 1</span></span></td>
<td><span data-ttu-id="8b22d-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-930">Product 1</span></span></td>
<td><span data-ttu-id="8b22d-931">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-931">10001</span></span></td>
<td><span data-ttu-id="8b22d-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-932">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-933">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8b22d-934">2,507.09</span></span></td>
<td><span data-ttu-id="8b22d-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b22d-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-936">Prod 2</span></span></td>
<td><span data-ttu-id="8b22d-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-937">Product 2</span></span></td>
<td><span data-ttu-id="8b22d-938">10001</span><span class="sxs-lookup"><span data-stu-id="8b22d-938">10001</span></span></td>
<td><span data-ttu-id="8b22d-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-939">Electricity</span></span></td>
<td><span data-ttu-id="8b22d-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-940">Variable cost</span></span></td>
<td><span data-ttu-id="8b22d-941">470.08</span><span class="sxs-lookup"><span data-stu-id="8b22d-941">470.08</span></span></td>
<td><span data-ttu-id="8b22d-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8b22d-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8b22d-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="8b22d-943">Conclusion</span></span>
<span data-ttu-id="8b22d-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8b22d-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="8b22d-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8b22d-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="8b22d-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8b22d-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8b22d-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8b22d-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8b22d-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8b22d-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="8b22d-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8b22d-951">CC099</span><span class="sxs-lookup"><span data-stu-id="8b22d-951">CC099</span></span></th>
<th><span data-ttu-id="8b22d-952">CC001</span><span class="sxs-lookup"><span data-stu-id="8b22d-952">CC001</span></span></th>
<th><span data-ttu-id="8b22d-953">CC002</span><span class="sxs-lookup"><span data-stu-id="8b22d-953">CC002</span></span></th>
<th><span data-ttu-id="8b22d-954">CC003</span><span class="sxs-lookup"><span data-stu-id="8b22d-954">CC003</span></span></th>
<th><span data-ttu-id="8b22d-955">CC004</span><span class="sxs-lookup"><span data-stu-id="8b22d-955">CC004</span></span></th>
<th><span data-ttu-id="8b22d-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-956">Proj 1</span></span></th>
<th><span data-ttu-id="8b22d-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-957">Proj 2</span></span></th>
<th><span data-ttu-id="8b22d-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8b22d-958">Prod 1</span></span></th>
<th><span data-ttu-id="8b22d-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8b22d-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8b22d-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="8b22d-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8b22d-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8b22d-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-971">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8b22d-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-973">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-975">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-978">776.36</span><span class="sxs-lookup"><span data-stu-id="8b22d-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-979">223.64</span><span class="sxs-lookup"><span data-stu-id="8b22d-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8b22d-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8b22d-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-982">000</span><span class="sxs-lookup"><span data-stu-id="8b22d-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-983">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-984">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-985">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-987">30.00</span><span class="sxs-lookup"><span data-stu-id="8b22d-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-988">10,00</span><span class="sxs-lookup"><span data-stu-id="8b22d-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8b22d-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8b22d-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8b22d-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8b22d-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8b22d-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8b22d-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="8b22d-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8b22d-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="8b22d-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8b22d-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="8b22d-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8b22d-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="8b22d-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



