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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 285799d70a945c2dae1e3c65296282d5c432a243
ms.contentlocale: ru-ru
ms.lasthandoff: 10/30/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="10359-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="10359-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="10359-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="10359-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="10359-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="10359-105">Term definition</span></span>
---------------

<span data-ttu-id="10359-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="10359-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="10359-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="10359-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="10359-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="10359-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="10359-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="10359-109">Rent</span></span>
-   <span data-ttu-id="10359-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-110">Electricity</span></span>
-   <span data-ttu-id="10359-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="10359-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="10359-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="10359-112">Overhead calculation overview</span></span>
<span data-ttu-id="10359-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="10359-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="10359-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="10359-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="10359-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="10359-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="10359-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="10359-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="10359-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="10359-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="10359-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="10359-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="10359-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="10359-119">Version type</span></span>
-   <span data-ttu-id="10359-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="10359-120">Date and time</span></span>
-   <span data-ttu-id="10359-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="10359-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="10359-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="10359-122">Fiscal year</span></span>
-   <span data-ttu-id="10359-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="10359-123">Fiscal period</span></span>

<span data-ttu-id="10359-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="10359-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="10359-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="10359-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="10359-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="10359-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="10359-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="10359-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="10359-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="10359-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="10359-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="10359-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="10359-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="10359-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="10359-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="10359-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="10359-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="10359-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="10359-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="10359-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="10359-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="10359-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="10359-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="10359-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="10359-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="10359-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="10359-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10359-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="10359-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="10359-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="10359-140">Main account</span></span></th>
<th><span data-ttu-id="10359-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="10359-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="10359-143">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-143">CC099</span></span></td>
<td><span data-ttu-id="10359-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-144">Default cost center</span></span></td>
<td><span data-ttu-id="10359-145">10001</span><span class="sxs-lookup"><span data-stu-id="10359-145">10001</span></span></td>
<td><span data-ttu-id="10359-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-146">Electricity</span></span></td>
<td><span data-ttu-id="10359-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="10359-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="10359-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="10359-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="10359-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="10359-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="10359-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-151">Define the cost behavior rule</span></span>

<span data-ttu-id="10359-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="10359-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="10359-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="10359-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="10359-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="10359-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="10359-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="10359-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="10359-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="10359-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="10359-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="10359-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="10359-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-160">Journal</span></span></th>
<th><span data-ttu-id="10359-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="10359-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10359-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="10359-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10359-163">Версия</span><span class="sxs-lookup"><span data-stu-id="10359-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-164">00001</span><span class="sxs-lookup"><span data-stu-id="10359-164">00001</span></span></td>
<td><span data-ttu-id="10359-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="10359-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="10359-166">Fiscal</span></span></td>
<td><span data-ttu-id="10359-167">2017</span><span class="sxs-lookup"><span data-stu-id="10359-167">2017</span></span></td>
<td><span data-ttu-id="10359-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-168">Period 1</span></span></td>
<td><span data-ttu-id="10359-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="10359-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="10359-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10359-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-173">Cost element</span></span></th>
<th><span data-ttu-id="10359-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-174">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="10359-177">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-177">CC099</span></span></td>
<td><span data-ttu-id="10359-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-178">Default cost center</span></span></td>
<td><span data-ttu-id="10359-179">10001</span><span class="sxs-lookup"><span data-stu-id="10359-179">10001</span></span></td>
<td><span data-ttu-id="10359-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-180">Electricity</span></span></td>
<td><span data-ttu-id="10359-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="10359-181">Unclassified</span></span></td>
<td><span data-ttu-id="10359-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="10359-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10359-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="10359-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-185">Cost element</span></span></th>
<th><span data-ttu-id="10359-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-186">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-187">Amount</span></span></th>
<th><span data-ttu-id="10359-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-189">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-189">CC099</span></span></td>
<td><span data-ttu-id="10359-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-190">Default cost center</span></span></td>
<td><span data-ttu-id="10359-191">10001</span><span class="sxs-lookup"><span data-stu-id="10359-191">10001</span></span></td>
<td><span data-ttu-id="10359-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-192">Electricity</span></span></td>
<td><span data-ttu-id="10359-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="10359-193">Unclassified</span></span></td>
<td><span data-ttu-id="10359-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="10359-194">10,000.00</span></span></td>
<td><span data-ttu-id="10359-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-196">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-196">CC099</span></span></td>
<td><span data-ttu-id="10359-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-197">Default cost center</span></span></td>
<td><span data-ttu-id="10359-198">10001</span><span class="sxs-lookup"><span data-stu-id="10359-198">10001</span></span></td>
<td><span data-ttu-id="10359-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-199">Electricity</span></span></td>
<td><span data-ttu-id="10359-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="10359-200">Unclassified</span></span></td>
<td><span data-ttu-id="10359-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="10359-201">-10,000.00</span></span></td>
<td><span data-ttu-id="10359-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-203">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-203">CC099</span></span></td>
<td><span data-ttu-id="10359-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-204">Default cost center</span></span></td>
<td><span data-ttu-id="10359-205">10001</span><span class="sxs-lookup"><span data-stu-id="10359-205">10001</span></span></td>
<td><span data-ttu-id="10359-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-206">Electricity</span></span></td>
<td><span data-ttu-id="10359-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-207">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="10359-208">1,000.00</span></span></td>
<td><span data-ttu-id="10359-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-210">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-210">CC099</span></span></td>
<td><span data-ttu-id="10359-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-211">Default cost center</span></span></td>
<td><span data-ttu-id="10359-212">10001</span><span class="sxs-lookup"><span data-stu-id="10359-212">10001</span></span></td>
<td><span data-ttu-id="10359-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-213">Electricity</span></span></td>
<td><span data-ttu-id="10359-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-214">Variable cost</span></span></td>
<td><span data-ttu-id="10359-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="10359-215">9,000.00</span></span></td>
<td><span data-ttu-id="10359-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-217">Подробные сведения о поведении затрат см. в разделе "Политика поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="10359-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="10359-218">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="10359-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="10359-219">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="10359-220">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="10359-221">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="10359-222">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-222">Define the cost distribution rule</span></span>

<span data-ttu-id="10359-223">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="10359-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="10359-224">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="10359-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="10359-225">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="10359-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="10359-226">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="10359-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="10359-227">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="10359-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="10359-228">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-229">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-229">Cost object</span></span></th>
<th><span data-ttu-id="10359-230">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="10359-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-231">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-231">CC001</span></span></td>
<td><span data-ttu-id="10359-232">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-232">HR</span></span></td>
<td><span data-ttu-id="10359-233">1000</span><span class="sxs-lookup"><span data-stu-id="10359-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-234">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-234">CC002</span></span></td>
<td><span data-ttu-id="10359-235">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-235">Finance</span></span></td>
<td><span data-ttu-id="10359-236">6,000</span><span class="sxs-lookup"><span data-stu-id="10359-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-237">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-237">CC003</span></span></td>
<td><span data-ttu-id="10359-238">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-238">Assembly</span></span></td>
<td><span data-ttu-id="10359-239">0</span><span class="sxs-lookup"><span data-stu-id="10359-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-240">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-241">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-241">Cost object</span></span></th>
<th><span data-ttu-id="10359-242">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-242">Magnitude</span></span></th>
<th><span data-ttu-id="10359-243">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-243">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-244">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-245">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-245">CC001</span></span></td>
<td><span data-ttu-id="10359-246">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-246">HR</span></span></td>
<td><span data-ttu-id="10359-247">1000</span><span class="sxs-lookup"><span data-stu-id="10359-247">1,000</span></span></td>
<td><span data-ttu-id="10359-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="10359-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="10359-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="10359-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-250">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-250">CC002</span></span></td>
<td><span data-ttu-id="10359-251">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-251">Finance</span></span></td>
<td><span data-ttu-id="10359-252">6,000</span><span class="sxs-lookup"><span data-stu-id="10359-252">6,000</span></span></td>
<td><span data-ttu-id="10359-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="10359-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="10359-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="10359-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-255">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-255">CC003</span></span></td>
<td><span data-ttu-id="10359-256">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-256">Assembly</span></span></td>
<td><span data-ttu-id="10359-257">0</span><span class="sxs-lookup"><span data-stu-id="10359-257">0</span></span></td>
<td><span data-ttu-id="10359-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="10359-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="10359-259">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-260">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="10359-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="10359-261">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-262">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-262">Cost object</span></span></th>
<th><span data-ttu-id="10359-263">Формула</span><span class="sxs-lookup"><span data-stu-id="10359-263">Formula</span></span></th>
<th><span data-ttu-id="10359-264">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-264">Magnitude</span></span></th>
<th><span data-ttu-id="10359-265">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-265">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-266">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-267">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-267">CC001</span></span></td>
<td><span data-ttu-id="10359-268">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-268">HR</span></span></td>
<td><span data-ttu-id="10359-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="10359-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="10359-270">1</span><span class="sxs-lookup"><span data-stu-id="10359-270">1</span></span></td>
<td><span data-ttu-id="10359-271">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="10359-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="10359-272">500.00</span><span class="sxs-lookup"><span data-stu-id="10359-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-273">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-273">CC002</span></span></td>
<td><span data-ttu-id="10359-274">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-274">Finance</span></span></td>
<td><span data-ttu-id="10359-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="10359-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="10359-276">1</span><span class="sxs-lookup"><span data-stu-id="10359-276">1</span></span></td>
<td><span data-ttu-id="10359-277">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="10359-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="10359-278">500.00</span><span class="sxs-lookup"><span data-stu-id="10359-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-279">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-279">CC003</span></span></td>
<td><span data-ttu-id="10359-280">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-280">Assembly</span></span></td>
<td><span data-ttu-id="10359-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="10359-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="10359-282">0</span><span class="sxs-lookup"><span data-stu-id="10359-282">0</span></span></td>
<td><span data-ttu-id="10359-283">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="10359-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="10359-284">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="10359-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-286">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-286">Journal</span></span></th>
<th><span data-ttu-id="10359-287">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="10359-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10359-288">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="10359-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10359-289">Версия</span><span class="sxs-lookup"><span data-stu-id="10359-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-290">00002</span><span class="sxs-lookup"><span data-stu-id="10359-290">00002</span></span></td>
<td><span data-ttu-id="10359-291">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="10359-292">Финансовый</span><span class="sxs-lookup"><span data-stu-id="10359-292">Fiscal</span></span></td>
<td><span data-ttu-id="10359-293">2017</span><span class="sxs-lookup"><span data-stu-id="10359-293">2017</span></span></td>
<td><span data-ttu-id="10359-294">Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-294">Period 1</span></span></td>
<td><span data-ttu-id="10359-295">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="10359-296">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="10359-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-297">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10359-298">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-299">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-299">Cost element</span></span></th>
<th><span data-ttu-id="10359-300">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-300">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-301">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-302">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-303">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-303">CC099</span></span></td>
<td><span data-ttu-id="10359-304">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-304">Default cost center</span></span></td>
<td><span data-ttu-id="10359-305">10001</span><span class="sxs-lookup"><span data-stu-id="10359-305">10001</span></span></td>
<td><span data-ttu-id="10359-306">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-306">Electricity</span></span></td>
<td><span data-ttu-id="10359-307">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-307">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="10359-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-309">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-310">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-310">CC099</span></span></td>
<td><span data-ttu-id="10359-311">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-311">Default cost center</span></span></td>
<td><span data-ttu-id="10359-312">10001</span><span class="sxs-lookup"><span data-stu-id="10359-312">10001</span></span></td>
<td><span data-ttu-id="10359-313">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-313">Electricity</span></span></td>
<td><span data-ttu-id="10359-314">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-314">Variable cost</span></span></td>
<td><span data-ttu-id="10359-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="10359-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10359-316">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="10359-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-317">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-318">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-318">Cost element</span></span></th>
<th><span data-ttu-id="10359-319">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-319">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-320">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-320">Amount</span></span></th>
<th><span data-ttu-id="10359-321">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-322">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-322">CC099</span></span></td>
<td><span data-ttu-id="10359-323">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-323">Default cost center</span></span></td>
<td><span data-ttu-id="10359-324">10001</span><span class="sxs-lookup"><span data-stu-id="10359-324">10001</span></span></td>
<td><span data-ttu-id="10359-325">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-325">Electricity</span></span></td>
<td><span data-ttu-id="10359-326">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-326">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="10359-327">-1,000.00</span></span></td>
<td><span data-ttu-id="10359-328">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-329">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-329">CC001</span></span></td>
<td><span data-ttu-id="10359-330">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-330">HR</span></span></td>
<td><span data-ttu-id="10359-331">10001</span><span class="sxs-lookup"><span data-stu-id="10359-331">10001</span></span></td>
<td><span data-ttu-id="10359-332">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-332">Electricity</span></span></td>
<td><span data-ttu-id="10359-333">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-333">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-334">500.00</span><span class="sxs-lookup"><span data-stu-id="10359-334">500.00</span></span></td>
<td><span data-ttu-id="10359-335">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-336">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-336">CC002</span></span></td>
<td><span data-ttu-id="10359-337">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-337">Finance</span></span></td>
<td><span data-ttu-id="10359-338">10001</span><span class="sxs-lookup"><span data-stu-id="10359-338">10001</span></span></td>
<td><span data-ttu-id="10359-339">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-339">Electricity</span></span></td>
<td><span data-ttu-id="10359-340">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-340">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-341">500.00</span><span class="sxs-lookup"><span data-stu-id="10359-341">500.00</span></span></td>
<td><span data-ttu-id="10359-342">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-343">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-343">CC099</span></span></td>
<td><span data-ttu-id="10359-344">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10359-344">Default cost center</span></span></td>
<td><span data-ttu-id="10359-345">10001</span><span class="sxs-lookup"><span data-stu-id="10359-345">10001</span></span></td>
<td><span data-ttu-id="10359-346">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-346">Electricity</span></span></td>
<td><span data-ttu-id="10359-347">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-347">Variable cost</span></span></td>
<td><span data-ttu-id="10359-348">-9000,00</span><span class="sxs-lookup"><span data-stu-id="10359-348">-9,000.00</span></span></td>
<td><span data-ttu-id="10359-349">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-350">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-350">CC001</span></span></td>
<td><span data-ttu-id="10359-351">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-351">HR</span></span></td>
<td><span data-ttu-id="10359-352">10001</span><span class="sxs-lookup"><span data-stu-id="10359-352">10001</span></span></td>
<td><span data-ttu-id="10359-353">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-353">Electricity</span></span></td>
<td><span data-ttu-id="10359-354">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-354">Variable cost</span></span></td>
<td><span data-ttu-id="10359-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="10359-355">1,285.71</span></span></td>
<td><span data-ttu-id="10359-356">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-357">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-357">CC002</span></span></td>
<td><span data-ttu-id="10359-358">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-358">Finance</span></span></td>
<td><span data-ttu-id="10359-359">10001</span><span class="sxs-lookup"><span data-stu-id="10359-359">10001</span></span></td>
<td><span data-ttu-id="10359-360">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-360">Electricity</span></span></td>
<td><span data-ttu-id="10359-361">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-361">Variable cost</span></span></td>
<td><span data-ttu-id="10359-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="10359-362">7,714.29</span></span></td>
<td><span data-ttu-id="10359-363">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-364">Подробные сведения о распределении затрат и базах распределения затрат см. в разделе "Политика распределения затрат и базы распределения".</span><span class="sxs-lookup"><span data-stu-id="10359-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="10359-365">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="10359-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="10359-366">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="10359-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="10359-367">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="10359-368">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="10359-369">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="10359-369">Define the overhead rate</span></span>

<span data-ttu-id="10359-370">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="10359-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="10359-371">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="10359-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-372">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-372">Cost object</span></span></th>
<th><span data-ttu-id="10359-373">Часы</span><span class="sxs-lookup"><span data-stu-id="10359-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-374">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-374">Proj 1</span></span></td>
<td><span data-ttu-id="10359-375">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-375">Project 1</span></span></td>
<td><span data-ttu-id="10359-376">3</span><span class="sxs-lookup"><span data-stu-id="10359-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-377">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-377">Proj 2</span></span></td>
<td><span data-ttu-id="10359-378">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-378">Project 2</span></span></td>
<td><span data-ttu-id="10359-379">1</span><span class="sxs-lookup"><span data-stu-id="10359-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-380">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-381">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-381">Cost object</span></span></th>
<th><span data-ttu-id="10359-382">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-382">Cost element</span></span></th>
<th><span data-ttu-id="10359-383">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-383">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-384">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="10359-384">Units</span></span></th>
<th><span data-ttu-id="10359-385">По норме</span><span class="sxs-lookup"><span data-stu-id="10359-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-386">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-386">CC001</span></span></td>
<td><span data-ttu-id="10359-387">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-387">HR</span></span></td>
<td><span data-ttu-id="10359-388">10001</span><span class="sxs-lookup"><span data-stu-id="10359-388">10001</span></span></td>
<td><span data-ttu-id="10359-389">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-389">Variable cost</span></span></td>
<td><span data-ttu-id="10359-390">1</span><span class="sxs-lookup"><span data-stu-id="10359-390">1</span></span></td>
<td><span data-ttu-id="10359-391">10</span><span class="sxs-lookup"><span data-stu-id="10359-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-392">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-393">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-393">Cost object</span></span></th>
<th><span data-ttu-id="10359-394">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-394">Magnitude</span></span></th>
<th><span data-ttu-id="10359-395">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-395">Cost element</span></span></th>
<th><span data-ttu-id="10359-396">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-396">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-397">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-398">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-398">Proj 1</span></span></td>
<td><span data-ttu-id="10359-399">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-399">Project 1</span></span></td>
<td><span data-ttu-id="10359-400">3</span><span class="sxs-lookup"><span data-stu-id="10359-400">3</span></span></td>
<td><span data-ttu-id="10359-401">10001</span><span class="sxs-lookup"><span data-stu-id="10359-401">10001</span></span></td>
<td><span data-ttu-id="10359-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="10359-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="10359-403">30.00</span><span class="sxs-lookup"><span data-stu-id="10359-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-404">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-404">Proj 2</span></span></td>
<td><span data-ttu-id="10359-405">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-405">Project 2</span></span></td>
<td><span data-ttu-id="10359-406">1</span><span class="sxs-lookup"><span data-stu-id="10359-406">1</span></span></td>
<td><span data-ttu-id="10359-407">10001</span><span class="sxs-lookup"><span data-stu-id="10359-407">10001</span></span></td>
<td><span data-ttu-id="10359-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="10359-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="10359-409">10,00</span><span class="sxs-lookup"><span data-stu-id="10359-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="10359-410">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-411">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-411">Journal</span></span></th>
<th><span data-ttu-id="10359-412">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="10359-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10359-413">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="10359-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10359-414">Версия</span><span class="sxs-lookup"><span data-stu-id="10359-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-415">00003</span><span class="sxs-lookup"><span data-stu-id="10359-415">00003</span></span></td>
<td><span data-ttu-id="10359-416">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="10359-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="10359-417">Финансовый</span><span class="sxs-lookup"><span data-stu-id="10359-417">Fiscal</span></span></td>
<td><span data-ttu-id="10359-418">2017</span><span class="sxs-lookup"><span data-stu-id="10359-418">2017</span></span></td>
<td><span data-ttu-id="10359-419">Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-419">Period 1</span></span></td>
<td><span data-ttu-id="10359-420">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="10359-421">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="10359-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-422">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10359-423">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-423">Cost object</span></span></th>
<th><span data-ttu-id="10359-424">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-425">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-426">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-426">Proj 1</span></span></td>
<td><span data-ttu-id="10359-427">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="10359-428">3,00</span><span class="sxs-lookup"><span data-stu-id="10359-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-429">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-430">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-430">Proj 2</span></span></td>
<td><span data-ttu-id="10359-431">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="10359-432">1.00</span><span class="sxs-lookup"><span data-stu-id="10359-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10359-433">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="10359-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-434">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-435">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-435">Cost element</span></span></th>
<th><span data-ttu-id="10359-436">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-436">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-437">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-437">Amount</span></span></th>
<th><span data-ttu-id="10359-438">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="10359-439">CC0001</span></span></td>
<td><span data-ttu-id="10359-440">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-440">HR</span></span></td>
<td><span data-ttu-id="10359-441">10001</span><span class="sxs-lookup"><span data-stu-id="10359-441">10001</span></span></td>
<td><span data-ttu-id="10359-442">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-442">Electricity</span></span></td>
<td><span data-ttu-id="10359-443">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-443">Variable cost</span></span></td>
<td><span data-ttu-id="10359-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="10359-444">-30.00</span></span></td>
<td><span data-ttu-id="10359-445">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-446">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-446">Proj 1</span></span></td>
<td><span data-ttu-id="10359-447">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="10359-448">10001</span><span class="sxs-lookup"><span data-stu-id="10359-448">10001</span></span></td>
<td><span data-ttu-id="10359-449">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-449">Electricity</span></span></td>
<td><span data-ttu-id="10359-450">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-450">Variable cost</span></span></td>
<td><span data-ttu-id="10359-451">30.00</span><span class="sxs-lookup"><span data-stu-id="10359-451">30.00</span></span></td>
<td><span data-ttu-id="10359-452">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-453">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-453">CC001</span></span></td>
<td><span data-ttu-id="10359-454">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-454">HR</span></span></td>
<td><span data-ttu-id="10359-455">10001</span><span class="sxs-lookup"><span data-stu-id="10359-455">10001</span></span></td>
<td><span data-ttu-id="10359-456">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-456">Electricity</span></span></td>
<td><span data-ttu-id="10359-457">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-457">Variable cost</span></span></td>
<td><span data-ttu-id="10359-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="10359-458">-10.00</span></span></td>
<td><span data-ttu-id="10359-459">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-460">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-460">Proj 2</span></span></td>
<td><span data-ttu-id="10359-461">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="10359-462">10001</span><span class="sxs-lookup"><span data-stu-id="10359-462">10001</span></span></td>
<td><span data-ttu-id="10359-463">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-463">Electricity</span></span></td>
<td><span data-ttu-id="10359-464">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-464">Variable cost</span></span></td>
<td><span data-ttu-id="10359-465">10,00</span><span class="sxs-lookup"><span data-stu-id="10359-465">10.00</span></span></td>
<td><span data-ttu-id="10359-466">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-467">Подробные сведения о политике ставки накладных расходов см. в разделе "Политика ставки накладных расходов и базы распределения".</span><span class="sxs-lookup"><span data-stu-id="10359-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="10359-468">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="10359-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="10359-469">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="10359-470">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="10359-471">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="10359-472">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="10359-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="10359-473">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="10359-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="10359-474">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="10359-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="10359-475">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="10359-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="10359-476">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="10359-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="10359-477">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="10359-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="10359-478">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-478">Define the cost allocation</span></span>

<span data-ttu-id="10359-479">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="10359-480">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="10359-481">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="10359-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-482">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-482">Cost object</span></span></th>
<th><span data-ttu-id="10359-483">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="10359-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-484">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-484">CC002</span></span></td>
<td><span data-ttu-id="10359-485">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-485">Finance</span></span></td>
<td><span data-ttu-id="10359-486">35</span><span class="sxs-lookup"><span data-stu-id="10359-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-487">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-487">CC003</span></span></td>
<td><span data-ttu-id="10359-488">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-488">Assembly</span></span></td>
<td><span data-ttu-id="10359-489">55</span><span class="sxs-lookup"><span data-stu-id="10359-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-490">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-490">CC004</span></span></td>
<td><span data-ttu-id="10359-491">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-491">Packaging</span></span></td>
<td><span data-ttu-id="10359-492">10</span><span class="sxs-lookup"><span data-stu-id="10359-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-493">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="10359-494">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="10359-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-495">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-495">Cost object</span></span></th>
<th><span data-ttu-id="10359-496">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="10359-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-497">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-497">CC003</span></span></td>
<td><span data-ttu-id="10359-498">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-498">Assembly</span></span></td>
<td><span data-ttu-id="10359-499">65</span><span class="sxs-lookup"><span data-stu-id="10359-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-500">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-500">CC004</span></span></td>
<td><span data-ttu-id="10359-501">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-501">Packaging</span></span></td>
<td><span data-ttu-id="10359-502">35</span><span class="sxs-lookup"><span data-stu-id="10359-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-503">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="10359-504">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="10359-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-505">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-505">Cost object</span></span></th>
<th><span data-ttu-id="10359-506">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="10359-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-507">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-507">Prod 1</span></span></td>
<td><span data-ttu-id="10359-508">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-508">Product 1</span></span></td>
<td><span data-ttu-id="10359-509">60</span><span class="sxs-lookup"><span data-stu-id="10359-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-510">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-510">Prod 2</span></span></td>
<td><span data-ttu-id="10359-511">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-511">Product 2</span></span></td>
<td><span data-ttu-id="10359-512">20</span><span class="sxs-lookup"><span data-stu-id="10359-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-513">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="10359-514">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="10359-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-515">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-515">Cost object</span></span></th>
<th><span data-ttu-id="10359-516">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="10359-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-517">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-517">Prod 1</span></span></td>
<td><span data-ttu-id="10359-518">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-518">Product 1</span></span></td>
<td><span data-ttu-id="10359-519">80</span><span class="sxs-lookup"><span data-stu-id="10359-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-520">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-520">Prod 2</span></span></td>
<td><span data-ttu-id="10359-521">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-521">Product 2</span></span></td>
<td><span data-ttu-id="10359-522">15</span><span class="sxs-lookup"><span data-stu-id="10359-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-523">**Примечание.** В Finance and Operations статистические меры, такие как время производства, которое использует продукт, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="10359-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="10359-524">Более подробные сведения о поставщиках статистических мер см. в разделе "Шаблоны поставщика статистической меры".</span><span class="sxs-lookup"><span data-stu-id="10359-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="10359-525">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.) В следующей таблице показан результат, когда услуги отдела кадров применяются в качестве базы распределения для общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="10359-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-526">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-526">Cost object</span></span></th>
<th><span data-ttu-id="10359-527">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-527">Magnitude</span></span></th>
<th><span data-ttu-id="10359-528">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-528">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-529">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-529">Amount</span></span></th>
<th><span data-ttu-id="10359-530">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-531">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-531">CC002</span></span></td>
<td><span data-ttu-id="10359-532">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-532">Finance</span></span></td>
<td><span data-ttu-id="10359-533">35</span><span class="sxs-lookup"><span data-stu-id="10359-533">35</span></span></td>
<td><span data-ttu-id="10359-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="10359-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="10359-535">175.00</span><span class="sxs-lookup"><span data-stu-id="10359-535">175.00</span></span></td>
<td><span data-ttu-id="10359-536">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-537">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-537">CC003</span></span></td>
<td><span data-ttu-id="10359-538">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-538">Assembly</span></span></td>
<td><span data-ttu-id="10359-539">55</span><span class="sxs-lookup"><span data-stu-id="10359-539">55</span></span></td>
<td><span data-ttu-id="10359-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="10359-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="10359-541">275.00</span><span class="sxs-lookup"><span data-stu-id="10359-541">275.00</span></span></td>
<td><span data-ttu-id="10359-542">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-543">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-543">CC004</span></span></td>
<td><span data-ttu-id="10359-544">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-544">Packaging</span></span></td>
<td><span data-ttu-id="10359-545">10</span><span class="sxs-lookup"><span data-stu-id="10359-545">10</span></span></td>
<td><span data-ttu-id="10359-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="10359-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="10359-547">50,00</span><span class="sxs-lookup"><span data-stu-id="10359-547">50.00</span></span></td>
<td><span data-ttu-id="10359-548">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-549">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-549">CC002</span></span></td>
<td><span data-ttu-id="10359-550">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-550">Finance</span></span></td>
<td><span data-ttu-id="10359-551">35</span><span class="sxs-lookup"><span data-stu-id="10359-551">35</span></span></td>
<td><span data-ttu-id="10359-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="10359-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="10359-553">436.00</span><span class="sxs-lookup"><span data-stu-id="10359-553">436.00</span></span></td>
<td><span data-ttu-id="10359-554">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-555">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-555">CC003</span></span></td>
<td><span data-ttu-id="10359-556">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-556">Assembly</span></span></td>
<td><span data-ttu-id="10359-557">55</span><span class="sxs-lookup"><span data-stu-id="10359-557">55</span></span></td>
<td><span data-ttu-id="10359-558">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="10359-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="10359-559">685.14</span><span class="sxs-lookup"><span data-stu-id="10359-559">685.14</span></span></td>
<td><span data-ttu-id="10359-560">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-561">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-561">CC004</span></span></td>
<td><span data-ttu-id="10359-562">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-562">Packaging</span></span></td>
<td><span data-ttu-id="10359-563">10</span><span class="sxs-lookup"><span data-stu-id="10359-563">10</span></span></td>
<td><span data-ttu-id="10359-564">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="10359-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="10359-565">124.57</span><span class="sxs-lookup"><span data-stu-id="10359-565">124.57</span></span></td>
<td><span data-ttu-id="10359-566">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-567">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="10359-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-568">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-568">Cost object</span></span></th>
<th><span data-ttu-id="10359-569">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-569">Magnitude</span></span></th>
<th><span data-ttu-id="10359-570">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-570">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-571">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-571">Amount</span></span></th>
<th><span data-ttu-id="10359-572">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-573">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-573">CC003</span></span></td>
<td><span data-ttu-id="10359-574">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-574">Assembly</span></span></td>
<td><span data-ttu-id="10359-575">65</span><span class="sxs-lookup"><span data-stu-id="10359-575">65</span></span></td>
<td><span data-ttu-id="10359-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="10359-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="10359-577">438.75</span><span class="sxs-lookup"><span data-stu-id="10359-577">438.75</span></span></td>
<td><span data-ttu-id="10359-578">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-579">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-579">CC004</span></span></td>
<td><span data-ttu-id="10359-580">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-580">Packaging</span></span></td>
<td><span data-ttu-id="10359-581">35</span><span class="sxs-lookup"><span data-stu-id="10359-581">35</span></span></td>
<td><span data-ttu-id="10359-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="10359-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="10359-583">236.25</span><span class="sxs-lookup"><span data-stu-id="10359-583">236.25</span></span></td>
<td><span data-ttu-id="10359-584">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-585">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-585">CC003</span></span></td>
<td><span data-ttu-id="10359-586">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-586">Assembly</span></span></td>
<td><span data-ttu-id="10359-587">65</span><span class="sxs-lookup"><span data-stu-id="10359-587">65</span></span></td>
<td><span data-ttu-id="10359-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="10359-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="10359-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="10359-589">5,297.69</span></span></td>
<td><span data-ttu-id="10359-590">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-591">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-591">CC004</span></span></td>
<td><span data-ttu-id="10359-592">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-592">Packaging</span></span></td>
<td><span data-ttu-id="10359-593">35</span><span class="sxs-lookup"><span data-stu-id="10359-593">35</span></span></td>
<td><span data-ttu-id="10359-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="10359-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="10359-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="10359-595">2,852.60</span></span></td>
<td><span data-ttu-id="10359-596">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-597">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="10359-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-598">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-598">Cost object</span></span></th>
<th><span data-ttu-id="10359-599">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-599">Magnitude</span></span></th>
<th><span data-ttu-id="10359-600">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-600">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-601">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-601">Amount</span></span></th>
<th><span data-ttu-id="10359-602">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-603">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-603">Prod 1</span></span></td>
<td><span data-ttu-id="10359-604">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-604">Product 1</span></span></td>
<td><span data-ttu-id="10359-605">60</span><span class="sxs-lookup"><span data-stu-id="10359-605">60</span></span></td>
<td><span data-ttu-id="10359-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="10359-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="10359-607">535.31</span><span class="sxs-lookup"><span data-stu-id="10359-607">535.31</span></span></td>
<td><span data-ttu-id="10359-608">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-609">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-609">Prod 2</span></span></td>
<td><span data-ttu-id="10359-610">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-610">Product 2</span></span></td>
<td><span data-ttu-id="10359-611">20</span><span class="sxs-lookup"><span data-stu-id="10359-611">20</span></span></td>
<td><span data-ttu-id="10359-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="10359-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="10359-613">178.44</span><span class="sxs-lookup"><span data-stu-id="10359-613">178.44</span></span></td>
<td><span data-ttu-id="10359-614">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-615">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-615">Prod 1</span></span></td>
<td><span data-ttu-id="10359-616">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-616">Product 1</span></span></td>
<td><span data-ttu-id="10359-617">60</span><span class="sxs-lookup"><span data-stu-id="10359-617">60</span></span></td>
<td><span data-ttu-id="10359-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="10359-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="10359-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="10359-619">4,487.12</span></span></td>
<td><span data-ttu-id="10359-620">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-621">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-621">Prod 2</span></span></td>
<td><span data-ttu-id="10359-622">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-622">Product 2</span></span></td>
<td><span data-ttu-id="10359-623">20</span><span class="sxs-lookup"><span data-stu-id="10359-623">20</span></span></td>
<td><span data-ttu-id="10359-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="10359-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="10359-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="10359-625">1,495.71</span></span></td>
<td><span data-ttu-id="10359-626">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10359-627">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="10359-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-628">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-628">Cost object</span></span></th>
<th><span data-ttu-id="10359-629">Величина</span><span class="sxs-lookup"><span data-stu-id="10359-629">Magnitude</span></span></th>
<th><span data-ttu-id="10359-630">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="10359-630">Allocation factor</span></span></th>
<th><span data-ttu-id="10359-631">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-631">Amount</span></span></th>
<th><span data-ttu-id="10359-632">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-633">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-633">Prod 1</span></span></td>
<td><span data-ttu-id="10359-634">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-634">Product 1</span></span></td>
<td><span data-ttu-id="10359-635">80</span><span class="sxs-lookup"><span data-stu-id="10359-635">80</span></span></td>
<td><span data-ttu-id="10359-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="10359-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="10359-637">241.05</span><span class="sxs-lookup"><span data-stu-id="10359-637">241.05</span></span></td>
<td><span data-ttu-id="10359-638">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-639">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-639">Prod 2</span></span></td>
<td><span data-ttu-id="10359-640">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-640">Product 2</span></span></td>
<td><span data-ttu-id="10359-641">15</span><span class="sxs-lookup"><span data-stu-id="10359-641">15</span></span></td>
<td><span data-ttu-id="10359-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="10359-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="10359-643">45.20</span><span class="sxs-lookup"><span data-stu-id="10359-643">45.20</span></span></td>
<td><span data-ttu-id="10359-644">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-645">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-645">Prod 1</span></span></td>
<td><span data-ttu-id="10359-646">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-646">Product 1</span></span></td>
<td><span data-ttu-id="10359-647">80</span><span class="sxs-lookup"><span data-stu-id="10359-647">80</span></span></td>
<td><span data-ttu-id="10359-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="10359-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="10359-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="10359-649">2,507.09</span></span></td>
<td><span data-ttu-id="10359-650">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-651">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-651">Prod 2</span></span></td>
<td><span data-ttu-id="10359-652">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-652">Product 2</span></span></td>
<td><span data-ttu-id="10359-653">15</span><span class="sxs-lookup"><span data-stu-id="10359-653">15</span></span></td>
<td><span data-ttu-id="10359-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="10359-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="10359-655">470.08</span><span class="sxs-lookup"><span data-stu-id="10359-655">470.08</span></span></td>
<td><span data-ttu-id="10359-656">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="10359-657">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="10359-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-658">Журнал</span><span class="sxs-lookup"><span data-stu-id="10359-658">Journal</span></span></th>
<th><span data-ttu-id="10359-659">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="10359-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10359-660">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="10359-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10359-661">Версия</span><span class="sxs-lookup"><span data-stu-id="10359-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-662">00004</span><span class="sxs-lookup"><span data-stu-id="10359-662">00004</span></span></td>
<td><span data-ttu-id="10359-663">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="10359-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="10359-664">Финансовый</span><span class="sxs-lookup"><span data-stu-id="10359-664">Fiscal</span></span></td>
<td><span data-ttu-id="10359-665">2017</span><span class="sxs-lookup"><span data-stu-id="10359-665">2017</span></span></td>
<td><span data-ttu-id="10359-666">Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-666">Period 1</span></span></td>
<td><span data-ttu-id="10359-667">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="10359-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="10359-668">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="10359-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10359-669">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10359-670">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-671">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-671">Cost element</span></span></th>
<th><span data-ttu-id="10359-672">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-672">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-673">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-674">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-675">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-675">CC001</span></span></td>
<td><span data-ttu-id="10359-676">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-676">HR</span></span></td>
<td><span data-ttu-id="10359-677">10001</span><span class="sxs-lookup"><span data-stu-id="10359-677">10001</span></span></td>
<td><span data-ttu-id="10359-678">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-678">Electricity</span></span></td>
<td><span data-ttu-id="10359-679">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-679">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-680">500.00</span><span class="sxs-lookup"><span data-stu-id="10359-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-681">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-682">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-682">CC001</span></span></td>
<td><span data-ttu-id="10359-683">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-683">HR</span></span></td>
<td><span data-ttu-id="10359-684">10001</span><span class="sxs-lookup"><span data-stu-id="10359-684">10001</span></span></td>
<td><span data-ttu-id="10359-685">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-685">Electricity</span></span></td>
<td><span data-ttu-id="10359-686">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-686">Variable cost</span></span></td>
<td><span data-ttu-id="10359-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="10359-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-688">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-689">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-689">CC002</span></span></td>
<td><span data-ttu-id="10359-690">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-690">Finance</span></span></td>
<td><span data-ttu-id="10359-691">10001</span><span class="sxs-lookup"><span data-stu-id="10359-691">10001</span></span></td>
<td><span data-ttu-id="10359-692">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-692">Electricity</span></span></td>
<td><span data-ttu-id="10359-693">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-693">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-694">675.00</span><span class="sxs-lookup"><span data-stu-id="10359-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-695">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-696">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-696">CC002</span></span></td>
<td><span data-ttu-id="10359-697">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-697">Finance</span></span></td>
<td><span data-ttu-id="10359-698">10001</span><span class="sxs-lookup"><span data-stu-id="10359-698">10001</span></span></td>
<td><span data-ttu-id="10359-699">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-699">Electricity</span></span></td>
<td><span data-ttu-id="10359-700">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-700">Variable cost</span></span></td>
<td><span data-ttu-id="10359-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="10359-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-702">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-703">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-703">CC003</span></span></td>
<td><span data-ttu-id="10359-704">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-704">Assembly</span></span></td>
<td><span data-ttu-id="10359-705">10001</span><span class="sxs-lookup"><span data-stu-id="10359-705">10001</span></span></td>
<td><span data-ttu-id="10359-706">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-706">Electricity</span></span></td>
<td><span data-ttu-id="10359-707">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-707">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-708">713.75</span><span class="sxs-lookup"><span data-stu-id="10359-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-709">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-710">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-710">CC003</span></span></td>
<td><span data-ttu-id="10359-711">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-711">Assembly</span></span></td>
<td><span data-ttu-id="10359-712">10001</span><span class="sxs-lookup"><span data-stu-id="10359-712">10001</span></span></td>
<td><span data-ttu-id="10359-713">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-713">Electricity</span></span></td>
<td><span data-ttu-id="10359-714">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-714">Variable cost</span></span></td>
<td><span data-ttu-id="10359-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="10359-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-716">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-717">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-717">CC003</span></span></td>
<td><span data-ttu-id="10359-718">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-718">Packaging</span></span></td>
<td><span data-ttu-id="10359-719">10001</span><span class="sxs-lookup"><span data-stu-id="10359-719">10001</span></span></td>
<td><span data-ttu-id="10359-720">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-720">Electricity</span></span></td>
<td><span data-ttu-id="10359-721">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-721">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-722">286.25</span><span class="sxs-lookup"><span data-stu-id="10359-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-723">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-724">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-724">CC003</span></span></td>
<td><span data-ttu-id="10359-725">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-725">Packaging</span></span></td>
<td><span data-ttu-id="10359-726">10001</span><span class="sxs-lookup"><span data-stu-id="10359-726">10001</span></span></td>
<td><span data-ttu-id="10359-727">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-727">Electricity</span></span></td>
<td><span data-ttu-id="10359-728">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-728">Variable cost</span></span></td>
<td><span data-ttu-id="10359-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="10359-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-730">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-731">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-731">Prod 1</span></span></td>
<td><span data-ttu-id="10359-732">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-732">Product 1</span></span></td>
<td><span data-ttu-id="10359-733">10001</span><span class="sxs-lookup"><span data-stu-id="10359-733">10001</span></span></td>
<td><span data-ttu-id="10359-734">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-734">Electricity</span></span></td>
<td><span data-ttu-id="10359-735">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-735">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-736">776.36</span><span class="sxs-lookup"><span data-stu-id="10359-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-737">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-738">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-738">Prod 1</span></span></td>
<td><span data-ttu-id="10359-739">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-739">Product 1</span></span></td>
<td><span data-ttu-id="10359-740">10001</span><span class="sxs-lookup"><span data-stu-id="10359-740">10001</span></span></td>
<td><span data-ttu-id="10359-741">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-741">Electricity</span></span></td>
<td><span data-ttu-id="10359-742">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-742">Variable cost</span></span></td>
<td><span data-ttu-id="10359-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="10359-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-744">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-745">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-745">Prod 2</span></span></td>
<td><span data-ttu-id="10359-746">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-746">Product 1</span></span></td>
<td><span data-ttu-id="10359-747">10001</span><span class="sxs-lookup"><span data-stu-id="10359-747">10001</span></span></td>
<td><span data-ttu-id="10359-748">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-748">Electricity</span></span></td>
<td><span data-ttu-id="10359-749">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-749">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-750">223.64</span><span class="sxs-lookup"><span data-stu-id="10359-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-751">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="10359-752">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-752">Prod 2</span></span></td>
<td><span data-ttu-id="10359-753">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-753">Product 1</span></span></td>
<td><span data-ttu-id="10359-754">10001</span><span class="sxs-lookup"><span data-stu-id="10359-754">10001</span></span></td>
<td><span data-ttu-id="10359-755">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-755">Electricity</span></span></td>
<td><span data-ttu-id="10359-756">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-756">Variable cost</span></span></td>
<td><span data-ttu-id="10359-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="10359-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10359-758">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="10359-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10359-759">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10359-760">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-760">Cost element</span></span></th>
<th><span data-ttu-id="10359-761">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="10359-761">Cost behavior</span></span></th>
<th><span data-ttu-id="10359-762">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="10359-762">Amount</span></span></th>
<th><span data-ttu-id="10359-763">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="10359-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10359-764">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-764">CC001</span></span></td>
<td><span data-ttu-id="10359-765">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-765">HR</span></span></td>
<td><span data-ttu-id="10359-766">10001</span><span class="sxs-lookup"><span data-stu-id="10359-766">10001</span></span></td>
<td><span data-ttu-id="10359-767">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-767">Electricity</span></span></td>
<td><span data-ttu-id="10359-768">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-768">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="10359-769">-500.00</span></span></td>
<td><span data-ttu-id="10359-770">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-771">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-771">CC002</span></span></td>
<td><span data-ttu-id="10359-772">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-772">Finance</span></span></td>
<td><span data-ttu-id="10359-773">10001</span><span class="sxs-lookup"><span data-stu-id="10359-773">10001</span></span></td>
<td><span data-ttu-id="10359-774">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-774">Electricity</span></span></td>
<td><span data-ttu-id="10359-775">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-775">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-776">175.00</span><span class="sxs-lookup"><span data-stu-id="10359-776">175.00</span></span></td>
<td><span data-ttu-id="10359-777">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-778">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-778">CC003</span></span></td>
<td><span data-ttu-id="10359-779">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-779">Assembly</span></span></td>
<td><span data-ttu-id="10359-780">10001</span><span class="sxs-lookup"><span data-stu-id="10359-780">10001</span></span></td>
<td><span data-ttu-id="10359-781">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-781">Electricity</span></span></td>
<td><span data-ttu-id="10359-782">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-782">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-783">275.00</span><span class="sxs-lookup"><span data-stu-id="10359-783">275.00</span></span></td>
<td><span data-ttu-id="10359-784">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-785">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-785">CC004</span></span></td>
<td><span data-ttu-id="10359-786">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-786">Packaging</span></span></td>
<td><span data-ttu-id="10359-787">10001</span><span class="sxs-lookup"><span data-stu-id="10359-787">10001</span></span></td>
<td><span data-ttu-id="10359-788">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-788">Electricity</span></span></td>
<td><span data-ttu-id="10359-789">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-789">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-790">50,00</span><span class="sxs-lookup"><span data-stu-id="10359-790">50,00</span></span></td>
<td><span data-ttu-id="10359-791">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-792">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-792">CC001</span></span></td>
<td><span data-ttu-id="10359-793">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="10359-793">HR</span></span></td>
<td><span data-ttu-id="10359-794">10001</span><span class="sxs-lookup"><span data-stu-id="10359-794">10001</span></span></td>
<td><span data-ttu-id="10359-795">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-795">Electricity</span></span></td>
<td><span data-ttu-id="10359-796">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-796">Variable cost</span></span></td>
<td><span data-ttu-id="10359-797">-1245,71</span><span class="sxs-lookup"><span data-stu-id="10359-797">-1,245.71</span></span></td>
<td><span data-ttu-id="10359-798">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-799">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-799">CC002</span></span></td>
<td><span data-ttu-id="10359-800">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-800">Finance</span></span></td>
<td><span data-ttu-id="10359-801">10001</span><span class="sxs-lookup"><span data-stu-id="10359-801">10001</span></span></td>
<td><span data-ttu-id="10359-802">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-802">Electricity</span></span></td>
<td><span data-ttu-id="10359-803">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-803">Variable cost</span></span></td>
<td><span data-ttu-id="10359-804">436.00</span><span class="sxs-lookup"><span data-stu-id="10359-804">436.00</span></span></td>
<td><span data-ttu-id="10359-805">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-806">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-806">CC003</span></span></td>
<td><span data-ttu-id="10359-807">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-807">Assembly</span></span></td>
<td><span data-ttu-id="10359-808">10001</span><span class="sxs-lookup"><span data-stu-id="10359-808">10001</span></span></td>
<td><span data-ttu-id="10359-809">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-809">Electricity</span></span></td>
<td><span data-ttu-id="10359-810">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-810">Variable cost</span></span></td>
<td><span data-ttu-id="10359-811">685.14</span><span class="sxs-lookup"><span data-stu-id="10359-811">685.14</span></span></td>
<td><span data-ttu-id="10359-812">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-813">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-813">CC004</span></span></td>
<td><span data-ttu-id="10359-814">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-814">Packaging</span></span></td>
<td><span data-ttu-id="10359-815">10001</span><span class="sxs-lookup"><span data-stu-id="10359-815">10001</span></span></td>
<td><span data-ttu-id="10359-816">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-816">Electricity</span></span></td>
<td><span data-ttu-id="10359-817">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-817">Variable cost</span></span></td>
<td><span data-ttu-id="10359-818">124.57</span><span class="sxs-lookup"><span data-stu-id="10359-818">124.57</span></span></td>
<td><span data-ttu-id="10359-819">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-820">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-820">CC002</span></span></td>
<td><span data-ttu-id="10359-821">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-821">Finance</span></span></td>
<td><span data-ttu-id="10359-822">10001</span><span class="sxs-lookup"><span data-stu-id="10359-822">10001</span></span></td>
<td><span data-ttu-id="10359-823">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-823">Electricity</span></span></td>
<td><span data-ttu-id="10359-824">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-824">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="10359-825">-675.00</span></span></td>
<td><span data-ttu-id="10359-826">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-827">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-827">CC003</span></span></td>
<td><span data-ttu-id="10359-828">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-828">Assembly</span></span></td>
<td><span data-ttu-id="10359-829">10001</span><span class="sxs-lookup"><span data-stu-id="10359-829">10001</span></span></td>
<td><span data-ttu-id="10359-830">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-830">Electricity</span></span></td>
<td><span data-ttu-id="10359-831">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-831">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-832">438.75</span><span class="sxs-lookup"><span data-stu-id="10359-832">438.75</span></span></td>
<td><span data-ttu-id="10359-833">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-834">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-834">CC004</span></span></td>
<td><span data-ttu-id="10359-835">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-835">Packaging</span></span></td>
<td><span data-ttu-id="10359-836">10001</span><span class="sxs-lookup"><span data-stu-id="10359-836">10001</span></span></td>
<td><span data-ttu-id="10359-837">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-837">Electricity</span></span></td>
<td><span data-ttu-id="10359-838">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-838">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-839">236.25</span><span class="sxs-lookup"><span data-stu-id="10359-839">236.25</span></span></td>
<td><span data-ttu-id="10359-840">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-841">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-841">CC002</span></span></td>
<td><span data-ttu-id="10359-842">Финансы</span><span class="sxs-lookup"><span data-stu-id="10359-842">Finance</span></span></td>
<td><span data-ttu-id="10359-843">10001</span><span class="sxs-lookup"><span data-stu-id="10359-843">10001</span></span></td>
<td><span data-ttu-id="10359-844">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-844">Electricity</span></span></td>
<td><span data-ttu-id="10359-845">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-845">Variable cost</span></span></td>
<td><span data-ttu-id="10359-846">-8150,29</span><span class="sxs-lookup"><span data-stu-id="10359-846">-8,150.29</span></span></td>
<td><span data-ttu-id="10359-847">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-848">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-848">CC003</span></span></td>
<td><span data-ttu-id="10359-849">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-849">Assembly</span></span></td>
<td><span data-ttu-id="10359-850">10001</span><span class="sxs-lookup"><span data-stu-id="10359-850">10001</span></span></td>
<td><span data-ttu-id="10359-851">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-851">Electricity</span></span></td>
<td><span data-ttu-id="10359-852">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-852">Variable cost</span></span></td>
<td><span data-ttu-id="10359-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="10359-853">5,297.69</span></span></td>
<td><span data-ttu-id="10359-854">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-855">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-855">CC004</span></span></td>
<td><span data-ttu-id="10359-856">Упаковка</span><span class="sxs-lookup"><span data-stu-id="10359-856">Packaging</span></span></td>
<td><span data-ttu-id="10359-857">10001</span><span class="sxs-lookup"><span data-stu-id="10359-857">10001</span></span></td>
<td><span data-ttu-id="10359-858">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-858">Electricity</span></span></td>
<td><span data-ttu-id="10359-859">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-859">Variable cost</span></span></td>
<td><span data-ttu-id="10359-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="10359-860">2,852.60</span></span></td>
<td><span data-ttu-id="10359-861">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-862">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-862">CC003</span></span></td>
<td><span data-ttu-id="10359-863">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-863">Assembly</span></span></td>
<td><span data-ttu-id="10359-864">10001</span><span class="sxs-lookup"><span data-stu-id="10359-864">10001</span></span></td>
<td><span data-ttu-id="10359-865">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-865">Electricity</span></span></td>
<td><span data-ttu-id="10359-866">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-866">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="10359-867">-713.75</span></span></td>
<td><span data-ttu-id="10359-868">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-869">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-869">Prod 1</span></span></td>
<td><span data-ttu-id="10359-870">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-870">Product 1</span></span></td>
<td><span data-ttu-id="10359-871">10001</span><span class="sxs-lookup"><span data-stu-id="10359-871">10001</span></span></td>
<td><span data-ttu-id="10359-872">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-872">Electricity</span></span></td>
<td><span data-ttu-id="10359-873">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-873">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-874">535.31</span><span class="sxs-lookup"><span data-stu-id="10359-874">535.31</span></span></td>
<td><span data-ttu-id="10359-875">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-876">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-876">Prod 2</span></span></td>
<td><span data-ttu-id="10359-877">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-877">Product 2</span></span></td>
<td><span data-ttu-id="10359-878">10001</span><span class="sxs-lookup"><span data-stu-id="10359-878">10001</span></span></td>
<td><span data-ttu-id="10359-879">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-879">Electricity</span></span></td>
<td><span data-ttu-id="10359-880">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-880">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-881">178.44</span><span class="sxs-lookup"><span data-stu-id="10359-881">178.44</span></span></td>
<td><span data-ttu-id="10359-882">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-883">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-883">CC003</span></span></td>
<td><span data-ttu-id="10359-884">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-884">Assembly</span></span></td>
<td><span data-ttu-id="10359-885">10001</span><span class="sxs-lookup"><span data-stu-id="10359-885">10001</span></span></td>
<td><span data-ttu-id="10359-886">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-886">Electricity</span></span></td>
<td><span data-ttu-id="10359-887">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-887">Variable cost</span></span></td>
<td><span data-ttu-id="10359-888">-5982,83</span><span class="sxs-lookup"><span data-stu-id="10359-888">-5,982.83</span></span></td>
<td><span data-ttu-id="10359-889">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-890">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-890">Prod 1</span></span></td>
<td><span data-ttu-id="10359-891">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-891">Product 1</span></span></td>
<td><span data-ttu-id="10359-892">10001</span><span class="sxs-lookup"><span data-stu-id="10359-892">10001</span></span></td>
<td><span data-ttu-id="10359-893">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-893">Electricity</span></span></td>
<td><span data-ttu-id="10359-894">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-894">Variable cost</span></span></td>
<td><span data-ttu-id="10359-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="10359-895">4,487.12</span></span></td>
<td><span data-ttu-id="10359-896">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-897">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-897">Prod 2</span></span></td>
<td><span data-ttu-id="10359-898">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-898">Product 2</span></span></td>
<td><span data-ttu-id="10359-899">10001</span><span class="sxs-lookup"><span data-stu-id="10359-899">10001</span></span></td>
<td><span data-ttu-id="10359-900">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-900">Electricity</span></span></td>
<td><span data-ttu-id="10359-901">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-901">Variable cost</span></span></td>
<td><span data-ttu-id="10359-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="10359-902">1,495.71</span></span></td>
<td><span data-ttu-id="10359-903">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-904">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-904">CC003</span></span></td>
<td><span data-ttu-id="10359-905">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-905">Assembly</span></span></td>
<td><span data-ttu-id="10359-906">10001</span><span class="sxs-lookup"><span data-stu-id="10359-906">10001</span></span></td>
<td><span data-ttu-id="10359-907">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-907">Electricity</span></span></td>
<td><span data-ttu-id="10359-908">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-908">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="10359-909">-286.25</span></span></td>
<td><span data-ttu-id="10359-910">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-911">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-911">Prod 1</span></span></td>
<td><span data-ttu-id="10359-912">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-912">Product 1</span></span></td>
<td><span data-ttu-id="10359-913">10001</span><span class="sxs-lookup"><span data-stu-id="10359-913">10001</span></span></td>
<td><span data-ttu-id="10359-914">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-914">Electricity</span></span></td>
<td><span data-ttu-id="10359-915">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-915">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-916">241.05</span><span class="sxs-lookup"><span data-stu-id="10359-916">241.05</span></span></td>
<td><span data-ttu-id="10359-917">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-918">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-918">Prod 2</span></span></td>
<td><span data-ttu-id="10359-919">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-919">Product 2</span></span></td>
<td><span data-ttu-id="10359-920">10001</span><span class="sxs-lookup"><span data-stu-id="10359-920">10001</span></span></td>
<td><span data-ttu-id="10359-921">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-921">Electricity</span></span></td>
<td><span data-ttu-id="10359-922">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-922">Fixed cost</span></span></td>
<td><span data-ttu-id="10359-923">45.20</span><span class="sxs-lookup"><span data-stu-id="10359-923">45.20</span></span></td>
<td><span data-ttu-id="10359-924">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-925">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-925">CC003</span></span></td>
<td><span data-ttu-id="10359-926">Сборка</span><span class="sxs-lookup"><span data-stu-id="10359-926">Assembly</span></span></td>
<td><span data-ttu-id="10359-927">10001</span><span class="sxs-lookup"><span data-stu-id="10359-927">10001</span></span></td>
<td><span data-ttu-id="10359-928">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-928">Electricity</span></span></td>
<td><span data-ttu-id="10359-929">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-929">Variable cost</span></span></td>
<td><span data-ttu-id="10359-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="10359-930">-2,977.17</span></span></td>
<td><span data-ttu-id="10359-931">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-932">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-932">Prod 1</span></span></td>
<td><span data-ttu-id="10359-933">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="10359-933">Product 1</span></span></td>
<td><span data-ttu-id="10359-934">10001</span><span class="sxs-lookup"><span data-stu-id="10359-934">10001</span></span></td>
<td><span data-ttu-id="10359-935">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-935">Electricity</span></span></td>
<td><span data-ttu-id="10359-936">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-936">Variable cost</span></span></td>
<td><span data-ttu-id="10359-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="10359-937">2,507.09</span></span></td>
<td><span data-ttu-id="10359-938">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10359-939">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-939">Prod 2</span></span></td>
<td><span data-ttu-id="10359-940">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="10359-940">Product 2</span></span></td>
<td><span data-ttu-id="10359-941">10001</span><span class="sxs-lookup"><span data-stu-id="10359-941">10001</span></span></td>
<td><span data-ttu-id="10359-942">Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-942">Electricity</span></span></td>
<td><span data-ttu-id="10359-943">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-943">Variable cost</span></span></td>
<td><span data-ttu-id="10359-944">470.08</span><span class="sxs-lookup"><span data-stu-id="10359-944">470.08</span></span></td>
<td><span data-ttu-id="10359-945">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="10359-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="10359-946">Заключение</span><span class="sxs-lookup"><span data-stu-id="10359-946">Conclusion</span></span>
<span data-ttu-id="10359-947">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="10359-948">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="10359-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="10359-949">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="10359-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="10359-950">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="10359-951">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="10359-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="10359-952">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="10359-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="10359-953">Итоговый</span><span class="sxs-lookup"><span data-stu-id="10359-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="10359-954">CC099</span><span class="sxs-lookup"><span data-stu-id="10359-954">CC099</span></span></th>
<th><span data-ttu-id="10359-955">CC001</span><span class="sxs-lookup"><span data-stu-id="10359-955">CC001</span></span></th>
<th><span data-ttu-id="10359-956">CC002</span><span class="sxs-lookup"><span data-stu-id="10359-956">CC002</span></span></th>
<th><span data-ttu-id="10359-957">CC003</span><span class="sxs-lookup"><span data-stu-id="10359-957">CC003</span></span></th>
<th><span data-ttu-id="10359-958">CC004</span><span class="sxs-lookup"><span data-stu-id="10359-958">CC004</span></span></th>
<th><span data-ttu-id="10359-959">Проект 1</span><span class="sxs-lookup"><span data-stu-id="10359-959">Proj 1</span></span></th>
<th><span data-ttu-id="10359-960">Проект 2</span><span class="sxs-lookup"><span data-stu-id="10359-960">Proj 2</span></span></th>
<th><span data-ttu-id="10359-961">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="10359-961">Prod 1</span></span></th>
<th><span data-ttu-id="10359-962">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="10359-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="10359-963">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="10359-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="10359-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="10359-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="10359-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="10359-973">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="10359-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-974">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="10359-975">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-976">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-977">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-978">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-979">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-980">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="10359-981">776.36</span><span class="sxs-lookup"><span data-stu-id="10359-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-982">223.64</span><span class="sxs-lookup"><span data-stu-id="10359-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="10359-984">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="10359-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-985">000</span><span class="sxs-lookup"><span data-stu-id="10359-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-986">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-987">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-988">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-989">0,00</span><span class="sxs-lookup"><span data-stu-id="10359-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-990">30.00</span><span class="sxs-lookup"><span data-stu-id="10359-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-991">10,00</span><span class="sxs-lookup"><span data-stu-id="10359-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="10359-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="10359-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10359-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="10359-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="10359-995">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="10359-996">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="10359-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="10359-997">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="10359-998">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="10359-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="10359-999">Для получения дополнительных сведений см. политику свертки затрат.</span><span class="sxs-lookup"><span data-stu-id="10359-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="10359-1000">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="10359-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




