---
title: "Расчет накладных расходов"
description: "В этом разделе описываются типовые процессы расчета и распределения накладных расходов."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: ru-ru
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="582d0-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="582d0-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="582d0-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="582d0-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="582d0-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="582d0-105">Term definition</span></span>
---------------

<span data-ttu-id="582d0-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="582d0-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="582d0-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="582d0-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="582d0-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="582d0-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="582d0-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="582d0-109">Rent</span></span>
-   <span data-ttu-id="582d0-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-110">Electricity</span></span>
-   <span data-ttu-id="582d0-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="582d0-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="582d0-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="582d0-112">Overhead calculation overview</span></span>
<span data-ttu-id="582d0-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="582d0-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="582d0-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="582d0-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="582d0-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="582d0-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="582d0-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="582d0-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="582d0-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="582d0-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="582d0-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="582d0-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="582d0-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="582d0-119">Version type</span></span>
-   <span data-ttu-id="582d0-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="582d0-120">Date and time</span></span>
-   <span data-ttu-id="582d0-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="582d0-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="582d0-122">Fiscal year</span></span>
-   <span data-ttu-id="582d0-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="582d0-123">Fiscal period</span></span>

<span data-ttu-id="582d0-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="582d0-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="582d0-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="582d0-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="582d0-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="582d0-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="582d0-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="582d0-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="582d0-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="582d0-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="582d0-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="582d0-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="582d0-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="582d0-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="582d0-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="582d0-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="582d0-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="582d0-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="582d0-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="582d0-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="582d0-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="582d0-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="582d0-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="582d0-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="582d0-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="582d0-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="582d0-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="582d0-140">Main account</span></span></th>
<th><span data-ttu-id="582d0-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="582d0-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="582d0-143">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-143">CC099</span></span></td>
<td><span data-ttu-id="582d0-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-144">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-145">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-145">10001</span></span></td>
<td><span data-ttu-id="582d0-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-146">Electricity</span></span></td>
<td><span data-ttu-id="582d0-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="582d0-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="582d0-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="582d0-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="582d0-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="582d0-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="582d0-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-151">Define the cost behavior rule</span></span>

<span data-ttu-id="582d0-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="582d0-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="582d0-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="582d0-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="582d0-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="582d0-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="582d0-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="582d0-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="582d0-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="582d0-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="582d0-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="582d0-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-160">Journal</span></span></th>
<th><span data-ttu-id="582d0-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="582d0-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="582d0-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="582d0-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="582d0-163">Версия</span><span class="sxs-lookup"><span data-stu-id="582d0-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-164">00001</span><span class="sxs-lookup"><span data-stu-id="582d0-164">00001</span></span></td>
<td><span data-ttu-id="582d0-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="582d0-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="582d0-166">Fiscal</span></span></td>
<td><span data-ttu-id="582d0-167">2017</span><span class="sxs-lookup"><span data-stu-id="582d0-167">2017</span></span></td>
<td><span data-ttu-id="582d0-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-168">Period 1</span></span></td>
<td><span data-ttu-id="582d0-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="582d0-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="582d0-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-173">Cost element</span></span></th>
<th><span data-ttu-id="582d0-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-174">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="582d0-177">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-177">CC099</span></span></td>
<td><span data-ttu-id="582d0-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-178">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-179">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-179">10001</span></span></td>
<td><span data-ttu-id="582d0-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-180">Electricity</span></span></td>
<td><span data-ttu-id="582d0-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="582d0-181">Unclassified</span></span></td>
<td><span data-ttu-id="582d0-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="582d0-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="582d0-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-185">Cost element</span></span></th>
<th><span data-ttu-id="582d0-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-186">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-187">Amount</span></span></th>
<th><span data-ttu-id="582d0-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-189">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-189">CC099</span></span></td>
<td><span data-ttu-id="582d0-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-190">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-191">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-191">10001</span></span></td>
<td><span data-ttu-id="582d0-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-192">Electricity</span></span></td>
<td><span data-ttu-id="582d0-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="582d0-193">Unclassified</span></span></td>
<td><span data-ttu-id="582d0-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="582d0-194">10,000.00</span></span></td>
<td><span data-ttu-id="582d0-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-196">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-196">CC099</span></span></td>
<td><span data-ttu-id="582d0-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-197">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-198">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-198">10001</span></span></td>
<td><span data-ttu-id="582d0-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-199">Electricity</span></span></td>
<td><span data-ttu-id="582d0-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="582d0-200">Unclassified</span></span></td>
<td><span data-ttu-id="582d0-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-201">-10,000.00</span></span></td>
<td><span data-ttu-id="582d0-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-203">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-203">CC099</span></span></td>
<td><span data-ttu-id="582d0-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-204">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-205">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-205">10001</span></span></td>
<td><span data-ttu-id="582d0-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-206">Electricity</span></span></td>
<td><span data-ttu-id="582d0-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-207">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-208">1,000.00</span></span></td>
<td><span data-ttu-id="582d0-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-210">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-210">CC099</span></span></td>
<td><span data-ttu-id="582d0-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-211">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-212">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-212">10001</span></span></td>
<td><span data-ttu-id="582d0-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-213">Electricity</span></span></td>
<td><span data-ttu-id="582d0-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-214">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="582d0-215">9,000.00</span></span></td>
<td><span data-ttu-id="582d0-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-217">Подробные сведения о поведении затрат см. в разделе "Политика поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="582d0-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="582d0-218">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="582d0-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="582d0-219">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="582d0-220">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="582d0-221">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="582d0-222">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-222">Define the cost distribution rule</span></span>

<span data-ttu-id="582d0-223">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="582d0-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="582d0-224">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="582d0-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="582d0-225">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="582d0-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="582d0-226">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="582d0-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="582d0-227">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="582d0-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="582d0-228">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-229">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-229">Cost object</span></span></th>
<th><span data-ttu-id="582d0-230">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="582d0-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-231">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-231">CC001</span></span></td>
<td><span data-ttu-id="582d0-232">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-232">HR</span></span></td>
<td><span data-ttu-id="582d0-233">1000</span><span class="sxs-lookup"><span data-stu-id="582d0-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-234">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-234">CC002</span></span></td>
<td><span data-ttu-id="582d0-235">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-235">Finance</span></span></td>
<td><span data-ttu-id="582d0-236">6,000</span><span class="sxs-lookup"><span data-stu-id="582d0-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-237">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-237">CC003</span></span></td>
<td><span data-ttu-id="582d0-238">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-238">Assembly</span></span></td>
<td><span data-ttu-id="582d0-239">0</span><span class="sxs-lookup"><span data-stu-id="582d0-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-240">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-241">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-241">Cost object</span></span></th>
<th><span data-ttu-id="582d0-242">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-242">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-243">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-243">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-244">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-245">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-245">CC001</span></span></td>
<td><span data-ttu-id="582d0-246">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-246">HR</span></span></td>
<td><span data-ttu-id="582d0-247">1000</span><span class="sxs-lookup"><span data-stu-id="582d0-247">1,000</span></span></td>
<td><span data-ttu-id="582d0-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="582d0-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="582d0-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-250">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-250">CC002</span></span></td>
<td><span data-ttu-id="582d0-251">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-251">Finance</span></span></td>
<td><span data-ttu-id="582d0-252">6,000</span><span class="sxs-lookup"><span data-stu-id="582d0-252">6,000</span></span></td>
<td><span data-ttu-id="582d0-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="582d0-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="582d0-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-255">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-255">CC003</span></span></td>
<td><span data-ttu-id="582d0-256">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-256">Assembly</span></span></td>
<td><span data-ttu-id="582d0-257">0</span><span class="sxs-lookup"><span data-stu-id="582d0-257">0</span></span></td>
<td><span data-ttu-id="582d0-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="582d0-259">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-260">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="582d0-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="582d0-261">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-262">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-262">Cost object</span></span></th>
<th><span data-ttu-id="582d0-263">Формула</span><span class="sxs-lookup"><span data-stu-id="582d0-263">Formula</span></span></th>
<th><span data-ttu-id="582d0-264">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-264">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-265">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-265">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-266">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-267">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-267">CC001</span></span></td>
<td><span data-ttu-id="582d0-268">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-268">HR</span></span></td>
<td><span data-ttu-id="582d0-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="582d0-270">1</span><span class="sxs-lookup"><span data-stu-id="582d0-270">1</span></span></td>
<td><span data-ttu-id="582d0-271">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="582d0-272">500.00</span><span class="sxs-lookup"><span data-stu-id="582d0-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-273">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-273">CC002</span></span></td>
<td><span data-ttu-id="582d0-274">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-274">Finance</span></span></td>
<td><span data-ttu-id="582d0-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="582d0-276">1</span><span class="sxs-lookup"><span data-stu-id="582d0-276">1</span></span></td>
<td><span data-ttu-id="582d0-277">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="582d0-278">500.00</span><span class="sxs-lookup"><span data-stu-id="582d0-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-279">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-279">CC003</span></span></td>
<td><span data-ttu-id="582d0-280">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-280">Assembly</span></span></td>
<td><span data-ttu-id="582d0-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="582d0-282">0</span><span class="sxs-lookup"><span data-stu-id="582d0-282">0</span></span></td>
<td><span data-ttu-id="582d0-283">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="582d0-284">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="582d0-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-286">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-286">Journal</span></span></th>
<th><span data-ttu-id="582d0-287">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="582d0-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="582d0-288">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="582d0-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="582d0-289">Версия</span><span class="sxs-lookup"><span data-stu-id="582d0-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-290">00002</span><span class="sxs-lookup"><span data-stu-id="582d0-290">00002</span></span></td>
<td><span data-ttu-id="582d0-291">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="582d0-292">Финансовый</span><span class="sxs-lookup"><span data-stu-id="582d0-292">Fiscal</span></span></td>
<td><span data-ttu-id="582d0-293">2017</span><span class="sxs-lookup"><span data-stu-id="582d0-293">2017</span></span></td>
<td><span data-ttu-id="582d0-294">Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-294">Period 1</span></span></td>
<td><span data-ttu-id="582d0-295">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="582d0-296">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="582d0-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-297">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-298">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-299">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-299">Cost element</span></span></th>
<th><span data-ttu-id="582d0-300">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-300">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-301">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-302">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-303">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-303">CC099</span></span></td>
<td><span data-ttu-id="582d0-304">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-304">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-305">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-305">10001</span></span></td>
<td><span data-ttu-id="582d0-306">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-306">Electricity</span></span></td>
<td><span data-ttu-id="582d0-307">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-307">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-309">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-310">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-310">CC099</span></span></td>
<td><span data-ttu-id="582d0-311">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-311">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-312">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-312">10001</span></span></td>
<td><span data-ttu-id="582d0-313">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-313">Electricity</span></span></td>
<td><span data-ttu-id="582d0-314">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-314">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="582d0-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="582d0-316">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-317">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-318">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-318">Cost element</span></span></th>
<th><span data-ttu-id="582d0-319">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-319">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-320">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-320">Amount</span></span></th>
<th><span data-ttu-id="582d0-321">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-322">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-322">CC099</span></span></td>
<td><span data-ttu-id="582d0-323">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-323">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-324">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-324">10001</span></span></td>
<td><span data-ttu-id="582d0-325">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-325">Electricity</span></span></td>
<td><span data-ttu-id="582d0-326">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-326">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-327">-1,000.00</span></span></td>
<td><span data-ttu-id="582d0-328">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-329">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-329">CC001</span></span></td>
<td><span data-ttu-id="582d0-330">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-330">HR</span></span></td>
<td><span data-ttu-id="582d0-331">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-331">10001</span></span></td>
<td><span data-ttu-id="582d0-332">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-332">Electricity</span></span></td>
<td><span data-ttu-id="582d0-333">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-333">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-334">500.00</span><span class="sxs-lookup"><span data-stu-id="582d0-334">500.00</span></span></td>
<td><span data-ttu-id="582d0-335">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-336">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-336">CC002</span></span></td>
<td><span data-ttu-id="582d0-337">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-337">Finance</span></span></td>
<td><span data-ttu-id="582d0-338">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-338">10001</span></span></td>
<td><span data-ttu-id="582d0-339">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-339">Electricity</span></span></td>
<td><span data-ttu-id="582d0-340">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-340">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-341">500.00</span><span class="sxs-lookup"><span data-stu-id="582d0-341">500.00</span></span></td>
<td><span data-ttu-id="582d0-342">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-343">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-343">CC099</span></span></td>
<td><span data-ttu-id="582d0-344">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="582d0-344">Default cost center</span></span></td>
<td><span data-ttu-id="582d0-345">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-345">10001</span></span></td>
<td><span data-ttu-id="582d0-346">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-346">Electricity</span></span></td>
<td><span data-ttu-id="582d0-347">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-347">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-348">-9000,00</span><span class="sxs-lookup"><span data-stu-id="582d0-348">-9,000.00</span></span></td>
<td><span data-ttu-id="582d0-349">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-350">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-350">CC001</span></span></td>
<td><span data-ttu-id="582d0-351">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-351">HR</span></span></td>
<td><span data-ttu-id="582d0-352">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-352">10001</span></span></td>
<td><span data-ttu-id="582d0-353">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-353">Electricity</span></span></td>
<td><span data-ttu-id="582d0-354">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-354">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="582d0-355">1,285.71</span></span></td>
<td><span data-ttu-id="582d0-356">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-357">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-357">CC002</span></span></td>
<td><span data-ttu-id="582d0-358">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-358">Finance</span></span></td>
<td><span data-ttu-id="582d0-359">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-359">10001</span></span></td>
<td><span data-ttu-id="582d0-360">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-360">Electricity</span></span></td>
<td><span data-ttu-id="582d0-361">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-361">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="582d0-362">7,714.29</span></span></td>
<td><span data-ttu-id="582d0-363">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-364">Подробные сведения о распределении затрат и базах распределения затрат см. в разделе "Политика распределения затрат и базы распределения".</span><span class="sxs-lookup"><span data-stu-id="582d0-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="582d0-365">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="582d0-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="582d0-366">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="582d0-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="582d0-367">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="582d0-368">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="582d0-369">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="582d0-369">Define the overhead rate</span></span>

<span data-ttu-id="582d0-370">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="582d0-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="582d0-371">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="582d0-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-372">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-372">Cost object</span></span></th>
<th><span data-ttu-id="582d0-373">Часы</span><span class="sxs-lookup"><span data-stu-id="582d0-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-374">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-374">Proj 1</span></span></td>
<td><span data-ttu-id="582d0-375">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-375">Project 1</span></span></td>
<td><span data-ttu-id="582d0-376">3</span><span class="sxs-lookup"><span data-stu-id="582d0-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-377">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-377">Proj 2</span></span></td>
<td><span data-ttu-id="582d0-378">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-378">Project 2</span></span></td>
<td><span data-ttu-id="582d0-379">1</span><span class="sxs-lookup"><span data-stu-id="582d0-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-380">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-381">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-381">Cost object</span></span></th>
<th><span data-ttu-id="582d0-382">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-382">Cost element</span></span></th>
<th><span data-ttu-id="582d0-383">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-383">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-384">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="582d0-384">Units</span></span></th>
<th><span data-ttu-id="582d0-385">По норме</span><span class="sxs-lookup"><span data-stu-id="582d0-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-386">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-386">CC001</span></span></td>
<td><span data-ttu-id="582d0-387">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-387">HR</span></span></td>
<td><span data-ttu-id="582d0-388">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-388">10001</span></span></td>
<td><span data-ttu-id="582d0-389">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-389">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-390">1</span><span class="sxs-lookup"><span data-stu-id="582d0-390">1</span></span></td>
<td><span data-ttu-id="582d0-391">10</span><span class="sxs-lookup"><span data-stu-id="582d0-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-392">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-393">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-393">Cost object</span></span></th>
<th><span data-ttu-id="582d0-394">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-394">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-395">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-395">Cost element</span></span></th>
<th><span data-ttu-id="582d0-396">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-396">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-397">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-398">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-398">Proj 1</span></span></td>
<td><span data-ttu-id="582d0-399">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-399">Project 1</span></span></td>
<td><span data-ttu-id="582d0-400">3</span><span class="sxs-lookup"><span data-stu-id="582d0-400">3</span></span></td>
<td><span data-ttu-id="582d0-401">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-401">10001</span></span></td>
<td><span data-ttu-id="582d0-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="582d0-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="582d0-403">30.00</span><span class="sxs-lookup"><span data-stu-id="582d0-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-404">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-404">Proj 2</span></span></td>
<td><span data-ttu-id="582d0-405">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-405">Project 2</span></span></td>
<td><span data-ttu-id="582d0-406">1</span><span class="sxs-lookup"><span data-stu-id="582d0-406">1</span></span></td>
<td><span data-ttu-id="582d0-407">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-407">10001</span></span></td>
<td><span data-ttu-id="582d0-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="582d0-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="582d0-409">10,00</span><span class="sxs-lookup"><span data-stu-id="582d0-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="582d0-410">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-411">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-411">Journal</span></span></th>
<th><span data-ttu-id="582d0-412">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="582d0-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="582d0-413">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="582d0-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="582d0-414">Версия</span><span class="sxs-lookup"><span data-stu-id="582d0-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-415">00003</span><span class="sxs-lookup"><span data-stu-id="582d0-415">00003</span></span></td>
<td><span data-ttu-id="582d0-416">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="582d0-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="582d0-417">Финансовый</span><span class="sxs-lookup"><span data-stu-id="582d0-417">Fiscal</span></span></td>
<td><span data-ttu-id="582d0-418">2017</span><span class="sxs-lookup"><span data-stu-id="582d0-418">2017</span></span></td>
<td><span data-ttu-id="582d0-419">Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-419">Period 1</span></span></td>
<td><span data-ttu-id="582d0-420">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="582d0-421">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="582d0-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-422">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-423">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-423">Cost object</span></span></th>
<th><span data-ttu-id="582d0-424">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-425">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-426">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-426">Proj 1</span></span></td>
<td><span data-ttu-id="582d0-427">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="582d0-428">3,00</span><span class="sxs-lookup"><span data-stu-id="582d0-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-429">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-430">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-430">Proj 2</span></span></td>
<td><span data-ttu-id="582d0-431">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="582d0-432">1.00</span><span class="sxs-lookup"><span data-stu-id="582d0-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="582d0-433">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-434">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-435">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-435">Cost element</span></span></th>
<th><span data-ttu-id="582d0-436">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-436">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-437">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-437">Amount</span></span></th>
<th><span data-ttu-id="582d0-438">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="582d0-439">CC0001</span></span></td>
<td><span data-ttu-id="582d0-440">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-440">HR</span></span></td>
<td><span data-ttu-id="582d0-441">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-441">10001</span></span></td>
<td><span data-ttu-id="582d0-442">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-442">Electricity</span></span></td>
<td><span data-ttu-id="582d0-443">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-443">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="582d0-444">-30.00</span></span></td>
<td><span data-ttu-id="582d0-445">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-446">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-446">Proj 1</span></span></td>
<td><span data-ttu-id="582d0-447">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="582d0-448">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-448">10001</span></span></td>
<td><span data-ttu-id="582d0-449">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-449">Electricity</span></span></td>
<td><span data-ttu-id="582d0-450">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-450">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-451">30.00</span><span class="sxs-lookup"><span data-stu-id="582d0-451">30.00</span></span></td>
<td><span data-ttu-id="582d0-452">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-453">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-453">CC001</span></span></td>
<td><span data-ttu-id="582d0-454">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-454">HR</span></span></td>
<td><span data-ttu-id="582d0-455">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-455">10001</span></span></td>
<td><span data-ttu-id="582d0-456">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-456">Electricity</span></span></td>
<td><span data-ttu-id="582d0-457">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-457">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="582d0-458">-10.00</span></span></td>
<td><span data-ttu-id="582d0-459">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-460">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-460">Proj 2</span></span></td>
<td><span data-ttu-id="582d0-461">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="582d0-462">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-462">10001</span></span></td>
<td><span data-ttu-id="582d0-463">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-463">Electricity</span></span></td>
<td><span data-ttu-id="582d0-464">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-464">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-465">10,00</span><span class="sxs-lookup"><span data-stu-id="582d0-465">10.00</span></span></td>
<td><span data-ttu-id="582d0-466">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-467">Подробные сведения о политике ставки накладных расходов см. в разделе "Политика ставки накладных расходов и базы распределения".</span><span class="sxs-lookup"><span data-stu-id="582d0-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="582d0-468">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="582d0-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="582d0-469">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="582d0-470">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="582d0-471">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="582d0-472">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="582d0-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="582d0-473">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="582d0-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="582d0-474">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="582d0-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="582d0-475">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="582d0-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="582d0-476">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="582d0-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="582d0-477">[![Взаимный метод](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="582d0-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="582d0-478">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-478">Define the cost allocation</span></span>

<span data-ttu-id="582d0-479">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="582d0-480">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="582d0-481">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="582d0-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-482">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-482">Cost object</span></span></th>
<th><span data-ttu-id="582d0-483">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-484">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-484">CC002</span></span></td>
<td><span data-ttu-id="582d0-485">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-485">Finance</span></span></td>
<td><span data-ttu-id="582d0-486">35</span><span class="sxs-lookup"><span data-stu-id="582d0-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-487">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-487">CC003</span></span></td>
<td><span data-ttu-id="582d0-488">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-488">Assembly</span></span></td>
<td><span data-ttu-id="582d0-489">55</span><span class="sxs-lookup"><span data-stu-id="582d0-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-490">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-490">CC004</span></span></td>
<td><span data-ttu-id="582d0-491">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-491">Packaging</span></span></td>
<td><span data-ttu-id="582d0-492">10</span><span class="sxs-lookup"><span data-stu-id="582d0-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-493">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="582d0-494">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="582d0-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-495">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-495">Cost object</span></span></th>
<th><span data-ttu-id="582d0-496">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="582d0-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-497">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-497">CC003</span></span></td>
<td><span data-ttu-id="582d0-498">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-498">Assembly</span></span></td>
<td><span data-ttu-id="582d0-499">65</span><span class="sxs-lookup"><span data-stu-id="582d0-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-500">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-500">CC004</span></span></td>
<td><span data-ttu-id="582d0-501">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-501">Packaging</span></span></td>
<td><span data-ttu-id="582d0-502">35</span><span class="sxs-lookup"><span data-stu-id="582d0-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-503">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="582d0-504">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="582d0-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-505">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-505">Cost object</span></span></th>
<th><span data-ttu-id="582d0-506">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="582d0-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-507">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-507">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-508">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-508">Product 1</span></span></td>
<td><span data-ttu-id="582d0-509">60</span><span class="sxs-lookup"><span data-stu-id="582d0-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-510">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-510">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-511">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-511">Product 2</span></span></td>
<td><span data-ttu-id="582d0-512">20</span><span class="sxs-lookup"><span data-stu-id="582d0-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-513">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="582d0-514">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="582d0-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-515">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-515">Cost object</span></span></th>
<th><span data-ttu-id="582d0-516">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="582d0-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-517">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-517">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-518">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-518">Product 1</span></span></td>
<td><span data-ttu-id="582d0-519">80</span><span class="sxs-lookup"><span data-stu-id="582d0-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-520">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-520">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-521">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-521">Product 2</span></span></td>
<td><span data-ttu-id="582d0-522">15</span><span class="sxs-lookup"><span data-stu-id="582d0-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-523">**Примечание.** В Finance and Operations статистические меры, такие как время производства, которое использует продукт, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="582d0-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="582d0-524">Более подробные сведения о поставщиках статистических мер см. в разделе "Шаблоны поставщика статистической меры".</span><span class="sxs-lookup"><span data-stu-id="582d0-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="582d0-525">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.) В следующей таблице показан результат, когда услуги отдела кадров применяются в качестве базы распределения для общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="582d0-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-526">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-526">Cost object</span></span></th>
<th><span data-ttu-id="582d0-527">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-527">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-528">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-528">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-529">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-529">Amount</span></span></th>
<th><span data-ttu-id="582d0-530">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-531">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-531">CC002</span></span></td>
<td><span data-ttu-id="582d0-532">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-532">Finance</span></span></td>
<td><span data-ttu-id="582d0-533">35</span><span class="sxs-lookup"><span data-stu-id="582d0-533">35</span></span></td>
<td><span data-ttu-id="582d0-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="582d0-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="582d0-535">175.00</span><span class="sxs-lookup"><span data-stu-id="582d0-535">175.00</span></span></td>
<td><span data-ttu-id="582d0-536">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-537">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-537">CC003</span></span></td>
<td><span data-ttu-id="582d0-538">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-538">Assembly</span></span></td>
<td><span data-ttu-id="582d0-539">55</span><span class="sxs-lookup"><span data-stu-id="582d0-539">55</span></span></td>
<td><span data-ttu-id="582d0-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="582d0-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="582d0-541">275.00</span><span class="sxs-lookup"><span data-stu-id="582d0-541">275.00</span></span></td>
<td><span data-ttu-id="582d0-542">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-543">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-543">CC004</span></span></td>
<td><span data-ttu-id="582d0-544">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-544">Packaging</span></span></td>
<td><span data-ttu-id="582d0-545">10</span><span class="sxs-lookup"><span data-stu-id="582d0-545">10</span></span></td>
<td><span data-ttu-id="582d0-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="582d0-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="582d0-547">50,00</span><span class="sxs-lookup"><span data-stu-id="582d0-547">50.00</span></span></td>
<td><span data-ttu-id="582d0-548">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-549">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-549">CC002</span></span></td>
<td><span data-ttu-id="582d0-550">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-550">Finance</span></span></td>
<td><span data-ttu-id="582d0-551">35</span><span class="sxs-lookup"><span data-stu-id="582d0-551">35</span></span></td>
<td><span data-ttu-id="582d0-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="582d0-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="582d0-553">436.00</span><span class="sxs-lookup"><span data-stu-id="582d0-553">436.00</span></span></td>
<td><span data-ttu-id="582d0-554">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-555">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-555">CC003</span></span></td>
<td><span data-ttu-id="582d0-556">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-556">Assembly</span></span></td>
<td><span data-ttu-id="582d0-557">55</span><span class="sxs-lookup"><span data-stu-id="582d0-557">55</span></span></td>
<td><span data-ttu-id="582d0-558">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="582d0-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="582d0-559">685.14</span><span class="sxs-lookup"><span data-stu-id="582d0-559">685.14</span></span></td>
<td><span data-ttu-id="582d0-560">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-561">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-561">CC004</span></span></td>
<td><span data-ttu-id="582d0-562">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-562">Packaging</span></span></td>
<td><span data-ttu-id="582d0-563">10</span><span class="sxs-lookup"><span data-stu-id="582d0-563">10</span></span></td>
<td><span data-ttu-id="582d0-564">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="582d0-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="582d0-565">124.57</span><span class="sxs-lookup"><span data-stu-id="582d0-565">124.57</span></span></td>
<td><span data-ttu-id="582d0-566">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-567">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="582d0-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-568">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-568">Cost object</span></span></th>
<th><span data-ttu-id="582d0-569">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-569">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-570">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-570">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-571">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-571">Amount</span></span></th>
<th><span data-ttu-id="582d0-572">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-573">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-573">CC003</span></span></td>
<td><span data-ttu-id="582d0-574">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-574">Assembly</span></span></td>
<td><span data-ttu-id="582d0-575">65</span><span class="sxs-lookup"><span data-stu-id="582d0-575">65</span></span></td>
<td><span data-ttu-id="582d0-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="582d0-577">438.75</span><span class="sxs-lookup"><span data-stu-id="582d0-577">438.75</span></span></td>
<td><span data-ttu-id="582d0-578">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-579">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-579">CC004</span></span></td>
<td><span data-ttu-id="582d0-580">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-580">Packaging</span></span></td>
<td><span data-ttu-id="582d0-581">35</span><span class="sxs-lookup"><span data-stu-id="582d0-581">35</span></span></td>
<td><span data-ttu-id="582d0-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="582d0-583">236.25</span><span class="sxs-lookup"><span data-stu-id="582d0-583">236.25</span></span></td>
<td><span data-ttu-id="582d0-584">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-585">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-585">CC003</span></span></td>
<td><span data-ttu-id="582d0-586">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-586">Assembly</span></span></td>
<td><span data-ttu-id="582d0-587">65</span><span class="sxs-lookup"><span data-stu-id="582d0-587">65</span></span></td>
<td><span data-ttu-id="582d0-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="582d0-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="582d0-589">5,297.69</span></span></td>
<td><span data-ttu-id="582d0-590">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-591">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-591">CC004</span></span></td>
<td><span data-ttu-id="582d0-592">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-592">Packaging</span></span></td>
<td><span data-ttu-id="582d0-593">35</span><span class="sxs-lookup"><span data-stu-id="582d0-593">35</span></span></td>
<td><span data-ttu-id="582d0-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="582d0-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="582d0-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="582d0-595">2,852.60</span></span></td>
<td><span data-ttu-id="582d0-596">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-597">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="582d0-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-598">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-598">Cost object</span></span></th>
<th><span data-ttu-id="582d0-599">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-599">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-600">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-600">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-601">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-601">Amount</span></span></th>
<th><span data-ttu-id="582d0-602">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-603">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-603">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-604">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-604">Product 1</span></span></td>
<td><span data-ttu-id="582d0-605">60</span><span class="sxs-lookup"><span data-stu-id="582d0-605">60</span></span></td>
<td><span data-ttu-id="582d0-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="582d0-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="582d0-607">535.31</span><span class="sxs-lookup"><span data-stu-id="582d0-607">535.31</span></span></td>
<td><span data-ttu-id="582d0-608">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-609">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-609">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-610">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-610">Product 2</span></span></td>
<td><span data-ttu-id="582d0-611">20</span><span class="sxs-lookup"><span data-stu-id="582d0-611">20</span></span></td>
<td><span data-ttu-id="582d0-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="582d0-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="582d0-613">178.44</span><span class="sxs-lookup"><span data-stu-id="582d0-613">178.44</span></span></td>
<td><span data-ttu-id="582d0-614">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-615">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-615">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-616">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-616">Product 1</span></span></td>
<td><span data-ttu-id="582d0-617">60</span><span class="sxs-lookup"><span data-stu-id="582d0-617">60</span></span></td>
<td><span data-ttu-id="582d0-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="582d0-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="582d0-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="582d0-619">4,487.12</span></span></td>
<td><span data-ttu-id="582d0-620">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-621">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-621">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-622">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-622">Product 2</span></span></td>
<td><span data-ttu-id="582d0-623">20</span><span class="sxs-lookup"><span data-stu-id="582d0-623">20</span></span></td>
<td><span data-ttu-id="582d0-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="582d0-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="582d0-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="582d0-625">1,495.71</span></span></td>
<td><span data-ttu-id="582d0-626">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="582d0-627">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="582d0-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-628">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-628">Cost object</span></span></th>
<th><span data-ttu-id="582d0-629">Величина</span><span class="sxs-lookup"><span data-stu-id="582d0-629">Magnitude</span></span></th>
<th><span data-ttu-id="582d0-630">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="582d0-630">Allocation factor</span></span></th>
<th><span data-ttu-id="582d0-631">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-631">Amount</span></span></th>
<th><span data-ttu-id="582d0-632">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-633">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-633">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-634">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-634">Product 1</span></span></td>
<td><span data-ttu-id="582d0-635">80</span><span class="sxs-lookup"><span data-stu-id="582d0-635">80</span></span></td>
<td><span data-ttu-id="582d0-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="582d0-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="582d0-637">241.05</span><span class="sxs-lookup"><span data-stu-id="582d0-637">241.05</span></span></td>
<td><span data-ttu-id="582d0-638">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-639">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-639">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-640">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-640">Product 2</span></span></td>
<td><span data-ttu-id="582d0-641">15</span><span class="sxs-lookup"><span data-stu-id="582d0-641">15</span></span></td>
<td><span data-ttu-id="582d0-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="582d0-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="582d0-643">45.20</span><span class="sxs-lookup"><span data-stu-id="582d0-643">45.20</span></span></td>
<td><span data-ttu-id="582d0-644">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-645">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-645">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-646">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-646">Product 1</span></span></td>
<td><span data-ttu-id="582d0-647">80</span><span class="sxs-lookup"><span data-stu-id="582d0-647">80</span></span></td>
<td><span data-ttu-id="582d0-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="582d0-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="582d0-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="582d0-649">2,507.09</span></span></td>
<td><span data-ttu-id="582d0-650">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-651">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-651">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-652">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-652">Product 2</span></span></td>
<td><span data-ttu-id="582d0-653">15</span><span class="sxs-lookup"><span data-stu-id="582d0-653">15</span></span></td>
<td><span data-ttu-id="582d0-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="582d0-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="582d0-655">470.08</span><span class="sxs-lookup"><span data-stu-id="582d0-655">470.08</span></span></td>
<td><span data-ttu-id="582d0-656">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="582d0-657">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="582d0-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-658">Журнал</span><span class="sxs-lookup"><span data-stu-id="582d0-658">Journal</span></span></th>
<th><span data-ttu-id="582d0-659">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="582d0-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="582d0-660">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="582d0-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="582d0-661">Версия</span><span class="sxs-lookup"><span data-stu-id="582d0-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-662">00004</span><span class="sxs-lookup"><span data-stu-id="582d0-662">00004</span></span></td>
<td><span data-ttu-id="582d0-663">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="582d0-664">Финансовый</span><span class="sxs-lookup"><span data-stu-id="582d0-664">Fiscal</span></span></td>
<td><span data-ttu-id="582d0-665">2017</span><span class="sxs-lookup"><span data-stu-id="582d0-665">2017</span></span></td>
<td><span data-ttu-id="582d0-666">Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-666">Period 1</span></span></td>
<td><span data-ttu-id="582d0-667">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="582d0-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="582d0-668">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="582d0-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="582d0-669">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-670">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-671">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-671">Cost element</span></span></th>
<th><span data-ttu-id="582d0-672">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-672">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-673">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-674">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-675">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-675">CC001</span></span></td>
<td><span data-ttu-id="582d0-676">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-676">HR</span></span></td>
<td><span data-ttu-id="582d0-677">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-677">10001</span></span></td>
<td><span data-ttu-id="582d0-678">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-678">Electricity</span></span></td>
<td><span data-ttu-id="582d0-679">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-679">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-680">500.00</span><span class="sxs-lookup"><span data-stu-id="582d0-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-681">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-682">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-682">CC001</span></span></td>
<td><span data-ttu-id="582d0-683">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-683">HR</span></span></td>
<td><span data-ttu-id="582d0-684">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-684">10001</span></span></td>
<td><span data-ttu-id="582d0-685">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-685">Electricity</span></span></td>
<td><span data-ttu-id="582d0-686">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-686">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="582d0-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-688">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-689">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-689">CC002</span></span></td>
<td><span data-ttu-id="582d0-690">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-690">Finance</span></span></td>
<td><span data-ttu-id="582d0-691">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-691">10001</span></span></td>
<td><span data-ttu-id="582d0-692">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-692">Electricity</span></span></td>
<td><span data-ttu-id="582d0-693">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-693">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-694">675.00</span><span class="sxs-lookup"><span data-stu-id="582d0-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-695">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-696">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-696">CC002</span></span></td>
<td><span data-ttu-id="582d0-697">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-697">Finance</span></span></td>
<td><span data-ttu-id="582d0-698">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-698">10001</span></span></td>
<td><span data-ttu-id="582d0-699">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-699">Electricity</span></span></td>
<td><span data-ttu-id="582d0-700">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-700">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="582d0-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-702">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-703">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-703">CC003</span></span></td>
<td><span data-ttu-id="582d0-704">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-704">Assembly</span></span></td>
<td><span data-ttu-id="582d0-705">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-705">10001</span></span></td>
<td><span data-ttu-id="582d0-706">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-706">Electricity</span></span></td>
<td><span data-ttu-id="582d0-707">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-707">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-708">713.75</span><span class="sxs-lookup"><span data-stu-id="582d0-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-709">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-710">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-710">CC003</span></span></td>
<td><span data-ttu-id="582d0-711">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-711">Assembly</span></span></td>
<td><span data-ttu-id="582d0-712">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-712">10001</span></span></td>
<td><span data-ttu-id="582d0-713">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-713">Electricity</span></span></td>
<td><span data-ttu-id="582d0-714">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-714">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="582d0-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-716">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-717">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-717">CC003</span></span></td>
<td><span data-ttu-id="582d0-718">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-718">Packaging</span></span></td>
<td><span data-ttu-id="582d0-719">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-719">10001</span></span></td>
<td><span data-ttu-id="582d0-720">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-720">Electricity</span></span></td>
<td><span data-ttu-id="582d0-721">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-721">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-722">286.25</span><span class="sxs-lookup"><span data-stu-id="582d0-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-723">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-724">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-724">CC003</span></span></td>
<td><span data-ttu-id="582d0-725">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-725">Packaging</span></span></td>
<td><span data-ttu-id="582d0-726">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-726">10001</span></span></td>
<td><span data-ttu-id="582d0-727">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-727">Electricity</span></span></td>
<td><span data-ttu-id="582d0-728">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-728">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="582d0-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-730">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-731">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-731">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-732">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-732">Product 1</span></span></td>
<td><span data-ttu-id="582d0-733">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-733">10001</span></span></td>
<td><span data-ttu-id="582d0-734">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-734">Electricity</span></span></td>
<td><span data-ttu-id="582d0-735">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-735">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-736">776.36</span><span class="sxs-lookup"><span data-stu-id="582d0-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-737">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-738">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-738">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-739">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-739">Product 1</span></span></td>
<td><span data-ttu-id="582d0-740">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-740">10001</span></span></td>
<td><span data-ttu-id="582d0-741">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-741">Electricity</span></span></td>
<td><span data-ttu-id="582d0-742">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-742">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="582d0-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-744">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-745">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-745">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-746">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-746">Product 1</span></span></td>
<td><span data-ttu-id="582d0-747">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-747">10001</span></span></td>
<td><span data-ttu-id="582d0-748">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-748">Electricity</span></span></td>
<td><span data-ttu-id="582d0-749">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-749">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-750">223.64</span><span class="sxs-lookup"><span data-stu-id="582d0-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-751">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="582d0-752">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-752">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-753">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-753">Product 1</span></span></td>
<td><span data-ttu-id="582d0-754">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-754">10001</span></span></td>
<td><span data-ttu-id="582d0-755">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-755">Electricity</span></span></td>
<td><span data-ttu-id="582d0-756">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-756">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="582d0-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="582d0-758">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="582d0-759">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="582d0-760">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-760">Cost element</span></span></th>
<th><span data-ttu-id="582d0-761">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-761">Cost behavior</span></span></th>
<th><span data-ttu-id="582d0-762">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="582d0-762">Amount</span></span></th>
<th><span data-ttu-id="582d0-763">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="582d0-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="582d0-764">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-764">CC001</span></span></td>
<td><span data-ttu-id="582d0-765">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-765">HR</span></span></td>
<td><span data-ttu-id="582d0-766">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-766">10001</span></span></td>
<td><span data-ttu-id="582d0-767">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-767">Electricity</span></span></td>
<td><span data-ttu-id="582d0-768">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-768">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="582d0-769">-500.00</span></span></td>
<td><span data-ttu-id="582d0-770">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-771">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-771">CC002</span></span></td>
<td><span data-ttu-id="582d0-772">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-772">Finance</span></span></td>
<td><span data-ttu-id="582d0-773">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-773">10001</span></span></td>
<td><span data-ttu-id="582d0-774">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-774">Electricity</span></span></td>
<td><span data-ttu-id="582d0-775">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-775">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-776">175.00</span><span class="sxs-lookup"><span data-stu-id="582d0-776">175.00</span></span></td>
<td><span data-ttu-id="582d0-777">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-778">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-778">CC003</span></span></td>
<td><span data-ttu-id="582d0-779">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-779">Assembly</span></span></td>
<td><span data-ttu-id="582d0-780">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-780">10001</span></span></td>
<td><span data-ttu-id="582d0-781">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-781">Electricity</span></span></td>
<td><span data-ttu-id="582d0-782">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-782">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-783">275.00</span><span class="sxs-lookup"><span data-stu-id="582d0-783">275.00</span></span></td>
<td><span data-ttu-id="582d0-784">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-785">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-785">CC004</span></span></td>
<td><span data-ttu-id="582d0-786">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-786">Packaging</span></span></td>
<td><span data-ttu-id="582d0-787">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-787">10001</span></span></td>
<td><span data-ttu-id="582d0-788">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-788">Electricity</span></span></td>
<td><span data-ttu-id="582d0-789">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-789">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-790">50,00</span><span class="sxs-lookup"><span data-stu-id="582d0-790">50,00</span></span></td>
<td><span data-ttu-id="582d0-791">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-792">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-792">CC001</span></span></td>
<td><span data-ttu-id="582d0-793">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="582d0-793">HR</span></span></td>
<td><span data-ttu-id="582d0-794">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-794">10001</span></span></td>
<td><span data-ttu-id="582d0-795">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-795">Electricity</span></span></td>
<td><span data-ttu-id="582d0-796">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-796">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-797">-1245,71</span><span class="sxs-lookup"><span data-stu-id="582d0-797">-1,245.71</span></span></td>
<td><span data-ttu-id="582d0-798">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-799">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-799">CC002</span></span></td>
<td><span data-ttu-id="582d0-800">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-800">Finance</span></span></td>
<td><span data-ttu-id="582d0-801">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-801">10001</span></span></td>
<td><span data-ttu-id="582d0-802">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-802">Electricity</span></span></td>
<td><span data-ttu-id="582d0-803">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-803">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-804">436.00</span><span class="sxs-lookup"><span data-stu-id="582d0-804">436.00</span></span></td>
<td><span data-ttu-id="582d0-805">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-806">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-806">CC003</span></span></td>
<td><span data-ttu-id="582d0-807">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-807">Assembly</span></span></td>
<td><span data-ttu-id="582d0-808">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-808">10001</span></span></td>
<td><span data-ttu-id="582d0-809">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-809">Electricity</span></span></td>
<td><span data-ttu-id="582d0-810">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-810">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-811">685.14</span><span class="sxs-lookup"><span data-stu-id="582d0-811">685.14</span></span></td>
<td><span data-ttu-id="582d0-812">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-813">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-813">CC004</span></span></td>
<td><span data-ttu-id="582d0-814">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-814">Packaging</span></span></td>
<td><span data-ttu-id="582d0-815">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-815">10001</span></span></td>
<td><span data-ttu-id="582d0-816">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-816">Electricity</span></span></td>
<td><span data-ttu-id="582d0-817">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-817">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-818">124.57</span><span class="sxs-lookup"><span data-stu-id="582d0-818">124.57</span></span></td>
<td><span data-ttu-id="582d0-819">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-820">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-820">CC002</span></span></td>
<td><span data-ttu-id="582d0-821">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-821">Finance</span></span></td>
<td><span data-ttu-id="582d0-822">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-822">10001</span></span></td>
<td><span data-ttu-id="582d0-823">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-823">Electricity</span></span></td>
<td><span data-ttu-id="582d0-824">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-824">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="582d0-825">-675.00</span></span></td>
<td><span data-ttu-id="582d0-826">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-827">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-827">CC003</span></span></td>
<td><span data-ttu-id="582d0-828">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-828">Assembly</span></span></td>
<td><span data-ttu-id="582d0-829">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-829">10001</span></span></td>
<td><span data-ttu-id="582d0-830">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-830">Electricity</span></span></td>
<td><span data-ttu-id="582d0-831">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-831">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-832">438.75</span><span class="sxs-lookup"><span data-stu-id="582d0-832">438.75</span></span></td>
<td><span data-ttu-id="582d0-833">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-834">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-834">CC004</span></span></td>
<td><span data-ttu-id="582d0-835">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-835">Packaging</span></span></td>
<td><span data-ttu-id="582d0-836">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-836">10001</span></span></td>
<td><span data-ttu-id="582d0-837">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-837">Electricity</span></span></td>
<td><span data-ttu-id="582d0-838">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-838">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-839">236.25</span><span class="sxs-lookup"><span data-stu-id="582d0-839">236.25</span></span></td>
<td><span data-ttu-id="582d0-840">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-841">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-841">CC002</span></span></td>
<td><span data-ttu-id="582d0-842">Финансы</span><span class="sxs-lookup"><span data-stu-id="582d0-842">Finance</span></span></td>
<td><span data-ttu-id="582d0-843">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-843">10001</span></span></td>
<td><span data-ttu-id="582d0-844">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-844">Electricity</span></span></td>
<td><span data-ttu-id="582d0-845">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-845">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-846">-8150,29</span><span class="sxs-lookup"><span data-stu-id="582d0-846">-8,150.29</span></span></td>
<td><span data-ttu-id="582d0-847">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-848">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-848">CC003</span></span></td>
<td><span data-ttu-id="582d0-849">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-849">Assembly</span></span></td>
<td><span data-ttu-id="582d0-850">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-850">10001</span></span></td>
<td><span data-ttu-id="582d0-851">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-851">Electricity</span></span></td>
<td><span data-ttu-id="582d0-852">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-852">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="582d0-853">5,297.69</span></span></td>
<td><span data-ttu-id="582d0-854">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-855">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-855">CC004</span></span></td>
<td><span data-ttu-id="582d0-856">Упаковка</span><span class="sxs-lookup"><span data-stu-id="582d0-856">Packaging</span></span></td>
<td><span data-ttu-id="582d0-857">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-857">10001</span></span></td>
<td><span data-ttu-id="582d0-858">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-858">Electricity</span></span></td>
<td><span data-ttu-id="582d0-859">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-859">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="582d0-860">2,852.60</span></span></td>
<td><span data-ttu-id="582d0-861">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-862">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-862">CC003</span></span></td>
<td><span data-ttu-id="582d0-863">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-863">Assembly</span></span></td>
<td><span data-ttu-id="582d0-864">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-864">10001</span></span></td>
<td><span data-ttu-id="582d0-865">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-865">Electricity</span></span></td>
<td><span data-ttu-id="582d0-866">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-866">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="582d0-867">-713.75</span></span></td>
<td><span data-ttu-id="582d0-868">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-869">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-869">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-870">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-870">Product 1</span></span></td>
<td><span data-ttu-id="582d0-871">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-871">10001</span></span></td>
<td><span data-ttu-id="582d0-872">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-872">Electricity</span></span></td>
<td><span data-ttu-id="582d0-873">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-873">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-874">535.31</span><span class="sxs-lookup"><span data-stu-id="582d0-874">535.31</span></span></td>
<td><span data-ttu-id="582d0-875">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-876">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-876">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-877">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-877">Product 2</span></span></td>
<td><span data-ttu-id="582d0-878">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-878">10001</span></span></td>
<td><span data-ttu-id="582d0-879">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-879">Electricity</span></span></td>
<td><span data-ttu-id="582d0-880">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-880">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-881">178.44</span><span class="sxs-lookup"><span data-stu-id="582d0-881">178.44</span></span></td>
<td><span data-ttu-id="582d0-882">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-883">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-883">CC003</span></span></td>
<td><span data-ttu-id="582d0-884">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-884">Assembly</span></span></td>
<td><span data-ttu-id="582d0-885">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-885">10001</span></span></td>
<td><span data-ttu-id="582d0-886">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-886">Electricity</span></span></td>
<td><span data-ttu-id="582d0-887">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-887">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-888">-5982,83</span><span class="sxs-lookup"><span data-stu-id="582d0-888">-5,982.83</span></span></td>
<td><span data-ttu-id="582d0-889">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-890">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-890">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-891">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-891">Product 1</span></span></td>
<td><span data-ttu-id="582d0-892">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-892">10001</span></span></td>
<td><span data-ttu-id="582d0-893">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-893">Electricity</span></span></td>
<td><span data-ttu-id="582d0-894">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-894">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="582d0-895">4,487.12</span></span></td>
<td><span data-ttu-id="582d0-896">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-897">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-897">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-898">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-898">Product 2</span></span></td>
<td><span data-ttu-id="582d0-899">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-899">10001</span></span></td>
<td><span data-ttu-id="582d0-900">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-900">Electricity</span></span></td>
<td><span data-ttu-id="582d0-901">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-901">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="582d0-902">1,495.71</span></span></td>
<td><span data-ttu-id="582d0-903">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-904">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-904">CC003</span></span></td>
<td><span data-ttu-id="582d0-905">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-905">Assembly</span></span></td>
<td><span data-ttu-id="582d0-906">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-906">10001</span></span></td>
<td><span data-ttu-id="582d0-907">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-907">Electricity</span></span></td>
<td><span data-ttu-id="582d0-908">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-908">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="582d0-909">-286.25</span></span></td>
<td><span data-ttu-id="582d0-910">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-911">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-911">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-912">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-912">Product 1</span></span></td>
<td><span data-ttu-id="582d0-913">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-913">10001</span></span></td>
<td><span data-ttu-id="582d0-914">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-914">Electricity</span></span></td>
<td><span data-ttu-id="582d0-915">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-915">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-916">241.05</span><span class="sxs-lookup"><span data-stu-id="582d0-916">241.05</span></span></td>
<td><span data-ttu-id="582d0-917">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-918">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-918">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-919">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-919">Product 2</span></span></td>
<td><span data-ttu-id="582d0-920">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-920">10001</span></span></td>
<td><span data-ttu-id="582d0-921">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-921">Electricity</span></span></td>
<td><span data-ttu-id="582d0-922">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-922">Fixed cost</span></span></td>
<td><span data-ttu-id="582d0-923">45.20</span><span class="sxs-lookup"><span data-stu-id="582d0-923">45.20</span></span></td>
<td><span data-ttu-id="582d0-924">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-925">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-925">CC003</span></span></td>
<td><span data-ttu-id="582d0-926">Сборка</span><span class="sxs-lookup"><span data-stu-id="582d0-926">Assembly</span></span></td>
<td><span data-ttu-id="582d0-927">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-927">10001</span></span></td>
<td><span data-ttu-id="582d0-928">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-928">Electricity</span></span></td>
<td><span data-ttu-id="582d0-929">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-929">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="582d0-930">-2,977.17</span></span></td>
<td><span data-ttu-id="582d0-931">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-932">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-932">Prod 1</span></span></td>
<td><span data-ttu-id="582d0-933">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="582d0-933">Product 1</span></span></td>
<td><span data-ttu-id="582d0-934">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-934">10001</span></span></td>
<td><span data-ttu-id="582d0-935">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-935">Electricity</span></span></td>
<td><span data-ttu-id="582d0-936">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-936">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="582d0-937">2,507.09</span></span></td>
<td><span data-ttu-id="582d0-938">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="582d0-939">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-939">Prod 2</span></span></td>
<td><span data-ttu-id="582d0-940">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="582d0-940">Product 2</span></span></td>
<td><span data-ttu-id="582d0-941">10001</span><span class="sxs-lookup"><span data-stu-id="582d0-941">10001</span></span></td>
<td><span data-ttu-id="582d0-942">Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-942">Electricity</span></span></td>
<td><span data-ttu-id="582d0-943">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-943">Variable cost</span></span></td>
<td><span data-ttu-id="582d0-944">470.08</span><span class="sxs-lookup"><span data-stu-id="582d0-944">470.08</span></span></td>
<td><span data-ttu-id="582d0-945">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="582d0-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="582d0-946">Заключение</span><span class="sxs-lookup"><span data-stu-id="582d0-946">Conclusion</span></span>
<span data-ttu-id="582d0-947">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="582d0-948">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="582d0-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="582d0-949">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="582d0-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="582d0-950">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="582d0-951">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="582d0-952">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="582d0-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="582d0-953">Итоговый</span><span class="sxs-lookup"><span data-stu-id="582d0-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="582d0-954">CC099</span><span class="sxs-lookup"><span data-stu-id="582d0-954">CC099</span></span></th>
<th><span data-ttu-id="582d0-955">CC001</span><span class="sxs-lookup"><span data-stu-id="582d0-955">CC001</span></span></th>
<th><span data-ttu-id="582d0-956">CC002</span><span class="sxs-lookup"><span data-stu-id="582d0-956">CC002</span></span></th>
<th><span data-ttu-id="582d0-957">CC003</span><span class="sxs-lookup"><span data-stu-id="582d0-957">CC003</span></span></th>
<th><span data-ttu-id="582d0-958">CC004</span><span class="sxs-lookup"><span data-stu-id="582d0-958">CC004</span></span></th>
<th><span data-ttu-id="582d0-959">Проект 1</span><span class="sxs-lookup"><span data-stu-id="582d0-959">Proj 1</span></span></th>
<th><span data-ttu-id="582d0-960">Проект 2</span><span class="sxs-lookup"><span data-stu-id="582d0-960">Proj 2</span></span></th>
<th><span data-ttu-id="582d0-961">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="582d0-961">Prod 1</span></span></th>
<th><span data-ttu-id="582d0-962">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="582d0-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="582d0-963">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="582d0-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="582d0-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="582d0-973">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="582d0-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-974">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="582d0-975">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-976">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-977">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-978">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-979">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-980">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="582d0-981">776.36</span><span class="sxs-lookup"><span data-stu-id="582d0-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-982">223.64</span><span class="sxs-lookup"><span data-stu-id="582d0-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="582d0-984">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="582d0-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-985">000</span><span class="sxs-lookup"><span data-stu-id="582d0-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-986">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-987">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-988">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-989">0,00</span><span class="sxs-lookup"><span data-stu-id="582d0-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-990">30.00</span><span class="sxs-lookup"><span data-stu-id="582d0-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-991">10,00</span><span class="sxs-lookup"><span data-stu-id="582d0-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="582d0-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="582d0-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="582d0-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="582d0-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="582d0-995">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="582d0-996">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="582d0-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="582d0-997">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="582d0-998">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="582d0-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="582d0-999">Для получения дополнительных сведений см. политику свертки затрат.</span><span class="sxs-lookup"><span data-stu-id="582d0-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="582d0-1000">(Обратите внимание, что этот раздел еще не завершен, но появится в ближайшее время.)</span><span class="sxs-lookup"><span data-stu-id="582d0-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




