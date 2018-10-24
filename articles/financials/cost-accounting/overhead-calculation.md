---
title: "Расчет накладных расходов"
description: "В этом разделе описываются типовые процессы расчета и распределения накладных расходов."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: ru-ru
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="a51dc-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="a51dc-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a51dc-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="a51dc-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a51dc-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="a51dc-105">Term definition</span></span>
---------------

<span data-ttu-id="a51dc-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="a51dc-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a51dc-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="a51dc-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a51dc-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="a51dc-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a51dc-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="a51dc-109">Rent</span></span>
-   <span data-ttu-id="a51dc-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-110">Electricity</span></span>
-   <span data-ttu-id="a51dc-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="a51dc-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a51dc-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="a51dc-112">Overhead calculation overview</span></span>
<span data-ttu-id="a51dc-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="a51dc-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a51dc-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="a51dc-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a51dc-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="a51dc-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a51dc-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="a51dc-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a51dc-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="a51dc-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a51dc-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="a51dc-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a51dc-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="a51dc-119">Version type</span></span>
-   <span data-ttu-id="a51dc-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="a51dc-120">Date and time</span></span>
-   <span data-ttu-id="a51dc-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a51dc-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="a51dc-122">Fiscal year</span></span>
-   <span data-ttu-id="a51dc-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="a51dc-123">Fiscal period</span></span>

<span data-ttu-id="a51dc-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="a51dc-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a51dc-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="a51dc-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a51dc-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="a51dc-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a51dc-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="a51dc-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a51dc-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="a51dc-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a51dc-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="a51dc-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a51dc-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="a51dc-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a51dc-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a51dc-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a51dc-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="a51dc-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a51dc-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="a51dc-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a51dc-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a51dc-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a51dc-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="a51dc-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a51dc-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a51dc-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="a51dc-140">Main account</span></span></th>
<th><span data-ttu-id="a51dc-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="a51dc-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a51dc-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-143">CC099</span></span></td>
<td><span data-ttu-id="a51dc-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-144">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-145">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-145">10001</span></span></td>
<td><span data-ttu-id="a51dc-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-146">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a51dc-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a51dc-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a51dc-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="a51dc-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a51dc-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a51dc-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="a51dc-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a51dc-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="a51dc-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a51dc-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="a51dc-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a51dc-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="a51dc-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a51dc-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a51dc-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a51dc-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a51dc-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-160">Journal</span></span></th>
<th><span data-ttu-id="a51dc-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="a51dc-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a51dc-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="a51dc-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a51dc-163">Версия</span><span class="sxs-lookup"><span data-stu-id="a51dc-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-164">00001</span><span class="sxs-lookup"><span data-stu-id="a51dc-164">00001</span></span></td>
<td><span data-ttu-id="a51dc-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a51dc-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="a51dc-166">Fiscal</span></span></td>
<td><span data-ttu-id="a51dc-167">2017</span><span class="sxs-lookup"><span data-stu-id="a51dc-167">2017</span></span></td>
<td><span data-ttu-id="a51dc-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-168">Period 1</span></span></td>
<td><span data-ttu-id="a51dc-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a51dc-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="a51dc-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-173">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a51dc-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-177">CC099</span></span></td>
<td><span data-ttu-id="a51dc-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-178">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-179">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-179">10001</span></span></td>
<td><span data-ttu-id="a51dc-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-180">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="a51dc-181">Unclassified</span></span></td>
<td><span data-ttu-id="a51dc-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a51dc-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-185">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-187">Amount</span></span></th>
<th><span data-ttu-id="a51dc-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-189">CC099</span></span></td>
<td><span data-ttu-id="a51dc-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-190">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-191">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-191">10001</span></span></td>
<td><span data-ttu-id="a51dc-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-192">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="a51dc-193">Unclassified</span></span></td>
<td><span data-ttu-id="a51dc-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-194">10,000.00</span></span></td>
<td><span data-ttu-id="a51dc-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-196">CC099</span></span></td>
<td><span data-ttu-id="a51dc-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-197">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-198">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-198">10001</span></span></td>
<td><span data-ttu-id="a51dc-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-199">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="a51dc-200">Unclassified</span></span></td>
<td><span data-ttu-id="a51dc-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a51dc-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-203">CC099</span></span></td>
<td><span data-ttu-id="a51dc-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-204">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-205">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-205">10001</span></span></td>
<td><span data-ttu-id="a51dc-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-206">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-208">1,000.00</span></span></td>
<td><span data-ttu-id="a51dc-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-210">CC099</span></span></td>
<td><span data-ttu-id="a51dc-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-211">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-212">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-212">10001</span></span></td>
<td><span data-ttu-id="a51dc-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-213">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-214">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-215">9,000.00</span></span></td>
<td><span data-ttu-id="a51dc-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="a51dc-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a51dc-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a51dc-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a51dc-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a51dc-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-221">Define the cost distribution rule</span></span>

<span data-ttu-id="a51dc-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="a51dc-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a51dc-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="a51dc-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a51dc-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="a51dc-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a51dc-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="a51dc-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a51dc-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="a51dc-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a51dc-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-228">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="a51dc-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-230">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-230">CC001</span></span></td>
<td><span data-ttu-id="a51dc-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-231">HR</span></span></td>
<td><span data-ttu-id="a51dc-232">1000</span><span class="sxs-lookup"><span data-stu-id="a51dc-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-233">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-233">CC002</span></span></td>
<td><span data-ttu-id="a51dc-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-234">Finance</span></span></td>
<td><span data-ttu-id="a51dc-235">6,000</span><span class="sxs-lookup"><span data-stu-id="a51dc-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-236">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-236">CC003</span></span></td>
<td><span data-ttu-id="a51dc-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-237">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-238">0</span><span class="sxs-lookup"><span data-stu-id="a51dc-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-240">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-241">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-241">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-242">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-244">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-244">CC001</span></span></td>
<td><span data-ttu-id="a51dc-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-245">HR</span></span></td>
<td><span data-ttu-id="a51dc-246">1000</span><span class="sxs-lookup"><span data-stu-id="a51dc-246">1,000</span></span></td>
<td><span data-ttu-id="a51dc-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a51dc-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a51dc-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-249">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-249">CC002</span></span></td>
<td><span data-ttu-id="a51dc-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-250">Finance</span></span></td>
<td><span data-ttu-id="a51dc-251">6,000</span><span class="sxs-lookup"><span data-stu-id="a51dc-251">6,000</span></span></td>
<td><span data-ttu-id="a51dc-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a51dc-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a51dc-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-254">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-254">CC003</span></span></td>
<td><span data-ttu-id="a51dc-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-255">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-256">0</span><span class="sxs-lookup"><span data-stu-id="a51dc-256">0</span></span></td>
<td><span data-ttu-id="a51dc-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a51dc-258">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="a51dc-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a51dc-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-261">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-262">Формула</span><span class="sxs-lookup"><span data-stu-id="a51dc-262">Formula</span></span></th>
<th><span data-ttu-id="a51dc-263">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-263">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-264">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-266">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-266">CC001</span></span></td>
<td><span data-ttu-id="a51dc-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-267">HR</span></span></td>
<td><span data-ttu-id="a51dc-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a51dc-269">1</span><span class="sxs-lookup"><span data-stu-id="a51dc-269">1</span></span></td>
<td><span data-ttu-id="a51dc-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a51dc-271">500.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-272">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-272">CC002</span></span></td>
<td><span data-ttu-id="a51dc-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-273">Finance</span></span></td>
<td><span data-ttu-id="a51dc-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a51dc-275">1</span><span class="sxs-lookup"><span data-stu-id="a51dc-275">1</span></span></td>
<td><span data-ttu-id="a51dc-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a51dc-277">500.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-278">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-278">CC003</span></span></td>
<td><span data-ttu-id="a51dc-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-279">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a51dc-281">0</span><span class="sxs-lookup"><span data-stu-id="a51dc-281">0</span></span></td>
<td><span data-ttu-id="a51dc-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a51dc-283">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a51dc-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-285">Journal</span></span></th>
<th><span data-ttu-id="a51dc-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="a51dc-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a51dc-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="a51dc-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a51dc-288">Версия</span><span class="sxs-lookup"><span data-stu-id="a51dc-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-289">00002</span><span class="sxs-lookup"><span data-stu-id="a51dc-289">00002</span></span></td>
<td><span data-ttu-id="a51dc-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a51dc-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="a51dc-291">Fiscal</span></span></td>
<td><span data-ttu-id="a51dc-292">2017</span><span class="sxs-lookup"><span data-stu-id="a51dc-292">2017</span></span></td>
<td><span data-ttu-id="a51dc-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-293">Period 1</span></span></td>
<td><span data-ttu-id="a51dc-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a51dc-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="a51dc-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-298">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-299">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-302">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-302">CC099</span></span></td>
<td><span data-ttu-id="a51dc-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-303">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-304">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-304">10001</span></span></td>
<td><span data-ttu-id="a51dc-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-305">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-306">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-309">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-309">CC099</span></span></td>
<td><span data-ttu-id="a51dc-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-310">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-311">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-311">10001</span></span></td>
<td><span data-ttu-id="a51dc-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-312">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-313">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a51dc-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-317">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-318">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-319">Amount</span></span></th>
<th><span data-ttu-id="a51dc-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-321">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-321">CC099</span></span></td>
<td><span data-ttu-id="a51dc-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-322">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-323">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-323">10001</span></span></td>
<td><span data-ttu-id="a51dc-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-324">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-325">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-326">-1,000.00</span></span></td>
<td><span data-ttu-id="a51dc-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-328">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-328">CC001</span></span></td>
<td><span data-ttu-id="a51dc-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-329">HR</span></span></td>
<td><span data-ttu-id="a51dc-330">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-330">10001</span></span></td>
<td><span data-ttu-id="a51dc-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-331">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-332">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-333">500.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-333">500.00</span></span></td>
<td><span data-ttu-id="a51dc-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-335">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-335">CC002</span></span></td>
<td><span data-ttu-id="a51dc-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-336">Finance</span></span></td>
<td><span data-ttu-id="a51dc-337">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-337">10001</span></span></td>
<td><span data-ttu-id="a51dc-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-338">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-339">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-340">500.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-340">500.00</span></span></td>
<td><span data-ttu-id="a51dc-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-342">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-342">CC099</span></span></td>
<td><span data-ttu-id="a51dc-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a51dc-343">Default cost center</span></span></td>
<td><span data-ttu-id="a51dc-344">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-344">10001</span></span></td>
<td><span data-ttu-id="a51dc-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-345">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-346">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-347">-9,000.00</span></span></td>
<td><span data-ttu-id="a51dc-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-349">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-349">CC001</span></span></td>
<td><span data-ttu-id="a51dc-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-350">HR</span></span></td>
<td><span data-ttu-id="a51dc-351">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-351">10001</span></span></td>
<td><span data-ttu-id="a51dc-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-352">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-353">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a51dc-354">1,285.71</span></span></td>
<td><span data-ttu-id="a51dc-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-356">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-356">CC002</span></span></td>
<td><span data-ttu-id="a51dc-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-357">Finance</span></span></td>
<td><span data-ttu-id="a51dc-358">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-358">10001</span></span></td>
<td><span data-ttu-id="a51dc-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-359">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-360">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a51dc-361">7,714.29</span></span></td>
<td><span data-ttu-id="a51dc-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="a51dc-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a51dc-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="a51dc-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a51dc-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a51dc-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a51dc-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="a51dc-367">Define the overhead rate</span></span>

<span data-ttu-id="a51dc-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="a51dc-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a51dc-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="a51dc-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-370">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-371">Часы</span><span class="sxs-lookup"><span data-stu-id="a51dc-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-372">Proj 1</span></span></td>
<td><span data-ttu-id="a51dc-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-373">Project 1</span></span></td>
<td><span data-ttu-id="a51dc-374">3</span><span class="sxs-lookup"><span data-stu-id="a51dc-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-375">Proj 2</span></span></td>
<td><span data-ttu-id="a51dc-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-376">Project 2</span></span></td>
<td><span data-ttu-id="a51dc-377">1</span><span class="sxs-lookup"><span data-stu-id="a51dc-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-379">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-380">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-381">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="a51dc-382">Units</span></span></th>
<th><span data-ttu-id="a51dc-383">По норме</span><span class="sxs-lookup"><span data-stu-id="a51dc-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-384">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-384">CC001</span></span></td>
<td><span data-ttu-id="a51dc-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-385">HR</span></span></td>
<td><span data-ttu-id="a51dc-386">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-386">10001</span></span></td>
<td><span data-ttu-id="a51dc-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-387">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-388">1</span><span class="sxs-lookup"><span data-stu-id="a51dc-388">1</span></span></td>
<td><span data-ttu-id="a51dc-389">10</span><span class="sxs-lookup"><span data-stu-id="a51dc-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-391">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-392">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-392">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-393">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-394">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-396">Proj 1</span></span></td>
<td><span data-ttu-id="a51dc-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-397">Project 1</span></span></td>
<td><span data-ttu-id="a51dc-398">3</span><span class="sxs-lookup"><span data-stu-id="a51dc-398">3</span></span></td>
<td><span data-ttu-id="a51dc-399">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-399">10001</span></span></td>
<td><span data-ttu-id="a51dc-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a51dc-401">30.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-402">Proj 2</span></span></td>
<td><span data-ttu-id="a51dc-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-403">Project 2</span></span></td>
<td><span data-ttu-id="a51dc-404">1</span><span class="sxs-lookup"><span data-stu-id="a51dc-404">1</span></span></td>
<td><span data-ttu-id="a51dc-405">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-405">10001</span></span></td>
<td><span data-ttu-id="a51dc-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a51dc-407">10,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a51dc-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-409">Journal</span></span></th>
<th><span data-ttu-id="a51dc-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="a51dc-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a51dc-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="a51dc-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a51dc-412">Версия</span><span class="sxs-lookup"><span data-stu-id="a51dc-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-413">00003</span><span class="sxs-lookup"><span data-stu-id="a51dc-413">00003</span></span></td>
<td><span data-ttu-id="a51dc-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="a51dc-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a51dc-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="a51dc-415">Fiscal</span></span></td>
<td><span data-ttu-id="a51dc-416">2017</span><span class="sxs-lookup"><span data-stu-id="a51dc-416">2017</span></span></td>
<td><span data-ttu-id="a51dc-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-417">Period 1</span></span></td>
<td><span data-ttu-id="a51dc-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a51dc-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="a51dc-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-421">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-422">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-424">Proj 1</span></span></td>
<td><span data-ttu-id="a51dc-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a51dc-426">3,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-428">Proj 2</span></span></td>
<td><span data-ttu-id="a51dc-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a51dc-430">1.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a51dc-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-433">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-434">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-435">Amount</span></span></th>
<th><span data-ttu-id="a51dc-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="a51dc-437">CC0001</span></span></td>
<td><span data-ttu-id="a51dc-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-438">HR</span></span></td>
<td><span data-ttu-id="a51dc-439">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-439">10001</span></span></td>
<td><span data-ttu-id="a51dc-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-440">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-441">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-442">-30.00</span></span></td>
<td><span data-ttu-id="a51dc-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-444">Proj 1</span></span></td>
<td><span data-ttu-id="a51dc-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a51dc-446">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-446">10001</span></span></td>
<td><span data-ttu-id="a51dc-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-447">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-448">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-449">30.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-449">30.00</span></span></td>
<td><span data-ttu-id="a51dc-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-451">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-451">CC001</span></span></td>
<td><span data-ttu-id="a51dc-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-452">HR</span></span></td>
<td><span data-ttu-id="a51dc-453">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-453">10001</span></span></td>
<td><span data-ttu-id="a51dc-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-454">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-455">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-456">-10.00</span></span></td>
<td><span data-ttu-id="a51dc-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-458">Proj 2</span></span></td>
<td><span data-ttu-id="a51dc-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a51dc-460">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-460">10001</span></span></td>
<td><span data-ttu-id="a51dc-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-461">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-462">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-463">10.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-463">10.00</span></span></td>
<td><span data-ttu-id="a51dc-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="a51dc-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a51dc-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a51dc-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a51dc-468">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="a51dc-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="a51dc-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a51dc-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="a51dc-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a51dc-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="a51dc-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a51dc-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="a51dc-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a51dc-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="a51dc-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a51dc-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a51dc-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a51dc-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-475">Define the cost allocation</span></span>

<span data-ttu-id="a51dc-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a51dc-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a51dc-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="a51dc-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-479">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-481">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-481">CC002</span></span></td>
<td><span data-ttu-id="a51dc-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-482">Finance</span></span></td>
<td><span data-ttu-id="a51dc-483">35</span><span class="sxs-lookup"><span data-stu-id="a51dc-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-484">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-484">CC003</span></span></td>
<td><span data-ttu-id="a51dc-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-485">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-486">55</span><span class="sxs-lookup"><span data-stu-id="a51dc-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-487">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-487">CC004</span></span></td>
<td><span data-ttu-id="a51dc-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-488">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-489">10</span><span class="sxs-lookup"><span data-stu-id="a51dc-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a51dc-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="a51dc-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-492">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="a51dc-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-494">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-494">CC003</span></span></td>
<td><span data-ttu-id="a51dc-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-495">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-496">65</span><span class="sxs-lookup"><span data-stu-id="a51dc-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-497">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-497">CC004</span></span></td>
<td><span data-ttu-id="a51dc-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-498">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-499">35</span><span class="sxs-lookup"><span data-stu-id="a51dc-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a51dc-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="a51dc-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-502">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="a51dc-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-504">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-505">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-506">60</span><span class="sxs-lookup"><span data-stu-id="a51dc-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-507">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-508">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-509">20</span><span class="sxs-lookup"><span data-stu-id="a51dc-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a51dc-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="a51dc-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-512">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="a51dc-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-514">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-515">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-516">80</span><span class="sxs-lookup"><span data-stu-id="a51dc-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-517">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-518">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-519">15</span><span class="sxs-lookup"><span data-stu-id="a51dc-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a51dc-520">В Finance and Operations статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="a51dc-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a51dc-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="a51dc-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="a51dc-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="a51dc-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-523">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-524">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-524">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-525">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-526">Amount</span></span></th>
<th><span data-ttu-id="a51dc-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-528">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-528">CC002</span></span></td>
<td><span data-ttu-id="a51dc-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-529">Finance</span></span></td>
<td><span data-ttu-id="a51dc-530">35</span><span class="sxs-lookup"><span data-stu-id="a51dc-530">35</span></span></td>
<td><span data-ttu-id="a51dc-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a51dc-532">175.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-532">175.00</span></span></td>
<td><span data-ttu-id="a51dc-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-534">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-534">CC003</span></span></td>
<td><span data-ttu-id="a51dc-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-535">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-536">55</span><span class="sxs-lookup"><span data-stu-id="a51dc-536">55</span></span></td>
<td><span data-ttu-id="a51dc-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a51dc-538">275.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-538">275.00</span></span></td>
<td><span data-ttu-id="a51dc-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-540">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-540">CC004</span></span></td>
<td><span data-ttu-id="a51dc-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-541">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-542">10</span><span class="sxs-lookup"><span data-stu-id="a51dc-542">10</span></span></td>
<td><span data-ttu-id="a51dc-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a51dc-544">50,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-544">50.00</span></span></td>
<td><span data-ttu-id="a51dc-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-546">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-546">CC002</span></span></td>
<td><span data-ttu-id="a51dc-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-547">Finance</span></span></td>
<td><span data-ttu-id="a51dc-548">35</span><span class="sxs-lookup"><span data-stu-id="a51dc-548">35</span></span></td>
<td><span data-ttu-id="a51dc-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="a51dc-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a51dc-550">436.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-550">436.00</span></span></td>
<td><span data-ttu-id="a51dc-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-552">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-552">CC003</span></span></td>
<td><span data-ttu-id="a51dc-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-553">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-554">55</span><span class="sxs-lookup"><span data-stu-id="a51dc-554">55</span></span></td>
<td><span data-ttu-id="a51dc-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="a51dc-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a51dc-556">685.14</span><span class="sxs-lookup"><span data-stu-id="a51dc-556">685.14</span></span></td>
<td><span data-ttu-id="a51dc-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-558">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-558">CC004</span></span></td>
<td><span data-ttu-id="a51dc-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-559">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-560">10</span><span class="sxs-lookup"><span data-stu-id="a51dc-560">10</span></span></td>
<td><span data-ttu-id="a51dc-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="a51dc-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a51dc-562">124.57</span><span class="sxs-lookup"><span data-stu-id="a51dc-562">124.57</span></span></td>
<td><span data-ttu-id="a51dc-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="a51dc-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-565">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-566">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-566">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-567">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-568">Amount</span></span></th>
<th><span data-ttu-id="a51dc-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-570">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-570">CC003</span></span></td>
<td><span data-ttu-id="a51dc-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-571">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-572">65</span><span class="sxs-lookup"><span data-stu-id="a51dc-572">65</span></span></td>
<td><span data-ttu-id="a51dc-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a51dc-574">438.75</span><span class="sxs-lookup"><span data-stu-id="a51dc-574">438.75</span></span></td>
<td><span data-ttu-id="a51dc-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-576">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-576">CC004</span></span></td>
<td><span data-ttu-id="a51dc-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-577">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-578">35</span><span class="sxs-lookup"><span data-stu-id="a51dc-578">35</span></span></td>
<td><span data-ttu-id="a51dc-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a51dc-580">236.25</span><span class="sxs-lookup"><span data-stu-id="a51dc-580">236.25</span></span></td>
<td><span data-ttu-id="a51dc-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-582">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-582">CC003</span></span></td>
<td><span data-ttu-id="a51dc-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-583">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-584">65</span><span class="sxs-lookup"><span data-stu-id="a51dc-584">65</span></span></td>
<td><span data-ttu-id="a51dc-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a51dc-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a51dc-586">5,297.69</span></span></td>
<td><span data-ttu-id="a51dc-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-588">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-588">CC004</span></span></td>
<td><span data-ttu-id="a51dc-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-589">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-590">35</span><span class="sxs-lookup"><span data-stu-id="a51dc-590">35</span></span></td>
<td><span data-ttu-id="a51dc-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a51dc-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a51dc-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a51dc-592">2,852.60</span></span></td>
<td><span data-ttu-id="a51dc-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="a51dc-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-595">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-596">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-596">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-597">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-598">Amount</span></span></th>
<th><span data-ttu-id="a51dc-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-600">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-601">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-602">60</span><span class="sxs-lookup"><span data-stu-id="a51dc-602">60</span></span></td>
<td><span data-ttu-id="a51dc-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a51dc-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a51dc-604">535.31</span><span class="sxs-lookup"><span data-stu-id="a51dc-604">535.31</span></span></td>
<td><span data-ttu-id="a51dc-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-606">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-607">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-608">20</span><span class="sxs-lookup"><span data-stu-id="a51dc-608">20</span></span></td>
<td><span data-ttu-id="a51dc-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a51dc-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a51dc-610">178.44</span><span class="sxs-lookup"><span data-stu-id="a51dc-610">178.44</span></span></td>
<td><span data-ttu-id="a51dc-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-612">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-613">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-614">60</span><span class="sxs-lookup"><span data-stu-id="a51dc-614">60</span></span></td>
<td><span data-ttu-id="a51dc-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a51dc-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a51dc-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a51dc-616">4,487.12</span></span></td>
<td><span data-ttu-id="a51dc-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-618">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-619">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-620">20</span><span class="sxs-lookup"><span data-stu-id="a51dc-620">20</span></span></td>
<td><span data-ttu-id="a51dc-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a51dc-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a51dc-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a51dc-622">1,495.71</span></span></td>
<td><span data-ttu-id="a51dc-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a51dc-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="a51dc-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-625">Cost object</span></span></th>
<th><span data-ttu-id="a51dc-626">Величина</span><span class="sxs-lookup"><span data-stu-id="a51dc-626">Magnitude</span></span></th>
<th><span data-ttu-id="a51dc-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="a51dc-627">Allocation factor</span></span></th>
<th><span data-ttu-id="a51dc-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-628">Amount</span></span></th>
<th><span data-ttu-id="a51dc-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-630">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-631">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-632">80</span><span class="sxs-lookup"><span data-stu-id="a51dc-632">80</span></span></td>
<td><span data-ttu-id="a51dc-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a51dc-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a51dc-634">241.05</span><span class="sxs-lookup"><span data-stu-id="a51dc-634">241.05</span></span></td>
<td><span data-ttu-id="a51dc-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-636">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-637">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-638">15</span><span class="sxs-lookup"><span data-stu-id="a51dc-638">15</span></span></td>
<td><span data-ttu-id="a51dc-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a51dc-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a51dc-640">45.20</span><span class="sxs-lookup"><span data-stu-id="a51dc-640">45.20</span></span></td>
<td><span data-ttu-id="a51dc-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-642">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-643">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-644">80</span><span class="sxs-lookup"><span data-stu-id="a51dc-644">80</span></span></td>
<td><span data-ttu-id="a51dc-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a51dc-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a51dc-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a51dc-646">2,507.09</span></span></td>
<td><span data-ttu-id="a51dc-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-648">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-649">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-650">15</span><span class="sxs-lookup"><span data-stu-id="a51dc-650">15</span></span></td>
<td><span data-ttu-id="a51dc-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a51dc-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a51dc-652">470.08</span><span class="sxs-lookup"><span data-stu-id="a51dc-652">470.08</span></span></td>
<td><span data-ttu-id="a51dc-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a51dc-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="a51dc-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="a51dc-655">Journal</span></span></th>
<th><span data-ttu-id="a51dc-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="a51dc-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a51dc-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="a51dc-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a51dc-658">Версия</span><span class="sxs-lookup"><span data-stu-id="a51dc-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-659">00004</span><span class="sxs-lookup"><span data-stu-id="a51dc-659">00004</span></span></td>
<td><span data-ttu-id="a51dc-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a51dc-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="a51dc-661">Fiscal</span></span></td>
<td><span data-ttu-id="a51dc-662">2017</span><span class="sxs-lookup"><span data-stu-id="a51dc-662">2017</span></span></td>
<td><span data-ttu-id="a51dc-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-663">Period 1</span></span></td>
<td><span data-ttu-id="a51dc-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a51dc-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="a51dc-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a51dc-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-668">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-669">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-672">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-672">CC001</span></span></td>
<td><span data-ttu-id="a51dc-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-673">HR</span></span></td>
<td><span data-ttu-id="a51dc-674">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-674">10001</span></span></td>
<td><span data-ttu-id="a51dc-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-675">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-676">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-677">500.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-679">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-679">CC001</span></span></td>
<td><span data-ttu-id="a51dc-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-680">HR</span></span></td>
<td><span data-ttu-id="a51dc-681">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-681">10001</span></span></td>
<td><span data-ttu-id="a51dc-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-682">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-683">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a51dc-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-686">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-686">CC002</span></span></td>
<td><span data-ttu-id="a51dc-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-687">Finance</span></span></td>
<td><span data-ttu-id="a51dc-688">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-688">10001</span></span></td>
<td><span data-ttu-id="a51dc-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-689">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-690">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-691">675.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-693">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-693">CC002</span></span></td>
<td><span data-ttu-id="a51dc-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-694">Finance</span></span></td>
<td><span data-ttu-id="a51dc-695">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-695">10001</span></span></td>
<td><span data-ttu-id="a51dc-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-696">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-697">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a51dc-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-700">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-700">CC003</span></span></td>
<td><span data-ttu-id="a51dc-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-701">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-702">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-702">10001</span></span></td>
<td><span data-ttu-id="a51dc-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-703">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-704">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-705">713.75</span><span class="sxs-lookup"><span data-stu-id="a51dc-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-707">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-707">CC003</span></span></td>
<td><span data-ttu-id="a51dc-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-708">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-709">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-709">10001</span></span></td>
<td><span data-ttu-id="a51dc-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-710">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-711">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a51dc-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-714">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-714">CC003</span></span></td>
<td><span data-ttu-id="a51dc-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-715">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-716">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-716">10001</span></span></td>
<td><span data-ttu-id="a51dc-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-717">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-718">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-719">286.25</span><span class="sxs-lookup"><span data-stu-id="a51dc-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-721">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-721">CC003</span></span></td>
<td><span data-ttu-id="a51dc-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-722">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-723">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-723">10001</span></span></td>
<td><span data-ttu-id="a51dc-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-724">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-725">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a51dc-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-728">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-729">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-730">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-730">10001</span></span></td>
<td><span data-ttu-id="a51dc-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-731">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-732">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-733">776.36</span><span class="sxs-lookup"><span data-stu-id="a51dc-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-735">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-736">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-737">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-737">10001</span></span></td>
<td><span data-ttu-id="a51dc-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-738">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-739">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a51dc-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-742">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-743">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-744">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-744">10001</span></span></td>
<td><span data-ttu-id="a51dc-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-745">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-746">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-747">223.64</span><span class="sxs-lookup"><span data-stu-id="a51dc-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="a51dc-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-749">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-750">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-751">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-751">10001</span></span></td>
<td><span data-ttu-id="a51dc-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-752">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-753">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a51dc-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a51dc-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a51dc-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a51dc-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-757">Cost element</span></span></th>
<th><span data-ttu-id="a51dc-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-758">Cost behavior</span></span></th>
<th><span data-ttu-id="a51dc-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a51dc-759">Amount</span></span></th>
<th><span data-ttu-id="a51dc-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="a51dc-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a51dc-761">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-761">CC001</span></span></td>
<td><span data-ttu-id="a51dc-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-762">HR</span></span></td>
<td><span data-ttu-id="a51dc-763">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-763">10001</span></span></td>
<td><span data-ttu-id="a51dc-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-764">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-765">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-766">-500.00</span></span></td>
<td><span data-ttu-id="a51dc-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-768">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-768">CC002</span></span></td>
<td><span data-ttu-id="a51dc-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-769">Finance</span></span></td>
<td><span data-ttu-id="a51dc-770">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-770">10001</span></span></td>
<td><span data-ttu-id="a51dc-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-771">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-772">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-773">175.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-773">175.00</span></span></td>
<td><span data-ttu-id="a51dc-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-775">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-775">CC003</span></span></td>
<td><span data-ttu-id="a51dc-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-776">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-777">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-777">10001</span></span></td>
<td><span data-ttu-id="a51dc-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-778">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-779">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-780">275.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-780">275.00</span></span></td>
<td><span data-ttu-id="a51dc-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-782">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-782">CC004</span></span></td>
<td><span data-ttu-id="a51dc-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-783">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-784">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-784">10001</span></span></td>
<td><span data-ttu-id="a51dc-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-785">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-786">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-787">50,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-787">50,00</span></span></td>
<td><span data-ttu-id="a51dc-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-789">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-789">CC001</span></span></td>
<td><span data-ttu-id="a51dc-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="a51dc-790">HR</span></span></td>
<td><span data-ttu-id="a51dc-791">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-791">10001</span></span></td>
<td><span data-ttu-id="a51dc-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-792">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-793">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="a51dc-794">-1,245.71</span></span></td>
<td><span data-ttu-id="a51dc-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-796">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-796">CC002</span></span></td>
<td><span data-ttu-id="a51dc-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-797">Finance</span></span></td>
<td><span data-ttu-id="a51dc-798">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-798">10001</span></span></td>
<td><span data-ttu-id="a51dc-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-799">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-800">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-801">436.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-801">436.00</span></span></td>
<td><span data-ttu-id="a51dc-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-803">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-803">CC003</span></span></td>
<td><span data-ttu-id="a51dc-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-804">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-805">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-805">10001</span></span></td>
<td><span data-ttu-id="a51dc-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-806">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-807">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-808">685.14</span><span class="sxs-lookup"><span data-stu-id="a51dc-808">685.14</span></span></td>
<td><span data-ttu-id="a51dc-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-810">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-810">CC004</span></span></td>
<td><span data-ttu-id="a51dc-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-811">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-812">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-812">10001</span></span></td>
<td><span data-ttu-id="a51dc-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-813">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-814">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-815">124.57</span><span class="sxs-lookup"><span data-stu-id="a51dc-815">124.57</span></span></td>
<td><span data-ttu-id="a51dc-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-817">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-817">CC002</span></span></td>
<td><span data-ttu-id="a51dc-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-818">Finance</span></span></td>
<td><span data-ttu-id="a51dc-819">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-819">10001</span></span></td>
<td><span data-ttu-id="a51dc-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-820">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-821">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-822">-675.00</span></span></td>
<td><span data-ttu-id="a51dc-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-824">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-824">CC003</span></span></td>
<td><span data-ttu-id="a51dc-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-825">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-826">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-826">10001</span></span></td>
<td><span data-ttu-id="a51dc-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-827">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-828">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-829">438.75</span><span class="sxs-lookup"><span data-stu-id="a51dc-829">438.75</span></span></td>
<td><span data-ttu-id="a51dc-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-831">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-831">CC004</span></span></td>
<td><span data-ttu-id="a51dc-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-832">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-833">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-833">10001</span></span></td>
<td><span data-ttu-id="a51dc-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-834">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-835">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-836">236.25</span><span class="sxs-lookup"><span data-stu-id="a51dc-836">236.25</span></span></td>
<td><span data-ttu-id="a51dc-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-838">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-838">CC002</span></span></td>
<td><span data-ttu-id="a51dc-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="a51dc-839">Finance</span></span></td>
<td><span data-ttu-id="a51dc-840">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-840">10001</span></span></td>
<td><span data-ttu-id="a51dc-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-841">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-842">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="a51dc-843">-8,150.29</span></span></td>
<td><span data-ttu-id="a51dc-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-845">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-845">CC003</span></span></td>
<td><span data-ttu-id="a51dc-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-846">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-847">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-847">10001</span></span></td>
<td><span data-ttu-id="a51dc-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-848">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-849">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a51dc-850">5,297.69</span></span></td>
<td><span data-ttu-id="a51dc-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-852">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-852">CC004</span></span></td>
<td><span data-ttu-id="a51dc-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="a51dc-853">Packaging</span></span></td>
<td><span data-ttu-id="a51dc-854">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-854">10001</span></span></td>
<td><span data-ttu-id="a51dc-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-855">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-856">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a51dc-857">2,852.60</span></span></td>
<td><span data-ttu-id="a51dc-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-859">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-859">CC003</span></span></td>
<td><span data-ttu-id="a51dc-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-860">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-861">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-861">10001</span></span></td>
<td><span data-ttu-id="a51dc-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-862">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-863">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="a51dc-864">-713.75</span></span></td>
<td><span data-ttu-id="a51dc-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-866">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-867">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-868">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-868">10001</span></span></td>
<td><span data-ttu-id="a51dc-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-869">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-870">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-871">535.31</span><span class="sxs-lookup"><span data-stu-id="a51dc-871">535.31</span></span></td>
<td><span data-ttu-id="a51dc-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-873">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-874">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-875">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-875">10001</span></span></td>
<td><span data-ttu-id="a51dc-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-876">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-877">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-878">178.44</span><span class="sxs-lookup"><span data-stu-id="a51dc-878">178.44</span></span></td>
<td><span data-ttu-id="a51dc-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-880">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-880">CC003</span></span></td>
<td><span data-ttu-id="a51dc-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-881">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-882">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-882">10001</span></span></td>
<td><span data-ttu-id="a51dc-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-883">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-884">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="a51dc-885">-5,982.83</span></span></td>
<td><span data-ttu-id="a51dc-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-887">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-888">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-889">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-889">10001</span></span></td>
<td><span data-ttu-id="a51dc-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-890">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-891">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a51dc-892">4,487.12</span></span></td>
<td><span data-ttu-id="a51dc-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-894">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-895">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-896">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-896">10001</span></span></td>
<td><span data-ttu-id="a51dc-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-897">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-898">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a51dc-899">1,495.71</span></span></td>
<td><span data-ttu-id="a51dc-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-901">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-901">CC003</span></span></td>
<td><span data-ttu-id="a51dc-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-902">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-903">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-903">10001</span></span></td>
<td><span data-ttu-id="a51dc-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-904">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-905">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="a51dc-906">-286.25</span></span></td>
<td><span data-ttu-id="a51dc-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-908">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-909">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-910">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-910">10001</span></span></td>
<td><span data-ttu-id="a51dc-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-911">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-912">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-913">241.05</span><span class="sxs-lookup"><span data-stu-id="a51dc-913">241.05</span></span></td>
<td><span data-ttu-id="a51dc-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-915">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-916">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-917">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-917">10001</span></span></td>
<td><span data-ttu-id="a51dc-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-918">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-919">Fixed cost</span></span></td>
<td><span data-ttu-id="a51dc-920">45.20</span><span class="sxs-lookup"><span data-stu-id="a51dc-920">45.20</span></span></td>
<td><span data-ttu-id="a51dc-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-922">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-922">CC003</span></span></td>
<td><span data-ttu-id="a51dc-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="a51dc-923">Assembly</span></span></td>
<td><span data-ttu-id="a51dc-924">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-924">10001</span></span></td>
<td><span data-ttu-id="a51dc-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-925">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-926">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="a51dc-927">-2,977.17</span></span></td>
<td><span data-ttu-id="a51dc-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-929">Prod 1</span></span></td>
<td><span data-ttu-id="a51dc-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-930">Product 1</span></span></td>
<td><span data-ttu-id="a51dc-931">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-931">10001</span></span></td>
<td><span data-ttu-id="a51dc-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-932">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-933">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a51dc-934">2,507.09</span></span></td>
<td><span data-ttu-id="a51dc-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a51dc-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-936">Prod 2</span></span></td>
<td><span data-ttu-id="a51dc-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-937">Product 2</span></span></td>
<td><span data-ttu-id="a51dc-938">10001</span><span class="sxs-lookup"><span data-stu-id="a51dc-938">10001</span></span></td>
<td><span data-ttu-id="a51dc-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-939">Electricity</span></span></td>
<td><span data-ttu-id="a51dc-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-940">Variable cost</span></span></td>
<td><span data-ttu-id="a51dc-941">470.08</span><span class="sxs-lookup"><span data-stu-id="a51dc-941">470.08</span></span></td>
<td><span data-ttu-id="a51dc-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="a51dc-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a51dc-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="a51dc-943">Conclusion</span></span>
<span data-ttu-id="a51dc-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a51dc-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="a51dc-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a51dc-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="a51dc-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a51dc-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a51dc-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a51dc-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="a51dc-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a51dc-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="a51dc-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a51dc-951">CC099</span><span class="sxs-lookup"><span data-stu-id="a51dc-951">CC099</span></span></th>
<th><span data-ttu-id="a51dc-952">CC001</span><span class="sxs-lookup"><span data-stu-id="a51dc-952">CC001</span></span></th>
<th><span data-ttu-id="a51dc-953">CC002</span><span class="sxs-lookup"><span data-stu-id="a51dc-953">CC002</span></span></th>
<th><span data-ttu-id="a51dc-954">CC003</span><span class="sxs-lookup"><span data-stu-id="a51dc-954">CC003</span></span></th>
<th><span data-ttu-id="a51dc-955">CC004</span><span class="sxs-lookup"><span data-stu-id="a51dc-955">CC004</span></span></th>
<th><span data-ttu-id="a51dc-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-956">Proj 1</span></span></th>
<th><span data-ttu-id="a51dc-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-957">Proj 2</span></span></th>
<th><span data-ttu-id="a51dc-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="a51dc-958">Prod 1</span></span></th>
<th><span data-ttu-id="a51dc-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="a51dc-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a51dc-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="a51dc-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a51dc-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="a51dc-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-971">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a51dc-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-973">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-974">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-975">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-976">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-977">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-978">776.36</span><span class="sxs-lookup"><span data-stu-id="a51dc-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-979">223.64</span><span class="sxs-lookup"><span data-stu-id="a51dc-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a51dc-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="a51dc-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-982">000</span><span class="sxs-lookup"><span data-stu-id="a51dc-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-983">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-984">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-985">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-986">0,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-987">30.00</span><span class="sxs-lookup"><span data-stu-id="a51dc-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-988">10,00</span><span class="sxs-lookup"><span data-stu-id="a51dc-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a51dc-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a51dc-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a51dc-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a51dc-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a51dc-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a51dc-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="a51dc-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a51dc-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="a51dc-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a51dc-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="a51dc-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a51dc-996">Дополнительные сведения см. в разделе [Свертка затрат](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="a51dc-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




