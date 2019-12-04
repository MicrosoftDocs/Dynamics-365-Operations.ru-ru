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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770812"
---
# <a name="overhead-calculation"></a><span data-ttu-id="64234-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="64234-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64234-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="64234-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="64234-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="64234-105">Term definition</span></span>
---------------

<span data-ttu-id="64234-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="64234-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="64234-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="64234-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="64234-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="64234-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="64234-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="64234-109">Rent</span></span>
-   <span data-ttu-id="64234-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-110">Electricity</span></span>
-   <span data-ttu-id="64234-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="64234-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="64234-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="64234-112">Overhead calculation overview</span></span>
<span data-ttu-id="64234-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="64234-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="64234-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="64234-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="64234-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="64234-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="64234-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="64234-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="64234-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="64234-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="64234-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="64234-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="64234-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="64234-119">Version type</span></span>
-   <span data-ttu-id="64234-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="64234-120">Date and time</span></span>
-   <span data-ttu-id="64234-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="64234-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="64234-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="64234-122">Fiscal year</span></span>
-   <span data-ttu-id="64234-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="64234-123">Fiscal period</span></span>

<span data-ttu-id="64234-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="64234-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="64234-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="64234-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="64234-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="64234-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="64234-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="64234-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="64234-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="64234-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="64234-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="64234-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="64234-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="64234-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="64234-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="64234-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="64234-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="64234-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="64234-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="64234-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="64234-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="64234-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="64234-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="64234-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="64234-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="64234-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="64234-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64234-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="64234-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="64234-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="64234-140">Main account</span></span></th>
<th><span data-ttu-id="64234-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="64234-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="64234-143">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-143">CC099</span></span></td>
<td><span data-ttu-id="64234-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-144">Default cost center</span></span></td>
<td><span data-ttu-id="64234-145">10001</span><span class="sxs-lookup"><span data-stu-id="64234-145">10001</span></span></td>
<td><span data-ttu-id="64234-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-146">Electricity</span></span></td>
<td><span data-ttu-id="64234-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="64234-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="64234-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="64234-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="64234-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="64234-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="64234-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-151">Define the cost behavior rule</span></span>

<span data-ttu-id="64234-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="64234-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="64234-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="64234-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="64234-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="64234-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="64234-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="64234-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="64234-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="64234-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="64234-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="64234-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="64234-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-160">Journal</span></span></th>
<th><span data-ttu-id="64234-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="64234-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64234-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="64234-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64234-163">Версия</span><span class="sxs-lookup"><span data-stu-id="64234-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-164">00001</span><span class="sxs-lookup"><span data-stu-id="64234-164">00001</span></span></td>
<td><span data-ttu-id="64234-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="64234-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="64234-166">Fiscal</span></span></td>
<td><span data-ttu-id="64234-167">2017</span><span class="sxs-lookup"><span data-stu-id="64234-167">2017</span></span></td>
<td><span data-ttu-id="64234-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-168">Period 1</span></span></td>
<td><span data-ttu-id="64234-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="64234-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="64234-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64234-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-173">Cost element</span></span></th>
<th><span data-ttu-id="64234-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-174">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="64234-177">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-177">CC099</span></span></td>
<td><span data-ttu-id="64234-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-178">Default cost center</span></span></td>
<td><span data-ttu-id="64234-179">10001</span><span class="sxs-lookup"><span data-stu-id="64234-179">10001</span></span></td>
<td><span data-ttu-id="64234-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-180">Electricity</span></span></td>
<td><span data-ttu-id="64234-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="64234-181">Unclassified</span></span></td>
<td><span data-ttu-id="64234-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="64234-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64234-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="64234-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-185">Cost element</span></span></th>
<th><span data-ttu-id="64234-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-186">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-187">Amount</span></span></th>
<th><span data-ttu-id="64234-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-189">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-189">CC099</span></span></td>
<td><span data-ttu-id="64234-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-190">Default cost center</span></span></td>
<td><span data-ttu-id="64234-191">10001</span><span class="sxs-lookup"><span data-stu-id="64234-191">10001</span></span></td>
<td><span data-ttu-id="64234-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-192">Electricity</span></span></td>
<td><span data-ttu-id="64234-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="64234-193">Unclassified</span></span></td>
<td><span data-ttu-id="64234-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="64234-194">10,000.00</span></span></td>
<td><span data-ttu-id="64234-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-196">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-196">CC099</span></span></td>
<td><span data-ttu-id="64234-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-197">Default cost center</span></span></td>
<td><span data-ttu-id="64234-198">10001</span><span class="sxs-lookup"><span data-stu-id="64234-198">10001</span></span></td>
<td><span data-ttu-id="64234-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-199">Electricity</span></span></td>
<td><span data-ttu-id="64234-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="64234-200">Unclassified</span></span></td>
<td><span data-ttu-id="64234-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="64234-201">-10,000.00</span></span></td>
<td><span data-ttu-id="64234-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-203">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-203">CC099</span></span></td>
<td><span data-ttu-id="64234-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-204">Default cost center</span></span></td>
<td><span data-ttu-id="64234-205">10001</span><span class="sxs-lookup"><span data-stu-id="64234-205">10001</span></span></td>
<td><span data-ttu-id="64234-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-206">Electricity</span></span></td>
<td><span data-ttu-id="64234-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-207">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="64234-208">1,000.00</span></span></td>
<td><span data-ttu-id="64234-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-210">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-210">CC099</span></span></td>
<td><span data-ttu-id="64234-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-211">Default cost center</span></span></td>
<td><span data-ttu-id="64234-212">10001</span><span class="sxs-lookup"><span data-stu-id="64234-212">10001</span></span></td>
<td><span data-ttu-id="64234-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-213">Electricity</span></span></td>
<td><span data-ttu-id="64234-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-214">Variable cost</span></span></td>
<td><span data-ttu-id="64234-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="64234-215">9,000.00</span></span></td>
<td><span data-ttu-id="64234-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="64234-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="64234-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="64234-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="64234-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="64234-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-221">Define the cost distribution rule</span></span>

<span data-ttu-id="64234-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="64234-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="64234-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="64234-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="64234-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="64234-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="64234-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="64234-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="64234-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="64234-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="64234-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-228">Cost object</span></span></th>
<th><span data-ttu-id="64234-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="64234-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-230">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-230">CC001</span></span></td>
<td><span data-ttu-id="64234-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-231">HR</span></span></td>
<td><span data-ttu-id="64234-232">1000</span><span class="sxs-lookup"><span data-stu-id="64234-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-233">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-233">CC002</span></span></td>
<td><span data-ttu-id="64234-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-234">Finance</span></span></td>
<td><span data-ttu-id="64234-235">6,000</span><span class="sxs-lookup"><span data-stu-id="64234-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-236">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-236">CC003</span></span></td>
<td><span data-ttu-id="64234-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-237">Assembly</span></span></td>
<td><span data-ttu-id="64234-238">0</span><span class="sxs-lookup"><span data-stu-id="64234-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-240">Cost object</span></span></th>
<th><span data-ttu-id="64234-241">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-241">Magnitude</span></span></th>
<th><span data-ttu-id="64234-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-242">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-244">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-244">CC001</span></span></td>
<td><span data-ttu-id="64234-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-245">HR</span></span></td>
<td><span data-ttu-id="64234-246">1000</span><span class="sxs-lookup"><span data-stu-id="64234-246">1,000</span></span></td>
<td><span data-ttu-id="64234-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="64234-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="64234-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="64234-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-249">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-249">CC002</span></span></td>
<td><span data-ttu-id="64234-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-250">Finance</span></span></td>
<td><span data-ttu-id="64234-251">6,000</span><span class="sxs-lookup"><span data-stu-id="64234-251">6,000</span></span></td>
<td><span data-ttu-id="64234-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="64234-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="64234-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="64234-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-254">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-254">CC003</span></span></td>
<td><span data-ttu-id="64234-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-255">Assembly</span></span></td>
<td><span data-ttu-id="64234-256">0</span><span class="sxs-lookup"><span data-stu-id="64234-256">0</span></span></td>
<td><span data-ttu-id="64234-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="64234-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="64234-258">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="64234-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="64234-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-261">Cost object</span></span></th>
<th><span data-ttu-id="64234-262">Формула</span><span class="sxs-lookup"><span data-stu-id="64234-262">Formula</span></span></th>
<th><span data-ttu-id="64234-263">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-263">Magnitude</span></span></th>
<th><span data-ttu-id="64234-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-264">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-266">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-266">CC001</span></span></td>
<td><span data-ttu-id="64234-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-267">HR</span></span></td>
<td><span data-ttu-id="64234-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="64234-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="64234-269">1</span><span class="sxs-lookup"><span data-stu-id="64234-269">1</span></span></td>
<td><span data-ttu-id="64234-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="64234-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="64234-271">500.00</span><span class="sxs-lookup"><span data-stu-id="64234-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-272">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-272">CC002</span></span></td>
<td><span data-ttu-id="64234-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-273">Finance</span></span></td>
<td><span data-ttu-id="64234-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="64234-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="64234-275">1</span><span class="sxs-lookup"><span data-stu-id="64234-275">1</span></span></td>
<td><span data-ttu-id="64234-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="64234-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="64234-277">500.00</span><span class="sxs-lookup"><span data-stu-id="64234-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-278">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-278">CC003</span></span></td>
<td><span data-ttu-id="64234-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-279">Assembly</span></span></td>
<td><span data-ttu-id="64234-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="64234-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="64234-281">0</span><span class="sxs-lookup"><span data-stu-id="64234-281">0</span></span></td>
<td><span data-ttu-id="64234-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="64234-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="64234-283">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="64234-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-285">Journal</span></span></th>
<th><span data-ttu-id="64234-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="64234-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64234-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="64234-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64234-288">Версия</span><span class="sxs-lookup"><span data-stu-id="64234-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-289">00002</span><span class="sxs-lookup"><span data-stu-id="64234-289">00002</span></span></td>
<td><span data-ttu-id="64234-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="64234-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="64234-291">Fiscal</span></span></td>
<td><span data-ttu-id="64234-292">2017</span><span class="sxs-lookup"><span data-stu-id="64234-292">2017</span></span></td>
<td><span data-ttu-id="64234-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-293">Period 1</span></span></td>
<td><span data-ttu-id="64234-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="64234-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="64234-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64234-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-298">Cost element</span></span></th>
<th><span data-ttu-id="64234-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-299">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-302">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-302">CC099</span></span></td>
<td><span data-ttu-id="64234-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-303">Default cost center</span></span></td>
<td><span data-ttu-id="64234-304">10001</span><span class="sxs-lookup"><span data-stu-id="64234-304">10001</span></span></td>
<td><span data-ttu-id="64234-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-305">Electricity</span></span></td>
<td><span data-ttu-id="64234-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-306">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="64234-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-309">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-309">CC099</span></span></td>
<td><span data-ttu-id="64234-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-310">Default cost center</span></span></td>
<td><span data-ttu-id="64234-311">10001</span><span class="sxs-lookup"><span data-stu-id="64234-311">10001</span></span></td>
<td><span data-ttu-id="64234-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-312">Electricity</span></span></td>
<td><span data-ttu-id="64234-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-313">Variable cost</span></span></td>
<td><span data-ttu-id="64234-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="64234-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64234-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="64234-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-317">Cost element</span></span></th>
<th><span data-ttu-id="64234-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-318">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-319">Amount</span></span></th>
<th><span data-ttu-id="64234-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-321">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-321">CC099</span></span></td>
<td><span data-ttu-id="64234-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-322">Default cost center</span></span></td>
<td><span data-ttu-id="64234-323">10001</span><span class="sxs-lookup"><span data-stu-id="64234-323">10001</span></span></td>
<td><span data-ttu-id="64234-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-324">Electricity</span></span></td>
<td><span data-ttu-id="64234-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-325">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="64234-326">-1,000.00</span></span></td>
<td><span data-ttu-id="64234-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-328">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-328">CC001</span></span></td>
<td><span data-ttu-id="64234-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-329">HR</span></span></td>
<td><span data-ttu-id="64234-330">10001</span><span class="sxs-lookup"><span data-stu-id="64234-330">10001</span></span></td>
<td><span data-ttu-id="64234-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-331">Electricity</span></span></td>
<td><span data-ttu-id="64234-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-332">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-333">500.00</span><span class="sxs-lookup"><span data-stu-id="64234-333">500.00</span></span></td>
<td><span data-ttu-id="64234-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-335">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-335">CC002</span></span></td>
<td><span data-ttu-id="64234-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-336">Finance</span></span></td>
<td><span data-ttu-id="64234-337">10001</span><span class="sxs-lookup"><span data-stu-id="64234-337">10001</span></span></td>
<td><span data-ttu-id="64234-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-338">Electricity</span></span></td>
<td><span data-ttu-id="64234-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-339">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-340">500.00</span><span class="sxs-lookup"><span data-stu-id="64234-340">500.00</span></span></td>
<td><span data-ttu-id="64234-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-342">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-342">CC099</span></span></td>
<td><span data-ttu-id="64234-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64234-343">Default cost center</span></span></td>
<td><span data-ttu-id="64234-344">10001</span><span class="sxs-lookup"><span data-stu-id="64234-344">10001</span></span></td>
<td><span data-ttu-id="64234-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-345">Electricity</span></span></td>
<td><span data-ttu-id="64234-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-346">Variable cost</span></span></td>
<td><span data-ttu-id="64234-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="64234-347">-9,000.00</span></span></td>
<td><span data-ttu-id="64234-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-349">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-349">CC001</span></span></td>
<td><span data-ttu-id="64234-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-350">HR</span></span></td>
<td><span data-ttu-id="64234-351">10001</span><span class="sxs-lookup"><span data-stu-id="64234-351">10001</span></span></td>
<td><span data-ttu-id="64234-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-352">Electricity</span></span></td>
<td><span data-ttu-id="64234-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-353">Variable cost</span></span></td>
<td><span data-ttu-id="64234-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="64234-354">1,285.71</span></span></td>
<td><span data-ttu-id="64234-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-356">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-356">CC002</span></span></td>
<td><span data-ttu-id="64234-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-357">Finance</span></span></td>
<td><span data-ttu-id="64234-358">10001</span><span class="sxs-lookup"><span data-stu-id="64234-358">10001</span></span></td>
<td><span data-ttu-id="64234-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-359">Electricity</span></span></td>
<td><span data-ttu-id="64234-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-360">Variable cost</span></span></td>
<td><span data-ttu-id="64234-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="64234-361">7,714.29</span></span></td>
<td><span data-ttu-id="64234-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="64234-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="64234-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="64234-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="64234-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="64234-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="64234-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="64234-367">Define the overhead rate</span></span>

<span data-ttu-id="64234-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="64234-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="64234-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="64234-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-370">Cost object</span></span></th>
<th><span data-ttu-id="64234-371">Часы</span><span class="sxs-lookup"><span data-stu-id="64234-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-372">Proj 1</span></span></td>
<td><span data-ttu-id="64234-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-373">Project 1</span></span></td>
<td><span data-ttu-id="64234-374">3</span><span class="sxs-lookup"><span data-stu-id="64234-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-375">Proj 2</span></span></td>
<td><span data-ttu-id="64234-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-376">Project 2</span></span></td>
<td><span data-ttu-id="64234-377">1</span><span class="sxs-lookup"><span data-stu-id="64234-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-379">Cost object</span></span></th>
<th><span data-ttu-id="64234-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-380">Cost element</span></span></th>
<th><span data-ttu-id="64234-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-381">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="64234-382">Units</span></span></th>
<th><span data-ttu-id="64234-383">По норме</span><span class="sxs-lookup"><span data-stu-id="64234-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-384">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-384">CC001</span></span></td>
<td><span data-ttu-id="64234-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-385">HR</span></span></td>
<td><span data-ttu-id="64234-386">10001</span><span class="sxs-lookup"><span data-stu-id="64234-386">10001</span></span></td>
<td><span data-ttu-id="64234-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-387">Variable cost</span></span></td>
<td><span data-ttu-id="64234-388">1</span><span class="sxs-lookup"><span data-stu-id="64234-388">1</span></span></td>
<td><span data-ttu-id="64234-389">10</span><span class="sxs-lookup"><span data-stu-id="64234-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-391">Cost object</span></span></th>
<th><span data-ttu-id="64234-392">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-392">Magnitude</span></span></th>
<th><span data-ttu-id="64234-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-393">Cost element</span></span></th>
<th><span data-ttu-id="64234-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-394">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-396">Proj 1</span></span></td>
<td><span data-ttu-id="64234-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-397">Project 1</span></span></td>
<td><span data-ttu-id="64234-398">3</span><span class="sxs-lookup"><span data-stu-id="64234-398">3</span></span></td>
<td><span data-ttu-id="64234-399">10001</span><span class="sxs-lookup"><span data-stu-id="64234-399">10001</span></span></td>
<td><span data-ttu-id="64234-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="64234-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="64234-401">30.00</span><span class="sxs-lookup"><span data-stu-id="64234-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-402">Proj 2</span></span></td>
<td><span data-ttu-id="64234-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-403">Project 2</span></span></td>
<td><span data-ttu-id="64234-404">1</span><span class="sxs-lookup"><span data-stu-id="64234-404">1</span></span></td>
<td><span data-ttu-id="64234-405">10001</span><span class="sxs-lookup"><span data-stu-id="64234-405">10001</span></span></td>
<td><span data-ttu-id="64234-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="64234-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="64234-407">10,00</span><span class="sxs-lookup"><span data-stu-id="64234-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="64234-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-409">Journal</span></span></th>
<th><span data-ttu-id="64234-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="64234-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64234-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="64234-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64234-412">Версия</span><span class="sxs-lookup"><span data-stu-id="64234-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-413">00003</span><span class="sxs-lookup"><span data-stu-id="64234-413">00003</span></span></td>
<td><span data-ttu-id="64234-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="64234-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="64234-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="64234-415">Fiscal</span></span></td>
<td><span data-ttu-id="64234-416">2017</span><span class="sxs-lookup"><span data-stu-id="64234-416">2017</span></span></td>
<td><span data-ttu-id="64234-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-417">Period 1</span></span></td>
<td><span data-ttu-id="64234-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="64234-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="64234-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64234-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-421">Cost object</span></span></th>
<th><span data-ttu-id="64234-422">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-424">Proj 1</span></span></td>
<td><span data-ttu-id="64234-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="64234-426">3,00</span><span class="sxs-lookup"><span data-stu-id="64234-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-428">Proj 2</span></span></td>
<td><span data-ttu-id="64234-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="64234-430">1.00</span><span class="sxs-lookup"><span data-stu-id="64234-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64234-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="64234-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-433">Cost element</span></span></th>
<th><span data-ttu-id="64234-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-434">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-435">Amount</span></span></th>
<th><span data-ttu-id="64234-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="64234-437">CC0001</span></span></td>
<td><span data-ttu-id="64234-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-438">HR</span></span></td>
<td><span data-ttu-id="64234-439">10001</span><span class="sxs-lookup"><span data-stu-id="64234-439">10001</span></span></td>
<td><span data-ttu-id="64234-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-440">Electricity</span></span></td>
<td><span data-ttu-id="64234-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-441">Variable cost</span></span></td>
<td><span data-ttu-id="64234-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="64234-442">-30.00</span></span></td>
<td><span data-ttu-id="64234-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-444">Proj 1</span></span></td>
<td><span data-ttu-id="64234-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="64234-446">10001</span><span class="sxs-lookup"><span data-stu-id="64234-446">10001</span></span></td>
<td><span data-ttu-id="64234-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-447">Electricity</span></span></td>
<td><span data-ttu-id="64234-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-448">Variable cost</span></span></td>
<td><span data-ttu-id="64234-449">30.00</span><span class="sxs-lookup"><span data-stu-id="64234-449">30.00</span></span></td>
<td><span data-ttu-id="64234-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-451">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-451">CC001</span></span></td>
<td><span data-ttu-id="64234-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-452">HR</span></span></td>
<td><span data-ttu-id="64234-453">10001</span><span class="sxs-lookup"><span data-stu-id="64234-453">10001</span></span></td>
<td><span data-ttu-id="64234-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-454">Electricity</span></span></td>
<td><span data-ttu-id="64234-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-455">Variable cost</span></span></td>
<td><span data-ttu-id="64234-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="64234-456">-10.00</span></span></td>
<td><span data-ttu-id="64234-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-458">Proj 2</span></span></td>
<td><span data-ttu-id="64234-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="64234-460">10001</span><span class="sxs-lookup"><span data-stu-id="64234-460">10001</span></span></td>
<td><span data-ttu-id="64234-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-461">Electricity</span></span></td>
<td><span data-ttu-id="64234-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-462">Variable cost</span></span></td>
<td><span data-ttu-id="64234-463">10.00</span><span class="sxs-lookup"><span data-stu-id="64234-463">10.00</span></span></td>
<td><span data-ttu-id="64234-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="64234-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="64234-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="64234-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="64234-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="64234-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="64234-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="64234-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="64234-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="64234-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="64234-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="64234-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="64234-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="64234-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="64234-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="64234-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="64234-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="64234-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-475">Define the cost allocation</span></span>

<span data-ttu-id="64234-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="64234-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="64234-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="64234-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-479">Cost object</span></span></th>
<th><span data-ttu-id="64234-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="64234-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-481">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-481">CC002</span></span></td>
<td><span data-ttu-id="64234-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-482">Finance</span></span></td>
<td><span data-ttu-id="64234-483">35</span><span class="sxs-lookup"><span data-stu-id="64234-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-484">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-484">CC003</span></span></td>
<td><span data-ttu-id="64234-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-485">Assembly</span></span></td>
<td><span data-ttu-id="64234-486">55</span><span class="sxs-lookup"><span data-stu-id="64234-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-487">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-487">CC004</span></span></td>
<td><span data-ttu-id="64234-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-488">Packaging</span></span></td>
<td><span data-ttu-id="64234-489">10</span><span class="sxs-lookup"><span data-stu-id="64234-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="64234-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="64234-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-492">Cost object</span></span></th>
<th><span data-ttu-id="64234-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="64234-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-494">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-494">CC003</span></span></td>
<td><span data-ttu-id="64234-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-495">Assembly</span></span></td>
<td><span data-ttu-id="64234-496">65</span><span class="sxs-lookup"><span data-stu-id="64234-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-497">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-497">CC004</span></span></td>
<td><span data-ttu-id="64234-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-498">Packaging</span></span></td>
<td><span data-ttu-id="64234-499">35</span><span class="sxs-lookup"><span data-stu-id="64234-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="64234-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="64234-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-502">Cost object</span></span></th>
<th><span data-ttu-id="64234-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="64234-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-504">Prod 1</span></span></td>
<td><span data-ttu-id="64234-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-505">Product 1</span></span></td>
<td><span data-ttu-id="64234-506">60</span><span class="sxs-lookup"><span data-stu-id="64234-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-507">Prod 2</span></span></td>
<td><span data-ttu-id="64234-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-508">Product 2</span></span></td>
<td><span data-ttu-id="64234-509">20</span><span class="sxs-lookup"><span data-stu-id="64234-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="64234-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="64234-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-512">Cost object</span></span></th>
<th><span data-ttu-id="64234-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="64234-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-514">Prod 1</span></span></td>
<td><span data-ttu-id="64234-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-515">Product 1</span></span></td>
<td><span data-ttu-id="64234-516">80</span><span class="sxs-lookup"><span data-stu-id="64234-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-517">Prod 2</span></span></td>
<td><span data-ttu-id="64234-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-518">Product 2</span></span></td>
<td><span data-ttu-id="64234-519">15</span><span class="sxs-lookup"><span data-stu-id="64234-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="64234-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="64234-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="64234-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="64234-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="64234-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="64234-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-523">Cost object</span></span></th>
<th><span data-ttu-id="64234-524">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-524">Magnitude</span></span></th>
<th><span data-ttu-id="64234-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-525">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-526">Amount</span></span></th>
<th><span data-ttu-id="64234-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-528">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-528">CC002</span></span></td>
<td><span data-ttu-id="64234-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-529">Finance</span></span></td>
<td><span data-ttu-id="64234-530">35</span><span class="sxs-lookup"><span data-stu-id="64234-530">35</span></span></td>
<td><span data-ttu-id="64234-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="64234-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="64234-532">175.00</span><span class="sxs-lookup"><span data-stu-id="64234-532">175.00</span></span></td>
<td><span data-ttu-id="64234-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-534">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-534">CC003</span></span></td>
<td><span data-ttu-id="64234-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-535">Assembly</span></span></td>
<td><span data-ttu-id="64234-536">55</span><span class="sxs-lookup"><span data-stu-id="64234-536">55</span></span></td>
<td><span data-ttu-id="64234-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="64234-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="64234-538">275.00</span><span class="sxs-lookup"><span data-stu-id="64234-538">275.00</span></span></td>
<td><span data-ttu-id="64234-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-540">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-540">CC004</span></span></td>
<td><span data-ttu-id="64234-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-541">Packaging</span></span></td>
<td><span data-ttu-id="64234-542">10</span><span class="sxs-lookup"><span data-stu-id="64234-542">10</span></span></td>
<td><span data-ttu-id="64234-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="64234-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="64234-544">50,00</span><span class="sxs-lookup"><span data-stu-id="64234-544">50.00</span></span></td>
<td><span data-ttu-id="64234-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-546">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-546">CC002</span></span></td>
<td><span data-ttu-id="64234-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-547">Finance</span></span></td>
<td><span data-ttu-id="64234-548">35</span><span class="sxs-lookup"><span data-stu-id="64234-548">35</span></span></td>
<td><span data-ttu-id="64234-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="64234-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="64234-550">436.00</span><span class="sxs-lookup"><span data-stu-id="64234-550">436.00</span></span></td>
<td><span data-ttu-id="64234-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-552">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-552">CC003</span></span></td>
<td><span data-ttu-id="64234-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-553">Assembly</span></span></td>
<td><span data-ttu-id="64234-554">55</span><span class="sxs-lookup"><span data-stu-id="64234-554">55</span></span></td>
<td><span data-ttu-id="64234-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="64234-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="64234-556">685.14</span><span class="sxs-lookup"><span data-stu-id="64234-556">685.14</span></span></td>
<td><span data-ttu-id="64234-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-558">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-558">CC004</span></span></td>
<td><span data-ttu-id="64234-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-559">Packaging</span></span></td>
<td><span data-ttu-id="64234-560">10</span><span class="sxs-lookup"><span data-stu-id="64234-560">10</span></span></td>
<td><span data-ttu-id="64234-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="64234-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="64234-562">124.57</span><span class="sxs-lookup"><span data-stu-id="64234-562">124.57</span></span></td>
<td><span data-ttu-id="64234-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="64234-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-565">Cost object</span></span></th>
<th><span data-ttu-id="64234-566">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-566">Magnitude</span></span></th>
<th><span data-ttu-id="64234-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-567">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-568">Amount</span></span></th>
<th><span data-ttu-id="64234-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-570">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-570">CC003</span></span></td>
<td><span data-ttu-id="64234-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-571">Assembly</span></span></td>
<td><span data-ttu-id="64234-572">65</span><span class="sxs-lookup"><span data-stu-id="64234-572">65</span></span></td>
<td><span data-ttu-id="64234-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="64234-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="64234-574">438.75</span><span class="sxs-lookup"><span data-stu-id="64234-574">438.75</span></span></td>
<td><span data-ttu-id="64234-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-576">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-576">CC004</span></span></td>
<td><span data-ttu-id="64234-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-577">Packaging</span></span></td>
<td><span data-ttu-id="64234-578">35</span><span class="sxs-lookup"><span data-stu-id="64234-578">35</span></span></td>
<td><span data-ttu-id="64234-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="64234-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="64234-580">236.25</span><span class="sxs-lookup"><span data-stu-id="64234-580">236.25</span></span></td>
<td><span data-ttu-id="64234-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-582">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-582">CC003</span></span></td>
<td><span data-ttu-id="64234-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-583">Assembly</span></span></td>
<td><span data-ttu-id="64234-584">65</span><span class="sxs-lookup"><span data-stu-id="64234-584">65</span></span></td>
<td><span data-ttu-id="64234-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="64234-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="64234-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="64234-586">5,297.69</span></span></td>
<td><span data-ttu-id="64234-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-588">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-588">CC004</span></span></td>
<td><span data-ttu-id="64234-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-589">Packaging</span></span></td>
<td><span data-ttu-id="64234-590">35</span><span class="sxs-lookup"><span data-stu-id="64234-590">35</span></span></td>
<td><span data-ttu-id="64234-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="64234-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="64234-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="64234-592">2,852.60</span></span></td>
<td><span data-ttu-id="64234-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="64234-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-595">Cost object</span></span></th>
<th><span data-ttu-id="64234-596">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-596">Magnitude</span></span></th>
<th><span data-ttu-id="64234-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-597">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-598">Amount</span></span></th>
<th><span data-ttu-id="64234-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-600">Prod 1</span></span></td>
<td><span data-ttu-id="64234-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-601">Product 1</span></span></td>
<td><span data-ttu-id="64234-602">60</span><span class="sxs-lookup"><span data-stu-id="64234-602">60</span></span></td>
<td><span data-ttu-id="64234-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="64234-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="64234-604">535.31</span><span class="sxs-lookup"><span data-stu-id="64234-604">535.31</span></span></td>
<td><span data-ttu-id="64234-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-606">Prod 2</span></span></td>
<td><span data-ttu-id="64234-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-607">Product 2</span></span></td>
<td><span data-ttu-id="64234-608">20</span><span class="sxs-lookup"><span data-stu-id="64234-608">20</span></span></td>
<td><span data-ttu-id="64234-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="64234-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="64234-610">178.44</span><span class="sxs-lookup"><span data-stu-id="64234-610">178.44</span></span></td>
<td><span data-ttu-id="64234-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-612">Prod 1</span></span></td>
<td><span data-ttu-id="64234-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-613">Product 1</span></span></td>
<td><span data-ttu-id="64234-614">60</span><span class="sxs-lookup"><span data-stu-id="64234-614">60</span></span></td>
<td><span data-ttu-id="64234-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="64234-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="64234-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="64234-616">4,487.12</span></span></td>
<td><span data-ttu-id="64234-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-618">Prod 2</span></span></td>
<td><span data-ttu-id="64234-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-619">Product 2</span></span></td>
<td><span data-ttu-id="64234-620">20</span><span class="sxs-lookup"><span data-stu-id="64234-620">20</span></span></td>
<td><span data-ttu-id="64234-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="64234-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="64234-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="64234-622">1,495.71</span></span></td>
<td><span data-ttu-id="64234-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64234-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="64234-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-625">Cost object</span></span></th>
<th><span data-ttu-id="64234-626">Величина</span><span class="sxs-lookup"><span data-stu-id="64234-626">Magnitude</span></span></th>
<th><span data-ttu-id="64234-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="64234-627">Allocation factor</span></span></th>
<th><span data-ttu-id="64234-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-628">Amount</span></span></th>
<th><span data-ttu-id="64234-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-630">Prod 1</span></span></td>
<td><span data-ttu-id="64234-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-631">Product 1</span></span></td>
<td><span data-ttu-id="64234-632">80</span><span class="sxs-lookup"><span data-stu-id="64234-632">80</span></span></td>
<td><span data-ttu-id="64234-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="64234-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="64234-634">241.05</span><span class="sxs-lookup"><span data-stu-id="64234-634">241.05</span></span></td>
<td><span data-ttu-id="64234-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-636">Prod 2</span></span></td>
<td><span data-ttu-id="64234-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-637">Product 2</span></span></td>
<td><span data-ttu-id="64234-638">15</span><span class="sxs-lookup"><span data-stu-id="64234-638">15</span></span></td>
<td><span data-ttu-id="64234-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="64234-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="64234-640">45.20</span><span class="sxs-lookup"><span data-stu-id="64234-640">45.20</span></span></td>
<td><span data-ttu-id="64234-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-642">Prod 1</span></span></td>
<td><span data-ttu-id="64234-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-643">Product 1</span></span></td>
<td><span data-ttu-id="64234-644">80</span><span class="sxs-lookup"><span data-stu-id="64234-644">80</span></span></td>
<td><span data-ttu-id="64234-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="64234-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="64234-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="64234-646">2,507.09</span></span></td>
<td><span data-ttu-id="64234-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-648">Prod 2</span></span></td>
<td><span data-ttu-id="64234-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-649">Product 2</span></span></td>
<td><span data-ttu-id="64234-650">15</span><span class="sxs-lookup"><span data-stu-id="64234-650">15</span></span></td>
<td><span data-ttu-id="64234-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="64234-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="64234-652">470.08</span><span class="sxs-lookup"><span data-stu-id="64234-652">470.08</span></span></td>
<td><span data-ttu-id="64234-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="64234-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="64234-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="64234-655">Journal</span></span></th>
<th><span data-ttu-id="64234-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="64234-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="64234-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="64234-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="64234-658">Версия</span><span class="sxs-lookup"><span data-stu-id="64234-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-659">00004</span><span class="sxs-lookup"><span data-stu-id="64234-659">00004</span></span></td>
<td><span data-ttu-id="64234-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="64234-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="64234-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="64234-661">Fiscal</span></span></td>
<td><span data-ttu-id="64234-662">2017</span><span class="sxs-lookup"><span data-stu-id="64234-662">2017</span></span></td>
<td><span data-ttu-id="64234-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-663">Period 1</span></span></td>
<td><span data-ttu-id="64234-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="64234-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="64234-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="64234-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64234-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="64234-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-668">Cost element</span></span></th>
<th><span data-ttu-id="64234-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-669">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-672">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-672">CC001</span></span></td>
<td><span data-ttu-id="64234-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-673">HR</span></span></td>
<td><span data-ttu-id="64234-674">10001</span><span class="sxs-lookup"><span data-stu-id="64234-674">10001</span></span></td>
<td><span data-ttu-id="64234-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-675">Electricity</span></span></td>
<td><span data-ttu-id="64234-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-676">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-677">500.00</span><span class="sxs-lookup"><span data-stu-id="64234-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-679">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-679">CC001</span></span></td>
<td><span data-ttu-id="64234-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-680">HR</span></span></td>
<td><span data-ttu-id="64234-681">10001</span><span class="sxs-lookup"><span data-stu-id="64234-681">10001</span></span></td>
<td><span data-ttu-id="64234-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-682">Electricity</span></span></td>
<td><span data-ttu-id="64234-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-683">Variable cost</span></span></td>
<td><span data-ttu-id="64234-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="64234-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-686">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-686">CC002</span></span></td>
<td><span data-ttu-id="64234-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-687">Finance</span></span></td>
<td><span data-ttu-id="64234-688">10001</span><span class="sxs-lookup"><span data-stu-id="64234-688">10001</span></span></td>
<td><span data-ttu-id="64234-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-689">Electricity</span></span></td>
<td><span data-ttu-id="64234-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-690">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-691">675.00</span><span class="sxs-lookup"><span data-stu-id="64234-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-693">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-693">CC002</span></span></td>
<td><span data-ttu-id="64234-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-694">Finance</span></span></td>
<td><span data-ttu-id="64234-695">10001</span><span class="sxs-lookup"><span data-stu-id="64234-695">10001</span></span></td>
<td><span data-ttu-id="64234-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-696">Electricity</span></span></td>
<td><span data-ttu-id="64234-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-697">Variable cost</span></span></td>
<td><span data-ttu-id="64234-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="64234-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-700">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-700">CC003</span></span></td>
<td><span data-ttu-id="64234-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-701">Assembly</span></span></td>
<td><span data-ttu-id="64234-702">10001</span><span class="sxs-lookup"><span data-stu-id="64234-702">10001</span></span></td>
<td><span data-ttu-id="64234-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-703">Electricity</span></span></td>
<td><span data-ttu-id="64234-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-704">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-705">713.75</span><span class="sxs-lookup"><span data-stu-id="64234-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-707">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-707">CC003</span></span></td>
<td><span data-ttu-id="64234-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-708">Assembly</span></span></td>
<td><span data-ttu-id="64234-709">10001</span><span class="sxs-lookup"><span data-stu-id="64234-709">10001</span></span></td>
<td><span data-ttu-id="64234-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-710">Electricity</span></span></td>
<td><span data-ttu-id="64234-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-711">Variable cost</span></span></td>
<td><span data-ttu-id="64234-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="64234-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-714">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-714">CC003</span></span></td>
<td><span data-ttu-id="64234-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-715">Packaging</span></span></td>
<td><span data-ttu-id="64234-716">10001</span><span class="sxs-lookup"><span data-stu-id="64234-716">10001</span></span></td>
<td><span data-ttu-id="64234-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-717">Electricity</span></span></td>
<td><span data-ttu-id="64234-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-718">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-719">286.25</span><span class="sxs-lookup"><span data-stu-id="64234-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-721">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-721">CC003</span></span></td>
<td><span data-ttu-id="64234-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-722">Packaging</span></span></td>
<td><span data-ttu-id="64234-723">10001</span><span class="sxs-lookup"><span data-stu-id="64234-723">10001</span></span></td>
<td><span data-ttu-id="64234-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-724">Electricity</span></span></td>
<td><span data-ttu-id="64234-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-725">Variable cost</span></span></td>
<td><span data-ttu-id="64234-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="64234-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-728">Prod 1</span></span></td>
<td><span data-ttu-id="64234-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-729">Product 1</span></span></td>
<td><span data-ttu-id="64234-730">10001</span><span class="sxs-lookup"><span data-stu-id="64234-730">10001</span></span></td>
<td><span data-ttu-id="64234-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-731">Electricity</span></span></td>
<td><span data-ttu-id="64234-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-732">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-733">776.36</span><span class="sxs-lookup"><span data-stu-id="64234-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-735">Prod 1</span></span></td>
<td><span data-ttu-id="64234-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-736">Product 1</span></span></td>
<td><span data-ttu-id="64234-737">10001</span><span class="sxs-lookup"><span data-stu-id="64234-737">10001</span></span></td>
<td><span data-ttu-id="64234-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-738">Electricity</span></span></td>
<td><span data-ttu-id="64234-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-739">Variable cost</span></span></td>
<td><span data-ttu-id="64234-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="64234-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-742">Prod 2</span></span></td>
<td><span data-ttu-id="64234-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-743">Product 1</span></span></td>
<td><span data-ttu-id="64234-744">10001</span><span class="sxs-lookup"><span data-stu-id="64234-744">10001</span></span></td>
<td><span data-ttu-id="64234-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-745">Electricity</span></span></td>
<td><span data-ttu-id="64234-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-746">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-747">223.64</span><span class="sxs-lookup"><span data-stu-id="64234-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="64234-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-749">Prod 2</span></span></td>
<td><span data-ttu-id="64234-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-750">Product 1</span></span></td>
<td><span data-ttu-id="64234-751">10001</span><span class="sxs-lookup"><span data-stu-id="64234-751">10001</span></span></td>
<td><span data-ttu-id="64234-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-752">Electricity</span></span></td>
<td><span data-ttu-id="64234-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-753">Variable cost</span></span></td>
<td><span data-ttu-id="64234-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="64234-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="64234-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="64234-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="64234-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="64234-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-757">Cost element</span></span></th>
<th><span data-ttu-id="64234-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="64234-758">Cost behavior</span></span></th>
<th><span data-ttu-id="64234-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="64234-759">Amount</span></span></th>
<th><span data-ttu-id="64234-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="64234-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64234-761">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-761">CC001</span></span></td>
<td><span data-ttu-id="64234-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-762">HR</span></span></td>
<td><span data-ttu-id="64234-763">10001</span><span class="sxs-lookup"><span data-stu-id="64234-763">10001</span></span></td>
<td><span data-ttu-id="64234-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-764">Electricity</span></span></td>
<td><span data-ttu-id="64234-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-765">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="64234-766">-500.00</span></span></td>
<td><span data-ttu-id="64234-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-768">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-768">CC002</span></span></td>
<td><span data-ttu-id="64234-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-769">Finance</span></span></td>
<td><span data-ttu-id="64234-770">10001</span><span class="sxs-lookup"><span data-stu-id="64234-770">10001</span></span></td>
<td><span data-ttu-id="64234-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-771">Electricity</span></span></td>
<td><span data-ttu-id="64234-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-772">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-773">175.00</span><span class="sxs-lookup"><span data-stu-id="64234-773">175.00</span></span></td>
<td><span data-ttu-id="64234-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-775">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-775">CC003</span></span></td>
<td><span data-ttu-id="64234-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-776">Assembly</span></span></td>
<td><span data-ttu-id="64234-777">10001</span><span class="sxs-lookup"><span data-stu-id="64234-777">10001</span></span></td>
<td><span data-ttu-id="64234-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-778">Electricity</span></span></td>
<td><span data-ttu-id="64234-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-779">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-780">275.00</span><span class="sxs-lookup"><span data-stu-id="64234-780">275.00</span></span></td>
<td><span data-ttu-id="64234-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-782">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-782">CC004</span></span></td>
<td><span data-ttu-id="64234-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-783">Packaging</span></span></td>
<td><span data-ttu-id="64234-784">10001</span><span class="sxs-lookup"><span data-stu-id="64234-784">10001</span></span></td>
<td><span data-ttu-id="64234-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-785">Electricity</span></span></td>
<td><span data-ttu-id="64234-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-786">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-787">50,00</span><span class="sxs-lookup"><span data-stu-id="64234-787">50,00</span></span></td>
<td><span data-ttu-id="64234-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-789">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-789">CC001</span></span></td>
<td><span data-ttu-id="64234-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="64234-790">HR</span></span></td>
<td><span data-ttu-id="64234-791">10001</span><span class="sxs-lookup"><span data-stu-id="64234-791">10001</span></span></td>
<td><span data-ttu-id="64234-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-792">Electricity</span></span></td>
<td><span data-ttu-id="64234-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-793">Variable cost</span></span></td>
<td><span data-ttu-id="64234-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="64234-794">-1,245.71</span></span></td>
<td><span data-ttu-id="64234-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-796">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-796">CC002</span></span></td>
<td><span data-ttu-id="64234-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-797">Finance</span></span></td>
<td><span data-ttu-id="64234-798">10001</span><span class="sxs-lookup"><span data-stu-id="64234-798">10001</span></span></td>
<td><span data-ttu-id="64234-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-799">Electricity</span></span></td>
<td><span data-ttu-id="64234-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-800">Variable cost</span></span></td>
<td><span data-ttu-id="64234-801">436.00</span><span class="sxs-lookup"><span data-stu-id="64234-801">436.00</span></span></td>
<td><span data-ttu-id="64234-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-803">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-803">CC003</span></span></td>
<td><span data-ttu-id="64234-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-804">Assembly</span></span></td>
<td><span data-ttu-id="64234-805">10001</span><span class="sxs-lookup"><span data-stu-id="64234-805">10001</span></span></td>
<td><span data-ttu-id="64234-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-806">Electricity</span></span></td>
<td><span data-ttu-id="64234-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-807">Variable cost</span></span></td>
<td><span data-ttu-id="64234-808">685.14</span><span class="sxs-lookup"><span data-stu-id="64234-808">685.14</span></span></td>
<td><span data-ttu-id="64234-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-810">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-810">CC004</span></span></td>
<td><span data-ttu-id="64234-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-811">Packaging</span></span></td>
<td><span data-ttu-id="64234-812">10001</span><span class="sxs-lookup"><span data-stu-id="64234-812">10001</span></span></td>
<td><span data-ttu-id="64234-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-813">Electricity</span></span></td>
<td><span data-ttu-id="64234-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-814">Variable cost</span></span></td>
<td><span data-ttu-id="64234-815">124.57</span><span class="sxs-lookup"><span data-stu-id="64234-815">124.57</span></span></td>
<td><span data-ttu-id="64234-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-817">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-817">CC002</span></span></td>
<td><span data-ttu-id="64234-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-818">Finance</span></span></td>
<td><span data-ttu-id="64234-819">10001</span><span class="sxs-lookup"><span data-stu-id="64234-819">10001</span></span></td>
<td><span data-ttu-id="64234-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-820">Electricity</span></span></td>
<td><span data-ttu-id="64234-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-821">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="64234-822">-675.00</span></span></td>
<td><span data-ttu-id="64234-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-824">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-824">CC003</span></span></td>
<td><span data-ttu-id="64234-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-825">Assembly</span></span></td>
<td><span data-ttu-id="64234-826">10001</span><span class="sxs-lookup"><span data-stu-id="64234-826">10001</span></span></td>
<td><span data-ttu-id="64234-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-827">Electricity</span></span></td>
<td><span data-ttu-id="64234-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-828">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-829">438.75</span><span class="sxs-lookup"><span data-stu-id="64234-829">438.75</span></span></td>
<td><span data-ttu-id="64234-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-831">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-831">CC004</span></span></td>
<td><span data-ttu-id="64234-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-832">Packaging</span></span></td>
<td><span data-ttu-id="64234-833">10001</span><span class="sxs-lookup"><span data-stu-id="64234-833">10001</span></span></td>
<td><span data-ttu-id="64234-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-834">Electricity</span></span></td>
<td><span data-ttu-id="64234-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-835">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-836">236.25</span><span class="sxs-lookup"><span data-stu-id="64234-836">236.25</span></span></td>
<td><span data-ttu-id="64234-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-838">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-838">CC002</span></span></td>
<td><span data-ttu-id="64234-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="64234-839">Finance</span></span></td>
<td><span data-ttu-id="64234-840">10001</span><span class="sxs-lookup"><span data-stu-id="64234-840">10001</span></span></td>
<td><span data-ttu-id="64234-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-841">Electricity</span></span></td>
<td><span data-ttu-id="64234-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-842">Variable cost</span></span></td>
<td><span data-ttu-id="64234-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="64234-843">-8,150.29</span></span></td>
<td><span data-ttu-id="64234-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-845">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-845">CC003</span></span></td>
<td><span data-ttu-id="64234-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-846">Assembly</span></span></td>
<td><span data-ttu-id="64234-847">10001</span><span class="sxs-lookup"><span data-stu-id="64234-847">10001</span></span></td>
<td><span data-ttu-id="64234-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-848">Electricity</span></span></td>
<td><span data-ttu-id="64234-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-849">Variable cost</span></span></td>
<td><span data-ttu-id="64234-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="64234-850">5,297.69</span></span></td>
<td><span data-ttu-id="64234-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-852">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-852">CC004</span></span></td>
<td><span data-ttu-id="64234-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="64234-853">Packaging</span></span></td>
<td><span data-ttu-id="64234-854">10001</span><span class="sxs-lookup"><span data-stu-id="64234-854">10001</span></span></td>
<td><span data-ttu-id="64234-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-855">Electricity</span></span></td>
<td><span data-ttu-id="64234-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-856">Variable cost</span></span></td>
<td><span data-ttu-id="64234-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="64234-857">2,852.60</span></span></td>
<td><span data-ttu-id="64234-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-859">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-859">CC003</span></span></td>
<td><span data-ttu-id="64234-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-860">Assembly</span></span></td>
<td><span data-ttu-id="64234-861">10001</span><span class="sxs-lookup"><span data-stu-id="64234-861">10001</span></span></td>
<td><span data-ttu-id="64234-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-862">Electricity</span></span></td>
<td><span data-ttu-id="64234-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-863">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="64234-864">-713.75</span></span></td>
<td><span data-ttu-id="64234-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-866">Prod 1</span></span></td>
<td><span data-ttu-id="64234-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-867">Product 1</span></span></td>
<td><span data-ttu-id="64234-868">10001</span><span class="sxs-lookup"><span data-stu-id="64234-868">10001</span></span></td>
<td><span data-ttu-id="64234-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-869">Electricity</span></span></td>
<td><span data-ttu-id="64234-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-870">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-871">535.31</span><span class="sxs-lookup"><span data-stu-id="64234-871">535.31</span></span></td>
<td><span data-ttu-id="64234-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-873">Prod 2</span></span></td>
<td><span data-ttu-id="64234-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-874">Product 2</span></span></td>
<td><span data-ttu-id="64234-875">10001</span><span class="sxs-lookup"><span data-stu-id="64234-875">10001</span></span></td>
<td><span data-ttu-id="64234-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-876">Electricity</span></span></td>
<td><span data-ttu-id="64234-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-877">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-878">178.44</span><span class="sxs-lookup"><span data-stu-id="64234-878">178.44</span></span></td>
<td><span data-ttu-id="64234-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-880">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-880">CC003</span></span></td>
<td><span data-ttu-id="64234-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-881">Assembly</span></span></td>
<td><span data-ttu-id="64234-882">10001</span><span class="sxs-lookup"><span data-stu-id="64234-882">10001</span></span></td>
<td><span data-ttu-id="64234-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-883">Electricity</span></span></td>
<td><span data-ttu-id="64234-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-884">Variable cost</span></span></td>
<td><span data-ttu-id="64234-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="64234-885">-5,982.83</span></span></td>
<td><span data-ttu-id="64234-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-887">Prod 1</span></span></td>
<td><span data-ttu-id="64234-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-888">Product 1</span></span></td>
<td><span data-ttu-id="64234-889">10001</span><span class="sxs-lookup"><span data-stu-id="64234-889">10001</span></span></td>
<td><span data-ttu-id="64234-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-890">Electricity</span></span></td>
<td><span data-ttu-id="64234-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-891">Variable cost</span></span></td>
<td><span data-ttu-id="64234-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="64234-892">4,487.12</span></span></td>
<td><span data-ttu-id="64234-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-894">Prod 2</span></span></td>
<td><span data-ttu-id="64234-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-895">Product 2</span></span></td>
<td><span data-ttu-id="64234-896">10001</span><span class="sxs-lookup"><span data-stu-id="64234-896">10001</span></span></td>
<td><span data-ttu-id="64234-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-897">Electricity</span></span></td>
<td><span data-ttu-id="64234-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-898">Variable cost</span></span></td>
<td><span data-ttu-id="64234-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="64234-899">1,495.71</span></span></td>
<td><span data-ttu-id="64234-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-901">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-901">CC003</span></span></td>
<td><span data-ttu-id="64234-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-902">Assembly</span></span></td>
<td><span data-ttu-id="64234-903">10001</span><span class="sxs-lookup"><span data-stu-id="64234-903">10001</span></span></td>
<td><span data-ttu-id="64234-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-904">Electricity</span></span></td>
<td><span data-ttu-id="64234-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-905">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="64234-906">-286.25</span></span></td>
<td><span data-ttu-id="64234-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-908">Prod 1</span></span></td>
<td><span data-ttu-id="64234-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-909">Product 1</span></span></td>
<td><span data-ttu-id="64234-910">10001</span><span class="sxs-lookup"><span data-stu-id="64234-910">10001</span></span></td>
<td><span data-ttu-id="64234-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-911">Electricity</span></span></td>
<td><span data-ttu-id="64234-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-912">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-913">241.05</span><span class="sxs-lookup"><span data-stu-id="64234-913">241.05</span></span></td>
<td><span data-ttu-id="64234-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-915">Prod 2</span></span></td>
<td><span data-ttu-id="64234-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-916">Product 2</span></span></td>
<td><span data-ttu-id="64234-917">10001</span><span class="sxs-lookup"><span data-stu-id="64234-917">10001</span></span></td>
<td><span data-ttu-id="64234-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-918">Electricity</span></span></td>
<td><span data-ttu-id="64234-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-919">Fixed cost</span></span></td>
<td><span data-ttu-id="64234-920">45.20</span><span class="sxs-lookup"><span data-stu-id="64234-920">45.20</span></span></td>
<td><span data-ttu-id="64234-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-922">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-922">CC003</span></span></td>
<td><span data-ttu-id="64234-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="64234-923">Assembly</span></span></td>
<td><span data-ttu-id="64234-924">10001</span><span class="sxs-lookup"><span data-stu-id="64234-924">10001</span></span></td>
<td><span data-ttu-id="64234-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-925">Electricity</span></span></td>
<td><span data-ttu-id="64234-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-926">Variable cost</span></span></td>
<td><span data-ttu-id="64234-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="64234-927">-2,977.17</span></span></td>
<td><span data-ttu-id="64234-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-929">Prod 1</span></span></td>
<td><span data-ttu-id="64234-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="64234-930">Product 1</span></span></td>
<td><span data-ttu-id="64234-931">10001</span><span class="sxs-lookup"><span data-stu-id="64234-931">10001</span></span></td>
<td><span data-ttu-id="64234-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-932">Electricity</span></span></td>
<td><span data-ttu-id="64234-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-933">Variable cost</span></span></td>
<td><span data-ttu-id="64234-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="64234-934">2,507.09</span></span></td>
<td><span data-ttu-id="64234-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64234-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-936">Prod 2</span></span></td>
<td><span data-ttu-id="64234-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="64234-937">Product 2</span></span></td>
<td><span data-ttu-id="64234-938">10001</span><span class="sxs-lookup"><span data-stu-id="64234-938">10001</span></span></td>
<td><span data-ttu-id="64234-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-939">Electricity</span></span></td>
<td><span data-ttu-id="64234-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-940">Variable cost</span></span></td>
<td><span data-ttu-id="64234-941">470.08</span><span class="sxs-lookup"><span data-stu-id="64234-941">470.08</span></span></td>
<td><span data-ttu-id="64234-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="64234-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="64234-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="64234-943">Conclusion</span></span>
<span data-ttu-id="64234-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="64234-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="64234-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="64234-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="64234-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="64234-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="64234-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="64234-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="64234-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="64234-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="64234-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="64234-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64234-951">CC099</span><span class="sxs-lookup"><span data-stu-id="64234-951">CC099</span></span></th>
<th><span data-ttu-id="64234-952">CC001</span><span class="sxs-lookup"><span data-stu-id="64234-952">CC001</span></span></th>
<th><span data-ttu-id="64234-953">CC002</span><span class="sxs-lookup"><span data-stu-id="64234-953">CC002</span></span></th>
<th><span data-ttu-id="64234-954">CC003</span><span class="sxs-lookup"><span data-stu-id="64234-954">CC003</span></span></th>
<th><span data-ttu-id="64234-955">CC004</span><span class="sxs-lookup"><span data-stu-id="64234-955">CC004</span></span></th>
<th><span data-ttu-id="64234-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="64234-956">Proj 1</span></span></th>
<th><span data-ttu-id="64234-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="64234-957">Proj 2</span></span></th>
<th><span data-ttu-id="64234-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="64234-958">Prod 1</span></span></th>
<th><span data-ttu-id="64234-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="64234-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="64234-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="64234-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="64234-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="64234-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="64234-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="64234-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="64234-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-971">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="64234-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-973">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-974">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-975">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-976">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-977">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="64234-978">776.36</span><span class="sxs-lookup"><span data-stu-id="64234-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-979">223.64</span><span class="sxs-lookup"><span data-stu-id="64234-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="64234-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="64234-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-982">000</span><span class="sxs-lookup"><span data-stu-id="64234-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-983">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-984">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-985">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-986">0,00</span><span class="sxs-lookup"><span data-stu-id="64234-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-987">30.00</span><span class="sxs-lookup"><span data-stu-id="64234-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-988">10,00</span><span class="sxs-lookup"><span data-stu-id="64234-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="64234-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="64234-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="64234-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="64234-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="64234-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="64234-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="64234-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="64234-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="64234-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="64234-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="64234-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="64234-996">Дополнительные сведения см. в разделе [Политика свертки затрат и расчет накладных расходов](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="64234-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



