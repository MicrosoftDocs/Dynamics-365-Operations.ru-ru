---
title: "Расчет накладных расходов"
description: "В этом разделе описываются типовые процессы расчета и распределения накладных расходов."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 549e9b4b073a4e93dd3a1dd52dd6f43e7420a31b
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="8d105-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8d105-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8d105-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="8d105-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8d105-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="8d105-105">Term definition</span></span>
---------------

<span data-ttu-id="8d105-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="8d105-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8d105-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="8d105-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8d105-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="8d105-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8d105-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="8d105-109">Rent</span></span>
-   <span data-ttu-id="8d105-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-110">Electricity</span></span>
-   <span data-ttu-id="8d105-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="8d105-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8d105-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8d105-112">Overhead calculation overview</span></span>
<span data-ttu-id="8d105-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="8d105-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8d105-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="8d105-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8d105-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="8d105-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8d105-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="8d105-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8d105-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="8d105-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8d105-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="8d105-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8d105-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="8d105-119">Version type</span></span>
-   <span data-ttu-id="8d105-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="8d105-120">Date and time</span></span>
-   <span data-ttu-id="8d105-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8d105-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="8d105-122">Fiscal year</span></span>
-   <span data-ttu-id="8d105-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="8d105-123">Fiscal period</span></span>

<span data-ttu-id="8d105-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="8d105-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8d105-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="8d105-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8d105-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8d105-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8d105-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="8d105-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8d105-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="8d105-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8d105-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="8d105-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8d105-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="8d105-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8d105-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8d105-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8d105-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="8d105-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8d105-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="8d105-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8d105-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8d105-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="8d105-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8d105-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="8d105-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8d105-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8d105-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="8d105-140">Main account</span></span></th>
<th><span data-ttu-id="8d105-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="8d105-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8d105-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-143">CC099</span></span></td>
<td><span data-ttu-id="8d105-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-144">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-145">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-145">10001</span></span></td>
<td><span data-ttu-id="8d105-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-146">Electricity</span></span></td>
<td><span data-ttu-id="8d105-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8d105-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8d105-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8d105-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8d105-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="8d105-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8d105-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8d105-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="8d105-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8d105-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="8d105-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8d105-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="8d105-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8d105-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="8d105-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8d105-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8d105-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8d105-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8d105-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-160">Journal</span></span></th>
<th><span data-ttu-id="8d105-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8d105-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d105-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8d105-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d105-163">Версия</span><span class="sxs-lookup"><span data-stu-id="8d105-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-164">00001</span><span class="sxs-lookup"><span data-stu-id="8d105-164">00001</span></span></td>
<td><span data-ttu-id="8d105-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8d105-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8d105-166">Fiscal</span></span></td>
<td><span data-ttu-id="8d105-167">2017</span><span class="sxs-lookup"><span data-stu-id="8d105-167">2017</span></span></td>
<td><span data-ttu-id="8d105-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-168">Period 1</span></span></td>
<td><span data-ttu-id="8d105-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8d105-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="8d105-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-173">Cost element</span></span></th>
<th><span data-ttu-id="8d105-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8d105-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-177">CC099</span></span></td>
<td><span data-ttu-id="8d105-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-178">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-179">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-179">10001</span></span></td>
<td><span data-ttu-id="8d105-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-180">Electricity</span></span></td>
<td><span data-ttu-id="8d105-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8d105-181">Unclassified</span></span></td>
<td><span data-ttu-id="8d105-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8d105-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d105-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-185">Cost element</span></span></th>
<th><span data-ttu-id="8d105-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-187">Amount</span></span></th>
<th><span data-ttu-id="8d105-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-189">CC099</span></span></td>
<td><span data-ttu-id="8d105-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-190">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-191">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-191">10001</span></span></td>
<td><span data-ttu-id="8d105-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-192">Electricity</span></span></td>
<td><span data-ttu-id="8d105-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8d105-193">Unclassified</span></span></td>
<td><span data-ttu-id="8d105-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8d105-194">10,000.00</span></span></td>
<td><span data-ttu-id="8d105-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-196">CC099</span></span></td>
<td><span data-ttu-id="8d105-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-197">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-198">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-198">10001</span></span></td>
<td><span data-ttu-id="8d105-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-199">Electricity</span></span></td>
<td><span data-ttu-id="8d105-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8d105-200">Unclassified</span></span></td>
<td><span data-ttu-id="8d105-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8d105-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-203">CC099</span></span></td>
<td><span data-ttu-id="8d105-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-204">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-205">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-205">10001</span></span></td>
<td><span data-ttu-id="8d105-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-206">Electricity</span></span></td>
<td><span data-ttu-id="8d105-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-208">1,000.00</span></span></td>
<td><span data-ttu-id="8d105-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-210">CC099</span></span></td>
<td><span data-ttu-id="8d105-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-211">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-212">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-212">10001</span></span></td>
<td><span data-ttu-id="8d105-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-213">Electricity</span></span></td>
<td><span data-ttu-id="8d105-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-214">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8d105-215">9,000.00</span></span></td>
<td><span data-ttu-id="8d105-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-217">Подробные сведения о поведении затрат см. в разделе "Политика поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="8d105-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="8d105-218">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="8d105-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8d105-219">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8d105-220">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8d105-221">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8d105-222">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-222">Define the cost distribution rule</span></span>

<span data-ttu-id="8d105-223">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="8d105-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8d105-224">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="8d105-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8d105-225">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="8d105-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8d105-226">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="8d105-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8d105-227">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="8d105-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8d105-228">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-229">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-229">Cost object</span></span></th>
<th><span data-ttu-id="8d105-230">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="8d105-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-231">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-231">CC001</span></span></td>
<td><span data-ttu-id="8d105-232">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-232">HR</span></span></td>
<td><span data-ttu-id="8d105-233">1000</span><span class="sxs-lookup"><span data-stu-id="8d105-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-234">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-234">CC002</span></span></td>
<td><span data-ttu-id="8d105-235">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-235">Finance</span></span></td>
<td><span data-ttu-id="8d105-236">6,000</span><span class="sxs-lookup"><span data-stu-id="8d105-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-237">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-237">CC003</span></span></td>
<td><span data-ttu-id="8d105-238">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-238">Assembly</span></span></td>
<td><span data-ttu-id="8d105-239">0</span><span class="sxs-lookup"><span data-stu-id="8d105-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-240">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-241">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-241">Cost object</span></span></th>
<th><span data-ttu-id="8d105-242">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-242">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-243">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-243">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-244">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-245">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-245">CC001</span></span></td>
<td><span data-ttu-id="8d105-246">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-246">HR</span></span></td>
<td><span data-ttu-id="8d105-247">1000</span><span class="sxs-lookup"><span data-stu-id="8d105-247">1,000</span></span></td>
<td><span data-ttu-id="8d105-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8d105-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8d105-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-250">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-250">CC002</span></span></td>
<td><span data-ttu-id="8d105-251">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-251">Finance</span></span></td>
<td><span data-ttu-id="8d105-252">6,000</span><span class="sxs-lookup"><span data-stu-id="8d105-252">6,000</span></span></td>
<td><span data-ttu-id="8d105-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8d105-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8d105-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-255">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-255">CC003</span></span></td>
<td><span data-ttu-id="8d105-256">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-256">Assembly</span></span></td>
<td><span data-ttu-id="8d105-257">0</span><span class="sxs-lookup"><span data-stu-id="8d105-257">0</span></span></td>
<td><span data-ttu-id="8d105-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8d105-259">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-260">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="8d105-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8d105-261">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-262">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-262">Cost object</span></span></th>
<th><span data-ttu-id="8d105-263">Формула</span><span class="sxs-lookup"><span data-stu-id="8d105-263">Formula</span></span></th>
<th><span data-ttu-id="8d105-264">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-264">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-265">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-265">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-266">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-267">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-267">CC001</span></span></td>
<td><span data-ttu-id="8d105-268">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-268">HR</span></span></td>
<td><span data-ttu-id="8d105-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8d105-270">1</span><span class="sxs-lookup"><span data-stu-id="8d105-270">1</span></span></td>
<td><span data-ttu-id="8d105-271">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8d105-272">500.00</span><span class="sxs-lookup"><span data-stu-id="8d105-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-273">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-273">CC002</span></span></td>
<td><span data-ttu-id="8d105-274">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-274">Finance</span></span></td>
<td><span data-ttu-id="8d105-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8d105-276">1</span><span class="sxs-lookup"><span data-stu-id="8d105-276">1</span></span></td>
<td><span data-ttu-id="8d105-277">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8d105-278">500.00</span><span class="sxs-lookup"><span data-stu-id="8d105-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-279">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-279">CC003</span></span></td>
<td><span data-ttu-id="8d105-280">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-280">Assembly</span></span></td>
<td><span data-ttu-id="8d105-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8d105-282">0</span><span class="sxs-lookup"><span data-stu-id="8d105-282">0</span></span></td>
<td><span data-ttu-id="8d105-283">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8d105-284">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8d105-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-286">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-286">Journal</span></span></th>
<th><span data-ttu-id="8d105-287">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8d105-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d105-288">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8d105-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d105-289">Версия</span><span class="sxs-lookup"><span data-stu-id="8d105-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-290">00002</span><span class="sxs-lookup"><span data-stu-id="8d105-290">00002</span></span></td>
<td><span data-ttu-id="8d105-291">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8d105-292">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8d105-292">Fiscal</span></span></td>
<td><span data-ttu-id="8d105-293">2017</span><span class="sxs-lookup"><span data-stu-id="8d105-293">2017</span></span></td>
<td><span data-ttu-id="8d105-294">Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-294">Period 1</span></span></td>
<td><span data-ttu-id="8d105-295">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8d105-296">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="8d105-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-297">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-298">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-299">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-299">Cost element</span></span></th>
<th><span data-ttu-id="8d105-300">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-300">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-301">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-302">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-303">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-303">CC099</span></span></td>
<td><span data-ttu-id="8d105-304">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-304">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-305">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-305">10001</span></span></td>
<td><span data-ttu-id="8d105-306">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-306">Electricity</span></span></td>
<td><span data-ttu-id="8d105-307">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-307">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-309">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-310">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-310">CC099</span></span></td>
<td><span data-ttu-id="8d105-311">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-311">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-312">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-312">10001</span></span></td>
<td><span data-ttu-id="8d105-313">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-313">Electricity</span></span></td>
<td><span data-ttu-id="8d105-314">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-314">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8d105-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d105-316">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-317">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-318">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-318">Cost element</span></span></th>
<th><span data-ttu-id="8d105-319">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-319">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-320">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-320">Amount</span></span></th>
<th><span data-ttu-id="8d105-321">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-322">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-322">CC099</span></span></td>
<td><span data-ttu-id="8d105-323">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-323">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-324">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-324">10001</span></span></td>
<td><span data-ttu-id="8d105-325">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-325">Electricity</span></span></td>
<td><span data-ttu-id="8d105-326">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-326">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-327">-1,000.00</span></span></td>
<td><span data-ttu-id="8d105-328">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-329">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-329">CC001</span></span></td>
<td><span data-ttu-id="8d105-330">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-330">HR</span></span></td>
<td><span data-ttu-id="8d105-331">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-331">10001</span></span></td>
<td><span data-ttu-id="8d105-332">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-332">Electricity</span></span></td>
<td><span data-ttu-id="8d105-333">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-333">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-334">500.00</span><span class="sxs-lookup"><span data-stu-id="8d105-334">500.00</span></span></td>
<td><span data-ttu-id="8d105-335">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-336">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-336">CC002</span></span></td>
<td><span data-ttu-id="8d105-337">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-337">Finance</span></span></td>
<td><span data-ttu-id="8d105-338">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-338">10001</span></span></td>
<td><span data-ttu-id="8d105-339">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-339">Electricity</span></span></td>
<td><span data-ttu-id="8d105-340">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-340">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-341">500.00</span><span class="sxs-lookup"><span data-stu-id="8d105-341">500.00</span></span></td>
<td><span data-ttu-id="8d105-342">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-343">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-343">CC099</span></span></td>
<td><span data-ttu-id="8d105-344">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8d105-344">Default cost center</span></span></td>
<td><span data-ttu-id="8d105-345">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-345">10001</span></span></td>
<td><span data-ttu-id="8d105-346">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-346">Electricity</span></span></td>
<td><span data-ttu-id="8d105-347">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-347">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-348">-9000,00</span><span class="sxs-lookup"><span data-stu-id="8d105-348">-9,000.00</span></span></td>
<td><span data-ttu-id="8d105-349">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-350">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-350">CC001</span></span></td>
<td><span data-ttu-id="8d105-351">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-351">HR</span></span></td>
<td><span data-ttu-id="8d105-352">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-352">10001</span></span></td>
<td><span data-ttu-id="8d105-353">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-353">Electricity</span></span></td>
<td><span data-ttu-id="8d105-354">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-354">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8d105-355">1,285.71</span></span></td>
<td><span data-ttu-id="8d105-356">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-357">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-357">CC002</span></span></td>
<td><span data-ttu-id="8d105-358">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-358">Finance</span></span></td>
<td><span data-ttu-id="8d105-359">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-359">10001</span></span></td>
<td><span data-ttu-id="8d105-360">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-360">Electricity</span></span></td>
<td><span data-ttu-id="8d105-361">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-361">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8d105-362">7,714.29</span></span></td>
<td><span data-ttu-id="8d105-363">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-364">Подробные сведения о распределении затрат и базах распределения затрат см. в разделе "Политика распределения затрат и базы распределения".</span><span class="sxs-lookup"><span data-stu-id="8d105-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="8d105-365">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="8d105-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8d105-366">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8d105-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8d105-367">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8d105-368">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8d105-369">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8d105-369">Define the overhead rate</span></span>

<span data-ttu-id="8d105-370">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="8d105-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8d105-371">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8d105-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-372">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-372">Cost object</span></span></th>
<th><span data-ttu-id="8d105-373">Часы</span><span class="sxs-lookup"><span data-stu-id="8d105-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-374">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-374">Proj 1</span></span></td>
<td><span data-ttu-id="8d105-375">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-375">Project 1</span></span></td>
<td><span data-ttu-id="8d105-376">3</span><span class="sxs-lookup"><span data-stu-id="8d105-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-377">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-377">Proj 2</span></span></td>
<td><span data-ttu-id="8d105-378">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-378">Project 2</span></span></td>
<td><span data-ttu-id="8d105-379">1</span><span class="sxs-lookup"><span data-stu-id="8d105-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-380">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-381">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-381">Cost object</span></span></th>
<th><span data-ttu-id="8d105-382">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-382">Cost element</span></span></th>
<th><span data-ttu-id="8d105-383">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-383">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-384">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="8d105-384">Units</span></span></th>
<th><span data-ttu-id="8d105-385">По норме</span><span class="sxs-lookup"><span data-stu-id="8d105-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-386">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-386">CC001</span></span></td>
<td><span data-ttu-id="8d105-387">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-387">HR</span></span></td>
<td><span data-ttu-id="8d105-388">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-388">10001</span></span></td>
<td><span data-ttu-id="8d105-389">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-389">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-390">1</span><span class="sxs-lookup"><span data-stu-id="8d105-390">1</span></span></td>
<td><span data-ttu-id="8d105-391">10</span><span class="sxs-lookup"><span data-stu-id="8d105-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-392">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-393">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-393">Cost object</span></span></th>
<th><span data-ttu-id="8d105-394">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-394">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-395">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-395">Cost element</span></span></th>
<th><span data-ttu-id="8d105-396">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-396">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-397">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-398">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-398">Proj 1</span></span></td>
<td><span data-ttu-id="8d105-399">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-399">Project 1</span></span></td>
<td><span data-ttu-id="8d105-400">3</span><span class="sxs-lookup"><span data-stu-id="8d105-400">3</span></span></td>
<td><span data-ttu-id="8d105-401">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-401">10001</span></span></td>
<td><span data-ttu-id="8d105-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8d105-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8d105-403">30.00</span><span class="sxs-lookup"><span data-stu-id="8d105-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-404">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-404">Proj 2</span></span></td>
<td><span data-ttu-id="8d105-405">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-405">Project 2</span></span></td>
<td><span data-ttu-id="8d105-406">1</span><span class="sxs-lookup"><span data-stu-id="8d105-406">1</span></span></td>
<td><span data-ttu-id="8d105-407">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-407">10001</span></span></td>
<td><span data-ttu-id="8d105-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8d105-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8d105-409">10,00</span><span class="sxs-lookup"><span data-stu-id="8d105-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8d105-410">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-411">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-411">Journal</span></span></th>
<th><span data-ttu-id="8d105-412">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8d105-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d105-413">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8d105-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d105-414">Версия</span><span class="sxs-lookup"><span data-stu-id="8d105-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-415">00003</span><span class="sxs-lookup"><span data-stu-id="8d105-415">00003</span></span></td>
<td><span data-ttu-id="8d105-416">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="8d105-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8d105-417">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8d105-417">Fiscal</span></span></td>
<td><span data-ttu-id="8d105-418">2017</span><span class="sxs-lookup"><span data-stu-id="8d105-418">2017</span></span></td>
<td><span data-ttu-id="8d105-419">Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-419">Period 1</span></span></td>
<td><span data-ttu-id="8d105-420">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8d105-421">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="8d105-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-422">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-423">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-423">Cost object</span></span></th>
<th><span data-ttu-id="8d105-424">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-425">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-426">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-426">Proj 1</span></span></td>
<td><span data-ttu-id="8d105-427">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8d105-428">3,00</span><span class="sxs-lookup"><span data-stu-id="8d105-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-429">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-430">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-430">Proj 2</span></span></td>
<td><span data-ttu-id="8d105-431">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8d105-432">1.00</span><span class="sxs-lookup"><span data-stu-id="8d105-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d105-433">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-434">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-435">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-435">Cost element</span></span></th>
<th><span data-ttu-id="8d105-436">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-436">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-437">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-437">Amount</span></span></th>
<th><span data-ttu-id="8d105-438">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="8d105-439">CC0001</span></span></td>
<td><span data-ttu-id="8d105-440">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-440">HR</span></span></td>
<td><span data-ttu-id="8d105-441">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-441">10001</span></span></td>
<td><span data-ttu-id="8d105-442">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-442">Electricity</span></span></td>
<td><span data-ttu-id="8d105-443">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-443">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="8d105-444">-30.00</span></span></td>
<td><span data-ttu-id="8d105-445">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-446">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-446">Proj 1</span></span></td>
<td><span data-ttu-id="8d105-447">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8d105-448">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-448">10001</span></span></td>
<td><span data-ttu-id="8d105-449">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-449">Electricity</span></span></td>
<td><span data-ttu-id="8d105-450">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-450">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-451">30.00</span><span class="sxs-lookup"><span data-stu-id="8d105-451">30.00</span></span></td>
<td><span data-ttu-id="8d105-452">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-453">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-453">CC001</span></span></td>
<td><span data-ttu-id="8d105-454">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-454">HR</span></span></td>
<td><span data-ttu-id="8d105-455">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-455">10001</span></span></td>
<td><span data-ttu-id="8d105-456">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-456">Electricity</span></span></td>
<td><span data-ttu-id="8d105-457">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-457">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="8d105-458">-10.00</span></span></td>
<td><span data-ttu-id="8d105-459">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-460">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-460">Proj 2</span></span></td>
<td><span data-ttu-id="8d105-461">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8d105-462">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-462">10001</span></span></td>
<td><span data-ttu-id="8d105-463">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-463">Electricity</span></span></td>
<td><span data-ttu-id="8d105-464">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-464">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-465">10,00</span><span class="sxs-lookup"><span data-stu-id="8d105-465">10.00</span></span></td>
<td><span data-ttu-id="8d105-466">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-467">Подробные сведения о политике ставки накладных расходов см. в разделе "Политика ставки накладных расходов и базы распределения".</span><span class="sxs-lookup"><span data-stu-id="8d105-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="8d105-468">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="8d105-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8d105-469">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8d105-470">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8d105-471">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="8d105-472">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="8d105-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8d105-473">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="8d105-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8d105-474">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="8d105-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8d105-475">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="8d105-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8d105-476">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="8d105-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8d105-477">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8d105-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8d105-478">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-478">Define the cost allocation</span></span>

<span data-ttu-id="8d105-479">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8d105-480">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8d105-481">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8d105-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-482">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-482">Cost object</span></span></th>
<th><span data-ttu-id="8d105-483">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-484">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-484">CC002</span></span></td>
<td><span data-ttu-id="8d105-485">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-485">Finance</span></span></td>
<td><span data-ttu-id="8d105-486">35</span><span class="sxs-lookup"><span data-stu-id="8d105-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-487">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-487">CC003</span></span></td>
<td><span data-ttu-id="8d105-488">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-488">Assembly</span></span></td>
<td><span data-ttu-id="8d105-489">55</span><span class="sxs-lookup"><span data-stu-id="8d105-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-490">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-490">CC004</span></span></td>
<td><span data-ttu-id="8d105-491">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-491">Packaging</span></span></td>
<td><span data-ttu-id="8d105-492">10</span><span class="sxs-lookup"><span data-stu-id="8d105-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-493">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8d105-494">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8d105-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-495">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-495">Cost object</span></span></th>
<th><span data-ttu-id="8d105-496">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="8d105-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-497">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-497">CC003</span></span></td>
<td><span data-ttu-id="8d105-498">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-498">Assembly</span></span></td>
<td><span data-ttu-id="8d105-499">65</span><span class="sxs-lookup"><span data-stu-id="8d105-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-500">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-500">CC004</span></span></td>
<td><span data-ttu-id="8d105-501">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-501">Packaging</span></span></td>
<td><span data-ttu-id="8d105-502">35</span><span class="sxs-lookup"><span data-stu-id="8d105-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-503">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8d105-504">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8d105-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-505">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-505">Cost object</span></span></th>
<th><span data-ttu-id="8d105-506">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="8d105-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-507">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-507">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-508">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-508">Product 1</span></span></td>
<td><span data-ttu-id="8d105-509">60</span><span class="sxs-lookup"><span data-stu-id="8d105-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-510">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-510">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-511">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-511">Product 2</span></span></td>
<td><span data-ttu-id="8d105-512">20</span><span class="sxs-lookup"><span data-stu-id="8d105-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-513">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8d105-514">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="8d105-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-515">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-515">Cost object</span></span></th>
<th><span data-ttu-id="8d105-516">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="8d105-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-517">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-517">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-518">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-518">Product 1</span></span></td>
<td><span data-ttu-id="8d105-519">80</span><span class="sxs-lookup"><span data-stu-id="8d105-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-520">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-520">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-521">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-521">Product 2</span></span></td>
<td><span data-ttu-id="8d105-522">15</span><span class="sxs-lookup"><span data-stu-id="8d105-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-523">**Примечание.** В Finance and Operations статистические меры, такие как время производства, которое использует продукт, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="8d105-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8d105-524">Более подробные сведения о поставщиках статистических мер см. в разделе "Шаблоны поставщика статистической меры".</span><span class="sxs-lookup"><span data-stu-id="8d105-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="8d105-525">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.) В следующей таблице показан результат, когда услуги отдела кадров применяются в качестве базы распределения для общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8d105-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-526">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-526">Cost object</span></span></th>
<th><span data-ttu-id="8d105-527">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-527">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-528">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-528">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-529">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-529">Amount</span></span></th>
<th><span data-ttu-id="8d105-530">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-531">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-531">CC002</span></span></td>
<td><span data-ttu-id="8d105-532">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-532">Finance</span></span></td>
<td><span data-ttu-id="8d105-533">35</span><span class="sxs-lookup"><span data-stu-id="8d105-533">35</span></span></td>
<td><span data-ttu-id="8d105-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8d105-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8d105-535">175.00</span><span class="sxs-lookup"><span data-stu-id="8d105-535">175.00</span></span></td>
<td><span data-ttu-id="8d105-536">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-537">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-537">CC003</span></span></td>
<td><span data-ttu-id="8d105-538">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-538">Assembly</span></span></td>
<td><span data-ttu-id="8d105-539">55</span><span class="sxs-lookup"><span data-stu-id="8d105-539">55</span></span></td>
<td><span data-ttu-id="8d105-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8d105-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8d105-541">275.00</span><span class="sxs-lookup"><span data-stu-id="8d105-541">275.00</span></span></td>
<td><span data-ttu-id="8d105-542">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-543">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-543">CC004</span></span></td>
<td><span data-ttu-id="8d105-544">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-544">Packaging</span></span></td>
<td><span data-ttu-id="8d105-545">10</span><span class="sxs-lookup"><span data-stu-id="8d105-545">10</span></span></td>
<td><span data-ttu-id="8d105-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8d105-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8d105-547">50,00</span><span class="sxs-lookup"><span data-stu-id="8d105-547">50.00</span></span></td>
<td><span data-ttu-id="8d105-548">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-549">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-549">CC002</span></span></td>
<td><span data-ttu-id="8d105-550">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-550">Finance</span></span></td>
<td><span data-ttu-id="8d105-551">35</span><span class="sxs-lookup"><span data-stu-id="8d105-551">35</span></span></td>
<td><span data-ttu-id="8d105-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8d105-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8d105-553">436.00</span><span class="sxs-lookup"><span data-stu-id="8d105-553">436.00</span></span></td>
<td><span data-ttu-id="8d105-554">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-555">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-555">CC003</span></span></td>
<td><span data-ttu-id="8d105-556">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-556">Assembly</span></span></td>
<td><span data-ttu-id="8d105-557">55</span><span class="sxs-lookup"><span data-stu-id="8d105-557">55</span></span></td>
<td><span data-ttu-id="8d105-558">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8d105-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8d105-559">685.14</span><span class="sxs-lookup"><span data-stu-id="8d105-559">685.14</span></span></td>
<td><span data-ttu-id="8d105-560">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-561">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-561">CC004</span></span></td>
<td><span data-ttu-id="8d105-562">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-562">Packaging</span></span></td>
<td><span data-ttu-id="8d105-563">10</span><span class="sxs-lookup"><span data-stu-id="8d105-563">10</span></span></td>
<td><span data-ttu-id="8d105-564">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8d105-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8d105-565">124.57</span><span class="sxs-lookup"><span data-stu-id="8d105-565">124.57</span></span></td>
<td><span data-ttu-id="8d105-566">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-567">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8d105-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-568">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-568">Cost object</span></span></th>
<th><span data-ttu-id="8d105-569">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-569">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-570">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-570">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-571">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-571">Amount</span></span></th>
<th><span data-ttu-id="8d105-572">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-573">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-573">CC003</span></span></td>
<td><span data-ttu-id="8d105-574">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-574">Assembly</span></span></td>
<td><span data-ttu-id="8d105-575">65</span><span class="sxs-lookup"><span data-stu-id="8d105-575">65</span></span></td>
<td><span data-ttu-id="8d105-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8d105-577">438.75</span><span class="sxs-lookup"><span data-stu-id="8d105-577">438.75</span></span></td>
<td><span data-ttu-id="8d105-578">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-579">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-579">CC004</span></span></td>
<td><span data-ttu-id="8d105-580">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-580">Packaging</span></span></td>
<td><span data-ttu-id="8d105-581">35</span><span class="sxs-lookup"><span data-stu-id="8d105-581">35</span></span></td>
<td><span data-ttu-id="8d105-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8d105-583">236.25</span><span class="sxs-lookup"><span data-stu-id="8d105-583">236.25</span></span></td>
<td><span data-ttu-id="8d105-584">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-585">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-585">CC003</span></span></td>
<td><span data-ttu-id="8d105-586">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-586">Assembly</span></span></td>
<td><span data-ttu-id="8d105-587">65</span><span class="sxs-lookup"><span data-stu-id="8d105-587">65</span></span></td>
<td><span data-ttu-id="8d105-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8d105-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8d105-589">5,297.69</span></span></td>
<td><span data-ttu-id="8d105-590">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-591">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-591">CC004</span></span></td>
<td><span data-ttu-id="8d105-592">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-592">Packaging</span></span></td>
<td><span data-ttu-id="8d105-593">35</span><span class="sxs-lookup"><span data-stu-id="8d105-593">35</span></span></td>
<td><span data-ttu-id="8d105-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8d105-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8d105-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8d105-595">2,852.60</span></span></td>
<td><span data-ttu-id="8d105-596">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-597">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8d105-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-598">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-598">Cost object</span></span></th>
<th><span data-ttu-id="8d105-599">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-599">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-600">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-600">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-601">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-601">Amount</span></span></th>
<th><span data-ttu-id="8d105-602">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-603">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-603">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-604">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-604">Product 1</span></span></td>
<td><span data-ttu-id="8d105-605">60</span><span class="sxs-lookup"><span data-stu-id="8d105-605">60</span></span></td>
<td><span data-ttu-id="8d105-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8d105-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8d105-607">535.31</span><span class="sxs-lookup"><span data-stu-id="8d105-607">535.31</span></span></td>
<td><span data-ttu-id="8d105-608">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-609">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-609">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-610">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-610">Product 2</span></span></td>
<td><span data-ttu-id="8d105-611">20</span><span class="sxs-lookup"><span data-stu-id="8d105-611">20</span></span></td>
<td><span data-ttu-id="8d105-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8d105-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8d105-613">178.44</span><span class="sxs-lookup"><span data-stu-id="8d105-613">178.44</span></span></td>
<td><span data-ttu-id="8d105-614">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-615">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-615">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-616">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-616">Product 1</span></span></td>
<td><span data-ttu-id="8d105-617">60</span><span class="sxs-lookup"><span data-stu-id="8d105-617">60</span></span></td>
<td><span data-ttu-id="8d105-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8d105-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8d105-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8d105-619">4,487.12</span></span></td>
<td><span data-ttu-id="8d105-620">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-621">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-621">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-622">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-622">Product 2</span></span></td>
<td><span data-ttu-id="8d105-623">20</span><span class="sxs-lookup"><span data-stu-id="8d105-623">20</span></span></td>
<td><span data-ttu-id="8d105-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8d105-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8d105-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8d105-625">1,495.71</span></span></td>
<td><span data-ttu-id="8d105-626">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d105-627">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="8d105-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-628">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-628">Cost object</span></span></th>
<th><span data-ttu-id="8d105-629">Величина</span><span class="sxs-lookup"><span data-stu-id="8d105-629">Magnitude</span></span></th>
<th><span data-ttu-id="8d105-630">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="8d105-630">Allocation factor</span></span></th>
<th><span data-ttu-id="8d105-631">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-631">Amount</span></span></th>
<th><span data-ttu-id="8d105-632">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-633">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-633">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-634">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-634">Product 1</span></span></td>
<td><span data-ttu-id="8d105-635">80</span><span class="sxs-lookup"><span data-stu-id="8d105-635">80</span></span></td>
<td><span data-ttu-id="8d105-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8d105-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8d105-637">241.05</span><span class="sxs-lookup"><span data-stu-id="8d105-637">241.05</span></span></td>
<td><span data-ttu-id="8d105-638">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-639">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-639">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-640">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-640">Product 2</span></span></td>
<td><span data-ttu-id="8d105-641">15</span><span class="sxs-lookup"><span data-stu-id="8d105-641">15</span></span></td>
<td><span data-ttu-id="8d105-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8d105-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8d105-643">45.20</span><span class="sxs-lookup"><span data-stu-id="8d105-643">45.20</span></span></td>
<td><span data-ttu-id="8d105-644">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-645">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-645">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-646">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-646">Product 1</span></span></td>
<td><span data-ttu-id="8d105-647">80</span><span class="sxs-lookup"><span data-stu-id="8d105-647">80</span></span></td>
<td><span data-ttu-id="8d105-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8d105-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8d105-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8d105-649">2,507.09</span></span></td>
<td><span data-ttu-id="8d105-650">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-651">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-651">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-652">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-652">Product 2</span></span></td>
<td><span data-ttu-id="8d105-653">15</span><span class="sxs-lookup"><span data-stu-id="8d105-653">15</span></span></td>
<td><span data-ttu-id="8d105-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8d105-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8d105-655">470.08</span><span class="sxs-lookup"><span data-stu-id="8d105-655">470.08</span></span></td>
<td><span data-ttu-id="8d105-656">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8d105-657">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="8d105-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-658">Журнал</span><span class="sxs-lookup"><span data-stu-id="8d105-658">Journal</span></span></th>
<th><span data-ttu-id="8d105-659">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="8d105-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d105-660">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="8d105-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d105-661">Версия</span><span class="sxs-lookup"><span data-stu-id="8d105-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-662">00004</span><span class="sxs-lookup"><span data-stu-id="8d105-662">00004</span></span></td>
<td><span data-ttu-id="8d105-663">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8d105-664">Финансовый</span><span class="sxs-lookup"><span data-stu-id="8d105-664">Fiscal</span></span></td>
<td><span data-ttu-id="8d105-665">2017</span><span class="sxs-lookup"><span data-stu-id="8d105-665">2017</span></span></td>
<td><span data-ttu-id="8d105-666">Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-666">Period 1</span></span></td>
<td><span data-ttu-id="8d105-667">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="8d105-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8d105-668">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="8d105-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d105-669">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-670">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-671">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-671">Cost element</span></span></th>
<th><span data-ttu-id="8d105-672">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-672">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-673">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-674">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-675">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-675">CC001</span></span></td>
<td><span data-ttu-id="8d105-676">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-676">HR</span></span></td>
<td><span data-ttu-id="8d105-677">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-677">10001</span></span></td>
<td><span data-ttu-id="8d105-678">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-678">Electricity</span></span></td>
<td><span data-ttu-id="8d105-679">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-679">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-680">500.00</span><span class="sxs-lookup"><span data-stu-id="8d105-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-681">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-682">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-682">CC001</span></span></td>
<td><span data-ttu-id="8d105-683">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-683">HR</span></span></td>
<td><span data-ttu-id="8d105-684">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-684">10001</span></span></td>
<td><span data-ttu-id="8d105-685">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-685">Electricity</span></span></td>
<td><span data-ttu-id="8d105-686">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-686">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8d105-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-688">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-689">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-689">CC002</span></span></td>
<td><span data-ttu-id="8d105-690">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-690">Finance</span></span></td>
<td><span data-ttu-id="8d105-691">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-691">10001</span></span></td>
<td><span data-ttu-id="8d105-692">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-692">Electricity</span></span></td>
<td><span data-ttu-id="8d105-693">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-693">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-694">675.00</span><span class="sxs-lookup"><span data-stu-id="8d105-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-695">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-696">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-696">CC002</span></span></td>
<td><span data-ttu-id="8d105-697">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-697">Finance</span></span></td>
<td><span data-ttu-id="8d105-698">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-698">10001</span></span></td>
<td><span data-ttu-id="8d105-699">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-699">Electricity</span></span></td>
<td><span data-ttu-id="8d105-700">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-700">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8d105-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-702">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-703">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-703">CC003</span></span></td>
<td><span data-ttu-id="8d105-704">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-704">Assembly</span></span></td>
<td><span data-ttu-id="8d105-705">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-705">10001</span></span></td>
<td><span data-ttu-id="8d105-706">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-706">Electricity</span></span></td>
<td><span data-ttu-id="8d105-707">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-707">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-708">713.75</span><span class="sxs-lookup"><span data-stu-id="8d105-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-709">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-710">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-710">CC003</span></span></td>
<td><span data-ttu-id="8d105-711">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-711">Assembly</span></span></td>
<td><span data-ttu-id="8d105-712">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-712">10001</span></span></td>
<td><span data-ttu-id="8d105-713">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-713">Electricity</span></span></td>
<td><span data-ttu-id="8d105-714">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-714">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8d105-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-716">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-717">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-717">CC003</span></span></td>
<td><span data-ttu-id="8d105-718">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-718">Packaging</span></span></td>
<td><span data-ttu-id="8d105-719">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-719">10001</span></span></td>
<td><span data-ttu-id="8d105-720">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-720">Electricity</span></span></td>
<td><span data-ttu-id="8d105-721">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-721">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-722">286.25</span><span class="sxs-lookup"><span data-stu-id="8d105-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-723">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-724">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-724">CC003</span></span></td>
<td><span data-ttu-id="8d105-725">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-725">Packaging</span></span></td>
<td><span data-ttu-id="8d105-726">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-726">10001</span></span></td>
<td><span data-ttu-id="8d105-727">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-727">Electricity</span></span></td>
<td><span data-ttu-id="8d105-728">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-728">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8d105-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-730">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-731">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-731">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-732">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-732">Product 1</span></span></td>
<td><span data-ttu-id="8d105-733">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-733">10001</span></span></td>
<td><span data-ttu-id="8d105-734">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-734">Electricity</span></span></td>
<td><span data-ttu-id="8d105-735">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-735">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-736">776.36</span><span class="sxs-lookup"><span data-stu-id="8d105-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-737">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-738">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-738">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-739">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-739">Product 1</span></span></td>
<td><span data-ttu-id="8d105-740">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-740">10001</span></span></td>
<td><span data-ttu-id="8d105-741">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-741">Electricity</span></span></td>
<td><span data-ttu-id="8d105-742">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-742">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8d105-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-744">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-745">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-745">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-746">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-746">Product 1</span></span></td>
<td><span data-ttu-id="8d105-747">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-747">10001</span></span></td>
<td><span data-ttu-id="8d105-748">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-748">Electricity</span></span></td>
<td><span data-ttu-id="8d105-749">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-749">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-750">223.64</span><span class="sxs-lookup"><span data-stu-id="8d105-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-751">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d105-752">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-752">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-753">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-753">Product 1</span></span></td>
<td><span data-ttu-id="8d105-754">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-754">10001</span></span></td>
<td><span data-ttu-id="8d105-755">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-755">Electricity</span></span></td>
<td><span data-ttu-id="8d105-756">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-756">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8d105-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d105-758">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d105-759">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d105-760">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-760">Cost element</span></span></th>
<th><span data-ttu-id="8d105-761">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-761">Cost behavior</span></span></th>
<th><span data-ttu-id="8d105-762">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="8d105-762">Amount</span></span></th>
<th><span data-ttu-id="8d105-763">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="8d105-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d105-764">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-764">CC001</span></span></td>
<td><span data-ttu-id="8d105-765">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-765">HR</span></span></td>
<td><span data-ttu-id="8d105-766">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-766">10001</span></span></td>
<td><span data-ttu-id="8d105-767">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-767">Electricity</span></span></td>
<td><span data-ttu-id="8d105-768">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-768">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="8d105-769">-500.00</span></span></td>
<td><span data-ttu-id="8d105-770">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-771">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-771">CC002</span></span></td>
<td><span data-ttu-id="8d105-772">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-772">Finance</span></span></td>
<td><span data-ttu-id="8d105-773">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-773">10001</span></span></td>
<td><span data-ttu-id="8d105-774">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-774">Electricity</span></span></td>
<td><span data-ttu-id="8d105-775">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-775">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-776">175.00</span><span class="sxs-lookup"><span data-stu-id="8d105-776">175.00</span></span></td>
<td><span data-ttu-id="8d105-777">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-778">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-778">CC003</span></span></td>
<td><span data-ttu-id="8d105-779">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-779">Assembly</span></span></td>
<td><span data-ttu-id="8d105-780">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-780">10001</span></span></td>
<td><span data-ttu-id="8d105-781">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-781">Electricity</span></span></td>
<td><span data-ttu-id="8d105-782">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-782">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-783">275.00</span><span class="sxs-lookup"><span data-stu-id="8d105-783">275.00</span></span></td>
<td><span data-ttu-id="8d105-784">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-785">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-785">CC004</span></span></td>
<td><span data-ttu-id="8d105-786">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-786">Packaging</span></span></td>
<td><span data-ttu-id="8d105-787">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-787">10001</span></span></td>
<td><span data-ttu-id="8d105-788">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-788">Electricity</span></span></td>
<td><span data-ttu-id="8d105-789">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-789">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-790">50,00</span><span class="sxs-lookup"><span data-stu-id="8d105-790">50,00</span></span></td>
<td><span data-ttu-id="8d105-791">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-792">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-792">CC001</span></span></td>
<td><span data-ttu-id="8d105-793">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="8d105-793">HR</span></span></td>
<td><span data-ttu-id="8d105-794">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-794">10001</span></span></td>
<td><span data-ttu-id="8d105-795">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-795">Electricity</span></span></td>
<td><span data-ttu-id="8d105-796">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-796">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-797">-1245,71</span><span class="sxs-lookup"><span data-stu-id="8d105-797">-1,245.71</span></span></td>
<td><span data-ttu-id="8d105-798">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-799">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-799">CC002</span></span></td>
<td><span data-ttu-id="8d105-800">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-800">Finance</span></span></td>
<td><span data-ttu-id="8d105-801">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-801">10001</span></span></td>
<td><span data-ttu-id="8d105-802">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-802">Electricity</span></span></td>
<td><span data-ttu-id="8d105-803">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-803">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-804">436.00</span><span class="sxs-lookup"><span data-stu-id="8d105-804">436.00</span></span></td>
<td><span data-ttu-id="8d105-805">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-806">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-806">CC003</span></span></td>
<td><span data-ttu-id="8d105-807">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-807">Assembly</span></span></td>
<td><span data-ttu-id="8d105-808">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-808">10001</span></span></td>
<td><span data-ttu-id="8d105-809">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-809">Electricity</span></span></td>
<td><span data-ttu-id="8d105-810">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-810">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-811">685.14</span><span class="sxs-lookup"><span data-stu-id="8d105-811">685.14</span></span></td>
<td><span data-ttu-id="8d105-812">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-813">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-813">CC004</span></span></td>
<td><span data-ttu-id="8d105-814">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-814">Packaging</span></span></td>
<td><span data-ttu-id="8d105-815">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-815">10001</span></span></td>
<td><span data-ttu-id="8d105-816">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-816">Electricity</span></span></td>
<td><span data-ttu-id="8d105-817">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-817">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-818">124.57</span><span class="sxs-lookup"><span data-stu-id="8d105-818">124.57</span></span></td>
<td><span data-ttu-id="8d105-819">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-820">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-820">CC002</span></span></td>
<td><span data-ttu-id="8d105-821">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-821">Finance</span></span></td>
<td><span data-ttu-id="8d105-822">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-822">10001</span></span></td>
<td><span data-ttu-id="8d105-823">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-823">Electricity</span></span></td>
<td><span data-ttu-id="8d105-824">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-824">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="8d105-825">-675.00</span></span></td>
<td><span data-ttu-id="8d105-826">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-827">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-827">CC003</span></span></td>
<td><span data-ttu-id="8d105-828">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-828">Assembly</span></span></td>
<td><span data-ttu-id="8d105-829">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-829">10001</span></span></td>
<td><span data-ttu-id="8d105-830">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-830">Electricity</span></span></td>
<td><span data-ttu-id="8d105-831">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-831">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-832">438.75</span><span class="sxs-lookup"><span data-stu-id="8d105-832">438.75</span></span></td>
<td><span data-ttu-id="8d105-833">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-834">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-834">CC004</span></span></td>
<td><span data-ttu-id="8d105-835">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-835">Packaging</span></span></td>
<td><span data-ttu-id="8d105-836">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-836">10001</span></span></td>
<td><span data-ttu-id="8d105-837">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-837">Electricity</span></span></td>
<td><span data-ttu-id="8d105-838">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-838">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-839">236.25</span><span class="sxs-lookup"><span data-stu-id="8d105-839">236.25</span></span></td>
<td><span data-ttu-id="8d105-840">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-841">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-841">CC002</span></span></td>
<td><span data-ttu-id="8d105-842">Финансы</span><span class="sxs-lookup"><span data-stu-id="8d105-842">Finance</span></span></td>
<td><span data-ttu-id="8d105-843">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-843">10001</span></span></td>
<td><span data-ttu-id="8d105-844">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-844">Electricity</span></span></td>
<td><span data-ttu-id="8d105-845">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-845">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-846">-8150,29</span><span class="sxs-lookup"><span data-stu-id="8d105-846">-8,150.29</span></span></td>
<td><span data-ttu-id="8d105-847">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-848">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-848">CC003</span></span></td>
<td><span data-ttu-id="8d105-849">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-849">Assembly</span></span></td>
<td><span data-ttu-id="8d105-850">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-850">10001</span></span></td>
<td><span data-ttu-id="8d105-851">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-851">Electricity</span></span></td>
<td><span data-ttu-id="8d105-852">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-852">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8d105-853">5,297.69</span></span></td>
<td><span data-ttu-id="8d105-854">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-855">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-855">CC004</span></span></td>
<td><span data-ttu-id="8d105-856">Упаковка</span><span class="sxs-lookup"><span data-stu-id="8d105-856">Packaging</span></span></td>
<td><span data-ttu-id="8d105-857">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-857">10001</span></span></td>
<td><span data-ttu-id="8d105-858">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-858">Electricity</span></span></td>
<td><span data-ttu-id="8d105-859">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-859">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8d105-860">2,852.60</span></span></td>
<td><span data-ttu-id="8d105-861">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-862">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-862">CC003</span></span></td>
<td><span data-ttu-id="8d105-863">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-863">Assembly</span></span></td>
<td><span data-ttu-id="8d105-864">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-864">10001</span></span></td>
<td><span data-ttu-id="8d105-865">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-865">Electricity</span></span></td>
<td><span data-ttu-id="8d105-866">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-866">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="8d105-867">-713.75</span></span></td>
<td><span data-ttu-id="8d105-868">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-869">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-869">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-870">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-870">Product 1</span></span></td>
<td><span data-ttu-id="8d105-871">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-871">10001</span></span></td>
<td><span data-ttu-id="8d105-872">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-872">Electricity</span></span></td>
<td><span data-ttu-id="8d105-873">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-873">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-874">535.31</span><span class="sxs-lookup"><span data-stu-id="8d105-874">535.31</span></span></td>
<td><span data-ttu-id="8d105-875">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-876">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-876">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-877">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-877">Product 2</span></span></td>
<td><span data-ttu-id="8d105-878">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-878">10001</span></span></td>
<td><span data-ttu-id="8d105-879">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-879">Electricity</span></span></td>
<td><span data-ttu-id="8d105-880">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-880">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-881">178.44</span><span class="sxs-lookup"><span data-stu-id="8d105-881">178.44</span></span></td>
<td><span data-ttu-id="8d105-882">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-883">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-883">CC003</span></span></td>
<td><span data-ttu-id="8d105-884">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-884">Assembly</span></span></td>
<td><span data-ttu-id="8d105-885">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-885">10001</span></span></td>
<td><span data-ttu-id="8d105-886">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-886">Electricity</span></span></td>
<td><span data-ttu-id="8d105-887">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-887">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-888">-5982,83</span><span class="sxs-lookup"><span data-stu-id="8d105-888">-5,982.83</span></span></td>
<td><span data-ttu-id="8d105-889">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-890">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-890">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-891">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-891">Product 1</span></span></td>
<td><span data-ttu-id="8d105-892">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-892">10001</span></span></td>
<td><span data-ttu-id="8d105-893">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-893">Electricity</span></span></td>
<td><span data-ttu-id="8d105-894">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-894">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8d105-895">4,487.12</span></span></td>
<td><span data-ttu-id="8d105-896">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-897">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-897">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-898">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-898">Product 2</span></span></td>
<td><span data-ttu-id="8d105-899">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-899">10001</span></span></td>
<td><span data-ttu-id="8d105-900">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-900">Electricity</span></span></td>
<td><span data-ttu-id="8d105-901">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-901">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8d105-902">1,495.71</span></span></td>
<td><span data-ttu-id="8d105-903">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-904">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-904">CC003</span></span></td>
<td><span data-ttu-id="8d105-905">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-905">Assembly</span></span></td>
<td><span data-ttu-id="8d105-906">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-906">10001</span></span></td>
<td><span data-ttu-id="8d105-907">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-907">Electricity</span></span></td>
<td><span data-ttu-id="8d105-908">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-908">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="8d105-909">-286.25</span></span></td>
<td><span data-ttu-id="8d105-910">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-911">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-911">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-912">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-912">Product 1</span></span></td>
<td><span data-ttu-id="8d105-913">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-913">10001</span></span></td>
<td><span data-ttu-id="8d105-914">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-914">Electricity</span></span></td>
<td><span data-ttu-id="8d105-915">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-915">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-916">241.05</span><span class="sxs-lookup"><span data-stu-id="8d105-916">241.05</span></span></td>
<td><span data-ttu-id="8d105-917">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-918">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-918">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-919">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-919">Product 2</span></span></td>
<td><span data-ttu-id="8d105-920">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-920">10001</span></span></td>
<td><span data-ttu-id="8d105-921">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-921">Electricity</span></span></td>
<td><span data-ttu-id="8d105-922">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-922">Fixed cost</span></span></td>
<td><span data-ttu-id="8d105-923">45.20</span><span class="sxs-lookup"><span data-stu-id="8d105-923">45.20</span></span></td>
<td><span data-ttu-id="8d105-924">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-925">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-925">CC003</span></span></td>
<td><span data-ttu-id="8d105-926">Сборка</span><span class="sxs-lookup"><span data-stu-id="8d105-926">Assembly</span></span></td>
<td><span data-ttu-id="8d105-927">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-927">10001</span></span></td>
<td><span data-ttu-id="8d105-928">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-928">Electricity</span></span></td>
<td><span data-ttu-id="8d105-929">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-929">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="8d105-930">-2,977.17</span></span></td>
<td><span data-ttu-id="8d105-931">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-932">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-932">Prod 1</span></span></td>
<td><span data-ttu-id="8d105-933">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="8d105-933">Product 1</span></span></td>
<td><span data-ttu-id="8d105-934">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-934">10001</span></span></td>
<td><span data-ttu-id="8d105-935">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-935">Electricity</span></span></td>
<td><span data-ttu-id="8d105-936">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-936">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8d105-937">2,507.09</span></span></td>
<td><span data-ttu-id="8d105-938">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d105-939">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-939">Prod 2</span></span></td>
<td><span data-ttu-id="8d105-940">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="8d105-940">Product 2</span></span></td>
<td><span data-ttu-id="8d105-941">10001</span><span class="sxs-lookup"><span data-stu-id="8d105-941">10001</span></span></td>
<td><span data-ttu-id="8d105-942">Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-942">Electricity</span></span></td>
<td><span data-ttu-id="8d105-943">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-943">Variable cost</span></span></td>
<td><span data-ttu-id="8d105-944">470.08</span><span class="sxs-lookup"><span data-stu-id="8d105-944">470.08</span></span></td>
<td><span data-ttu-id="8d105-945">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="8d105-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8d105-946">Заключение</span><span class="sxs-lookup"><span data-stu-id="8d105-946">Conclusion</span></span>
<span data-ttu-id="8d105-947">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8d105-948">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="8d105-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8d105-949">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="8d105-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8d105-950">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8d105-951">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8d105-952">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="8d105-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8d105-953">Итоговый</span><span class="sxs-lookup"><span data-stu-id="8d105-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8d105-954">CC099</span><span class="sxs-lookup"><span data-stu-id="8d105-954">CC099</span></span></th>
<th><span data-ttu-id="8d105-955">CC001</span><span class="sxs-lookup"><span data-stu-id="8d105-955">CC001</span></span></th>
<th><span data-ttu-id="8d105-956">CC002</span><span class="sxs-lookup"><span data-stu-id="8d105-956">CC002</span></span></th>
<th><span data-ttu-id="8d105-957">CC003</span><span class="sxs-lookup"><span data-stu-id="8d105-957">CC003</span></span></th>
<th><span data-ttu-id="8d105-958">CC004</span><span class="sxs-lookup"><span data-stu-id="8d105-958">CC004</span></span></th>
<th><span data-ttu-id="8d105-959">Проект 1</span><span class="sxs-lookup"><span data-stu-id="8d105-959">Proj 1</span></span></th>
<th><span data-ttu-id="8d105-960">Проект 2</span><span class="sxs-lookup"><span data-stu-id="8d105-960">Proj 2</span></span></th>
<th><span data-ttu-id="8d105-961">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="8d105-961">Prod 1</span></span></th>
<th><span data-ttu-id="8d105-962">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="8d105-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8d105-963">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="8d105-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8d105-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8d105-973">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="8d105-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8d105-975">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-978">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-979">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-980">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8d105-981">776.36</span><span class="sxs-lookup"><span data-stu-id="8d105-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-982">223.64</span><span class="sxs-lookup"><span data-stu-id="8d105-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8d105-984">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="8d105-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-985">000</span><span class="sxs-lookup"><span data-stu-id="8d105-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-987">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-988">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-989">0,00</span><span class="sxs-lookup"><span data-stu-id="8d105-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-990">30.00</span><span class="sxs-lookup"><span data-stu-id="8d105-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-991">10,00</span><span class="sxs-lookup"><span data-stu-id="8d105-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8d105-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8d105-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d105-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8d105-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8d105-995">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8d105-996">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="8d105-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8d105-997">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8d105-998">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="8d105-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8d105-999">Для получения дополнительных сведений см. политику свертки затрат.</span><span class="sxs-lookup"><span data-stu-id="8d105-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="8d105-1000">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="8d105-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




