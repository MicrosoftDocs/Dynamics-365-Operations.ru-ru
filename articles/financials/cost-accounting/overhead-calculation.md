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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544063"
---
# <a name="overhead-calculation"></a><span data-ttu-id="d3179-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="d3179-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3179-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="d3179-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="d3179-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="d3179-105">Term definition</span></span>
---------------

<span data-ttu-id="d3179-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="d3179-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="d3179-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="d3179-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="d3179-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="d3179-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="d3179-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="d3179-109">Rent</span></span>
-   <span data-ttu-id="d3179-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-110">Electricity</span></span>
-   <span data-ttu-id="d3179-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="d3179-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="d3179-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="d3179-112">Overhead calculation overview</span></span>
<span data-ttu-id="d3179-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="d3179-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="d3179-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="d3179-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="d3179-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="d3179-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="d3179-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="d3179-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="d3179-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="d3179-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="d3179-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="d3179-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="d3179-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="d3179-119">Version type</span></span>
-   <span data-ttu-id="d3179-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="d3179-120">Date and time</span></span>
-   <span data-ttu-id="d3179-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="d3179-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="d3179-122">Fiscal year</span></span>
-   <span data-ttu-id="d3179-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="d3179-123">Fiscal period</span></span>

<span data-ttu-id="d3179-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="d3179-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="d3179-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="d3179-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="d3179-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d3179-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="d3179-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="d3179-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="d3179-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="d3179-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="d3179-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="d3179-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="d3179-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="d3179-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="d3179-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="d3179-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="d3179-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="d3179-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="d3179-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="d3179-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="d3179-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="d3179-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="d3179-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="d3179-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="d3179-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="d3179-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d3179-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="d3179-140">Main account</span></span></th>
<th><span data-ttu-id="d3179-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="d3179-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="d3179-143">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-143">CC099</span></span></td>
<td><span data-ttu-id="d3179-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-144">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-145">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-145">10001</span></span></td>
<td><span data-ttu-id="d3179-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-146">Electricity</span></span></td>
<td><span data-ttu-id="d3179-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d3179-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="d3179-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="d3179-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="d3179-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="d3179-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="d3179-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-151">Define the cost behavior rule</span></span>

<span data-ttu-id="d3179-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="d3179-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="d3179-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="d3179-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="d3179-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="d3179-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="d3179-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="d3179-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="d3179-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="d3179-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="d3179-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="d3179-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-160">Journal</span></span></th>
<th><span data-ttu-id="d3179-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="d3179-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d3179-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="d3179-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d3179-163">Версия</span><span class="sxs-lookup"><span data-stu-id="d3179-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-164">00001</span><span class="sxs-lookup"><span data-stu-id="d3179-164">00001</span></span></td>
<td><span data-ttu-id="d3179-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="d3179-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="d3179-166">Fiscal</span></span></td>
<td><span data-ttu-id="d3179-167">2017</span><span class="sxs-lookup"><span data-stu-id="d3179-167">2017</span></span></td>
<td><span data-ttu-id="d3179-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-168">Period 1</span></span></td>
<td><span data-ttu-id="d3179-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d3179-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="d3179-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-173">Cost element</span></span></th>
<th><span data-ttu-id="d3179-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-174">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="d3179-177">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-177">CC099</span></span></td>
<td><span data-ttu-id="d3179-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-178">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-179">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-179">10001</span></span></td>
<td><span data-ttu-id="d3179-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-180">Electricity</span></span></td>
<td><span data-ttu-id="d3179-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="d3179-181">Unclassified</span></span></td>
<td><span data-ttu-id="d3179-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d3179-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d3179-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-185">Cost element</span></span></th>
<th><span data-ttu-id="d3179-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-186">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-187">Amount</span></span></th>
<th><span data-ttu-id="d3179-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-189">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-189">CC099</span></span></td>
<td><span data-ttu-id="d3179-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-190">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-191">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-191">10001</span></span></td>
<td><span data-ttu-id="d3179-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-192">Electricity</span></span></td>
<td><span data-ttu-id="d3179-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="d3179-193">Unclassified</span></span></td>
<td><span data-ttu-id="d3179-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d3179-194">10,000.00</span></span></td>
<td><span data-ttu-id="d3179-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-196">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-196">CC099</span></span></td>
<td><span data-ttu-id="d3179-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-197">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-198">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-198">10001</span></span></td>
<td><span data-ttu-id="d3179-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-199">Electricity</span></span></td>
<td><span data-ttu-id="d3179-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="d3179-200">Unclassified</span></span></td>
<td><span data-ttu-id="d3179-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-201">-10,000.00</span></span></td>
<td><span data-ttu-id="d3179-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-203">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-203">CC099</span></span></td>
<td><span data-ttu-id="d3179-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-204">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-205">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-205">10001</span></span></td>
<td><span data-ttu-id="d3179-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-206">Electricity</span></span></td>
<td><span data-ttu-id="d3179-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-207">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-208">1,000.00</span></span></td>
<td><span data-ttu-id="d3179-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-210">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-210">CC099</span></span></td>
<td><span data-ttu-id="d3179-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-211">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-212">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-212">10001</span></span></td>
<td><span data-ttu-id="d3179-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-213">Electricity</span></span></td>
<td><span data-ttu-id="d3179-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-214">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="d3179-215">9,000.00</span></span></td>
<td><span data-ttu-id="d3179-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="d3179-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="d3179-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="d3179-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="d3179-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="d3179-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-221">Define the cost distribution rule</span></span>

<span data-ttu-id="d3179-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="d3179-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="d3179-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="d3179-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="d3179-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="d3179-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="d3179-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="d3179-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="d3179-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="d3179-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="d3179-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-228">Cost object</span></span></th>
<th><span data-ttu-id="d3179-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="d3179-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-230">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-230">CC001</span></span></td>
<td><span data-ttu-id="d3179-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-231">HR</span></span></td>
<td><span data-ttu-id="d3179-232">1000</span><span class="sxs-lookup"><span data-stu-id="d3179-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-233">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-233">CC002</span></span></td>
<td><span data-ttu-id="d3179-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-234">Finance</span></span></td>
<td><span data-ttu-id="d3179-235">6,000</span><span class="sxs-lookup"><span data-stu-id="d3179-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-236">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-236">CC003</span></span></td>
<td><span data-ttu-id="d3179-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-237">Assembly</span></span></td>
<td><span data-ttu-id="d3179-238">0</span><span class="sxs-lookup"><span data-stu-id="d3179-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-240">Cost object</span></span></th>
<th><span data-ttu-id="d3179-241">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-241">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-242">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-244">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-244">CC001</span></span></td>
<td><span data-ttu-id="d3179-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-245">HR</span></span></td>
<td><span data-ttu-id="d3179-246">1000</span><span class="sxs-lookup"><span data-stu-id="d3179-246">1,000</span></span></td>
<td><span data-ttu-id="d3179-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d3179-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d3179-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-249">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-249">CC002</span></span></td>
<td><span data-ttu-id="d3179-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-250">Finance</span></span></td>
<td><span data-ttu-id="d3179-251">6,000</span><span class="sxs-lookup"><span data-stu-id="d3179-251">6,000</span></span></td>
<td><span data-ttu-id="d3179-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d3179-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d3179-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-254">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-254">CC003</span></span></td>
<td><span data-ttu-id="d3179-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-255">Assembly</span></span></td>
<td><span data-ttu-id="d3179-256">0</span><span class="sxs-lookup"><span data-stu-id="d3179-256">0</span></span></td>
<td><span data-ttu-id="d3179-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d3179-258">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="d3179-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="d3179-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-261">Cost object</span></span></th>
<th><span data-ttu-id="d3179-262">Формула</span><span class="sxs-lookup"><span data-stu-id="d3179-262">Formula</span></span></th>
<th><span data-ttu-id="d3179-263">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-263">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-264">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-266">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-266">CC001</span></span></td>
<td><span data-ttu-id="d3179-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-267">HR</span></span></td>
<td><span data-ttu-id="d3179-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d3179-269">1</span><span class="sxs-lookup"><span data-stu-id="d3179-269">1</span></span></td>
<td><span data-ttu-id="d3179-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d3179-271">500.00</span><span class="sxs-lookup"><span data-stu-id="d3179-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-272">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-272">CC002</span></span></td>
<td><span data-ttu-id="d3179-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-273">Finance</span></span></td>
<td><span data-ttu-id="d3179-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d3179-275">1</span><span class="sxs-lookup"><span data-stu-id="d3179-275">1</span></span></td>
<td><span data-ttu-id="d3179-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d3179-277">500.00</span><span class="sxs-lookup"><span data-stu-id="d3179-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-278">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-278">CC003</span></span></td>
<td><span data-ttu-id="d3179-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-279">Assembly</span></span></td>
<td><span data-ttu-id="d3179-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d3179-281">0</span><span class="sxs-lookup"><span data-stu-id="d3179-281">0</span></span></td>
<td><span data-ttu-id="d3179-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d3179-283">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d3179-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-285">Journal</span></span></th>
<th><span data-ttu-id="d3179-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="d3179-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d3179-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="d3179-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d3179-288">Версия</span><span class="sxs-lookup"><span data-stu-id="d3179-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-289">00002</span><span class="sxs-lookup"><span data-stu-id="d3179-289">00002</span></span></td>
<td><span data-ttu-id="d3179-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="d3179-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="d3179-291">Fiscal</span></span></td>
<td><span data-ttu-id="d3179-292">2017</span><span class="sxs-lookup"><span data-stu-id="d3179-292">2017</span></span></td>
<td><span data-ttu-id="d3179-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-293">Period 1</span></span></td>
<td><span data-ttu-id="d3179-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d3179-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="d3179-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-298">Cost element</span></span></th>
<th><span data-ttu-id="d3179-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-299">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-302">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-302">CC099</span></span></td>
<td><span data-ttu-id="d3179-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-303">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-304">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-304">10001</span></span></td>
<td><span data-ttu-id="d3179-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-305">Electricity</span></span></td>
<td><span data-ttu-id="d3179-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-306">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-309">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-309">CC099</span></span></td>
<td><span data-ttu-id="d3179-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-310">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-311">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-311">10001</span></span></td>
<td><span data-ttu-id="d3179-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-312">Electricity</span></span></td>
<td><span data-ttu-id="d3179-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-313">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="d3179-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d3179-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-317">Cost element</span></span></th>
<th><span data-ttu-id="d3179-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-318">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-319">Amount</span></span></th>
<th><span data-ttu-id="d3179-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-321">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-321">CC099</span></span></td>
<td><span data-ttu-id="d3179-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-322">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-323">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-323">10001</span></span></td>
<td><span data-ttu-id="d3179-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-324">Electricity</span></span></td>
<td><span data-ttu-id="d3179-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-325">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-326">-1,000.00</span></span></td>
<td><span data-ttu-id="d3179-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-328">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-328">CC001</span></span></td>
<td><span data-ttu-id="d3179-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-329">HR</span></span></td>
<td><span data-ttu-id="d3179-330">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-330">10001</span></span></td>
<td><span data-ttu-id="d3179-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-331">Electricity</span></span></td>
<td><span data-ttu-id="d3179-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-332">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-333">500.00</span><span class="sxs-lookup"><span data-stu-id="d3179-333">500.00</span></span></td>
<td><span data-ttu-id="d3179-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-335">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-335">CC002</span></span></td>
<td><span data-ttu-id="d3179-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-336">Finance</span></span></td>
<td><span data-ttu-id="d3179-337">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-337">10001</span></span></td>
<td><span data-ttu-id="d3179-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-338">Electricity</span></span></td>
<td><span data-ttu-id="d3179-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-339">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-340">500.00</span><span class="sxs-lookup"><span data-stu-id="d3179-340">500.00</span></span></td>
<td><span data-ttu-id="d3179-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-342">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-342">CC099</span></span></td>
<td><span data-ttu-id="d3179-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3179-343">Default cost center</span></span></td>
<td><span data-ttu-id="d3179-344">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-344">10001</span></span></td>
<td><span data-ttu-id="d3179-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-345">Electricity</span></span></td>
<td><span data-ttu-id="d3179-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-346">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="d3179-347">-9,000.00</span></span></td>
<td><span data-ttu-id="d3179-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-349">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-349">CC001</span></span></td>
<td><span data-ttu-id="d3179-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-350">HR</span></span></td>
<td><span data-ttu-id="d3179-351">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-351">10001</span></span></td>
<td><span data-ttu-id="d3179-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-352">Electricity</span></span></td>
<td><span data-ttu-id="d3179-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-353">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d3179-354">1,285.71</span></span></td>
<td><span data-ttu-id="d3179-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-356">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-356">CC002</span></span></td>
<td><span data-ttu-id="d3179-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-357">Finance</span></span></td>
<td><span data-ttu-id="d3179-358">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-358">10001</span></span></td>
<td><span data-ttu-id="d3179-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-359">Electricity</span></span></td>
<td><span data-ttu-id="d3179-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-360">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d3179-361">7,714.29</span></span></td>
<td><span data-ttu-id="d3179-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="d3179-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="d3179-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="d3179-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="d3179-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="d3179-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="d3179-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="d3179-367">Define the overhead rate</span></span>

<span data-ttu-id="d3179-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="d3179-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="d3179-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="d3179-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-370">Cost object</span></span></th>
<th><span data-ttu-id="d3179-371">Часы</span><span class="sxs-lookup"><span data-stu-id="d3179-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-372">Proj 1</span></span></td>
<td><span data-ttu-id="d3179-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-373">Project 1</span></span></td>
<td><span data-ttu-id="d3179-374">3</span><span class="sxs-lookup"><span data-stu-id="d3179-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-375">Proj 2</span></span></td>
<td><span data-ttu-id="d3179-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-376">Project 2</span></span></td>
<td><span data-ttu-id="d3179-377">1</span><span class="sxs-lookup"><span data-stu-id="d3179-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-379">Cost object</span></span></th>
<th><span data-ttu-id="d3179-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-380">Cost element</span></span></th>
<th><span data-ttu-id="d3179-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-381">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="d3179-382">Units</span></span></th>
<th><span data-ttu-id="d3179-383">По норме</span><span class="sxs-lookup"><span data-stu-id="d3179-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-384">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-384">CC001</span></span></td>
<td><span data-ttu-id="d3179-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-385">HR</span></span></td>
<td><span data-ttu-id="d3179-386">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-386">10001</span></span></td>
<td><span data-ttu-id="d3179-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-387">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-388">1</span><span class="sxs-lookup"><span data-stu-id="d3179-388">1</span></span></td>
<td><span data-ttu-id="d3179-389">10</span><span class="sxs-lookup"><span data-stu-id="d3179-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-391">Cost object</span></span></th>
<th><span data-ttu-id="d3179-392">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-392">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-393">Cost element</span></span></th>
<th><span data-ttu-id="d3179-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-394">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-396">Proj 1</span></span></td>
<td><span data-ttu-id="d3179-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-397">Project 1</span></span></td>
<td><span data-ttu-id="d3179-398">3</span><span class="sxs-lookup"><span data-stu-id="d3179-398">3</span></span></td>
<td><span data-ttu-id="d3179-399">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-399">10001</span></span></td>
<td><span data-ttu-id="d3179-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d3179-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d3179-401">30.00</span><span class="sxs-lookup"><span data-stu-id="d3179-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-402">Proj 2</span></span></td>
<td><span data-ttu-id="d3179-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-403">Project 2</span></span></td>
<td><span data-ttu-id="d3179-404">1</span><span class="sxs-lookup"><span data-stu-id="d3179-404">1</span></span></td>
<td><span data-ttu-id="d3179-405">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-405">10001</span></span></td>
<td><span data-ttu-id="d3179-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d3179-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d3179-407">10,00</span><span class="sxs-lookup"><span data-stu-id="d3179-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d3179-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-409">Journal</span></span></th>
<th><span data-ttu-id="d3179-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="d3179-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d3179-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="d3179-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d3179-412">Версия</span><span class="sxs-lookup"><span data-stu-id="d3179-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-413">00003</span><span class="sxs-lookup"><span data-stu-id="d3179-413">00003</span></span></td>
<td><span data-ttu-id="d3179-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="d3179-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="d3179-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="d3179-415">Fiscal</span></span></td>
<td><span data-ttu-id="d3179-416">2017</span><span class="sxs-lookup"><span data-stu-id="d3179-416">2017</span></span></td>
<td><span data-ttu-id="d3179-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-417">Period 1</span></span></td>
<td><span data-ttu-id="d3179-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="d3179-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="d3179-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-421">Cost object</span></span></th>
<th><span data-ttu-id="d3179-422">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-424">Proj 1</span></span></td>
<td><span data-ttu-id="d3179-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d3179-426">3,00</span><span class="sxs-lookup"><span data-stu-id="d3179-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-428">Proj 2</span></span></td>
<td><span data-ttu-id="d3179-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d3179-430">1.00</span><span class="sxs-lookup"><span data-stu-id="d3179-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d3179-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-433">Cost element</span></span></th>
<th><span data-ttu-id="d3179-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-434">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-435">Amount</span></span></th>
<th><span data-ttu-id="d3179-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="d3179-437">CC0001</span></span></td>
<td><span data-ttu-id="d3179-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-438">HR</span></span></td>
<td><span data-ttu-id="d3179-439">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-439">10001</span></span></td>
<td><span data-ttu-id="d3179-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-440">Electricity</span></span></td>
<td><span data-ttu-id="d3179-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-441">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="d3179-442">-30.00</span></span></td>
<td><span data-ttu-id="d3179-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-444">Proj 1</span></span></td>
<td><span data-ttu-id="d3179-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d3179-446">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-446">10001</span></span></td>
<td><span data-ttu-id="d3179-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-447">Electricity</span></span></td>
<td><span data-ttu-id="d3179-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-448">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-449">30.00</span><span class="sxs-lookup"><span data-stu-id="d3179-449">30.00</span></span></td>
<td><span data-ttu-id="d3179-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-451">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-451">CC001</span></span></td>
<td><span data-ttu-id="d3179-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-452">HR</span></span></td>
<td><span data-ttu-id="d3179-453">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-453">10001</span></span></td>
<td><span data-ttu-id="d3179-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-454">Electricity</span></span></td>
<td><span data-ttu-id="d3179-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-455">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="d3179-456">-10.00</span></span></td>
<td><span data-ttu-id="d3179-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-458">Proj 2</span></span></td>
<td><span data-ttu-id="d3179-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d3179-460">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-460">10001</span></span></td>
<td><span data-ttu-id="d3179-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-461">Electricity</span></span></td>
<td><span data-ttu-id="d3179-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-462">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-463">10.00</span><span class="sxs-lookup"><span data-stu-id="d3179-463">10.00</span></span></td>
<td><span data-ttu-id="d3179-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="d3179-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="d3179-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="d3179-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="d3179-468">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="d3179-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="d3179-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="d3179-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="d3179-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="d3179-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="d3179-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="d3179-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="d3179-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="d3179-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="d3179-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="d3179-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="d3179-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="d3179-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-475">Define the cost allocation</span></span>

<span data-ttu-id="d3179-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="d3179-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="d3179-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="d3179-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-479">Cost object</span></span></th>
<th><span data-ttu-id="d3179-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-481">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-481">CC002</span></span></td>
<td><span data-ttu-id="d3179-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-482">Finance</span></span></td>
<td><span data-ttu-id="d3179-483">35</span><span class="sxs-lookup"><span data-stu-id="d3179-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-484">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-484">CC003</span></span></td>
<td><span data-ttu-id="d3179-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-485">Assembly</span></span></td>
<td><span data-ttu-id="d3179-486">55</span><span class="sxs-lookup"><span data-stu-id="d3179-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-487">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-487">CC004</span></span></td>
<td><span data-ttu-id="d3179-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-488">Packaging</span></span></td>
<td><span data-ttu-id="d3179-489">10</span><span class="sxs-lookup"><span data-stu-id="d3179-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="d3179-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="d3179-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-492">Cost object</span></span></th>
<th><span data-ttu-id="d3179-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="d3179-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-494">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-494">CC003</span></span></td>
<td><span data-ttu-id="d3179-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-495">Assembly</span></span></td>
<td><span data-ttu-id="d3179-496">65</span><span class="sxs-lookup"><span data-stu-id="d3179-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-497">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-497">CC004</span></span></td>
<td><span data-ttu-id="d3179-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-498">Packaging</span></span></td>
<td><span data-ttu-id="d3179-499">35</span><span class="sxs-lookup"><span data-stu-id="d3179-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="d3179-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="d3179-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-502">Cost object</span></span></th>
<th><span data-ttu-id="d3179-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="d3179-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-504">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-505">Product 1</span></span></td>
<td><span data-ttu-id="d3179-506">60</span><span class="sxs-lookup"><span data-stu-id="d3179-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-507">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-508">Product 2</span></span></td>
<td><span data-ttu-id="d3179-509">20</span><span class="sxs-lookup"><span data-stu-id="d3179-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="d3179-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="d3179-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-512">Cost object</span></span></th>
<th><span data-ttu-id="d3179-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="d3179-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-514">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-515">Product 1</span></span></td>
<td><span data-ttu-id="d3179-516">80</span><span class="sxs-lookup"><span data-stu-id="d3179-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-517">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-518">Product 2</span></span></td>
<td><span data-ttu-id="d3179-519">15</span><span class="sxs-lookup"><span data-stu-id="d3179-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d3179-520">В Finance and Operations статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="d3179-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="d3179-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="d3179-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="d3179-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="d3179-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-523">Cost object</span></span></th>
<th><span data-ttu-id="d3179-524">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-524">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-525">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-526">Amount</span></span></th>
<th><span data-ttu-id="d3179-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-528">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-528">CC002</span></span></td>
<td><span data-ttu-id="d3179-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-529">Finance</span></span></td>
<td><span data-ttu-id="d3179-530">35</span><span class="sxs-lookup"><span data-stu-id="d3179-530">35</span></span></td>
<td><span data-ttu-id="d3179-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d3179-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d3179-532">175.00</span><span class="sxs-lookup"><span data-stu-id="d3179-532">175.00</span></span></td>
<td><span data-ttu-id="d3179-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-534">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-534">CC003</span></span></td>
<td><span data-ttu-id="d3179-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-535">Assembly</span></span></td>
<td><span data-ttu-id="d3179-536">55</span><span class="sxs-lookup"><span data-stu-id="d3179-536">55</span></span></td>
<td><span data-ttu-id="d3179-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d3179-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d3179-538">275.00</span><span class="sxs-lookup"><span data-stu-id="d3179-538">275.00</span></span></td>
<td><span data-ttu-id="d3179-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-540">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-540">CC004</span></span></td>
<td><span data-ttu-id="d3179-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-541">Packaging</span></span></td>
<td><span data-ttu-id="d3179-542">10</span><span class="sxs-lookup"><span data-stu-id="d3179-542">10</span></span></td>
<td><span data-ttu-id="d3179-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d3179-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d3179-544">50,00</span><span class="sxs-lookup"><span data-stu-id="d3179-544">50.00</span></span></td>
<td><span data-ttu-id="d3179-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-546">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-546">CC002</span></span></td>
<td><span data-ttu-id="d3179-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-547">Finance</span></span></td>
<td><span data-ttu-id="d3179-548">35</span><span class="sxs-lookup"><span data-stu-id="d3179-548">35</span></span></td>
<td><span data-ttu-id="d3179-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="d3179-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d3179-550">436.00</span><span class="sxs-lookup"><span data-stu-id="d3179-550">436.00</span></span></td>
<td><span data-ttu-id="d3179-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-552">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-552">CC003</span></span></td>
<td><span data-ttu-id="d3179-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-553">Assembly</span></span></td>
<td><span data-ttu-id="d3179-554">55</span><span class="sxs-lookup"><span data-stu-id="d3179-554">55</span></span></td>
<td><span data-ttu-id="d3179-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="d3179-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d3179-556">685.14</span><span class="sxs-lookup"><span data-stu-id="d3179-556">685.14</span></span></td>
<td><span data-ttu-id="d3179-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-558">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-558">CC004</span></span></td>
<td><span data-ttu-id="d3179-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-559">Packaging</span></span></td>
<td><span data-ttu-id="d3179-560">10</span><span class="sxs-lookup"><span data-stu-id="d3179-560">10</span></span></td>
<td><span data-ttu-id="d3179-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="d3179-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d3179-562">124.57</span><span class="sxs-lookup"><span data-stu-id="d3179-562">124.57</span></span></td>
<td><span data-ttu-id="d3179-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="d3179-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-565">Cost object</span></span></th>
<th><span data-ttu-id="d3179-566">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-566">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-567">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-568">Amount</span></span></th>
<th><span data-ttu-id="d3179-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-570">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-570">CC003</span></span></td>
<td><span data-ttu-id="d3179-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-571">Assembly</span></span></td>
<td><span data-ttu-id="d3179-572">65</span><span class="sxs-lookup"><span data-stu-id="d3179-572">65</span></span></td>
<td><span data-ttu-id="d3179-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d3179-574">438.75</span><span class="sxs-lookup"><span data-stu-id="d3179-574">438.75</span></span></td>
<td><span data-ttu-id="d3179-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-576">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-576">CC004</span></span></td>
<td><span data-ttu-id="d3179-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-577">Packaging</span></span></td>
<td><span data-ttu-id="d3179-578">35</span><span class="sxs-lookup"><span data-stu-id="d3179-578">35</span></span></td>
<td><span data-ttu-id="d3179-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d3179-580">236.25</span><span class="sxs-lookup"><span data-stu-id="d3179-580">236.25</span></span></td>
<td><span data-ttu-id="d3179-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-582">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-582">CC003</span></span></td>
<td><span data-ttu-id="d3179-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-583">Assembly</span></span></td>
<td><span data-ttu-id="d3179-584">65</span><span class="sxs-lookup"><span data-stu-id="d3179-584">65</span></span></td>
<td><span data-ttu-id="d3179-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d3179-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d3179-586">5,297.69</span></span></td>
<td><span data-ttu-id="d3179-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-588">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-588">CC004</span></span></td>
<td><span data-ttu-id="d3179-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-589">Packaging</span></span></td>
<td><span data-ttu-id="d3179-590">35</span><span class="sxs-lookup"><span data-stu-id="d3179-590">35</span></span></td>
<td><span data-ttu-id="d3179-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d3179-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d3179-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d3179-592">2,852.60</span></span></td>
<td><span data-ttu-id="d3179-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="d3179-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-595">Cost object</span></span></th>
<th><span data-ttu-id="d3179-596">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-596">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-597">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-598">Amount</span></span></th>
<th><span data-ttu-id="d3179-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-600">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-601">Product 1</span></span></td>
<td><span data-ttu-id="d3179-602">60</span><span class="sxs-lookup"><span data-stu-id="d3179-602">60</span></span></td>
<td><span data-ttu-id="d3179-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d3179-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d3179-604">535.31</span><span class="sxs-lookup"><span data-stu-id="d3179-604">535.31</span></span></td>
<td><span data-ttu-id="d3179-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-606">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-607">Product 2</span></span></td>
<td><span data-ttu-id="d3179-608">20</span><span class="sxs-lookup"><span data-stu-id="d3179-608">20</span></span></td>
<td><span data-ttu-id="d3179-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d3179-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d3179-610">178.44</span><span class="sxs-lookup"><span data-stu-id="d3179-610">178.44</span></span></td>
<td><span data-ttu-id="d3179-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-612">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-613">Product 1</span></span></td>
<td><span data-ttu-id="d3179-614">60</span><span class="sxs-lookup"><span data-stu-id="d3179-614">60</span></span></td>
<td><span data-ttu-id="d3179-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d3179-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d3179-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d3179-616">4,487.12</span></span></td>
<td><span data-ttu-id="d3179-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-618">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-619">Product 2</span></span></td>
<td><span data-ttu-id="d3179-620">20</span><span class="sxs-lookup"><span data-stu-id="d3179-620">20</span></span></td>
<td><span data-ttu-id="d3179-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d3179-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d3179-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d3179-622">1,495.71</span></span></td>
<td><span data-ttu-id="d3179-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3179-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="d3179-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-625">Cost object</span></span></th>
<th><span data-ttu-id="d3179-626">Величина</span><span class="sxs-lookup"><span data-stu-id="d3179-626">Magnitude</span></span></th>
<th><span data-ttu-id="d3179-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="d3179-627">Allocation factor</span></span></th>
<th><span data-ttu-id="d3179-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-628">Amount</span></span></th>
<th><span data-ttu-id="d3179-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-630">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-631">Product 1</span></span></td>
<td><span data-ttu-id="d3179-632">80</span><span class="sxs-lookup"><span data-stu-id="d3179-632">80</span></span></td>
<td><span data-ttu-id="d3179-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d3179-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d3179-634">241.05</span><span class="sxs-lookup"><span data-stu-id="d3179-634">241.05</span></span></td>
<td><span data-ttu-id="d3179-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-636">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-637">Product 2</span></span></td>
<td><span data-ttu-id="d3179-638">15</span><span class="sxs-lookup"><span data-stu-id="d3179-638">15</span></span></td>
<td><span data-ttu-id="d3179-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d3179-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d3179-640">45.20</span><span class="sxs-lookup"><span data-stu-id="d3179-640">45.20</span></span></td>
<td><span data-ttu-id="d3179-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-642">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-643">Product 1</span></span></td>
<td><span data-ttu-id="d3179-644">80</span><span class="sxs-lookup"><span data-stu-id="d3179-644">80</span></span></td>
<td><span data-ttu-id="d3179-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d3179-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d3179-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d3179-646">2,507.09</span></span></td>
<td><span data-ttu-id="d3179-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-648">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-649">Product 2</span></span></td>
<td><span data-ttu-id="d3179-650">15</span><span class="sxs-lookup"><span data-stu-id="d3179-650">15</span></span></td>
<td><span data-ttu-id="d3179-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d3179-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d3179-652">470.08</span><span class="sxs-lookup"><span data-stu-id="d3179-652">470.08</span></span></td>
<td><span data-ttu-id="d3179-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d3179-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="d3179-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="d3179-655">Journal</span></span></th>
<th><span data-ttu-id="d3179-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="d3179-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d3179-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="d3179-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d3179-658">Версия</span><span class="sxs-lookup"><span data-stu-id="d3179-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-659">00004</span><span class="sxs-lookup"><span data-stu-id="d3179-659">00004</span></span></td>
<td><span data-ttu-id="d3179-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="d3179-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="d3179-661">Fiscal</span></span></td>
<td><span data-ttu-id="d3179-662">2017</span><span class="sxs-lookup"><span data-stu-id="d3179-662">2017</span></span></td>
<td><span data-ttu-id="d3179-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-663">Period 1</span></span></td>
<td><span data-ttu-id="d3179-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="d3179-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="d3179-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="d3179-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d3179-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-668">Cost element</span></span></th>
<th><span data-ttu-id="d3179-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-669">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-672">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-672">CC001</span></span></td>
<td><span data-ttu-id="d3179-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-673">HR</span></span></td>
<td><span data-ttu-id="d3179-674">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-674">10001</span></span></td>
<td><span data-ttu-id="d3179-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-675">Electricity</span></span></td>
<td><span data-ttu-id="d3179-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-676">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-677">500.00</span><span class="sxs-lookup"><span data-stu-id="d3179-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-679">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-679">CC001</span></span></td>
<td><span data-ttu-id="d3179-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-680">HR</span></span></td>
<td><span data-ttu-id="d3179-681">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-681">10001</span></span></td>
<td><span data-ttu-id="d3179-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-682">Electricity</span></span></td>
<td><span data-ttu-id="d3179-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-683">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="d3179-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-686">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-686">CC002</span></span></td>
<td><span data-ttu-id="d3179-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-687">Finance</span></span></td>
<td><span data-ttu-id="d3179-688">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-688">10001</span></span></td>
<td><span data-ttu-id="d3179-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-689">Electricity</span></span></td>
<td><span data-ttu-id="d3179-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-690">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-691">675.00</span><span class="sxs-lookup"><span data-stu-id="d3179-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-693">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-693">CC002</span></span></td>
<td><span data-ttu-id="d3179-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-694">Finance</span></span></td>
<td><span data-ttu-id="d3179-695">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-695">10001</span></span></td>
<td><span data-ttu-id="d3179-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-696">Electricity</span></span></td>
<td><span data-ttu-id="d3179-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-697">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="d3179-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-700">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-700">CC003</span></span></td>
<td><span data-ttu-id="d3179-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-701">Assembly</span></span></td>
<td><span data-ttu-id="d3179-702">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-702">10001</span></span></td>
<td><span data-ttu-id="d3179-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-703">Electricity</span></span></td>
<td><span data-ttu-id="d3179-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-704">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-705">713.75</span><span class="sxs-lookup"><span data-stu-id="d3179-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-707">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-707">CC003</span></span></td>
<td><span data-ttu-id="d3179-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-708">Assembly</span></span></td>
<td><span data-ttu-id="d3179-709">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-709">10001</span></span></td>
<td><span data-ttu-id="d3179-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-710">Electricity</span></span></td>
<td><span data-ttu-id="d3179-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-711">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="d3179-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-714">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-714">CC003</span></span></td>
<td><span data-ttu-id="d3179-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-715">Packaging</span></span></td>
<td><span data-ttu-id="d3179-716">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-716">10001</span></span></td>
<td><span data-ttu-id="d3179-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-717">Electricity</span></span></td>
<td><span data-ttu-id="d3179-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-718">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-719">286.25</span><span class="sxs-lookup"><span data-stu-id="d3179-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-721">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-721">CC003</span></span></td>
<td><span data-ttu-id="d3179-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-722">Packaging</span></span></td>
<td><span data-ttu-id="d3179-723">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-723">10001</span></span></td>
<td><span data-ttu-id="d3179-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-724">Electricity</span></span></td>
<td><span data-ttu-id="d3179-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-725">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="d3179-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-728">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-729">Product 1</span></span></td>
<td><span data-ttu-id="d3179-730">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-730">10001</span></span></td>
<td><span data-ttu-id="d3179-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-731">Electricity</span></span></td>
<td><span data-ttu-id="d3179-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-732">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-733">776.36</span><span class="sxs-lookup"><span data-stu-id="d3179-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-735">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-736">Product 1</span></span></td>
<td><span data-ttu-id="d3179-737">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-737">10001</span></span></td>
<td><span data-ttu-id="d3179-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-738">Electricity</span></span></td>
<td><span data-ttu-id="d3179-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-739">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d3179-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-742">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-743">Product 1</span></span></td>
<td><span data-ttu-id="d3179-744">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-744">10001</span></span></td>
<td><span data-ttu-id="d3179-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-745">Electricity</span></span></td>
<td><span data-ttu-id="d3179-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-746">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-747">223.64</span><span class="sxs-lookup"><span data-stu-id="d3179-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="d3179-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-749">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-750">Product 1</span></span></td>
<td><span data-ttu-id="d3179-751">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-751">10001</span></span></td>
<td><span data-ttu-id="d3179-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-752">Electricity</span></span></td>
<td><span data-ttu-id="d3179-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-753">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d3179-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d3179-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d3179-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d3179-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-757">Cost element</span></span></th>
<th><span data-ttu-id="d3179-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-758">Cost behavior</span></span></th>
<th><span data-ttu-id="d3179-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d3179-759">Amount</span></span></th>
<th><span data-ttu-id="d3179-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="d3179-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3179-761">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-761">CC001</span></span></td>
<td><span data-ttu-id="d3179-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-762">HR</span></span></td>
<td><span data-ttu-id="d3179-763">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-763">10001</span></span></td>
<td><span data-ttu-id="d3179-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-764">Electricity</span></span></td>
<td><span data-ttu-id="d3179-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-765">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="d3179-766">-500.00</span></span></td>
<td><span data-ttu-id="d3179-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-768">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-768">CC002</span></span></td>
<td><span data-ttu-id="d3179-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-769">Finance</span></span></td>
<td><span data-ttu-id="d3179-770">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-770">10001</span></span></td>
<td><span data-ttu-id="d3179-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-771">Electricity</span></span></td>
<td><span data-ttu-id="d3179-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-772">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-773">175.00</span><span class="sxs-lookup"><span data-stu-id="d3179-773">175.00</span></span></td>
<td><span data-ttu-id="d3179-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-775">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-775">CC003</span></span></td>
<td><span data-ttu-id="d3179-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-776">Assembly</span></span></td>
<td><span data-ttu-id="d3179-777">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-777">10001</span></span></td>
<td><span data-ttu-id="d3179-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-778">Electricity</span></span></td>
<td><span data-ttu-id="d3179-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-779">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-780">275.00</span><span class="sxs-lookup"><span data-stu-id="d3179-780">275.00</span></span></td>
<td><span data-ttu-id="d3179-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-782">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-782">CC004</span></span></td>
<td><span data-ttu-id="d3179-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-783">Packaging</span></span></td>
<td><span data-ttu-id="d3179-784">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-784">10001</span></span></td>
<td><span data-ttu-id="d3179-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-785">Electricity</span></span></td>
<td><span data-ttu-id="d3179-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-786">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-787">50,00</span><span class="sxs-lookup"><span data-stu-id="d3179-787">50,00</span></span></td>
<td><span data-ttu-id="d3179-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-789">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-789">CC001</span></span></td>
<td><span data-ttu-id="d3179-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="d3179-790">HR</span></span></td>
<td><span data-ttu-id="d3179-791">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-791">10001</span></span></td>
<td><span data-ttu-id="d3179-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-792">Electricity</span></span></td>
<td><span data-ttu-id="d3179-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-793">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="d3179-794">-1,245.71</span></span></td>
<td><span data-ttu-id="d3179-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-796">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-796">CC002</span></span></td>
<td><span data-ttu-id="d3179-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-797">Finance</span></span></td>
<td><span data-ttu-id="d3179-798">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-798">10001</span></span></td>
<td><span data-ttu-id="d3179-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-799">Electricity</span></span></td>
<td><span data-ttu-id="d3179-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-800">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-801">436.00</span><span class="sxs-lookup"><span data-stu-id="d3179-801">436.00</span></span></td>
<td><span data-ttu-id="d3179-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-803">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-803">CC003</span></span></td>
<td><span data-ttu-id="d3179-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-804">Assembly</span></span></td>
<td><span data-ttu-id="d3179-805">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-805">10001</span></span></td>
<td><span data-ttu-id="d3179-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-806">Electricity</span></span></td>
<td><span data-ttu-id="d3179-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-807">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-808">685.14</span><span class="sxs-lookup"><span data-stu-id="d3179-808">685.14</span></span></td>
<td><span data-ttu-id="d3179-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-810">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-810">CC004</span></span></td>
<td><span data-ttu-id="d3179-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-811">Packaging</span></span></td>
<td><span data-ttu-id="d3179-812">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-812">10001</span></span></td>
<td><span data-ttu-id="d3179-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-813">Electricity</span></span></td>
<td><span data-ttu-id="d3179-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-814">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-815">124.57</span><span class="sxs-lookup"><span data-stu-id="d3179-815">124.57</span></span></td>
<td><span data-ttu-id="d3179-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-817">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-817">CC002</span></span></td>
<td><span data-ttu-id="d3179-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-818">Finance</span></span></td>
<td><span data-ttu-id="d3179-819">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-819">10001</span></span></td>
<td><span data-ttu-id="d3179-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-820">Electricity</span></span></td>
<td><span data-ttu-id="d3179-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-821">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="d3179-822">-675.00</span></span></td>
<td><span data-ttu-id="d3179-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-824">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-824">CC003</span></span></td>
<td><span data-ttu-id="d3179-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-825">Assembly</span></span></td>
<td><span data-ttu-id="d3179-826">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-826">10001</span></span></td>
<td><span data-ttu-id="d3179-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-827">Electricity</span></span></td>
<td><span data-ttu-id="d3179-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-828">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-829">438.75</span><span class="sxs-lookup"><span data-stu-id="d3179-829">438.75</span></span></td>
<td><span data-ttu-id="d3179-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-831">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-831">CC004</span></span></td>
<td><span data-ttu-id="d3179-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-832">Packaging</span></span></td>
<td><span data-ttu-id="d3179-833">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-833">10001</span></span></td>
<td><span data-ttu-id="d3179-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-834">Electricity</span></span></td>
<td><span data-ttu-id="d3179-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-835">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-836">236.25</span><span class="sxs-lookup"><span data-stu-id="d3179-836">236.25</span></span></td>
<td><span data-ttu-id="d3179-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-838">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-838">CC002</span></span></td>
<td><span data-ttu-id="d3179-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="d3179-839">Finance</span></span></td>
<td><span data-ttu-id="d3179-840">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-840">10001</span></span></td>
<td><span data-ttu-id="d3179-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-841">Electricity</span></span></td>
<td><span data-ttu-id="d3179-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-842">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="d3179-843">-8,150.29</span></span></td>
<td><span data-ttu-id="d3179-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-845">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-845">CC003</span></span></td>
<td><span data-ttu-id="d3179-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-846">Assembly</span></span></td>
<td><span data-ttu-id="d3179-847">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-847">10001</span></span></td>
<td><span data-ttu-id="d3179-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-848">Electricity</span></span></td>
<td><span data-ttu-id="d3179-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-849">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d3179-850">5,297.69</span></span></td>
<td><span data-ttu-id="d3179-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-852">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-852">CC004</span></span></td>
<td><span data-ttu-id="d3179-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="d3179-853">Packaging</span></span></td>
<td><span data-ttu-id="d3179-854">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-854">10001</span></span></td>
<td><span data-ttu-id="d3179-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-855">Electricity</span></span></td>
<td><span data-ttu-id="d3179-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-856">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d3179-857">2,852.60</span></span></td>
<td><span data-ttu-id="d3179-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-859">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-859">CC003</span></span></td>
<td><span data-ttu-id="d3179-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-860">Assembly</span></span></td>
<td><span data-ttu-id="d3179-861">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-861">10001</span></span></td>
<td><span data-ttu-id="d3179-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-862">Electricity</span></span></td>
<td><span data-ttu-id="d3179-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-863">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="d3179-864">-713.75</span></span></td>
<td><span data-ttu-id="d3179-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-866">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-867">Product 1</span></span></td>
<td><span data-ttu-id="d3179-868">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-868">10001</span></span></td>
<td><span data-ttu-id="d3179-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-869">Electricity</span></span></td>
<td><span data-ttu-id="d3179-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-870">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-871">535.31</span><span class="sxs-lookup"><span data-stu-id="d3179-871">535.31</span></span></td>
<td><span data-ttu-id="d3179-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-873">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-874">Product 2</span></span></td>
<td><span data-ttu-id="d3179-875">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-875">10001</span></span></td>
<td><span data-ttu-id="d3179-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-876">Electricity</span></span></td>
<td><span data-ttu-id="d3179-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-877">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-878">178.44</span><span class="sxs-lookup"><span data-stu-id="d3179-878">178.44</span></span></td>
<td><span data-ttu-id="d3179-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-880">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-880">CC003</span></span></td>
<td><span data-ttu-id="d3179-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-881">Assembly</span></span></td>
<td><span data-ttu-id="d3179-882">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-882">10001</span></span></td>
<td><span data-ttu-id="d3179-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-883">Electricity</span></span></td>
<td><span data-ttu-id="d3179-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-884">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="d3179-885">-5,982.83</span></span></td>
<td><span data-ttu-id="d3179-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-887">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-888">Product 1</span></span></td>
<td><span data-ttu-id="d3179-889">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-889">10001</span></span></td>
<td><span data-ttu-id="d3179-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-890">Electricity</span></span></td>
<td><span data-ttu-id="d3179-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-891">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d3179-892">4,487.12</span></span></td>
<td><span data-ttu-id="d3179-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-894">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-895">Product 2</span></span></td>
<td><span data-ttu-id="d3179-896">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-896">10001</span></span></td>
<td><span data-ttu-id="d3179-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-897">Electricity</span></span></td>
<td><span data-ttu-id="d3179-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-898">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d3179-899">1,495.71</span></span></td>
<td><span data-ttu-id="d3179-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-901">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-901">CC003</span></span></td>
<td><span data-ttu-id="d3179-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-902">Assembly</span></span></td>
<td><span data-ttu-id="d3179-903">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-903">10001</span></span></td>
<td><span data-ttu-id="d3179-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-904">Electricity</span></span></td>
<td><span data-ttu-id="d3179-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-905">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="d3179-906">-286.25</span></span></td>
<td><span data-ttu-id="d3179-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-908">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-909">Product 1</span></span></td>
<td><span data-ttu-id="d3179-910">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-910">10001</span></span></td>
<td><span data-ttu-id="d3179-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-911">Electricity</span></span></td>
<td><span data-ttu-id="d3179-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-912">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-913">241.05</span><span class="sxs-lookup"><span data-stu-id="d3179-913">241.05</span></span></td>
<td><span data-ttu-id="d3179-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-915">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-916">Product 2</span></span></td>
<td><span data-ttu-id="d3179-917">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-917">10001</span></span></td>
<td><span data-ttu-id="d3179-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-918">Electricity</span></span></td>
<td><span data-ttu-id="d3179-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-919">Fixed cost</span></span></td>
<td><span data-ttu-id="d3179-920">45.20</span><span class="sxs-lookup"><span data-stu-id="d3179-920">45.20</span></span></td>
<td><span data-ttu-id="d3179-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-922">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-922">CC003</span></span></td>
<td><span data-ttu-id="d3179-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="d3179-923">Assembly</span></span></td>
<td><span data-ttu-id="d3179-924">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-924">10001</span></span></td>
<td><span data-ttu-id="d3179-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-925">Electricity</span></span></td>
<td><span data-ttu-id="d3179-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-926">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="d3179-927">-2,977.17</span></span></td>
<td><span data-ttu-id="d3179-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-929">Prod 1</span></span></td>
<td><span data-ttu-id="d3179-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="d3179-930">Product 1</span></span></td>
<td><span data-ttu-id="d3179-931">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-931">10001</span></span></td>
<td><span data-ttu-id="d3179-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-932">Electricity</span></span></td>
<td><span data-ttu-id="d3179-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-933">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d3179-934">2,507.09</span></span></td>
<td><span data-ttu-id="d3179-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3179-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-936">Prod 2</span></span></td>
<td><span data-ttu-id="d3179-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="d3179-937">Product 2</span></span></td>
<td><span data-ttu-id="d3179-938">10001</span><span class="sxs-lookup"><span data-stu-id="d3179-938">10001</span></span></td>
<td><span data-ttu-id="d3179-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-939">Electricity</span></span></td>
<td><span data-ttu-id="d3179-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-940">Variable cost</span></span></td>
<td><span data-ttu-id="d3179-941">470.08</span><span class="sxs-lookup"><span data-stu-id="d3179-941">470.08</span></span></td>
<td><span data-ttu-id="d3179-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="d3179-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="d3179-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="d3179-943">Conclusion</span></span>
<span data-ttu-id="d3179-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="d3179-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="d3179-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="d3179-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="d3179-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="d3179-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="d3179-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="d3179-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="d3179-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="d3179-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="d3179-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d3179-951">CC099</span><span class="sxs-lookup"><span data-stu-id="d3179-951">CC099</span></span></th>
<th><span data-ttu-id="d3179-952">CC001</span><span class="sxs-lookup"><span data-stu-id="d3179-952">CC001</span></span></th>
<th><span data-ttu-id="d3179-953">CC002</span><span class="sxs-lookup"><span data-stu-id="d3179-953">CC002</span></span></th>
<th><span data-ttu-id="d3179-954">CC003</span><span class="sxs-lookup"><span data-stu-id="d3179-954">CC003</span></span></th>
<th><span data-ttu-id="d3179-955">CC004</span><span class="sxs-lookup"><span data-stu-id="d3179-955">CC004</span></span></th>
<th><span data-ttu-id="d3179-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="d3179-956">Proj 1</span></span></th>
<th><span data-ttu-id="d3179-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="d3179-957">Proj 2</span></span></th>
<th><span data-ttu-id="d3179-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="d3179-958">Prod 1</span></span></th>
<th><span data-ttu-id="d3179-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="d3179-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="d3179-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="d3179-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d3179-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="d3179-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="d3179-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-971">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="d3179-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-973">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-974">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-975">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-976">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-977">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d3179-978">776.36</span><span class="sxs-lookup"><span data-stu-id="d3179-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-979">223.64</span><span class="sxs-lookup"><span data-stu-id="d3179-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="d3179-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="d3179-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-982">000</span><span class="sxs-lookup"><span data-stu-id="d3179-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-983">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-984">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-985">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-986">0,00</span><span class="sxs-lookup"><span data-stu-id="d3179-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-987">30.00</span><span class="sxs-lookup"><span data-stu-id="d3179-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-988">10,00</span><span class="sxs-lookup"><span data-stu-id="d3179-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d3179-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d3179-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d3179-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d3179-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d3179-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="d3179-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="d3179-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="d3179-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="d3179-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="d3179-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="d3179-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="d3179-996">Дополнительные сведения см. в разделе [Свертка затрат](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="d3179-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



