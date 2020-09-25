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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759480"
---
# <a name="overhead-calculation"></a><span data-ttu-id="059ff-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="059ff-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="059ff-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="059ff-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="059ff-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="059ff-105">Term definition</span></span>
---------------

<span data-ttu-id="059ff-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="059ff-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="059ff-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="059ff-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="059ff-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="059ff-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="059ff-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="059ff-109">Rent</span></span>
-   <span data-ttu-id="059ff-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-110">Electricity</span></span>
-   <span data-ttu-id="059ff-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="059ff-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="059ff-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="059ff-112">Overhead calculation overview</span></span>
<span data-ttu-id="059ff-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="059ff-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="059ff-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="059ff-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="059ff-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="059ff-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="059ff-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="059ff-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="059ff-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="059ff-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="059ff-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="059ff-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="059ff-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="059ff-119">Version type</span></span>
-   <span data-ttu-id="059ff-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="059ff-120">Date and time</span></span>
-   <span data-ttu-id="059ff-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="059ff-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="059ff-122">Fiscal year</span></span>
-   <span data-ttu-id="059ff-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="059ff-123">Fiscal period</span></span>

<span data-ttu-id="059ff-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="059ff-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="059ff-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="059ff-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="059ff-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="059ff-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="059ff-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="059ff-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="059ff-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="059ff-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="059ff-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="059ff-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="059ff-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="059ff-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="059ff-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="059ff-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="059ff-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="059ff-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="059ff-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="059ff-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="059ff-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="059ff-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="059ff-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="059ff-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="059ff-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="059ff-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="059ff-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="059ff-140">Main account</span></span></th>
<th><span data-ttu-id="059ff-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="059ff-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="059ff-143">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-143">CC099</span></span></td>
<td><span data-ttu-id="059ff-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-144">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-145">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-145">10001</span></span></td>
<td><span data-ttu-id="059ff-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-146">Electricity</span></span></td>
<td><span data-ttu-id="059ff-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="059ff-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="059ff-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="059ff-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="059ff-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="059ff-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="059ff-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-151">Define the cost behavior rule</span></span>

<span data-ttu-id="059ff-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="059ff-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="059ff-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="059ff-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="059ff-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="059ff-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="059ff-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="059ff-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="059ff-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="059ff-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="059ff-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="059ff-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-160">Journal</span></span></th>
<th><span data-ttu-id="059ff-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="059ff-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="059ff-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="059ff-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="059ff-163">Версия</span><span class="sxs-lookup"><span data-stu-id="059ff-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-164">00001</span><span class="sxs-lookup"><span data-stu-id="059ff-164">00001</span></span></td>
<td><span data-ttu-id="059ff-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="059ff-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="059ff-166">Fiscal</span></span></td>
<td><span data-ttu-id="059ff-167">2017</span><span class="sxs-lookup"><span data-stu-id="059ff-167">2017</span></span></td>
<td><span data-ttu-id="059ff-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-168">Period 1</span></span></td>
<td><span data-ttu-id="059ff-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="059ff-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="059ff-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-173">Cost element</span></span></th>
<th><span data-ttu-id="059ff-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-174">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="059ff-177">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-177">CC099</span></span></td>
<td><span data-ttu-id="059ff-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-178">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-179">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-179">10001</span></span></td>
<td><span data-ttu-id="059ff-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-180">Electricity</span></span></td>
<td><span data-ttu-id="059ff-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="059ff-181">Unclassified</span></span></td>
<td><span data-ttu-id="059ff-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="059ff-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="059ff-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-185">Cost element</span></span></th>
<th><span data-ttu-id="059ff-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-186">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-187">Amount</span></span></th>
<th><span data-ttu-id="059ff-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-189">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-189">CC099</span></span></td>
<td><span data-ttu-id="059ff-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-190">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-191">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-191">10001</span></span></td>
<td><span data-ttu-id="059ff-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-192">Electricity</span></span></td>
<td><span data-ttu-id="059ff-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="059ff-193">Unclassified</span></span></td>
<td><span data-ttu-id="059ff-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="059ff-194">10,000.00</span></span></td>
<td><span data-ttu-id="059ff-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-196">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-196">CC099</span></span></td>
<td><span data-ttu-id="059ff-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-197">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-198">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-198">10001</span></span></td>
<td><span data-ttu-id="059ff-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-199">Electricity</span></span></td>
<td><span data-ttu-id="059ff-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="059ff-200">Unclassified</span></span></td>
<td><span data-ttu-id="059ff-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-201">-10,000.00</span></span></td>
<td><span data-ttu-id="059ff-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-203">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-203">CC099</span></span></td>
<td><span data-ttu-id="059ff-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-204">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-205">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-205">10001</span></span></td>
<td><span data-ttu-id="059ff-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-206">Electricity</span></span></td>
<td><span data-ttu-id="059ff-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-207">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-208">1,000.00</span></span></td>
<td><span data-ttu-id="059ff-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-210">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-210">CC099</span></span></td>
<td><span data-ttu-id="059ff-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-211">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-212">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-212">10001</span></span></td>
<td><span data-ttu-id="059ff-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-213">Electricity</span></span></td>
<td><span data-ttu-id="059ff-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-214">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="059ff-215">9,000.00</span></span></td>
<td><span data-ttu-id="059ff-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="059ff-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="059ff-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="059ff-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="059ff-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="059ff-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-221">Define the cost distribution rule</span></span>

<span data-ttu-id="059ff-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="059ff-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="059ff-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="059ff-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="059ff-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="059ff-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="059ff-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="059ff-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="059ff-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="059ff-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="059ff-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-228">Cost object</span></span></th>
<th><span data-ttu-id="059ff-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="059ff-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-230">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-230">CC001</span></span></td>
<td><span data-ttu-id="059ff-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-231">HR</span></span></td>
<td><span data-ttu-id="059ff-232">1000</span><span class="sxs-lookup"><span data-stu-id="059ff-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-233">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-233">CC002</span></span></td>
<td><span data-ttu-id="059ff-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-234">Finance</span></span></td>
<td><span data-ttu-id="059ff-235">6,000</span><span class="sxs-lookup"><span data-stu-id="059ff-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-236">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-236">CC003</span></span></td>
<td><span data-ttu-id="059ff-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-237">Assembly</span></span></td>
<td><span data-ttu-id="059ff-238">0</span><span class="sxs-lookup"><span data-stu-id="059ff-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-240">Cost object</span></span></th>
<th><span data-ttu-id="059ff-241">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-241">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-242">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-244">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-244">CC001</span></span></td>
<td><span data-ttu-id="059ff-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-245">HR</span></span></td>
<td><span data-ttu-id="059ff-246">1000</span><span class="sxs-lookup"><span data-stu-id="059ff-246">1,000</span></span></td>
<td><span data-ttu-id="059ff-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="059ff-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="059ff-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-249">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-249">CC002</span></span></td>
<td><span data-ttu-id="059ff-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-250">Finance</span></span></td>
<td><span data-ttu-id="059ff-251">6,000</span><span class="sxs-lookup"><span data-stu-id="059ff-251">6,000</span></span></td>
<td><span data-ttu-id="059ff-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="059ff-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="059ff-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-254">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-254">CC003</span></span></td>
<td><span data-ttu-id="059ff-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-255">Assembly</span></span></td>
<td><span data-ttu-id="059ff-256">0</span><span class="sxs-lookup"><span data-stu-id="059ff-256">0</span></span></td>
<td><span data-ttu-id="059ff-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="059ff-258">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="059ff-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="059ff-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-261">Cost object</span></span></th>
<th><span data-ttu-id="059ff-262">Формула</span><span class="sxs-lookup"><span data-stu-id="059ff-262">Formula</span></span></th>
<th><span data-ttu-id="059ff-263">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-263">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-264">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-266">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-266">CC001</span></span></td>
<td><span data-ttu-id="059ff-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-267">HR</span></span></td>
<td><span data-ttu-id="059ff-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="059ff-269">1</span><span class="sxs-lookup"><span data-stu-id="059ff-269">1</span></span></td>
<td><span data-ttu-id="059ff-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="059ff-271">500.00</span><span class="sxs-lookup"><span data-stu-id="059ff-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-272">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-272">CC002</span></span></td>
<td><span data-ttu-id="059ff-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-273">Finance</span></span></td>
<td><span data-ttu-id="059ff-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="059ff-275">1</span><span class="sxs-lookup"><span data-stu-id="059ff-275">1</span></span></td>
<td><span data-ttu-id="059ff-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="059ff-277">500.00</span><span class="sxs-lookup"><span data-stu-id="059ff-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-278">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-278">CC003</span></span></td>
<td><span data-ttu-id="059ff-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-279">Assembly</span></span></td>
<td><span data-ttu-id="059ff-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="059ff-281">0</span><span class="sxs-lookup"><span data-stu-id="059ff-281">0</span></span></td>
<td><span data-ttu-id="059ff-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="059ff-283">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="059ff-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-285">Journal</span></span></th>
<th><span data-ttu-id="059ff-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="059ff-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="059ff-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="059ff-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="059ff-288">Версия</span><span class="sxs-lookup"><span data-stu-id="059ff-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-289">00002</span><span class="sxs-lookup"><span data-stu-id="059ff-289">00002</span></span></td>
<td><span data-ttu-id="059ff-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="059ff-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="059ff-291">Fiscal</span></span></td>
<td><span data-ttu-id="059ff-292">2017</span><span class="sxs-lookup"><span data-stu-id="059ff-292">2017</span></span></td>
<td><span data-ttu-id="059ff-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-293">Period 1</span></span></td>
<td><span data-ttu-id="059ff-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="059ff-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="059ff-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-298">Cost element</span></span></th>
<th><span data-ttu-id="059ff-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-299">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-302">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-302">CC099</span></span></td>
<td><span data-ttu-id="059ff-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-303">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-304">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-304">10001</span></span></td>
<td><span data-ttu-id="059ff-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-305">Electricity</span></span></td>
<td><span data-ttu-id="059ff-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-306">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-309">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-309">CC099</span></span></td>
<td><span data-ttu-id="059ff-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-310">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-311">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-311">10001</span></span></td>
<td><span data-ttu-id="059ff-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-312">Electricity</span></span></td>
<td><span data-ttu-id="059ff-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-313">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="059ff-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="059ff-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-317">Cost element</span></span></th>
<th><span data-ttu-id="059ff-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-318">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-319">Amount</span></span></th>
<th><span data-ttu-id="059ff-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-321">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-321">CC099</span></span></td>
<td><span data-ttu-id="059ff-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-322">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-323">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-323">10001</span></span></td>
<td><span data-ttu-id="059ff-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-324">Electricity</span></span></td>
<td><span data-ttu-id="059ff-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-325">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-326">-1,000.00</span></span></td>
<td><span data-ttu-id="059ff-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-328">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-328">CC001</span></span></td>
<td><span data-ttu-id="059ff-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-329">HR</span></span></td>
<td><span data-ttu-id="059ff-330">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-330">10001</span></span></td>
<td><span data-ttu-id="059ff-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-331">Electricity</span></span></td>
<td><span data-ttu-id="059ff-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-332">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-333">500.00</span><span class="sxs-lookup"><span data-stu-id="059ff-333">500.00</span></span></td>
<td><span data-ttu-id="059ff-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-335">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-335">CC002</span></span></td>
<td><span data-ttu-id="059ff-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-336">Finance</span></span></td>
<td><span data-ttu-id="059ff-337">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-337">10001</span></span></td>
<td><span data-ttu-id="059ff-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-338">Electricity</span></span></td>
<td><span data-ttu-id="059ff-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-339">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-340">500.00</span><span class="sxs-lookup"><span data-stu-id="059ff-340">500.00</span></span></td>
<td><span data-ttu-id="059ff-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-342">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-342">CC099</span></span></td>
<td><span data-ttu-id="059ff-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="059ff-343">Default cost center</span></span></td>
<td><span data-ttu-id="059ff-344">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-344">10001</span></span></td>
<td><span data-ttu-id="059ff-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-345">Electricity</span></span></td>
<td><span data-ttu-id="059ff-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-346">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="059ff-347">-9,000.00</span></span></td>
<td><span data-ttu-id="059ff-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-349">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-349">CC001</span></span></td>
<td><span data-ttu-id="059ff-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-350">HR</span></span></td>
<td><span data-ttu-id="059ff-351">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-351">10001</span></span></td>
<td><span data-ttu-id="059ff-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-352">Electricity</span></span></td>
<td><span data-ttu-id="059ff-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-353">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="059ff-354">1,285.71</span></span></td>
<td><span data-ttu-id="059ff-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-356">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-356">CC002</span></span></td>
<td><span data-ttu-id="059ff-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-357">Finance</span></span></td>
<td><span data-ttu-id="059ff-358">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-358">10001</span></span></td>
<td><span data-ttu-id="059ff-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-359">Electricity</span></span></td>
<td><span data-ttu-id="059ff-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-360">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="059ff-361">7,714.29</span></span></td>
<td><span data-ttu-id="059ff-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="059ff-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="059ff-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="059ff-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="059ff-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="059ff-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="059ff-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="059ff-367">Define the overhead rate</span></span>

<span data-ttu-id="059ff-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="059ff-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="059ff-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="059ff-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-370">Cost object</span></span></th>
<th><span data-ttu-id="059ff-371">Часы</span><span class="sxs-lookup"><span data-stu-id="059ff-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-372">Proj 1</span></span></td>
<td><span data-ttu-id="059ff-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-373">Project 1</span></span></td>
<td><span data-ttu-id="059ff-374">3</span><span class="sxs-lookup"><span data-stu-id="059ff-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-375">Proj 2</span></span></td>
<td><span data-ttu-id="059ff-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-376">Project 2</span></span></td>
<td><span data-ttu-id="059ff-377">1</span><span class="sxs-lookup"><span data-stu-id="059ff-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-379">Cost object</span></span></th>
<th><span data-ttu-id="059ff-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-380">Cost element</span></span></th>
<th><span data-ttu-id="059ff-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-381">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="059ff-382">Units</span></span></th>
<th><span data-ttu-id="059ff-383">По норме</span><span class="sxs-lookup"><span data-stu-id="059ff-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-384">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-384">CC001</span></span></td>
<td><span data-ttu-id="059ff-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-385">HR</span></span></td>
<td><span data-ttu-id="059ff-386">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-386">10001</span></span></td>
<td><span data-ttu-id="059ff-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-387">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-388">1</span><span class="sxs-lookup"><span data-stu-id="059ff-388">1</span></span></td>
<td><span data-ttu-id="059ff-389">10</span><span class="sxs-lookup"><span data-stu-id="059ff-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-391">Cost object</span></span></th>
<th><span data-ttu-id="059ff-392">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-392">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-393">Cost element</span></span></th>
<th><span data-ttu-id="059ff-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-394">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-396">Proj 1</span></span></td>
<td><span data-ttu-id="059ff-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-397">Project 1</span></span></td>
<td><span data-ttu-id="059ff-398">3</span><span class="sxs-lookup"><span data-stu-id="059ff-398">3</span></span></td>
<td><span data-ttu-id="059ff-399">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-399">10001</span></span></td>
<td><span data-ttu-id="059ff-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="059ff-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="059ff-401">30.00</span><span class="sxs-lookup"><span data-stu-id="059ff-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-402">Proj 2</span></span></td>
<td><span data-ttu-id="059ff-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-403">Project 2</span></span></td>
<td><span data-ttu-id="059ff-404">1</span><span class="sxs-lookup"><span data-stu-id="059ff-404">1</span></span></td>
<td><span data-ttu-id="059ff-405">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-405">10001</span></span></td>
<td><span data-ttu-id="059ff-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="059ff-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="059ff-407">10,00</span><span class="sxs-lookup"><span data-stu-id="059ff-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="059ff-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-409">Journal</span></span></th>
<th><span data-ttu-id="059ff-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="059ff-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="059ff-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="059ff-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="059ff-412">Версия</span><span class="sxs-lookup"><span data-stu-id="059ff-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-413">00003</span><span class="sxs-lookup"><span data-stu-id="059ff-413">00003</span></span></td>
<td><span data-ttu-id="059ff-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="059ff-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="059ff-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="059ff-415">Fiscal</span></span></td>
<td><span data-ttu-id="059ff-416">2017</span><span class="sxs-lookup"><span data-stu-id="059ff-416">2017</span></span></td>
<td><span data-ttu-id="059ff-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-417">Period 1</span></span></td>
<td><span data-ttu-id="059ff-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="059ff-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="059ff-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-421">Cost object</span></span></th>
<th><span data-ttu-id="059ff-422">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-424">Proj 1</span></span></td>
<td><span data-ttu-id="059ff-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="059ff-426">3,00</span><span class="sxs-lookup"><span data-stu-id="059ff-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-428">Proj 2</span></span></td>
<td><span data-ttu-id="059ff-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="059ff-430">1.00</span><span class="sxs-lookup"><span data-stu-id="059ff-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="059ff-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-433">Cost element</span></span></th>
<th><span data-ttu-id="059ff-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-434">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-435">Amount</span></span></th>
<th><span data-ttu-id="059ff-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="059ff-437">CC0001</span></span></td>
<td><span data-ttu-id="059ff-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-438">HR</span></span></td>
<td><span data-ttu-id="059ff-439">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-439">10001</span></span></td>
<td><span data-ttu-id="059ff-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-440">Electricity</span></span></td>
<td><span data-ttu-id="059ff-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-441">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="059ff-442">-30.00</span></span></td>
<td><span data-ttu-id="059ff-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-444">Proj 1</span></span></td>
<td><span data-ttu-id="059ff-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="059ff-446">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-446">10001</span></span></td>
<td><span data-ttu-id="059ff-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-447">Electricity</span></span></td>
<td><span data-ttu-id="059ff-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-448">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-449">30.00</span><span class="sxs-lookup"><span data-stu-id="059ff-449">30.00</span></span></td>
<td><span data-ttu-id="059ff-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-451">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-451">CC001</span></span></td>
<td><span data-ttu-id="059ff-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-452">HR</span></span></td>
<td><span data-ttu-id="059ff-453">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-453">10001</span></span></td>
<td><span data-ttu-id="059ff-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-454">Electricity</span></span></td>
<td><span data-ttu-id="059ff-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-455">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="059ff-456">-10.00</span></span></td>
<td><span data-ttu-id="059ff-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-458">Proj 2</span></span></td>
<td><span data-ttu-id="059ff-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="059ff-460">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-460">10001</span></span></td>
<td><span data-ttu-id="059ff-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-461">Electricity</span></span></td>
<td><span data-ttu-id="059ff-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-462">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-463">10.00</span><span class="sxs-lookup"><span data-stu-id="059ff-463">10.00</span></span></td>
<td><span data-ttu-id="059ff-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="059ff-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="059ff-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="059ff-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="059ff-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="059ff-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="059ff-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="059ff-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="059ff-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="059ff-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="059ff-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="059ff-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="059ff-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="059ff-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="059ff-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="059ff-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="059ff-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="059ff-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-475">Define the cost allocation</span></span>

<span data-ttu-id="059ff-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="059ff-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="059ff-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="059ff-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-479">Cost object</span></span></th>
<th><span data-ttu-id="059ff-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-481">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-481">CC002</span></span></td>
<td><span data-ttu-id="059ff-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-482">Finance</span></span></td>
<td><span data-ttu-id="059ff-483">35</span><span class="sxs-lookup"><span data-stu-id="059ff-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-484">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-484">CC003</span></span></td>
<td><span data-ttu-id="059ff-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-485">Assembly</span></span></td>
<td><span data-ttu-id="059ff-486">55</span><span class="sxs-lookup"><span data-stu-id="059ff-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-487">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-487">CC004</span></span></td>
<td><span data-ttu-id="059ff-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-488">Packaging</span></span></td>
<td><span data-ttu-id="059ff-489">10</span><span class="sxs-lookup"><span data-stu-id="059ff-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="059ff-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="059ff-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-492">Cost object</span></span></th>
<th><span data-ttu-id="059ff-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="059ff-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-494">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-494">CC003</span></span></td>
<td><span data-ttu-id="059ff-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-495">Assembly</span></span></td>
<td><span data-ttu-id="059ff-496">65</span><span class="sxs-lookup"><span data-stu-id="059ff-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-497">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-497">CC004</span></span></td>
<td><span data-ttu-id="059ff-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-498">Packaging</span></span></td>
<td><span data-ttu-id="059ff-499">35</span><span class="sxs-lookup"><span data-stu-id="059ff-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="059ff-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="059ff-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-502">Cost object</span></span></th>
<th><span data-ttu-id="059ff-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="059ff-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-504">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-505">Product 1</span></span></td>
<td><span data-ttu-id="059ff-506">60</span><span class="sxs-lookup"><span data-stu-id="059ff-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-507">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-508">Product 2</span></span></td>
<td><span data-ttu-id="059ff-509">20</span><span class="sxs-lookup"><span data-stu-id="059ff-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="059ff-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="059ff-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-512">Cost object</span></span></th>
<th><span data-ttu-id="059ff-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="059ff-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-514">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-515">Product 1</span></span></td>
<td><span data-ttu-id="059ff-516">80</span><span class="sxs-lookup"><span data-stu-id="059ff-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-517">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-518">Product 2</span></span></td>
<td><span data-ttu-id="059ff-519">15</span><span class="sxs-lookup"><span data-stu-id="059ff-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="059ff-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="059ff-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="059ff-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="059ff-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="059ff-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="059ff-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-523">Cost object</span></span></th>
<th><span data-ttu-id="059ff-524">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-524">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-525">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-526">Amount</span></span></th>
<th><span data-ttu-id="059ff-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-528">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-528">CC002</span></span></td>
<td><span data-ttu-id="059ff-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-529">Finance</span></span></td>
<td><span data-ttu-id="059ff-530">35</span><span class="sxs-lookup"><span data-stu-id="059ff-530">35</span></span></td>
<td><span data-ttu-id="059ff-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="059ff-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="059ff-532">175.00</span><span class="sxs-lookup"><span data-stu-id="059ff-532">175.00</span></span></td>
<td><span data-ttu-id="059ff-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-534">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-534">CC003</span></span></td>
<td><span data-ttu-id="059ff-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-535">Assembly</span></span></td>
<td><span data-ttu-id="059ff-536">55</span><span class="sxs-lookup"><span data-stu-id="059ff-536">55</span></span></td>
<td><span data-ttu-id="059ff-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="059ff-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="059ff-538">275.00</span><span class="sxs-lookup"><span data-stu-id="059ff-538">275.00</span></span></td>
<td><span data-ttu-id="059ff-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-540">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-540">CC004</span></span></td>
<td><span data-ttu-id="059ff-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-541">Packaging</span></span></td>
<td><span data-ttu-id="059ff-542">10</span><span class="sxs-lookup"><span data-stu-id="059ff-542">10</span></span></td>
<td><span data-ttu-id="059ff-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="059ff-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="059ff-544">50,00</span><span class="sxs-lookup"><span data-stu-id="059ff-544">50.00</span></span></td>
<td><span data-ttu-id="059ff-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-546">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-546">CC002</span></span></td>
<td><span data-ttu-id="059ff-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-547">Finance</span></span></td>
<td><span data-ttu-id="059ff-548">35</span><span class="sxs-lookup"><span data-stu-id="059ff-548">35</span></span></td>
<td><span data-ttu-id="059ff-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="059ff-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="059ff-550">436.00</span><span class="sxs-lookup"><span data-stu-id="059ff-550">436.00</span></span></td>
<td><span data-ttu-id="059ff-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-552">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-552">CC003</span></span></td>
<td><span data-ttu-id="059ff-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-553">Assembly</span></span></td>
<td><span data-ttu-id="059ff-554">55</span><span class="sxs-lookup"><span data-stu-id="059ff-554">55</span></span></td>
<td><span data-ttu-id="059ff-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="059ff-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="059ff-556">685.14</span><span class="sxs-lookup"><span data-stu-id="059ff-556">685.14</span></span></td>
<td><span data-ttu-id="059ff-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-558">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-558">CC004</span></span></td>
<td><span data-ttu-id="059ff-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-559">Packaging</span></span></td>
<td><span data-ttu-id="059ff-560">10</span><span class="sxs-lookup"><span data-stu-id="059ff-560">10</span></span></td>
<td><span data-ttu-id="059ff-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="059ff-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="059ff-562">124.57</span><span class="sxs-lookup"><span data-stu-id="059ff-562">124.57</span></span></td>
<td><span data-ttu-id="059ff-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="059ff-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-565">Cost object</span></span></th>
<th><span data-ttu-id="059ff-566">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-566">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-567">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-568">Amount</span></span></th>
<th><span data-ttu-id="059ff-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-570">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-570">CC003</span></span></td>
<td><span data-ttu-id="059ff-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-571">Assembly</span></span></td>
<td><span data-ttu-id="059ff-572">65</span><span class="sxs-lookup"><span data-stu-id="059ff-572">65</span></span></td>
<td><span data-ttu-id="059ff-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="059ff-574">438.75</span><span class="sxs-lookup"><span data-stu-id="059ff-574">438.75</span></span></td>
<td><span data-ttu-id="059ff-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-576">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-576">CC004</span></span></td>
<td><span data-ttu-id="059ff-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-577">Packaging</span></span></td>
<td><span data-ttu-id="059ff-578">35</span><span class="sxs-lookup"><span data-stu-id="059ff-578">35</span></span></td>
<td><span data-ttu-id="059ff-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="059ff-580">236.25</span><span class="sxs-lookup"><span data-stu-id="059ff-580">236.25</span></span></td>
<td><span data-ttu-id="059ff-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-582">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-582">CC003</span></span></td>
<td><span data-ttu-id="059ff-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-583">Assembly</span></span></td>
<td><span data-ttu-id="059ff-584">65</span><span class="sxs-lookup"><span data-stu-id="059ff-584">65</span></span></td>
<td><span data-ttu-id="059ff-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="059ff-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="059ff-586">5,297.69</span></span></td>
<td><span data-ttu-id="059ff-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-588">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-588">CC004</span></span></td>
<td><span data-ttu-id="059ff-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-589">Packaging</span></span></td>
<td><span data-ttu-id="059ff-590">35</span><span class="sxs-lookup"><span data-stu-id="059ff-590">35</span></span></td>
<td><span data-ttu-id="059ff-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="059ff-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="059ff-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="059ff-592">2,852.60</span></span></td>
<td><span data-ttu-id="059ff-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="059ff-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-595">Cost object</span></span></th>
<th><span data-ttu-id="059ff-596">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-596">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-597">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-598">Amount</span></span></th>
<th><span data-ttu-id="059ff-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-600">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-601">Product 1</span></span></td>
<td><span data-ttu-id="059ff-602">60</span><span class="sxs-lookup"><span data-stu-id="059ff-602">60</span></span></td>
<td><span data-ttu-id="059ff-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="059ff-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="059ff-604">535.31</span><span class="sxs-lookup"><span data-stu-id="059ff-604">535.31</span></span></td>
<td><span data-ttu-id="059ff-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-606">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-607">Product 2</span></span></td>
<td><span data-ttu-id="059ff-608">20</span><span class="sxs-lookup"><span data-stu-id="059ff-608">20</span></span></td>
<td><span data-ttu-id="059ff-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="059ff-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="059ff-610">178.44</span><span class="sxs-lookup"><span data-stu-id="059ff-610">178.44</span></span></td>
<td><span data-ttu-id="059ff-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-612">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-613">Product 1</span></span></td>
<td><span data-ttu-id="059ff-614">60</span><span class="sxs-lookup"><span data-stu-id="059ff-614">60</span></span></td>
<td><span data-ttu-id="059ff-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="059ff-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="059ff-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="059ff-616">4,487.12</span></span></td>
<td><span data-ttu-id="059ff-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-618">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-619">Product 2</span></span></td>
<td><span data-ttu-id="059ff-620">20</span><span class="sxs-lookup"><span data-stu-id="059ff-620">20</span></span></td>
<td><span data-ttu-id="059ff-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="059ff-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="059ff-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="059ff-622">1,495.71</span></span></td>
<td><span data-ttu-id="059ff-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="059ff-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="059ff-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-625">Cost object</span></span></th>
<th><span data-ttu-id="059ff-626">Величина</span><span class="sxs-lookup"><span data-stu-id="059ff-626">Magnitude</span></span></th>
<th><span data-ttu-id="059ff-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="059ff-627">Allocation factor</span></span></th>
<th><span data-ttu-id="059ff-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-628">Amount</span></span></th>
<th><span data-ttu-id="059ff-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-630">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-631">Product 1</span></span></td>
<td><span data-ttu-id="059ff-632">80</span><span class="sxs-lookup"><span data-stu-id="059ff-632">80</span></span></td>
<td><span data-ttu-id="059ff-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="059ff-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="059ff-634">241.05</span><span class="sxs-lookup"><span data-stu-id="059ff-634">241.05</span></span></td>
<td><span data-ttu-id="059ff-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-636">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-637">Product 2</span></span></td>
<td><span data-ttu-id="059ff-638">15</span><span class="sxs-lookup"><span data-stu-id="059ff-638">15</span></span></td>
<td><span data-ttu-id="059ff-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="059ff-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="059ff-640">45.20</span><span class="sxs-lookup"><span data-stu-id="059ff-640">45.20</span></span></td>
<td><span data-ttu-id="059ff-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-642">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-643">Product 1</span></span></td>
<td><span data-ttu-id="059ff-644">80</span><span class="sxs-lookup"><span data-stu-id="059ff-644">80</span></span></td>
<td><span data-ttu-id="059ff-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="059ff-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="059ff-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="059ff-646">2,507.09</span></span></td>
<td><span data-ttu-id="059ff-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-648">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-649">Product 2</span></span></td>
<td><span data-ttu-id="059ff-650">15</span><span class="sxs-lookup"><span data-stu-id="059ff-650">15</span></span></td>
<td><span data-ttu-id="059ff-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="059ff-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="059ff-652">470.08</span><span class="sxs-lookup"><span data-stu-id="059ff-652">470.08</span></span></td>
<td><span data-ttu-id="059ff-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="059ff-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="059ff-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="059ff-655">Journal</span></span></th>
<th><span data-ttu-id="059ff-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="059ff-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="059ff-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="059ff-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="059ff-658">Версия</span><span class="sxs-lookup"><span data-stu-id="059ff-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-659">00004</span><span class="sxs-lookup"><span data-stu-id="059ff-659">00004</span></span></td>
<td><span data-ttu-id="059ff-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="059ff-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="059ff-661">Fiscal</span></span></td>
<td><span data-ttu-id="059ff-662">2017</span><span class="sxs-lookup"><span data-stu-id="059ff-662">2017</span></span></td>
<td><span data-ttu-id="059ff-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-663">Period 1</span></span></td>
<td><span data-ttu-id="059ff-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="059ff-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="059ff-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="059ff-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="059ff-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-668">Cost element</span></span></th>
<th><span data-ttu-id="059ff-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-669">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-672">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-672">CC001</span></span></td>
<td><span data-ttu-id="059ff-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-673">HR</span></span></td>
<td><span data-ttu-id="059ff-674">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-674">10001</span></span></td>
<td><span data-ttu-id="059ff-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-675">Electricity</span></span></td>
<td><span data-ttu-id="059ff-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-676">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-677">500.00</span><span class="sxs-lookup"><span data-stu-id="059ff-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-679">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-679">CC001</span></span></td>
<td><span data-ttu-id="059ff-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-680">HR</span></span></td>
<td><span data-ttu-id="059ff-681">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-681">10001</span></span></td>
<td><span data-ttu-id="059ff-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-682">Electricity</span></span></td>
<td><span data-ttu-id="059ff-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-683">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="059ff-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-686">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-686">CC002</span></span></td>
<td><span data-ttu-id="059ff-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-687">Finance</span></span></td>
<td><span data-ttu-id="059ff-688">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-688">10001</span></span></td>
<td><span data-ttu-id="059ff-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-689">Electricity</span></span></td>
<td><span data-ttu-id="059ff-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-690">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-691">675.00</span><span class="sxs-lookup"><span data-stu-id="059ff-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-693">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-693">CC002</span></span></td>
<td><span data-ttu-id="059ff-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-694">Finance</span></span></td>
<td><span data-ttu-id="059ff-695">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-695">10001</span></span></td>
<td><span data-ttu-id="059ff-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-696">Electricity</span></span></td>
<td><span data-ttu-id="059ff-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-697">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="059ff-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-700">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-700">CC003</span></span></td>
<td><span data-ttu-id="059ff-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-701">Assembly</span></span></td>
<td><span data-ttu-id="059ff-702">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-702">10001</span></span></td>
<td><span data-ttu-id="059ff-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-703">Electricity</span></span></td>
<td><span data-ttu-id="059ff-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-704">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-705">713.75</span><span class="sxs-lookup"><span data-stu-id="059ff-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-707">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-707">CC003</span></span></td>
<td><span data-ttu-id="059ff-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-708">Assembly</span></span></td>
<td><span data-ttu-id="059ff-709">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-709">10001</span></span></td>
<td><span data-ttu-id="059ff-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-710">Electricity</span></span></td>
<td><span data-ttu-id="059ff-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-711">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="059ff-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-714">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-714">CC003</span></span></td>
<td><span data-ttu-id="059ff-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-715">Packaging</span></span></td>
<td><span data-ttu-id="059ff-716">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-716">10001</span></span></td>
<td><span data-ttu-id="059ff-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-717">Electricity</span></span></td>
<td><span data-ttu-id="059ff-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-718">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-719">286.25</span><span class="sxs-lookup"><span data-stu-id="059ff-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-721">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-721">CC003</span></span></td>
<td><span data-ttu-id="059ff-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-722">Packaging</span></span></td>
<td><span data-ttu-id="059ff-723">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-723">10001</span></span></td>
<td><span data-ttu-id="059ff-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-724">Electricity</span></span></td>
<td><span data-ttu-id="059ff-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-725">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="059ff-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-728">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-729">Product 1</span></span></td>
<td><span data-ttu-id="059ff-730">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-730">10001</span></span></td>
<td><span data-ttu-id="059ff-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-731">Electricity</span></span></td>
<td><span data-ttu-id="059ff-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-732">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-733">776.36</span><span class="sxs-lookup"><span data-stu-id="059ff-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-735">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-736">Product 1</span></span></td>
<td><span data-ttu-id="059ff-737">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-737">10001</span></span></td>
<td><span data-ttu-id="059ff-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-738">Electricity</span></span></td>
<td><span data-ttu-id="059ff-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-739">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="059ff-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-742">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-743">Product 1</span></span></td>
<td><span data-ttu-id="059ff-744">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-744">10001</span></span></td>
<td><span data-ttu-id="059ff-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-745">Electricity</span></span></td>
<td><span data-ttu-id="059ff-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-746">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-747">223.64</span><span class="sxs-lookup"><span data-stu-id="059ff-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="059ff-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-749">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-750">Product 1</span></span></td>
<td><span data-ttu-id="059ff-751">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-751">10001</span></span></td>
<td><span data-ttu-id="059ff-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-752">Electricity</span></span></td>
<td><span data-ttu-id="059ff-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-753">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="059ff-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="059ff-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="059ff-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="059ff-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-757">Cost element</span></span></th>
<th><span data-ttu-id="059ff-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-758">Cost behavior</span></span></th>
<th><span data-ttu-id="059ff-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="059ff-759">Amount</span></span></th>
<th><span data-ttu-id="059ff-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="059ff-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="059ff-761">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-761">CC001</span></span></td>
<td><span data-ttu-id="059ff-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-762">HR</span></span></td>
<td><span data-ttu-id="059ff-763">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-763">10001</span></span></td>
<td><span data-ttu-id="059ff-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-764">Electricity</span></span></td>
<td><span data-ttu-id="059ff-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-765">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="059ff-766">-500.00</span></span></td>
<td><span data-ttu-id="059ff-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-768">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-768">CC002</span></span></td>
<td><span data-ttu-id="059ff-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-769">Finance</span></span></td>
<td><span data-ttu-id="059ff-770">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-770">10001</span></span></td>
<td><span data-ttu-id="059ff-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-771">Electricity</span></span></td>
<td><span data-ttu-id="059ff-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-772">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-773">175.00</span><span class="sxs-lookup"><span data-stu-id="059ff-773">175.00</span></span></td>
<td><span data-ttu-id="059ff-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-775">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-775">CC003</span></span></td>
<td><span data-ttu-id="059ff-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-776">Assembly</span></span></td>
<td><span data-ttu-id="059ff-777">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-777">10001</span></span></td>
<td><span data-ttu-id="059ff-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-778">Electricity</span></span></td>
<td><span data-ttu-id="059ff-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-779">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-780">275.00</span><span class="sxs-lookup"><span data-stu-id="059ff-780">275.00</span></span></td>
<td><span data-ttu-id="059ff-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-782">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-782">CC004</span></span></td>
<td><span data-ttu-id="059ff-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-783">Packaging</span></span></td>
<td><span data-ttu-id="059ff-784">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-784">10001</span></span></td>
<td><span data-ttu-id="059ff-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-785">Electricity</span></span></td>
<td><span data-ttu-id="059ff-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-786">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-787">50,00</span><span class="sxs-lookup"><span data-stu-id="059ff-787">50,00</span></span></td>
<td><span data-ttu-id="059ff-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-789">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-789">CC001</span></span></td>
<td><span data-ttu-id="059ff-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="059ff-790">HR</span></span></td>
<td><span data-ttu-id="059ff-791">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-791">10001</span></span></td>
<td><span data-ttu-id="059ff-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-792">Electricity</span></span></td>
<td><span data-ttu-id="059ff-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-793">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="059ff-794">-1,245.71</span></span></td>
<td><span data-ttu-id="059ff-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-796">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-796">CC002</span></span></td>
<td><span data-ttu-id="059ff-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-797">Finance</span></span></td>
<td><span data-ttu-id="059ff-798">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-798">10001</span></span></td>
<td><span data-ttu-id="059ff-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-799">Electricity</span></span></td>
<td><span data-ttu-id="059ff-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-800">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-801">436.00</span><span class="sxs-lookup"><span data-stu-id="059ff-801">436.00</span></span></td>
<td><span data-ttu-id="059ff-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-803">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-803">CC003</span></span></td>
<td><span data-ttu-id="059ff-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-804">Assembly</span></span></td>
<td><span data-ttu-id="059ff-805">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-805">10001</span></span></td>
<td><span data-ttu-id="059ff-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-806">Electricity</span></span></td>
<td><span data-ttu-id="059ff-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-807">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-808">685.14</span><span class="sxs-lookup"><span data-stu-id="059ff-808">685.14</span></span></td>
<td><span data-ttu-id="059ff-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-810">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-810">CC004</span></span></td>
<td><span data-ttu-id="059ff-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-811">Packaging</span></span></td>
<td><span data-ttu-id="059ff-812">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-812">10001</span></span></td>
<td><span data-ttu-id="059ff-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-813">Electricity</span></span></td>
<td><span data-ttu-id="059ff-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-814">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-815">124.57</span><span class="sxs-lookup"><span data-stu-id="059ff-815">124.57</span></span></td>
<td><span data-ttu-id="059ff-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-817">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-817">CC002</span></span></td>
<td><span data-ttu-id="059ff-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-818">Finance</span></span></td>
<td><span data-ttu-id="059ff-819">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-819">10001</span></span></td>
<td><span data-ttu-id="059ff-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-820">Electricity</span></span></td>
<td><span data-ttu-id="059ff-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-821">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="059ff-822">-675.00</span></span></td>
<td><span data-ttu-id="059ff-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-824">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-824">CC003</span></span></td>
<td><span data-ttu-id="059ff-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-825">Assembly</span></span></td>
<td><span data-ttu-id="059ff-826">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-826">10001</span></span></td>
<td><span data-ttu-id="059ff-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-827">Electricity</span></span></td>
<td><span data-ttu-id="059ff-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-828">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-829">438.75</span><span class="sxs-lookup"><span data-stu-id="059ff-829">438.75</span></span></td>
<td><span data-ttu-id="059ff-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-831">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-831">CC004</span></span></td>
<td><span data-ttu-id="059ff-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-832">Packaging</span></span></td>
<td><span data-ttu-id="059ff-833">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-833">10001</span></span></td>
<td><span data-ttu-id="059ff-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-834">Electricity</span></span></td>
<td><span data-ttu-id="059ff-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-835">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-836">236.25</span><span class="sxs-lookup"><span data-stu-id="059ff-836">236.25</span></span></td>
<td><span data-ttu-id="059ff-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-838">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-838">CC002</span></span></td>
<td><span data-ttu-id="059ff-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="059ff-839">Finance</span></span></td>
<td><span data-ttu-id="059ff-840">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-840">10001</span></span></td>
<td><span data-ttu-id="059ff-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-841">Electricity</span></span></td>
<td><span data-ttu-id="059ff-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-842">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="059ff-843">-8,150.29</span></span></td>
<td><span data-ttu-id="059ff-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-845">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-845">CC003</span></span></td>
<td><span data-ttu-id="059ff-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-846">Assembly</span></span></td>
<td><span data-ttu-id="059ff-847">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-847">10001</span></span></td>
<td><span data-ttu-id="059ff-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-848">Electricity</span></span></td>
<td><span data-ttu-id="059ff-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-849">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="059ff-850">5,297.69</span></span></td>
<td><span data-ttu-id="059ff-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-852">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-852">CC004</span></span></td>
<td><span data-ttu-id="059ff-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="059ff-853">Packaging</span></span></td>
<td><span data-ttu-id="059ff-854">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-854">10001</span></span></td>
<td><span data-ttu-id="059ff-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-855">Electricity</span></span></td>
<td><span data-ttu-id="059ff-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-856">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="059ff-857">2,852.60</span></span></td>
<td><span data-ttu-id="059ff-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-859">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-859">CC003</span></span></td>
<td><span data-ttu-id="059ff-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-860">Assembly</span></span></td>
<td><span data-ttu-id="059ff-861">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-861">10001</span></span></td>
<td><span data-ttu-id="059ff-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-862">Electricity</span></span></td>
<td><span data-ttu-id="059ff-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-863">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="059ff-864">-713.75</span></span></td>
<td><span data-ttu-id="059ff-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-866">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-867">Product 1</span></span></td>
<td><span data-ttu-id="059ff-868">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-868">10001</span></span></td>
<td><span data-ttu-id="059ff-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-869">Electricity</span></span></td>
<td><span data-ttu-id="059ff-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-870">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-871">535.31</span><span class="sxs-lookup"><span data-stu-id="059ff-871">535.31</span></span></td>
<td><span data-ttu-id="059ff-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-873">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-874">Product 2</span></span></td>
<td><span data-ttu-id="059ff-875">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-875">10001</span></span></td>
<td><span data-ttu-id="059ff-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-876">Electricity</span></span></td>
<td><span data-ttu-id="059ff-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-877">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-878">178.44</span><span class="sxs-lookup"><span data-stu-id="059ff-878">178.44</span></span></td>
<td><span data-ttu-id="059ff-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-880">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-880">CC003</span></span></td>
<td><span data-ttu-id="059ff-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-881">Assembly</span></span></td>
<td><span data-ttu-id="059ff-882">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-882">10001</span></span></td>
<td><span data-ttu-id="059ff-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-883">Electricity</span></span></td>
<td><span data-ttu-id="059ff-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-884">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="059ff-885">-5,982.83</span></span></td>
<td><span data-ttu-id="059ff-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-887">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-888">Product 1</span></span></td>
<td><span data-ttu-id="059ff-889">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-889">10001</span></span></td>
<td><span data-ttu-id="059ff-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-890">Electricity</span></span></td>
<td><span data-ttu-id="059ff-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-891">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="059ff-892">4,487.12</span></span></td>
<td><span data-ttu-id="059ff-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-894">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-895">Product 2</span></span></td>
<td><span data-ttu-id="059ff-896">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-896">10001</span></span></td>
<td><span data-ttu-id="059ff-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-897">Electricity</span></span></td>
<td><span data-ttu-id="059ff-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-898">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="059ff-899">1,495.71</span></span></td>
<td><span data-ttu-id="059ff-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-901">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-901">CC003</span></span></td>
<td><span data-ttu-id="059ff-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-902">Assembly</span></span></td>
<td><span data-ttu-id="059ff-903">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-903">10001</span></span></td>
<td><span data-ttu-id="059ff-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-904">Electricity</span></span></td>
<td><span data-ttu-id="059ff-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-905">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="059ff-906">-286.25</span></span></td>
<td><span data-ttu-id="059ff-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-908">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-909">Product 1</span></span></td>
<td><span data-ttu-id="059ff-910">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-910">10001</span></span></td>
<td><span data-ttu-id="059ff-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-911">Electricity</span></span></td>
<td><span data-ttu-id="059ff-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-912">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-913">241.05</span><span class="sxs-lookup"><span data-stu-id="059ff-913">241.05</span></span></td>
<td><span data-ttu-id="059ff-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-915">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-916">Product 2</span></span></td>
<td><span data-ttu-id="059ff-917">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-917">10001</span></span></td>
<td><span data-ttu-id="059ff-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-918">Electricity</span></span></td>
<td><span data-ttu-id="059ff-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-919">Fixed cost</span></span></td>
<td><span data-ttu-id="059ff-920">45.20</span><span class="sxs-lookup"><span data-stu-id="059ff-920">45.20</span></span></td>
<td><span data-ttu-id="059ff-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-922">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-922">CC003</span></span></td>
<td><span data-ttu-id="059ff-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="059ff-923">Assembly</span></span></td>
<td><span data-ttu-id="059ff-924">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-924">10001</span></span></td>
<td><span data-ttu-id="059ff-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-925">Electricity</span></span></td>
<td><span data-ttu-id="059ff-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-926">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="059ff-927">-2,977.17</span></span></td>
<td><span data-ttu-id="059ff-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-929">Prod 1</span></span></td>
<td><span data-ttu-id="059ff-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="059ff-930">Product 1</span></span></td>
<td><span data-ttu-id="059ff-931">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-931">10001</span></span></td>
<td><span data-ttu-id="059ff-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-932">Electricity</span></span></td>
<td><span data-ttu-id="059ff-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-933">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="059ff-934">2,507.09</span></span></td>
<td><span data-ttu-id="059ff-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="059ff-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-936">Prod 2</span></span></td>
<td><span data-ttu-id="059ff-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="059ff-937">Product 2</span></span></td>
<td><span data-ttu-id="059ff-938">10001</span><span class="sxs-lookup"><span data-stu-id="059ff-938">10001</span></span></td>
<td><span data-ttu-id="059ff-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-939">Electricity</span></span></td>
<td><span data-ttu-id="059ff-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-940">Variable cost</span></span></td>
<td><span data-ttu-id="059ff-941">470.08</span><span class="sxs-lookup"><span data-stu-id="059ff-941">470.08</span></span></td>
<td><span data-ttu-id="059ff-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="059ff-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="059ff-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="059ff-943">Conclusion</span></span>
<span data-ttu-id="059ff-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="059ff-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="059ff-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="059ff-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="059ff-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="059ff-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="059ff-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="059ff-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="059ff-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="059ff-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="059ff-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="059ff-951">CC099</span><span class="sxs-lookup"><span data-stu-id="059ff-951">CC099</span></span></th>
<th><span data-ttu-id="059ff-952">CC001</span><span class="sxs-lookup"><span data-stu-id="059ff-952">CC001</span></span></th>
<th><span data-ttu-id="059ff-953">CC002</span><span class="sxs-lookup"><span data-stu-id="059ff-953">CC002</span></span></th>
<th><span data-ttu-id="059ff-954">CC003</span><span class="sxs-lookup"><span data-stu-id="059ff-954">CC003</span></span></th>
<th><span data-ttu-id="059ff-955">CC004</span><span class="sxs-lookup"><span data-stu-id="059ff-955">CC004</span></span></th>
<th><span data-ttu-id="059ff-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="059ff-956">Proj 1</span></span></th>
<th><span data-ttu-id="059ff-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="059ff-957">Proj 2</span></span></th>
<th><span data-ttu-id="059ff-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="059ff-958">Prod 1</span></span></th>
<th><span data-ttu-id="059ff-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="059ff-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="059ff-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="059ff-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="059ff-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="059ff-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="059ff-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-971">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="059ff-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-973">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-974">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-975">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-976">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-977">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="059ff-978">776.36</span><span class="sxs-lookup"><span data-stu-id="059ff-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-979">223.64</span><span class="sxs-lookup"><span data-stu-id="059ff-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="059ff-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="059ff-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-982">000</span><span class="sxs-lookup"><span data-stu-id="059ff-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-983">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-984">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-985">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-986">0,00</span><span class="sxs-lookup"><span data-stu-id="059ff-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-987">30.00</span><span class="sxs-lookup"><span data-stu-id="059ff-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-988">10,00</span><span class="sxs-lookup"><span data-stu-id="059ff-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="059ff-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="059ff-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="059ff-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="059ff-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="059ff-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="059ff-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="059ff-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="059ff-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="059ff-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="059ff-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="059ff-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="059ff-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="059ff-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



