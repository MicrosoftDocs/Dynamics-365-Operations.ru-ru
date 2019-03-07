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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "335125"
---
# <a name="overhead-calculation"></a><span data-ttu-id="dc283-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="dc283-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc283-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="dc283-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="dc283-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="dc283-105">Term definition</span></span>
---------------

<span data-ttu-id="dc283-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="dc283-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="dc283-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="dc283-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="dc283-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="dc283-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="dc283-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="dc283-109">Rent</span></span>
-   <span data-ttu-id="dc283-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-110">Electricity</span></span>
-   <span data-ttu-id="dc283-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="dc283-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="dc283-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="dc283-112">Overhead calculation overview</span></span>
<span data-ttu-id="dc283-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="dc283-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="dc283-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="dc283-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="dc283-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="dc283-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="dc283-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="dc283-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="dc283-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="dc283-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="dc283-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="dc283-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="dc283-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="dc283-119">Version type</span></span>
-   <span data-ttu-id="dc283-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="dc283-120">Date and time</span></span>
-   <span data-ttu-id="dc283-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="dc283-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="dc283-122">Fiscal year</span></span>
-   <span data-ttu-id="dc283-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="dc283-123">Fiscal period</span></span>

<span data-ttu-id="dc283-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="dc283-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="dc283-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="dc283-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="dc283-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc283-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="dc283-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="dc283-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="dc283-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="dc283-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="dc283-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="dc283-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="dc283-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="dc283-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="dc283-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="dc283-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="dc283-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="dc283-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="dc283-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="dc283-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="dc283-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="dc283-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="dc283-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="dc283-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="dc283-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="dc283-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dc283-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="dc283-140">Main account</span></span></th>
<th><span data-ttu-id="dc283-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="dc283-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="dc283-143">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-143">CC099</span></span></td>
<td><span data-ttu-id="dc283-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-144">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-145">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-145">10001</span></span></td>
<td><span data-ttu-id="dc283-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-146">Electricity</span></span></td>
<td><span data-ttu-id="dc283-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="dc283-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="dc283-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="dc283-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="dc283-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="dc283-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="dc283-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-151">Define the cost behavior rule</span></span>

<span data-ttu-id="dc283-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="dc283-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="dc283-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="dc283-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="dc283-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="dc283-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="dc283-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="dc283-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="dc283-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="dc283-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="dc283-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="dc283-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-160">Journal</span></span></th>
<th><span data-ttu-id="dc283-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="dc283-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dc283-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="dc283-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dc283-163">Версия</span><span class="sxs-lookup"><span data-stu-id="dc283-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-164">00001</span><span class="sxs-lookup"><span data-stu-id="dc283-164">00001</span></span></td>
<td><span data-ttu-id="dc283-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="dc283-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="dc283-166">Fiscal</span></span></td>
<td><span data-ttu-id="dc283-167">2017</span><span class="sxs-lookup"><span data-stu-id="dc283-167">2017</span></span></td>
<td><span data-ttu-id="dc283-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-168">Period 1</span></span></td>
<td><span data-ttu-id="dc283-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dc283-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="dc283-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-173">Cost element</span></span></th>
<th><span data-ttu-id="dc283-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-174">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="dc283-177">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-177">CC099</span></span></td>
<td><span data-ttu-id="dc283-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-178">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-179">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-179">10001</span></span></td>
<td><span data-ttu-id="dc283-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-180">Electricity</span></span></td>
<td><span data-ttu-id="dc283-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="dc283-181">Unclassified</span></span></td>
<td><span data-ttu-id="dc283-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="dc283-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dc283-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-185">Cost element</span></span></th>
<th><span data-ttu-id="dc283-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-186">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-187">Amount</span></span></th>
<th><span data-ttu-id="dc283-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-189">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-189">CC099</span></span></td>
<td><span data-ttu-id="dc283-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-190">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-191">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-191">10001</span></span></td>
<td><span data-ttu-id="dc283-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-192">Electricity</span></span></td>
<td><span data-ttu-id="dc283-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="dc283-193">Unclassified</span></span></td>
<td><span data-ttu-id="dc283-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="dc283-194">10,000.00</span></span></td>
<td><span data-ttu-id="dc283-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-196">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-196">CC099</span></span></td>
<td><span data-ttu-id="dc283-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-197">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-198">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-198">10001</span></span></td>
<td><span data-ttu-id="dc283-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-199">Electricity</span></span></td>
<td><span data-ttu-id="dc283-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="dc283-200">Unclassified</span></span></td>
<td><span data-ttu-id="dc283-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-201">-10,000.00</span></span></td>
<td><span data-ttu-id="dc283-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-203">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-203">CC099</span></span></td>
<td><span data-ttu-id="dc283-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-204">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-205">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-205">10001</span></span></td>
<td><span data-ttu-id="dc283-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-206">Electricity</span></span></td>
<td><span data-ttu-id="dc283-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-207">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-208">1,000.00</span></span></td>
<td><span data-ttu-id="dc283-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-210">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-210">CC099</span></span></td>
<td><span data-ttu-id="dc283-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-211">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-212">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-212">10001</span></span></td>
<td><span data-ttu-id="dc283-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-213">Electricity</span></span></td>
<td><span data-ttu-id="dc283-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-214">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="dc283-215">9,000.00</span></span></td>
<td><span data-ttu-id="dc283-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="dc283-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="dc283-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="dc283-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="dc283-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="dc283-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-221">Define the cost distribution rule</span></span>

<span data-ttu-id="dc283-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="dc283-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="dc283-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="dc283-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="dc283-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="dc283-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="dc283-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="dc283-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="dc283-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="dc283-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="dc283-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-228">Cost object</span></span></th>
<th><span data-ttu-id="dc283-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="dc283-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-230">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-230">CC001</span></span></td>
<td><span data-ttu-id="dc283-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-231">HR</span></span></td>
<td><span data-ttu-id="dc283-232">1000</span><span class="sxs-lookup"><span data-stu-id="dc283-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-233">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-233">CC002</span></span></td>
<td><span data-ttu-id="dc283-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-234">Finance</span></span></td>
<td><span data-ttu-id="dc283-235">6,000</span><span class="sxs-lookup"><span data-stu-id="dc283-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-236">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-236">CC003</span></span></td>
<td><span data-ttu-id="dc283-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-237">Assembly</span></span></td>
<td><span data-ttu-id="dc283-238">0</span><span class="sxs-lookup"><span data-stu-id="dc283-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-240">Cost object</span></span></th>
<th><span data-ttu-id="dc283-241">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-241">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-242">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-244">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-244">CC001</span></span></td>
<td><span data-ttu-id="dc283-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-245">HR</span></span></td>
<td><span data-ttu-id="dc283-246">1000</span><span class="sxs-lookup"><span data-stu-id="dc283-246">1,000</span></span></td>
<td><span data-ttu-id="dc283-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dc283-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="dc283-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-249">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-249">CC002</span></span></td>
<td><span data-ttu-id="dc283-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-250">Finance</span></span></td>
<td><span data-ttu-id="dc283-251">6,000</span><span class="sxs-lookup"><span data-stu-id="dc283-251">6,000</span></span></td>
<td><span data-ttu-id="dc283-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dc283-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="dc283-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-254">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-254">CC003</span></span></td>
<td><span data-ttu-id="dc283-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-255">Assembly</span></span></td>
<td><span data-ttu-id="dc283-256">0</span><span class="sxs-lookup"><span data-stu-id="dc283-256">0</span></span></td>
<td><span data-ttu-id="dc283-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dc283-258">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="dc283-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="dc283-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-261">Cost object</span></span></th>
<th><span data-ttu-id="dc283-262">Формула</span><span class="sxs-lookup"><span data-stu-id="dc283-262">Formula</span></span></th>
<th><span data-ttu-id="dc283-263">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-263">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-264">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-266">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-266">CC001</span></span></td>
<td><span data-ttu-id="dc283-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-267">HR</span></span></td>
<td><span data-ttu-id="dc283-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dc283-269">1</span><span class="sxs-lookup"><span data-stu-id="dc283-269">1</span></span></td>
<td><span data-ttu-id="dc283-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dc283-271">500.00</span><span class="sxs-lookup"><span data-stu-id="dc283-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-272">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-272">CC002</span></span></td>
<td><span data-ttu-id="dc283-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-273">Finance</span></span></td>
<td><span data-ttu-id="dc283-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dc283-275">1</span><span class="sxs-lookup"><span data-stu-id="dc283-275">1</span></span></td>
<td><span data-ttu-id="dc283-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dc283-277">500.00</span><span class="sxs-lookup"><span data-stu-id="dc283-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-278">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-278">CC003</span></span></td>
<td><span data-ttu-id="dc283-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-279">Assembly</span></span></td>
<td><span data-ttu-id="dc283-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dc283-281">0</span><span class="sxs-lookup"><span data-stu-id="dc283-281">0</span></span></td>
<td><span data-ttu-id="dc283-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dc283-283">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="dc283-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-285">Journal</span></span></th>
<th><span data-ttu-id="dc283-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="dc283-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dc283-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="dc283-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dc283-288">Версия</span><span class="sxs-lookup"><span data-stu-id="dc283-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-289">00002</span><span class="sxs-lookup"><span data-stu-id="dc283-289">00002</span></span></td>
<td><span data-ttu-id="dc283-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="dc283-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="dc283-291">Fiscal</span></span></td>
<td><span data-ttu-id="dc283-292">2017</span><span class="sxs-lookup"><span data-stu-id="dc283-292">2017</span></span></td>
<td><span data-ttu-id="dc283-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-293">Period 1</span></span></td>
<td><span data-ttu-id="dc283-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dc283-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="dc283-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-298">Cost element</span></span></th>
<th><span data-ttu-id="dc283-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-299">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-302">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-302">CC099</span></span></td>
<td><span data-ttu-id="dc283-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-303">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-304">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-304">10001</span></span></td>
<td><span data-ttu-id="dc283-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-305">Electricity</span></span></td>
<td><span data-ttu-id="dc283-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-306">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-309">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-309">CC099</span></span></td>
<td><span data-ttu-id="dc283-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-310">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-311">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-311">10001</span></span></td>
<td><span data-ttu-id="dc283-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-312">Electricity</span></span></td>
<td><span data-ttu-id="dc283-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-313">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="dc283-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dc283-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-317">Cost element</span></span></th>
<th><span data-ttu-id="dc283-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-318">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-319">Amount</span></span></th>
<th><span data-ttu-id="dc283-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-321">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-321">CC099</span></span></td>
<td><span data-ttu-id="dc283-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-322">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-323">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-323">10001</span></span></td>
<td><span data-ttu-id="dc283-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-324">Electricity</span></span></td>
<td><span data-ttu-id="dc283-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-325">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-326">-1,000.00</span></span></td>
<td><span data-ttu-id="dc283-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-328">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-328">CC001</span></span></td>
<td><span data-ttu-id="dc283-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-329">HR</span></span></td>
<td><span data-ttu-id="dc283-330">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-330">10001</span></span></td>
<td><span data-ttu-id="dc283-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-331">Electricity</span></span></td>
<td><span data-ttu-id="dc283-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-332">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-333">500.00</span><span class="sxs-lookup"><span data-stu-id="dc283-333">500.00</span></span></td>
<td><span data-ttu-id="dc283-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-335">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-335">CC002</span></span></td>
<td><span data-ttu-id="dc283-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-336">Finance</span></span></td>
<td><span data-ttu-id="dc283-337">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-337">10001</span></span></td>
<td><span data-ttu-id="dc283-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-338">Electricity</span></span></td>
<td><span data-ttu-id="dc283-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-339">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-340">500.00</span><span class="sxs-lookup"><span data-stu-id="dc283-340">500.00</span></span></td>
<td><span data-ttu-id="dc283-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-342">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-342">CC099</span></span></td>
<td><span data-ttu-id="dc283-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc283-343">Default cost center</span></span></td>
<td><span data-ttu-id="dc283-344">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-344">10001</span></span></td>
<td><span data-ttu-id="dc283-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-345">Electricity</span></span></td>
<td><span data-ttu-id="dc283-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-346">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="dc283-347">-9,000.00</span></span></td>
<td><span data-ttu-id="dc283-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-349">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-349">CC001</span></span></td>
<td><span data-ttu-id="dc283-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-350">HR</span></span></td>
<td><span data-ttu-id="dc283-351">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-351">10001</span></span></td>
<td><span data-ttu-id="dc283-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-352">Electricity</span></span></td>
<td><span data-ttu-id="dc283-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-353">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="dc283-354">1,285.71</span></span></td>
<td><span data-ttu-id="dc283-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-356">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-356">CC002</span></span></td>
<td><span data-ttu-id="dc283-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-357">Finance</span></span></td>
<td><span data-ttu-id="dc283-358">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-358">10001</span></span></td>
<td><span data-ttu-id="dc283-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-359">Electricity</span></span></td>
<td><span data-ttu-id="dc283-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-360">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="dc283-361">7,714.29</span></span></td>
<td><span data-ttu-id="dc283-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="dc283-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="dc283-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="dc283-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="dc283-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="dc283-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="dc283-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="dc283-367">Define the overhead rate</span></span>

<span data-ttu-id="dc283-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="dc283-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="dc283-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="dc283-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-370">Cost object</span></span></th>
<th><span data-ttu-id="dc283-371">Часы</span><span class="sxs-lookup"><span data-stu-id="dc283-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-372">Proj 1</span></span></td>
<td><span data-ttu-id="dc283-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-373">Project 1</span></span></td>
<td><span data-ttu-id="dc283-374">3</span><span class="sxs-lookup"><span data-stu-id="dc283-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-375">Proj 2</span></span></td>
<td><span data-ttu-id="dc283-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-376">Project 2</span></span></td>
<td><span data-ttu-id="dc283-377">1</span><span class="sxs-lookup"><span data-stu-id="dc283-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-379">Cost object</span></span></th>
<th><span data-ttu-id="dc283-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-380">Cost element</span></span></th>
<th><span data-ttu-id="dc283-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-381">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="dc283-382">Units</span></span></th>
<th><span data-ttu-id="dc283-383">По норме</span><span class="sxs-lookup"><span data-stu-id="dc283-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-384">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-384">CC001</span></span></td>
<td><span data-ttu-id="dc283-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-385">HR</span></span></td>
<td><span data-ttu-id="dc283-386">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-386">10001</span></span></td>
<td><span data-ttu-id="dc283-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-387">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-388">1</span><span class="sxs-lookup"><span data-stu-id="dc283-388">1</span></span></td>
<td><span data-ttu-id="dc283-389">10</span><span class="sxs-lookup"><span data-stu-id="dc283-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-391">Cost object</span></span></th>
<th><span data-ttu-id="dc283-392">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-392">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-393">Cost element</span></span></th>
<th><span data-ttu-id="dc283-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-394">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-396">Proj 1</span></span></td>
<td><span data-ttu-id="dc283-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-397">Project 1</span></span></td>
<td><span data-ttu-id="dc283-398">3</span><span class="sxs-lookup"><span data-stu-id="dc283-398">3</span></span></td>
<td><span data-ttu-id="dc283-399">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-399">10001</span></span></td>
<td><span data-ttu-id="dc283-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="dc283-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="dc283-401">30.00</span><span class="sxs-lookup"><span data-stu-id="dc283-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-402">Proj 2</span></span></td>
<td><span data-ttu-id="dc283-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-403">Project 2</span></span></td>
<td><span data-ttu-id="dc283-404">1</span><span class="sxs-lookup"><span data-stu-id="dc283-404">1</span></span></td>
<td><span data-ttu-id="dc283-405">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-405">10001</span></span></td>
<td><span data-ttu-id="dc283-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="dc283-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="dc283-407">10,00</span><span class="sxs-lookup"><span data-stu-id="dc283-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="dc283-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-409">Journal</span></span></th>
<th><span data-ttu-id="dc283-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="dc283-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dc283-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="dc283-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dc283-412">Версия</span><span class="sxs-lookup"><span data-stu-id="dc283-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-413">00003</span><span class="sxs-lookup"><span data-stu-id="dc283-413">00003</span></span></td>
<td><span data-ttu-id="dc283-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="dc283-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="dc283-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="dc283-415">Fiscal</span></span></td>
<td><span data-ttu-id="dc283-416">2017</span><span class="sxs-lookup"><span data-stu-id="dc283-416">2017</span></span></td>
<td><span data-ttu-id="dc283-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-417">Period 1</span></span></td>
<td><span data-ttu-id="dc283-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="dc283-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="dc283-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-421">Cost object</span></span></th>
<th><span data-ttu-id="dc283-422">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-424">Proj 1</span></span></td>
<td><span data-ttu-id="dc283-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="dc283-426">3,00</span><span class="sxs-lookup"><span data-stu-id="dc283-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-428">Proj 2</span></span></td>
<td><span data-ttu-id="dc283-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="dc283-430">1.00</span><span class="sxs-lookup"><span data-stu-id="dc283-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dc283-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-433">Cost element</span></span></th>
<th><span data-ttu-id="dc283-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-434">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-435">Amount</span></span></th>
<th><span data-ttu-id="dc283-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="dc283-437">CC0001</span></span></td>
<td><span data-ttu-id="dc283-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-438">HR</span></span></td>
<td><span data-ttu-id="dc283-439">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-439">10001</span></span></td>
<td><span data-ttu-id="dc283-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-440">Electricity</span></span></td>
<td><span data-ttu-id="dc283-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-441">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="dc283-442">-30.00</span></span></td>
<td><span data-ttu-id="dc283-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-444">Proj 1</span></span></td>
<td><span data-ttu-id="dc283-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="dc283-446">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-446">10001</span></span></td>
<td><span data-ttu-id="dc283-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-447">Electricity</span></span></td>
<td><span data-ttu-id="dc283-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-448">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-449">30.00</span><span class="sxs-lookup"><span data-stu-id="dc283-449">30.00</span></span></td>
<td><span data-ttu-id="dc283-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-451">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-451">CC001</span></span></td>
<td><span data-ttu-id="dc283-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-452">HR</span></span></td>
<td><span data-ttu-id="dc283-453">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-453">10001</span></span></td>
<td><span data-ttu-id="dc283-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-454">Electricity</span></span></td>
<td><span data-ttu-id="dc283-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-455">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="dc283-456">-10.00</span></span></td>
<td><span data-ttu-id="dc283-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-458">Proj 2</span></span></td>
<td><span data-ttu-id="dc283-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="dc283-460">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-460">10001</span></span></td>
<td><span data-ttu-id="dc283-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-461">Electricity</span></span></td>
<td><span data-ttu-id="dc283-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-462">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-463">10.00</span><span class="sxs-lookup"><span data-stu-id="dc283-463">10.00</span></span></td>
<td><span data-ttu-id="dc283-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="dc283-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="dc283-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="dc283-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="dc283-468">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="dc283-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="dc283-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="dc283-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="dc283-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="dc283-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="dc283-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="dc283-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="dc283-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="dc283-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="dc283-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="dc283-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="dc283-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="dc283-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-475">Define the cost allocation</span></span>

<span data-ttu-id="dc283-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="dc283-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="dc283-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="dc283-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-479">Cost object</span></span></th>
<th><span data-ttu-id="dc283-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-481">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-481">CC002</span></span></td>
<td><span data-ttu-id="dc283-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-482">Finance</span></span></td>
<td><span data-ttu-id="dc283-483">35</span><span class="sxs-lookup"><span data-stu-id="dc283-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-484">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-484">CC003</span></span></td>
<td><span data-ttu-id="dc283-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-485">Assembly</span></span></td>
<td><span data-ttu-id="dc283-486">55</span><span class="sxs-lookup"><span data-stu-id="dc283-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-487">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-487">CC004</span></span></td>
<td><span data-ttu-id="dc283-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-488">Packaging</span></span></td>
<td><span data-ttu-id="dc283-489">10</span><span class="sxs-lookup"><span data-stu-id="dc283-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="dc283-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="dc283-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-492">Cost object</span></span></th>
<th><span data-ttu-id="dc283-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="dc283-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-494">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-494">CC003</span></span></td>
<td><span data-ttu-id="dc283-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-495">Assembly</span></span></td>
<td><span data-ttu-id="dc283-496">65</span><span class="sxs-lookup"><span data-stu-id="dc283-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-497">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-497">CC004</span></span></td>
<td><span data-ttu-id="dc283-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-498">Packaging</span></span></td>
<td><span data-ttu-id="dc283-499">35</span><span class="sxs-lookup"><span data-stu-id="dc283-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="dc283-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="dc283-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-502">Cost object</span></span></th>
<th><span data-ttu-id="dc283-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="dc283-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-504">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-505">Product 1</span></span></td>
<td><span data-ttu-id="dc283-506">60</span><span class="sxs-lookup"><span data-stu-id="dc283-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-507">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-508">Product 2</span></span></td>
<td><span data-ttu-id="dc283-509">20</span><span class="sxs-lookup"><span data-stu-id="dc283-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="dc283-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="dc283-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-512">Cost object</span></span></th>
<th><span data-ttu-id="dc283-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="dc283-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-514">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-515">Product 1</span></span></td>
<td><span data-ttu-id="dc283-516">80</span><span class="sxs-lookup"><span data-stu-id="dc283-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-517">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-518">Product 2</span></span></td>
<td><span data-ttu-id="dc283-519">15</span><span class="sxs-lookup"><span data-stu-id="dc283-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dc283-520">В Finance and Operations статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="dc283-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="dc283-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="dc283-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="dc283-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="dc283-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-523">Cost object</span></span></th>
<th><span data-ttu-id="dc283-524">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-524">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-525">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-526">Amount</span></span></th>
<th><span data-ttu-id="dc283-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-528">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-528">CC002</span></span></td>
<td><span data-ttu-id="dc283-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-529">Finance</span></span></td>
<td><span data-ttu-id="dc283-530">35</span><span class="sxs-lookup"><span data-stu-id="dc283-530">35</span></span></td>
<td><span data-ttu-id="dc283-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="dc283-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dc283-532">175.00</span><span class="sxs-lookup"><span data-stu-id="dc283-532">175.00</span></span></td>
<td><span data-ttu-id="dc283-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-534">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-534">CC003</span></span></td>
<td><span data-ttu-id="dc283-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-535">Assembly</span></span></td>
<td><span data-ttu-id="dc283-536">55</span><span class="sxs-lookup"><span data-stu-id="dc283-536">55</span></span></td>
<td><span data-ttu-id="dc283-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="dc283-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dc283-538">275.00</span><span class="sxs-lookup"><span data-stu-id="dc283-538">275.00</span></span></td>
<td><span data-ttu-id="dc283-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-540">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-540">CC004</span></span></td>
<td><span data-ttu-id="dc283-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-541">Packaging</span></span></td>
<td><span data-ttu-id="dc283-542">10</span><span class="sxs-lookup"><span data-stu-id="dc283-542">10</span></span></td>
<td><span data-ttu-id="dc283-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="dc283-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dc283-544">50,00</span><span class="sxs-lookup"><span data-stu-id="dc283-544">50.00</span></span></td>
<td><span data-ttu-id="dc283-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-546">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-546">CC002</span></span></td>
<td><span data-ttu-id="dc283-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-547">Finance</span></span></td>
<td><span data-ttu-id="dc283-548">35</span><span class="sxs-lookup"><span data-stu-id="dc283-548">35</span></span></td>
<td><span data-ttu-id="dc283-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="dc283-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dc283-550">436.00</span><span class="sxs-lookup"><span data-stu-id="dc283-550">436.00</span></span></td>
<td><span data-ttu-id="dc283-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-552">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-552">CC003</span></span></td>
<td><span data-ttu-id="dc283-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-553">Assembly</span></span></td>
<td><span data-ttu-id="dc283-554">55</span><span class="sxs-lookup"><span data-stu-id="dc283-554">55</span></span></td>
<td><span data-ttu-id="dc283-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="dc283-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dc283-556">685.14</span><span class="sxs-lookup"><span data-stu-id="dc283-556">685.14</span></span></td>
<td><span data-ttu-id="dc283-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-558">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-558">CC004</span></span></td>
<td><span data-ttu-id="dc283-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-559">Packaging</span></span></td>
<td><span data-ttu-id="dc283-560">10</span><span class="sxs-lookup"><span data-stu-id="dc283-560">10</span></span></td>
<td><span data-ttu-id="dc283-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="dc283-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dc283-562">124.57</span><span class="sxs-lookup"><span data-stu-id="dc283-562">124.57</span></span></td>
<td><span data-ttu-id="dc283-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="dc283-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-565">Cost object</span></span></th>
<th><span data-ttu-id="dc283-566">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-566">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-567">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-568">Amount</span></span></th>
<th><span data-ttu-id="dc283-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-570">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-570">CC003</span></span></td>
<td><span data-ttu-id="dc283-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-571">Assembly</span></span></td>
<td><span data-ttu-id="dc283-572">65</span><span class="sxs-lookup"><span data-stu-id="dc283-572">65</span></span></td>
<td><span data-ttu-id="dc283-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="dc283-574">438.75</span><span class="sxs-lookup"><span data-stu-id="dc283-574">438.75</span></span></td>
<td><span data-ttu-id="dc283-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-576">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-576">CC004</span></span></td>
<td><span data-ttu-id="dc283-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-577">Packaging</span></span></td>
<td><span data-ttu-id="dc283-578">35</span><span class="sxs-lookup"><span data-stu-id="dc283-578">35</span></span></td>
<td><span data-ttu-id="dc283-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="dc283-580">236.25</span><span class="sxs-lookup"><span data-stu-id="dc283-580">236.25</span></span></td>
<td><span data-ttu-id="dc283-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-582">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-582">CC003</span></span></td>
<td><span data-ttu-id="dc283-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-583">Assembly</span></span></td>
<td><span data-ttu-id="dc283-584">65</span><span class="sxs-lookup"><span data-stu-id="dc283-584">65</span></span></td>
<td><span data-ttu-id="dc283-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="dc283-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="dc283-586">5,297.69</span></span></td>
<td><span data-ttu-id="dc283-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-588">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-588">CC004</span></span></td>
<td><span data-ttu-id="dc283-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-589">Packaging</span></span></td>
<td><span data-ttu-id="dc283-590">35</span><span class="sxs-lookup"><span data-stu-id="dc283-590">35</span></span></td>
<td><span data-ttu-id="dc283-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="dc283-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="dc283-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="dc283-592">2,852.60</span></span></td>
<td><span data-ttu-id="dc283-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="dc283-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-595">Cost object</span></span></th>
<th><span data-ttu-id="dc283-596">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-596">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-597">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-598">Amount</span></span></th>
<th><span data-ttu-id="dc283-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-600">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-601">Product 1</span></span></td>
<td><span data-ttu-id="dc283-602">60</span><span class="sxs-lookup"><span data-stu-id="dc283-602">60</span></span></td>
<td><span data-ttu-id="dc283-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="dc283-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="dc283-604">535.31</span><span class="sxs-lookup"><span data-stu-id="dc283-604">535.31</span></span></td>
<td><span data-ttu-id="dc283-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-606">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-607">Product 2</span></span></td>
<td><span data-ttu-id="dc283-608">20</span><span class="sxs-lookup"><span data-stu-id="dc283-608">20</span></span></td>
<td><span data-ttu-id="dc283-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="dc283-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="dc283-610">178.44</span><span class="sxs-lookup"><span data-stu-id="dc283-610">178.44</span></span></td>
<td><span data-ttu-id="dc283-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-612">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-613">Product 1</span></span></td>
<td><span data-ttu-id="dc283-614">60</span><span class="sxs-lookup"><span data-stu-id="dc283-614">60</span></span></td>
<td><span data-ttu-id="dc283-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="dc283-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="dc283-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="dc283-616">4,487.12</span></span></td>
<td><span data-ttu-id="dc283-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-618">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-619">Product 2</span></span></td>
<td><span data-ttu-id="dc283-620">20</span><span class="sxs-lookup"><span data-stu-id="dc283-620">20</span></span></td>
<td><span data-ttu-id="dc283-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="dc283-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="dc283-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="dc283-622">1,495.71</span></span></td>
<td><span data-ttu-id="dc283-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc283-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="dc283-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-625">Cost object</span></span></th>
<th><span data-ttu-id="dc283-626">Величина</span><span class="sxs-lookup"><span data-stu-id="dc283-626">Magnitude</span></span></th>
<th><span data-ttu-id="dc283-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="dc283-627">Allocation factor</span></span></th>
<th><span data-ttu-id="dc283-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-628">Amount</span></span></th>
<th><span data-ttu-id="dc283-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-630">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-631">Product 1</span></span></td>
<td><span data-ttu-id="dc283-632">80</span><span class="sxs-lookup"><span data-stu-id="dc283-632">80</span></span></td>
<td><span data-ttu-id="dc283-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="dc283-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="dc283-634">241.05</span><span class="sxs-lookup"><span data-stu-id="dc283-634">241.05</span></span></td>
<td><span data-ttu-id="dc283-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-636">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-637">Product 2</span></span></td>
<td><span data-ttu-id="dc283-638">15</span><span class="sxs-lookup"><span data-stu-id="dc283-638">15</span></span></td>
<td><span data-ttu-id="dc283-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="dc283-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="dc283-640">45.20</span><span class="sxs-lookup"><span data-stu-id="dc283-640">45.20</span></span></td>
<td><span data-ttu-id="dc283-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-642">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-643">Product 1</span></span></td>
<td><span data-ttu-id="dc283-644">80</span><span class="sxs-lookup"><span data-stu-id="dc283-644">80</span></span></td>
<td><span data-ttu-id="dc283-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="dc283-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="dc283-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="dc283-646">2,507.09</span></span></td>
<td><span data-ttu-id="dc283-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-648">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-649">Product 2</span></span></td>
<td><span data-ttu-id="dc283-650">15</span><span class="sxs-lookup"><span data-stu-id="dc283-650">15</span></span></td>
<td><span data-ttu-id="dc283-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="dc283-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="dc283-652">470.08</span><span class="sxs-lookup"><span data-stu-id="dc283-652">470.08</span></span></td>
<td><span data-ttu-id="dc283-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dc283-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="dc283-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="dc283-655">Journal</span></span></th>
<th><span data-ttu-id="dc283-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="dc283-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dc283-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="dc283-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dc283-658">Версия</span><span class="sxs-lookup"><span data-stu-id="dc283-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-659">00004</span><span class="sxs-lookup"><span data-stu-id="dc283-659">00004</span></span></td>
<td><span data-ttu-id="dc283-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="dc283-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="dc283-661">Fiscal</span></span></td>
<td><span data-ttu-id="dc283-662">2017</span><span class="sxs-lookup"><span data-stu-id="dc283-662">2017</span></span></td>
<td><span data-ttu-id="dc283-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-663">Period 1</span></span></td>
<td><span data-ttu-id="dc283-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="dc283-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="dc283-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="dc283-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dc283-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-668">Cost element</span></span></th>
<th><span data-ttu-id="dc283-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-669">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-672">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-672">CC001</span></span></td>
<td><span data-ttu-id="dc283-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-673">HR</span></span></td>
<td><span data-ttu-id="dc283-674">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-674">10001</span></span></td>
<td><span data-ttu-id="dc283-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-675">Electricity</span></span></td>
<td><span data-ttu-id="dc283-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-676">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-677">500.00</span><span class="sxs-lookup"><span data-stu-id="dc283-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-679">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-679">CC001</span></span></td>
<td><span data-ttu-id="dc283-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-680">HR</span></span></td>
<td><span data-ttu-id="dc283-681">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-681">10001</span></span></td>
<td><span data-ttu-id="dc283-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-682">Electricity</span></span></td>
<td><span data-ttu-id="dc283-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-683">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="dc283-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-686">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-686">CC002</span></span></td>
<td><span data-ttu-id="dc283-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-687">Finance</span></span></td>
<td><span data-ttu-id="dc283-688">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-688">10001</span></span></td>
<td><span data-ttu-id="dc283-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-689">Electricity</span></span></td>
<td><span data-ttu-id="dc283-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-690">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-691">675.00</span><span class="sxs-lookup"><span data-stu-id="dc283-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-693">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-693">CC002</span></span></td>
<td><span data-ttu-id="dc283-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-694">Finance</span></span></td>
<td><span data-ttu-id="dc283-695">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-695">10001</span></span></td>
<td><span data-ttu-id="dc283-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-696">Electricity</span></span></td>
<td><span data-ttu-id="dc283-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-697">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="dc283-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-700">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-700">CC003</span></span></td>
<td><span data-ttu-id="dc283-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-701">Assembly</span></span></td>
<td><span data-ttu-id="dc283-702">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-702">10001</span></span></td>
<td><span data-ttu-id="dc283-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-703">Electricity</span></span></td>
<td><span data-ttu-id="dc283-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-704">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-705">713.75</span><span class="sxs-lookup"><span data-stu-id="dc283-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-707">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-707">CC003</span></span></td>
<td><span data-ttu-id="dc283-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-708">Assembly</span></span></td>
<td><span data-ttu-id="dc283-709">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-709">10001</span></span></td>
<td><span data-ttu-id="dc283-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-710">Electricity</span></span></td>
<td><span data-ttu-id="dc283-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-711">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="dc283-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-714">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-714">CC003</span></span></td>
<td><span data-ttu-id="dc283-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-715">Packaging</span></span></td>
<td><span data-ttu-id="dc283-716">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-716">10001</span></span></td>
<td><span data-ttu-id="dc283-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-717">Electricity</span></span></td>
<td><span data-ttu-id="dc283-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-718">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-719">286.25</span><span class="sxs-lookup"><span data-stu-id="dc283-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-721">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-721">CC003</span></span></td>
<td><span data-ttu-id="dc283-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-722">Packaging</span></span></td>
<td><span data-ttu-id="dc283-723">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-723">10001</span></span></td>
<td><span data-ttu-id="dc283-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-724">Electricity</span></span></td>
<td><span data-ttu-id="dc283-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-725">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="dc283-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-728">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-729">Product 1</span></span></td>
<td><span data-ttu-id="dc283-730">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-730">10001</span></span></td>
<td><span data-ttu-id="dc283-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-731">Electricity</span></span></td>
<td><span data-ttu-id="dc283-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-732">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-733">776.36</span><span class="sxs-lookup"><span data-stu-id="dc283-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-735">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-736">Product 1</span></span></td>
<td><span data-ttu-id="dc283-737">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-737">10001</span></span></td>
<td><span data-ttu-id="dc283-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-738">Electricity</span></span></td>
<td><span data-ttu-id="dc283-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-739">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="dc283-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-742">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-743">Product 1</span></span></td>
<td><span data-ttu-id="dc283-744">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-744">10001</span></span></td>
<td><span data-ttu-id="dc283-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-745">Electricity</span></span></td>
<td><span data-ttu-id="dc283-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-746">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-747">223.64</span><span class="sxs-lookup"><span data-stu-id="dc283-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="dc283-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-749">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-750">Product 1</span></span></td>
<td><span data-ttu-id="dc283-751">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-751">10001</span></span></td>
<td><span data-ttu-id="dc283-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-752">Electricity</span></span></td>
<td><span data-ttu-id="dc283-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-753">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="dc283-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dc283-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dc283-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dc283-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-757">Cost element</span></span></th>
<th><span data-ttu-id="dc283-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-758">Cost behavior</span></span></th>
<th><span data-ttu-id="dc283-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="dc283-759">Amount</span></span></th>
<th><span data-ttu-id="dc283-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="dc283-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dc283-761">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-761">CC001</span></span></td>
<td><span data-ttu-id="dc283-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-762">HR</span></span></td>
<td><span data-ttu-id="dc283-763">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-763">10001</span></span></td>
<td><span data-ttu-id="dc283-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-764">Electricity</span></span></td>
<td><span data-ttu-id="dc283-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-765">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="dc283-766">-500.00</span></span></td>
<td><span data-ttu-id="dc283-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-768">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-768">CC002</span></span></td>
<td><span data-ttu-id="dc283-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-769">Finance</span></span></td>
<td><span data-ttu-id="dc283-770">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-770">10001</span></span></td>
<td><span data-ttu-id="dc283-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-771">Electricity</span></span></td>
<td><span data-ttu-id="dc283-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-772">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-773">175.00</span><span class="sxs-lookup"><span data-stu-id="dc283-773">175.00</span></span></td>
<td><span data-ttu-id="dc283-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-775">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-775">CC003</span></span></td>
<td><span data-ttu-id="dc283-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-776">Assembly</span></span></td>
<td><span data-ttu-id="dc283-777">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-777">10001</span></span></td>
<td><span data-ttu-id="dc283-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-778">Electricity</span></span></td>
<td><span data-ttu-id="dc283-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-779">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-780">275.00</span><span class="sxs-lookup"><span data-stu-id="dc283-780">275.00</span></span></td>
<td><span data-ttu-id="dc283-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-782">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-782">CC004</span></span></td>
<td><span data-ttu-id="dc283-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-783">Packaging</span></span></td>
<td><span data-ttu-id="dc283-784">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-784">10001</span></span></td>
<td><span data-ttu-id="dc283-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-785">Electricity</span></span></td>
<td><span data-ttu-id="dc283-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-786">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-787">50,00</span><span class="sxs-lookup"><span data-stu-id="dc283-787">50,00</span></span></td>
<td><span data-ttu-id="dc283-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-789">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-789">CC001</span></span></td>
<td><span data-ttu-id="dc283-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="dc283-790">HR</span></span></td>
<td><span data-ttu-id="dc283-791">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-791">10001</span></span></td>
<td><span data-ttu-id="dc283-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-792">Electricity</span></span></td>
<td><span data-ttu-id="dc283-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-793">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="dc283-794">-1,245.71</span></span></td>
<td><span data-ttu-id="dc283-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-796">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-796">CC002</span></span></td>
<td><span data-ttu-id="dc283-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-797">Finance</span></span></td>
<td><span data-ttu-id="dc283-798">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-798">10001</span></span></td>
<td><span data-ttu-id="dc283-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-799">Electricity</span></span></td>
<td><span data-ttu-id="dc283-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-800">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-801">436.00</span><span class="sxs-lookup"><span data-stu-id="dc283-801">436.00</span></span></td>
<td><span data-ttu-id="dc283-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-803">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-803">CC003</span></span></td>
<td><span data-ttu-id="dc283-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-804">Assembly</span></span></td>
<td><span data-ttu-id="dc283-805">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-805">10001</span></span></td>
<td><span data-ttu-id="dc283-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-806">Electricity</span></span></td>
<td><span data-ttu-id="dc283-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-807">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-808">685.14</span><span class="sxs-lookup"><span data-stu-id="dc283-808">685.14</span></span></td>
<td><span data-ttu-id="dc283-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-810">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-810">CC004</span></span></td>
<td><span data-ttu-id="dc283-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-811">Packaging</span></span></td>
<td><span data-ttu-id="dc283-812">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-812">10001</span></span></td>
<td><span data-ttu-id="dc283-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-813">Electricity</span></span></td>
<td><span data-ttu-id="dc283-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-814">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-815">124.57</span><span class="sxs-lookup"><span data-stu-id="dc283-815">124.57</span></span></td>
<td><span data-ttu-id="dc283-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-817">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-817">CC002</span></span></td>
<td><span data-ttu-id="dc283-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-818">Finance</span></span></td>
<td><span data-ttu-id="dc283-819">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-819">10001</span></span></td>
<td><span data-ttu-id="dc283-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-820">Electricity</span></span></td>
<td><span data-ttu-id="dc283-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-821">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="dc283-822">-675.00</span></span></td>
<td><span data-ttu-id="dc283-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-824">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-824">CC003</span></span></td>
<td><span data-ttu-id="dc283-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-825">Assembly</span></span></td>
<td><span data-ttu-id="dc283-826">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-826">10001</span></span></td>
<td><span data-ttu-id="dc283-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-827">Electricity</span></span></td>
<td><span data-ttu-id="dc283-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-828">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-829">438.75</span><span class="sxs-lookup"><span data-stu-id="dc283-829">438.75</span></span></td>
<td><span data-ttu-id="dc283-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-831">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-831">CC004</span></span></td>
<td><span data-ttu-id="dc283-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-832">Packaging</span></span></td>
<td><span data-ttu-id="dc283-833">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-833">10001</span></span></td>
<td><span data-ttu-id="dc283-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-834">Electricity</span></span></td>
<td><span data-ttu-id="dc283-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-835">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-836">236.25</span><span class="sxs-lookup"><span data-stu-id="dc283-836">236.25</span></span></td>
<td><span data-ttu-id="dc283-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-838">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-838">CC002</span></span></td>
<td><span data-ttu-id="dc283-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="dc283-839">Finance</span></span></td>
<td><span data-ttu-id="dc283-840">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-840">10001</span></span></td>
<td><span data-ttu-id="dc283-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-841">Electricity</span></span></td>
<td><span data-ttu-id="dc283-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-842">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="dc283-843">-8,150.29</span></span></td>
<td><span data-ttu-id="dc283-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-845">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-845">CC003</span></span></td>
<td><span data-ttu-id="dc283-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-846">Assembly</span></span></td>
<td><span data-ttu-id="dc283-847">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-847">10001</span></span></td>
<td><span data-ttu-id="dc283-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-848">Electricity</span></span></td>
<td><span data-ttu-id="dc283-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-849">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="dc283-850">5,297.69</span></span></td>
<td><span data-ttu-id="dc283-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-852">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-852">CC004</span></span></td>
<td><span data-ttu-id="dc283-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="dc283-853">Packaging</span></span></td>
<td><span data-ttu-id="dc283-854">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-854">10001</span></span></td>
<td><span data-ttu-id="dc283-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-855">Electricity</span></span></td>
<td><span data-ttu-id="dc283-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-856">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="dc283-857">2,852.60</span></span></td>
<td><span data-ttu-id="dc283-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-859">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-859">CC003</span></span></td>
<td><span data-ttu-id="dc283-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-860">Assembly</span></span></td>
<td><span data-ttu-id="dc283-861">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-861">10001</span></span></td>
<td><span data-ttu-id="dc283-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-862">Electricity</span></span></td>
<td><span data-ttu-id="dc283-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-863">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="dc283-864">-713.75</span></span></td>
<td><span data-ttu-id="dc283-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-866">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-867">Product 1</span></span></td>
<td><span data-ttu-id="dc283-868">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-868">10001</span></span></td>
<td><span data-ttu-id="dc283-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-869">Electricity</span></span></td>
<td><span data-ttu-id="dc283-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-870">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-871">535.31</span><span class="sxs-lookup"><span data-stu-id="dc283-871">535.31</span></span></td>
<td><span data-ttu-id="dc283-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-873">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-874">Product 2</span></span></td>
<td><span data-ttu-id="dc283-875">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-875">10001</span></span></td>
<td><span data-ttu-id="dc283-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-876">Electricity</span></span></td>
<td><span data-ttu-id="dc283-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-877">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-878">178.44</span><span class="sxs-lookup"><span data-stu-id="dc283-878">178.44</span></span></td>
<td><span data-ttu-id="dc283-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-880">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-880">CC003</span></span></td>
<td><span data-ttu-id="dc283-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-881">Assembly</span></span></td>
<td><span data-ttu-id="dc283-882">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-882">10001</span></span></td>
<td><span data-ttu-id="dc283-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-883">Electricity</span></span></td>
<td><span data-ttu-id="dc283-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-884">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="dc283-885">-5,982.83</span></span></td>
<td><span data-ttu-id="dc283-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-887">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-888">Product 1</span></span></td>
<td><span data-ttu-id="dc283-889">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-889">10001</span></span></td>
<td><span data-ttu-id="dc283-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-890">Electricity</span></span></td>
<td><span data-ttu-id="dc283-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-891">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="dc283-892">4,487.12</span></span></td>
<td><span data-ttu-id="dc283-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-894">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-895">Product 2</span></span></td>
<td><span data-ttu-id="dc283-896">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-896">10001</span></span></td>
<td><span data-ttu-id="dc283-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-897">Electricity</span></span></td>
<td><span data-ttu-id="dc283-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-898">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="dc283-899">1,495.71</span></span></td>
<td><span data-ttu-id="dc283-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-901">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-901">CC003</span></span></td>
<td><span data-ttu-id="dc283-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-902">Assembly</span></span></td>
<td><span data-ttu-id="dc283-903">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-903">10001</span></span></td>
<td><span data-ttu-id="dc283-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-904">Electricity</span></span></td>
<td><span data-ttu-id="dc283-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-905">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="dc283-906">-286.25</span></span></td>
<td><span data-ttu-id="dc283-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-908">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-909">Product 1</span></span></td>
<td><span data-ttu-id="dc283-910">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-910">10001</span></span></td>
<td><span data-ttu-id="dc283-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-911">Electricity</span></span></td>
<td><span data-ttu-id="dc283-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-912">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-913">241.05</span><span class="sxs-lookup"><span data-stu-id="dc283-913">241.05</span></span></td>
<td><span data-ttu-id="dc283-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-915">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-916">Product 2</span></span></td>
<td><span data-ttu-id="dc283-917">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-917">10001</span></span></td>
<td><span data-ttu-id="dc283-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-918">Electricity</span></span></td>
<td><span data-ttu-id="dc283-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-919">Fixed cost</span></span></td>
<td><span data-ttu-id="dc283-920">45.20</span><span class="sxs-lookup"><span data-stu-id="dc283-920">45.20</span></span></td>
<td><span data-ttu-id="dc283-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-922">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-922">CC003</span></span></td>
<td><span data-ttu-id="dc283-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="dc283-923">Assembly</span></span></td>
<td><span data-ttu-id="dc283-924">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-924">10001</span></span></td>
<td><span data-ttu-id="dc283-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-925">Electricity</span></span></td>
<td><span data-ttu-id="dc283-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-926">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="dc283-927">-2,977.17</span></span></td>
<td><span data-ttu-id="dc283-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-929">Prod 1</span></span></td>
<td><span data-ttu-id="dc283-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="dc283-930">Product 1</span></span></td>
<td><span data-ttu-id="dc283-931">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-931">10001</span></span></td>
<td><span data-ttu-id="dc283-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-932">Electricity</span></span></td>
<td><span data-ttu-id="dc283-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-933">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="dc283-934">2,507.09</span></span></td>
<td><span data-ttu-id="dc283-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dc283-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-936">Prod 2</span></span></td>
<td><span data-ttu-id="dc283-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="dc283-937">Product 2</span></span></td>
<td><span data-ttu-id="dc283-938">10001</span><span class="sxs-lookup"><span data-stu-id="dc283-938">10001</span></span></td>
<td><span data-ttu-id="dc283-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-939">Electricity</span></span></td>
<td><span data-ttu-id="dc283-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-940">Variable cost</span></span></td>
<td><span data-ttu-id="dc283-941">470.08</span><span class="sxs-lookup"><span data-stu-id="dc283-941">470.08</span></span></td>
<td><span data-ttu-id="dc283-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="dc283-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="dc283-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="dc283-943">Conclusion</span></span>
<span data-ttu-id="dc283-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="dc283-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="dc283-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="dc283-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="dc283-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="dc283-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="dc283-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="dc283-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="dc283-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="dc283-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="dc283-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dc283-951">CC099</span><span class="sxs-lookup"><span data-stu-id="dc283-951">CC099</span></span></th>
<th><span data-ttu-id="dc283-952">CC001</span><span class="sxs-lookup"><span data-stu-id="dc283-952">CC001</span></span></th>
<th><span data-ttu-id="dc283-953">CC002</span><span class="sxs-lookup"><span data-stu-id="dc283-953">CC002</span></span></th>
<th><span data-ttu-id="dc283-954">CC003</span><span class="sxs-lookup"><span data-stu-id="dc283-954">CC003</span></span></th>
<th><span data-ttu-id="dc283-955">CC004</span><span class="sxs-lookup"><span data-stu-id="dc283-955">CC004</span></span></th>
<th><span data-ttu-id="dc283-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="dc283-956">Proj 1</span></span></th>
<th><span data-ttu-id="dc283-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="dc283-957">Proj 2</span></span></th>
<th><span data-ttu-id="dc283-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="dc283-958">Prod 1</span></span></th>
<th><span data-ttu-id="dc283-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="dc283-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="dc283-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="dc283-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="dc283-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="dc283-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="dc283-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-971">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="dc283-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-973">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-974">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-975">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-976">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-977">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="dc283-978">776.36</span><span class="sxs-lookup"><span data-stu-id="dc283-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-979">223.64</span><span class="sxs-lookup"><span data-stu-id="dc283-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="dc283-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="dc283-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-982">000</span><span class="sxs-lookup"><span data-stu-id="dc283-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-983">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-984">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-985">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-986">0,00</span><span class="sxs-lookup"><span data-stu-id="dc283-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-987">30.00</span><span class="sxs-lookup"><span data-stu-id="dc283-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-988">10,00</span><span class="sxs-lookup"><span data-stu-id="dc283-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="dc283-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="dc283-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dc283-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="dc283-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dc283-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="dc283-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="dc283-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="dc283-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="dc283-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="dc283-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="dc283-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="dc283-996">Дополнительные сведения см. в разделе [Свертка затрат](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="dc283-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



